---
title: Eksempel på reduktionsdage
description: Eksempel på reduktionsdage.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87c46cd7ee7410e1c7cb88868cd19f5075482f8c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975650"
---
# <a name="reduction-days-example"></a><span data-ttu-id="d95ba-103">Eksempel på reduktionsdage</span><span class="sxs-lookup"><span data-stu-id="d95ba-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d95ba-104">Du har oprettet en abonnementspostering for en kundes vedligeholdelsesabonnement som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d95ba-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d95ba-105">Fra dato</span><span class="sxs-lookup"><span data-stu-id="d95ba-105">From date</span></span></p></th>
<th><p><span data-ttu-id="d95ba-106">Til dato</span><span class="sxs-lookup"><span data-stu-id="d95ba-106">To date</span></span></p></th>
<th><p><span data-ttu-id="d95ba-107">Abonnement</span><span class="sxs-lookup"><span data-stu-id="d95ba-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="d95ba-108">Abonnementstype</span><span class="sxs-lookup"><span data-stu-id="d95ba-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="d95ba-109">Projekt</span><span class="sxs-lookup"><span data-stu-id="d95ba-109">Project</span></span></p></th>
<th><p><span data-ttu-id="d95ba-110">Kategori</span><span class="sxs-lookup"><span data-stu-id="d95ba-110">Category</span></span></p></th>
<th><p><span data-ttu-id="d95ba-111">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="d95ba-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="d95ba-112">Salgspris</span><span class="sxs-lookup"><span data-stu-id="d95ba-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d95ba-113">1. marts 2011</span><span class="sxs-lookup"><span data-stu-id="d95ba-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="d95ba-114">31. marts 2011</span><span class="sxs-lookup"><span data-stu-id="d95ba-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="d95ba-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="d95ba-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="d95ba-116"><strong>Regulær</strong></span><span class="sxs-lookup"><span data-stu-id="d95ba-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="d95ba-117">9013</span><span class="sxs-lookup"><span data-stu-id="d95ba-117">9013</span></span></p></td>
<td><p><span data-ttu-id="d95ba-118">Abn.art2</span><span class="sxs-lookup"><span data-stu-id="d95ba-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="d95ba-119">EUR</span><span class="sxs-lookup"><span data-stu-id="d95ba-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="d95ba-120">200,00</span><span class="sxs-lookup"><span data-stu-id="d95ba-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d95ba-121">Kunden rapporterer, at der ikke er behov for servicedækning i to dage (d. 10. og 11. marts).</span><span class="sxs-lookup"><span data-stu-id="d95ba-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="d95ba-122">Du indvilliger i at reducere abonnementet med disse to dage.</span><span class="sxs-lookup"><span data-stu-id="d95ba-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="d95ba-123">Du opretter en ny postering af typen **Reduktionsdage** som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d95ba-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d95ba-124">Fra-dato</span><span class="sxs-lookup"><span data-stu-id="d95ba-124">From date</span></span></p></th>
<th><p><span data-ttu-id="d95ba-125">Til-dato</span><span class="sxs-lookup"><span data-stu-id="d95ba-125">To date</span></span></p></th>
<th><p><span data-ttu-id="d95ba-126">Abonnement</span><span class="sxs-lookup"><span data-stu-id="d95ba-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="d95ba-127">Abonnementstype</span><span class="sxs-lookup"><span data-stu-id="d95ba-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="d95ba-128">Projekt</span><span class="sxs-lookup"><span data-stu-id="d95ba-128">Project</span></span></p></th>
<th><p><span data-ttu-id="d95ba-129">Kategori</span><span class="sxs-lookup"><span data-stu-id="d95ba-129">Category</span></span></p></th>
<th><p><span data-ttu-id="d95ba-130">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="d95ba-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="d95ba-131">Salgspris</span><span class="sxs-lookup"><span data-stu-id="d95ba-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d95ba-132">10. marts 2011</span><span class="sxs-lookup"><span data-stu-id="d95ba-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="d95ba-133">11. marts 2011</span><span class="sxs-lookup"><span data-stu-id="d95ba-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="d95ba-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="d95ba-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="d95ba-135"><strong>Reduktionsdage</strong></span><span class="sxs-lookup"><span data-stu-id="d95ba-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="d95ba-136">9013</span><span class="sxs-lookup"><span data-stu-id="d95ba-136">9013</span></span></p></td>
<td><p><span data-ttu-id="d95ba-137">Abn.art2</span><span class="sxs-lookup"><span data-stu-id="d95ba-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="d95ba-138">EUR</span><span class="sxs-lookup"><span data-stu-id="d95ba-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="d95ba-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="d95ba-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d95ba-140">Når posteringerne for marts 2011 faktureres, reduceres salgsprisen på EUR 200 med EUR 12,90.</span><span class="sxs-lookup"><span data-stu-id="d95ba-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="d95ba-141">Det beløb, der kan faktureres for abonnementsposteringen, er derfor EUR 187,10, og der faktureres to posteringer til et samlet beløb på EUR 187,10.</span><span class="sxs-lookup"><span data-stu-id="d95ba-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="d95ba-142">Se også</span><span class="sxs-lookup"><span data-stu-id="d95ba-142">See also</span></span>

[<span data-ttu-id="d95ba-143">Reducere dagene på abonnementsgebyrer</span><span class="sxs-lookup"><span data-stu-id="d95ba-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


