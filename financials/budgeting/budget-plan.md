---
title: "Budgetplanlægning"
description: "Formålet med denne øvelse er at give en automatiseret visning af Microsoft Dynamics 365 for operationer funktionalitet opdateringer i området i budgetplanlægningen. Hensigten med denne øvelse er at illustrere en hurtig konfiguration af et eksempel med budgetplanlægningsmodulet, og hvordan budgetplanlægning kan opnås med denne konfiguration.  Denne øvelse vil fokusere specielt på følgende forretningsprocesser eller opgaver – oprettelse af organisationshierarkiet for budget planlægning og konfiguration af brugersikkerhed - definition af budgetplanscenarier, budget plan kolonner, layout og Excel-skabeloner - oprettelse og aktivering af proces - oprettelse af Budgetplansdokumentet ved at trække i faktiske oplysninger fra Finans - bruger fordelinger til at justere budget plan dokumentdata - redigering budget plan dokument budgetplanlægningsdata i Excel"
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 81b44aa7af3a05ebc28963f406fab98bfbbb340d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning"></a>Budgetplanlægning

Formålet med denne øvelse er at give en automatiseret visning af Microsoft Dynamics 365 for operationer funktionalitet opdateringer i området i budgetplanlægningen. Hensigten med denne øvelse er at illustrere en hurtig konfiguration af et eksempel med budgetplanlægningsmodulet, og hvordan budgetplanlægning kan opnås med denne konfiguration.  Denne øvelse vil fokusere specielt på følgende forretningsprocesser eller opgaver – oprettelse af organisationshierarkiet for budget planlægning og konfiguration af brugersikkerhed - definition af budgetplanscenarier, budget plan kolonner, layout og Excel-skabeloner - oprettelse og aktivering af proces - oprettelse af Budgetplansdokumentet ved at trække i faktiske oplysninger fra Finans - bruger fordelinger til at justere budget plan dokumentdata - redigering budget plan dokument budgetplanlægningsdata i Excel 

<a name="prerequisites"></a>Forudsætninger 
------------------

I dette selvstudium skal du få adgang til Dynamics-365 for handlingsmiljø med demodata for Contoso og klargøres som administrator på forekomsten. Brug ikke i privat browser-tilstand for denne øvelse - log ud fra en anden konto i browseren, hvis det er nødvendigt, og log på med Dynamics 365 operationer administratorlegitimationsoplysninger. Når du logger ind Dynamics 365 for operationer, du **skal** Marker afkrydsningsfeltet "Hold mig logget ind". Derved oprettes en vedvarende cookie, som Excel-appen aktuelt skal bruge. Hvis du logger på den Dynamics 365 for operationer ved hjælp af en anden webbrowser end Internet Explorer, blive derefter du bedt om at logge ind i Excel-App. Når du klikker på "Log på" i Excel-appen, åbnes et pop op-vindue i Internet Explorer, og når du logger på, **SKAL** du markere afkrydsningsfeltet "Forbliv logget på". Hvis der ikke ser ud til at ske noget, når du klikker på "Log på" i Excel-appen, skal du rydde cachen med IE-cookies.

## <a name="scenario-overview"></a>**Scenario overview**
Lene arbejder som økonomichef i Contoso Entertainment Systems i Tyskland (DEMF). Når FY2016 nærmer sig, skal hun arbejde på at konfigurere virksomhedens budget for det kommende år. Forberedelse af budgettet ser ud som følger:

1.  Lene bruger faktiske beløb fra forrige år som udgangspunkt til at oprette budgettet.
2.  Baseret på de foregående år faktiske oplysninger, opretter hun estimater for 12 måneder i det kommende år
3.  Lene gennemgår budgettet med regnskabsdirektøren. Når det er gjort, foretager hun de nødvendige tilpasninger af budgetplanen og færdiggør budgetforberedelsen.

Konfiguration af skema for scenariet i budgetplanlægningen ser ud som følger:

![Screenshot1](./media/screenshot1-300x152.png)

Julia bruger følgende Excel-skabelon til at udarbejde budgettet:

