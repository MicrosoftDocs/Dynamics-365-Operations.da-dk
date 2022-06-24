---
title: Procesvejledningsstruktur
description: Denne artikel indeholder oplysninger om procesvejledningsstruktur til udviklere, der udvider vores mobilprocesser for lagersteder i X++.
author: Mirzaab
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e88f32e0347a808d03615cf85e50b1592d691670
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860429"
---
# <a name="process-guide-framework"></a>Procesvejledningsstruktur

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om procesvejledningsstruktur til udviklere, der udvider mobilprocesserne for lagersteder i X++. Mobilprocesserne for lagerstedet kan udvides, fordi processerne opdeles i små trin. Forretningslogikken og opbygningen af brugergrænsefladen for hvert trin er blevet udtrækket til individuelle klasser, hvilket gør det muligt at udvide dem.

## <a name="overview-of-the-existing-design"></a>Oversigt over det eksisterende design

De mobile kørselsflow for lagersteder udsættes via et enkelt brugerdefineret tjenesteslutpunkt. Anmodningen ankommer fra mobilappen i form af en XML-streng, som indeholder metadataene fra den brugergrænseflade, der er vist i mobilappen, samt de værdier, som brugeren har angivet.

Når anmodningen modtages, er det første trin at deserialisere denne XML. Klassen **WHSMobileAppServiceXMLTranslator** konverterer XML'en til en container, som indeholder både kontroloplysninger og sessionsoplysninger.

Derefter bruges oplysningerne i containeren til at aflede, hvilken lagerstedsproces brugeren arbejder på, eller skal til at starte (repræsenteret af fastteksten **WHSWorkExecuteMode**), og dermed instantiere den afledte klasse **WHSWorkExecuteDisplay**. Metoden **displayform()** aktiveres og gør derefter følgende:

-   Behandler dataene fra brugeren (delegeret til **WHSRFControlData**-klassen, men nogle processer implementerer specifik logik ved at tilsidesætte **processControl()**-metoden).

-   Udfører forretningslogik.

-   Øger trinnet.

-   Bygger den container, der repræsenterer den nye brugergrænseflade (typisk i en **build... ()**-metode).

Containeren returneres derefter til oversætteren, hvorefter XML-dokumentet serialiseres og sendes tilbage som svar til mobilenheden.

I følgende sekvensdiagram vises en oversigt over kørselsflowet. Bemærk, at diagrammet nærmest er en skemaisk oversigt og ikke er en 1:1-repræsentation af den faktiske kode.

![Skematisk oversigt over processen.](media/schematic-overview.png) 

### <a name="reason-for-the-redesign"></a>Årsag til det nye design

Ovennævnte design giver en meget simpel struktur for at bygge processer, der bruges i mobile flow. Som det fremgår af ovenstående, tager **displayform()**-metoderne dog flere ansvarsområder. Den delegerer dem til andre metoder og klasser, men hvis der ikke er konkrete klasseansvarsområder, sker det på en uoverensstemmende måde på tværs af klasserne. Og da antallet af understøttede scenarier vokser organisk, kan nogle af disse klasser blive ret komplekse. For at gøre tingene mere interessant tilsidesættes nogle af disse klasser/metoder og genbruges i flere tilstande. Resultatet er meget lange metoder med høj cyklomatisk kompleksitet. Disse har tidligere voldt vedligeholdelsesproblemer. Det har været risiko og mulig tilbagefald forbundet med at rette fejl i disse metoder.
Der henvises for eksempel til metoden **processWorkLine** i klassen **WhsWorkExecuteDisplay** fra flere processer (stort set alle steder, hvor der udføres arbejde).

Hvis disse skal kunne udvides, kan du vælge at opdele **displayForm**-metoderne i mindre metoder og indføre udvidelsespunkter. Men på grund af scenariomatrixen vil det dog være udfordrende for partnere at skrive udvidelser og validere dem i forhold til tilbagefald. Ikke blot vil koden – på grund af den manglende distribution af struktureret ansvarlighed som nævnt ovenfor – blive ved med at blive stadigt større på uforudsigelige måder over tid, hvilket udgør en udfordring i forbindelse med opbygning af kvalitetsudvidelser.

