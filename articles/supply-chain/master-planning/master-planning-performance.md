---
title: Forbedre ydeevne af varedisponering
description: I dette emne forklares de forskellige indstillinger, der kan hjælpe dig med at forbedre varedisponeringen eller foretage fejlfinding af problemer.
author: t-benebo
manager: AnnBe
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 7e8c1d7ee51eb6e335554a01fd050bd80f2a070d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915218"
---
# <a name="improve-master-planning-performance"></a>Forbedre ydeevne af varedisponering

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

I dette emne forklares de forskellige indstillinger, der kan hjælpe dig med at forbedre varedisponeringen eller foretage fejlfinding af problemer. Det indeholder oplysninger om parametre og indstillinger samt om anbefalede konfigurationer og handlinger. Det indeholder endvidere en oversigt over alle de vigtige parametre, du bør overveje, når du har varedisponeringsjob, der kører i lang tid.

Dette emne henvender sig til systemadministratorer eller IT-brugere, der har mulighed for at foretage fejlfinding. Det er også beregnet til produktions- eller forsyningsplanlæggere, fordi det indeholder oplysninger om parametre, der vedrører forretningsmæssige planlægningsbehov. 

## <a name="parameters-related-to-master-planning-performance"></a>Parametre relateret til ydelsen af varedisponering

De forskellige parametre påvirker kørselstiden for varedisponeringen og skal tages i betragtning.

### <a name="number-of-threads"></a>Antal tråde

Parameteret **Antal tråde** giver dig mulighed for at justere processen til behovsplanlægning, så den kan forbedre ydelsen på det specifikke datasæt. Dette parameter angiver det samlede antal tråde, der vil blive brugt til at køre varedisponering. Den medfører parallelisering af varedisponeringskørslen, hvilket hjælper med at reducere kørselstiden. 

Du kan angive parameteren **Antal tråde** i dialogboksen **Kørsel af en varedisponering**. Hvis du vil åbne denne dialogboks, skal du gå til **Varedisponering \> Varedisponering \> Kør \> Varedisponering** eller vælge **Kør** i arbejdsområdet **Varedisponering**. Hvis du vil bestemme den bedste værdi for denne parameter, er du nødt til at bruge en proces, hvor du prøver dig frem. Du kan dog bruge følgende formler til at beregne en startværdi:

- **Hvis din branche er produktion:** (Antal tråde) = (Antal ordreforslag ÷ 1.000)
- **Ellers:** (Antal tråde) = (Antal varer ÷ 1.000)

Antallet af hjælpefunktioner, der bruges under varedisponering, skal være mindre end eller lig med det maksimale antal tråde, der er tilladt på batchserveren. Hvis antallet af hjælpefunktioner overstiger antallet af tråde på batchserveren, udfører de ekstra tråde ikke noget arbejde.

> [!NOTE]
> Indstilling af parametret **Antal tråde** til **0** (nul) øger kørselstiden for varedisponeringen. Det anbefales derfor, at du altid angiver en værdi, der er mere end 0.

### <a name="number-of-tasks-in-helper-task-bundle"></a>Antal opgaver i bundt med hjælpefunktioner

Ved at ændre indstillingen **Antal opgaver i bundt med hjælpefunktioner** (dvs. bundtets størrelse) kan du muligvis reducere kørselstiden. Denne indstilling styrer antallet af varer, der er planlagt sammen af en enkelt hjælpefunktion.

Du kan indstille parameteren **Antal opgaver i bundt** i sektionen **Performance** under fanen **Generelt** på siden **Varedisponeringsparametre** (**Varedisponering \> Konfiguration \> Varedisponeringsparametre**). Den bedste værdi for denne parameter afhænger af dine data. Det anbefales derfor, at du starter med værdien **1**og derefter forsøger dig frem for at bestemme den bedste værdi for din konfiguration.

Det anbefales generelt, at du øger antallet af opgaver, når antallet af elementer er meget stort (i hundredtusindvis). Ellers skal du reducere antallet af opgaver. For følgende specifikke industrier anbefales disse punkter:

