---
title: Ruter og operationer
description: "Dette emne indeholder oplysninger om ruter og operationer. En rute definerer processen til fremstilling af et produkt eller en produktvariant. Det beskriver hvert trin (operation) i produktionsprocessen, og den rækkefølge, som disse trin skal udføres i. For hvert trin definerer ruten også kræves operationsressourcer, kræves opstillingstid og operationstid, og hvordan omkostningerne skal beregnes."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 556b9859d0b162b11f0bcbfc6552f6fd9a900596
ms.lasthandoff: 03/31/2017


---

# <a name="routes-and-operations"></a>Ruter og operationer

Dette emne indeholder oplysninger om ruter og operationer. En rute definerer processen til fremstilling af et produkt eller en produktvariant. Det beskriver hvert trin (operation) i produktionsprocessen, og den rækkefølge, som disse trin skal udføres i. For hvert trin definerer ruten også kræves operationsressourcer, kræves opstillingstid og operationstid, og hvordan omkostningerne skal beregnes.

<a name="overview"></a>Overblik
--------

En rute beskriver rækkefølgen af operationer, der kræves for at producere et produkt eller en produktvariant. Ruten definerer også de operationsressourcer, der skal bruges, den tid, der kræves for at oprette og udføre operationen, og hvordan omkostningerne skal beregnes for hver operation. Du kan bruge den samme rute til at producere flere produkter, eller du kan definere en entydig rute for hver vare eller produktvariant. Du kan også have flere ruter til samme produkt. I dette tilfælde den rute, der bruges, varierer afhængigt af faktorer som det antal, der skal produceres. Definitionen af en rute i Microsoft Dynamics 365 for operationer består af fire separate elementer, der tilsammen beskriver produktionsprocessen:

-   **Rute** – en rute, der definerer strukturen i produktionsprocessen. Med andre ord, definerer den rækkefølgen af operationer.
-   **Handling** – en handling identificerer et navngivet trin i en rute, som **montage**. Den samme operation kan forekomme i flere ruter og kan have forskellige operationsnumre.
-   **Operationsrelation** – en Operationsrelation definerer operationelle egenskaber for en operation, som opstillingstid og procestid, omkostningsarter, parametrene og ressourcekrav. Operationsrelationen kan operationelle egenskaber af en operation til varierer, afhængigt af den rute, der skal bruges i handlingen eller de produkter, der produceres.
-   **Ruteversion** – en ruteversion, der definerer den rute, der bruges til at producere et produkt eller en produktvariant. Ruteversioner kan ruter skal genbruges på tværs af produkter eller ændret sig med tiden. De kan også aktivere forskellige ruter skal bruges til at fremstille det samme produkt. I dette tilfælde den rute, der bruges, afhænger af faktorer som placeringen eller det antal, der skal produceres.

## <a name="routes"></a>Ruter
En rute beskriver rækkefølgen af operationer, der bruges til at producere et produkt eller en produktvariant. Hver operation er tildelt et operationsnummer og en efterfølgende operation. Rækkefølgen af operationer udgør et rute-netværk, der kan repræsenteres af et styret diagram, der har en eller flere startpunkter og et enkelt slutpunkt. I Dynamics 365 for operationer, ruter adskiller sig på grundlag af typen struktur. De to typer ruter er simple ruter og ruteversioner netværk. I produktionsparametre, kan du angive, om kun simple ruter kan bruges, eller om der kan bruges mere komplekse rutenetværk.

### <a name="simple-routes"></a>Simple ruter

En simpel rute er sekventiel, og der er kun et udgangspunkt for ruten.  

