---
title: Ruter og operationer
description: Dette emne indeholder en beskrivelse af ruter og operationer.
author: sorenva
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable, ProdRouteJob, ProdRouteTrans, ProdRouteOverview, ProdRouteJobOverview, ProdRouteJobListPagePreviewPane, RouteTable, RouteVersionFeasibility, ProdRouteJobCurrent, RouteGroup, RouteProductionOrder, EngChgCaseRouteTablePart, EcoResProductProdTypeFormulaNoActiveRouteFormPart,
ms.author: sorenand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6be472336ce8ea58973e897c42f6ee9ae92c0761
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819274"
---
# <a name="routes-and-operations"></a>Ruter og operationer

[!include [banner](../includes/banner.md)]

Dette emne indeholder en beskrivelse af ruter og operationer. En rute definerer processen til fremstilling af et produkt eller en produktvariant. Den beskriver hvert trin (operation) i produktionsprocessen, og den rækkefølge, som disse trin skal udføres i. For hvert trin definerer ruten også de krævede operationsressourcer, den krævede opstillingstid og operationstid, og hvordan omkostningerne skal beregnes.

<a name="overview"></a>Overblik
--------

En rute beskriver rækkefølgen af operationer, der kræves for at producere et produkt eller en produktvariant. For hver operation definerer ruten også de operationsressourcer, der skal bruges, den tid, der kræves for at opsætte og udføre operationen, og hvordan omkostningerne skal beregnes. Du kan bruge den samme rute til at producere flere produkter, eller du kan definere en entydig rute for hvert produkt eller produktvariant. Du kan også have flere ruter til samme produkt. I dette tilfælde varierer den rute, der bruges, afhængigt af faktorer som det antal, der skal produceres. Definitionen af en rute i Supply Chain Management består af fire separate elementer, der tilsammen beskriver produktionsprocessen:

- **Rute** – En rute, der definerer strukturen i produktionsprocessen. Med andre ord, definerer den rækkefølgen af operationer.
- **Operation** – En operation identificerer et navngivet trin i en rute, f.eks. **Montage**. Den samme operation kan forekomme i flere ruter og kan have forskellige operationsnumre.
- **Operationsrelation** – En operationsrelation definerer operationelle egenskaber for en operation, f.eks. opstillingstid og procestid, omkostningskategorier, forbrugsparametre og ressourcekrav. Operationsrelationen gør det muligt, at de operationelle egenskaber for en operation varierer, afhængigt af den rute, der skal bruges i operationen, eller de produkter, der produceres.
- **Ruteversion** – En ruteversion, der definerer den rute, der bruges til at producere et produkt eller en produktvariant. Ruteversioner giver mulighed for, at ruter kan genbruges på tværs af produkter eller ændres med tiden. De kan også aktivere forskellige ruter til at blive brugt til at fremstille det samme produkt. I dette tilfælde afhænger den rute, der bruges, af faktorer som lokalitet eller det antal, der skal produceres.

## <a name="routes"></a>Ruter
En rute beskriver rækkefølgen af operationer, der bruges for at producere et produkt eller en produktvariant. Hver operation er tildelt et operationsnummer og en efterfølgende operation. Rækkefølgen af operationer udgør et rutenetværk, der kan repræsenteres af et styret diagram, der har et eller flere startpunkter og et enkelt slutpunkt. I Supply Chain Management adskiller ruter sig på grundlag af typen af struktur. De to typer ruter er simple ruter og rutenetværk. I produktionsstyringsparametrene kan du angive, om kun simple ruter kan bruges, eller om der kan bruges mere komplekse rutenetværk.

### <a name="simple-routes"></a>Simple ruter

En simpel rute er sekventiel, og der er kun et udgangspunkt for ruten.  

