---
title: Oversigt over MyLeaveRequests
description: MyLeaveRequests-enheden i Microsoft Dynamics 365 Human Resources indeholder listen over orlovsanmodninger i systemet, beregnet (begrænset) til de anmodninger, der er tilgængelige for den aktuelle bruger, der forespørger om enheden.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417737"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="251e1-103">Oversigt over MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="251e1-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="251e1-104">MyLeaveRequests-enheden i Microsoft Dynamics 365 Human Resources indeholder listen over orlovsanmodninger i systemet, beregnet (begrænset) til de anmodninger, der er tilgængelige for den aktuelle bruger, der forespørger om enheden.</span><span class="sxs-lookup"><span data-stu-id="251e1-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="251e1-105">Nøgle</span><span class="sxs-lookup"><span data-stu-id="251e1-105">Key</span></span>

  | <span data-ttu-id="251e1-106">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="251e1-106">Property Name</span></span> | <span data-ttu-id="251e1-107">Datatype</span><span class="sxs-lookup"><span data-stu-id="251e1-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="251e1-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="251e1-108">dataAreaId</span></span>    | <span data-ttu-id="251e1-109">Streng</span><span class="sxs-lookup"><span data-stu-id="251e1-109">String</span></span>    |
  | <span data-ttu-id="251e1-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="251e1-110">RequestId</span></span>     | <span data-ttu-id="251e1-111">Streng</span><span class="sxs-lookup"><span data-stu-id="251e1-111">String</span></span>    |
  | <span data-ttu-id="251e1-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="251e1-112">LeaveType</span></span>     | <span data-ttu-id="251e1-113">Streng</span><span class="sxs-lookup"><span data-stu-id="251e1-113">String</span></span>    |
  | <span data-ttu-id="251e1-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="251e1-114">LeaveDate</span></span>     | <span data-ttu-id="251e1-115">Dato</span><span class="sxs-lookup"><span data-stu-id="251e1-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="251e1-116">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="251e1-116">Properties</span></span>

  | <span data-ttu-id="251e1-117">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="251e1-117">Property Name</span></span>     | <span data-ttu-id="251e1-118">Datatype</span><span class="sxs-lookup"><span data-stu-id="251e1-118">Data Type</span></span> | <span data-ttu-id="251e1-119">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="251e1-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="251e1-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="251e1-120">dataAreaId</span></span>        | <span data-ttu-id="251e1-121">Streng</span><span class="sxs-lookup"><span data-stu-id="251e1-121">String</span></span>    | <span data-ttu-id="251e1-122">X</span><span class="sxs-lookup"><span data-stu-id="251e1-122">X</span></span>        |
  | <span data-ttu-id="251e1-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="251e1-123">RequestId</span></span>         | <span data-ttu-id="251e1-124">Streng</span><span class="sxs-lookup"><span data-stu-id="251e1-124">String</span></span>    | <span data-ttu-id="251e1-125">X</span><span class="sxs-lookup"><span data-stu-id="251e1-125">X</span></span>        |
  | <span data-ttu-id="251e1-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="251e1-126">LeaveType</span></span>         | <span data-ttu-id="251e1-127">Streng</span><span class="sxs-lookup"><span data-stu-id="251e1-127">String</span></span>    | <span data-ttu-id="251e1-128">X</span><span class="sxs-lookup"><span data-stu-id="251e1-128">X</span></span>        |
  | <span data-ttu-id="251e1-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="251e1-129">LeaveDate</span></span>         | <span data-ttu-id="251e1-130">Dato</span><span class="sxs-lookup"><span data-stu-id="251e1-130">Date</span></span>      | <span data-ttu-id="251e1-131">X</span><span class="sxs-lookup"><span data-stu-id="251e1-131">X</span></span>        |
  | <span data-ttu-id="251e1-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="251e1-132">ReasonCodeId</span></span>      | <span data-ttu-id="251e1-133">Streng</span><span class="sxs-lookup"><span data-stu-id="251e1-133">String</span></span>    |          |
  | <span data-ttu-id="251e1-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="251e1-134">PersonnelNumber</span></span>   | <span data-ttu-id="251e1-135">Streng</span><span class="sxs-lookup"><span data-stu-id="251e1-135">String</span></span>    | <span data-ttu-id="251e1-136">X</span><span class="sxs-lookup"><span data-stu-id="251e1-136">X</span></span>        |
  | <span data-ttu-id="251e1-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="251e1-137">RequestDate</span></span>       | <span data-ttu-id="251e1-138">Dato</span><span class="sxs-lookup"><span data-stu-id="251e1-138">Date</span></span>      | <span data-ttu-id="251e1-139">X</span><span class="sxs-lookup"><span data-stu-id="251e1-139">X</span></span>        |
  | <span data-ttu-id="251e1-140">Kommentar</span><span class="sxs-lookup"><span data-stu-id="251e1-140">Comment</span></span>           | <span data-ttu-id="251e1-141">Streng</span><span class="sxs-lookup"><span data-stu-id="251e1-141">String</span></span>    |          |
  | <span data-ttu-id="251e1-142">Status</span><span class="sxs-lookup"><span data-stu-id="251e1-142">Status</span></span>            | <span data-ttu-id="251e1-143">Fasttekst</span><span class="sxs-lookup"><span data-stu-id="251e1-143">Enum</span></span>      | <span data-ttu-id="251e1-144">X</span><span class="sxs-lookup"><span data-stu-id="251e1-144">X</span></span>        |
  | <span data-ttu-id="251e1-145">Beløb</span><span class="sxs-lookup"><span data-stu-id="251e1-145">Amount</span></span>            | <span data-ttu-id="251e1-146">Kommatal</span><span class="sxs-lookup"><span data-stu-id="251e1-146">Real</span></span>      |          |
  | <span data-ttu-id="251e1-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="251e1-147">HalfDayDefinition</span></span> | <span data-ttu-id="251e1-148">Fasttekst</span><span class="sxs-lookup"><span data-stu-id="251e1-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="251e1-149">Handlinger</span><span class="sxs-lookup"><span data-stu-id="251e1-149">Actions</span></span>

 | <span data-ttu-id="251e1-150">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="251e1-150">Action Name</span></span>                               | <span data-ttu-id="251e1-151">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="251e1-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="251e1-152">indsend</span><span class="sxs-lookup"><span data-stu-id="251e1-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="251e1-153">Send den anmodning, der skal behandles af arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="251e1-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="251e1-154">Se også</span><span class="sxs-lookup"><span data-stu-id="251e1-154">See also</span></span>

- [<span data-ttu-id="251e1-155">Sende en orlovsanmodning til arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="251e1-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="251e1-156">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="251e1-156">Authentication</span></span>](hr-developer-api-authentication.md)