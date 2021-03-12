---
title: Kombinere serviceordrer
description: Du kan kombinere serviceordrer.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55de251f7f9cdbae99eaec13d4ddd7d3bf26b2bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996670"
---
# <a name="combine-service-orders"></a><span data-ttu-id="cefee-103">Kombinere serviceordrer</span><span class="sxs-lookup"><span data-stu-id="cefee-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="cefee-104">Når du opretter serviceordrelinjer automatisk i formularen **Serviceaftaler**, kan du vælge en af følgende indstillinger for at angive, hvordan de skal grupperes:</span><span class="sxs-lookup"><span data-stu-id="cefee-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="cefee-105">**Efter serviceaftale**</span><span class="sxs-lookup"><span data-stu-id="cefee-105">**By service agreement**</span></span>

  - <span data-ttu-id="cefee-106">**Efter serviceopgave**</span><span class="sxs-lookup"><span data-stu-id="cefee-106">**By service task**</span></span>

  - <span data-ttu-id="cefee-107">**Efter medarbejder**</span><span class="sxs-lookup"><span data-stu-id="cefee-107">**By employee**</span></span>

  - <span data-ttu-id="cefee-108">**Efter serviceobjekt**</span><span class="sxs-lookup"><span data-stu-id="cefee-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="cefee-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="cefee-109">Example</span></span>

<span data-ttu-id="cefee-110">Du opretter en serviceaftale med 31. marts 2007 som startdato.</span><span class="sxs-lookup"><span data-stu-id="cefee-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="cefee-111">I feltet **Kombinere serviceordrer** skal du angive **Efter serviceobjekt**.</span><span class="sxs-lookup"><span data-stu-id="cefee-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="cefee-112">Derefter opretter du følgende serviceaftalelinjer:</span><span class="sxs-lookup"><span data-stu-id="cefee-112">You then create the following service agreement lines:</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cefee-113">Aftalelinjenummer</span><span class="sxs-lookup"><span data-stu-id="cefee-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="cefee-114">Posteringstype</span><span class="sxs-lookup"><span data-stu-id="cefee-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="cefee-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cefee-115">Description</span></span></p></th>
<th><p><span data-ttu-id="cefee-116">Interval</span><span class="sxs-lookup"><span data-stu-id="cefee-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="cefee-117">Seriviceobjekt</span><span class="sxs-lookup"><span data-stu-id="cefee-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="cefee-118">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="cefee-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cefee-119">1</span><span class="sxs-lookup"><span data-stu-id="cefee-119">1</span></span></p></td>
<td><p><span data-ttu-id="cefee-120"><strong>Time</strong></span><span class="sxs-lookup"><span data-stu-id="cefee-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="cefee-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="cefee-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="cefee-122">Ugentlig</span><span class="sxs-lookup"><span data-stu-id="cefee-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="cefee-123">X-1</span><span class="sxs-lookup"><span data-stu-id="cefee-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="cefee-124">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="cefee-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cefee-125">2</span><span class="sxs-lookup"><span data-stu-id="cefee-125">2</span></span></p></td>
<td><p><span data-ttu-id="cefee-126"><strong>Time</strong></span><span class="sxs-lookup"><span data-stu-id="cefee-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="cefee-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="cefee-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="cefee-128">Hver 14. dag</span><span class="sxs-lookup"><span data-stu-id="cefee-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="cefee-129">X-2</span><span class="sxs-lookup"><span data-stu-id="cefee-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="cefee-130">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="cefee-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cefee-131">3</span><span class="sxs-lookup"><span data-stu-id="cefee-131">3</span></span></p></td>
<td><p><span data-ttu-id="cefee-132"><strong>Time</strong></span><span class="sxs-lookup"><span data-stu-id="cefee-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="cefee-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="cefee-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="cefee-134">Ugentlig</span><span class="sxs-lookup"><span data-stu-id="cefee-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="cefee-135">X-2</span><span class="sxs-lookup"><span data-stu-id="cefee-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="cefee-136">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="cefee-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cefee-137">Du angiver ikke tidsvinduer for serviceaftalelinjer.</span><span class="sxs-lookup"><span data-stu-id="cefee-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="cefee-138">Serviceaftalelinjerne flyttes derfor ikke fra den beregnede dag, de ligger på.</span><span class="sxs-lookup"><span data-stu-id="cefee-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="cefee-139">Derefter skal du oprette serviceordrelinjer fra formularen **Opret serviceordrer** fra 01-04-2007 til 30-04-2007.</span><span class="sxs-lookup"><span data-stu-id="cefee-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="cefee-140">Der oprettes i alt ti serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="cefee-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="cefee-141">Da den samlingsindstilling, du har valgt, var **Efter serviceobjekt**, har alle de serviceordrer, der oprettes, kun serviceordrelinjer med ét specifikt serviceobjekt.</span><span class="sxs-lookup"><span data-stu-id="cefee-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="cefee-142">Serviceordrelinjer, der oprettes ud fra serviceaftalen, og som har samme servicedato og samme objekt, samles på samme serviceordre.</span><span class="sxs-lookup"><span data-stu-id="cefee-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="cefee-143">I dette eksempel har den kalender, der er angivet i formularen <STRONG>Parametre for servicestyring</STRONG>, ingen lukkede dage.</span><span class="sxs-lookup"><span data-stu-id="cefee-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="cefee-144">Der sker en yderligere gruppering af serviceordrelinjer efter eventuelle tidsvinduer, du har angivet på serviceaftalelinjerne.</span><span class="sxs-lookup"><span data-stu-id="cefee-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="cefee-145">Se også</span><span class="sxs-lookup"><span data-stu-id="cefee-145">See also</span></span>

[<span data-ttu-id="cefee-146">Oprette serviceordrer automatisk</span><span class="sxs-lookup"><span data-stu-id="cefee-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  


