---
title: "Administrere underleverandørarbejde i produktionen"
description: "I dette emne beskrives, hvordan underleverandøroperationer administreres i Microsoft Dynamics 365 for Finance and Operations. Det beskrives med andre ord, hvordan produktionsoperationer, der er tildelt til en ressource, administreres af en leverandør."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 26feea4d86cf8b976f41342c8543594593c4b135
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="manage-subcontracting-work-in-production"></a>Administrere underleverandørarbejde i produktionen

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan underleverandøroperationer administreres i Microsoft Dynamics 365 for Finance and Operations. Det beskrives med andre ord, hvordan produktionsoperationer, der er tildelt til en ressource, administreres af en leverandør.

I [produktionsprocesser](production-process-overview.md) kan arbejdet udføres af ressourcer, der ejes eller administreres af leverandører. Leverandørressourcer bruges typisk til at udjævne periodiske ekstra behov, der overgår den tilgængelige kapacitet for en virksomheds egne ressourcer. Leverandøren kan muligvis også tilbyde særlige [ressourceegenskaber](resource-capabilities.md) eller ressourcer til en lavere pris.  

Afhængigt af de leverandørressourcer, der anvendes i produktionsprocessen, stiller en [rute](routes-operations.md) ofte yderligere logistiske krav, fordi de materialer og halvfabrikata først skal transporteres til leverandørens sted. Resultatet af operationen hos underleverandøren skal derefter transporteres enten til den lokalitet, der er allokeret til den næste operation, eller til et lagersted med færdigvarer.  

Når der bruges underleverandørarbejde eller -aktiviteter, påvirker de alle faser af operationer, fra definitionen af de operationer, der skal bruges i produktion, efterkalkulation, prognoser, planlægning og tidsplanlægning, til administration af logistik for materiale, halvfabrikata og færdigvarer. Endelig kræver disse ressourcer deres egne processer til styring af regnskab og omkostninger.  

For interne ressourcer tildeles typisk en fast omkostningssats for en periode. Derimod er omkostningerne for underleverandørressourcer baseret på købsprisen for den relaterede service. Servicen defineres som et andet produkt og bruges til at udføre udtagnings- og indkøbsprocesserne for en given underleverandøroperation.  

Der er i øjeblikket ingen eksplicit definition af halvfabrikata i Microsoft Dynamics 365 for Finance and Operations. For en produktionsordre, der kræver mere end én operation for at omdanne råvarer til en færdigvare, bogføres færdigvaren først tilbage på lageret i den sidste operation. De halvfabrikata, der er et resultat af de tidligere operationer, figurerer i igangværende forarbejdning (IGVF), men de bogføres eller spores ikke på lageret. Selvom du kan opdele ruter og styklister i flere mindre enheder, øger denne metode antallet af produkter, styklister og ruter, der skal administreres.  

Der er to metoder til modellering af underleverandørarbejde til produktionsoperationer. Disse metoder adskiller sig fra hinanden på den måde, som processen med underleverandørarbejde kan modelleres på, den måde, halvfabrikata repræsenteres i processen, og den måde, omkostningsstyring administreres på.

-   Underleverandørarbejde på ruteoperationer i produktionsordrer eller batchordrer
    -   Serviceproduktet skal være et produkt, der er på lager, og det skal være en del af styklisten.
    -   Denne metode understøtter først ind først ud (FIFO) eller standardomkostninger.
    -   Halvfabrikata er repræsenteret af serviceproduktet i processen.
    -   Omkostningsstyring tildeler de omkostninger, der er knyttet til arbejde udført af underleverandør, til materialeomkostningerne.
-   Underleverandørarbejde på produktionsflowaktiviteter i et lean produktionsflow
    -   Servicen er et ikke-lagerført serviceprodukt, og det er ikke en del af styklisten.
    -   Denne metode bruger købsaftaler som serviceaftaler.
    -   Denne metode bruger efterkalkuleret varetræk.
    -   Denne metode giver mulighed for aggregerede og asynkrone indkøb. (Materialeforbrug er uafhængigt af indkøbsprocessen).
    -   Omkostningsstyring allokerer arbejde udført af underleverandør i sin egen kostprisopdelingsblok.