- I detail- og distributionsbrancherne, hvor der er mange uafhængige varer, kan du bruge mange hjælpefunktioner, fordi der ikke er nogen afhængighed mellem varerne. 
- I produktionsbranchen, hvor der findes mange styklister og delte underkomponenter, skal du bruge færre hjælpefunktioner, da afhængighederne mellem varerne kan forårsage ventetider.

> [!TIP]
> Hvis du har problemer med ydeevne, anbefales det, at du reducerer indstillingen **Antal opgaver i bundt med hjælpefunktioner** til **1**. Du kan derefter starte processen med at prøve dig frem for at finde den bedste værdi til din konfiguration. Generelt opstår problemer med ydelsen, når en vare tager længere tid at behandle end de resterende varer. I dette tilfælde kan du se, at to efterfølgende opgaver, der har status som **Disponering** i varedisponeringskørslen, har en kørselstid, der er væsentligt forskellig. I ekstreme tilfælde kan forskellen være op til 30 minutter. Du kan aflede, hvor lang tid opgaverne skal udføres, ved at se på varigheden af hver opgave.

### <a name="use-of-cache"></a>Brug af cache

Parameteren **Brug af cache** giver dig mulighed for at justere processen til behovsplanlægning, så den kan udføres bedre på det specifikke datasæt. Du kan f eks. justere den for at opnå følgende resultater:

- Hvis der foretages cachelagring, indsamles der flere data i datalageret. Det forventes, at dataene vil blive brugt igen senere. Hvis dataene er i hukommelsen, kan du gemme nogle databaseanmodninger. Hvis der ikke er flere cachelagringer, øges hukommelseskravene dog.
- Hvis der foretages mindre cachelagring, skal de samme data muligvis hentes fra databasen hyppigere. Derudover gemmer AOS (Application Object Server) kun lidt data i hukommelsen i hele processen.

Det er vanskeligt at forudsige, hvilken indstilling der er bedst, fordi hvert enkelt tilfælde afhænger ikke blot af dataene, men også af hardwaren. Da mindre cachelagring f.eks. medfører yderligere belastning på databaseserveren, er det sandsynligvis ikke en god ide at bruge denne indstilling, hvis databaseserveren allerede er overbelastet.

Du kan indstille parameteren **Brug af cache** i sektionen **Performance** under fanen **Generelt** på siden **Varedisponeringsparametre** (**Varedisponering \> Konfiguration \> Varedisponeringsparametre**). Effektiviteten af cachelagring afhænger meget af kundens data. Hvis der aldrig er brug for cachelagrede data, spilder du blot hukommelse, hvis du gemmer data, indtil planlægningsprocessen er afsluttet. Hvis du i dette tilfælde konfigurerer mindre cachelagring, kan det medføre, at ydeevnen øges, fordi AOS kræver mindre hukommelse, og færre serverressourcer frigøres til andre opgaver.

> [!TIP]
> Generelt anbefales det, at du angiver parameteren **Brug af cache** til **Maksimum**, da parameteren er beregnet som en funktion til forbedring af performance. Det anbefales, at du angiver parameteren til **Minimum**, hvis du kører lokalt og har begrænset hukommelse (ca. 2 \[GB\]).

### <a name="number-of-orders-in-firming-bundle"></a>Antal ordrer i autorisationsbundt

Parameteren **Antal ordrer i autorisationsbundt** angiver det samlede antal ordrer, der skal behandles ad gangen af hver tråd/batch. Den medfører parallelisering af processen til automatisk autorisation.

Du kan indstille parameteren **Antal ordrer i autorisationsbundt** i sektionen **Performance** under fanen **Generelt** på siden **Varedisponeringsparametre** (**Varedisponering \> Konfiguration \> Varedisponeringsparametre**). Paralliseringen af processen til automatisk autorisation er baseret på de ordrer, der skal behandles sammen. Hvis dette parameter eksempelvis er angivet til **50**, vil hver tråd eller batchopgave f.eks. hente 50 ordrer ad gangen og behandle dem sammen. Det anbefales, at du bruger en proces, hvor du prøver dig frem, for at finde den bedste værdi. Du kan dog bruge følgende formel til at beregne en startværdi:

(Antal ordrer pr. bundt) = (Antal efterspørgselsvarer ÷ antal tråde)

