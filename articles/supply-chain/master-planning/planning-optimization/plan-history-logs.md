---
title: Få vist planhistorik og planlægningslogs
description: Dette emne beskriver, hvordan du kan få vist historikken for planlægningsjobs, der udløses af funktionen Planlægningsoptimering.
author: t-benebo
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 9b4cba4dd94eb198e770d152d4f759a706065dee
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469751"
---
# <a name="view-plan-history-and-planning-logs"></a>Få vist planhistorik og planlægningslogs

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du kan få vist historikken for planlægningsjobs, der udløses af funktionen Planlægningsoptimering i Microsoft Dynamics 365 Supply Chain Management.

Hvis du vil have vist historikken for en plan, skal du åbne planen ved at gå til **Varedisponering** \> **Opsætning** \> **Planer** \> **Behovsplaner** og vælge **Historik**. Historikken viser alle job for den valgte plan. Listen omfatter afsluttede og aktive job.

Historikken for job til varedisponering i Planlægningsoptimering beholder kun 60 poster pr. behovsplan. Når du kører en ny beregning af varedisponering, slettes den tidligste historikpost for planen.

Ud over at se starttidspunkt og status for job, kan du få vist loggen for et bestemt job. Loggen indeholder yderligere oplysninger og advarsler. Ikke alle job har en log. Hvis du vil have vist loggen for et job, skla du vælge **Log**. Logposter gemmes kun i 30 dage efter den dato, hvor jobbet er afsluttet, og derefter slettes de automatisk.

Hvis indstillingen **Batchafvikling** i oversigtspanelet **Kør i baggrunden** blev aktiveret, da behandling af varedisponering blev konfigureret, indeholder batchjobloggen flere oplysninger om eventuelle advarsler og fejl, der blev genereret under varedisponeringskørslen. Fejl ved automatisk autorisation registreres f.eks. kun i batchjobloggen. De vises ikke i logfiler på siden **Historik**.

Hvis du vil se fejl og andre advarsler eller fejl, der er opstået under en kørsel af varedisponering, for automatisk autorisation, skal du følge disse trin.

1. Gå til **Systemadministration \> Forespørgsler \> Batchjob**.
1. Find og vælg den post, der repræsenterer den kørsel af varedisponering, du er interesseret i. (F.eks. værdien af feltet **Jobbeskrivelse** kan starte med *Varedisponering*).
1. Følg et af disse trin, afhængigt af om du bruger den *udvidede formular* eller *ældre (ikke-forbedret) formular* til siden **Batchjob**:

    - Hvis du bruger den forbedrede formular: Vælg **Batchjobhistorik** i handlingsruden. På siden **Batchjobhistorik** skal du derefter vælge **Log** i handlingsruden.
    - Hvis du bruger den ældre formular: Vælg **Log** på fanen **Batchjob** i handlingsruden.

1. Vælg **Meddelelsesdetaljer** for at åbne ruden **Meddelelsesdetaljer**, hvor du kan få vist alle de advarsler og fejl, du har registreret under behandlingen.

## <a name="related-resources"></a>Tilknyttede ressourcer

- [Oversigt over planlægningsoptimering](planning-optimization-overview.md)
- [Start her med planlægningsoptimering](get-started.md)
- [Analyse af om Planlægningsoptimering passer til](planning-optimization-fit-analysis.md)
- [Anvend filtre på en plan](plan-filters.md)
- [Annullere et planlægningsjob](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
