---
title: Administrere underleverance arbejde i produktionen
description: "Dette emne forklarer, hvordan underleverandøroperationer administreres i Microsoft Dynamics 365 for operationer. Med andre ord, det forklarer, hvordan produktionsoperationer, der er tildelt en ressource, der administreres af en leverandør."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 79430358bebd93fd96f1169d22737d3537dbfc08
ms.lasthandoff: 03/31/2017


---

# <a name="manage-subcontracting-work-in-production"></a>Administrere underleverance arbejde i produktionen

Dette emne forklarer, hvordan underleverandøroperationer administreres i Microsoft Dynamics 365 for operationer. Med andre ord, det forklarer, hvordan produktionsoperationer, der er tildelt en ressource, der administreres af en leverandør.

I [produktionsprocesser](production-process-overview.md), arbejdet udføres af ressourcer, der ejes eller administreres af kreditorer. Kreditorressourcer bruges typisk til niveau periodiske overskydende behov, der overgår den tilgængelige kapacitet for en virksomheds egne ressourcer. Leverandøren kan muligvis også tilbyde særlige [ressourceegenskaber](resource-capabilities.md)eller ressourcer til en lavere pris.  

Afhængigt af leverandør-ressourcer, der anvendes i produktionsprocessen, en [rute](routes-operations.md) har ofte yderligere logistiske krav, fordi de materiale- og halvfabrikata skal først transporteres til kreditorens websted. Resultatet af operationen hos underleverandøren transporteres derefter enten til den placering, der er allokeret til den næste operation eller et lager med færdigvarer.  

Når der bruges underleverandører operationer eller aktiviteter, kan de påvirke alle faser af operationer fra definitionen af de operationer, der skal bruges i produktionen, omkostningsberegning, forecasting, planlægning og planlægning til administration af logistik for materiale, halvfabrikata og færdigvarer. Endelig kræver disse ressourcer deres egne processer til kontrol af regnskabs- og omkostningsberegning.  

For interne ressourcer tildeles typisk en faste omkostningssats for en periode. Derimod er omkostningerne for underleverandører ressourcer baseret på købsprisen for de relaterede service. Tjenesten er defineret som et andet produkt, og bruges til at drive udtagning og købe processer for en given underleverandøroperation.  

Der er i øjeblikket ingen eksplicit begrebet halvfabrikata i Microsoft Dynamics 365 for operationer. For en produktionsordre, der kræver mere end én handling for at omdanne råvarer til en færdigvare, bogføres færdigvaren tilbage på lageret i den sidste operation. De halvfabrikata, der resulterer i de tidligere operationer figurerer i igangværende arbejde (IGVA), men de er ikke bogført eller spores på lageret. Selvom du kan opdele ruter og styklister (styklister) i flere mindre enheder, øger denne metode antallet af produkter, styklister og ruter, der skal administreres.  

Der er to metoder til modellering underleverandører til produktionsoperationer. Disse metoder er forskellige i den måde, at processen underleverance kan modelleres, den måde, halvfabrikata er repræsenteret i processen, og den måde, omkostningsstyring er administreret.

-   Udlicitering af ruteoperationer i produktionsordrer eller batchordrer
    -   Service-produktet skal være et produkt, der er på lager, og det skal være en del af Styklisten.
    -   Denne metode understøtter først ind først ud (FIFO) eller standardomkostninger.
    -   Halvfabrikata er repræsenteret af produktets service i processen.
    -   Omkostningsstyring tildeler de omkostninger, der er knyttet til arbejde udført af underleverandør til de materialeomkostninger.
-   Underentreprisen af produktionsflowaktiviteter i et lean produktionsflow
    -   Tjenesten er et ikke-lagerførte service produkt, og det er ikke en del af Styklisten.
    -   Denne metode bruger købsaftaler som serviceaftaler.
    -   Denne metode bruger efterkalkuleret varetræk.
    -   Denne metode giver mulighed for indkøb af aggregerede og asynkrone. (Materialeforbrug er uafhængig af indkøbsprocessen.)
    -   Omkostningsstyring allokerer arbejde udført af underleverandør i sine egne omkostninger opdeling blok.

