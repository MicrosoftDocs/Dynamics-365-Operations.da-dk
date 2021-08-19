---
title: Direkte afledte faste ordrer behandles i en gennemsynsarbejdsproces
description: Direkte afledte faste ordrer behandles i en arbejdsproces med status Til gennemsyn.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d20f1c1d6e8fc83dd996b04bf0321a41f7b39290f306d1ac9f4fcd17514832e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721169"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Direkte afledte faste ordrer behandles i en gennemsynsarbejdsproces

KB-nummer: 4612450

## <a name="symptoms"></a>Symptomer

Direkte afledte faste ordrer behandles i en arbejdsproces med status *Til gennemsyn*.

## <a name="resolution"></a>Løsning

Statussen *Til gennemsyn* tildeles til faste afledte ordrer (underleverandørindkøbsordrer), når sporing af ændringer er aktiveret. Hvis en indkøbsordre er afledt (en underleverandørindkøbsordre), sendes den derfor kun til en arbejdsproces. Hvis en indkøbsordre er et fast indkøbsordreforslag, godkendes den automatisk for at sikre, at planlægningssystemet ikke opretter nye ordreforslag, mens indkøbsordren stadig har status *Kladde*.
