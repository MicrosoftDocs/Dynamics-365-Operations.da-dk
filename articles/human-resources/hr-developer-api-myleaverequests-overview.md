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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803627"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="f0fb3-103">Oversigt over MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="f0fb3-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f0fb3-104">MyLeaveRequests-enheden i Microsoft Dynamics 365 Human Resources indeholder listen over orlovsanmodninger i systemet, beregnet (begrænset) til de anmodninger, der er tilgængelige for den aktuelle bruger, der forespørger om enheden.</span><span class="sxs-lookup"><span data-stu-id="f0fb3-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="f0fb3-105">Nøgle</span><span class="sxs-lookup"><span data-stu-id="f0fb3-105">Key</span></span>

  | <span data-ttu-id="f0fb3-106">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="f0fb3-106">Property Name</span></span> | <span data-ttu-id="f0fb3-107">Datatype</span><span class="sxs-lookup"><span data-stu-id="f0fb3-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="f0fb3-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="f0fb3-108">dataAreaId</span></span>    | <span data-ttu-id="f0fb3-109">Streng</span><span class="sxs-lookup"><span data-stu-id="f0fb3-109">String</span></span>    |
  | <span data-ttu-id="f0fb3-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="f0fb3-110">RequestId</span></span>     | <span data-ttu-id="f0fb3-111">Streng</span><span class="sxs-lookup"><span data-stu-id="f0fb3-111">String</span></span>    |
  | <span data-ttu-id="f0fb3-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="f0fb3-112">LeaveType</span></span>     | <span data-ttu-id="f0fb3-113">Streng</span><span class="sxs-lookup"><span data-stu-id="f0fb3-113">String</span></span>    |
  | <span data-ttu-id="f0fb3-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="f0fb3-114">LeaveDate</span></span>     | <span data-ttu-id="f0fb3-115">Dato</span><span class="sxs-lookup"><span data-stu-id="f0fb3-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="f0fb3-116">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="f0fb3-116">Properties</span></span>

  | <span data-ttu-id="f0fb3-117">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="f0fb3-117">Property Name</span></span>     | <span data-ttu-id="f0fb3-118">Datatype</span><span class="sxs-lookup"><span data-stu-id="f0fb3-118">Data Type</span></span> | <span data-ttu-id="f0fb3-119">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="f0fb3-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="f0fb3-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="f0fb3-120">dataAreaId</span></span>        | <span data-ttu-id="f0fb3-121">Streng</span><span class="sxs-lookup"><span data-stu-id="f0fb3-121">String</span></span>    | <span data-ttu-id="f0fb3-122">X</span><span class="sxs-lookup"><span data-stu-id="f0fb3-122">X</span></span>        |
  | <span data-ttu-id="f0fb3-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="f0fb3-123">RequestId</span></span>         | <span data-ttu-id="f0fb3-124">Streng</span><span class="sxs-lookup"><span data-stu-id="f0fb3-124">String</span></span>    | <span data-ttu-id="f0fb3-125">X</span><span class="sxs-lookup"><span data-stu-id="f0fb3-125">X</span></span>        |
  | <span data-ttu-id="f0fb3-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="f0fb3-126">LeaveType</span></span>         | <span data-ttu-id="f0fb3-127">Streng</span><span class="sxs-lookup"><span data-stu-id="f0fb3-127">String</span></span>    | <span data-ttu-id="f0fb3-128">X</span><span class="sxs-lookup"><span data-stu-id="f0fb3-128">X</span></span>        |
  | <span data-ttu-id="f0fb3-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="f0fb3-129">LeaveDate</span></span>         | <span data-ttu-id="f0fb3-130">Dato</span><span class="sxs-lookup"><span data-stu-id="f0fb3-130">Date</span></span>      | <span data-ttu-id="f0fb3-131">X</span><span class="sxs-lookup"><span data-stu-id="f0fb3-131">X</span></span>        |
  | <span data-ttu-id="f0fb3-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="f0fb3-132">ReasonCodeId</span></span>      | <span data-ttu-id="f0fb3-133">Streng</span><span class="sxs-lookup"><span data-stu-id="f0fb3-133">String</span></span>    |          |
  | <span data-ttu-id="f0fb3-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="f0fb3-134">PersonnelNumber</span></span>   | <span data-ttu-id="f0fb3-135">Streng</span><span class="sxs-lookup"><span data-stu-id="f0fb3-135">String</span></span>    | <span data-ttu-id="f0fb3-136">X</span><span class="sxs-lookup"><span data-stu-id="f0fb3-136">X</span></span>        |
  | <span data-ttu-id="f0fb3-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="f0fb3-137">RequestDate</span></span>       | <span data-ttu-id="f0fb3-138">Dato</span><span class="sxs-lookup"><span data-stu-id="f0fb3-138">Date</span></span>      | <span data-ttu-id="f0fb3-139">X</span><span class="sxs-lookup"><span data-stu-id="f0fb3-139">X</span></span>        |
  | <span data-ttu-id="f0fb3-140">Kommentar</span><span class="sxs-lookup"><span data-stu-id="f0fb3-140">Comment</span></span>           | <span data-ttu-id="f0fb3-141">Streng</span><span class="sxs-lookup"><span data-stu-id="f0fb3-141">String</span></span>    |          |
  | <span data-ttu-id="f0fb3-142">Status</span><span class="sxs-lookup"><span data-stu-id="f0fb3-142">Status</span></span>            | <span data-ttu-id="f0fb3-143">Fasttekst</span><span class="sxs-lookup"><span data-stu-id="f0fb3-143">Enum</span></span>      | <span data-ttu-id="f0fb3-144">X</span><span class="sxs-lookup"><span data-stu-id="f0fb3-144">X</span></span>        |
  | <span data-ttu-id="f0fb3-145">Beløb</span><span class="sxs-lookup"><span data-stu-id="f0fb3-145">Amount</span></span>            | <span data-ttu-id="f0fb3-146">Kommatal</span><span class="sxs-lookup"><span data-stu-id="f0fb3-146">Real</span></span>      |          |
  | <span data-ttu-id="f0fb3-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="f0fb3-147">HalfDayDefinition</span></span> | <span data-ttu-id="f0fb3-148">Fasttekst</span><span class="sxs-lookup"><span data-stu-id="f0fb3-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="f0fb3-149">Handlinger</span><span class="sxs-lookup"><span data-stu-id="f0fb3-149">Actions</span></span>

 | <span data-ttu-id="f0fb3-150">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="f0fb3-150">Action Name</span></span>                               | <span data-ttu-id="f0fb3-151">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f0fb3-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="f0fb3-152">indsend</span><span class="sxs-lookup"><span data-stu-id="f0fb3-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="f0fb3-153">Send den anmodning, der skal behandles af arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="f0fb3-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f0fb3-154">Se også</span><span class="sxs-lookup"><span data-stu-id="f0fb3-154">See also</span></span>

- [<span data-ttu-id="f0fb3-155">Sende en orlovsanmodning til arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="f0fb3-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="f0fb3-156">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="f0fb3-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]