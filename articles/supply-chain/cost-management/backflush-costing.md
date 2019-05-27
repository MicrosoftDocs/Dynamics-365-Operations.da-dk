---
title: Efterkalkuleret varetræk
description: I dette emne introduceres begrebet efterkalkuleret varetræk, der bruges til lean manufacturing.
author: cvocph
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanCosting, LeanCostingTimeBucket
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272063
ms.assetid: 62a2a7da-ff79-49bf-a6e8-29460ba5252f
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: conradv
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 484bac74ccb498f0b006458f5e6d8fb0e9461a8f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556063"
---
# <a name="backflush-costing"></a>Efterkalkuleret varetræk

[!include [banner](../includes/banner.md)]

I dette emne introduceres begrebet efterkalkuleret varetræk, der bruges til lean manufacturing. 

Med efterkalkulation af lean manufacturing kan produktionsflowet bruge metoden til omkostningsakkumulering, også kaldet efterkalkuleret varetræk. I metoden til efterkalkuleret varetræk akkumuleres de direkte materialer, der forbruges, i produktionsflowets omkostningskonto for igangværende arbejde (IGVF). Lagermodelgruppen for standardkostprisen anvendes. De produkter, der modtages fra produktionsflowet, trækkes fra IGVF til deres standardkostpris. Den væsentligste forskel mellem efterkalkuleret varetræk og standardkostprisen er, at for efterkalkuleret varetræk beregnes afvigelser ikke pr. kanban eller færdigt produkt. I stedet beregnes afvigelser pr. produktionsflow over en periode. Denne metode medfører et virkeligt lean koncept til rapportering af materialeforbrug. Dedikerede plukkede mængder materiale rapporteres ikke til en kanban- eller produktionsordre. I stedet klargøres komplette batches eller materialehåndteringsenheder til produktionsflowet. Når batches eller materialehåndteringsenheder registreres som tomme, bliver de angivet som forbrugt. Avanceret forbrug kan bruges, afhængigt af [konfigurationen af produktionsflowet](../production-control/lean-manufacturing-modeling-lean-organization.md). Før avanceret forbrug kan anvendes, skal organisationer tillade sig at lade materiale forsvinde i produktionsflowets IGVF. Det periodiske efterkalkulerede varetræk bestemmer den faktiske værdi af IGVF til slutningen af perioden. Denne afgørelse er baseret på kanban-materialehåndteringsenhederne og kanban-jobbets status. Afvigelser mellem de gældende værdier og de faktiske værdier for IGVF pr. kostprisgruppe og vare efterkalkuleres og vises som afvigelser.

## <a name="configuring-backflush-costing"></a>Konfiguration af efterkalkuleret varetræk
Du kan aktivere efterkalkulation ved at foretage følgende opsætning:

-   **Opret IGVF-konti til produktionsgruppen og produktionsflowet.** IGVF-konti til produktionsflowet er angivet i produktionsgruppen. Det efterkalkulerede varetræk for produktionsflowet beregner afvigelser som forskellen i IGVF-værdien, før og efter efterkalkuleret varetræk er udført for hvert produktionsflow. Det anbefales derfor, at du opretter en IGVF-konto for hvert produktionsflow.
-   **Tildel en omkostningsart til ressourcegruppen.** Du skal tildele en omkostningsart til kørselskategorien for arbejdscellen. Du kan bestemme afvigelser pr. aktivitet ved at oprette en omkostningsart for hver arbejdscelle. Omkostningsarterne for opsætning og antal indgår ikke i efterkalkulation af lean manufacturing. IGVF-kontiene pr. ressourcegruppe ignoreres i efterkalkuleret varetræk. For aktiviteter udført af underleverandør kræves ingen omkostningsart. Den kostprisgruppe, der er tilknyttet den aktive tjeneste, bruges i stedet.
-   **Tildel kostprisgrupper.** Hvis du vil aktivere segmentering af kostbidrag i et produktionsflow, skal du tildele kostprisgrupper efter kostgruppetype:
    -   **Kostprisgruppe for direkte materiale** - Direkte materiale kræver en kostprisgruppe, der identificerer materialekategorien for efterkalkulation. Denne kostprisgruppe aktiverer en samlet oversigt over omkostninger, IGVF og afvigelser efter direkte materialer.
    -   **Kostprisgruppe for direkte produktion** - Kostprisgruppen for direkte produktion henter det direkte kostbidrag for driftsmæssige ressourcer til produktionsflowet. Denne kostprisgruppe aktiverer en samlet oversigt over omkostninger, IGVF og afvigelser efter direkte produktionsomkostning.
    -   **Indirekte kostprisgruppe** Den Indirekte kostprisgruppe kræves for at beregne det indirekte kostbidrag til produktionsflowet. Denne kostprisgruppe aktiverer en samlet oversigt over omkostninger, IGVF og afvigelser efter indirekte omkostning.
    -   **Direkte outsourcingkostprisgruppe** - Kostprisgruppen for tjenesterne aktiverer en samlet oversigt over tildelte omkostninger og IGVF og bestemmer omkostningsafvigelserne i de tjenester, der udføres af underleverandør.
    -   **Kostprisgruppen for et færdigt produkt** - Færdigvarer kræver en kostprisgruppe, der identificerer produktkategorien for efterkalkulation. Denne kostprisgruppe aktiverer en samlet oversigt over omkostninger, IGVF og afvigelser efter produktkategori. Standardkostprisen for produkter beregnes ved hjælp af omkostningsberegningen, der er baseret på styklisten (BOM), og enten produktionsflowet og kanban-regler eller ruten.