## <a name="subcontracting-of-route-operations"></a>Udlicitering af ruteoperationer
Hvis du bruger underleverance af ruteoperationer til produktion eller batchordrer, service-produkt, der anvendes til udtagning af tjenesten skal defineres som et produkt af den **Service** type. Det skal desuden have en varemodelgruppe, der har den **produkt på lager** indstilling **lager politik** indstillet til **Ja**. Denne indstilling angiver, om et produkt er registreret som lager på produktkvitteringen (**produkt på lager** = **Ja**), eller om produktet er udgiftsført på en driftskonto (**produkt på lager** = **Nej**). Selvom denne funktionsmåde kan virke modstridende, er det det faktum, at kun produkter, der har denne politik oprettes der lagerposteringer, der kan bruges i omkostningsstyring til at beregne planlagte omkostninger og bestemme de faktiske omkostninger, når en produktionsordre afsluttes.  

Hvis du vil tages i betragtning ved planlægningen og omkostningsberegning, skal tjenesten føjes til Styklisten. Styklistelinjen skal være af den **leverandør** type og skal fordeles til ruteoperationen, som tjenesten er tildelt til. Denne ruteoperation skal have en efterkalkuleret ressource og ressourcekrav, der peger på en ressource af den **leverandør** type, der forbinder handlingen og relaterede service til tilsvarende kreditorkontoen.  

Når du bruger denne konfiguration, oprettes en indkøbsordre for relaterede service-produkt, baseret på vurdering af en produktionsordre. Indkøbsordren for tjenesten bruges som et anker for på underleverandøroperationer. Underleverandør arbejde kan håndteres gennem de **givet i underentreprise arbejde** listeside i Produktionsstyring. Underleverandør arbejde bruges til at levere råvarer og senere et halvfabrikataprodukt til leverandøren som forberedelse til handlingen. Den bruges også til at få det færdige produkt for operationen hos underleverandøren i varemodtagelse, hvor produktet service bruges til at identificere ankomst af den halvfærdige vare. Når indkøbsordrelinjen er modtaget, opdateres produktionsoperationen som fuldført.  

En produktionsordre kan have mange operationer, og hver handling, der kan allokeres til en anden leverandør. Derfor kan en produktionsordre fra start til slut udløse flere indkøbsordrer.

