---
title: Interaktion mellem felter med servicestatus og fremskridt
description: I formularen Serviceordrer afspejler feltet Status i serviceordrens header status for hele serviceordren, og Status rapporterer status for de enkelte linjer i serviceordren.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd70d00f7ce531b225362065dfd9f1f5c1adc754
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207318"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="b66c7-103">Interaktion mellem felter med servicestatus og fremskridt</span><span class="sxs-lookup"><span data-stu-id="b66c7-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b66c7-104">I formularen **Serviceordrer** afspejler feltet **Status** i serviceordrens header status for hele serviceordren, og **Status** rapporterer status for de enkelte linjer i serviceordren.</span><span class="sxs-lookup"><span data-stu-id="b66c7-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b66c7-105">Status</span><span class="sxs-lookup"><span data-stu-id="b66c7-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="b66c7-106">Status for linje 1</span><span class="sxs-lookup"><span data-stu-id="b66c7-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="b66c7-107">Status for linje 2</span><span class="sxs-lookup"><span data-stu-id="b66c7-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="b66c7-108">Status for linje 3</span><span class="sxs-lookup"><span data-stu-id="b66c7-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b66c7-109"><strong>Under behandling</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-110"><strong>Oprettet</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-111"><strong>Oprettet</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-112"><strong>Oprettet</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b66c7-113"><strong>Under behandling</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-114"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-115"><strong>Oprettet</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-116"><strong>Oprettet</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b66c7-117"><strong>Under behandling</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-118"><strong>Oprettet</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-119"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-120"><strong>Bogført</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b66c7-121"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-122"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-123"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-124"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b66c7-125"><strong>Bogført</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-126"><strong>Bogført</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-127"><strong>Bogført</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-128"><strong>Bogført</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b66c7-129"><strong>Bogført</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-130"><strong>Bogført</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-131"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b66c7-132"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="b66c7-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b66c7-133">En serviceordre er igangværende, hvis status for alle linjer er **Oprettet**. Den er stadig igangværende, hvis status for nogle af linjerne er **Annulleret** eller **Bogført**.</span><span class="sxs-lookup"><span data-stu-id="b66c7-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="b66c7-134">Hvis alle linjerne i en serviceordre er mærket **Bogført**, er status for ordren **Bogført**.</span><span class="sxs-lookup"><span data-stu-id="b66c7-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="b66c7-135">Hvis nogle linjer er **Bogført**, og nogle er **Annulleret**, er status stadig **Bogført**.</span><span class="sxs-lookup"><span data-stu-id="b66c7-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


