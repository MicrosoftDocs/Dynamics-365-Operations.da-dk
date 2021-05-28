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
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="c9f1b-103">Direkte afledte faste ordrer behandles i en gennemsynsarbejdsproces</span><span class="sxs-lookup"><span data-stu-id="c9f1b-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="c9f1b-104">KB-nummer: 4612450</span><span class="sxs-lookup"><span data-stu-id="c9f1b-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="c9f1b-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="c9f1b-105">Symptoms</span></span>

<span data-ttu-id="c9f1b-106">Direkte afledte faste ordrer behandles i en arbejdsproces med status *Til gennemsyn*.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="c9f1b-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="c9f1b-107">Resolution</span></span>

<span data-ttu-id="c9f1b-108">Statussen *Til gennemsyn* tildeles til faste afledte ordrer (underleverandørindkøbsordrer), når sporing af ændringer er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="c9f1b-109">Hvis en indkøbsordre er afledt (en underleverandørindkøbsordre), sendes den derfor kun til en arbejdsproces.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="c9f1b-110">Hvis en indkøbsordre er et fast indkøbsordreforslag, godkendes den automatisk for at sikre, at planlægningssystemet ikke opretter nye ordreforslag, mens indkøbsordren stadig har status *Kladde*.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
