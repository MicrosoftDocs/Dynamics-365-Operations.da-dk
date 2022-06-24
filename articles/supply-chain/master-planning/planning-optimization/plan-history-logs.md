---
title: Få vist planhistorik og planlægningslogs
description: Denne artikel beskriver, hvordan du kan få vist historikken for planlægningsjobs, der udløses af funktionen Planlægningsoptimering.
author: t-benebo
ms.date: 06/01/2020
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
ms.openlocfilehash: b2c9257fc67a06b57418b2f5b035b2b540131405
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863934"
---
# <a name="view-plan-history-and-planning-logs"></a>Få vist planhistorik og planlægningslogs

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan du kan få vist historikken for planlægningsjobs, der udløses af funktionen Planlægningsoptimering i Microsoft Dynamics 365 Supply Chain Management.

Hvis du vil have vist historikken for en plan, skal du åbne planen ved at gå til **Varedisponering** \> **Opsætning** \> **Planer** \> **Behovsplaner** og vælge **Historik**. Historikken viser alle job for den valgte plan. Listen omfatter afsluttede og aktive job.

Systemet beholder maksimalt 60 historikposter pr. behovsplan og sletter poster, der er ældre end 30 dage. Hver gang du kører en ny beregning fra behovsplanlægningen, tilføjer systemet en ny historikpost og rydder derefter op i de ældste poster efter behov.

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
