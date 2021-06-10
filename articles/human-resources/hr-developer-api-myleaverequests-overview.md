---
title: Oversigt over MyLeaveRequests
description: MyLeaveRequests-enheden i Microsoft Dynamics 365 Human Resources indeholder listen over orlovsanmodninger i systemet, beregnet (begrænset) til de anmodninger, der er tilgængelige for den aktuelle bruger, der forespørger om enheden.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054950"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="1ebd8-103">Oversigt over MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="1ebd8-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1ebd8-104">MyLeaveRequests-enheden i Microsoft Dynamics 365 Human Resources indeholder listen over orlovsanmodninger i systemet, beregnet (begrænset) til de anmodninger, der er tilgængelige for den aktuelle bruger, der forespørger om enheden.</span><span class="sxs-lookup"><span data-stu-id="1ebd8-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="1ebd8-105">Nøgle</span><span class="sxs-lookup"><span data-stu-id="1ebd8-105">Key</span></span>

  | <span data-ttu-id="1ebd8-106">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="1ebd8-106">Property Name</span></span> | <span data-ttu-id="1ebd8-107">Datatype</span><span class="sxs-lookup"><span data-stu-id="1ebd8-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="1ebd8-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="1ebd8-108">dataAreaId</span></span>    | <span data-ttu-id="1ebd8-109">Streng</span><span class="sxs-lookup"><span data-stu-id="1ebd8-109">String</span></span>    |
  | <span data-ttu-id="1ebd8-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="1ebd8-110">RequestId</span></span>     | <span data-ttu-id="1ebd8-111">Streng</span><span class="sxs-lookup"><span data-stu-id="1ebd8-111">String</span></span>    |
  | <span data-ttu-id="1ebd8-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="1ebd8-112">LeaveType</span></span>     | <span data-ttu-id="1ebd8-113">Streng</span><span class="sxs-lookup"><span data-stu-id="1ebd8-113">String</span></span>    |
  | <span data-ttu-id="1ebd8-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="1ebd8-114">LeaveDate</span></span>     | <span data-ttu-id="1ebd8-115">Dato</span><span class="sxs-lookup"><span data-stu-id="1ebd8-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="1ebd8-116">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="1ebd8-116">Properties</span></span>

  | <span data-ttu-id="1ebd8-117">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="1ebd8-117">Property Name</span></span>     | <span data-ttu-id="1ebd8-118">Datatype</span><span class="sxs-lookup"><span data-stu-id="1ebd8-118">Data Type</span></span> | <span data-ttu-id="1ebd8-119">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="1ebd8-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="1ebd8-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="1ebd8-120">dataAreaId</span></span>        | <span data-ttu-id="1ebd8-121">Streng</span><span class="sxs-lookup"><span data-stu-id="1ebd8-121">String</span></span>    | <span data-ttu-id="1ebd8-122">X</span><span class="sxs-lookup"><span data-stu-id="1ebd8-122">X</span></span>        |
  | <span data-ttu-id="1ebd8-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="1ebd8-123">RequestId</span></span>         | <span data-ttu-id="1ebd8-124">Streng</span><span class="sxs-lookup"><span data-stu-id="1ebd8-124">String</span></span>    | <span data-ttu-id="1ebd8-125">X</span><span class="sxs-lookup"><span data-stu-id="1ebd8-125">X</span></span>        |
  | <span data-ttu-id="1ebd8-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="1ebd8-126">LeaveType</span></span>         | <span data-ttu-id="1ebd8-127">Streng</span><span class="sxs-lookup"><span data-stu-id="1ebd8-127">String</span></span>    | <span data-ttu-id="1ebd8-128">X</span><span class="sxs-lookup"><span data-stu-id="1ebd8-128">X</span></span>        |
  | <span data-ttu-id="1ebd8-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="1ebd8-129">LeaveDate</span></span>         | <span data-ttu-id="1ebd8-130">Dato</span><span class="sxs-lookup"><span data-stu-id="1ebd8-130">Date</span></span>      | <span data-ttu-id="1ebd8-131">X</span><span class="sxs-lookup"><span data-stu-id="1ebd8-131">X</span></span>        |
  | <span data-ttu-id="1ebd8-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="1ebd8-132">ReasonCodeId</span></span>      | <span data-ttu-id="1ebd8-133">Streng</span><span class="sxs-lookup"><span data-stu-id="1ebd8-133">String</span></span>    |          |
  | <span data-ttu-id="1ebd8-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="1ebd8-134">PersonnelNumber</span></span>   | <span data-ttu-id="1ebd8-135">Streng</span><span class="sxs-lookup"><span data-stu-id="1ebd8-135">String</span></span>    | <span data-ttu-id="1ebd8-136">X</span><span class="sxs-lookup"><span data-stu-id="1ebd8-136">X</span></span>        |
  | <span data-ttu-id="1ebd8-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="1ebd8-137">RequestDate</span></span>       | <span data-ttu-id="1ebd8-138">Dato</span><span class="sxs-lookup"><span data-stu-id="1ebd8-138">Date</span></span>      | <span data-ttu-id="1ebd8-139">X</span><span class="sxs-lookup"><span data-stu-id="1ebd8-139">X</span></span>        |
  | <span data-ttu-id="1ebd8-140">Kommentar</span><span class="sxs-lookup"><span data-stu-id="1ebd8-140">Comment</span></span>           | <span data-ttu-id="1ebd8-141">Streng</span><span class="sxs-lookup"><span data-stu-id="1ebd8-141">String</span></span>    |          |
  | <span data-ttu-id="1ebd8-142">Status</span><span class="sxs-lookup"><span data-stu-id="1ebd8-142">Status</span></span>            | <span data-ttu-id="1ebd8-143">Fasttekst</span><span class="sxs-lookup"><span data-stu-id="1ebd8-143">Enum</span></span>      | <span data-ttu-id="1ebd8-144">X</span><span class="sxs-lookup"><span data-stu-id="1ebd8-144">X</span></span>        |
  | <span data-ttu-id="1ebd8-145">Beløb</span><span class="sxs-lookup"><span data-stu-id="1ebd8-145">Amount</span></span>            | <span data-ttu-id="1ebd8-146">Kommatal</span><span class="sxs-lookup"><span data-stu-id="1ebd8-146">Real</span></span>      |          |
  | <span data-ttu-id="1ebd8-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="1ebd8-147">HalfDayDefinition</span></span> | <span data-ttu-id="1ebd8-148">Fasttekst</span><span class="sxs-lookup"><span data-stu-id="1ebd8-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="1ebd8-149">Handlinger</span><span class="sxs-lookup"><span data-stu-id="1ebd8-149">Actions</span></span>

 | <span data-ttu-id="1ebd8-150">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="1ebd8-150">Action Name</span></span>                               | <span data-ttu-id="1ebd8-151">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1ebd8-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="1ebd8-152">indsend</span><span class="sxs-lookup"><span data-stu-id="1ebd8-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="1ebd8-153">Send den anmodning, der skal behandles af arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="1ebd8-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="1ebd8-154">Se også</span><span class="sxs-lookup"><span data-stu-id="1ebd8-154">See also</span></span>

- [<span data-ttu-id="1ebd8-155">Sende en orlovsanmodning til arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="1ebd8-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="1ebd8-156">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="1ebd8-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]