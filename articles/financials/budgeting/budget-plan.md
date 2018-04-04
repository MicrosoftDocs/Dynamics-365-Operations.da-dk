---
title: "Budgetplanlægning"
description: "Formålet med denne øvelse er at give en automatiseret visning af Microsoft Dynamics 365 for Finance and Operations-funktionalitetsopdateringer i området for budgetplanlægning. Hensigten med denne øvelse er at illustrere en hurtig konfiguration af et eksempel med budgetplanlægningsmodulet, og hvordan budgetplanlægning kan opnås med denne konfiguration.  Denne øvelse vil fokusere specielt på følgende forretningsprocesser eller opgaver: -    - Oprettelse af organisationshierarkiet for budgetplanlægning og konfiguration af brugersikkerhed   - Definition af budgetplanscenarier, budgetplankolonner, layout og Excel-skabeloner   - Oprettelse og aktivering af budgetplanlægningsproces   - Oprettelse af budgetplansdokumentet ved at trække i faktiske oplysninger fra Finans    - Brug af allokeringer for at justere data i budgetplansdokument   - Redigering af budgetplansdokumentets dat i Excel"
author: twheeloc
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 59781da7681ece1c0c013f59e0d1a5d7efc51c3a
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="budget-planning"></a>Budgetplanlægning

[!include[banner](../includes/banner.md)]


Formålet med denne øvelse er at give en automatiseret visning af Microsoft Dynamics 365 for Finance and Operations-funktionalitetsopdateringer i området for budgetplanlægning. Hensigten med denne øvelse er at illustrere en hurtig konfiguration af et eksempel med budgetplanlægningsmodulet, og hvordan budgetplanlægning kan opnås med denne konfiguration.  Denne øvelse vil fokusere specielt på følgende forretningsprocesser eller opgaver: -    - Oprettelse af organisationshierarkiet for budgetplanlægning og konfiguration af brugersikkerhed   - Definition af budgetplanscenarier, budgetplankolonner, layout og Excel-skabeloner   - Oprettelse og aktivering af budgetplanlægningsproces   - Oprettelse af budgetplansdokumentet ved at trække i faktiske oplysninger fra Finans    - Brug af allokeringer for at justere data i budgetplansdokument   - Redigering af budgetplansdokumentets dat i Excel 

<a name="prerequisites"></a>Forudsætninger 
------------------

I dette selvstudium skal du have adgang til Finance and Operations-miljøet med demodata til Contoso og være klargjort som administrator på forekomsten. Brug ikke privat browsertilstand til denne øvelse – log ud fra en anden konto i browseren, hvis det er nødvendigt, og log på med legitimationsoplysninger for administrator til Finance and Operations. Når du logger på Finance and Operations, **SKAL** du markere afkrydsningsfeltet "Forbliv logget på". Derved oprettes en vedvarende cookie, som Excel-appen aktuelt skal bruge. Hvis du logger på Finance and Operations ved hjælp af en anden webbrowser end Internet Explorer, bliver du derefter bedt om at logge på i Excel-appen. Når du klikker på "Log på" i Excel-appen, åbnes et pop op-vindue i Internet Explorer, og når du logger på, **SKAL** du markere afkrydsningsfeltet "Forbliv logget på". Hvis der ikke ser ud til at ske noget, når du klikker på "Log på" i Excel-appen, skal du rydde cachen med IE-cookies.

## <a name="scenario-overview"></a>**Oversigt over scenarie**
Lene arbejder som økonomichef i Contoso Entertainment Systems i Tyskland (DEMF). Når FY2016 nærmer sig, skal hun arbejde på at konfigurere virksomhedens budget for det kommende år. Forberedelse af budgettet ser ud som følger:

1.  Lene bruger faktiske beløb fra forrige år som udgangspunkt til at oprette budgettet.
2.  Baseret på de foregående år faktiske oplysninger, opretter hun estimater for 12 måneder i det kommende år
3.  Lene gennemgår budgettet med regnskabsdirektøren. Når det er gjort, foretager hun de nødvendige tilpasninger af budgetplanen og færdiggør budgetforberedelsen.

Konfigurationsskema til budgetplanlægning for scenariet ser ud som følger:

![Konfigurationsskema til budgetplanlægning](./media/screenshot1-300x152.png)

Julia bruger følgende Excel-skabelon til at udarbejde budgettet:

