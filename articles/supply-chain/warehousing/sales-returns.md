---
title: Salgsreturneringer
description: "Dette emne indeholder oplysninger om processen for returordrer. Det indeholder oplysninger om returneringer fra kunder og deres virkning på efterkalkulation og disponible lagerantal."
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fa56911c19e9b6514829084221ba03c7cd421c92
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="sales-returns"></a>Salgsreturneringer

[!include[banner](../includes/banner.md)]


Dette emne indeholder oplysninger om processen for returordrer. Det indeholder oplysninger om returneringer fra kunder og deres virkning på efterkalkulation og disponible lagerantal.

Kunder kan returnere varer af forskellige årsager. En vare kan f.eks. være defekt, eller den opfylder ikke kundens forventninger. Returvareprocessen starter, når en kunde afgiver en anmodning om at returnere en vare. Når kundens anmodning er modtaget, oprettes en returordre i Microsoft Dynamics 365 for Finance and Operations.

## <a name="return-order-process"></a>Returordreproces
I følgende illustration vises en oversigt over returvareprocessen.  

[![Returordreproces](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Der er to typer returordreprocesser: fysisk returnering og kun kreditering.

-   **Fysisk returnering** – Returordren godkender den fysisk returnering af produkter.
-   **Kun kreditering** – Returordren godkender en kundekreditering, men kræver ikke, at kunden fysisk returnerer varerne.

### <a name="physical-return-order-process"></a>Fysisk returordreproces

1.  **Opret en returordre.** Dokumenterer formelt godkendelsen til kunden til at returnere alle defekte eller uønskede produkter. Returordren kræver ikke, at virksomheden accepterer de returnerede produkter eller giver kunden en kreditnota. Hvis returneringen accepteret, kan du godkende, at en erstatningsvare sendes, før den defekt vare er blevet returneret.
2.  **Ankommer til lageret til inspektion.** Fuldfør en indledende kontrol, og valider i forhold til returordredokumentet. Returordren understøtter også karantæne af de returnerede varer for yderligere inspektion og kvalitetskontrol.
3.  **Bestem disposition.** Afslut inspektionsprocessen, og beslut, hvad der skal ske med de returnerede produkter. Som en del af dette trin skal du beslutte, om du vil kreditere kunden, afvise produktreturneringen eller acceptere produktreturneringen, skrot produktet, og send derefter et erstatningsprodukt til kunden.
4.  **Generér en følgeseddel.** Generér en følgeseddel, og udfør den dispositionsbeslutning, du foretog i trin 3. Færdiggør logistikprocesserne.
5.  **Generér en faktura.** Luk returordren.

### <a name="credit-only-process"></a>Proces for kun kreditering

1.  **Opret en returordre.** Dokumenterer formelt godkendelsen til kunden til at modtage en kreditnota uden at returnere de defekte eller uønskede produkter. Dispositionskoden **Kun kreditering** godkender beslutningen om, at kreditere kunden uden fysisk returnering.
2.  **Generér en faktura.** Generér en kreditnota, og luk derefter returordren.

## <a name="return-material-authorization"></a>RMA (Return Materials Authorization)
RMA-behandling (Return Material Authorization) bygger på salgsordrefunktionalitet. En RMA er registreret som en returordre, der er oprettet som en salgsordre, og kan have en anden salgsordre, der er knyttet til den, kaldes en erstatningsordre. Begge salgsordrer sammenkædes med det oprindelige RMA-nummer.

-   **Returordre** – For at registrere en RMA, opretter du en returordre, som er en salgsordre, der er tildelt typen, **Returneret ordre.** De ændringer, du foretager af RMA-oplysningerne, opdateres automatisk i salgsordren. Indtil returordren har status **Åben**, vises den ikke på listen over salgsordrer. Du kan bruge RMA til at håndtere ankomsten og modtagelsen af de returnerede varer samt til at godkende dispositionshandlingen kun kreditering (se afsnittet **Dispositionskoder og dispositionshandlinger**). Alle andre opfølgende processer skal håndteres i salgsordren.
-   **Erstatningsordre** – Når en erstatningsordre skal leveres til kunden, kan RMA'en kan omfatte en anden tilknyttede salgsordre. Du kan manuelt oprette en erstatningsordre for RMA'en til at understøtte for øjeblikkelig levering. Alternativt kan erstatningsordren oprettes automatisk efter modtagelse, inspektion og kvittering er fuldført for det RMA-linjeelement, der har en dispositionskode, der angiver erstatning. Erstatningsordren har de samme funktioner, der er knyttet til en salgsordre. Du kan f.eks. bruge den til at konfigurere et brugerdefineret produkt som erstatningsvare, oprette en produktionsordre for at reparere en returneret vare, oprette en indkøbsordre til direkte levering for at sende erstatningen fra en leverandør eller understøtte andre formål.

## <a name="create-a-return-order"></a>Oprette en returordre
Returordreprocessen starter, når en kunde kontakter organisationen for at returnere et defekt eller uønsket produkt og/eller for at få en kreditnota. Når din virksomhed accepterer returnering, dokumenteres returneringen ved en returordre. Denne returordre bliver kontaktpunktet i den interne behandling af det returnerede produkt. Følgende illustration viser fremgangsmåden for oprettelse af en returordre.  

[![Fremgangsmåde for oprettelse af en returordre](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Opret et returordrehoved.

Når du opretter en returordre, skal oplysningerne i følgende tabel medtages.

| Felt              | Betegnelse                                              | Bemærkninger                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Debitorkonto   | En reference til kundetabellen                       | Du skal angive en eksisterende kundekonto.                                                                                                                                                                                                                                                                                                  |
| Leveringsadresse   | Den adresse, som varen er returneret til.                 | Organisationens adresse bruges som standard. Hvis et bestemt lagersted er markeret i hovedet, ændres leveringsadressen til leveringsadressen på lageret. Du kan ændre denne adresse på siden **Oplysninger om returordre**.                                                                                                  |
| Sted/lagersted     | Det sted eller lagersted, der modtager det returnerede produkt | Leveringsadressen for returordren bestemmes baseret på leveringsadressen på stedet eller lagerstedet.                                                                                                                                                                                                                                 |
| RMA-nummer (Return Materials Authorization-nummer)         | Det id, der er tilknyttet returordren.              | RMA-nummeret bruges som en alternativ nøgle under hele returordreprocessen. RMA-nummeret, der tildeles på basis af den RMA-nummerserie, der er konfigureret på siden **Debitorparametre**.                                                                                                                              |
| Frist           | Den seneste dato, hvor en vare kan returneres               | Standardværdien beregnes som dags dato plus gyldighedsperioden. Hvis en returnering f.eks. kun er gyldig i 90 dage fra den dato, hvor returordren oprettes, og returordren blev oprettet den 1. maj, er værdien i feltet **30. juli**. Gyldighedsperioden angives på siden **Debitorparametre**. |
| Årsagskode for returnering | Kundens årsag til at returnere produktet.          | Årsagskoden vælges på listen over brugerdefinerede årsagskoder. Du kan opdatere dette felt når som helst.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Opret returordrelinjer

Når du har fuldført returneringshovedet, kan du oprette returlinjer ved hjælp af en af følgende metoder:

-   Du kan angive oplysninger om varen, antal og andre oplysninger for hver returvarelinje manuelt.
-   Opret en returlinje ved hjælp af funktionen **Find salgsordre**. Vi anbefaler, at du bruger denne funktion, når du opretter en returordre. Funktionen **Find salgsordre** opretter en reference fra returlinjen til den fakturerede salgsordrelinje og henter linjeoplysninger som varenummer, antal, pris, rabat og omkostningsværdier fra salgslinjen. Referencen er med til at sikre, at når produktet returneres til virksomheden, er det værdisat til samme kostpris, som det blev solgt til. Referencen validerer også, at der ikke oprettes returordrer for en mængde, der overstiger det antal, der blev solgt på fakturaen.

**Bemærk:** Returlinjer, der har en reference til en salgsordre, skal håndteres som rettelser eller tilbageførsler af salget. Du kan finde flere oplysninger i afsnittet "Bogfør i finans" senere i dette emne.

### <a name="charges"></a>Tillæg

Gebyrer og afgifter kan føjes til returordren gennem en eller flere af følgende metoder:

-   Du kan manuelt føje tillæg til returordrehovedet, returordrelinjen eller begge dele.
-   Gebyrer kan føjes automatisk til returordrehovedet som funktion af returårsagskoden.
-   Gebyrer kan føjes automatisk til returordrelinjen baseret på linjens dispositionskode.

Gebyrer tilføjes automatisk efter en returårsagskode eller dispositionskode, der er knyttet til linjen. Hvis årsagskoden ændres senere, fjernes den eksisterende gebyrpost ikke, men en ny gebyrpost kan tilføjes på basis af den nye årsagskode. Når du føjer gebyrer til returordrelinjer, bliver gebyrer, der beregnes som en procentdel af linje- eller ordreværdien, negative, når linjen eller linjeordren er negativ, medmindre procentdelen også er et negativt tal. Et gebyr, der har en negativ værdi, repræsenterer en kreditering til kunden.

### <a name="return-reason-codes"></a>Årsagskoder for returneringer

Ved at anvende årsagskoder til returneringer, kan du hjælpe med til at gøre det nemmere at analysere returmønstre. Årsagskoder indeholder oplysninger om, hvorfor en kunde ønsker at returnere varer. Nogle organisationer har mange årsagskoder. Disse organisation kan gruppere årsagskoderne til årsagskodegrupper for at få et bedre overblik og for at få akkumuleret rapportering.

### <a name="disposition-codes-and-disposition-actions"></a>Dispositionskoder og dispositionshandlingerne

Et vigtigt skridt i returordreprocessen er tildelingen af en dispositionskode til returordrelinjen som en del af modtagelsesregistreringen. Dispositionskoden bestemmer følgende oplysninger:

-   **De finansielle følger** – Skal kunden krediteres for de returnerede varer, og skal eventuelle gebyrer føjes til returordrelinjen?
-   **Disponeringen af den returnerede vare** – Skal varen føjes til lageret igen, skal den kasseres, eller skal den sendes tilbage til kunden?
-   **Logistik for den returnerede vare** – Skal der udstedes en erstatningsvare til kunden?

Foruden fastlæggelsen af, hvordan de returnerede varer skal disponeres, kan dispositionskoder medføre, at der skal påføres gebyrer til returlinjen. De kan også bruges til at gruppere returneringer til statistiske analyser. Dispositionskoder er defineret som en del af opsætningen af returordrer. Men hver dispositionskode skal referere til en af de indbyggede dispositionshandlinger. Følgende tabel indeholder de indbyggede dispositionskoder og deres handlinger. **Vigtigt:** Hvis en vare ikke skal returneres, men kunden stadig skal krediteres, skal dispositionskoden **Kun kreditering** tildeles til returlinjen.

<table>
<thead>
<tr class="header">
<th>Dispositionskode</th>
<th>Finansielle konsekvenser</th>
<th>Konsekvenser for logistik</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Krediter kun</td>
<td><ul>
<li>Kunden krediteres salgsprisen minus eventuelle gebyrer eller afgifter.</li>
<li>Tab fra kassationen af varen bogføres i Finans.</li>
</ul></td>
<td>Varen skal ikke returneres. Denne dispositionshandling bruges i følgende tilfælde:
<ul>
<li>Der er tilstrækkelig tillid mellem parterne.</li>
<li>Udgiften til returnering af den defekte vare er for stor.</li>
<li>Det kan ikke tillades, at varerne sendes tilbage til lageret. På grund af andre betingelser er en fysisk returnering ikke længere nødvendig.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kredit</td>
<td><ul>
<li>Kunden krediteres salgsprisen minus eventuelle gebyrer eller afgifter.</li>
<li>Lagerværdien forøges med omkostningerne ved den returnerede vare.</li>
</ul></td>
<td>Varen returneres og føjes til lageret igen.</td>
</tr>
<tr class="odd">
<td>Erstat og krediter</td>
<td><ul>
<li>Kunden krediteres salgsprisen minus eventuelle gebyrer eller afgifter.</li>
<li>Lagerværdien forøges med omkostningerne ved den returnerede vare.</li>
<li>En separat salgsordre for en erstatning oprettes og håndteres separat.</li>
</ul></td>
<td>Varen returneres og føjes til lageret igen.</td>
</tr>
<tr class="even">
<td>Erstat og kasser</td>
<td><ul>
<li>Kunden krediteres salgsprisen minus eventuelle gebyrer eller afgifter.</li>
<li>Tab fra kassationen af varen bogføres i Finans.</li>
<li>En separat salgsordre for en erstatning oprettes og håndteres separat.</li>
</ul></td>
<td>Varen returneres og kasseres.</td>
</tr>
<tr class="odd">
<td>Returner til kunde</td>
<td>Ingen, bortset fra eventuelle gebyrer eller afgifter.</td>
<td>Varen returneres, men sendes tilbage til kunden efter besigtigelse. Denne dispositionshandlingen kan bruges, hvis varen bevidst er blevet beskadiget, eller hvis garantien er afvist.</td>
</tr>
<tr class="even">
<td>Kasseres</td>
<td><ul>
<li>Kunden krediteres salgsprisen minus eventuelle gebyrer eller afgifter.</li>
<li>Tab fra kassationen af varen bogføres i Finans.</li>
</ul></td>
<td>Varen returneres eller kasseres.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Ankommer til lageret til inspektion
Før du kan modtage returnerede varer på lageret fysisk ved at bogføre en følgeseddel, skal varerne gennemgå ankomstregistrering og valgfri inspektion. I følgende illustration vises en oversigt over ankomstprocessen. I følgende afsnit beskrives de enkelte trin, som vises i illustrationen.  

[![Modtagelsesproces](./media/salesreturn03.png)](./media/salesreturn03.png)  

Processen har flere andre variationer, som ikke er beskrevet i dette emne. Her er nogle af disse variationer.

-   Brug ikke listen **Modtagelsesoversigt** til at oprette en modtagelseskladde. Opret i stedet modtagelseskladden manuelt. Returordrer har **Salgsordre** som reference.
-   Hvis du bruger lokationsstyring, kan du generere palletransporter. Returlinjen får status som **Ankommet** under palletransport.
-   Registrer modtagelsen af den returnerede vare direkte fra returordrelinjen ved hjælp af funktionen **Registrering**.

Under ankomstprocessen integreres returneringer med den generelle proces til modtagelse af lager. Modtagelsesprocessen understøtter også oprettelse af karantæneordrer for returnerede varer, der skal underkastes en særskilt undersøgelse.

### <a name="identify-products-in-the-arrival-overview-list"></a>Identificer produkter på listen Modtagelsesoversigt

Siden **Modtagelsesoversigt** viser en liste over alle planlagte indgående modtagelser. **Bemærk:** Modtagelser fra returordrer skal behandles separat i forhold til andre typer af transaktioner ved ankomsten. Når du har identificeret en indgående pakke på siden **Modtagelsesoversigt** (for eksempel ved hjælp af det ledsagende RMA-dokument), skal du i handlingsruden klikke på **Start modtagelse** for at oprette og initialisere en modtagelseskladde, der svarer til modtagelsen.

### <a name="edit-the-arrival-journal"></a>Rediger modtagelseskladden

Når du angiver indstillingen **Karantænestyring** til **Ja**, kan du oprette en karantæneordre for returlinjen. Hvis en linje er blevet sendt i karantæne for inspektion, kan du ikke angive en dispositionskode. **Bemærk:** Hvis du angiver indstillingen **Karantænestyring** til **Ja** i varens lagermodelgruppe, vil indstillingen **Karantænestyring** på siden **Kladdelinjer** være markeret for modtagelseskladdelinjen, og den kan ikke ændres. Hvis linjen sendes i karantæne, skal du angive det relevante karantænelagersted. Hvis modtagelseslinjen ikke sendes til inspektion, skal lagerstedets modtagelsesassistent angive dispositionskoden direkte på modtagelseskladdelinjen og derefter bogføre modtagelseskladden. Hvis den samme dispositionskode ikke skal tildeles til hele mængden på returlinjen, eller hvis du ikke har modtaget det fulde antal på linjen, skal du opdele linjen. Når du opdeler en modtagelseskladdelinje, opdeler du også returlinjen (**SalesLine**) og opretter et nyt parti-ID. Du kan opdele linjen ved at reducere antallet på modtagelseskladdelinjen. Når kladden bogføres, oprettes en ny returlinje, der har status som **Forventet** for den resterende mængde. Du kan også opdele linjen ved at klikke på **Funktioner** &gt; **Opdel**.

### <a name="process-the-quarantine-order"></a>Behandl karantæneordren

Hvis de returnerede produkter sendes til inspektion på karantænelagerstedet, foretages der yderligere behandling i en karantæneordre. Der oprettes én karantæneordre for hver modtagelseslinje, der sendes i karantæne. Dispositionskoden angiver resultatet af inspektionsprocessen. Du kan opdele en karantæneordre, ligesom du kan opdele modtagelseskladden. Hvis du opdele karantæneordren, kan du få en tilsvarende opdeling af returlinjen. Når dispositionskoden er angivet, skal du fuldføre karantæneordren ved hjælp af enten funktionen **Afslut** eller funktionen **Færdigmeld**. Hvis du vælger **Færdigmeld**, oprettes der en ny modtagelse i det angivne lagersted. Du kan derefter behandle denne ankomst ved hjælp af siden **Modtagelsesoversigt**. Hvis modtagelsen stammer fra en karantæneordre, kan du ikke ændre den dispositionskode, der er tildelt under inspektionen. Hvis du fuldfører karantæneordren ved hjælp af funktionen **Afslut**, registreres partiet automatisk. Nogle gange sendes en vare måske tilbage fra karantæne til forsendelses- og modtagelsesafdelingen. Hvis karantæneinspektøren f.eks. ikke ved, hvor varen skal opbevares på lageret. I dette tilfælde skal den tilsvarende følgeseddel opdateres for korrekt at registrere og reagere på den dispositionskode, der er angivet på grund af karantænen. Bekræftelse af modtagelsen kan sendes til kunden, når returlinjen registreres. Rapporten **Bekræftelse af returnering** ligner returordredokumentet. Rapporten **Bekræftelse af returnering** journaliseres ikke eller registreres på anden måde i systemet, og det er ikke et nødvendigt trin i returordreprocessen.

## <a name="replace-a-product"></a>Erstat et produkt
Der er to metoder til håndtering af produkterstatning:

-   **Forudgående erstatning** – Erstat et produkt, før det returnerede produkt modtages fra kunden.
-   **Udskiftning af dispositionskode** – Opret automatisk en ny erstatningsordrelinje.

### <a name="up-front-replacement"></a>Forudgående erstatning

I forudgående erstatning kan erstatningsvaren leveres til kunden, inden varen er returneret. Denne metode er nyttig, hvis varen f-eks. er en del af en maskine, som ikke kan fjernes, medmindre der er en reservedel tilgængelig til at overtage pladsen, eller hvis du bare ønsker, at kunden skal have erstatningsproduktet så hurtigst muligt. Forudgående erstatning-ordren er en uafhængig salgsordre. Oplysningerne i hovedet er initialiseret fra kunden, og linjeoplysningerne initialiseres fra returordren. Du kan redigere, behandle og slette erstatningsordre uafhængigt af returordren. Når du sletter en erstatningsordre, modtager du en meddelelse om, at ordren er oprettet som en erstatningsordre. I følgende illustration vises processen for forudgående erstatning.  

![Proces for forudgående erstatning](./media/SalesReturn04.png)

Returordren indeholder en reference til erstatningsordren. Hvis der oprettes en ordre for forudgående erstatning for en returordre, før de defekte varer returneres, kan du ikke vælge dispositionskoder for erstatning, når den defekte vare er blevet returneret.

### <a name="replacement-by-disposition-code"></a>Udskiftning af dispositionskode

Hvis du leverer en erstatningsvare til kunden, og du bruger dispositionshandlingerne **Erstat og kassér** eller **Erstat og krediter** på returordren, skal du bruge den proces, der er vist i følgende illustration.  

![Udskiftningsproces, når der bruges en dispositionskode](./media/SalesReturn05.png)

Erstatningsvaren leveres ved hjælp af en uafhængig salgsordre, udskiftningssalgsordren. Denne salgsordre oprettes, når følgesedlen for returordren genereres. Ordrehovedet bruger oplysninger fra kunden, der refereres til i returordrehovedet. Linjeoplysningerne indsamles fra de oplysninger, der er angivet på siden **Erstatningsvare**. Siden **Erstatningsvare** side skal være udfyldt for linjer, der har dispositionshandlinger, der starter med ordet "Erstat". Dog er hverken antallet eller identiteten af erstatningsvaren godkendt eller begrænset. På denne måde er der mulighed for tilfælde, hvor kunden ønsker den samme vare, men i en anden konfiguration eller størrelse, og også for tilfælde hvor kunderne ønsker en helt anden vare. Som standard angives en identisk vare på siden **Erstatningsvare**. Men du kan vælge en anden vare, forudsat at funktionen er konfigureret. **Bemærk:** Du kan redigere og slette erstatningssalgsordren, når den er oprettet.

## <a name="generate-a-packing-slip"></a>Generér en følgeseddel
Før returnerede varer kan modtages på lager, skal du opdatere følgesedlen for den ordre, som varerne tilhører. Ligesom fakturaopdateringsprocessen er opdateringen af den økonomiske transaktion, er følgeseddelopdateringsprocessen den fysiske opdatering af lagerposten. Denne proces indfører med andre ord ændringerne på lageret. Ved returneringer bliver de trin, der tildeles dispositionshandlingen, implementeret under opdateringen af følgesedlen. Når du genererer følgesedlen, indtræffer følgende hændelser:

-   På lageret bruges standardprocessen til at udføre en fysisk tilgang på lageret. Finansposteringer oprettes, hvis lagermodelgruppen (**Bogfør fysisk varelager**) og debitorparametrene (**Bogfør følgeseddel i Finans**) er indstillet korrekt.
-   Varer, der er markeret med en dispositionshandling, der indeholder ordet "kassation" kasseres, og lagertabet bogføres i Finans.
-   Varer, der er mærket med dispositionshandlingen **Returner til kunde**, modtages og leveres til kunden. Disse varer har ingen indflydelse på lageret.
-   Der oprettes en erstatningssalgsordre. Denne salgsordre er baseret på oplysninger på siden **Erstatningsvare**.

Du kan generere følgesedlen kun for linjer, der har returneringsstatussen **Registreret**, og kun for det fulde antal på returlinjen. Hvis flere linjer i returordren har statussen **Registreret**, kan du generere følgesedlen for en delmængde af linjerne ved at slette linjerne fra siden **Bogfør følgeseddel**. Delleverancer defineres ved hjælp af returordrelinjer, ikke ved hjælp af returordreforsendelser. Hvis du derfor modtager hele det antal, der er angivet på én returordrelinje, men intet fra de andre linjer i returordren, er leverancen ikke en delleverance. Hvis en returordrelinje derimod angiver, at ti enheder af en vare skal returneres, men du kun modtager fire, er det en delleverance. Hvis ikke alle de forventede returvarer er ankommet, kan du sætte forsendelsen til side og vente på at resten af det returnerede antal ankommer. Alternativt kan du registrere og bogføre delmængden. Som en del af posteringsprocessen for følgesedler, kan du knytte følgesedlens referencenummer fra kundens forsendelsesdokumenter til ordrelinjerne. Denne tilknytning er valgfri og er kun til orientering. Den opretter ikke nogen transaktionsopdateringer. Generelt kan du springe over følgeseddelprocessen og gå direkte til fakturering. I dette tilfælde færdiggøres de trin, du vil have udført under genereringen af følgesedlen, under fakturering.

## <a name="generate-an-invoice"></a>Generér en faktura
Selvom siden **Returordre** indeholder de oplysninger og handlinger, der er nødvendige for at håndtere de særlige logistiske aspekter af returordren, skal du bruge siden **Salgsordre** til at fuldføre faktureringsprocessen. Din organisation kan derefter fakturere returordrer og salgsordrer samtidig, og den samme person kan fuldføre faktureringsprocessen efter behov. Hvis du vil have vist returordren fra siden **Salgsordre**, skal du klikke på linket til salgsordrenummeret for at åbne den tilknyttede salgsordre. Du kan også finde returordren på siden **Alle salgsordrer**. Returordrer er salgsordrer, der har ordretypen **Returneret ordre**.

### <a name="credit-correction"></a>Kreditrettelse

Kontroller, at forskellige gebyrer er korrekte, som en del af faktureringsprocessen. For at få finansposterringerne til at blive rettelser (Storno), bør du overveje at bruge indstillingen **Kreditrettelse** under fanen **Andet** på siden **Bogføring af faktura**, når du bogfører fakturaen eller kreditnotaen. **Bemærk:** Som standard er indstillingen **Kreditrettelse** aktiveret, hvis indstillingen **Kreditnota som rettelse** er blevet aktiveret på siden **Debitorparametre**. Vi anbefaler dog, at du ikke bogfører returneringer med Storno.

## <a name="create-intercompany-return-orders"></a>Opret interne ordrer
Returordrer kan udføres mellem to firmaer i organisationen. Følgende scenarier understøttes:

-   Enkle interne returneringer mellem to virksomheder, der deltager i en intern relation
-   En intern kæde, der er etableret, når der oprettes en returordre for kunden i den sælgende virksomhed
-   En intern kæde, der er etableret, når der oprettes en returordre til leverandøren i den købende virksomhed
-   Forsendelsesreturneringen med direkte levering mellem en ekstern kunde og to selskaber, der deltager i en intern relation

### <a name="setup"></a>Konfiguration

Følgende illustration viser minimumskravet til opsætning, der er nødvendig for at to selskaber kan deltage i en intern relation og drage fordel af intern handel.  

![Minimumskrav til opsætning](./media/SalesReturn06.png)

I følgende scenarie er CompBuy den købende virksomhed, og CompSell er den sælgende virksomhed. Normalt leverer den sælgende virksomhed varer til enten den købende virksomhed eller i scenarier med direkte levering direkte til slutkunden. I CompBuy er kreditoren IC\_CompSell defineret som et internt slutpunkt, der er tilknyttet firmaet CompSell. I CompSell er kunden IC\_CompBuy samtidig defineret som et internt slutpunkt, der er tilknyttet firmaet CompBuy. De relevante oplysninger om handlingspolitik og værditilknytninger skal være defineret i begge firmaer. I et scenarie med direkte levering oprettes en intern returordre, der også er en intern salgsordre, i den sælgende virksomhed. RMA-nummeret for den interne returordre kan hentes fra RMA-nummerserien i CompSell, eller den kan kopieres fra RMA-nummeret, der er tilknyttet den oprindelige returordre i CompBuy. Indstillingerne for RMA-nummer på handlingspolitikken **PurchaseRequisition** i CompBuy bestemmer disse handlinger. Hvis RMA-nummeret synkroniseres, skal du planlægge at minimere risikoen for sammenfald af numre, hvis de to virksomheder bruger samme nummerserie.

### <a name="simple-intercompany-returns"></a>Enkle interne returneringer

Dette scenario omfatter to firmaer i samme organisation, som vist i følgende illustration.  

![Enkel intern returnering](./media/SalesReturn07.png)

Ordrekæden kan etableres, når der oprettes en returordre til leverandøren i den købende virksomhed, eller der oprettes en kundereturordre i den sælgende virksomhed. Finance and Operations opretter den tilsvarende ordre i et andet firma og sørger for, at hoved- og linjeoplysningerne på returordren til leverandøren afspejler indstillingerne for kundereturordren. Den returordre, der er oprettet, kan enten inkludere eller udelade referencen (**Find salgsordre**) til en eksisterende debitorfaktura. Følgesedler og fakturaer i de to ordrer kan behandles individuelt. Du behøver f.eks. ikke at oprette en følgeseddel for returordren til leverandøren, før du genererer følgesedlen til kundereturordren.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Returneringer af direkte leveringer mellem tre parter

Dette scenarie kan opstå, hvis et tidligere salg af typen **Direkte levering** er afsluttet, og hvis der findes en faktura til kunden i det firma, der arbejder sammen med kunden. I følgende illustration har virksomheden CompBuy tidligere solgt og faktureret produkter til kunden Extern. Produkterne blev leveret direkte fra firmaet CompSell til kunden via en intern ordrekæde.  

![Returneringer af direkte leveringer mellem tre parter](./media/SalesReturn08.png)

Hvis kunden Extern ønsker at returnere produkterne, oprettes der en returordre (RMA02) for kunden i firmaet CompBuy. Hvis du vil oprette den interne kæde skal returvareordren mærkes til direkte levering. Når du bruger funktionen **Find salgsordre** til at finde debitorfakturaen, der skal returneres, etableres en intern ordrekæde, der består af følgende dokumenter:

-   **Oprindelig returordre:** RMA02 (firma CompBuy)
-   **Indkøbsordre:** PO02 (firma CompBuy)
-   **Intern returordre:** RMA\_00032 (firma CompSell)

Når den interne kæde med direkte levering er oprettet, skal al fysisk håndtering og behandling af returneringer foregå i forbindelse med den interne returordre, RMA\_00032 i firmaet CompSell. Produkterne kan ikke modtages i virksomheden CompBuy. Når der tildeles en dispositionskode til den interne returvareordre, synkroniseres den med den oprindelige returordre for at tillade korrekt fakturering af den oprindelige ordre.

## <a name="post-to-the-ledger"></a>Bogfør i finans
De finansposteringer, der genereres, når returvareordren faktureres, er påvirket af et par vigtige indstillinger og parametre:

-   **Returkostpris** – For lagermodeller, bortset fra **Standardomkostning**, bestemmer parameteren **Returkostpris** kostprisen for varen, når den er accepteret tilbage på lageret eller kasseret. Hvis du vil beregne en korrekt vurdering af lageret, er det vigtigt, at du angiver parameteren **Returkostpris** korrekt. Hvis du bruger funktionen **Find salgsordre** til at oprette en returordrelinje, der indeholder en reference til en debitorfaktura, er værdien **Returkostpris** lig med kostprisen for den vare, der sælges. Ellers kommer kostprisværdien fra vareopsætningen eller angives manuelt.
-   **Kreditrettelse/Storno** – Parameteren **Kreditrettelse** på siden **Bogføring af faktura** bestemmer, om posteringer skal registreres som positive (DR/CR)-poster eller som korrigerende negative poster.

I følgende eksempler er returkostprisen repræsenteret som **Fakturakostpris**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Eksempel 1: Returvareordren henviser ikke til en debitorfaktura

Returvareordren henviser ikke til en debitorfaktura. Den returnerede vare krediteres. Parameteren **Kreditrettelse** er ikke markeret, når returordrefakturaen eller -kreditnotaen oprettes.  

![Returordren henviser ikke til en debitorfaktura](./media/SalesReturn09.png)  

**Bemærk:** Varens stampris bruges som standardværdi for parameteren **Returkostpris**. Standardprisen er forskellig fra kostprisen på tidspunktet for lagerafgangen. Virkningen er derfor, at der opstår et tab på 3. Desuden indeholder returordren ikke den rabat, der blev givet til kunden på salgsordren. Der opstår derfor en for stor kreditering.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Eksempel 2: Kreditrettelse er valgt for returordren

Eksempel 2 er det samme som eksempel 1, men parameteren **Kreditrettelse** er markeret, når returordrefakturaen oprettes.  

![Returordre, hvor kreditrettelse er markeret ](./media/SalesReturn10.png)  

**Bemærk:** Finansposteringerne angives som negative rettelser.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Eksempel 3: Returordrelinjen er oprettet ved hjælp af funktionen Find salgsordre

I dette eksempel oprettes returordrelinjen ved hjælp af funktionen **Find salgsordre**. Parameteren **Kreditrettelse** er ikke markeret, når fakturaen oprettes.  

![Returordrelinje, der er oprettet ved hjælp af Find salgsordre ](./media/SalesReturn11.png)  

**Bemærk:** **Rabat** og **Returkostpris** er angivet korrekt. Der opstår derfor en præcis tilbageførsel af kundens faktura.