> [!NOTE]
> Hvis du angiver parameteren **Antal ordrer i autorisationsbundt** til **0** (nul), sker der ingen parallisering af processen til automatisk autorisation. Hele processen vil blive kørt på en enkelt batchopgave og have en akkumuleret kørselstid. Kørselstiden for varedisponeringen vil derfor stige. Derfor anbefales det, at du angiver denne parameter til en værdi, der er større end **0** (nul).

### <a name="time-fences"></a>Tidshorisonter

Tidshorisonenter angiver, hvor langt ud i fremtiden beregningerne og andre behov skal beregnes af varedisponeringen. Jo større tidshorisonten er, jo længere tager kørslen af varedisponeringen. Angiv derfor tidshorisonten i overensstemmelse med virksomhedens behov. Du kan finde flere oplysninger om tidshorisonter under [Definere varedisponering](master-planning-setup.md).

### <a name="actions"></a>Handlinger

Blandt tidshorisonterne kan du også finde parameteren for **Handlingsmeddelelse**. Beregningen af handlingsmeddelelser medfører en længere kørselstid for varedisponering. Hvis handlingsmeddelelser ikke regelmæssigt analyseres og anvendes (dagligt, ugentligt osv.), skal du overveje at deaktivere beregningen under kørslen af varedisponeringen. Hvis du vil deaktivere beregningen, skal du på siden **Behovsplaner** (**Behovsplaner \> Opsætning \> Planer \> Behovsplaner**) angive tidshorisonten for **Handlingsmeddelelse** til **0** (nul). Kontroller også, at indstillingen **Handlingsmeddelelser** er slået fra for alle disponeringsgrupper.

### <a name="futures"></a>Terminer

Beregningen af terminer medfører en længere kørselstid for varedisponering. Hvis du ikke planlægger styklister, eller hvis forsinkelserne ikke skal overføres fra forsyning til behov under planlægningen, skal du overveje at deaktivere fremtidige beregninger ved varedisponering. Hvis du vil deaktivere beregningerne, skal indstille tidshoristonen **Terminer** til **0** (nul) for den behovsplan, du kører. Kontroller også, at indstillingen **Terminer** er slået fra for alle disponeringsgrupper.

## <a name="one-heavy-routine-at-a-time"></a>Én tung rutine ad gangen

Når du planlægger behovsplanlægning, må du ikke planlægge noget andet batchjob på samme tid. Sørg især for, at du ikke planlægger andre tunge rutiner, f.eks. lagerlukning, samtidigt.

## <a name="review-the-session-log"></a>Gennemse sessionsloggen

Systemet kan indsamle yderligere oplysninger om de opgaver, der køres under varedisponering. Hvis du vil have systemet til at indsamle disse oplysninger, skal du slå indstillingen **Spor behandlingstidspunkt** i dialogboksen **Kørsel af en varedisponering** til. De oplysninger, der indsamles, kan hjælpe dig med at finde flaskehalse i kørslen. Når f.eks. parameteren **Antal opgaver i bundt med hjælpefunktioner** er indstillet til **1**, kan du f.eks. identificere den vare, der har den længste kørselstid. Du kan også sammenligne kørselstiderne for de forskellige tråde, der har statussen **Disponering**, og sammenligne varigheden for hver opgave.

Hvis du vil gennemgå systemets varedisponeringskørsler, skal du følge et af disse trin.

- I arbejdsområdet **Varedisponering** skal du vælg en behovsplan på rullelisten og derefter vælge **Oversigt** på feltet **Varedisponering**. Vælg et job, vælg **Forespørgsler** i oversigtspanelet, og vælg derefter **Procesopgavens varighed**.
- På siden **Behovsplaner** skal du vælge en plan i den venstre rude og derefter vælge **Oversigt** i oversigtspanelet. Vælg et job, vælg **Forespørgsler** i oversigtspanelet, og vælg derefter **Procesopgavens varighed**.

Når du gennemgår sessionslogfilen, skal du overveje følgende:

- **Opdatering** bør ikke tage lang tid (det bør generelt tage op til 30 minutter), men den er enkelttrådet.
- **Kopiér plan** bør ikke tage lang tid (det skal tage ca. ét minut).
- **Automatisk autorisation** tager normalt ca. 30 minutter. Det kan dog tage op til flere timer, afhængigt af antallet af ordrer og kompleksiteten af varerne.
- **Automatisk autorisation** bør tage kortere tid en **Disponering**.
- **Disponering** skal tage længst tid i forhold til resten.
- **Handling** og **Fremtidig meddelelse** kan tage lang tid, afhængigt af dataene og antallet af styklister.