Dette medfører, at det nye design er den bæredygtige mulighed med det mål at have klart definerede klasser, der har uafhængige ansvarsområder. En klasse skal have ét ansvarsområde, én årsag til at ændre sig og én årsag til at blive udvidet.

## <a name="design-overview"></a>Designoversigt

I den ændrede struktur er kernestrategien baseret på to principper: opdeling af udførelsesflowet i individuelle komponenter med veldefinerede ansvarsområder og anvendelse af veldefinerede udvidelsespunkter i hver af komponenterne.

Navnet på den nye struktur er "ProcessGuide". Det skyldes, at formålet med disse klasser er at føre en bruger gennem en forretningsproces (i modsætning til den omfattende klient, der er en formularbaseret oplevelse, hvor brugeren har større fleksibilitet i den måde, brugeren arbejder med dataene på, eller i den rækkefølge, opgaver udføres på).

> [!NOTE]
> En væsentlig detalje er den bevidste udeladelse af præfikset "WHS". Da de mobile processer oprindeligt blev introduceret i forbindelse med lagerstyring, har de efterfølgende brudt grænser og understøtter nu forskellige processer til produktions- og lagerstyring. Som følge heraf var lagerstedsreferencen udeladt i navnet på strukturen.

Når du skal identificere komponenterne, skal du som det første se på processen Produktionsstart (klassen **WhsWorkExecuteDisplayProdStart**). Her er en skematisk oversigt over processen.

![Billede af skematisk proces.](media/production-start-process-schematic.png)

I forbindelse med kontrolflowet er følgende komponenter nødvendige:

-   En controller, der skal stykke hele forretningsprocessen sammen.
-   Et trin, der er ansvarlig for udførelsen af et trin i processen.
-   En dataprocessor til behandling af dataene i et trin.
-   En sidegenerator, der er ansvarlig for at opbygge brugergrænsefladen for et trin.
-   En navigationsagent, der er ansvarlig for trinovergangen.
-   En klasse, der er ansvarlig for at udføre forretningsprocessen.

Hvis du starter med trin 1 i diagrammet med procesflowet ovenfor og begynder at behandle dataene fra det forrige trin og derefter slutter med at opbygge en brugergrænseflade, vil data fortsat blive behandlet i næste trin. Dette skaber en tæt kobling mellem fortløbende trin, og derfor vil vores nye skematiske proces på højt niveau ser sådan ud:

![Billede af skematisk proces på højt niveau.](media/high-level-schematic.png)

De følgende er de vigtigste komponenter i den ændrede proces:

-   **ProcessGuideController** – Denne klasse orkestrerer den overordnede udførelse af forretningsprocessen. Den definerer de fabrikker, der instantierer trinnet, og den navigationsagent, der efterfølgende udgør procesudførelsen, samt oprydningslogikken for annullering eller afslutning af processen.

-   **ProcessGuideStep** – Denne klasse repræsenterer ét enkelt trin i forretningsprocessen. Denne klasse indeholder en definition på de fabrikker, der instantierer en sidegenerator, handlinger og dataprocessorer og er ansvarlig for at starte dem i den rette rækkefølge.

-   **ProcessGuideNavigationAgent** – Denne klasse er ansvarlig for navigering mellem trinene. Når et trin er udført, er navigationsagenten ansvarlig for at definere det næste trin og overfører eventuelle parametre, som det foregående trin muligvis skal bruge for at kommunikere, til det næste.

-   **ProcessGuidePageBuilder** – Denne klasse er ansvarlig for at instantiere brugergrænsefladen.

-   **ProcessGuideAction** – Denne klasse repræsenterer en handling, der vises som en knap for brugeren.

-   **ProcessGuideDataProcessor** – Denne klasse er ansvarlig for behandling af de data, brugeren har angivet i et felt.

