---
title: Oversigt over produktionsproces
description: Dette emne indeholder en oversigt over produktionsprocessen. Den beskriver de forskellige stadier af produktionsordrer, batchordrer og kanbans fra oprettelse af ordre til afslutning af regnskabsperioden.
author: cvocph
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, Kanban, ProdTable, ProdTableOverview, EcoResProductDiscreteManufacturingWorkspace, KanbanPrepareProductForLeanWorkspace, EcoResProductProcessManufacturingWorkspace, OpResLifecycleManagementWorkspace, ProdParmCostEstimation, ProdParmRelease, ProdSchedule, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19832
ms.assetid: 0e83c7ea-feba-4ed6-8717-8b48a3b8804a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3d82089d2917a0ec0b9ceead7cd1ec22457733
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188143"
---
# <a name="production-process-overview"></a>Oversigt over produktionsproces

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt over produktionsprocessen. Den beskriver de forskellige stadier af produktionsordrer, batchordrer og kanbans fra oprettelse af ordre til afslutning af regnskabsperioden. 

Produktionen af produkter, en proces, der også kaldes produktionslivscyklus, følger bestemte trin, der er nødvendige for at gennemføre fremstillingen af en vare. Livscyklussen begynder med oprettelsen af produktionsordre, batchordre eller kanban. Det slutter med en færdig produceret vare, der enten er klar til en kunde eller en anden fase i produktionen. Hvert enkelt trin i dette forløb kræver, at der angives forskellige former for oplysninger, så processen kan fuldføres. Når et trin er afsluttet, viser produktionsordren, batchordren eller kanban en ændring i produktionsstatus. Forskellige typer af produkter kræver forskellige fremstillingsprocesser.  

Modulet **Produktionsstyring** er knyttet til andre moduler, som **Administration af produktoplysninger**, **Lagerstyring**, **Finans**, **Lagerstedsstyring**, **Projektregnskab** og **Virksomhedsadministration**. Denne integration understøtter det informationsflow, der er nødvendigt for at fuldføre produktionen af en færdig vare.  

Produktionsprocessen er typisk påvirket af omkostningsregnskabet og metoderne til lagerets værdiansættelse, der er valgt for en bestemt produktionsproces. Supply Chain Management understøtter både faktiske omkostninger (first in, first out \[FIFO\]; last in, first out \[LIFO\], glidende gennemsnit, periodisk vægtet gennemsnit) og metoder for standardomkostninger. Lean manufacturing er implementeret på basis af princippet for efterkalkuleret varetræk.  

Valget af metoderne for måling af kostværdi definerer også kravene til rapportering af materiale- og ressourceforbrug i produktionsprocessen. Normalt kræver metoder for faktiske omkostninger nøjagtig rapportering på jobniveau, mens metoder for periodisk efterkalkulation tillader mindre detaljeret rapportering af materiale- og ressourceforbrug.

## <a name="mixed-mode-manufacturing"></a>Produktion i blandet tilstand
Forskellige produkter og produktionstopologier kræver anvendelse af forskellige ordretyper. Supply Chain Management kan anvende de forskellige typer i blandet tilstand. Med andre ord kan alle ordretyper forekomme i løbet af start-til-slut-processen for produktionen af en færdigvare.

-   **Produktionsordre** – Dette er den klassiske ordretype produktion af et bestemt produkt eller en produktvariant i et bestemt antal på en bestemt dato. Produktionsordrer er baseret på styklister og ruter.
-   **Batchordre** – Denne ordretype bruges til forarbejdningsindustrien og diskrete processer, hvor produktionskonverteringen er baseret på en formel, eller hvor samprodukter og biprodukter kan være slutprodukter enten ud over eller i stedet for det primære produkt. Batchordrer bruger styklister og ruter som **formel** type.
-   **Kanban** – Kanban bruges til at signalere tilbagevendende lean manufacturing-processer, der er baseret på produktionsflow, kanbanregler og styklister.
-   **Projekt** – Et produktionsprojekt kombinerer produkter og tjenester med en bestemt tidsplan og et budget. Produktionsdelen i et projekt kan leveres via en af de andre typer.

## <a name="manufacturing-principles"></a>Principper for produktion
Hvis du vil vælge det produktionsprincip, der er mest velegnet til et bestemt produkt og et relateret marked, skal du overveje kravene til produktion og logistik samt kundernes forventninger om leveringstider.

