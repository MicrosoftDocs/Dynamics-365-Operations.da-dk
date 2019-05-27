---
title: Interaktion mellem felter med servicestatus og fremskridt
description: I formularen Serviceordrer afspejler feltet Status i serviceordrens header status for hele serviceordren, og Status rapporterer status for de enkelte linjer i serviceordren.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dd7b5160149a38dd62535901c1225bf704f404d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570780"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="18c39-103">Interaktion mellem felter med servicestatus og fremskridt</span><span class="sxs-lookup"><span data-stu-id="18c39-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="18c39-104">I formularen **Serviceordrer** afspejler feltet **Status** i serviceordrens header status for hele serviceordren, og **Status** rapporterer status for de enkelte linjer i serviceordren.</span><span class="sxs-lookup"><span data-stu-id="18c39-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18c39-105">Status</span><span class="sxs-lookup"><span data-stu-id="18c39-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="18c39-106">Status for linje 1</span><span class="sxs-lookup"><span data-stu-id="18c39-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="18c39-107">Status for linje 2</span><span class="sxs-lookup"><span data-stu-id="18c39-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="18c39-108">Status for linje 3</span><span class="sxs-lookup"><span data-stu-id="18c39-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18c39-109"><strong>Under behandling</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-110"><strong>Oprettet</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-111"><strong>Oprettet</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-112"><strong>Oprettet</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18c39-113"><strong>Under behandling</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-114"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-115"><strong>Oprettet</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-116"><strong>Oprettet</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18c39-117"><strong>Under behandling</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-118"><strong>Oprettet</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-119"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-120"><strong>Bogført</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18c39-121"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-122"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-123"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-124"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18c39-125"><strong>Bogført</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-126"><strong>Bogført</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-127"><strong>Bogført</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-128"><strong>Bogført</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18c39-129"><strong>Bogført</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-130"><strong>Bogført</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-131"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="18c39-132"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="18c39-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18c39-133">En serviceordre er igangværende, hvis status for alle linjer er **Oprettet**. Den er stadig igangværende, hvis status for nogle af linjerne er **Annulleret** eller **Bogført**.</span><span class="sxs-lookup"><span data-stu-id="18c39-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="18c39-134">Hvis alle linjerne i en serviceordre er mærket **Bogført**, er status for ordren **Bogført**.</span><span class="sxs-lookup"><span data-stu-id="18c39-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="18c39-135">Hvis nogle linjer er **Bogført**, og nogle er **Annulleret**, er status stadig **Bogført**.</span><span class="sxs-lookup"><span data-stu-id="18c39-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