## <a name="execution-flow"></a>Udførelsesflow

Udgangspunktet for udførelsesflowet forbliver uændret. Derfor ankommer anmodningen stadig via de samme slutpunkter, efterfulgt af deserialisering af XML'en til containeren. Denne container overføres derefter til **getNextFormState()**.

Der er tre vigtige klasser, som du skal bemærke:

-  **ProcessGuideSessionState** – Den indeholder oplysninger om sessionstilstand – tilstand, overførsel, controller og trin, der udføres, osv.

-  **ProcessGuidePage** – Den indeholder en typesikker repræsentation af metadataene til brugergrænsefladen.

-  **ProcessGuideRequest** – Den indeholder ovennævnte to som medlemmer og er en typesikker repræsentation af den anmodning, der er modtaget fra mobilenheden.

Disse klasser oprettes ved hjælp af containeroplysningerne (både de tilstands- og brugerdata, der er angivet for kontrolelementet). Dette giver en typesikker måde at få adgang til og manipulere værdierne på. Sammenlignet med gentaget adgang til containeren i løbet af processen giver dette både fordelen af bedre læsbarhed og ydeevne.

Oplysningerne om sessionstilstanden bruges til at instantiere den korrekte **ProcessGuideController**-klasse. Når den er instantieret, aktiveres metoden **createResponse()** i klassen **ProcessGuideController**. Denne metode er indgangspunktet for logikken for procesvejledningen, og når den er kørt, kommer den tilbage med svaret (der repræsenteres i klassen **ProcessGuideResponse**). Derefter konverteres svaret tilbage til containeren og sendes tilbage til den ældre logik, hvorefter det serialiseres til XML og sendes tilbage til mobilenheden.

Derefter skal controlleren finde det næste trin, der skal udføres. Hvis dette er starten på en ny proces, vil controlleren kalde **initialStep()** for at hente det første trin i processen. Derefter kalder den metoden **execute()** i **ProcessGuideStep**. Denne metode instantierer derefter en **ProcessGuidePageBuilder**-klasse og kalder **buildPage()**, som vender tilbage med et **ProcessGuidePage**-objekt, som er en virtuel repræsentation af den brugergrænseflade, som brugeren skal kunne se. Derefter sender trinnet resultatet tilbage til controlleren, som gemmer den aktuelle sessions tilstand, hvorefter resultatet sendes tilbage til **getNextFormState()** i formularen for klassen **ProcessGuideResponse**. Derefter konverteres svaret tilbage til containeren og serialiseres efterfølgende til XML, og svaret sendes tilbage til mobilenheden.

I følgende sekvensdiagram forklares dette kontrolflow. Bemærk, at dette er det mest almindelige kontrolflow, og det er en forenklet beskrivelse af designet.

![Forenklet kontrolflow.](media/control-flow.png)

Når brugeren udfører en handling på mobilenheden ved at klikke på en knap (eller scanne en værdi – som typisk udløser standardhandlingen) – modtages anmodningen ved metoden **createResponse()** i klassen **ProcessGuideController** via den samme rute. Men denne gang ved controlleren, hvilket trin brugeren er i, på grund af sessionstilstanden. Den instantierer derefter den relevante **ProcessGuideStep**-klasse og aktiverer udførelsesmetoden. **ProcessGuideStep** læser derefter det handlingsnavn, som brugeren har startet, og instantierer derefter den relevante **ProcessGuideAction**-klasse og kalder **execute()**.

Klassen **ProcessGuideAction** er ansvarlig for at udføre den specifikke handling, men der er to undtagelser, du skal lægge mærke til.

Den første er **ProcessGuideOKAction**-klassen. Denne handling angiver, at brugeren ønsker at bekræfte og gå videre i processen. I overensstemmelse med dette – denne metode foretager faktisk et tilbagekald til ProcessGuideStep-klassen, hvilket betyder, at trinnet aktiverer **processData()** i **ProcessGuideDataProcessor**. Derved behandles de data, som brugeren har angivet, og trinnets tilstand opdateres derefter, og resultatet sendes tilbage til controlleren. Afhængigt af resultatet af processoren aktiverer trinnet sidegeneratoren for at opbygge den relevante brugergrænseflade, eller status for trinnet angives som fuldført. Dette afspejles i den øverste halvdel af sekvensdiagrammet nedenfor.