-   **Fremstilling til lager** – Dette er det klassiske produktionsprincip, hvor produkterne er produceret til lager, baseret på prognoser eller minimum for påfyldning af lager (sidstnævnte beregnes normalt på grundlag af prognose eller historisk forbrug).
-   **Fremstilling til ordre** – Standardprodukter fremstilles til bestilling eller færdigmeldes til bestilling. Selvom før-produktionen kan ske ved hjælp af princippet for fremstilling til lager, udløses der dyre trin i værdikæden eller trin, der opretter varianter, af en salgsordre eller en flytteordre.
-   **Konfigurer til bestilling** – Som for princippet Fremstilling til ordre, oprettes de endelige operationer i værdikæden til ordren. Den faktiske produktvariant, der produceres, er ikke foruddefineret, men oprettes på tidspunktet for ordreindtastning baseret på konfigurationsmodellen for det solgte produkt. Princippet Konfigurer til bestilling kræver en vis mængde af procesensretning for en bestemt produktserie.
-   **Tekniker til ordre** – Processer af typen Tekniker til ordre udføres normalt af et projekt og starter normalt med teknikerfasen. I den tekniske fase udviklet og beskrives de faktiske produkter, der er nødvendige for at opfylde ordren. Produktionsordrer, batchordrer eller kanban kan derefter oprettes for at producere produkterne.

## <a name="overview-of-the-production-life-cycle"></a>Oversigt over produktionsforløbet
De følgende trin i produktionens livscyklus kan opstå for alle typer af produktion i blandet tilstand. Dog repræsenteres ikke alle som en eksplicit ordrestatus.

1.  **Oprettet**– Du kan oprette en produktionsordre, batchordre eller kanban manuelt, eller du kan konfigurere systemet til at generere dem baseret på forskellige behovssignaler. Varedisponering opretter produktionsordrer, batchordrer eller kanbans ved autorisation af ordreforslag. Andre behovssignaler er salgsordrer eller udlignet forsyningssignaler fra andre produktionsordrer eller kanbans. For kanbans med faste mængder genereres der behovssignaler, når kanbans registreres som tomme.
2.  **Forkalkuleret**– Du kan beregne estimater for materiale- og ressourceforbrug. Forkalkulationen opretter lagerposteringer for råvarer, der har statussen **I bestilling**. Kvitteringer for de vigtigste produkter, samprodukter og biprodukter genereres, når produktionsordrer eller batchordrer estimeres. Hvis styklisten indeholder linjer af typen **Sporet forsyning**, genereres indkøbsordrer for materialer eller underleverandøroperationstjenester og udlignes til produktionsordren eller batchordren. Der reserveres varer eller ordrer efter reservationsstrategien for produktionsordren, og prisen på de færdige varer beregnes baseret på parameterindstillingerne.
3.  **Planlagt** – Du kan planlægge produktion ud fra operationer, individuelle job eller begge dele.
    -   **Grovplanlægning** – Denne planlægningsmetode giver en grov, langsigtet plan. Når du bruger denne metode, kan du angive start- og slutdatoer for produktionsordrer. Hvis produktionsordrerne er knyttet til ruteoperationer, kan du knytte dem til bærergrupper.
    -   **Finplanlægning** – Denne planlægningsmetode giver en detaljeret plan. Hver operation opdeles i individuelle job med specifikke datoer, tider og tilknyttede operationsressourcer. Hvis der bruges kapacitetsbegrænsning, bliver job knyttet til operationsressourcer ud fra tilgængelighed. Du kan få vist planen og ændre den i en Gantt-plan.
    -   **Kanban-plan** – Kanban-job er planlagt på kanban-planlægningsområde, eller de planlægges automatisk baseret på konfiguration af automatisk planlægning af kanban-regler.

