---
title: Oversigt over MyLeaveRequests
description: ''
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008483"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="e905c-102">Oversigt over MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="e905c-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="e905c-103">MyLeaveRequests-enheden i Microsoft Dynamics 365 Human Resources indeholder listen over orlovsanmodninger i systemet, beregnet (begrænset) til de anmodninger, der er tilgængelige for den aktuelle bruger, der forespørger om enheden.</span><span class="sxs-lookup"><span data-stu-id="e905c-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="e905c-104">Nøgle</span><span class="sxs-lookup"><span data-stu-id="e905c-104">Key</span></span>

  | <span data-ttu-id="e905c-105">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="e905c-105">Property Name</span></span> | <span data-ttu-id="e905c-106">Datatype</span><span class="sxs-lookup"><span data-stu-id="e905c-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="e905c-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="e905c-107">dataAreaId</span></span>    | <span data-ttu-id="e905c-108">Streng</span><span class="sxs-lookup"><span data-stu-id="e905c-108">String</span></span>    |
  | <span data-ttu-id="e905c-109">RequestId</span><span class="sxs-lookup"><span data-stu-id="e905c-109">RequestId</span></span>     | <span data-ttu-id="e905c-110">Streng</span><span class="sxs-lookup"><span data-stu-id="e905c-110">String</span></span>    |
  | <span data-ttu-id="e905c-111">LeaveType</span><span class="sxs-lookup"><span data-stu-id="e905c-111">LeaveType</span></span>     | <span data-ttu-id="e905c-112">Streng</span><span class="sxs-lookup"><span data-stu-id="e905c-112">String</span></span>    |
  | <span data-ttu-id="e905c-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="e905c-113">LeaveDate</span></span>     | <span data-ttu-id="e905c-114">Dato</span><span class="sxs-lookup"><span data-stu-id="e905c-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="e905c-115">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="e905c-115">Properties</span></span>

  | <span data-ttu-id="e905c-116">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="e905c-116">Property Name</span></span>     | <span data-ttu-id="e905c-117">Datatype</span><span class="sxs-lookup"><span data-stu-id="e905c-117">Data Type</span></span> | <span data-ttu-id="e905c-118">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="e905c-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="e905c-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="e905c-119">dataAreaId</span></span>        | <span data-ttu-id="e905c-120">Streng</span><span class="sxs-lookup"><span data-stu-id="e905c-120">String</span></span>    | <span data-ttu-id="e905c-121">X</span><span class="sxs-lookup"><span data-stu-id="e905c-121">X</span></span>        |
  | <span data-ttu-id="e905c-122">RequestId</span><span class="sxs-lookup"><span data-stu-id="e905c-122">RequestId</span></span>         | <span data-ttu-id="e905c-123">Streng</span><span class="sxs-lookup"><span data-stu-id="e905c-123">String</span></span>    | <span data-ttu-id="e905c-124">X</span><span class="sxs-lookup"><span data-stu-id="e905c-124">X</span></span>        |
  | <span data-ttu-id="e905c-125">LeaveType</span><span class="sxs-lookup"><span data-stu-id="e905c-125">LeaveType</span></span>         | <span data-ttu-id="e905c-126">Streng</span><span class="sxs-lookup"><span data-stu-id="e905c-126">String</span></span>    | <span data-ttu-id="e905c-127">X</span><span class="sxs-lookup"><span data-stu-id="e905c-127">X</span></span>        |
  | <span data-ttu-id="e905c-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="e905c-128">LeaveDate</span></span>         | <span data-ttu-id="e905c-129">Dato</span><span class="sxs-lookup"><span data-stu-id="e905c-129">Date</span></span>      | <span data-ttu-id="e905c-130">X</span><span class="sxs-lookup"><span data-stu-id="e905c-130">X</span></span>        |
  | <span data-ttu-id="e905c-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="e905c-131">ReasonCodeId</span></span>      | <span data-ttu-id="e905c-132">Streng</span><span class="sxs-lookup"><span data-stu-id="e905c-132">String</span></span>    |          |
  | <span data-ttu-id="e905c-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="e905c-133">PersonnelNumber</span></span>   | <span data-ttu-id="e905c-134">Streng</span><span class="sxs-lookup"><span data-stu-id="e905c-134">String</span></span>    | <span data-ttu-id="e905c-135">X</span><span class="sxs-lookup"><span data-stu-id="e905c-135">X</span></span>        |
  | <span data-ttu-id="e905c-136">RequestDate</span><span class="sxs-lookup"><span data-stu-id="e905c-136">RequestDate</span></span>       | <span data-ttu-id="e905c-137">Dato</span><span class="sxs-lookup"><span data-stu-id="e905c-137">Date</span></span>      | <span data-ttu-id="e905c-138">X</span><span class="sxs-lookup"><span data-stu-id="e905c-138">X</span></span>        |
  | <span data-ttu-id="e905c-139">Kommentar</span><span class="sxs-lookup"><span data-stu-id="e905c-139">Comment</span></span>           | <span data-ttu-id="e905c-140">Streng</span><span class="sxs-lookup"><span data-stu-id="e905c-140">String</span></span>    |          |
  | <span data-ttu-id="e905c-141">Status</span><span class="sxs-lookup"><span data-stu-id="e905c-141">Status</span></span>            | <span data-ttu-id="e905c-142">Fasttekst</span><span class="sxs-lookup"><span data-stu-id="e905c-142">Enum</span></span>      | <span data-ttu-id="e905c-143">X</span><span class="sxs-lookup"><span data-stu-id="e905c-143">X</span></span>        |
  | <span data-ttu-id="e905c-144">Beløb</span><span class="sxs-lookup"><span data-stu-id="e905c-144">Amount</span></span>            | <span data-ttu-id="e905c-145">Kommatal</span><span class="sxs-lookup"><span data-stu-id="e905c-145">Real</span></span>      |          |
  | <span data-ttu-id="e905c-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="e905c-146">HalfDayDefinition</span></span> | <span data-ttu-id="e905c-147">Fasttekst</span><span class="sxs-lookup"><span data-stu-id="e905c-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="e905c-148">Handlinger</span><span class="sxs-lookup"><span data-stu-id="e905c-148">Actions</span></span>

 | <span data-ttu-id="e905c-149">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="e905c-149">Action Name</span></span>                               | <span data-ttu-id="e905c-150">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e905c-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="e905c-151">indsend</span><span class="sxs-lookup"><span data-stu-id="e905c-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="e905c-152">Send den anmodning, der skal behandles af arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="e905c-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e905c-153">Se også</span><span class="sxs-lookup"><span data-stu-id="e905c-153">See also</span></span>

- [<span data-ttu-id="e905c-154">Sende en orlovsanmodning til arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="e905c-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="e905c-155">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="e905c-155">Authentication</span></span>](hr-developer-api-authentication.md)