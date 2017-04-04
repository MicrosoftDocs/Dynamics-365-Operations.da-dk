---
title: Salgsreturneringer
description: "Dette emne indeholder oplysninger om processen for returordrer. Den indeholder oplysninger om returneringer fra kunder og deres virkning på efterkalkulationsarket og disponible lagerantal."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: b265a20a271230de5dba6df93900a24aad642885
ms.lasthandoff: 03/31/2017


---

# <a name="sales-returns"></a>Salgsreturneringer

Dette emne indeholder oplysninger om processen for returordrer. Den indeholder oplysninger om returneringer fra kunder og deres virkning på efterkalkulationsarket og disponible lagerantal.

Kunder kan returnere varer til forskellige årsager. For eksempel en vare kan være defekt, eller den ikke kan opfylde kundens forventninger. Returvareprocessen starter, når en kunde afgiver en anmodning om at returnere en vare. Efter kundens anmodning er modtaget, oprettes en returordre i Microsoft Dynamics 365 for operationer.

## <a name="return-order-process"></a>Returordreprocessen
Figuren nedenfor giver et overblik over returordreprocessen.  

[![salesreturns01](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Der findes to typer returordreprocessen: fysisk tilbage og kun kredit.

-   **Fysisk returnering** – returvareordren autoriserer fysisk returnering af produkter.
-   **Krediter kun** – returvareordren autoriserer en debitorkreditering, men ikke kræver, at kunden fysisk returnerer varerne.

### <a name="physical-return-order-process"></a>Fysiske returordreprocessen

1.  **Opret en returordre.** Formelt dokument bevillingen til debitor skal returnere defekte eller uønskede produkter. Returordren kræver ikke, at virksomheden accepterer de returnerede produkter eller levere en kredit til kunden. Hvis returnering er accepteret, kan du give en erstatningsvare, sendes før defekt vare er blevet returneret.
2.  **Ankomme til lageret til inspektion.** Fuldfør en indledende kontrol og validering mod returvareordre. Returordren understøtter også karantæne af de returnerede varer for yderligere inspektion og kvalitetskontrol.
3.  **Bestemme disposition.** Afslutte inspektionsprocessen, og beslutte, hvad der skal ske med de returnerede produkter. Beslutte, om du vil kreditere kunden, afvise returneringen produkt eller acceptere produkt returnering, skrot af produktet og derefter sende et erstatningsprodukt til kunden som en del af dette trin.
4.  **Oprette en følgeseddel.** Oprette en følgeseddel, og foretag afgørelsen disposition, du oprettede i trin 3. Færdiggør logistik-processer.
5.  **Oprette en faktura.** Luk returordren.

### <a name="credit-only-process"></a>Kun behandle kredit

1.  **Opret en returordre.** Formelt dokument bevillingen til kunden for at modtage en kredit uden at returnere de defekte eller uønskede produkter. Den **kun kredit** dispositionskode godkender, at beslutningen om at kreditere kunden uden fysisk returnering.
2.  **Oprette en faktura.** Oprette en kreditnota, og derefter lukker returordren.

## <a name="return-material-authorization"></a>Returnere materiale tilladelse
Returnere materiale tilladelse (RMA) behandling bygger på salgsordren funktionalitet. Et RMA er registreret som en returordre, der er oprettet som en salgsordre, og kan have en anden salgsordre, der er knyttet til den, kaldes en erstatningsordre. Begge salgsordrer sammenkædes oprindelige RMA-nummeret.

-   **Returordre** – til at registrere en RMA, du opretter en returordre, som er en salgsordre, der er tildelt typen, **returneret ordre.** De ændringer, du foretager til RMA-oplysninger opdateres automatisk i salgsordren. Indtil status for returordren er **åbne**, vises den ikke på listen over salgsordrer. Du kan bruge RMA til at håndtere ankomsten og modtagelsen af returnerede varer samt til at give et eneste dispositionshandlingen kredit (se afsnit **dispositionskoder og dispositionshandlingerne**). Alle andre opfølgende processer skal håndteres i salgsordren.
-   **Erstatningsordre** – når en erstatningsordre skal leveres til kunden, RMA'EN kan omfatte en anden tilknyttede salgsordre. Du kan manuelt oprette en erstatningsordre for RMA til støtte for direkte levering. Alternativt kan erstatningsordren oprettes automatisk efter modtagelse og inspektion på modtagelse er udført for linjeelementet RMA, der har en dispositionskode, der angiver udskiftning. Erstatningsordren har de samme funktioner, der er knyttet til en salgsordre. For eksempel kan du bruge den til at konfigurere et brugerdefineret produkt som erstatningsvaren, oprette en produktionsordre for at reparere en returneret vare, opretter en indkøbsordre for direkte levering til at sende erstatningen fra en leverandør eller understøtter andre formål.

## <a name="create-a-return-order"></a>Oprette en returordre
Returordreprocessen starter, når en kunde kontakter organisationen til at returnere et defekt eller uønsket produkt og/eller skal krediteres. Når din virksomhed accepterer returnering, er returnering dokumenteret ved en returordre. Denne returordre bliver kontaktpunkt i den interne behandling af det returnerede produkt. Følgende illustration viser fremgangsmåden for oprettelse af en returordre.  

[![Fremgangsmåden for oprettelse af en returordre](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Oprette en returordrehovedet

Når du opretter en returordre, skal oplysningerne i følgende tabel medtages.

| Felt              | Betegnelse                                              | Bemærkninger                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Debitorkonto   | En reference til tabellen kunder                       | Du skal angive en eksisterende debitorkonto.                                                                                                                                                                                                                                                                                                  |
| Leveringsadresse   | Den adresse, som varen er returneret til                 | Organisationens adresse bruges som standard. Hvis et bestemt lagersted er markeret i hovedet, ændres leveringsadressen til leveringsadressen på lageret. Du kan ændre denne adresse på den **returnere oplysninger om** side.                                                                                                  |
| Lokation/lagersted     | Det sted eller lagersted, der modtager det returnerede produkt | Leveringsadressen for returordren bestemmes baseret på leveringsadressen af sted eller lagersted.                                                                                                                                                                                                                                 |
| RMA-nummer (Return Materials Authorization-nummer)         | Det ID, der er knyttet til returordren              | RMA-nummeret bruges som en alternativ nøgle under hele processen returordre. RMA-nummeret, der er tildelt er baseret på RMA-nummerserie, der er konfigureret på den **Accounts receivable parameters** side.                                                                                                                              |
| Frist           | Den sidste dato, en vare kan returneres.               | Standardværdien, der beregnes som dags dato plus gyldighedsperioden. Eksempelvis hvis returnering er gyldig for kun 90 dage fra dato, hvor den returordre oprettes, og returvareordren blev oprettet på 1 maj, værdien i feltet er **30 juli**. Gyldighedsperioden er angivet på den **Accounts receivable parameters** side. |
| Årsagskode for returnering | Kundens årsag til returnering af produktet          | Årsagskoden vælges på listen over brugerdefinerede årsagskoder. Du kan til enhver tid opdatere dette felt.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Oprette returordrelinjer

Når du har fuldført Returner sidehoved, kan du oprette linjer ved hjælp af en af følgende metoder:

-   Du kan angive oplysninger om varen, antal og andre oplysninger for hver returvarelinje manuelt.
-   Oprette en returlinje ved hjælp af den **Find salgsordre** funktion. Vi anbefaler, at du bruger denne funktion, når du opretter en returordre. Den **Find salgsordre** funktion opretter en reference fra den returledning til fakturerede salgsordrelinjen, og henter linje oplysninger som varenummer, antal, pris, rabat og omkostningsværdier fra salgslinjen. Referencen er med til at sikre, når produktet returneres til virksomheden, det er værdisat til samme kostpris, at den blev solgt til. Referencen validerer, returnerer ordrer ikke er oprettet for en mængde, der overstiger det antal, der blev solgt på fakturaen.

**Bemærk:** linjer, der har en reference til en salgsordre skal håndteres som rettelser eller tilbageførsler af salget. Se afsnittet "Post til Finans" senere i dette emne for at få yderligere oplysninger.

### <a name="charges"></a>Tillæg

Gebyrer og afgifter, der kan føjes til returordren gennem en eller flere af følgende metoder:

-   Du kan manuelt føje tillæg til returordrehovedet, returordrelinjen eller begge dele.
-   Gebyrer kan føjes automatisk til returordrehovedet som funktion af returårsagskoden.
-   Gebyrer kan automatisk føjes til returordrelinjen, baseret på dispositionskoden for linjen.

Gebyrer tilføjes automatisk efter en Returårsagskode eller dispositionskode, der er knyttet til linjen. Hvis årsagskoden ændres senere, fjernes den eksisterende post gebyr, men kan tilføjes en ny post i tillægget, baseret på den nye årsagskode. Når du føjer tillæg til at returnere ordrelinjer, bliver gebyrer, der beregnes som en procentdel af værdien linje eller en ordre negativ når den streg eller linje rækkefølge er negativ, medmindre procenten, der også er et negativt tal. Et gebyr, der har en negativ værdi repræsenterer en kredit til kunden.

### <a name="return-reason-codes"></a>Årsagskoder for returneringer

Årsagskoder for returneringer, kan du hjælpe, gør det nemmere at analysere return mønstre. Årsagskoder indeholder oplysninger om, hvorfor en kunde ønsker at returnere varer. Nogle organisationer har mange årsagskoder. Disse organisation kan gruppere årsagskoderne til årsagskodegrupper til at få et bedre overblik og for at have rapporteret akkumuleret.

### <a name="disposition-codes-and-disposition-actions"></a>Dispositionskoder og dispositionshandlingerne

Et vigtigt skridt i processen returordre er at tildele en dispositionskode til returordrelinjen som en del af registrering af ankomst. Dispositionskoden bestemmer følgende oplysninger:

-   **De finansielle følger** – bør krediteres kunden for de returnerede varer, og skal eventuelle gebyrer føjes til returordrelinjen?
-   **Fordeling af den returnerede vare** – skal varen være føjet til lageret, skal det kasseres eller skal den sendes tilbage til kunden?
-   **Logistik til den returnerede vare** – skal udstedes en erstatningsvare til kunden?

Foruden fastlæggelsen af, hvordan de returnerede varer er solgt, kan dispositionskoder medføre gebyrer, der skal anvendes til returlinjen. De kan også bruges til at gruppere returnerer til statistiske analyser. Dispositionskoder er defineret som en del af opsætningen af returordrer. Men hver dispositionskode skal referere til en af de indbyggede dispositionshandlingerne. I følgende tabel vises de indbyggede dispositionskoder og deres handlinger. **Vigtigt:** Hvis en vare skal returneres ikke, men kunden skal stadig krediteret, tildele den **kun kredit** dispositionskode til returlinjen.

<table>
<thead>
<tr class="header">
<th>Dispositionskode</th>
<th>Økonomiske konsekvenser</th>
<th>Konsekvenser for logistik</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Krediter kun</td>
<td><ul>
<li>Kunden krediteres salgspris minus eventuelle gebyrer eller afgifter.</li>
<li>Tab fra ophugning varen er bogført i Finans.</li>
</ul></td>
<td>Varen skal returneres ikke. Denne dispositionshandlingen bruges i følgende tilfælde:
<ul>
<li>Der er tilstrækkelig tillid mellem parterne.</li>
<li>Udgifter til tilbagelevering defekt vare er prohibitiv.</li>
<li>Ikke tillades varerne tilbage til lageret. På grund af andre betingelser en fysisk returnering er ikke længere nødvendigt.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kredit</td>
<td><ul>
<li>Kunden krediteres salgspris minus eventuelle gebyrer eller afgifter.</li>
<li>Lagerværdien forøges med omkostningerne ved den returnerede vare.</li>
</ul></td>
<td>Varen returneres og føjes til lageret.</td>
</tr>
<tr class="odd">
<td>Erstat og krediter</td>
<td><ul>
<li>Kunden krediteres salgspris minus eventuelle gebyrer eller afgifter.</li>
<li>Lagerværdien forøges med omkostningerne ved den returnerede vare.</li>
<li>En separat salgsordre for en erstatning oprettes og håndteres separat.</li>
</ul></td>
<td>Varen returneres og føjes til lageret.</td>
</tr>
<tr class="even">
<td>Erstat og kasser</td>
<td><ul>
<li>Kunde krediteres salgspris minus eventuelle gebyrer eller afgifter.</li>
<li>Tab fra ophugning varen er bogført i Finans.</li>
<li>En separat salgsordre for en erstatning oprettes og håndteres separat.</li>
</ul></td>
<td>Varen er returneret og kasseret.</td>
</tr>
<tr class="odd">
<td>Returner til kunde</td>
<td>Ingen, bortset fra eventuelle gebyrer eller afgifter.</td>
<td>Varen er returneret, men sendes tilbage til kunden efter besigtigelse. Denne dispositionshandlingen kan bruges, hvis varen er bevidst blevet beskadiget, eller hvis garantien er nedlagt.</td>
</tr>
<tr class="even">
<td>Kasseres</td>
<td><ul>
<li>Kunden krediteres salgspris minus eventuelle gebyrer eller afgifter.</li>
<li>Tab fra ophugning varen er bogført i Finans.</li>
</ul></td>
<td>Varen er returneret eller kasseres.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Ankomst til lagerstedet til inspektion
Før du kan modtage returnerede varer på lageret fysisk ved at bogføre en følgeseddel, skal varerne gennemgå ankomst, registrering og valgfri inspektion. Figuren nedenfor giver et overblik over modtagelsesprocessen. I de følgende afsnit beskrives hvert trin, der er vist i illustrationen.  

[![Modtagelsesprocessen](./media/salesreturn03.png)](./media/salesreturn03.png)  

Processen har flere variationer, som ikke er beskrevet i dette emne. Her er nogle af disse variationer:

-   Brug ikke den **modtagelsesoversigt** listen for at oprette en modtagelseskladde. I stedet manuelt oprette modtagelseskladden. Returnere ordrer har **salgsordre** som reference.
-   Hvis du bruger lokationsstyring, kan du generere palletransporter. Returlinjen får status af **ankommet** under palletransport.
-   Registrere modtagelsen af den returnerede vare direkte fra returordrelinje, ved hjælp af den **registrering** funktion.

Returnerer er integreret med den generelle proces til modtagelse af lager under processen ved ankomsten. Modtagelsesprocessen understøtter også oprettelse af karantæneordrer for returnerede varer, der skal underkastes en særskilt undersøgelse.

### <a name="identify-products-in-the-arrival-overview-list"></a>Identificere produkter på listen ankomst oversigt

Den **modtagelsesoversigt** side viser en liste over alle planlagte indgående modtagelser. **Bemærk:** ankomster fra returordrer skal behandles separat fra andre typer af transaktioner ved ankomsten. Når du har identificeret en indgående pakke på den **modtagelsesoversigt** side (for eksempel ved hjælp af ledsagedokumentet RMA), i handlingsruden, skal du klikke på **Start modtagelse** til at oprette og initialisere en modtagelseskladde, der svarer til ankomst.

### <a name="edit-the-arrival-journal"></a>Rediger modtagelseskladden

Ved at angive den **karantæne management** at **Ja**, kan du oprette en karantæneordre for returlinjen. Hvis en linje har været sendt i karantæne til inspektion, kan du ikke angive en dispositionskode. **Bemærk:** Hvis du indstiller den **karantæne management** at **Ja** i varens lagermodelgruppe, den **karantæne management** indstilling på den **kladdelinjer** side vil være markeret for modtagelseskladdelinjen, og kan ikke ændres. Hvis linjen sendes i karantæne, skal du angive den relevante karantænelagersted. Hvis linjen ankomst ikke sendes til inspektion, skal warehouse ankomst-assistenten angive dispositionskoden direkte på modtagelseskladdelinjen og derefter bogføre modtagelseskladden. Hvis ikke bør tildeles samme dispositionskode til hele mængden af returlinjen, eller hvis du ikke har modtaget det fulde antal på linjen, skal du opdele linjen. Når du opdeler en modtagelseskladdelinjen, du også opdele returlinjen (**SalesLine**), og Opret et nyt parti-ID. Du kan opdele linjen ved at reducere antallet af modtagelseskladdelinjen. Når kladden bogføres, oprettes en ny return linje, der har status som **forventet** for den resterende mængde. Du kan også opdele linjen ved at klikke på **funktion**&gt;**Opdel**.

### <a name="process-the-quarantine-order"></a>Behandle karantæneordren

Hvis de returnerede produkter, som sendes til inspektion på karantænelagerstedet, foretages yderligere behandling i en karantæneordre. Oprettes der en karantæneordre for hver modtagelseslinje, der sendes i karantæne. Dispositionskoden, angiver resultatet af den inspektion. Du kan opdele en karantæneordre, ligesom du kan opdele modtagelseskladden. Hvis du opdele karantæneordren, kan du få en tilsvarende opdeling af returlinjen. Når dispositionskoden er angivet, skal du fuldføre karantæneordren enten ved hjælp af den **End** funktion eller den **færdigmelde** funktion. Hvis du vælger **færdigmelde**, oprettes der en ny ankomst i det angivne lagersted. Du kan derefter behandle denne ankomst ved hjælp af den **modtagelsesoversigt** side. Hvis ankomst stammer fra en karantæneordre, kan du ikke ændre den dispositionskode, der er tildelt under inspektionen. Hvis du fuldfører karantæneordren ved hjælp af den **End** funktion, partiet registreres automatisk. Nogle gange kan en vare sendes tilbage fra karantæne til forsendelses- og modtagelsesafdelingen. Karantæne inspektøren kan eksempelvis ikke ved, hvor varen opbevares på lageret. I dette tilfælde skal den tilsvarende følgeseddel opdateres for at registrere og reagere på den dispositionskode, der er angivet på grund af karantænen korrekt. Bekræftelse af modtagelsen kan sendes til kunden, når returlinjen registreres. Den **returnering** rapporten ligner returvareordre. Den **returnering** rapport, der ikke er journaliseret eller på anden måde er registreret i systemet, og det er ikke et nødvendigt trin i processen returordre.

## <a name="replace-a-product"></a>Erstatte et produkt
Der er to metoder til håndtering af produktet erstatning:

-   **Forudgående erstatning** – erstatte et produkt, før det returnerede produkt er modtaget fra kunden.
-   **Udskiftning af dispositionskode** – automatisk oprette en ny ordrelinje erstatning.

### <a name="up-front-replacement"></a>Forudgående erstatning

Erstatningsvaren kan leveres til kunden i forudgående erstatning, inden varen er returneret. Denne metode er nyttig, hvis for eksempel varen er en del af maskinen, som ikke kan fjernes, medmindre en reservedel, der kan overtage pladsen, eller hvis du bare vil kunden have erstatning produktet hurtigst muligt. Forudgående erstatning rækkefølge er en uafhængig salgsordre. Oplysningerne i hovedet er initialiseret fra kunden, og linjeoplysningerne initialiseres fra returvareordren. Du kan redigere, behandle og slette erstatningsordre uafhængigt af returordren. Når du sletter en erstatningsordre, modtager du en meddelelse, at ordren er oprettet som en erstatningsordre. I følgende illustration vises processen for forudgående erstatning.  

[![Forudgående erstatning proces](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)  

Returvareordren indeholder en reference til erstatningsordren. Hvis der oprettes en ordre for forudgående erstatning for en returordre, før de defekte varer returneres, kan du ikke vælge dispositionskoder for erstatning, efter at den defekte vare er blevet returneret.

### <a name="replacement-by-disposition-code"></a>Udskiftning af dispositionskode

Hvis du leverer en erstatningsvare til kunden, og du bruger den **Erstat og kasser** eller **Erstat og Krediter** dispositionshandling på den returordre, bruge den proces, der er vist i følgende illustration.  

[![Af udskiftningsprocessen, når der bruges en dispositionskode](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)  

Erstatningsvaren leveres ved hjælp af en uafhængig salgsordre, udskiftning af salgsordren. Denne salgsordre oprettes, når følgesedlen for returordren genereres. Ordrehovedet bruger oplysninger fra kunden, der refereres til i returordrehovedet. Oplysningerne i indsamles fra de oplysninger, der er angivet på den **erstatningsvare** side. Den **erstatningsvare** side skal være udfyldt for linjer, der har dispositionshandlingerne, der starter med ordet "Erstat". Dog er hverken antallet eller identiteten af erstatningsvaren godkendt eller begrænset. På denne måde kan i tilfælde, hvor kunden ønsker det samme element, men i en anden konfiguration eller størrelse, og også tilfælde, hvor kunderne ønsker en helt anden vare. Som standard angives en identisk vare på den **erstatningsvare** side. Du kan vælge et andet element, forudsat at der er oprettet af funktionen. **Bemærk:** du kan redigere og slette den udskiftningssalgsordre, når den er oprettet.

## <a name="generate-a-packing-slip"></a>Oprette en følgeseddel
Inden returnerede varer kan modtages på lageret, skal du opdatere følgesedlen for den ordre, at varerne tilhører. Ligesom opdateringsprocessen faktura er opdateringen af den økonomiske transaktion, følgesedlen er den fysiske opdatering af lagerposten. Med andre ord, forpligter denne proces ændringerne foretages på lageret. Ved returneringer bliver de trin, der tildeles dispositionshandlingen, implementeret under opdateringen af følgesedlen. Når du genererer følgesedlen, indtræffer følgende hændelser:

-   Den standardproces bruges til at udføre en fysisk tilgang på lageret. Finansposteringer oprettes, hvis lagermodel gruppe (**Bogfør fysisk varelager**) og Accounts receivable parameters (**Bogfør følgeseddel i Finans**) er indstillet korrekt.
-   Varer, der er markeret med en dispositionshandling, der indeholder ordet "spild" kasseres, og lager-tab bogføres i Finans.
-   Varer, der er mærket med den **Returner til kunde** dispositionshandlingen modtages og leveres til kunden. Disse elementer har ingen indflydelse på lageret.
-   Der oprettes en udskiftningssalgsordre. Denne salgsordre er baseret på oplysninger om den **erstatningsvare** side.

Du kan generere følgesedlen kun for linjer, der har statussen returnering af **registreret**, og kun for det fulde antal på returlinjer. Hvis flere linjer i returordren har den **registreret** status, kan du generere følgesedlen for en delmængde af linjerne ved at slette linjerne fra den **Bogfør følgeseddel** side. Delvis returnerer defineres ved hjælp af returordrelinjer, ikke på grundlag af returordreforsendelser. Derfor, hvis du modtager hele det antal, der er angivet på en returordrelinje, intet men fra de andre linjer i returordren, leveringen er ikke en delleverance. Men hvis en returordrelinje kræver, at 10 enheder af en vare returneres, men du får kun fire enheder, er leveringen en delleverance. Hvis ikke alle de forventede returvarer er ankommet, kan du sætte forsendelsen til side og vente på resten af det returnerede antal modtages. Alternativt kan du registrere og bogføre delmængden. Som en del af processen til bogføring af følgesedler, kan du knytte den referencenummer fra kundens forsendelsesdokumenterne til ordrelinjerne. Denne tilknytning er valgfri og er kun til reference. Den opretter ikke nogen transaktionsopdateringer. Generelt kan du springe på følgesedlen forsinkes proces og gå direkte til fakturering. I dette tilfælde er de trin, du har udført under pakningen slip generation udført under fakturering.

## <a name="generate-an-invoice"></a>Generér en faktura
Selvom de **returordre** side, der indeholder de oplysninger og handlinger, der er nødvendige for at håndtere de særlige logistiske aspekter af returordren, skal du bruge den **salgsordre** side til at fuldføre faktureringsprocessen. Organisationen kan derefter fakturere returordrer og salgsordrer samtidig og den samme person kan fuldføre faktureringsprocessen efter behov. Sådan får du vist returordre fra den **salgsordre** skal du klikke på linket at åbne den tilknyttede salgsordre Salgsordrenummeret. Du kan også finde returordren på den **alle Sales orders** side. Returnere ordrer, er ordrer, der har en af ordretypen **returneret ordre**.

### <a name="credit-correction"></a>Kreditrettelse

Kontroller, at eventuelle tillæg er korrekt, som en del af faktureringsprocessen. For at få de finanskonteringer bliver rettelser (Storno), bør du overveje at bruge den **kredit rettelse** indstilling på den **andre** tab af den **bogføring af faktura** side, når du bogfører fakturaen eller kreditnotaen. **Bemærk:** som standard, den **kredit rettelse** indstilling er aktiveret, hvis den **kreditnota som rettelse** indstilling på den **Accounts receivable parameters** side er blevet aktiveret. Vi anbefaler dog, at du ikke bogfører returnerer med Storno.

## <a name="create-intercompany-return-orders"></a>Oprette interne returordrer
Returordrer kan udføres mellem to firmaer i organisationen. Følgende scenarier understøttes:

-   Simple interne returneringer mellem to virksomheder, der deltager i en intern relation
-   En intern kæde, der er etableret, når der oprettes en returordre for kunden i den sælgende virksomhed
-   En intern kæde, der er etableret, når der oprettes en returordre for kreditoren i den købende virksomhed
-   Direkte levering levering returnerer mellem en ekstern kunde og to selskaber, der deltager i en intern relation

### <a name="setup"></a>Konfiguration

I følgende illustration minimumskrav til opsætning, der er nødvendig for to selskaber til at deltage i en interne forhold og drage fordel af intern handel.  

[![Minimum setup](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)  

CompBuy er den købende virksomhed i følgende scenario, og CompSell er den sælgende virksomhed. Normalt leveres den sælgende virksomhed varer enten køber eller, i scenarier for direkte levering levering, direkte til slutkunden. I CompBuy, kreditorens IC\_CompSell er defineret som et internt slutpunkt, der er tilknyttet firmaet CompSell. På samme tid, i CompSell, kunde IC\_CompBuy er defineret som et internt slutpunkt, der er tilknyttet firmaet CompBuy. De relevante oplysninger om politik og værditilknytninger skal være defineret i begge firmaer. En intern returordre, der også er en intern salgsordre, oprettes i en direkte levering leverance scenario i den sælgende virksomhed. RMA-nummeret for den interne returordre kan plukkes fra RMA-nummerserie i CompSell, eller den kan kopieres fra RMA-nummeret, der er tilknyttet den oprindelige salgsordre i CompBuy. Indstillingerne RMA-nummeret på den **PurchaseRequisition** handlingspolitikken i CompBuy bestemmer disse handlinger. Hvis der synkroniseres RMA-nummeret, skal du planlægge at minimere risikoen for antal kampe, hvis de to virksomheder kan bruge samme nummerserie.

### <a name="simple-intercompany-returns"></a>Simple interne returneringer

Dette scenario omfatter to firmaer i samme organisation, som vist i følgende illustration.  

[![Simple interne afkast](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)  

Ordrekæde kan etableres, når der oprettes en returordre for kreditoren i den købende virksomhed eller en kunde returordre oprettes i den sælgende virksomhed. Dynamics 365 for operationer opretter den tilsvarende ordre i et andet firma og sørger for, at oplysninger på kreditoren, hovedet returnerer rækkefølge afspejler indstillingerne for kunden returordre. Den returordre, der er etableret kan enten inkluderer eller udelader referencen (**Find salgsordre**) til en eksisterende debitorfaktura. Følgesedler og fakturaer i de to ordrer kan behandles individuelt. Du har ikke oprette en følgeseddel for returordren kreditor, før du genererer følgesedlen for returordren kunde.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Returnerer leverancen direkte levering mellem tre parter

Denne situation kan fastslås, hvis en tidligere salg af den **direkte levering** type er afsluttet, og hvis en faktura mod kunden findes i det firma, der arbejder sammen med kunden. I følgende illustration har virksomheden CompBuy tidligere solgt og produkter til ekstern kunden, der faktureres. Produkterne, der er leveret direkte fra firmaet CompSell til kunden via en intern ordrekæde.  

[![Returnerer leverancen direkte levering mellem tre parter](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)  

Hvis ekstern kunden ønsker at returnere produkter, oprettes en returordre (RMA02) for kunden i firmaet CompBuy. Hvis du vil oprette den interne kæde, mærkes returvareordren til direkte levering. Når du bruger den **Find salgsordre** funktion til at plukke debitorfakturaen, der skal returneres, er etableret en intern ordrekæde består af følgende dokumenter:

-   **Oprindelige returordre:** RMA02 (firma CompBuy)
-   **Indkøbsordre:** PO02 (firma CompBuy)
-   **Interne returordre:** RMA\_00032 (firma CompSell)

Når du har oprettet den interne kæde med direkte levering, alle fysiske håndtering og forarbejdning af opgørelserne skal forekomme i forbindelse med interne returordren, RMA\_00032 i virksomheden CompSell. Produkterne, der kan ikke modtages i virksomheden CompBuy. Når der tildeles en dispositionskode til interne returvareordren, synkroniseres de med den oprindelige returordre til at tillade korrekt fakturering af den oprindelige ordre.

## <a name="post-to-the-ledger"></a>Bogfører til Finans
De finanskonteringer, der genereres, når returvareordren faktureres er påvirket af et par vigtige indstillinger og parametre:

-   **Returnere kostpris** – For lager modeller, bortset fra **kostpris (Standard)**, **returnere kostpris** parameter bestemmer kostprisen for varen, når den har accepteret tilbage på lageret eller kasseres. Hvis du vil beregne en korrekt vurdering af lager, er det vigtigt, at du angiver den **returnere kostpris** parameter korrekt. Hvis du bruger den **Find salgsordre** funktion til at oprette en returordrelinje, der indeholder en reference til en debitorfaktura, den **returnere kostpris** værdi er lig med kostprisen for den vare, der sælges. Ellers værdien kostpris kommer fra vareopsætningen eller angives manuelt.
-   **Kredit rettelse/Storno** – **kredit rettelse** parameter på den **bogføring af faktura** side bestemmer, om bogføringer skal være registreret som positive (DR/CR) poster eller rette, negative poster.

Følgende eksempler, returkostprisen er repræsenteret som **Fakturaafrundingspræcision kostpris**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Eksempel 1: Returvareordren ikke henvise til en debitorfaktura

Returordren henvise ikke til en debitorfaktura. Den returnerede vare krediteres. Den **kredit rettelse** parameter ikke er markeret, når returvareordre, faktura eller kreditnota, der oprettes.  

[![Returordre henvise ikke til en kunde-invoic](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)  

**Bemærk:** master Vareprisen bruges som standardværdi for den **returnere kostpris** parameter. Standardprisen er forskellig fra kostprisen på tidspunktet for lagerafgang. Virkningen er derfor, at et tab på 3, der er påløbet. Desuden indeholder ikke returvareordren den rabat, der blev givet til kunden på salgsordren. Der opstår derfor en stor kredit.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Eksempel 2: Kreditrettelse er valgt for returordren

Eksempel 2 er den samme som eksempel 1, men **kredit rettelse** parameteren markeres, når fakturaen returordre oprettes.  

[![Returordre, hvor kreditrettelse er markeret](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)  

**Bemærk:** finansposteringer, der er angivet som negative rettelser.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Eksempel 3: Returordrelinjen er oprettet ved hjælp af funktionen Find salgsordre

I dette eksempel oprettes returordrelinjen ved hjælp af den **Find salgsordre** funktion. Den **kredit rettelse** parameter ikke er markeret, når fakturaen oprettes.  

[![Returnere en ordrelinje, der er oprettet ved hjælp af Søg-salgsordre](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)  

**Bemærk:****rabat** og **returnere kostpris** er angivet korrekt. Der opstår derfor en præcis tilbageførsel af kundens faktura.


