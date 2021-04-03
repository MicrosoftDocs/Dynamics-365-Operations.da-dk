---
title: Oversigt over MyLeaveRequests
description: MyLeaveRequests-enheden i Microsoft Dynamics 365 Human Resources indeholder listen over orlovsanmodninger i systemet, beregnet (begrænset) til de anmodninger, der er tilgængelige for den aktuelle bruger, der forespørger om enheden.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465504"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="0c759-103">Oversigt over MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="0c759-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0c759-104">MyLeaveRequests-enheden i Microsoft Dynamics 365 Human Resources indeholder listen over orlovsanmodninger i systemet, beregnet (begrænset) til de anmodninger, der er tilgængelige for den aktuelle bruger, der forespørger om enheden.</span><span class="sxs-lookup"><span data-stu-id="0c759-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="0c759-105">Nøgle</span><span class="sxs-lookup"><span data-stu-id="0c759-105">Key</span></span>

  | <span data-ttu-id="0c759-106">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="0c759-106">Property Name</span></span> | <span data-ttu-id="0c759-107">Datatype</span><span class="sxs-lookup"><span data-stu-id="0c759-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="0c759-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="0c759-108">dataAreaId</span></span>    | <span data-ttu-id="0c759-109">Streng</span><span class="sxs-lookup"><span data-stu-id="0c759-109">String</span></span>    |
  | <span data-ttu-id="0c759-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="0c759-110">RequestId</span></span>     | <span data-ttu-id="0c759-111">Streng</span><span class="sxs-lookup"><span data-stu-id="0c759-111">String</span></span>    |
  | <span data-ttu-id="0c759-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="0c759-112">LeaveType</span></span>     | <span data-ttu-id="0c759-113">Streng</span><span class="sxs-lookup"><span data-stu-id="0c759-113">String</span></span>    |
  | <span data-ttu-id="0c759-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="0c759-114">LeaveDate</span></span>     | <span data-ttu-id="0c759-115">Dato</span><span class="sxs-lookup"><span data-stu-id="0c759-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="0c759-116">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="0c759-116">Properties</span></span>

  | <span data-ttu-id="0c759-117">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="0c759-117">Property Name</span></span>     | <span data-ttu-id="0c759-118">Datatype</span><span class="sxs-lookup"><span data-stu-id="0c759-118">Data Type</span></span> | <span data-ttu-id="0c759-119">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="0c759-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="0c759-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="0c759-120">dataAreaId</span></span>        | <span data-ttu-id="0c759-121">Streng</span><span class="sxs-lookup"><span data-stu-id="0c759-121">String</span></span>    | <span data-ttu-id="0c759-122">X</span><span class="sxs-lookup"><span data-stu-id="0c759-122">X</span></span>        |
  | <span data-ttu-id="0c759-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="0c759-123">RequestId</span></span>         | <span data-ttu-id="0c759-124">Streng</span><span class="sxs-lookup"><span data-stu-id="0c759-124">String</span></span>    | <span data-ttu-id="0c759-125">X</span><span class="sxs-lookup"><span data-stu-id="0c759-125">X</span></span>        |
  | <span data-ttu-id="0c759-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="0c759-126">LeaveType</span></span>         | <span data-ttu-id="0c759-127">Streng</span><span class="sxs-lookup"><span data-stu-id="0c759-127">String</span></span>    | <span data-ttu-id="0c759-128">X</span><span class="sxs-lookup"><span data-stu-id="0c759-128">X</span></span>        |
  | <span data-ttu-id="0c759-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="0c759-129">LeaveDate</span></span>         | <span data-ttu-id="0c759-130">Dato</span><span class="sxs-lookup"><span data-stu-id="0c759-130">Date</span></span>      | <span data-ttu-id="0c759-131">X</span><span class="sxs-lookup"><span data-stu-id="0c759-131">X</span></span>        |
  | <span data-ttu-id="0c759-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="0c759-132">ReasonCodeId</span></span>      | <span data-ttu-id="0c759-133">Streng</span><span class="sxs-lookup"><span data-stu-id="0c759-133">String</span></span>    |          |
  | <span data-ttu-id="0c759-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="0c759-134">PersonnelNumber</span></span>   | <span data-ttu-id="0c759-135">Streng</span><span class="sxs-lookup"><span data-stu-id="0c759-135">String</span></span>    | <span data-ttu-id="0c759-136">X</span><span class="sxs-lookup"><span data-stu-id="0c759-136">X</span></span>        |
  | <span data-ttu-id="0c759-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="0c759-137">RequestDate</span></span>       | <span data-ttu-id="0c759-138">Dato</span><span class="sxs-lookup"><span data-stu-id="0c759-138">Date</span></span>      | <span data-ttu-id="0c759-139">X</span><span class="sxs-lookup"><span data-stu-id="0c759-139">X</span></span>        |
  | <span data-ttu-id="0c759-140">Kommentar</span><span class="sxs-lookup"><span data-stu-id="0c759-140">Comment</span></span>           | <span data-ttu-id="0c759-141">Streng</span><span class="sxs-lookup"><span data-stu-id="0c759-141">String</span></span>    |          |
  | <span data-ttu-id="0c759-142">Status</span><span class="sxs-lookup"><span data-stu-id="0c759-142">Status</span></span>            | <span data-ttu-id="0c759-143">Fasttekst</span><span class="sxs-lookup"><span data-stu-id="0c759-143">Enum</span></span>      | <span data-ttu-id="0c759-144">X</span><span class="sxs-lookup"><span data-stu-id="0c759-144">X</span></span>        |
  | <span data-ttu-id="0c759-145">Beløb</span><span class="sxs-lookup"><span data-stu-id="0c759-145">Amount</span></span>            | <span data-ttu-id="0c759-146">Kommatal</span><span class="sxs-lookup"><span data-stu-id="0c759-146">Real</span></span>      |          |
  | <span data-ttu-id="0c759-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="0c759-147">HalfDayDefinition</span></span> | <span data-ttu-id="0c759-148">Fasttekst</span><span class="sxs-lookup"><span data-stu-id="0c759-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="0c759-149">Handlinger</span><span class="sxs-lookup"><span data-stu-id="0c759-149">Actions</span></span>

 | <span data-ttu-id="0c759-150">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="0c759-150">Action Name</span></span>                               | <span data-ttu-id="0c759-151">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0c759-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="0c759-152">indsend</span><span class="sxs-lookup"><span data-stu-id="0c759-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="0c759-153">Send den anmodning, der skal behandles af arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="0c759-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0c759-154">Se også</span><span class="sxs-lookup"><span data-stu-id="0c759-154">See also</span></span>

- [<span data-ttu-id="0c759-155">Sende en orlovsanmodning til arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="0c759-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="0c759-156">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="0c759-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]