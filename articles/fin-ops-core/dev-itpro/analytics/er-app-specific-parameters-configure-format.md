---
title: Konfigurer ER-formater for at bruge de parametre, der er angivet for den enkelte juridiske enhed
description: I dette emne forklares det, hvordan du kan konfigurere Elektroniske rapporteringsformater til at bruge de parametre, der er angivet for den enkelte juridiske enhed.
author: NickSelin
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 16eab3ffa7d4a780ec9709f5c8a5c263b1e75365
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751172"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a>Konfigurer ER-formater for at bruge de parametre, der er angivet for den enkelte juridiske enhed

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Oversigt

I mange af de Elektroniske rapporteringsformater, du kommer til at designe, skal du filtrere data ved hjælp af et sæt værdier, der er specifikke for de enkelte juridiske enheder i din forekomst (f.eks. et sæt momskoder til filtrering af momstransaktioner). Når filtrering af denne type i øjeblikket er konfigureret i et ER-format, bruges de værdier, der er afhængige af den juridiske enhed (f.eks. momskoder) i udtryk for ER-formatet, til at angive data filtreringsregler. ER-formatet er derfor gjort specifikt for den juridiske enheds, og hvis du vil generere de nødvendige rapporter, skal du oprette afledte kopier af det oprindelige ER-format for hver juridisk enhed, hvor du skal køre ER-formatet. Hvert afledte ER-format skal redigeres for at samle de specifikke værdier for juridiske i det, og omorganiseres, når den oprindelige (basis)version er blevet opdateret, eksporteret fra et testmiljø og importeret til et produktionsmiljø, når det skal udrulles med henblik på anvendelse i produktionen osv. Vedligeholdelse af denne type af konfigurerede ER-løsninger er derfor temmelig kompliceret og tidskrævende af flere årsager:

-   Jo flere juridiske enheder der er, des flere ER-formatkonfigurationer skal der vedligeholdes.
-   Vedligeholdelse af ER-konfigurationer kræver, at erhvervsbrugere er bekendt med ER.

De ER-programspecifikke parametre gør det muligt for superbrugere at konfigurere datafiltreringen i et ER-format, så den er baseret på et sæt abstrakte regler. Dette sæt regler kan konfigureres til at bruge de datakilder, der er tilgængelige i et ER-format. Erhvervsbrugere kan derefter angive de rigtige regler ud over den bevarede ER-ramme ved hjælp af den brugergrænseflade (UI), der genereres automatisk på basis af indstillingerne for det tilsvarende ER-format og de aktuelle oplysninger om den juridiske enhed, du har adgang til i ER-formatets datakilder. Regelsættet, der er angivet for et ER-format, kan eksporteres fra Dynamics 365 Finance (Finance)'s aktuelle juridiske enhed for forekomsten. Det kan derefter importeres til en anden juridisk enhed af enten den samme Finance-forekomst eller en anden forekomst som et sæt regler for det samme ER-format.

## <a name="prerequisites"></a>Forudsætninger

For at gennemføre eksemplerne i dette emne, skal du have adgang til den forekomst af Regulatory Configuration Service (RCS), der er klargjort til den samme lejer som Finance, for en af følgende roller:

- Udvikler til elektronisk rapportering
- Funktionel konsulent i elektronisk rapportering
- Systemadministrator

Vi anbefaler, at du udfører trinnene i emnet [Understøt parameteriserede opkald om ER-datakilder af typen BEREGNET FELT](er-calculated-field-type.md). Hvis du allerede har fuldført disse trin, kan du springe trinnene i den efterfølgende sektion **Importer ER-konfigurationer til RCS** over.

## <a name="import-er-configurations-into-rcs"></a>Importer ER-konfigurationer til RCS

Download og gem følgende ER-konfigurationer lokalt.