## <a name="subcontracting-of-route-operations"></a>Underleverandørarbejde på ruteoperationer
Hvis du vil bruge underleverandørarbejde på ruteoperationer til produktions- eller batchordrer, skal det serviceprodukt, der anvendes til udtagning af servicen, defineres som et produkt af typen **Serviceydelse**. Det skal desuden have en varemodelgruppe, hvor indstillingen **Lagerført produkt** under **Lagerpolitik** er sat til **Ja**. Denne indstilling angiver, om et produkt er registreret som lager på produktkvitteringen (**Lagerført produkt** = **Ja**), eller om produktet er udgiftsført på en driftskonto (**Lagerført produkt** = **Nej**). Selvom denne funktionsmåde kan virke modstridende, er den baseret på det faktum, at kun produkter, der har denne politik, kan oprette lagerposteringer, der kan bruges i omkostningsstyring til at beregne planlagte omkostninger og bestemme de faktiske omkostninger, når en produktionsordre afsluttes.  

Hvis den skal tages i betragtning ved planlægningen og omkostningsberegningen, skal servicen føjes til styklisten. Styklistelinjen skal være af typen **Leverandør** og skal fordeles til den ruteoperation, som servicen er tildelt til. Denne ruteoperation skal have en efterkalkuleret ressource og et ressourcekrav, der peger på en ressource af typen **Leverandør**, der forbinder operationen og relaterede service med den tilsvarende kreditorkonto.  

Når du bruger denne konfiguration, oprettes en indkøbsordre for det relaterede serviceprodukt, baseret på vurdering af en produktionsordre. Indkøbsordren for servicen bruges som et anker for underleverandøroperationerne. Underleverandørarbejdet kan håndteres via listesiden **Arbejde udført af underleverandør** i Produktionsstyring. Underleverandørarbejdet bruges til at levere råvarer og senere et halvfabrikataprodukt til leverandøren som forberedelse til operationen. Det bruges også til at modtage det færdige produkt af operationen hos underleverandøren i varemodtagelse, hvor serviceproduktet bruges til at identificere ankomsten af den halvfabrikatatproduktet. Når indkøbsordrelinjen modtages, opdateres produktionsoperationen med status fuldført.  

En produktionsordre kan have mange operationer, og hver af dem kan allokeres til en anden leverandør. Derfor kan en produktionsordre fra start til slut udløse flere indkøbsordrer.

## <a name="subcontracting-of-production-flow-activities"></a>Underleverandørarbejde på produktionsflowaktiviteter
Med [lean manufacturing](lean-manufacturing-overview.md)-løsningsmodellerne fungerer underleverandørarbejdet som en service, der er relateret til en aktivitet i et [produktionsflow](tasks/create-production-flow-version.md) (emnet Opgaveguide). Derfor omtales denne type underleverandørarbejde også som [aktivitetsbaseret underleverandørarbejde.](activity-based-subcontracting.md) En særlig kostprisgruppetype, **Direkte outsourcing**, er blevet indført, og de servicer, der udføres af underleverandører, er ikke en del af styklisten for færdigvarerne. Når du bruger lean manufacturing, defineres alle aktiviteter af kanbans, der kan relateres til en eller flere produktionsflowaktiviteter. Denne beskrivelse kunne indtil videre lige så godt være en beskrivelse af produktionsordrer. Men mens produktionsordrer altid skal afsluttes med et færdigt produkt, kan du oprette kanbans for at levere et halvfabrikataprodukt. Du behøver ikke at indføre et nyt produkt og styklisteniveau.  

Da kanban-regler kan være meget dynamiske, kan du udforme forskellige forsyningsvarianter for samme produkt i et produktionsflow. Når du bruger lean underleverandørarbejde, er materialeflowet og det økonomiske flow strengt adskilt. Alle materialeflows repræsenteres af kanban-aktiviteter. Indkøbsordrerne for serviceprodukterne og bogføring af kvitteringer for disse servicer kan automatiseres, baseret på status for kanban-job i produktionsflowet. Kanban-job kan startes og fuldføres, inden der oprettes indkøbsordrer. Dokumenter vedrørende underleverandørarbejde (indkøbsordre og købskvittering for servicen) kan aggregeres efter periode og service. Derfor kan antallet af indkøbsdokumenter og -linjer holdes nede, selv i operationer, der gentages ofte, hvor leverandører leverer underleverandørydelser i et samlet flow.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Modellering af underleverandørarbejde i et produktionsflow

I et [lean produktionsflow](lean-manufacturing-modeling-lean-organization.md) kan en procesaktivitet defineres som givet i underentreprise, når den tildeles til en arbejdscelle (ressourcegruppe), der har en enkelt leverandørressource. Når en arbejdscelle gives i underentreprise, skal de relaterede procesaktiviteter knyttes til en aktiv købsaftalelinje, der indeholder servicevaren og prisen på servicen. Serviceaftalen for aktiviteten definerer også beregningsforholdet mellem produktantallet for kanban-jobbet og det resulterende serviceantal. Du kan vælge, om serviceantallet skal beregnes på grundlag af antallet af job, det produktantal, der rapporteres for jobbene eller det samlede produktantal (dette samlede antal omfatter kasserede produkter).  

