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
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026379"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Direkte afledte faste ordrer behandles i en gennemsynsarbejdsproces

KB-nummer: 4612450

## <a name="symptoms"></a>Symptomer

Direkte afledte faste ordrer behandles i en arbejdsproces med status *Til gennemsyn*.

## <a name="resolution"></a>Løsning

Statussen *Til gennemsyn* tildeles til faste afledte ordrer (underleverandørindkøbsordrer), når sporing af ændringer er aktiveret. Hvis en indkøbsordre er afledt (en underleverandørindkøbsordre), sendes den derfor kun til en arbejdsproces. Hvis en indkøbsordre er et fast indkøbsordreforslag, godkendes den automatisk for at sikre, at planlægningssystemet ikke opretter nye ordreforslag, mens indkøbsordren stadig har status *Kladde*.