[![Excel-skabelon](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

## <a name="exercise-1-configuration"></a>Øvelse 1: Konfiguration

### <a name="task-1-create-organizational-hierarchy"></a>**Opgave 1: Opret et organisationshierarki**
Ad hele budgetteringsprocessen sker i økonomiafdelingen, skal Lene oprette et meget simpelt organisationshierarki – kun bestående af økonomiafdelingen. 1.1. Naviger til organisationshierarkier (Organisationsadministration &gt; Organisationer &gt; Organisationshierarkier), og klik på knappen Ny

![Organisationshierarki](./media/screenshot3.png) 

1.2. Skriv navnet for organisationshierarkiet, og klik på knappen Tildel formål

[![Navn](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Vælg formålet for budgetplanlægning, klik på knappen Tilføj, og tildel nyoprettet organisationshierarki: 

[![Tildel formål](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Gentag trinnene ovenfor af hensyn til organisationens sikkerhed. Luk formen, når det er gjort.

[![Sikkerhedsorganisation](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Klik på knappen Vis i formen Organisationshierarkier. Klik på Rediger i Hierarkidesigner, og opret et hierarki ved at klikke på knappen Indsæt.

[![Indsæt](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Vælg Økonomiafdeling for budgetteringshierarkiet. 

[![Finans](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Når du er færdig, skal du klikke på knappen Publicer og Luk. Vælg 1-1/2015 som ikrafttrædelsesdato for publicering af hierarkiet.

[![Gælder fra](./media/screenshot9.png)](./media/screenshot9.png)

### <a name="task-2-configure-user-security"></a>Opgave 2: Konfigurer brugersikkerhed
Budgetplanlægning bruger særlige sikkerhedspolitikker til at konfigurere adgang til budgetplandata. Lene skal give sig selv adgang til økonomiske budgetplaner. 

2.1. Skift til DEMF juridisk enhedskontekst. 


2.2. Naviger til Budgettering &gt; Opsætning &gt; Budgetplanlægning &gt; Budgetplanlægningskonfiguration. Indstiller værdien for sikkerhedsmodel til Baseret på sikkerhedsorganisationer under fanen Parametre 

[![Parametre](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. Naviger til Systemadministration &gt; Brugere &gt; Brugere. Give brugeradministrator (Lene Jeppesen) rollen som budgetchef. 

[![Budgetchef](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. Vælg brugerrolle, og klik på Tildel organisationer 

[![Tildel organisationer](./media/screenshot13.png)](./media/screenshot13.png)

2.5. Vælg "Giv adgang til bestemte organisationer enkeltvist". Vælg organisationshierarkiet, der er oprettet i første trin. Vælg noden Økonomi, og på knappen Tildel med underordnede 

***Vigtigt!*** *Kontroller, at du befinder dig i DEMF's juridiske enhedskontekst under udførelse af denne opgave, da organisatorisk sikkerhed anvendes pr. juridisk enhed* 

[![Giv adgang](./media/screenshot14.png)](./media/screenshot14.png)

### <a name="task-3-create-scenarios"></a>Opgave 3: Opret scenarier
3.1. Naviger til Budgettering &gt; Opsætning &gt; Budgetplanlægning &gt; Budgetplanlægningskonfiguration. Bemærk på siden Scenarier de scenarier, som vi skal bruge videre frem i denne øvelse: Forrige års faktiske og budgetterede. 

*Bemærk! Du kan oprette nye scenarier for denne opgave, hvis du ønsker det, og bruge dem i stedet.* 

[![Nye scenarier](./media/screenshot15.png)](./media/screenshot15.png) 

*Da Lene ikke bruger formel godkendelsesproces til udarbejdelsen af budgettet, springer vi opsætning af arbejdsgange, stadier og stadier i arbejdsgange over i denne øvelse og vil bruge en eksisterende konfiguration til automatisk – Godkend arbejdsgang. Se tillæg til konfiguration af denne arbejdsgang.*

### <a name="task-4-create-budget-plan-columns"></a>Opgave 4: Opret budgetplankolonner
Budgetplankolonner er enten monetære eller antalsbaserede kolonner, der kan bruges i dokumentlayoutet til en budgetplan. I vores eksempel skal vi oprette en kolonne til forrige år faktiske oplysninger og 12 kolonner, der repræsenterer hver måned i et budgetteret år. Kolonner kan oprettes ved enten blot at klikke på knappen Tilføj og indsætte værdierne eller med hjælp af en dataenhed. I denne øvelse vil vi benytte dataenhed til at udfylde værdierne. 

4.1. Åbn siden Kolonner i Budgettering &gt; Opsætning &gt; Budgetplanlægning &gt; Budgetplanlægningskonfiguration. Klik på Office-knappen i øverste højre hjørne af formularen, og vælg Kolonner (ufiltreret) 

[![Kolonner ufiltreret](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. Systemet åbner Excel-projektmappen, der skal bruges til at udfylde værdierne. Hvis du bliver spurgt, skal du klikke på Aktivér redigering og Hav tillid til denne app 

[![Aktivér redigering](./media/screenshot18.png)](./media/screenshot18.png) 

[![Hav tillid til denne app](./media/screenshot17.png)](./media/screenshot17.png)

4.3. Vi skal bruge flere kolonner til at angive værdierne i. Klik på Design i den højre siderude for at føje kolonner til gitteret: 

[![Design](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. Klik på lille blyantknap ved siden af PlanColumns for at få vist tilgængelige kolonner, der skal føjes til gitteret 

[![Rediger](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. Dobbeltklik på hvert tilgængeligt felt for at føje dem til de markerede felter, og klik på Opdater 

![Vedligeholdelse](./media/screenshot21.png)](./Media/screenshot21.png) 

4.6. Tilføj alle de kolonner, der skal oprettes, i Excel-tabellen. Brug funktionen Autofyld i Excel til hurtigt at tilføje linjerne. Sørg for, at linjerne er tilføjet som en del af tabellen (når du bruger lodret rulning, skal du kunne se kolonneoverskrifter øverst i gitteret) 

[![Autofyld](./media/screenshot22.png)](./media/screenshot22.png) 

4.7. Gå tilbage til Finance and Operations, og opdater siden. Publicerede værdier vises i Finance and Operations. 

[![Opdatér](./media/screenshot23.png)](./media/screenshot23.png)

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Opgave 5: Opret dokumentlayouter og skabeloner til budgetplan
Layout definerer, hvordan budgetplanens dokumentlinjegitter skal se ud, når brugeren åbner budgetplansdokumentet. Det er også muligt at skifte layout for budgetplandokumentet for at få vist samme data med forskellige vinkler. Da Lene nu har fået defineret kolonner, der skal bruges sammen med vores budgetplansdokumentet, skal hun oprette et dokumentlayout for budgetplanen, der skal ligne Excel-tabellen, som hun bruger til at oprette budgetdata (se afsnittet Oversigt over scenarie i denne øvelse) 

5.1. I Budgettering &gt; Opsætning &gt; Budgetplanlægning &gt; Budgetplanlægningskonfiguration skal du åbne siden Layouts. Opret et nyt layout for budgetposten Månedlig:

-   Vælg MA + BU-dimensionsopsætning for at medtage hovedkonti og virksomhedsenheder i layoutet.
-   Vis alle kolonner med budgetplaner, der er oprettet i det forrige trin, i sektionen Elementer. Gør alle redigerbare undtagen Faktiske omkostninger for forrige år.
-   Klik på knappen Beskrivelser for at vælge, hvilke økonomiske dimensioner der skal vise beskrivelser i gitteret.

[![Beskrivelser](./media/screenshot24.png)](./media/screenshot24.png) 

Baseret på definitionen af budgetplanens layout kan vi oprette en Excel-skabelon, der skal bruges som en alternativ måde at redigere budgetdata på. Da Excel-skabelonen skal matche layoutdefinitionen af budgetplanen, kan du ikke redigere budgetplanens layout efter oprettelse af Excel-skabelonen, derfor skal denne opgave udføres, når alle layoutkomponenter er defineret. 

5.2. For det layout, der blev oprettet i trin 5.1., skal du klikke på knappen Skabelon &gt; Generer. Bekræft advarselsmeddelelsen. Hvis du vil have vist skabelonen, skal du klikke på Skabelon &gt; Vis. 

*Bemærk! Sørg for at vælge "Gem som" og vælge det sted, hvor skabelonen skal gemmes for at redigere den. Hvis brugeren vælger "Åbn" i dialogboksen uden at gemme, bevares de ændringer, der er udført på filen, ikke, når filen lukkes.* 
[![Skabelonvisning](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt; Valgfrit trin&gt; Rediger Excel-skabelonen for at gøre den mere brugervenlig – tilføj samlede formler, overskriftsfelter, formatering osv. Gem ændringerne, og overfør filen til budgetplanslayoutet ved at klikke på Layout &gt; Overfør [![Overfør](./media/screenshot26.png)](./media/screenshot26.png)

### <a name="task-6-create-a-budget-planning-process"></a>Opgave 6: Opret en budgetplanlægningsproces
Lene skal oprette og aktivere en ny budgetplanlægningsproces, der kombinerer hele opsætningen ovenfor for at begynde at indtaste budgetplaner. Budgetplanlægningsprocessen definerer, hvilke budgetteringsorganisationer, arbejdsgangslayout og skabeloner der skal bruges til at oprette budgetplaner. 

6.1. Naviger til Budgettering &gt; Opsætning &gt; Budgetplanlægning &gt; Budgetplanlægningsproces, og opret en ny post.

-   Budgetplanlægningsproces – DEMF-budgettering FY2016
-   Budgetcyklus – FY2016
-   Finans – DEMF
-   Standardkontostruktur – Manufacturing P&L
-   Organisationshierarkiet – Vælg det hierarki, der er oprettet i begyndelsen af øvelsen
-   Budgetplanlægningsarbejdsgang – Tildel automatisk – Godkend arbejdsgang for økonomiafdeling
-   I regler og skabeloner til budgetplanlægning skal du for hvert stadie i arbejdsgangens budgetplanlægning vælge, om tilføjelse og redigering af linjer er tilladt, og hvilket layout der skal bruges som standard

*Bemærk! Du kan oprette flere dokumentlayout og tildele dem, så de er tilgængelige i budgetplanlægningen arbejdsgangsstadie ved at klikke på knappen Alternative layouts.* 

[![Alternative layouts](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. Vælg Handlinger &gt; Aktiver for at aktivere denne budgetplanlægningsarbejdsgang 

[![Aktivér](./media/screenshot28.png)](./media/screenshot28.png)

## <a name="exercise-2-process-simulation"></a>Øvelse 2: Processimulering

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Opgave 7: Generér startdata for budgetplan fra Finans
7.1. Naviger til Budgettering &gt; Periodisk &gt; Opret budgetplan fra finansmodulet. Udfyld de periodiske procesparametre, og klik på knappen Generér. 

[![Generer](./media/screenshot29.png)](./media/screenshot29.png) 

7.2. Naviger til budgettering &gt; Budgetplaner til at finde en budgetplan, der er oprettet af processen Generér. 

[![Budgetplan](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. Åbn oplysninger om dokumentet ved at klikke på dokumentnummerlinket. Budgetplanen vises som defineret i det layout, der er oprettet under denne øvelse 

[![Budgetplansvisning](./media/screenshot31.png)](./media/screenshot31.png)

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Opgave 8: Opret budget for indeværende år baseret på faktiske oplysninger i forrige år
Fordelingsmetoderne kan bruges i budgetplanen til nemt at kopiere oplysninger til budgetplaner fra ét scenarie til et andet/sprede dem på tværs af perioder/allokere til andre dimensioner. Vi skal bruge fordelinger til at oprette budget for indeværende år fra forrige års faktiske oplysninger. 

8.1. Vælg alle linjer i budgetplanens dokumentgitter og klik på knappen Fordel budget 

[![Alle linjer](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. Vælg fordelingsmetode, periodenøgle, kilde- og destinationsscenarier, og klik på Alloker 

[![Alloker](./media/screenshot33.png)](./media/screenshot33.png)

De faktiske beløb for tidligere år vil blive kopieret til budgettet for indeværende år og fordelt på tværs af perioder med periodenøglen Salgskurve. 

[![Salgskurve](./media/screenshot34.png)](./media/screenshot34.png)

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Opgave 9: Juster budgetplansdokumentet ved hjælp af Excel, og færdiggør dokumentet
9.1. Klik på knappen Regneark for at åbne dokumentindholdet i Excel

[![Excel](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Når Excel-projektmappen åbnes, skal du justere tallene i budgetplansdokumentet og klikke på knappen Publicer.

[![Publicer](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Vend tilbage til budgetplansdokumentet i Finance and Operations. Klik på Arbejdsgang &gt; Send for automatisk at godkende dokumentet

[![Automatisk godkendt](./media/screenshot37.png)](./media/screenshot37.png) 

Når arbejdsprocessen er fuldført, ændres dokumentstadiets budgetplan til Godkendt. [![Godkendt](./media/screenshot38.png)](./media/screenshot38.png)

## <a name="appendix"></a>Appendiks

### <a name="auto-approve-workflow-configuration"></a>Automatisk godkendelse af konfiguration af arbejdsgang.

A. Budgettering &gt; Opsætning &gt; Budgetplanlægning &gt; Arbejdsgang for budgettering Opret en ny arbejdsgang ved hjælp af arbejdsgange i skabelonen Budgetplanlægning:

[![Opret en ny arbejdsgang](./media/screenshot39.png)](./media/screenshot39.png)

Denne arbejdsgang indeholder kun én opgave – Stadieovergang for budgetplan 

[![Stadieoverførsel for budgetplan](./media/screenshot40.png)](./media/screenshot40.png) 

Gem og aktiver arbejdsgangen. 

B. Naviger til Budgettering &gt; Opsætning &gt; Budgetplanlægning &gt; Budgetplanlægningskonfiguration. Opret 2 faser under fanen Stadier – Start og Sendt 

[![Start og Sendt](./media/screenshot41.png)](./media/screenshot41.png)

C. Naviger til Budgettering &gt; Opsætning &gt; Budgetplanlægning &gt; Budgetplanlægningskonfiguration. Tilknyt under fanen Arbejdsprocesstadier den arbejdsgang, der er automatisk godkendt i Trin A med stadierne Start og Sendt 

[![Budgettering og budgetplanlægning](./media/screenshot42.png)](./media/screenshot42.png)  