[![](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>Øvelse 1: Konfiguration
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**Opgave 1: Oprette organisationshierarki**
Ad hele budgetteringsprocessen sker i økonomiafdelingen, skal Lene oprette et meget simpelt organisationshierarki – kun bestående af økonomiafdelingen. 1.1. Naviger til organisationshierarkier (virksomhedsadministration &gt;organisationer &gt;organisationshierarkier), og klik på knappen Nyt / ny

![Screenshot3](./media/screenshot3.png) 

1.2. Skriv et navn til organisationshierarkiet, og klik på knappen Tildel formål

[![Screenshot4](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Vælg formål for budgetplanlægning, skal du klikke på knappen Tilføj og tildele nyoprettede organisationshierarki: 

[![Screenshot5](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Gentag trinnene ovenfor af hensyn til organisationens sikkerhed. Luk formen, når det er gjort.

[![Screenshot6](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Klik på knappen Vis i formen Organisationshierarkier. Klik på Rediger i Hierarkidesigner, og opret et hierarki ved at klikke på knappen Indsæt.

[![Screenshot7](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Vælg Økonomiafdeling for budgetteringshierarkiet. 

[![Screenshot8](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Når du er færdig, skal du klikke på knappen Publicer og Luk. Vælg 1-1/2015 som ikrafttrædelsesdato for publicering af hierarkiet.

[![Screenshot9](./media/screenshot9.png)](./media/screenshot9.png)

## <a name="task-2-configure-user-security"></a>Opgave 2: Konfigurer brugersikkerhed
Budgetplanlægning bruger særlige sikkerhedspolitikker til at konfigurere adgang til budgetplandata. Lene skal give sig selv adgang til økonomiske budgetplaner. 2.1. Skift til DEMF juridiske enhed kontekst: [![Screenshot10](./media/screenshot10.png)](./media/screenshot10.png) 2.2. Naviger til budgettering &gt;Setup &gt;budgetplanlægning &gt;konfiguration af budgetplanlægning. Indstiller værdien sikkerhed model til baseret på sikringsorganer parametre under fanen [![Screenshot11](./media/screenshot11.png)](./media/screenshot11.png) 2.3. Gå til systemadministration &gt;brugere &gt;brugere. Give brugeradministrator (Lene Jeppesen) rollen som budgetchef. [![Screenshot12](./media/screenshot12.png)](./media/screenshot12.png) 2.4. Pluk brugerrolle, og klik på Tildel organisationer [![Screenshot13](./media/screenshot13.png)](./media/screenshot13.png)2.5. Vælg "Giv adgang til bestemte organisationer enkeltvist". Vælg organisationshierarkiet, der er oprettet i første trin. Vælg noden Økonomi og på tilskud med børn knap ***vigtigt!*** *– Kontroller, at du i DEMF juridiske enhed kontekst ved udførelse af denne opgave, som organisatorisk sikkerhed anvendes pr. juridisk enhed*[![Screenshot14](./media/screenshot14.png)](./media/screenshot14.png)

## <a name="task-3-create-scenarios"></a>Opgave 3: Opret scenarier
3.1. Naviger til budgettering&gt;Setup &gt;budgetplanlægning &gt;konfiguration af budgetplanlægning. Bemærk på siden Scenarier de scenarier, som vi skal bruge videre frem i denne øvelse: Forrige års faktiske og budgetterede. *Bemærk! Du kan oprette nye scenarier for denne opgave, hvis du ønsker det, og bruge dem i stedet.* [![Screenshot15](./media/screenshot15.png)](./media/screenshot15.png)*Note: som Lene bruger ikke formelle godkendelsesprocessen for udarbejdelsen af budgettet, vi springer over arbejdsprocesser, stadier og faser i arbejdsprocessen Opsætning i denne øvelse og vil bruge en eksisterende installation til automatisk – Godkend arbejdsgang. Se tillæg til konfiguration af arbejdsgang.*

## <a name="task-4-create-budget-plan-columns"></a>Opgave 4: Opret budgetplankolonner
Budgetplankolonner er enten monetære eller antalsbaserede kolonner, der kan bruges i dokumentlayoutet til en budgetplan. I vores eksempel skal vi oprette en kolonne til forrige år faktiske oplysninger og 12 kolonner, der repræsenterer hver måned i et budgetteret år. Kolonner kan oprettes ved enten blot at klikke på knappen Tilføj og indsætte værdierne eller med hjælp af en dataenhed. I denne øvelse vil vi benytte dataenhed til at udfylde værdierne. 4.1. I Budgettering&gt;Setup &gt;budgetplanlægning &gt;Budget planlægning åbne kolonner konfigurationsside. Klik på Office-knappen i øverste højre hjørne af formularen, og Vælg kolonner (ufiltreret) [![Screenshot16](./media/screenshot16.png)](./media/screenshot16.png) 4.2. Systemet åbner Excel-projektmappen, der skal bruges til at udfylde værdierne. Hvis du bliver bedt om det, skal du klikke på Aktivér redigering og har tillid til dette program [![Screenshot18](./media/screenshot18.png)](./media/screenshot18.png)[![Screenshot17](./media/screenshot17.png)](./media/screenshot17.png) 4.3. Vi skal flere kolonner til at udfylde værdierne. Klik på den højre rude for at føje kolonner til gitteret: [![Screenshot19](./media/screenshot19.png)](./media/screenshot19.png) 4.4. Klik på lille blyant-knappen ved siden af PlanColumns for at få vist tilgængelige kolonner, der skal føjes til gitteret [![Screenshot20](./media/screenshot20.png)](./media/screenshot20.png) 4.5. Dobbeltklik på hvert felt, der er tilgængelige til at føje dem til de markerede felter og klikke på Opdater [![Screenshot21](./media/screenshot21.png)](./media/screenshot21.png) 4.6. Tilføj alle de kolonner, der skal oprettes, i Excel-tabellen. Brug funktionen Autofyld i Excel til hurtigt at tilføje linjerne. Sørg for, at linjerne er tilføjet som en del af tabellen (når du bruger Lodret skriftrulle, du skal kunne se kolonneoverskrifter øverst i gitteret) [![Screenshot22](./media/screenshot22.png)](./media/screenshot22.png) 4.7. Tilbage til Dynamics 365 for operationer og opdaterer siden. Publicerede værdier vises i Dynamics 365 for operationer. [![Screenshot23](./media/screenshot23.png)](./media/screenshot23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Opgave 5: Opret dokumentlayouter og skabeloner til budgetplan
Layout definerer, hvordan budgetplanens dokumentlinjegitter skal se ud, når brugeren åbner budgetplansdokumentet. Det er også muligt at skifte layout for budgetplandokumentet for at få vist samme data med forskellige vinkler. Da Lene nu har fået defineret kolonner, der skal bruges sammen med vores budgetplansdokumentet, skal hun oprette et dokumentlayout for budgetplanen, der skal ligne Excel-tabellen, som hun bruger til at oprette budgetdata (se afsnittet Oversigt over scenarie i denne øvelse) 5.1. I Budgettering&gt;Setup &gt;budgetplanlægning &gt;Budget planlægning åben layout konfigurationssiden. Opret et nyt layout for budgetposten Månedlig:

-   Vælg MA + BU-dimensionsopsætning for at medtage hovedkonti og virksomhedsenheder i layoutet.
-   Vis alle kolonner med budgetplaner, der er oprettet i det forrige trin, i sektionen Elementer. Gør alle redigerbare undtagen Faktiske omkostninger for forrige år.
-   Klik på knappen Beskrivelser for at vælge, hvilke økonomiske dimensioner der skal vise beskrivelser i gitteret.

[![Screenshot24](./media/screenshot24.png)](./media/screenshot24.png) baseret på budgettet vil Layoutdefinitionen vi kan oprette en Excel-skabelon, der skal bruges som en alternativ måde at redigere budgetdata. Da Excel-skabelonen skal matche layoutdefinitionen af budgetplanen, kan du ikke redigere budgetplanens layout efter oprettelse af Excel-skabelonen, derfor skal denne opgave udføres, når alle layoutkomponenter er defineret. 5.2. I layout, der er oprettet i 5.1. Trin, skal du klikke på knappen skabelon &gt;Generer. Bekræft advarselsmeddelelsen. For at få vist skabelonen, skal du klikke på skabelon &gt;visning. *Bemærk: Sørg for at vælge "Gem som" og vælge det sted, hvor skabelonen skal gemmes for at redigere den. Hvis brugeren vælger "Åbn" i dialogboksen uden at gemme, bevares de ændringer, der er gjort ved filen ikke, når filen lukkes.* [![Screenshot25](./media/screenshot25.png)](./media/screenshot25.png) 5.3. &lt;Valgfrit&gt; ændre Excel-skabelon til at gøre det ser mere brugervenligt – tilføje samlede formler, overskriftsfelter, formatering osv. Gem ændringerne, og overføre filen til budget plan layout ved at klikke på Layout &gt;overføre [![Screenshot26](./media/screenshot26.png)](./media/screenshot26.png)

## <a name="task-6-create-a-budget-planning-process"></a>Opgave 6: Opret en budgetplanlægningsproces
Lene skal oprette og aktivere en ny budgetplanlægningsproces, der kombinerer hele opsætningen ovenfor for at begynde at indtaste budgetplaner. Budgetplanlægningsprocessen definerer, hvilke budgetteringsorganisationer, arbejdsgangslayout og skabeloner der skal bruges til at oprette budgetplaner. 6.1. Naviger til budgettering &gt;Setup &gt;budgetplanlægning &gt;Budget planlægningsprocessen og oprette en ny post.

-   Budgetplanlægningsproces – DEMF-budgettering FY2016
-   Budgetcyklus – FY2016
-   Finans – DEMF
-   Standardkontostruktur – Manufacturing P&L
-   Organisationshierarkiet – Vælg det hierarki, der er oprettet i begyndelsen af øvelsen
-   Budgetplanlægningsarbejdsgang – Tildel automatisk – Godkend arbejdsgang for økonomiafdeling
-   I regler og skabeloner til budgetplanlægning skal du for hvert stadie i arbejdsgangens budgetplanlægning vælge, om tilføjelse og redigering af linjer er tilladt, og hvilket layout der skal bruges som standard

*Bemærk! Du kan oprette flere dokumentlayout og tildele dem, så de er tilgængelige i budgetplanlægningen arbejdsgangsstadie ved at klikke på knappen Alternative layouts.* [![Screenshot27](./media/screenshot27.png)](./media/screenshot27.png) 6.2. Vælg handlinger &gt;Aktiver for at aktivere denne budgetplanlægningsarbejdsgangen [![Screenshot28](./media/screenshot28.png)](./media/screenshot28.png)

<a name="exercise-2-process-simulation"></a>Øvelse 2: Processimulering
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Opgave 7: Generér startdata for budgetplan fra Finans
7.1. Naviger til budgettering &gt;periodisk &gt;Generer budgetplan fra finansmodulet. Udfyld de periodiske procesparametre, og klik på knappen Generér. [![Screenshot29](./media/screenshot29.png)](./media/screenshot29.png) 7.2. Naviger til budgettering &gt;Budget har til hensigt at finde en budgetplan, der er oprettet af Generer proces. [![Screenshot30](./media/screenshot30.png)](./media/screenshot30.png) 7.3. Åbn oplysninger om dokumentet ved at klikke på dokumentnummerlinket. Budgetplanen vises som defineret i det layout, der er oprettet under denne øvelse [![Screenshot31](./media/screenshot31.png)](./media/screenshot31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Opgave 8: Opret budget for indeværende år baseret på faktiske oplysninger i forrige år
Fordelingsmetoderne kan bruges i budgetplanen til nemt at kopiere oplysninger til budgetplaner fra ét scenarie til et andet/sprede dem på tværs af perioder/allokere til andre dimensioner. Vi skal bruge fordelinger til at oprette budget for indeværende år fra forrige års faktiske oplysninger. 8.1. Vælg alle linjer i dokumentgitteret budget plan og klikke på knappen Fordel budget [![Screenshot32](./media/screenshot32.png)](./media/screenshot32.png) 8.2. Vælg fordelingsmetoden, periodenøglen, kilde og destination scenarier og klik på Alloker 

[![Screenshot33](./media/screenshot33.png)](./media/screenshot33.png)

De faktiske beløb for tidligere år vil blive kopieret til budgettet for indeværende år og fordele dem på tværs af perioder med salg kurve periodenøglen. 

[![Screenshot34](./media/screenshot34.png)](./media/screenshot34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Opgave 9: Juster budgetplansdokumentet ved hjælp af Excel, og færdiggør dokumentet
9.1. Klik på knappen regneark for at åbne dokumentindholdet i Excel

[![Screenshot35](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Når Excel-projektmappen åbnes, skal du justere tallene i budgetplansdokumentet og klikke på knappen Publicer.

[![Screenshot36](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Vend tilbage til Budgetplansdokumentet i Dynamics 365 for operationer. Klik på arbejdsproces &gt;sende til automatisk at godkende dokumentet

[![Screenshot37](./media/screenshot37.png)](./media/screenshot37.png) 

Når arbejdsprocessen er fuldført, ændres budgetplansstadie dokument til godkendt. [![Screenshot38](./media/screenshot38.png)](./media/screenshot38.png)

<a name="appendix"></a>Appendiks
========

### <a name="auto-approve-workflow-configuration"></a>Automatisk godkendelse af konfiguration af arbejdsgang.

A. Budgettering &gt;Setup &gt;budgetplanlægning &gt;arbejdsgange i budgettering, oprette en ny arbejdsproces ved hjælp af skabelonen arbejdsgange i budgetplanlægningen:

[![Screenshot39](./media/screenshot39.png)](./media/screenshot39.png)

Denne arbejdsproces indeholder kun én opgave – fase overgang budgetplanen. 

[![Screenshot40](./media/screenshot40.png)](./media/screenshot40.png) 

Gemme og aktivere arbejdsprocessen. 

B. Naviger til budgettering &gt;Setup &gt;budgetplanlægning &gt;konfiguration af budgetplanlægning. Fanen Opret 2 faser – indledende og sendt i faser 

[![Screenshot41](./media/screenshot41.png)](./media/screenshot41.png)

C. Naviger til budgettering &gt;Setup &gt;budgetplanlægning &gt;konfiguration af budgetplanlægning. I fanen arbejdsprocesstadier knytte arbejdsprocessen automatisk – Godkend oprettes i ét trin med faserne, der er oprettet og sendt 

[![Screenshot42](./media/screenshot42.png)](./media/screenshot42.png)  


