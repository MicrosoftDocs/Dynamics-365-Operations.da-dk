---
title: Vise planhistorik og planlægningslogge
description: Denne artikel forklarer, hvordan du får vist historikken for planlægningsjobs.
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
ms.openlocfilehash: ab469686a009364bf53cb963506fd2107075a283
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740925"
---
# <a name="view-plan-history-and-planning-logs"></a>Vise planhistorik og planlægningslogge

[!include [banner](../../includes/banner.md)]

Denne artikel forklarer, hvordan du får vist historikken for planlægningsjobs i Microsoft Dynamics 365 Supply Chain Management.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
