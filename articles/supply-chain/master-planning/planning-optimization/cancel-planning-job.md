---
title: Annullere et planlægningsjob
description: I dette emne beskrives det, hvordan du kan annullere et aktivt planlægningsjob, der bruger funktionen Planlægningsoptimering.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
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
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773928"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a>Annullere et planlægningsjob

I Microsoft Dynamics 365 Supply Chain Management kan du annullere et aktivt planlægningsjob, der bruger funktionen Planlægningsoptimering.

Benyt følgende fremgangsmåde for at annullere et aktivt planlægningsjob.

> [!NOTE]
> Kun aktive jobs kan annulleres.

1. Gå til **Varedisponering \> Opsætning \> Planer**.
2. Vælg den relevante plan for den planlagte kørsel.
3. Vælg **Historik**.
4. Vælg det planlægningsjob, du vil annullere.
5. Vælg **Annuller**.

Jobstatussen angives til **Annulleres** indtil planlægningsoptimeringstjenesten bekræfter, at jobbet er blevet annulleret. Statussen ændres derefter til **Annulleret**.

> [!NOTE]
> Hvis du vil have vist statusændringerne, skal du opdatere siden ved at klikke på knappen **Opdater**.

## <a name="related-resources"></a>Tilknyttede ressourcer

[Oversigt over Planlægningsoptimering](planning-optimization-overview.md)

[Introduktion til Planlægningsoptimering](get-started.md)

[Analyse af om Planlægningsoptimering passer til](planning-optimization-fit-analysis.md)

[Få vist planhistorik og planlægningslogs](plan-history-logs.md)

[Anvend filtre på en plan](plan-filters.md)