Overførselsaktiviteter kan også defineres som givet i underentreprise. Denne definition opstår implicit, når du vælger den part, der er ansvarlig for forsendelsen, i overførselsaktiviteten. Når du vælger **Afsender** eller **Modtager**, betragtes aktiviteten som givet i underentreprise, hvis det tilsvarende kilde- eller destinationslagersted er et lagersted, der administreres af leverandøren. Når du vælger **Fragtmand**, er aktiviteten altid givet i underentreprise. Som underleverandørprocesaktiviteter skal en overførselsaktivitet for en underleverandør have forbindelse til en serviceaftale, før produktionsflowet kan aktiveres.

### <a name="backflush-costing"></a>Efterkalkuleret varetræk

Omkostningsregnskabet for arbejde udført af underleverandør er helt integreret i efterkalkulationen for lean manufacturing-løsningen (efterkalkuleret varetræk). Når indkøbsordretilgangen af servicen bogføres, eller når fakturering finder sted, fordeles omkostningerne for servicen til produktionsflowet. For efterkalkuleret varetræk beregnes variansen af underleverandørservicer ved modregning af underleverandørarbejdsblokkens standardkostpris for modtagne produkter mod de faktisk modtagne og fakturerede ydelsesmængder.

## <a name="material-supply-for-subcontracted-operations"></a>Materialeforsyning til underleverandøroperationer
Halvfabrikata og andre relaterede materialer skal overføres til det sted, hvor arbejdet udføres fysisk. Når du bruger underleverandøroperationer og aktiviteter, er denne overførsel ofte relateret til meromkostninger til transport til et sted, der drives af kreditor. Hvis du tildeler materiale i styklisten for operationen hos underleverandøren, kan du angive, at materialet skal gemmes midlertidigt på indlagringslokationen for ressourcegruppen for den tildelte ressource. Varedisponering eller lean genopfyldning klargør derefter materialet til den pågældende lokation.  

For at modellere det lager, der er placeret på leverandørens lokalitet, er det bedste praksis i branchen at definere et lagersted, der administreres af leverandøren. Du kan let definere et leverandøradministreret lagersted ved at oprette et nyt lagersted og tildele kreditorkontoen. For at dokumentere, at materiale skal overføres til leverandøren før en operation kan udføres, skal du allokere leverandør det leverandøradministrerede lagerstedet til indlagringslagerstedet for den ressourcegruppe, der opbevarer ressourcen.  

For at genbestille materiale til dette lagersted kan du bruge flere strategier:

-   Flytteordrer
-   Overførselskladder
-   Udbetalingskanbans
-   Direkte køb til leverandørens lokalitet

Halvfabrikata er en undtagelse til denne regel. Hvis du vil overføre halvfabrikata, er du begrænset til disse indstillinger:

-   For produktions- og batchordrer kan halvfabrikata kun overføres logisk ved hjælp af pluklistekladden fra listesiden **Arbejde udført af underleverandør**. Denne kladde opretter et følgeseddeldokument, der kan bruges til at overføre halvfabrikata og råvarer til leverandøren.
-   For underleveranceoperationer i produktionsflow dokumenteres overførsel af halvfabrikata ved modtagelsen af udbetalingskanbans eller produktionskanbans hos kreditoren. Hvis du vil udforme en eksplicit overførselsaktivitet, kan du afslutte en produktionskanban med en ekstra overførselsaktivitet.

**Bemærk:** En produktionsrute for en enkelt produktionsordre kan ikke gå på tværs af flere steder. Denne regel gælder også for det arbejde, der udføres af underleverandører. Lagerstederne, der repræsenterer leverandøradministrerede materialelokationer, skal derfor være defineret på samme sted som de interne ressourcer, der bruges i ruten. Selvom produktionsflow kan gå på tværs af steder, kan de ikke transportere halvfærdige produkter fra én lokation til en anden, fordi denne handling indebærer en ændring af omkostningssammenhængen.  

Lagerstedet for udlagring og lokaliteten af en underleverandørs ressourcegruppe tildeles normalt direkte til lagerstedet og lokaliteten af det næste trin i rute- eller produktionsflowoperationen. Denne konfiguration hjælper med at reducere den mængde jobrapportering, der forekommer, eller antallet af yderligere overførselsoperationer, der skal modelleres.