[![Simpel rute](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Hvis du kun aktiverer simple ruter i produktionsstyringsparametrene, genererer Supply Chain Management automatisk operationsnumrene (10, 20, 30 og så videre), når du definerer ruten.

### <a name="route-networks"></a>Rutenetværk

Hvis du aktiverer de mere komplekse rutenetværk i produktionsstyringsparametrene, kan du definere ruter, der har flere startpunkter og operationer, der kan køres parallelt.  

[![Rutenetværk](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

> [!NOTE]
> - Hver operation kan kun have en efterfølgende operation, og hele ruten skal afsluttes med en fælles operation.
> - Dette er ingen sikkerhed for, at flere operationer, der har samme efterfølgende operation (f.eks. operationerne 30 og 40 i den foregående illustration), faktisk køres parallelt. Tilgængeligheden og kapaciteten af ressourcerne kan lægge begrænsninger på den måde, operationerne planlægges.
> - Du kan ikke bruge 0 (nul) som operationsnummeret. Dette nummer er reserveret og bruges til at angive, at den sidste operation i ruten ikke har nogen efterfølgende operation.

### <a name="parallel-operations"></a>Parallelle operationer

Nogle gange kræves en kombination af flere operationsressourcer, der har forskellige egenskaber, for at udføre en operation. For eksempel kan en samleoperation kræve en maskine, et værktøj og en arbejder for hver to maskiner til at overvåge driften. I dette eksempel kan dannes ved hjælp af parallelle operationer, hvor en operation er angivet som den primære operation, og de andre er sekundære.  

[![Rute, der har primære og sekundære operationer](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Den primære operation repræsenterer typisk flaskehalsressourcen og bestemmer operationstiden for de sekundære operationer. Men under planlægning, der involverer kapacitetsbegrænsning, skal de ressourcer, der er planlagt for både den primære operation og de sekundære operationer, være tilgængelige og have ledig kapacitet på samme tid.  

Både den primære operation og de sekundære operationer skal have samme operationsnummer (30 i den foregående illustration).  

I det foregående eksempel er ressourcekravet til den primære operation (30) maskinen, mens ressourcekravene for de sekundære operationer (30' og 30'') er værktøjet og arbejderen. En halvtreds procent belastning hjælper med til at sikre, at den planlagte arbejder kan overvåge to maskiner på samme tid.

### <a name="approval-of-routes"></a>Godkendelse af ruter

En rute skal være godkendt, før den kan bruges i planlægnings- eller fremstillingsprocessen. Godkendelse angiver, at rutedesignet er blevet fuldført. Det samme frigivne produkt eller den samme frigivne produktvariant kan have flere godkendte ruter. Godkendelse af en rute opstår typisk, når den første relevante ruteversion er godkendt. Men i nogle forretningsscenarier er godkendelse af ruten og ruteversionen separate aktiviteter, der kan omfatte forskellige procesejere.  

Hver rute kan være godkendt eller ikke-godkendt separat. Bemærk imidlertid, at hvis en rute ikke er godkendt, er alle relaterede ruteversioner heller ikke godkendt. I produktionsstyringsparametrene kan du angive, om ruter kan være ikke-godkendt, og om godkendte ruter kan ændres.  

Hvis du skal holde en log, der registrerer, hvem der godkender hver rute, kan du kræve elektroniske signaturer til rutegodkendelsen. Brugerne er så nødt til at bekræfte deres identitet ved hjælp af en [elektronisk signatur](../../fin-and-ops/organization-administration/electronic-signature-overview.md).

## <a name="operations"></a>Operations
En operation er trin i produktionsprocessen. Hver operation har et id og en kort beskrivelse. Følgende tabeller viser typiske eksempler på operationer fra en maskinfabrik.

| Handling  | Beskrivelse        |
|------------|--------------------|
| PipeCut    | Rørskæring       |
| TIGweld    | TIG-svejsning        |
| JigAssy    | Samling med værktøj       |
| Inspektion | Kvalitetsinspektion |

Operationsegenskaberne for operationen, f.eks. opstillingstid og procestid, ressourcekrav, efterkalkulationsoplysninger og forbrugsberegning er angivet på operationsrelationen. (Du kan finde flere oplysninger om operationsrelationer i næste afsnit).

## <a name="operation-relations"></a>Operationsrelationer
Følgende operationelle egenskaber for en operation vedligeholdes på operationsrelationen:

- Omkostningskategorier
- Forbrugsparametre
- Behandlingstider
- Behandlingsmængder
- Ressourcebehov
- Noter og instruktioner

Du kan definere flere operationsrelationer for den samme operation. Hver operationsrelation gælder dog kun for én operation og indeholder egenskaber, der er specifikke for en rute, en frigivet produkt eller et sæt frigivne produkter, der er knyttet til en varegruppe. Derfor kan den samme operation bruges i flere ruter, der har forskellige operationelle egenskaber. Desuden kan du lettere vedligeholde dine stamdata, hvis du bruger standardoperationer, der har samme operationelle egenskaber, uanset den rute, der bruges, og det produkt, der fremstilles. Anvendelsesområdet for operationsrelationen er defineret via egenskaberne **Varekode**, **Varerelation**, **Rutekode** og **Ruterelation**, som vist i følgende tabel.

| Varekode | Varerelation         | Rutekode | Ruterelation   | Anvendelsesområdet for operationsrelationen                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabellen     | &lt;Vare-id&gt;       | Rute      | &lt;Rute-id&gt; | De operationelle egenskaber for en operation, når den bruges i ruten hvor **rutenummer**=&lt;rute-id&gt; til at producere det frigivne produkt hvor **varenummer,**=&lt;vare-id&gt;.                                                                                                                        |
| Tabellen     | &lt;Vare-id&gt;       | Alt        |                  | De operationelle standardegenskaber for en operation, når den bruges til at producere det frigivne produkt, hvor **varenummer**=&lt;vare-id&gt;. Med andre ord gælder disse operationelle egenskaber, når der ikke er nogen rutespecifik operationsrelation for det frigivne produkt.                                     |
| Multi     | &lt;Varegruppe-id&gt; | Rute      | &lt;Rute-id&gt; | De operationelle egenskaber for en operation, når den bruges i ruten, hvor **rutenummer**=&lt;rute-id&gt; til at producere frigivne produkter, der er tilknyttet varegruppe &lt;varegruppe-id&gt;, medmindre der er en rutespecifik operationsrelation til det frigivne produkt.                         |
| Multi     | &lt;Varegruppe-id&gt; | Alt        |                  | De operationelle standardegenskaberne for en operation, når den bruges til at producere frigivne produkter, der er tilknyttet varegruppe &lt;varegruppe-id&gt;, medmindre der findes en mere specifik operationsrelation.                                                                                                  |
| Alt       |                       | Rute      | &lt;Rute-id&gt; | De operationelle standardegenskaber for operationen, når den bruges i ruten hvor **rutenummer**=&lt;rute-id&gt;. Med andre ord gælder disse operationelle egenskaber, når der ikke er nogen operationsrelation for denne rute, der er specifik for det frigivne produkt eller dets tilknyttede varegruppe. |
| Alt       |                       | Alt        |                  | De operationelle standardegenskaber for en operation. Disse operationelle egenskaber gælder, når der ikke findes en mere specifik operationsrelation.                                                                                                                                                                |

Du kan også angive, at en operationsrelation er specifik for et sted. På denne måde kan operationelle egenskaber for en operation variere afhængigt af lokaliteten (dvs. stedet), hvor operationen skal udføres. For konfigurerede produkter kan du også angive forskellige operationelle egenskaber for hver produktkonfiguration.  

Operationsrelationer giver dig masser af fleksibilitet, når du definerer dine ruter. Desuden hjælper muligheden for at definere standardegenskaber med til at reducere mængden af stamdata, som du skal vedligeholde. Men denne fleksibilitet betyder også, at du skal være opmærksom på den kontekst, du ændrer en operationsrelation i.  

> [!NOTE]
> Da de operationelle egenskaber gemmes i operationsrelationer pr. operation for den enkelte rute, har alle forekomster af den samme operation (f.eks. samling) samme opstillingstid, operationstid og ressourcekrav. Hvis to forekomster af en operation derfor skal udføres i den samme rute, men har forskellige operationstider, skal du oprette to separate operationer, f.eks. Samling1 og Samling2.

### <a name="modifying-product-specific-routes"></a>Ændring af produktspecifikke ruter

Når du åbner siden **Rute** fra siden **Oplysninger om frigivne produkter**, vises de ruteversioner, der er knyttet til det valgte frigivne produkt. I denne sammenhæng viser Supply Chain Management for hver operation operationsegenskaberne fra den operationsrelation, der passer bedst til ruteversionen. Bemærk, at listen over operationer omfatter egenskaberne **Varekode** og **Rutekode** fra operationsrelationen. Derfor kan du bestemme, hvilken operationsrelationen der vises.  

På siden **Rute** side, kan du kan ændre operationsegenskaberne for operationen, f.eks. operationstiden eller omkostningskategorierne. Dine ændringer gemmes på den operationsrelation, der er specifik for ruten og det frigivne produkt, der refereres til i den aktuelle ruteversion. Hvis den operationsrelation, der er vist, ikke er specifik for ruten og det frigivne produkt, før dine ændringer er gemt, opretter systemet en kopi af operationsrelationen. Denne kopi *er* specifik for ruten og det frigivne produkt. Derfor påvirker dine ændringer ikke andre ruter eller frigivne produkter. For at kontrollere hvilken operationsrelation, der ændres på siden **Rute**, skal du se på felterne **Varekode** og **Rutekode**.  

Du kan også manuelt oprette en operation, der er specifik for en rute og et frigivet produkt ved hjælp af funktionen **Kopiér og rediger relation**.  

> [!NOTE]
> Hvis du tilføjer en ny operation til en rute på siden **Rute**, oprettes der kun en operationsrelation for det aktuelt frigivne produkt. Hvis ruten derfor også bruges til at fremstille andre frigivne produkter, findes der ingen gældende operationsrelationen for disse frigivne produkter, og ruten kan ikke længere bruges til disse frigivne produkter.

### <a name="maintaining-operation-relations-per-route"></a>Vedligehold operationsrelationer pr. rute

Når du åbner siden **Rutedetaljer** siden fra listesiden **Ruter**, vises der en liste over de operationsrelationer, der gælder for den valgte rute. Du kan derfor let kontrollere, hvilke operationelle egenskaber, der bruges til hvilke produkter. Du kan ændre både standardegenskabsværdierne og produktspecifikke egenskabsværdier.  

Hvis du tilføjer en ny operationsrelation på siden **Rutedetaljer**, angives feltet **Rutekode** automatisk til **Rute**, og feltet **Ruterelation** angives til rutenummeret for den aktuelle rute.

### <a name="maintaining-operation-relations-per-operation"></a>Vedligehold operationsrelationer pr. operation

Fra siden **Operationer** kan du åbne siden **Operationsrelationer**. På denne side kan du ændre alle operationsrelationer for en specifik operation. Du kan endda redigere operationsrelationer, der indeholder standardværdier.  

Hvis din virksomhed bruger standardoperationer, og de operationelle parametre er de samme på tværs af alle produkter og processer, er siden **Operationsrelationer** side en praktisk måde til at opretholde de operationelle standardegenskaber for disse operationer.

### <a name="applying-operation-relations"></a>Anvendelse af operationsrelationer

I nogle tilfælde skal Supply Chain Management finde operationelle egenskaber for en operation. Når der f.eks. oprettes en indkøbsordre, skal de operationelle egenskaber for hver operation kopieres fra operationsrelationerne til produktionsruten. I sådanne situationer søger Supply Chain Management efter de relevante operationsrelationer fra den mest specifikke kombination til den mindst specifikke kombination.  

Når Supply Chain Management søger efter den mest relevante operationsrelation for et frigivet produkt, foretrækkes en operationsrelation, der svarer til vare-id'et for det frigivne produkt, i forhold til en operationsrelation, der svarer til varegruppe-id'et. Til gengæld foretrækkes en operationsrelation, der svarer til varegruppe-id'et, i forhold til standardoperationsrelationen. Søgningen sker i følgende rækkefølge:

1.  **Varekode**=**tabel** og **varerelation**=&lt;vare-id&gt;
2.  **Varekode**=**gruppe** og **varerelation**=&lt;varegruppe-id&gt;
3.  **Varekode**=**alle**
4.  **Rutekode**=**rute** og **ruterelation**=&lt;rute-id&gt;
5.  **Rutekode**=**alle**
6.  **Konfiguration**=&lt;konfigurations-id&gt;
7.  **Konfiguration**=
8.  **Sted**=&lt;sted-id&gt;
9.  **Sted**=

En operation bør derfor kun anvendes én gang for hver rute. Hvis operationen forekommer flere gange på den samme rute, har alle forekomster af denne operation samme operationsrelationen, og du kan ikke have andre egenskaber (for eksempel procestider) for hver forekomst.

## <a name="route-versions"></a>Ruteversioner

Ruteversioner bruges til at tage hensyn til afvigelser i produktionen af produkter eller til at give dig større kontrol over produktionsprocessen. De definerer, hvilken rute der skal bruges, når et bestemt frigivet produkt eller en bestemt frigiven produktvariant produceres. Du kan bruge følgende begrænsninger til at definere, hvilken rute der bruges til et frigivet produkt, :

- Produktdimensioner (størrelse, farve, type eller konfiguration)
- Produktionsmængde
- Produktionssted
- Produktionsdato

Når du producerer produktet på et bestemt sted, i en bestemt mængde eller i en bestemt periode, kan du angive en bestemt ruteversion som standardruteversionen. Bemærk dog, at kun én aktiv rute er tilladt for et bestemt frigivet produkt og et bestemt sæt begrænsninger.  

I produktionsstyringsparametrene kan du kræve, at gyldighedsperioden for en ruteversion altid skal angives.

### <a name="approval-of-route-versions"></a>Godkendelse af ruteversioner

Før en ruteversion kan bruges i planlægnings- eller fremstillingsprocessen, skal den godkendes. Når du godkender en ruteversion, kan du også godkende den tilhørende rute. Bemærk dog, at en ruteversion kun kan godkendes, hvis den relaterede rute også er godkendt.

### <a name="activating-the-default-route-version"></a>Aktivering af standardruteversionen

Når du aktiverer en ruteversion, angiver du den som den standardruteversion, varedisponeringen skal bruge, eller der skal bruges til at oprette produktionsordrer. Du kan kun have én aktiv ruteversion for et bestemt sæt begrænsninger (f.eks. periode, sted eller antal). Du modtager en fejlmeddelelse, hvis den version, du forsøger at aktivere, er i konflikt med en version, der allerede er aktiv. For at forhindre en tvetydig aktivering skal du derefter enten deaktivere versionen, der er i konflikt, eller redigere ruteversionens begrænsninger (som regel perioden).

### <a name="electronic-signatures"></a>Elektroniske signaturer

Hvis du skal holde en log, der registrerer, hvem der godkender og aktiverer hver ruteversion, kan du kræve elektroniske signaturer til disse opgaver. Brugere, der kan godkende og aktivere ruteversioner, skal bekræfte deres identitet ved hjælp af en [elektronisk signatur](../../fin-and-ops/organization-administration/electronic-signature-overview.md).

### <a name="product-change-that-uses-case-management"></a>Produktændring, der bruger sagsstyring

Produktændringssagen til godkendelse og aktivering af nye eller ændrede ruter og ruteversioner giver dig på en nem måde en oversigt over ruteversionens begrænsninger. Du kan også godkende og aktivere alle ruter, der er relateret til en bestemt ændring i én operation og dokumentere resultaterne i produktændringssagen.

## <a name="maintaining-routes"></a>Vedligeholdelse af ruter

Afhængigt af virksomhedens behov, kan du muligvis reducere det arbejde, der kræves for at bevare dine procesdefinitioner.

### <a name="making-routes-independent-of-resources"></a>Gør ruter uafhængige af ressourcer

I mange systemer skal operationsressourcen eller den ressourcegruppe, som skal udføre en operation, angives i ruten. I Supply Chain Management kan du definere en række krav, som en operationsressource skal opfylde for at være gældende for operationen. Derfor behøver den specifikke operationsressource eller ressourcegruppe, der skal bruges, ikke at blive fastlagt, før operationen faktisk er planlagt. Denne funktion er især nyttig, når du har mange arbejdere eller maskiner, der kan udføre den samme operation.  

Du angiver f.eks., at en operation kræver en operationsressource af typen **Maskine**, der har en **Udstansningskapacitet** på 20 tons. Planlægningsprogrammet vil derefter løse disse krav til en bestemt operationsressource eller ressourcegruppe, når operationen er planlagt. Fordi du blot kan angive disse krav i stedet for at binde operationen til en bestemt maskine, har du meget mere fleksibilitet. Desuden er vedligeholdelse lettere, når ressourcer flyttes, eller der tilføjes nye ressourcer.  

Du kan finde yderligere oplysninger om de forskellige typer ressourcebehov, og hvordan du bruger dem, i Ressourcekrav for operationer og [Ressourceegenskaber](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Deling af ruter på tværs af steder

Hvis du producerer det samme produkt på mere end ét produktionssted, og fremgangsmåden til fremstilling af produktet er den samme på alle steder, kan du ofte designe en delt rute, der bruges på tværs af alle produktionssteder. Hvis du vil oprette en delt rute, skal du ikke angive et sted på selve ruten. Du skal dog stadig oprette en ruteversion, der knytter den delte rute til produktet på hvert sted.  

Du skal også sikre dig, at ressourcekravene for hver operation i ruten ikke kræver bestemte operationsressourcer eller ressourcegrupper, men at de i stedet er udtrykt i form af karakteristika for de påkrævede ressourcer. Planlægningsprogrammet vil derefter kunne tildele de relevante operationsressourcer fra det sted, hvor produktionen er planlagt til. Hvis der f.eks er små forskelle i procestiden, eller hvis opstillingstiden for en bestemt operation er stedspecifik, kan du angive disse oplysninger ved at tilføje en ekstra operationsrelation for det pågældende sted.  

For at få fuldt udbytte af fordelene ved delte ruter skal du også bruge ressourceforbrug på den tilknyttede stykliste. Når du angiver flaget for ressourceforbrug på styklistelinjen, skal lagerstedet og lokaliteten, hvor råmaterialer skal forbruges fra, udledes fra den operationsressource, som operationen er planlagt på. Derfor behøver lagerstedet og lokaliteten ikke at blive fastlagt, før produktionen faktisk planlægges. På denne måde kan du både gøre styklisten og ruten uafhængig af den fysiske lokalitet, hvor produktet fremstilles.

### <a name="standard-operation-relations"></a>Standardoperationsrelationer

Hvis din virksomhed bruger standardiserede operationer i produktionen, og der er meget lidt eller ingen variation i opstillingstid, operationstid, forbrugsberegning, omkostningsberegning osv., kan du med fordel oprette standardoperationsrelationer for alle operationer. I dette tilfælde skal du undgå at oprette operationsrelationer, der er specifikke for en rute eller et frigivet produkt.  

Hvis du også udtrykker ressourcekrav med hensyn til færdigheder og funktioner og gør dine ruter uafhængige af stedet, kan du hjælpe med til at holde den løbende vedligeholdelse af dine forretningsprocesser på et minimum.  

Når du bruger denne metode, bliver siden **Operationsrelationer** din primære destination for opretholdelse af procestider og andre egenskaber.

### <a name="resource-specific-process-times"></a>Ressourcespecifikke procestider

Hvis du ikke angiver en operationsressource eller ressourcegruppe som en del af ressourcekravene for en operation, kan de relevante ressourcer fungere ved forskellige hastigheder. Den tid, der kræves for at behandle en operation, kan derfor variere. Du kan løse dette problem ved at bruge feltet **Formel** på operationsrelationen til at angive, hvordan procestiden beregnes. Følgende valgmuligheder er tilgængelige:

- **Standard** – (standardindstilling) Beregningen bruger kun felterne fra operationsrelationen og ganger den angivne procestid med ordreantallet.
- **Kapacitet** – Beregningen omfatter feltet **Kapacitet** fra operationsressourcen. Tiden er derfor ressourceafhængig. Den værdi, der er angivet på operationsressourcen, er kapacitet pr. time. **Procestid** beregnes som **Ordreantal** divideret med **Kapacitet**.
- **Batch** – En batchkapacitet beregnes ved hjælp af oplysninger fra operationsrelationen. Antallet af batches, og derfor procestiden, kan beregnes baseret på ordreantallet.
- **Ressourcebatch** – Denne indstilling er grundlæggende den samme som indstillingen **Batch**. Men beregningen omfatter feltet **Batchkapacitet** fra operationsressourcen. Tiden er derfor ressourceafhængig.

### <a name="set-up-route-groups"></a>Konfigurer rutegrupper

Du kan definere rutegrupper og opsætningen for den hertil hørende rute eller jobtyperne under **Produktionskontrol > Opsætning > Ruter > Rutegrupper**. For hver rute/jobtype i rutegruppen kan du vælge eller nulstille følgende indstillinger:

- **Aktivering** - Vælg denne indstilling for at aktivere beregninger for og planlægning af den valgte jobtype og for at modtage jobtilbagemelding, når du kører finplanlægning. Du er nødt til at vælge denne indstilling for at aktivere jobtypen og dernæst vælge resten af indstillingerne for den pågældende jobtype. Hvis du ikke vælger at aktivere, vil den pågældende jobtype ikke blive slået til, uanset om du vælger de øvrige indstillinger. 
- **Jobstyring** - Vælg denne indstilling for at medtage jobtypen i jobstyring, når du kører finplanlægning. 
- **Arbejdstid** - Vælg denne indstilling for at planlægge jobtypen i henhold til arbejdstidskalenderen, der er defineret for operationsressourcen, ellers anvendes den gregorianske kalender. Arbejdstiden kan enten planlægges i henhold til den gregorianske kalender eller den angivne arbejdskalender. Hvis du markerer denne indstilling, bliver planlægningen baseret den angivne arbejdstidskalender. Derudover planlægges job af jobtypen fra midnat på den dato, der er angivet som jobbets startdato.
- **Kapacitet** - Vælg denne indstilling for at reservere kapacitet til jobtypen, når du kører finplanlægning. Hvis du vælger denne indstilling, reserveres der kapacitet, når der køres finplanlægning for den valgte jobtype. Det giver dig en oversigt over, hvilke jobtyper i hver rutegruppe der bruger operationsressourcer. Disse ressourcer skal eksempelvis være angivet som flaskehalse, såfremt der er tale om en situation, hvor tørreressourcer er flaskehalsressourcer. Tørreoperationer, der er tilknyttet jobtyper i køtid, vil reservere tørreressourcer. 

Du skal aktivere eller deaktivere det for hver jobtype. Når du deaktivere det, vil ingen andre elementer i opsætningen (jobstyring, arbejdstid og kapacitet) blive taget i betragtning, da jobtypen ikke er aktiv. 

Blandt jobtyperne finder du "Overlap". Overlap gør det muligt at udføre forskellige jobs på samme tid. Når jobs overlapper, kan ressourcerne anvendes, men de kan ikke reserveres til det pågældende job.
Derfor påvirker de øvrige indstillinger (jobstyring, arbejdstid og kapacitet) ikke rutegruppen, når der vælges "Aktivering" for "Overlap. 

> [!NOTE]
> I forbindelse med opgraderingen af versioner støder du muligvis på følgende fejl **Der opstod en CLR-fejl ved start af planlægningsprogrammet**. Hvis du får denne fejl, skal du gå til siden **Rutegrupper** og nulstille indstillingerne **Jobstyring**, **Arbejdstid** og **Kapacitet** for alle de ruter, hvor du har aktiveret **Overlap**. 

## <a name="additional-resources"></a>Yderligere ressourcer

- [Styklister og formler](bill-of-material-bom.md)

- [Omkostningsarter, der bruges i produktionsrute](../cost-management/cost-categories-used-production-routings.md)

- [Ressourceegenskaber](resource-capabilities.md)

- [Oversigt over elektroniske signaturer](../../fin-and-ops/organization-administration/electronic-signature-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]