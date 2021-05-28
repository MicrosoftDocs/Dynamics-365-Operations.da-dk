---
title: Akkumulering af debitorrabatter mislykkes, når der bruges varerabatgrupper
description: Når du bruger debitorrabataftaler sammen med varerabatgrupper, beregnes rabatter, men akkumuleringen mislykkes.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026361"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a><span data-ttu-id="7d791-103">Akkumulering af debitorrabatter mislykkes, når der bruges varerabatgrupper</span><span class="sxs-lookup"><span data-stu-id="7d791-103">Cumulation of customer rebates fails when item rebate groups are used</span></span>

<span data-ttu-id="7d791-104">KB-nummer: 4611372</span><span class="sxs-lookup"><span data-stu-id="7d791-104">KB number: 4611372</span></span>

## <a name="symptoms"></a><span data-ttu-id="7d791-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="7d791-105">Symptoms</span></span>

<span data-ttu-id="7d791-106">Når du bruger debitorrabataftaler (af typen *beløb*) sammen med varerabatgrupper, beregnes rabatter, men akkumuleringen mislykkes.</span><span class="sxs-lookup"><span data-stu-id="7d791-106">When you use customer rebate agreements (of the *amount* type) in combination with item rebate groups, rebates are calculated, but cumulation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="7d791-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="7d791-107">Resolution</span></span>

<span data-ttu-id="7d791-108">Systemet fungerer som designet.</span><span class="sxs-lookup"><span data-stu-id="7d791-108">The system is behaving as designed.</span></span> <span data-ttu-id="7d791-109">Varegrupper grupperer kun varer, der har samme grænsebetingelse.</span><span class="sxs-lookup"><span data-stu-id="7d791-109">Item groups group only items that have the same threshold condition.</span></span> <span data-ttu-id="7d791-110">Rabatbetingelsen (grænseværdien) angives i forhold til beløbet for hver vare og ikke i forhold til det akkumulerede beløb for en vare i varegruppen.</span><span class="sxs-lookup"><span data-stu-id="7d791-110">The rebate condition (threshold) is set against the amount for each item, not against the cumulated amount for any item in the item group.</span></span>
