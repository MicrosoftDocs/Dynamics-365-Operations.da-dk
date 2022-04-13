---
title: Annullere et planlægningsjob
description: I dette emne beskrives det, hvordan du kan annullere et aktivt planlægningsjob, der bruger funktionen Planlægningsoptimering.
author: t-benebo
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 02bfae460566e7dfcb9abbc43b2b57a6b06d444c
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/23/2022
ms.locfileid: "8470255"
---
# <a name="cancel-a-planning-job"></a>Annullere et planlægningsjob

[!include [banner](../../includes/banner.md)]

I Microsoft Dynamics 365 Supply Chain Management kan du annullere et aktivt planlægningsjob, der bruger funktionen Planlægningsoptimering. Når du vælger **Annuller** i dialogboksen, når et planlægningsoptimeringsjob udløses direkte fra brugergrænsefladen (ikke i baggrunden), annullerer dette ikke planlægningsoptimeringsjobbet. Selvom du får vist en advarsel såsom "Handlingen er annulleret", skal du stadig bruge følgende trin for at annullere et planlægningsjob med planlægningsoptimering.


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

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over planlægningsoptimering](planning-optimization-overview.md)

[Kom i gang med planlægningsoptimering](get-started.md)

[Analyse af om Planlægningsoptimering passer til](planning-optimization-fit-analysis.md)

[Få vist planhistorik og planlægningslogs](plan-history-logs.md)

[Anvend filtre på en plan](plan-filters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]