## <a name="filtering-of-items"></a>Filtrering af varer

Filtre, der anvendes i dialogboksen **Kørsel af en varedisponering** påvirker varigheden af varedisponeringens kørsel. Gå til **Varedisponering \> Varedisponering \> Kør \> Varedisponering**, eller vælg **Kør** i arbejdsområdet **Varedisponering**. Hvis du vil udelade varer fra kørslen, anbefales det, at du filtrerer efter varens levetidstilstand (ikke efter varenumre). Når du filtrerer efter levetidstilstanden, tager opdateringsprocessen kortere tid, end når du filtrerer efter varenumre.

## <a name="automatically-filter-by-items-with-direct-demand"></a>Filtrér automatisk efter varer med direkte efterspørgsel

Hvis du vil forbedre kørselstiden for varedisponering, kan du vælge kun at medtage varer med direkte behov. Dette filter kan kun bruges til en komplet varedisponeringskørsel, hvor der ikke er anvendt andre filtre i feltet **Poster, der skal medtaqes**. En varedisponering, der køres med filtre, ignorer indstillingen **Filtrer automatisk efter elementer med direkte behov**.

Feltet **Filtrer automatisk efter varer med direkte behov** findes på siden **Varedisponeringsparametre** og kan bruges sammen med indstillingerne for både forbehandling og efterbehandling.

### <a name="pre-processing"></a>Forbehandling
Parametret **Forbehandling: Filtrér automatisk efter elementer med direkte behov** sikrer, at forbehandlingsfasen for varedisponering kun omfatter varer, der opfylder mindst én af følgende betingelser:
  - Varen har en forventet tilgang eller afgang, såsom en indkøbsordre, en salgsordre, et tilbud, en overførselsordre eller en produktionsordre. 
  - Varen har varedækning med sikkerhedslager (et disponibelt minimumslager).
  - Prognosebehov efter i dag findes for varen.
  - Prognoseforsyning efter i dag findes for varen.
  - Varen indeholder alle kontinuitetslinjer fra det call center-modul, der endnu ikke er oprettet.

> [!NOTE]
> En vare, der har et fysisk tilgængeligt disponibelt lager, vil ikke vise en behovspostering, fordi der ikke er behov for varen.

### <a name="post-processing"></a>Efterbehandling
Indstillingen **Efterbehandling: Filtrér automatisk efter varer med direkte behov** er kun relevant, hvis du angiver **krav til styklisteversion** i dine disponeringsgrupper. Ellers behøver du ikke at aktivere parameteret. 

Før dækningstrinnet starter, er der et trin forud herfor, hvor varer, hvor dækningsindstillingen **Styklisteversionskrav** er aktiveret, vil blive behandlet igen. Dette gøres for at sikre, at varer fra den påkrævede styklisteversion er planlagt. Varer, der anses for at have behov under forbehandling, har ikke længere nogen behov og bør derfor udelukkes fra planlægningskørslen.

## <a name="performance-checklist-summary"></a>Oversigt over performancetjekliste

- **Antal tråde** – angiv en værdi, der er større end **0** (nul).
- **Antal opgaver i bundt med hjælpefunktioner** – angiv til en værdi, der er større end **0** (nul). (Brug de formler, der er angivet tidligere i dette emne).
- **Brug af cache** – Angiv som **maksimum**, medmindre systemet mangler hukommelse.
- **Antal ordrer i autorisationsbundt** – angiv til en værdi, der er større end **0** (nul). (Brug den formel, der er angivet tidligere i dette emne).
- **Tidshorisonter** – juster efter dine forretningsbehov.
- **Handlinger og terminer** – deaktiver aktioner og terminer, hvis du ikke bruger dem.
- **Én tung rutine ad gangen** – kør ikke varedisponering sammen med andre tunge rutiner.
- **Gennemse sessionsloggen.**
- **Filtrering af varer** – brug levetidstilstanden til at udelade varer fra varedisponeringskørslen. (Brug ikke varenumrene).