[![Simpel rute](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Hvis du aktiverer kun simple ruter i produktionsparametrene, operationsnumrene genererer automatisk Dynamics 365 for operationer (10, 20, 30 og så videre) når du definerer ruten.

### <a name="route-networks"></a>Rutenetværk

Hvis du aktiverer mere komplekse rutenetværk i produktionsparametrene kontrolelement, kan du definere ruter, der har flere Start point og operationer, der kan køres parallelt.  

[![Route network](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Bemærkninger:**

-   Hver operation kan have en efterfølgende operation, og hele ruten skal afsluttes med en enkelt handling.
-   Der er ingen garanti for, at flere operationer, der har samme efterfølgende handling (eksempelvis handlinger 30 og 40 i den foregående illustration) faktisk køres parallelt. Disponeringen og kapaciteten for ressourcerne kan lægge begrænsninger på den måde, operationerne planlægges.
-   Du kan ikke bruge 0 (nul) som operationsnummeret. Dette nummer er reserveret og bruges til at angive, at den sidste operation i ruten har ingen efterfølgende operation.

### <a name="parallel-operations"></a>Parallelle operationer

Nogle gange en kombination af flere operationsressourcer, der har forskellige egenskaber, der kræves for at udføre en handling. For eksempel kan en samleproces kræve en maskine, et værktøj og en arbejder for hver to maskiner til at overvåge driften. I dette eksempel kan dannes ved hjælp af parallelle operationer, hvor en operation er angivet som den primære operation, og de andre er sekundære.  

[![Rute, der er primære og sekundære operationer](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Normalt er den primære operation repræsenterer flaskehalsressource, og bestemmer operationstiden for de sekundære operationer. Men under planlægning, der involverer kapacitetsbegrænsning, de ressourcer, der er planlagt for både den primære operation og de sekundære operationer skal være tilgængelige og har ledig kapacitet på samme tid.  

Både den primære operation og de sekundære operationer, skal have samme operationsnummer (30 i den foregående illustration).  

I det foregående eksempel er ressourcekrav til den primære operation (30) maskinen, ressourcekravene for de sekundære operationer (30' og 30'') er værktøjet og arbejderen. En Femti procent belastning hjælper med at sikre, at den planlagte arbejder kan overvåge to maskiner på samme tid.

### <a name="approval-of-routes"></a>Godkendelse af ruter

En rute skal godkendes, før den kan bruges i processen planlægning eller produktion. Godkendelsen angiver, at ruten design er fuldført. Den samme frigivet produkt eller frigivet produktvariant kan have flere godkendte ruter. Godkendelse af en rute opstår typisk, når den første relevante ruteversion er godkendt. Men i nogle business scenarier, godkendelse af ruten og ruteversionen er separate aktiviteter, der kan omfatte forskellige procesejere.  

Hver rute kan være godkendte eller ikke-godkendt separat. Bemærk dog, at når en rute er ikke-godkendte, alle relaterede ruteversioner er også ikke-godkendte. Produktionsparametre, kan du angive om ruter kan være ikke-godkendt, og om godkendte ruter kan ændres.  

Hvis du skal holde en log, som poster, som godkender hver rute, kan du kræve elektroniske signaturer til godkendelse. Brugere vil være at bekræfte deres identitet ved hjælp af en [elektronisk signatur](/dynamics365/operations/organization-administration/electronic-signature-overview).

## <a name="operations"></a>Drift
En handling er et trin i produktionsprocessen. I Dynamics 365 for operationer har hver handling et ID og en enkel beskrivelse. Følgende tabeller viser typiske eksempler på operationer fra en computer shop.

| Handling  | Betegnelse        |
|------------|--------------------|
| PipeCut    | Pipe opskæring       |
| TIGweld    | TIG svejsning        |
| JigAssy    | Ophængnings assembly       |
| Inspektion | Kvalitetskontrol |

Operationens opstillingstid og procestid og ressourcekrav, oplysninger om omkostningsberegning og forbrugsberegning, operationelle egenskaber er angivet på operationsrelationen. (Yderligere oplysninger om operationsrelationer, se næste afsnit).

## <a name="operation-relations"></a>Operationsrelationer
Følgende operationelle egenskaber for en operation, der vedligeholdes på operationsrelationen:

-   Omkostningskategorier
-   Forbrug-parametre
-   Afviklingstider
-   Behandling af mængder
-   Ressourcebehov
-   Noter og instruktioner

Du kan definere flere operationsrelationer for den samme handling. Dog hver operationsrelationen gælder kun for én operation og indeholder egenskaber, der er specifikke for en rute, en frigivet produkt eller et sæt frigivne produkter, der er knyttet til en varegruppe. Derfor kan den samme handling bruges i flere ruter, der har forskellige operationelle egenskaber. Desuden kan du nemt vedligeholde stamdata, hvis du bruger standard operationer, der har samme operationelle egenskaber, uanset den rute, der bruges og produkt, der fremstilles. Anvendelsesområdet for operationsrelationen er defineret via den **vare kode**, **vare relation**, **Route kode** og **Route relation** egenskaber, som vist i følgende tabel.

| Varekode | Varerelation         | Rutekode | Ruterelation   | Anvendelsesområdet for operationsrelationen                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabellen     | &lt;Vare-id&gt;       | Rute      | &lt;Rute-id&gt; | Operationelle egenskaber for en handling, når det bruges i ruten hvor **rutenummer**=&lt;rute-ID&gt; til at producere det endelige produkt hvor **det varenummer,**=&lt;vare ID&gt;.                                                                                                                        |
| Tabellen     | &lt;Vare-id&gt;       | Alt        |                  | Operationelle standardegenskaberne for en handling, når det bruges til at producere det endelige produkt hvor **det varenummer,**=&lt;vare ID&gt;. Med andre ord, gælder disse operationelle egenskaber, når der er ingen specifikke rute operationsrelationen for frigivet produkt.                                     |
| Multi     | &lt;Gruppe-ID for varen&gt; | Rute      | &lt;Rute-id&gt; | Operationelle egenskaber for en handling, når det bruges i ruten hvor **rutenummer**=&lt;rute-ID&gt; til at oprette frigivne produkter, der er tilknyttet varegruppe &lt;vare-ID'ET&gt;, medmindre der er en rute-specifikke operationsrelationen for frigivet produkt.                         |
| Multi     | &lt;Gruppe-ID for varen&gt; | Alt        |                  | Operationelle standardegenskaberne for en handling, når det bruges til at oprette frigivne produkter, der er tilknyttet varegruppe &lt;vare-ID'ET&gt;, medmindre der findes en mere specifik Operationsrelation.                                                                                                  |
| Alt       |                       | Rute      | &lt;Rute-id&gt; | De operationelle standardegenskaber for handlingen, når det bruges i ruten hvor **rutenummer**=&lt;rute-ID&gt;. Med andre ord, gælder disse operationelle egenskaber, når der er ingen Operationsrelation for denne rute, der er specifikke for en frigivet produkt eller den tilknyttede varegruppe. |
| Alt       |                       | Alt        |                  | Operationelle standardegenskaberne for en operation. Disse operationelle egenskaber gælder, når der ikke findes en mere specifik Operationsrelation.                                                                                                                                                                |

Du kan også angive, at en Operationsrelation er specifikke for et websted. På denne måde kan operationelle egenskaber for en operation variere afhængigt af placering (sted), hvor handlingen skal udføres. Du kan også angive forskellige operationelle egenskaber for produktkonfiguration af hvert for konfigurerede varer.  

Operationsrelationer giver dig masser af fleksibilitet, når du definerer dine ruter. Mulighed for at definere standardegenskaber hjælper desuden med at reducere mængden af stamdata, som du skal vedligeholde. Men denne fleksibilitet betyder også, at du skal være opmærksom på, som du kan ændre en Operationsrelation i konteksten.  

**Bemærk:** da operationelle egenskaber gemmes i operationsrelationer pr. operation pr. rute, alle forekomster af den samme operation (for eksempel Assembly) har samme opstillingstid, Operationstid, ressourcekrav osv. Hvis to forekomster af en handling skal udføres i den samme rute, men forskellige operationstider, skal du derfor oprette to forskellige operationer, såsom Assembly1 og Assembly2.

### <a name="modifying-product-specific-routes"></a>Ændring af produktspecifikke ruter

Når du åbner den **rute** siden fra den **udgivet produktdetaljer** side, vises de ruteversioner, der er knyttet til det valgte produkt. I denne sammenhæng, for hver operation viser Dynamics 365 for operationer fra operationsrelationen operationelle egenskaber, passer bedst til ruteversionen. Bemærk, at listen over handlinger omfatter den **vare kode** og **Route kode** egenskaber fra operationsrelationen. Derfor kan du bestemme, hvilke operationsrelationen vises.  

På den **rute** side, du kan ændre operationen, som operationstiden eller omkostningsarterne operationelle egenskaber. Dine ændringer gemmes på operationsrelationen, der er specifikke for ruten og frigivet produkt, der refereres til i den aktuelle ruteversion. Hvis operationsrelationen, der er vist ikke er specifikke for ruten og det endelige produkt, før ændringerne er gemt, opretter systemet en kopi af operationsrelationen. Denne kopi *er* bestemt til rute- og frigivet produkt. Derfor er ændringerne påvirker ikke andre ruter, eller frigivne produkter. At kontrollere, hvilke operationsrelationen ændres på den **rute** side, skal du se den **vare kode** og **Route kode** felter.  

Du kan også manuelt oprette en handling, der er specifikke for en rute og frigivet produkt ved hjælp af den **kopier og rediger relation** funktion.  

**Bemærk:** Hvis du tilføjer en ny operation til en rute i den **rute** side, en Operationsrelation oprettes kun for det aktuelle produkt. Derfor, hvis ruten bruges også til at fremstille andre produkter, der er frigivet, der findes ingen gældende operationsrelationen for de frigivne produkter, og ruten kan ikke længere bruges til de frigivne produkter.

### <a name="maintaining-operation-relations-per-route"></a>Vedligeholdelse af operationsrelationer pr. rute

Når du åbner den **distribuere oplysninger** siden fra den **ruter** listeside, der vises en liste over de operationsrelationer, der gælder for den valgte rute. Du kan derfor let kontrollere, hvilke operationelle egenskaber, der bruges til hvilke produkter. Du kan ændre både standardegenskabsværdierne og produktspecifikke egenskabsværdier.  

Hvis du tilføjer en ny operationsrelationen på den **distribuere oplysninger** side, den **Route kode** er automatisk indstillet til **rute**, og **Route relation** er angivet til rutenummeret for den aktuelle rute.

### <a name="maintaining-operation-relations-per-operation"></a>Vedligeholdelse af operationsrelationer pr. operation

Fra den **Operations** side, kan du åbne den **operationsrelationer** side. På denne side kan du ændre alle operationsrelationer for en specifik operation. Du kan endda redigere operationsrelationer, der indeholder standardværdier.  

Hvis din virksomhed bruger standard operationer, og de operationelle parametre er de samme på tværs af alle produkter og processer, de **operationsrelationer** side er en praktisk metode til at opretholde de operationelle standardegenskaber for disse operationer.

### <a name="applying-operation-relations"></a>Anvendelse af operationsrelationer

I nogle tilfælde skal Dynamics 365 for operationer finde operationelle egenskaber for en operation. For eksempel når der oprettes en indkøbsordre, skal operationelle egenskaber for hver operation kopieres fra operationsrelationer til produktionsruten. I sådanne situationer søger Dynamics 365 for operationer de relevante operationsrelationer fra den mest specifikke kombination til den mindst specifikke kombination.  

Når Dynamics 365 for operationer søger efter de mest relevante Operationsrelation for et frigivet produkt, en Operationsrelation, der svarer til vare-ID'ET for det udgivne produkt foretrækkes over en Operationsrelation, svarer til varegruppen-id. Til gengæld er en Operationsrelation, der svarer til element-ID den foretrukne over operationsrelationen standard. Søgningen foretages i følgende rækkefølge:

1.  **Punkt kode**=**tabel** og **vare relation**=&lt;vare ID&gt;
2.  **Punkt kode**=**gruppe** og **vare relation**=&lt;vare gruppe-ID&gt;
3.  **Punkt kode**=**alle**
4.  **Distribuere kode**=**rute** og **Route relation**=&lt;rute-ID&gt;
5.  **Distribuere kode**=**alle**
6.  **Konfiguration af**=&lt;variant-ID&gt;
7.  **Configuration**=
8.  **Webstedet**=&lt;ID på webstedet&gt;
9.  **Site**=

En operation bør derfor anvendes kun én gang for hver rute. Hvis handlingen forekommer flere gange i den samme rute, alle forekomster af denne handling har samme operationsrelationen, og du kan ikke have andre egenskaber (for eksempel køre gange) for hver forekomst.

## <a name="route-versions"></a>Ruteversioner
Ruteversioner bruges til at imødekomme variationer i produktionen af produkter eller giver større kontrol over produktionsprocessen. De definerer, hvilken rute, der skal bruges, når en bestemt frigivet produkt eller variant frigivet produkt er fremstillet. Til at definere, hvilken rute, der bruges til et frigivet produkt, kan du bruge følgende begrænsninger:

-   Produktdimensioner (størrelse, farve, typografi eller konfiguration)
-   Produktionsantal
-   Produktionsstedet
-   Dato for produktion

Når du arbejder med produkt på et bestemt sted i en bestemt mængde eller i en bestemt periode, kan du angive en bestemt ruteversion som standard ruteversionen. Bemærk dog, at kun én aktiv rute er tilladt for et givet produkt og et bestemt sæt begrænsninger.  

I produktionsparametre, kan du kræve, at gyldighedsperioden for en ruteversion altid være angivet.

### <a name="approval-of-route-versions"></a>Godkendelse af ruteversioner

Før en ruteversion, der kan bruges i planlægnings- eller fremstillingsproces, skal den godkendes. Når du godkender en ruteversion, kan du også godkende den relaterede rute. Bemærk dog, at en ruteversion skal godkendes kun, hvis den relaterede rute er også godkendt.

### <a name="activating-the-default-route-version"></a>Aktivere ruteversionen standard

Når du aktiverer en ruteversion, angiver du det som standard ruteversionen, som planlægningen skal bruge, eller, der skal bruges til at oprette produktionsordrer. Du kan have én aktive ruteversion for et bestemt sæt betingelser (for eksempel periode, websted eller antal). Hvis den version, du forsøger at aktivere er i konflikt med en version, der allerede er aktiv, vises en fejlmeddelelse. For at forhindre en tvetydig aktivering, skal du derefter enten deaktivere versionen konflikt eller ændre begrænsninger (som regel perioden) i ruteversionen.

### <a name="electronic-signatures"></a>Elektroniske signaturer

Hvis du skal holde en log, som poster, der godkender og aktiverer hver ruteversion, kan du kræve elektroniske signaturer for disse opgaver. Brugere, der kan godkende og aktivere ruteversioner vil være at bekræfte deres identitet ved hjælp af en [elektronisk signatur](/dynamics365/operations/organization-administration/electronic-signature-overview).

### <a name="product-change-that-uses-case-management"></a>Produktændring af, der bruger sagsstyring

Produktet og små bogstaver for godkendelse og aktivering af nye eller ændrede ruter og ruteversioner giver dig en nem måde at se en oversigt over ruten version begrænsninger. Du kan også godkende og aktivere alle ruter, der er relateret til en bestemt ændring i én operation og dokumentere resultaterne i de store og små bogstaver produkt.

## <a name="maintaining-routes"></a>Vedligeholdelse af ruter
Afhængigt af virksomhedens behov, kan du muligvis reducere det arbejde, der kræves for at bevare din proces definitioner.

### <a name="making-routes-independent-of-resources"></a>Gør ruter, der er uafhængige af ressourcer

I mange systemer, skal operationsressourcen eller den ressourcegruppe, som skal udføre en handling angives i ruten. I Dynamics 365 for operationer, kan du definere en række krav, som en operationsressource skal opfylde for at være gældende for handlingen. Derfor behøver operationsressourcen eller ressourcegruppen, der skal bruges skal fastlægges, indtil handlingen er faktisk planlagt. Denne funktion er især nyttig, når du har mange arbejdere eller maskiner, der kan udføre den samme handling.  

For eksempel angive, at en handling kræver en operationsressource i den **maskine** type, der har en **Stamping** mulighed for 20 tons. Planlægningsprogrammet kan derefter løse disse krav til en bestemt operationsressource eller ressourcegruppe, når operationen er planlagt. Fordi du kan blot angive disse krav i stedet for bindende operationen til en bestemt maskine, er du meget mere fleksibel. Desuden er vedligeholdelse lettere, når ressourcer er flyttet, eller der tilføjes nye ressourcer.  

Yderligere oplysninger om de forskellige typer ressourcebehov og hvordan du bruger dem, se ressourcekravene for operationer og [ressourceegenskaber](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Deling af ruter på tværs af websteder

Hvis du giver det samme produkt på mere end én produktionslokation, og fremgangsmåde til fremstilling af produktet er det samme på alle steder, kan du ofte designe en delt rute, der bruges på tværs af alle produktionsanlæg. Hvis du vil oprette en delt rute, Angiv ikke et websted på selve ruten. Du skal dog stadig oprette en ruteversion, der knytter den delte rute til produktet på hver lokation.  

Du skal også sikre dig, at ressourcekravene for hver operation i ruten ikke ringe for bestemte operationsressourcer eller ressourcegrupper, men i stedet er udtrykt i forhold til specifikationer af de påkrævede ressourcer. Planlægningsprogrammet vil derefter kunne tildele de relevante operationsressourcer fra det websted, der er planlagt til produktion på. Hvis der er små forskelle i tiden, eller hvis opstillingstiden for en bestemt operation er lokationsspecifikke, kan du angive disse oplysninger ved at tilføje en ekstra Operationsrelation for det pågældende websted.  

For at få fuldt udbytte af fordelene ved delt ruter, skal du også bruge ressourceforbrug på den tilknyttede stykliste stykliste. Når du har angivet flaget for ressourceforbrug på styklistelinjen, lagerstedet og lokaliteten, der skal forbruges råmaterialer fra udledes fra den operationsressource, der planlægges operationen på. Derfor behøver lagerstedet og lokaliteten skal fastlægges, indtil produktionen planlægges faktisk. På denne måde kan du både Styklisten og ruten uafhængigt af den fysiske placering, hvor produktet er fremstillet.

### <a name="standard-operation-relations"></a>Standard operationsrelationer

Hvis din virksomhed bruger standardiserede operationer i produktionen, og der er meget lidt eller ingen variation i opstillingstid, Operationstid, forbrugsberegning, omkostningsberegning, og osv., du kan med fordel oprette standard operationsrelationer for alle operationer. I dette tilfælde skal du undgå at oprette operationsrelationer, der er specifikke for en rute eller frigivet produkt.  

Hvis du også express ressourcekrav med hensyn til færdigheder og funktioner og gøre dine ruter uafhængige af webstedet, kan du hjælpe, holde den løbende vedligeholdelse af dine forretningsprocesser på et minimum.  

Når du bruger denne metode, den **operationsrelationer** side, bliver din primære destination for opretholdelse af procestid og andre egenskaber.

### <a name="resource-specific-process-times"></a>Ressourcespecifikke procestider

Hvis du ikke angiver en operationsressource eller ressourcegruppe som en del af ressourcekravene for en operation, kan de relevante ressourcer fungere ved forskellige hastigheder. Den tid, der kræves for at behandle en operation kan derfor variere. Du kan løse problemet, kan du bruge den **formel** på operationsrelationen til at angive, hvordan procestiden beregnes. Følgende valgmuligheder er tilgængelige:

-   **Standard** – (standard indstilling) beregningen bruger kun felterne fra operationsrelationen og ganger den angivne procestid med ordreantallet.
-   **Kapacitet** – omfatter beregningen af den **kapacitet** fra operationsressourcen. Tiden er derfor afhængige af ressourcen. Den værdi, der er angivet på operationsressourcen er kapacitet pr. time. Denne værdi ganges med ordreantallet og **faktor** værdi fra operationsrelationen.
-   **Batch** – en batchkapacitet beregnes ved hjælp af oplysninger fra operationsrelationen. Antallet af partier og derfor procestiden kan beregnes baseret på ordreantallet.
-   **Ressource batch** – denne indstilling er grundlæggende den samme som den **parti** indstilling. Dog omfatter beregningen af den **Batch-kapacitet** fra operationsressourcen. Tiden er derfor afhængige af ressourcen.


<a name="see-also"></a>Se også
--------

[Bills of materials and formulas](bill-of-material-bom.md)

[Cost categories used in production routing](../cost-management/cost-categories-used-production-routings.md)

[Resource capabilities](resource-capabilities.md)

[Electronic signature overview](/dynamics365/operations/organization-administration/electronic-signature-overview)