### <a name="costing-sheet"></a>Kostprisark

Efterkalkulationsarket modellerer omkostningsstrukturen for firmaet og bygges af kostprisgrupperne for at klassificere omkostningerne. Efterkalkulationsarket har forskellige udformninger. Det viser oplysninger om omkostninger i overensstemmelse med den struktur, der er anvendt i det. I efterkalkulationsarket kan du også definere den formel, der skal bruges til at beregne de indirekte omkostninger. Beregningsformlen kan være baseret på antal, vægt, rumfang eller værdi.

-   **Definer en efterkalkulationsversion.** I efterkalkulationsversionen definerer firmaet, hvordan omkostningen skal vedligeholdes. En efterkalkulationsversion kan indeholde standardkostprisposter eller planlagte kostprisposter, afhængigt af hvilken efterkalkulationstype der er tildelt til efterkalkulationsversionen. Den efterkalkulationsversion, der anvendes til efterkalkulation af lean manufacturing, skal baseres på standardomkostninger.
-   **Tilknyt en lagermodelgruppe for frigivne produkter.** Alle produkter, der er relateret til produktionsflowet, skal tildeles til en lagermodelgruppe, der bruger lagermodelgruppen **Standardkostpris**. Standardkostprisen vedligeholdes pr. lokation og aktiveringsdato. For produktmastere kan lagermodelgruppen kun vælges, hvis omkostningerne vedligeholdes pr. variant eller produktmaster.
-   **Pr. definition er underleverandørtjenester ikke-lagerførte tjenester.** Underleverandørens aktiviteter har ingen lagermodelgruppe. For at efterkalkulere en aktivitet, der er udført af underleverandør, korrekt, skal du sikre dig, at serviceaktiviteten hører til en lagermodelgruppe, hvor lagerpolitikken er indstillet til **Lagerført produkt = falsk**.

For slutprodukter kræver beregning af omkostninger, der er baseret på produktionsflowet, at en standardomkostning vedligeholdes for de tjenester, der er relateret til underleverandøraktiviteter. Den kostprisgruppe, der er tildelt til tjenesterne, bruges til at bestemme omkostningsafvigelserne for den aktivitet, der er udført af underleverandør.

## <a name="cost-calculation-for-lean-manufacturing"></a>Omkostningsberegning for lean manufacturing
For produkter, der leveres af et produktionsflow, skal styklistekalkulationen baseres på en ruteversion eller et produktionsflow. Styklistekalkulationen beregner kostprisen for et produkt og den relaterede opdeling på de ressourcer og materialer, der er nødvendige for at bygge produktet. Fradraget fra IGVF-kontoen for produktionsflowet sker ved at bruge opdelingen af et produkt efter vare- og kostprisgruppe.

### <a name="calculation-that-is-based-on-the-production-flow"></a>Kalkulation, der er baseret på produktionsflowet

lean manufacturing til Microsoft Dynamics 365 for Finance and Operations er uafhængig af ruter. Omkostningsberegningen for produkter, der leveres fra et produktionsflow, kan baseres på selve produktionsflowet. Før beregningen kan udføres skal en kanban-regel oprettes, der leverer produktet fra produktionsflowet. Hvis et produkt kan leveres fra flere produktionsflow på det samme sted på beregningsdatoen, kan du vælge produktionsflowet for styklistekalkulationen. På siden **Standardproduktionsflow** kan du konfigurere et produktionsflow for standard for hver vare. Hvis der findes flere kanban-regler for samme produkt i det produktionsflow, der er aktivt på beregningsdatoen, vælges den første kanban-regel, der er aktiv for beregningen.