4.  **Frigivet** – Du kan frigive produktionsordren eller batchordren, når planen er færdig og materialet er tilgængelig og kan plukkes eller forarbejdes. Kontrol af materialets tilgængelighed kan hjælpe den tilsynsførende med at vurdere, om materialet er tilgængeligt til produktionsordrer eller batchordrer. Du kan også udskrive produktionsordredokumenterne som pluklisten, jobkort, rutekort og rutejob. Når produktionsordren frigives, ændres ordrens status, så den angiver, at produktionen kan begynde. Når der lokationsstyring for lager, betyder frigivelse af produktionsordre eller batchordre, at produktionsstyklistelinjerne frigives til lokationsstyring for lager. Lagerstedsbølger og lagerstedsarbejde oprettes derefter ud fra konfigurationen af lageret.
5.  **Forberedt**/**plukket** – Når alle materialer og ressourcer er midlertidigt placeret på produktionslokationen, opdateres produktionsstyklistelinjerne eller kanban-linjerne til statussen **Plukket**. Sporede forsyningsordrer og relateret lagerstedsarbejde udføres normalt i denne fase. Kanban-kort eller jobkort, der skal bruges til at rapportere produktionsfremskridt, bør tildeles og udskrives.
6.  **Startet** – Når en produktionsordre, batchordre eller kanban er startet, kan du rapportere materiale- og ressourceforbrug mod ordren. Systemet kan konfigureres til automatisk at bogføre det materiale- og ressourceforbrug, der tildeles ordren ved start. Denne tildeling kaldes også forhåndstræk, fremadrettet rydning eller automatisk forbrug. Du kan manuelt fordele materialer til produktionsordrer eller batchordrer ved at oprette yderligere pluklistekladder. Du kan også manuelt tildele arbejdskraft og andre ruteomkostninger til ordren. Hvis du bruger grovplanlægning, kan du tildele disse omkostninger ved at oprette en rutekortkladde. Hvis du bruger finplanlægning, kan du tildele disse omkostninger ved at oprette en jobkortkladde. Produktionsordrer eller batchordrer kan startes i batches af den ønskede endelige størrelse. Inden for en produktionsordre, batchordre eller kanban kan job, der er oprettet, startes og rapporteres separat via kladder, til MES Terminal (Manufacturing Execution Terminal) eller kanban-områderne.
7.  Rapport i gang/**fuldførte** job – Brug MES Terminal, produktionskladder, kanban-områder eller mobile scanningsfunktioner til at rapporter produktionsfremskridt for job eller ressource. Materiale- og ressourceforbrug bogføres, og status for de relaterede kanbans, produktionsordrer og batchordrer kan opdateres til **Modtaget** eller **Færdigmeldt**. Læg-på-lager-arbejde for lagerstedet kan oprettes, afhængigt af konfiguration af lageret.
8.  **Færdigmeldt** (produktkvitteringen) – Når en produktionsordre eller batchordre meldes færdig, opdateres mængden af færdigvarer, der er fuldført på lageret. Dette antal omfatter antallet af relevante samprodukter og biprodukter. Hvis du bruger IGVA-regnskabsførelse (igangværende arbejde), oprettes en finanskladde til at reducere IGVA-kontiene og øge lageret af færdige varer. Når omkostningen for en produktionsordre beregnes, bogføres de faktiske produktionsomkostninger. Hvis de materiale- og lønomkostninger, der er forbundet med produktionen, ikke allerede er fordelt i en kladde eller via forhåndstræk, kan de fordeles automatisk vha. et baglænstræk. Fordeling gennem baglæns træk indebærer, at lagertransaktionsprocesser fratrækkes efterfølgende. Hvis produktionsordren er færdig, skal du markere afkrydsningsfeltet **Slutkørsel** for at ændre den tilbageværende status til **Afsluttet**. Hvis ikke, skal dette felt stå tomt, så der kan rapporteres ekstra producerede antal.
9.  **Kvalitetsvurdering** – En produktkvittering kan udløse oprettelse af kvalitetsordrer, afhængigt af konfigurationen af testprocesser og kvalitetsregler, der er fastsat for bestemte produkter. Da en kvalitetsordre kan opdatere lagerstatus eller batchattributterne for de testede produkter, er kvalitetsvurdering en obligatorisk proces i mange brancher.
10. **Lægge på lager** og **Levér til ordre** – Efter produktkvitteringen og kvalitetsvurdering kan valgfri læg-på-lager-arbejde dirigere modtagne produkter til det næste forbrugspunkt, til et lager med færdigvarer eller til en forsendelseszone, hvis der er krav om levering til ordre.
11. **Afsluttet** – Inden produktionen afsluttes, beregnes der faktiske omkostninger for det antal, der er produceret. Alle estimerede omkostninger til materialer, løn og indirekte omkostninger tilbageføres og erstattes med faktiske omkostninger. Hvis du markerer afkrydsningsfeltet **Slutkørsel**, når du udfører omkostningsberegningen, ændres produktionsordrens status til **Afsluttet**. Denne status forhindrer, at ekstra omkostninger bogføres på en færdigmeldt produktionsordre.
12. **Periodens afslutning** – Nogle principper for omkostningsregnskaber, f.eks. periodiske gennemsnit, efterkalkulation ved baglæns træk, FIFO eller LIFO, kræver periodiske aktiviteter for at lukke lageret eller regnskabsperioden. Systemet forsøger normalt at rapportere alt materiale og ressourceforbrug samt korrektioner af lager og spild, før perioderne lukkes. Denne rapportering sker typisk ved hjælp af lagerbevægelseskladder eller reguleringskladder. Målet er at vurdere den økonomiske præstation pr. driftsenhed pr. periode. I nogle tilfælde, når der bruges langvarige produktionsordrer, der spænder over finansielle rapporteringsperioder, bruges produktionskladder bruges til at rapportere produktionens fremskridt og ressourceforbrug i slutningen af perioden.


## <a name="additional-resources"></a>Yderligere ressourcer

[Produktionstilbagemelding](production-feedback.md)

[Oversigt over produktkonfigurationsmodeller](../pim/product-configuration-models.md)

[Oversigt over lean manufacturing](lean-manufacturing-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]