---
title: Bruge analytiske rapporter i Microsoft Dynamics 365 for Talent - Attract
description: Dette emne beskriver de analytiske rapporter til indsigt i ansættelsesprocessen i Microsoft Dynamics 365 for Talent - Attract
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: f69c45e885d789d05a081064f30ccd6ce6bfec52
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742881"
---
# <a name="use-analytic-reports"></a>Bruge analyserapporter

Analytiske rapporter i Attract indeholder en out-of-the-box (OOTB)-løsning, der giver indsigt i ansættelsesprocessen. Tilgængelige funktioner omfatter:

- **Jobanalyser:** Klik på fanen **Analyser** i det job for at se målværdier for jobansøgere.
- **Analysehub:** Klik på **Analyser** i venstre navigationslinje for at se samlet metrik på tværs af job.
- **Brugerspecifik sikkerhed:** Adgang til rapporter styres af Attract-[rolle](security-attract.md) og jobdeltagerrolle.
- **Tværgående filtrering:** Klik på visuelle elementer i en rapport for at få vist andre målepunkter, der er filtreret efter udvalgte data.

>[!NOTE] 
>- Denne funktion findes på nuværende tidspunkt i [prøveversionen](access-preview-feature.md). Hvis du vil prøve den, skal du have [**Tilføjelsesprogrammet Omfattende ansættelser**](attract-comprehensive-hiring.md).
>- Alle rapporter for offentlig visning vises på engelsk.
>- Rapporter opdateres hver 3. time. Den seneste opdateringstidspunkt (i den lokale tidszone) findes øverst i rapporten. Opdateringstiderne er en tilnærmelse og varierer afhængigt af datamængde og ressourcebelastning i dit område.

## <a name="job-analytics"></a>Jobanalyser

Jobanalyse-rapporter er et øjebliksbillede af ansættelsesprocessen for et job.  Nøgleværdier omfatter:

- Aktive ansøgere efter stadie
- Ansøgningskilde
- Ansøgertype (intern eller ekstern)

## <a name="analytics-hub"></a>Analysehub

Analysehub-rapporter samler jobdata på tværs af job for at vise tendenser i ansættelsesprocessen. Attract omfatter to OOTB-rapporter: Oversigt over pipeline og Tragtanalyse.

### <a name="pipeline-summary"></a>Oversigt over pipeline

Rapporten Oversigt over pipeline samler data til åbne job. Nøgleværdier omfatter:

- Ansøgere på tværs af alle job efter stadie
- Ansøgningskilde
- Åbne job efter anciennitetsniveau

### <a name="funnel-analysis"></a>Tragtanalyse

Tragtanalyserapporten samler data for job, der er lukket som udfyldte. Nøgleværdier omfatter:

- Tidsforløb for ansættelse
- Omregningsmetrik (ved pegning)
- Hyppighed af tilbudsaccept

Bemærk! For at få det mest nøjagtige billede af, hvor lang tid en ansættelse tager, anbefales det, at du bruger [Tilbudsstyring](offer-setup.md), en funktionen, der er tilgængelig som en del af tilføjelsesprogrammet Omfattende ansættelser.

>[!TIP] 
>Prøv at pege på visuelle elementer for at få flere oplysninger. Hvis du f.eks. peger på **Aktive ansøgere**, viser visuelle elementer de gennemsnitlige dage i fasen. Analyse af disse oplysninger kan give indsigt, der er vigtig for at reducere den tid, ansættelsen tager, og give rekrutteringspersoner mulighed for at fokusere på, hvordan de kan reducere den tid, der bruges på de enkelte stadier.

## <a name="user-specific-security"></a>Brugerspecifik sikkerhed

Attract-rapporter er tilgængelige for administrator-, læs alle-, rekrutterings- og ansættelseschef [roller](security-attract.md). Ikke-tildelte brugere har ikke adgang til nogen af de analytiske rapportsider (Jobanalyser og Analysehub).

Jobanalyser-rapporter viser data for det valgte job. Analysehub-rapporter samler data på tværs af alle job, som en bruger kan få vist. Brugere, der kan få vist både Mine job og Alle job på siden Job, har de samme tilgængelige visninger i analysehubben.

## <a name="cross-filter"></a>Tværgående filtrer

En af de fantastiske funktioner i Power BI er den måde, som alle visuelle elementer på en rapportside er forbundet på. Hvis du markerer et datapunkt i et af de visuelle elementer, bliver alle andre visuelle elementer på siden, der indeholder denne dataændring, baseret på det markerede. Få mere at vide, og få vist et eksempel i [Hvordan visuelle elementer filtreres på tværs af hinanden i en Power BI-rapport](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).

## <a name="export-to-excel"></a>Eksportér til Excel

Hvis du vil have vist rapportdata i Excel, kan du klikke på menuen Indstillinger (tre prikker) i et visuelt element og vælge **Eksporter underliggende data**. Eksporterede data eksporteres som filtrerede i overensstemmelse med brugertilladelser i Attract. Du kan finde flere oplysninger under [Eksportere data fra visualiseringer](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).