### <a name="calculation-that-is-based-on-the-route"></a>Beregning, der er baseret på ruten

Beregning, der er baseret på en rute, er gyldig som en beregning, der er baseret på et produktionsflow. En beregning, der er baseret på en rute, kan dog ikke bruge efterkalkulation til lean manufacturing-funktioner. Ruten skal bruge ressourcekravene for ressourcegrupper. Hvis du vil undgå systematiske afvigelser, skal den bruge samme arbejdsceller, eller i det mindste de samme omkostningsarter. Igen skal du undgå omkostningsarter for opsætning og antal. De hjælper ikke med at beregne omkostningerne i en mere detaljeret opdeling end efterkalkuleret varetræk for lean manufacturing. Overvej at resultaterne af kostprisopdelingen for at finde ud af, hvilken indstilling (produktionsflowet eller rute), du skal bruge til at beregne kostprisen. Den version, der kommer tættest på virkeligheden og giver færrest afvigelser overordnet set, er den bedste valgmulighed. I et Lean manufacturing-miljø, hvor et produkt leveres af et enkelt produktionsflow og en enkelt kanban-regel, er den beregning, der er baseret på produktionsflowet, sandsynligvis mest nøjagtig. For et produkt, der kan leveres af lean manufacturing og produktionsordrer på samme sted, eller som kan have flere produktionsflow eller flere kanban-regler i det samme flow, kan en beregning være mere nøjagtig, hvis den er baseret på en ruteversion, der er udviklet specielt til omkostningsberegningen, og ikke til produktion. Produktionsflowberegningen skal bruges til beregning af produkter, der involverer underleverandørarbejde. I Microsoft Dynamics 365 for Finance and Operations bruger omkostningsmodellerne for underleverandørarbejde via produktionsordrer og underleverandørarbejde i Lean manufacturing to forskellige metoder. Lean manufacturing introducerer en ny kostprisgruppetype **Direkte outsourcing** for at beregne underleverandørtjenester.

## <a name="material-consumption"></a>Materialeforbrug
Når der forbruges materiale fra lageret til IGVF, føjes materialekostprisen til IGVF til den faktiske standardkostpris for en kostprisgruppe. Denne handling finder sted på følgende betingelser:

-   Kanban-afgange bogføres for kanban-pluklinjer, der opdaterer lageret.
-   Overførselsjob, der opdaterer lager ved plukning, fuldføres, men ikke modtagelse (overførsel af materiale fra lageret til IGVF).

## <a name="receiving-products-from-the-production-flow"></a>Modtagelse af produkter fra produktionsflowet
Produkter modtages fra produktionsflowet på følgende betingelser:

-   Procesjob, hvor **Opdater lagerbeholdning ved modtagelse** er indstillet til **Ja**, fuldføres.
-   Overførselsjob, hvor lageret opdateres ved modtagelse, men hvor **Opdater lagerbeholdning ved angivelse af pluk** er indstillet til **Nej** (Overfør fra IGVF til lager), fuldføres. Med denne indstilling kan du modtage produkter fra et produktionsflow, uafhængigt af stykliste- og rutekonfigurationen. Processen følger blot de fysiske processer. Denne indstilling er særligt velegnet til modtagelse af biprodukter, samprodukter eller spild fra et produktionsflow og til at korrigere omkostningssaldoen for produktionsflowets IGVF tilsvarende.

Produkter, der modtages fra produktionsflowet, trækkes fra IGVF.

## <a name="products-in-wip"></a>Produkter i IGVF
I IGVF-modellen til Lean manufacturing i Microsoft Dynamics 365 for Finance and Operations kan du bruge status for kanban-materialehåndteringsenheden til at administrere det materiale, halvfabrikata og færdigvarer, der er en del af IGVF.

-   **Tildelt** - Kanban kan har forbrugt materiale, der er registreret i IGVF.
-   **Modtaget** - Hvis en kanban refererer til den seneste aktivitet, hvor **Opdater lagerbeholdning ved modtagelse** er angivet til **Nej**, repræsenterer den en fuld materialehåndteringsenhed for et produkt eller et halvfabrikataprodukt, der ikke er registreret på lageret.

Bemærk, at materiale i IGVF ikke er synligt i oversigter over disponibel lagerbeholdning. Det er dog synligt i oversigterne over kanban-antal.