| **Indholdsbeskrivelse**                        | **Filnavn**                                        |
|------------------------------------------------|------------------------------------------------------|
| Eksempel på konfigurationsfil for **ER-datamodel**    | [Model til at lære parameteriserede calls.version.1.xml](https://download.microsoft.com/download/2/d/b/2db913a0-3622-494e-91a2-97fc494af9b9/Modeltolearnparameterizedcalls.version.1.xml)     |
| Eksempel på konfigurationsfil for **ER-metadata**      | [Metadata til at lære parameteriserede calls.version.1.xml](https://download.microsoft.com/download/1/b/3/1b343968-5a47-4000-b5a8-6487698ef4c0/Metadatatolearnparameterizedcalls.version.1.xml)  |
| Eksempel på konfigurationsfil for **ER-modeltilknytning** | [Tilknytning for at lære parameteriserede calls.version.1.1.xml](https://download.microsoft.com/download/8/6/6/866e0ab6-2e05-4d98-9d52-d2da2038f6e4/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| Eksempel på konfiguration af **ER-format**             | [Format til at lære parameteriserede calls.version.1.1.xml](https://download.microsoft.com/download/e/3/9/e392eadc-b9b4-4834-95c3-b8066dd00b9c/Formattolearnparameterizedcalls.version.1.1.xml)  |

Dernæst skal du logge på din RCS-forekomst.

I dette eksempel skal du oprette en konfiguration til eksempelfirmaet Litware, Inc. Før du kan fuldføre denne procedure skal du fuldføre trinnene i emnet [Opret en konfigurationsudbyder og marker den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md) i RCS.

1.  Vælg **Elektronisk rapportering** på standarddashboardet.
2.  Vælg **Rapporteringskonfigurationer**.
3.  Importér de ER-konfigurationer, som du downloadede tidligere, til RCS i følgende rækkefølge: datamodel, metadata, modeltilknytning og format. Benyt følgende fremgangsmåde for hver ER-konfiguration:

    1.  Vælg **Udveksling**.
    2.  Vælg **Indlæs fra XML-fil**.
    3.  Vælg **Gennemse** for at vælge filen til den krævede ER-konfiguration i XML-format.
    4.  Vælg **OK**.

## <a name="review-the-er-solution-that-is-provided"></a>Gennemse den ER-løsning, der leveres

1.  Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.
2.  Vælg emnet **Format til at lære parameteriserede kald**.
3.  Vælg **Designer**.
4.  Vælg **Udvid/skjul**.

    ER-formatet **Format til at lære parametriserede opkald** er designet, så der oprettes en momsangivelse i XML-format, der indeholder flere momsniveauer (almindelig, reduceret og ingen). Hvert niveau har et forskelligt antal detaljer.

    ![Flere niveauer i ER-format. Format til at lære parameteriserede kald](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  På fanen **Tilknytning** skal du udvide objekterne **Model**, **Data** og **Opsummering**.

    Datakilden **Model.Data.Opsummering** returnerer listen over momstransaktioner. Disse transaktioner opsummeres efter momskode. For denne datakilde er det beregnede felt **Model.Data.Opsummering.Niveau** konfigureret til at returnere koden for momsniveauet for hver opsummeret post. For alle momskoder, der kan hentes fra datakilden **Model.Data.Opsummering.Niveau** på kørselstidspunktet, returneres koden for momsniveau (**Almindelig**, **Reduceret**, **Ingen** eller **Andre**) som en tekstværdi. Det beregnede felt **Model.Data.Opsummering** bruges til at filtrere poster for datakilden **Model. Data.Opsummering** og angiver de filtrerede data i hvert XML-element, der repræsenterer et beskatningsniveau, ved hjælp af felterne **Model.Data2.Niveau1**, **Model.Data2.Niveau2** og **Model.Data2.Niveau3**.

    ![Datakilden Model.Data.Opsummering med liste over momstransaktioner](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    Det beregnede felt **Model.Data.Opsummering** er konfigureret, så det indeholder et ET-udtryk. Bemærk, at momskoderne codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) er hardcoded ind i denne konfiguration. Derfor er dette ER-format afhængigt af den juridiske enhed, hvor disse momskoder er blevet konfigureret.

    ![Det beregnede felt Model.Data.Opsummering.Niveau med hardcodede momskoder](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    Hvis du vil understøtte forskellige sæt momskoder for hver juridisk enhed, skal du følge disse trin:

    - Opret en afledt version af ER-formatet for hver juridisk enhed.
    - Opdater momskoderne i det beregnede felt **Model.Data.Opsummering.Niveau** ud fra indstillingen for den juridiske enhed.

6.  Luk siden **Formatdesigner**.

## <a name="create-a-derived-format"></a>Oprette et afledt format

Derefter skal du bruge funktionen programspecifikke parametre for ER til at understøtte et andet sæt momskoder for hver juridisk enhed i et enkelt ER-format.

1.  Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.
2.  Vælg emnet **Format til at lære parameteriserede kald**.
3.  Vælg **Opret konfiguration**.
4.  Vælg indstillingen **Afledt fra navn: Format til at lære parameteriserede kald, Microsoft**.
5.  Gå til feltet **Navn**, og angiv **Format til at lære, hvordan man leder efter LE-data**.
6.  Vælg **Opret konfiguration**.

## <a name="configure-a-derived-format"></a>Konfigurer et afledt format

### <a name="add-a-format-enumeration"></a>Tilføj et fasttekst-format

Derefter skal du tilføje et nyt ER-fasttekstformat. Værdierne i dette fasttekstformat vises for erhvervsbrugere, der angiver de juridiske enheds-afhængige sæt momskoder for de forskellige beskatningsniveauer, der bruges i ER-formatet.

1.  Vælg **Designer**.
2.  Vælg **Fasttekst-formater**.
3.  Vælg **Tilføj**.
4.  I feltet **Navn** skal du angive **Liste med beskatningsniveauer**.
5.  Vælg **Gem**.
6.  Vælg **Tilføj** under fanen **Værdier for fasttekstformat**.
7.  I feltet **Navn** skal du angive **Almindelig beskatning**.
8.  Vælg **Tilføj** igen.
9.  I feltet **Navn** skal du angive **Reduceret beskatning**.
10. Vælg **Tilføj** igen.
11. I feltet **Navn** skal du angive **Ingen beskatning**.
12. Vælg **Tilføj** igen.
13. I feltet **Navn** skal du skrive **Andet**.

    ![Ny post på siden Formatfasttekster](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    Da erhvervsbrugere kan bruge forskellige sprog til at angive juridisk enheds-afhængige sæt momskoder, anbefales det, at du oversætter værdierne i denne optælling til de sprog, der er konfigureret som de foretrukne sprog for disse brugere i Finance.

14. Vælg en post for **Ingen beskatning**.
15. Klik på feltet **Etikette**.
16. Vælg **Oversæt**.
17. I panelet **Tekstoversættelse** i feltet **Etikette-ID** skal du indtaste **LBL_LEVELENUM_NO**.
18. I feltet **Tekst i standardsprog** skal du indtaste **Ingen beskatning**.
19. I feltet **Sprog** skal du vælge **DE**.
20. I feltet **Oversat tekst** skal du indtaste **keine Besteuerung**.
21. Vælg **Oversæt**.

    ![Tekstoversættelses-slide-out](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. Vælg **Gem**.
23. Luk siden **Fasttekstformat**.

### <a name="add-a-new-lookup-data-source"></a>Tilføje en ny opslagsdatakilde

Derefter skal du tilføje en ny datakilde for at angive, hvordan erhvervsbrugere skal angive de juridiske enhedsafhængige regler for at genkende det korrekte beskatningsniveau for hver enkelt opsummerede transaktionspost.

1.  På fanen **Tilknytning** skal du vælge **Tilføj**.
2.  Vælg **Fasttekst-format\Opslag**.

    Du har netop identificeret, at de enkelte regler, som erhvervsbrugere angiver for genkendelse af beskatningsniveau, skal returnere en værdi i et ER-fasttekstformat. Bemærk, at datakildetypen **Opslag** kan tilgås under blokkene **Datamodel** og **Dynamics 365 for Operations** ud over blokken **Fasttekstformat**. Du kan derfor bruge fasttekst for ER-datamodeller og programmer til at angive den type værdier, der skal returneres for datakilder af den pågældende type.
    
3.  I feltet **Navn** skal du angive **Vælger**.
4.  I feltet **Fasttekstformat** skal du vælge **Liste med beskatningsniveauer**.

    Du har netop angivet, at for hver regel, der er angivet i denne datakilde, skal en erhvervsbruger vælge en af værdierne fra fasttekstformatet **Listen over beskatningsniveauer** som en returneret værdi.
    
5.  Vælg **Rediger opslag**.
6.  Vælg **Kolonner**.
7.  Udvid elementet **Model**.
8.  Udvid elementet **Data**.
9.  Udvid elementet **Moms**.
10. Vælg elementet varen **Model.Data.Moms.Code**.
11. Klik på knappen **Tilføj** (pilen til højre).

    ![Kolonner-slide-out](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    Du har netop angivet, at for hver regel, der er angivet i denne datakilde for genkendelse af beskatningsniveau, skal en erhvervsbruger vælge en af momskoderne som en betingelse. Den liste over momskoder, som erhvervsbrugeren kan vælge, vil blive returneret af datakilden **Model.Data.Moms**. Da denne datakilde indeholder feltet **Navn**, vises navnet på momskoden for hver momskodeværdi i det opslag, der vises for erhvervsbrugeren.
    
12. Vælg **OK**.

    ![Opslagsdesignerside](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    Erhvervsbrugere kan tilføje flere regler som poster i denne datakilde. Hver post nummereres af en stregkode. Reglerne evalueres i rækkefølge efter stigende linjenummer.

    Da du har valgt feltet **Momskode** som en betingelse for reglerne i denne opslagsdatakilde, og idet **Momskode** er konfigureret som et felt af datatypen **Streng**, evalueres hver regel på tidspunktet for kørslen ved at sammenligne den momskode, der overføres til datakilden med den momskode, der er defineret i denne post i datakilden.

    Når der findes en regel, der opfylder den konfigurerede betingelse, returnerer denne datakilde opslagsværdien for den regel, der er defineret i feltet **Opslagsresultat**. Hvis der ikke findes en regel, udløses der en undtagelse, der giver brugeren besked om, at den aktuelle datakilde ikke kan returnere en korrekt værdi.

13. Vælg **Gem**.
14. Luk siden **Opslagsdesigner**.
15. Vælg **OK**.

    Bemærk, at du har tilføjet en ny datakilde, der returnerer beskatningsniveauet, som værdi i fasttekstformatet **Liste over beskatningsniveauværdier**, som videregives til datakilden som argument for parametret **Kode** i datatypen **Streng**.
    
    ![Formatdesignerside med ny datakilde](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    Bemærk, at evalueringen af konfigurerede regler afhænger af datatypen for de felter, der er valgt til at skulle definere betingelserne for disse regler. Når du vælger et felt, der er konfigureret som et felt af datatypen **Numerisk** eller **data**, vil kriterierne være forskellige fra de kriterier, der blev beskrevet tidligere for datatypen **Streng**. I felterne **Numerisk** og **Dato** skal reglen angives som et værdiinterval. Reglens betingelse betragtes derefter som opfyldt, når en værdi, der overføres til datakilden, ligger inden for det konfigurerede interval.
    
    I følgende illustration vises et eksempel på denne type opsætning. Ud over feltet **Model.Data.Moms.Kode** af datatypen **Streng** er det feltet **Model.Moms.Opsummering.Grundlag** for datatypen **Reel**, der bruges til at angive betingelser for en opslagsdatakilde.
    
    ![Opslagsdesignerside med flere kolonner](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    Da felterne **Model.Data.Moms.Kode** og **Model.Moms.Opsummering.Grundlag** er markeret for denne opslagsdatakilde, konfigureres hver enkelt regel i denne datakilde på følgende måde:
    
    -   På den liste, der vises, skal værdien af fasttekstformatet **Listen over beskatningsniveauer** være angivet som en returneret værdi.
    -   Momskoden skal angives som betingelse for reglen. Det er kun de momskoder, der leveres af datakilden **Model.Data.Moms**, der er anvendelige.
    -   Minimum- og maksimumværdierne for momsgrundlagsbeløbet skal angives som betingelser for reglen.

    Her er, hvordan hver regel i denne datakilde evalueres under kørsel:
    -   Er koden for datatypen **Streng**, der blev overført til denne datakilde, lig med en regels momskode?
    -   Falder værdien af datatypen **Reel**, der blev overført til denne datakilde, mellem bestemte minimum- og maksimumværdier?

    En regel anses for at være anvendelig, når begge betingelser er opfyldt.

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a>Oversæt etiketten for den opslagsdatakilde, der blev tilføjet

Da erhvervsbrugere kan bruge forskellige sprog til at angive juridisk enheds-afhængige sæt momskoder, anbefales det, at du oversætter etiketten i alle opslagsdatakilder, som du har tilføjet, således at det fremstår i hver brugers foretrukne sprog på den tilsvarende side.

1.  Vælg datakilden **Model.Data.Vælger**.
2.  Vælg **Rediger**.
3.  Klik på feltet **Etikette**.
4.  Vælg **Oversæt**.
5.  I panelet **Tekstoversættelse** i feltet **Etikette-ID** skal du indtaste **LBL_SELECTOR_DS**.
6.  I feltet **Tekst i standardsprog** skal du angive **Vælg beskatningsniveau efter momskode**.
7.  I feltet **Sprog** skal du vælge **DE**.
8.  I feltet **Oversat tekst** skal du angive **Steuerebene für Steuerkennzeichen auswählen**.
9.  Vælg **Oversæt**.
10. Vælg **OK**.

    ![Datakildeegenskaber-slide-out](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a>Tilføje et nyt felt som skal bruge det konfigurerede opslag

1.  Udvid elementet **Model.Data**.
2.  Vælg elementet **Model.Data.Opsummering**.
3.  Vælg **Tilføj**.
4.  Vælg **Funktioner/Beregnet felt**.
5.  I feltet **Navn** skal du angive **NiveauViaOpslag**.
6.  Vælg **Rediger formel**.
7.  I **Formelfeltet** skal du angive **Model.Vælger (Model.Data.Opsummering.Kode)**.
8.  Vælg **Gem**.

    ![Tilføjelse af Model.Vælger(Model.Data.Opsummering.Kode) til formeldesignersiden](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  Luk siden **Formeleditor**.
10. Vælg **OK**.

    ![Formatdesignerside med ny formel tilføjet](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    Bemærk, at det beregnede felt **NiveauViaOpslag**, som du har tilføjet, returnerer beskatningsniveauet som værdien fasttekstformatet **Liste over beskatningsniveauer** for hver enkelt opsummeret momstransaktionspost. Postens momskode overføres til opslagsdatakilden **Model.Vælger**, og regelsættet for denne datakilde vil blive brugt til at vælge det korrekte beskatningsniveau.

### <a name="add-a-new-format-enumeration-based-data-source&quot;></a>Tilføj en ny datakilde baseret på fasttekstformat

Derefter skal du tilføje en ny datakilde, der henviser til fasttekstformat, som du tidligere har tilføjet. Værdierne i denne datakilde vil blive brugt i et ET-formatudtryk senere.

1.  Vælg **Tilføj rod**.
2.  Vælg **Fasttekst-formater\Fasttekst**.
3.  I feltet **Navn** skal du angive **Beskatningsniveau**.
4.  I feltet **Fasttekstformat** skal du vælge **Liste med beskatningsniveauer**.
5.  Vælg **Gem**.

### <a name=&quot;modify-an-existing-field-to-start-to-use-the-lookup&quot;></a>Rediger et eksisterende felt for at begynde at bruge opslaget

Derefter skal du redigere det eksisterende beregnede felt, så det bruger den konfigurerede opslagsdatakilde til at returnere den korrekte værdi for værdier for beskatningsniveau, afhængigt af momskoden.

1.  Vælg elementet **Model.Data.Opsummering.Niveau**.
2.  Vælg **Rediger**.
3.  Vælg **Rediger formel**.

    Bemærk, at det aktuelle udtryk for feltet **Model.Data.Opsummering.Niveau** indeholder følgende hardcodede momskoder:
    
    SAG (@.Kode, &quot;MOMS19&quot;, &quot;Almindelig&quot;, &quot;InVAT19&quot;, &quot;Almindelig&quot;, &quot;MOMS7&quot;, &quot;Reduceret&quot;, &quot;InVAT7&quot;, &quot;Reduceret&quot;, &quot;TREDJE&quot;, &quot;Ingen&quot;, &quot;InVAT0&quot;, &quot;Ingen&quot;, &quot;Andet")

4.  I feltet **Formel** skal du skrive **SAG(@.NiveauViaOpslag, Beskatningsniveau.'Almindelig beskatning', "Almindelig", Beskatningsniveau.'Reduceret beskatning', "Reduceret", Beskatningsniveau.'Ingen beskatning', "Ingen", "Andet")**.

    ![Side med ER-operationsdesigner](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    Bemærk, at udtrykket i feltet **Model.Data.Opsummering.Niveau** returnerer nu beskatningsniveauet baseret på momskoden for den aktuelle post og det sæt regler, som en erhvervsbruger konfigurerer i opslagsdatakilden **Model.Data.Vælger**.
    
5.  Vælg **Gem**.
6.  Luk siden **Formeldesigner**.
7.  Vælg **OK**.
8.  Vælg **Gem**.
9.  Luk siden **Formatdesigner**.

## <a name="complete-the-draft-version-of-a-derived-format"></a>Fuldfør kladdeversionen af et afledt format

1.  I oversigtspanelet **Versioner** skal du vælge **Skift status**.
2.  Vælg **Fuldfør**.
3.  Vælg **OK**.

## <a name="export-completed-version-of-modified-format"></a>Eksportér den fuldførte version af et tilpasset format

1.  I konfigurationstræet skal du vælge elementet **Format for at lære, hvordan man slår LE-data op**.
2.  På oversigtspanelet **Versioner** skal du vælge den post, der har statussen **Fuldført**.
3.  Vælg **Udveksling**.
4.  Vælg **Eksporter som XML-fil**.
5.  Vælg **OK**.
6.  Webbrowseren henter en **Format for at lære, hvordan du søger efter LE-data.xml**-fil. Gem filen lokalt.

Gentag trinnene i dette afsnit for overordnede elementer i formatet **Format til at lære, hvordan du søger efter LE-data**, og gem følgende filer lokalt:

-   Format til at lære parameteriserede kald.xml
-   Tilknytning for at lære parameteriserede kald.xml
-   Model til at lære parameteriserede kald.xml

Du kan få mere at vide om konfigurationen af ER-formatet **Format til at lære, hvordan du søger efter LE-data** til at konfigurere juridisk enhedsafhængige sæt af momskoder for at filtrere momstransaktioner efter forskellige beskatningsniveauer ved at fuldføre trinnene i emnet [Konfigurer parametrene for et ER-format for hver juridisk enhed](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Konfigurer parametrene for et ER-format for hver juridisk enhed](er-app-specific-parameters-set-up.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