## <a name="subcontracting-of-production-flow-activities"></a>Underentreprisen af produktionsflowaktiviteter
Den [lean produktion](lean-manufacturing-overview.md)løsning modeller underleverance arbejde som en tjeneste, der er relateret til en aktivitet af en [produktionsflowet](http://ax.help.dynamics.com/en/wiki/create-a-production-flow-version/) (guide emnet). Derfor denne type udlicitering også omtales som [aktivitetsbaseret underleverance.](activity-based-subcontracting.md) En særlig omkostningstype gruppe, **direkte outsourcing**, er indført og underleverandører tjenester ikke er del af Styklisten for færdige varer. Når du bruger lean produktion, vil alle aktiviteter, der er defineret af kanbans, der kan relateres til en eller flere produktionsflowaktiviteter. Denne forklaring lyder indtil videre, ligesom en forklaring af produktionsordrer. Der skal altid afsluttes produktionsordrer med et færdigt produkt, kan du oprette kanbans for at levere et halvfabrikataprodukt. Du behøver ikke at indføre et nyt produkt og styklisteniveau.  

Da kanban-regler kan være meget dynamisk, kan du udforme forskellige varianter af forsyning for samme produkt på et produktionsflow. Når du bruger lean er underleverance, materiale flow og det økonomiske flow strengt adskilt. Alle materialebevægelsen repræsenteres af kanban-aktiviteter. Indkøbsordrer for produkterne, service og kvittering for bogføring af disse tjenester kan automatiseres, baseret på status for kanban-job i produktionsflowet. Kanban-job kan startes og fuldføres, inden der oprettes indkøbsordrer. Underleverance dokumenter (købsordre og købsleverance af tjenesten) kan samles ved periode og service. Derfor kan antallet af dokumenter og linjer holdes små, selv i meget gentagne operationer, hvor producenter leverer underleverandørtjenester i et enkelt stykke flow.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Modellering underleverance i et produktionsflow

I en [lean produktionsflow](lean-manufacturing-modeling-lean-organization.md), en procesaktivitet kan defineres som givet i underentreprise når tildeles til en arbejdscelle (ressourcegruppen), der har en enkelt leverandørressource. Når en arbejdscelle er givet i underentreprise, skal de relaterede aktiviteter være knyttet til en aktiv købsaftalelinjen, der indeholder serviceartiklen og prisen på tjenesten. Serviceaftalen aktivitetens definerer også beregning af forholdet mellem produktantal, kanban-job og det resulterende antal service. Du kan vælge, om tjenesten antallet beregnes på grundlag af antallet af sager, god produktantal, der rapporteres i sagerne eller det samlede antal (dette samlede antal omfatter kasserede produkter).  

Overførselsaktiviteter kan også defineres som givet i underentreprise. Denne definition opstår implicit, når du vælger den part, der er ansvarlig for levering i overførselsaktivitet. Når du vælger **skipperen** eller **modtager**, hvis tilsvarende kilden eller destinationen lagersted er et lagersted, der administreres af leverandøren, betragtes aktiviteten givet i underentreprise. Når du vælger **luftfartsselskab**, aktiviteten er altid givet i underentreprise. Som underleverandør procesaktiviteter, en underleverandør overførselsaktivitet skal have forbindelse til en serviceaftale, før produktionsflowet, der kan aktiveres.

### <a name="backflush-costing"></a>Efterkalkuleret varetræk

Omkostningsregnskab for arbejde udført af underleverandør er fuldstændigt integreret i efterkalkulation af lean produktion løsningen (efterkalkuleret varetræk). Bogføring af købsordreleverance af tjenesten, eller når der sker fakturering, fordeles omkostningerne for tjenesten til produktionsflowet. Efterkalkuleret varetræk beregnes variansen af underleverandørtjenester ved modregning standardkostprisen for modtagne produkter mod de faktisk modtagne og fakturerede ydelsesmængder underleverance tekstblokken.

## <a name="material-supply-for-subcontracted-operations"></a>Materiale forsyning til underleveranceoperationer
Halvfabrikata og andre relaterede materialer skal overføres til det sted, hvor arbejdet udføres fysisk. Når du bruger underleverandøroperationer og aktiviteter, er denne overførsel ofte relateret til meromkostninger til transport til et websted, der drives af kreditor. Ved fordeling af materiale i Styklisten for operationen hos underleverandøren, kan du angive, at materialet skal gemmes midlertidigt på det input, hvor ressourcegruppen for den tildelte ressource. Varedisponering eller lean genopfyldning derefter bestemmelser materiale til den pågældende placering.  

For at modellere det lager, der er placeret på et websted af typen leverandør, er det bedste praksis i branchen til at definere et lagersted, der administreres af kreditor. Let at definere en leverandør administreret lagersted ved at oprette et nyt lagersted og tildele kreditorkontoen. For at dokumentere, at materiale, der skal overføres til leverandøren før en handling kan udføres, bør du allokere leverandør administreret lagerstedet til indlagringslagerstedet på den ressourcegruppe, der indeholder ressourcen.  

For at genbestille materiale til dette lager, kan du bruge flere strategier:

-   Flytteordrer
-   Overførselskladder
-   Tilbagetrækning kanbans
-   Direkte køb til sted, leverandør

Halvfabrikata er en undtagelse til denne regel. Hvis du vil overføre halvfabrikata, er du begrænset til disse indstillinger:

-   For produktions- og batchordrer halvfabrikata kan kun overføres logisk ved hjælp af pluklistekladden fra den **givet i underentreprise arbejde** listeside. Denne kladde oprettes en følgeseddel dokument, der kan bruges til at overføre halvfabrikata og råvarer til leverandøren.
-   Overførsel af halvfabrikata er til underleveranceoperationer i produktionsflow dokumenteret ved modtagelsen af tilbagetrækning eller produktion kanbans hos kreditoren. Hvis du vil udforme en eksplicit overførselsaktivitet, kan du afslutte en produktionskanban med en ekstra overførselsaktivitet.

**Bemærk:** en produktionsrute for en enkelt produktionsordre kan ikke på tværs af flere websteder. Denne regel gælder også for det arbejde, der er underleverandører. Lagerstederne, der repræsenterer derfor leverandør administreret materialet placeringer skal være defineret i samme område som de interne ressourcer, der bruges i ruten. Selvom produktionsflow kan på tværs af websteder, kan de transport halvfærdige produkter fra én lokation til en anden, fordi handlingen indebærer en ændring af kostprisen kontekst.  

Lagersted for udlagring og placeringen af en ressourcegruppe af underleverandørens tildeles normalt direkte til lagerstedet og lokaliteten af det næste trin i handlingen i rute- eller strømmen. Installationsprogrammet hjælper med at reducere mængden af job, rapportering, der opstår eller antal yderligere videregivelse, der skal modelleres.