## <a name="consuming-products-in-wip"></a>Forbrug af produkter i IGVF
Produkter i IGVF forbruges, når tilsvarende kanban-materialehåndteringsenheder tømmes. Et signal om en tom kanban medfører ikke en aktiv efterkalkulationspostering, men træder i kraft, når næste efterkalkulerede varetræk køres. Tomme kanban-håndteringsenheder efterkalkuleres ikke længere som disponibel lagerbeholdning og beregnes derfor som forbrugt inden for perioden.

### <a name="automatic-empty-registration"></a>Automatisk tømningsregistrering

Planlagte eller hændelses-kanbans kan indstilles til automatisk tømningsregistrering i kanban-reglen:

-   **Ved modtagelse af håndteringsenheder** – Som standard angives materialet som forbrugt for planlagte kanbans, når det sidste job i den pågældende kanban er fuldført. For fastmængde-kanbans anbefales denne indstilling kun for enkeltbeholder-kanbans, fordi den returnerer kortet til efterspørgselskilden, når en kanban modtages på den endelige destination.
-   **Ved registrering af kildeforudsætningen** - Denne indstilling er kun tilgængelig for hændelses-kanbans, og er standardindstillingen for dem. I forbindelse med IGVF er denne indstilling velegnet til at holde IGVF ren, fordi kanbans til komponenter i IGVF tømmes automatisk, og derfor forbruges de fra IGVF, når den overordnede kanban forberedes.

Konklusionen er, at kanban-materialehåndteringsenheder kan tildeles (= igangværende), modtages (= fuld) eller tømmes. Der er ingen delvis tømning. Hvis du vil aktivere præcis registrering af forbrug, er det derfor vigtigt, at du begrænser de produktmængder, der i en kanban, så de er mindre end forbruget pr. periode. Produkter, der flyttes til produktionen i store batches, som dækker dages eller ugers efterspørgsel, skal ikke forbruges til IGVF. I stedet for skal disse produkter opbevares på lageret.

## <a name="backflush-costing"></a>Efterkalkuleret varetræk
Kør efterkalkuleret varetræk for periodisk at vurdere IGVF og producere en ultimostatus, der beregner afvigelser af materiale, arbejdskraft og indirekte omkostninger. De beregnede afvigelser bogføres på afvigelseskontiene. I den efterkalkuleret varetræksproces bruges alle produktionsflow for den juridiske enhed i samme batchkørsel. Når efterkalkuleret varetræk køres i en batch, kan behandlingen være flertrådet efter produktionsflow. Efterkalkulationsperioden defineres af en slutdato. Du kan ikke bogføre nye posteringer på en dato, hvor der er kørt en beregning af efterkalkuleret varetræk. Du bør aldrig køre efterkalkuleret varetræk for dags dato, før dagen faktisk er forbi. Efterkalkuleret varetræk udfører følgende trin.

1.  Bestem de uudnyttede mængder i produktionsflowet pr. periodens slutdato. Når efterkalkuleret varetræk er udført, kan du få vist de uudnyttede mængder på datoen for efterkalkulationskørslen i dialogboksen **Uudnyttede mængder**.
2.  Beregn produktionsflowets realiserede nettoforbrug i perioden.
3.  Fjern IGVF fra det realiserede ressourceforbrug og produkter.
4.  Beregn afvigelser i produktion til standardomkostninger for perioden. **For anvendte komponenter i perioden:**
    -   Foretag økonomisk opdatering af de realiserede nettomængder af materiale, som produktionsflowet har forbrugt i perioden. Systemet behandler de individuelle lagertransaktioner i FIFU-rækkefølge (først ind først ud) for at foretag økonomisk opdatering af de fysisk opdaterede posteringer for produktionsflowet, indtil de realiserede nettomængder for perioden er nået.
    -   Posteringer opdeles økonomisk for at tilknytte de nøjagtigt forbrugte mængder.
    -   Uudnyttede mængder i produktionsflowets IGVF har fortsat status som fysisk opdaterede.

    **For fuldførte produktionsmængder i perioden:**
    -   Foretag økonomisk opdatering af lagerposteringer for de fuldførte mængder for perioden.

    **For konverteringsomkostningen:**
    -   De anvendte posteringer af konverteringsomkostninger (ruteposteringer), der er registreret for perioden, opdateres økonomisk.
    -   Alle direkte produktionsomkostninger opdateres økonomisk. Alle kanban-procesjob, der fuldføres i perioden, akkumuleres.
    -   Alle indirekte omkostninger, der er beregnet for det anvendte materiale i perioden, beregnes og fratrækkes fra IGVF. De resterende indirekte omkostninger bogføres som en afvigelse.

5.  Beregn afvigelserne i produktionen til standardomkostninger. Afvigelsen beregnes pr. kostgruppe.





