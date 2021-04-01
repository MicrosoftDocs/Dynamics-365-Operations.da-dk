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
ms.openlocfilehash: 7bd3ac8cf3c025b082b33247fcd020aebc010bc8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247712"
---
# <a name="combine-service-orders"></a><span data-ttu-id="e51bc-103">Kombinere serviceordrer</span><span class="sxs-lookup"><span data-stu-id="e51bc-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e51bc-104">Når du opretter serviceordrelinjer automatisk i formularen **Serviceaftaler**, kan du vælge en af følgende indstillinger for at angive, hvordan de skal grupperes:</span><span class="sxs-lookup"><span data-stu-id="e51bc-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="e51bc-105">**Efter serviceaftale**</span><span class="sxs-lookup"><span data-stu-id="e51bc-105">**By service agreement**</span></span>

  - <span data-ttu-id="e51bc-106">**Efter serviceopgave**</span><span class="sxs-lookup"><span data-stu-id="e51bc-106">**By service task**</span></span>

  - <span data-ttu-id="e51bc-107">**Efter medarbejder**</span><span class="sxs-lookup"><span data-stu-id="e51bc-107">**By employee**</span></span>

  - <span data-ttu-id="e51bc-108">**Efter serviceobjekt**</span><span class="sxs-lookup"><span data-stu-id="e51bc-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="e51bc-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e51bc-109">Example</span></span>

<span data-ttu-id="e51bc-110">Du opretter en serviceaftale med 31. marts 2007 som startdato.</span><span class="sxs-lookup"><span data-stu-id="e51bc-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="e51bc-111">I feltet **Kombinere serviceordrer** skal du angive **Efter serviceobjekt**.</span><span class="sxs-lookup"><span data-stu-id="e51bc-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="e51bc-112">Derefter opretter du følgende serviceaftalelinjer:</span><span class="sxs-lookup"><span data-stu-id="e51bc-112">You then create the following service agreement lines:</span></span>

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
<th><p><span data-ttu-id="e51bc-113">Aftalelinjenummer</span><span class="sxs-lookup"><span data-stu-id="e51bc-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="e51bc-114">Posteringstype</span><span class="sxs-lookup"><span data-stu-id="e51bc-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="e51bc-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e51bc-115">Description</span></span></p></th>
<th><p><span data-ttu-id="e51bc-116">Interval</span><span class="sxs-lookup"><span data-stu-id="e51bc-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="e51bc-117">Seriviceobjekt</span><span class="sxs-lookup"><span data-stu-id="e51bc-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="e51bc-118">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="e51bc-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e51bc-119">1</span><span class="sxs-lookup"><span data-stu-id="e51bc-119">1</span></span></p></td>
<td><p><span data-ttu-id="e51bc-120"><strong>Time</strong></span><span class="sxs-lookup"><span data-stu-id="e51bc-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="e51bc-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="e51bc-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="e51bc-122">Ugentlig</span><span class="sxs-lookup"><span data-stu-id="e51bc-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="e51bc-123">X-1</span><span class="sxs-lookup"><span data-stu-id="e51bc-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="e51bc-124">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="e51bc-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e51bc-125">2</span><span class="sxs-lookup"><span data-stu-id="e51bc-125">2</span></span></p></td>
<td><p><span data-ttu-id="e51bc-126"><strong>Time</strong></span><span class="sxs-lookup"><span data-stu-id="e51bc-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="e51bc-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="e51bc-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="e51bc-128">Hver 14. dag</span><span class="sxs-lookup"><span data-stu-id="e51bc-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="e51bc-129">X-2</span><span class="sxs-lookup"><span data-stu-id="e51bc-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="e51bc-130">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="e51bc-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e51bc-131">3</span><span class="sxs-lookup"><span data-stu-id="e51bc-131">3</span></span></p></td>
<td><p><span data-ttu-id="e51bc-132"><strong>Time</strong></span><span class="sxs-lookup"><span data-stu-id="e51bc-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="e51bc-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="e51bc-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="e51bc-134">Ugentlig</span><span class="sxs-lookup"><span data-stu-id="e51bc-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="e51bc-135">X-2</span><span class="sxs-lookup"><span data-stu-id="e51bc-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="e51bc-136">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="e51bc-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e51bc-137">Du angiver ikke tidsvinduer for serviceaftalelinjer.</span><span class="sxs-lookup"><span data-stu-id="e51bc-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="e51bc-138">Serviceaftalelinjerne flyttes derfor ikke fra den beregnede dag, de ligger på.</span><span class="sxs-lookup"><span data-stu-id="e51bc-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="e51bc-139">Derefter skal du oprette serviceordrelinjer fra formularen **Opret serviceordrer** fra 01-04-2007 til 30-04-2007.</span><span class="sxs-lookup"><span data-stu-id="e51bc-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="e51bc-140">Der oprettes i alt ti serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="e51bc-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="e51bc-141">Da den samlingsindstilling, du har valgt, var **Efter serviceobjekt**, har alle de serviceordrer, der oprettes, kun serviceordrelinjer med ét specifikt serviceobjekt.</span><span class="sxs-lookup"><span data-stu-id="e51bc-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="e51bc-142">Serviceordrelinjer, der oprettes ud fra serviceaftalen, og som har samme servicedato og samme objekt, samles på samme serviceordre.</span><span class="sxs-lookup"><span data-stu-id="e51bc-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e51bc-143">I dette eksempel har den kalender, der er angivet i formularen <STRONG>Parametre for servicestyring</STRONG>, ingen lukkede dage.</span><span class="sxs-lookup"><span data-stu-id="e51bc-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="e51bc-144">Der sker en yderligere gruppering af serviceordrelinjer efter eventuelle tidsvinduer, du har angivet på serviceaftalelinjerne.</span><span class="sxs-lookup"><span data-stu-id="e51bc-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="e51bc-145">Se også</span><span class="sxs-lookup"><span data-stu-id="e51bc-145">See also</span></span>

[<span data-ttu-id="e51bc-146">Oprette serviceordrer automatisk</span><span class="sxs-lookup"><span data-stu-id="e51bc-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]