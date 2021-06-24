---
title: Få vist planhistorik og planlægningslogs
description: Dette emne beskriver, hvordan du kan få vist historikken for planlægningsjobs, der udløses af funktionen Planlægningsoptimering.
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187241"
---
# <a name="view-plan-history-and-planning-logs"></a>Få vist planhistorik og planlægningslogs

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du kan få vist historikken for planlægningsjobs, der udløses af funktionen Planlægningsoptimering i Microsoft Dynamics 365 Supply Chain Management.

Hvis du vil have vist historikken for en plan, skal du åbne planen ved at gå til **Varedisponering** \> **Opsætning** \> **Planer** \> **Behovsplaner** og vælge **Historik**. Historikken viser alle job for den valgte plan. Listen omfatter afsluttede og aktive job.

Historikken for job til varedisponering i Planlægningsoptimering beholder kun 60 poster pr. behovsplan. Når du kører en ny beregning af varedisponering, slettes den tidligste historikpost for planen.

Ud over at se starttidspunkt og status for job, kan du få vist loggen for et bestemt job. Loggen indeholder yderligere oplysninger og advarsler. Ikke alle job har en log. Hvis du vil have vist loggen for et job, skla du vælge **Log**. Logposter gemmes kun i 30 dage efter den dato, hvor jobbet er afsluttet, og derefter slettes de automatisk.

## <a name="related-resources"></a>Tilknyttede ressourcer

- [Oversigt over planlægningsoptimering](planning-optimization-overview.md)
- [Start her med planlægningsoptimering](get-started.md)
- [Analyse af om Planlægningsoptimering passer til](planning-optimization-fit-analysis.md)
- [Anvend filtre på en plan](plan-filters.md)
- [Annullere et planlægningsjob](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]