Den anden undtagelse er annulleringshandlingen, der er implementeret i klasserne **ProcessGuideCancelResetProcessAction** og **ProcessGuideCancelExitProcessAction**. Disse handlinger repræsenterer en hensigt om at annullere processen og enten vende tilbage til starten af processen eller helt afslutte processen. På samme måde som med handlingen **OK** udfører disse handlinger også et tilbagekald til trinnet, der signalerer hensigten til **ProcessGuideController**. Controlleren udfører derefter den nødvendige oprydning af tilstandsvariabler og flytter enten kontrolelementet til det første trin i processen eller afslutter processen helt.

Når trinnet er fuldført, og trinnets status er angivet til **Fuldført**, instantierer controlleren **ProcessGuideNavigationAgent**, som returnerer navnet på næste trin. Controlleren instantierer derefter dette trin og aktiverer metoden **execute()** – og cyklussen fortsætter. Oftest aktiverer det nye trin den tilsvarende **ProcessGuidePageBuilder** for at bygge brugergrænsefladen for det næste skærmbillede, som skal vises til brugeren, som derefter sendes tilbage. Dette flow vises i den nederste halvdel af sekvensdiagrammet nedenfor.

![sekvensdiagram.](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>Opbygge en ny proces ved hjælp af ProcessGuide-strukturen

Kontrolflowet kan bedst forklares ved hjælp af et eksempel, der findes i programmet – processen Produktionsstart.

## <a name="overview-of-the-production-start-process"></a>Oversigt over processen Produktionsstart

Lad os starte med at forstå procesforløbet. I første trin bliver brugeren bedt om at angive et produktionsordre-id.

![Spørg efter produktions-id.](media/production-id-prompt.png)

Når brugeren angiver produktionsordre-id'et, valideres ordrenummeret. Nogle af de valideringer, der køres, er baseret på, om ordren er på samme lagersted, som brugeren er logget på, og status for ordren. Hvis valideringen mislykkes, får brugeren vist en fejlmeddelelse. Hvis valideringen lykkes, får brugeren vist detaljer om produktionsordren og varen.

Brugeren kan enten annullere for at gå tilbage til starten af processen eller klikke på **OK** for at bekræfte. I det sidstnævnte tilfælde angives produktionsordren til statussen **Igangsat**, de tilsvarende kladder bogføres, kontrolelementet flyttes tilbage til første trin, og brugeren får vist meddelelsen "Arbejde fuldført".


## <a name="creating-the-controller"></a>Oprette controlleren

Det første trin i at opbygge forretningsprocessen er at oprette controllerklassen, som udvides fra den abstrakte **ProcessGuideController**-klasse, der implementerer en controllers standardfunktionsmåde. Det nye klassenavn er **ProdProcessGuideProductionStartController**, og den får **WHSWorkExecuteMode**-værdien **StartProdOrder**. Der bruges samme **SysExtension**-baserede instantiering som den, der blev brugt i **WHSWorkExecuteDisplay**-klasserne, hvilket hjælper med at instantiere controlleren, når brugeren udfører et menupunkt for denne tilstand.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> Klassens navngivningsmønster er **\<FunctionalArea\>ProcessGuide\<Businessprocessname\>Controller**. Det er det mønster, der bruges til controllerklasser og til at udvide til andre klasser.


## <a name="building-the-first-step"></a>Opbygge det første trin

Derefter skal du definere det første trin ved at oprette klassen **ProdProcessGuidePromptProductionIdStep**, der udvides fra **ProcessGuideStep**.

Opgaven med at instantiere klassen uddelegeres til en trinfabrik, som aktiveres af **ProcessGuideController**-basisklassen. Standardimplementeringen af fabrikken instantierer trinnet baseret på navn. Du skal derfor gøre to ting for at instantiere **ProdProcessGuidePromptProductionIdStep** som det første trin i controlleren:

-   Udfyld klassen **ProdProcessGuidePromptProductionIdStep** med en **ProcessGuideStepName**-attribut.

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   Implementer den abstrakte metode **initialStepName()** i controllerklassen for at returnere trinnavnet.

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> Værdien i attributten **ProcessGuideStepName** behøver ikke at svare præcist til klassenavnet som vist ovenfor. Implementering af dette giver dog mulighed for ensartethed og typesikkerhed i forbindelse med krydsreferencer, når klassen bruges. Det anbefales, at du bruger denne navngivningskonvention.
>
> **ProcessGuideStepName**, der er baseret på instantiering af trinnet, implementeres i klassen **ProcessGuideStepDefaultFactory**. I de sjældne tilfælde, hvor du vil anvende en anden strategi til at instantiere trinnet, skal du gøre følgende:
> -   Opret en ny fabriksklasse, der nedarver fra **ProcessGuidStepAbstractFactory**.
> -   Du kan vælge at oprette en ny parameterklasse, der implementerer **ProcessGuideIStepCreationParameters**-grænsefladen, som indeholder de parametre, som fabrikken har brug for.
> -   I controllerklassen skal du tilsidesætte metoderne **stepFactory()** og **stepCreationParameters()** for at returnere ovenstående fabrik og parametre.

Det næste trin er at implementere funktionaliteten i klassen **ProdProcessGuidePromptProductionIdStep**. Du skal implementere logikken for opbygning af brugergrænsefladen, behandling af de brugerindtastede data og fastlæggelse af, hvornår trinnet er fuldført.

### <a name="building-the-user-interface-for-the-first-step"></a>Opbygge brugergrænsefladen til første trin

Brugergrænsefladen opbygges ved hjælp af en klasse arvet fra den abstrakte **ProcessGuidePageBuilder**-klasse. Til dette trin skal du navngive klassen, så den repræsenterer det, den gør – **ProdProcessGuidePromptProductionIdPageBuilder**.

Instantieringsmekanismen for klassen svarer til, hvordan trinnet blev instantieret fra controlleren. 

-   Udfyld klassen **ProdProcessGuidePromptProductionIdPageBuilder** med en **ProcessGuidePageBuilderName**-attribut.

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   I klassen **ProdProcessGuidePromptProductionIdStep** skal du implementere den abstrakte metode **pageBuilderName()** for at returnere dette navn.

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> På samme måde som ved trinfabrikken findes der også et abstrakt fabriksmønster, der er implementeret for sidegeneratorfabrikken. Så i de sjældne tilfælde, hvor du vil anvende en anden strategi til at instantiere sidegeneratoren, kan du gøre følgende:
> - Opret en ny fabriksklasse, der nedarver fra **ProcessGuidePageBuilderAbstractFactory**.
> - Du kan vælge at oprette en ny parameterklasse, der implementerer **ProcessGuideIPageBuilderCreationParameters**-grænsefladen, som indeholder de parametre, som fabrikken har brug for.
> - I trinklassen skal du tilsidesætte metoderne **pageBuilderFactory()** og **pageBuilderCreationParameters()** for at returnere ovenstående fabrik og parametre.

For at kunne implementere brugergrænsefladen skal du bruge en side med ét tekstfelt til indtastning af produktionsordre-id'et samt en **OK**-knap og en **Annuller**-knap. Knappen **Annuller** skal afslutte processen.

Dette kan kun implementeres, hvis du tilsidesætter to metoder i klassen **ProdProcessGuidePromptProductionIdPageBuilder**:

-   Brug metoden **addDataControls()** til at tilføje tekstfeltet.

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   Brug metoden **addActionControls()** til at tilføje knapperne **OK** og **Annuller**.

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

På denne måde tilføjes datakontrolelementerne efterfulgt af knapperne. Men hvis du vil bygge en skærm med indbyrdes forbundne datakontrolelementer og knapper, kan du tilsidesætte **addControls()**-metoden i stedet for fleksibilitet.

Et andet scenarie, du kan overveje, er, hvordan du kan gendanne siden i tilfælde af valideringsfejl, for eksempel hvis brugeren angiver et forkert produktionsordre-id. **ProcessGuidePageBuilder**-basisklassen implementerer standardfunktionsmåden, som gendanner brugergrænsefladen, fjerner den scannede værdi og tilføjer fejlkontrollen med fejlmeddelelsen. Da dette er den standardfunktionsmåde, du vil bruge, behøver du ikke tilføje kode for håndtering af fejl.

> [!TIP]
> Hvis du vil implementere en brugerdefineret funktionsmåde for brugergrænsefladen til fejlsituationer, kan du tilsidesætte en eller flere af metoderne **rebuildFromRequestPage()**, **isErrorState()** og **reuseRequestPageOnError()**.

### <a name="processing-the-user-entered-data-in-the-first-step"></a>Behandle de brugerindtastede data i første trin

Behandlingen af dataene sker i klassen **ProcessGuideDataProcessorDefault**, som til gengæld aktiverer den ældre **WhsRfControlData**-klasse. Du behøver ikke ændre denne standardfunktionsmåde, og **WhsRfControlData** har allerede en logik til validering af feltet **ProdId**, så du behøver ikke skrive en logik til håndtering af dette. Hvis der kræves udvidelser til valideringslogikken, kan du overveje at bruge den **WhsControl**-baserede udvidelsesmekanisme.

### <a name="determine-if-the-first-step-is-complete"></a>Afgøre, om det første trin er fuldført

Når valideringen lykkes, er tiden inde til at markere trinnet som fuldført. Det kan du gøre i basisklassen, men betingelsen skal implementeres for at afgøre, at trinnet er fuldført. Det gør følgende tilsidesættelsesmetode.

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a>Trin to: Få vist ordredetaljer, og bekræft

I andet trin i processen får brugeren vist et skærmbillede med oplysninger om ordren. Brugeren kan enten klikke på knappen **OK** for at bekræfte starten af produktionsordren eller klikke på **Annuller** for at gå tilbage til starten af processen. I dette eksempel skal du kalde trinnet **ProdProcessGuideConfirmProductionOrderStep** og sidegeneratorklassen **ProdProcessGuideConfirmProductionOrderPageBuilder**.

Klassen ProdProcessGuideConfirmProductionOrderStep ser ud som den nedenstående.

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

Da brugeren ikke angiver nogen værdier her, behøver du ikke at tilsidesætte **isComplete()**-metoden. Trinnet er udført, når brugeren klikker på **OK**.

Sidegeneratorklassen tilsidesætter **addDataControls()**-metoden for at tilføje tre etiketter. Den første etiket viser produktionsordre-id'et, den anden indeholder vareoplysninger (for eksempel vare-id, dimensioner eller beskrivelse), og den tredje indeholder antallet og måleenheden.

**addActionControls()** tilsidesættes derefter for at tilføje to knapper – knappen **OK** og knappen **Annuller**, der bruges til at annullere processen og gå tilbage til starten af processen.

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> Du kan finde samme kildekode til X++-metoderne i denne artikel ved hjælp af Application Explorer. Filtrer på klassenavnet, højreklik på klassenavnet, og vælg derefter **Vis kode**.

### <a name="step-3-start-the-production-order"></a>Trin 3: Starte produktionsordren

Det tredje trin er der, hvor forretningslogikken ved at starte produktionsordren udføres. Dette trin er noget forskelligt fra de foregående trin, da dette trin ikke har en brugergrænseflade. Dette trin udføres uovervåget, når brugeren klikker på **OK** i det forrige trin.

Den abstrakte **ProcessGuideStepWithoutPrompt**-klasse implementerer standardfunktionsmåden for sådanne trin. Det aktuelle trin skal derfor udvide klassen **ProcessGuideStepWithoutPrompt** og tilsidesætte **doExecute()**-metoden.

I følgende kodeeksempel vises implementering af klassen og metoden **doExecute()**. Metoden henter ganske enkelt ordre-id'et og bruger-id'et fra sessionstilstanden og aktiverer metoden for at starte denne produktionsordre.

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

Hvis der er en undtagelse, sikrer logikken for håndtering af strukturundtagelser, at processen rulles tilbage til forrige trin.

> [!NOTE]
> Når du aktiverer **addProcessCompletionMessage()**, føjes meddelelsen "Arbejdet er fuldført" til navigationsparametrene. Denne meddelelse vises i næste trin (hvis der er en brugergrænseflade). Basisklasserne håndterer denne logik, og der er ikke behov for at føje specifik kode til procesklasserne for at opnå denne funktionsmåde.


### <a name="building-the-navigation-through-the-steps"></a>Opbygge navigationen gennem trinnene

**ProcessGuideController**-basisklassen instantierer **ProcessGuideNavigationAgentDefault**-klassen, der er afhængig af en foruddefineret navigationsrute, som er et simpelt kort over kilde- og destinationstrin. Da der ikke er nogen betinget forgrening til produktionsstartscenariet, er denne implementering tilstrækkelig. Du behøver derfor kun at tilsidesætte metoden **initializeNavigationRoute()** for at definere navigationsruten.

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

Der er processer, hvor der vil være betinget forgrening (baseret på brugerhandlinger eller andre betingelser). Disse processer skal gøre følgende:

-   Implementere bestemte navigationsagenter, der er nedarvet fra **ProcessGuideNavigationAgent**-klassen.

-   Implementere den specifikke navigationsagent, der er nedarvet fra **ProcessGuideNavigationAgentAbstractFactory**-klassen, og som indeholder logik, der instantierer den korrekte navigationsagent baseret på aktuelle trin, sessionstilstande, brugerhandlinger eller anden logik.

-   Tilsidesæt eventuelt **navigationAgentCreationParameters()** i controllerklassen for at overføre passende parametre.

-   Tilsidesæt **navigationAgentFactory()** i controlleren for at instantiere navigationsagentfabrikken, der er oprettet ovenfor.

### <a name="action-classes"></a>Handlingsklasser

Handlingsklasser repræsenterer brugerhandlinger, så i dette eksempel bruges handlingen **OK** til at vise, hvordan handlingerne oprettes.

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

Klassen skal implementere to abstrakte metoder:

-   **label()**, som returnerer den etiket, der skal vises i et knapkontrolelement, der er bundet til denne handling.

-   **doExecute()**, som udfører handlingen. Som nævnt tidligere, udfører knappen **OK** blot et tilbagekald til trinnet. Andre handlinger kan dog have en mere kompleks logik her.

Handlingerne instantieres ved hjælp af **SysExtension**-strukturen baseret på attributten **ProcessGuideActionName**. På samme måde som sidegeneratorerne instantieres, implementerer trinklassen standardhandlingsfabrikken, hvilket kan tilsidesættes. Sidegeneratoren tilføjer et knapkontrolelement på denne måde.

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

Når den gør det, beder den trinnet om at oprette en handlingsklasse for det overførte navn, og handlingen knyttes til knappen.

### <a name="summary"></a>Resumé

Hvis du vil opsummere alt det, hvad der er forklaret i denne artikel, findes der her en omfattende oversigt over den kode, der skal bruges til processen:

1.  **ProdProcessGuideProductionStartController**

    1.  Tilsidesæt **initialStepName()** for at angive navnet på det første trin.
    2.  Tilsidesæt **initializeNavigationRoute()** for at opbygge navigationsoversigten.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  Tilsidesæt **isComplete()** for at angive, hvornår trinnet betragtes som fuldført.
    2.  Tilsidesæt **pageBuilderName()** for at angive den sidegenerator, der skal bruges.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  Tilsidesæt **addDataControls()** for at tilføje tekstfeltet **Produktions-id**.
    2.  Tilsidesæt **addActionControls()** for at tilføje knapperne **OK** og **Annuller**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  Tilsidesæt **pageBuilderName()** for at angive den sidegenerator, der skal bruges.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  Tilsidesæt **addDataControls()** for at tilføje etiketter for ordre-, vare- og antalsoplysninger.

    2.  Tilsidesæt **addActionControls()** for at tilføje knapperne **OK** og **Annuller**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > Metoden **generateItemInfoForProdId()**, der bruges til generering af etiketter for vareoplysninger, er udeladt i Denne artikel. Denne metode forespørger et par tabeller for at hente vare-id, beskrivelse og dimensioner. Hvis du vil have en bedre forståelse af **generateItemInfoForProdId()**, skal du se på kildekoden.

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  Tilsidesæt **doExecute()** for at udføre startprocessen for produktionen og tilføje meddelelsen om færdiggørelse af processen.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> Bemærk, at mange af de almindelige mønstre (gendannelse af brugergrænseflade efter fejl, angivelse af meddelelse om færdiggørelse af processer, funktionsmåden for **OK** og **Annuller**) er flyttet til strukturen – hvilket betyder, at programudvikleren ikke behøver skrive standardkode, hvor der både er risiko for fejl og for uoverensstemmende funktionsmåder på tværs af processer. Hvor scenariet skal afvige fra den almindelige sti, får programudvikleren dog mulighed for at tilsidesætte passende metoder – men så er det en tilsigtet afvigelse, der både er eksplicit og kan spores.


### <a name="extending-a-business-process"></a>Udvide en forretningsproces

Denne artikel har indtil videre fremhævet, hvordan du kan opbygge en ny proces ved hjælp af **ProcessGuide**-strukturen. I dette sidste afsnit kan du finde nogle eksempler på, hvordan denne forretningsproces kan udvides.

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>Tilføje et trin i et flow (ved hjælp af ProcessGuideNavigationAgentDefault)

Hvor skal der udvides:

-   Den underordnede klasse til klassen **ProcessGuideController** for processen.

Sådan udvider du:

-   Udvid metoden **initializeNavigationRoute()** i controllerklassen, og aktivér **addFollowingStep()** i klassen **ProcessGuideNavigationRoute**.

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>Tilføje et trin i et flow (ved hjælp af den brugerdefinerede navigationsagent)

Hvor skal der udvides:

-   Den underordnede klasse til klassen **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent**.

Sådan udvider du:

-   Opret en ny underordnet klasse for **ProcessGuideNavigationAgent**, der returnerer navnet på det ønskede trin.

-   Opret en ny klasse, der er afledt af **ProcessGuideNavigationAgentFactory**, der betinget returnerer den navigationsagent, der er oprettet ovenfor.

-   Udvid metoden **navigationAgentFactory()** i controllerklassen for at returnere fabrikken, der er oprettet ovenfor.

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>Tilføje et nyt kontrolelement i brugergrænsefladen for et eksisterende trin 

Hvor skal der udvides:

-   Underordnet til **ProdProcessGuidePageBuilder** for trinnet.

Sådan udvider du:

-   Udvid metoden **addDataControls()**, og tilføj den ekstra kontrol.

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>Fuldføre gennemgangen af brugergrænsefladen i et eksisterende trin

Hvor skal der udvides:

-   Underordnet til **ProdProcessGuideStep**.

Sådan udvider du:

-   Opret en ny underordnet klasse til klassen **ProdProcessGuidePageBuilder**, og implementer den ønskede brugergrænseflade.

-   Udvid metoden **pageBuildeName()** i trinklassen for at returnere **ProcessGuidePageBuilderNameAttribute** for den klasse, der er oprettet ovenfor.

### <a name="alter-logic-when-a-step-is-considered-complete"></a>Ændre logikken, når et trin betragtes som fuldført

Hvor skal der udvides:

-   Underordnet til **ProdProcessGuideStep**.

Sådan udvider du:

-   Udvid metoden **isComplete()** for at bygge den ekstra logik.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]