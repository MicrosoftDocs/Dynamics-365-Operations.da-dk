---
title: Status for rekrutteringsanmodning
description: Dette emne beskriver den status for rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0032e6bfdbfd2792dafda8bf24a1b0cbc551740d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464640"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="27fd3-103">Status for rekrutteringsanmodning</span><span class="sxs-lookup"><span data-stu-id="27fd3-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="27fd3-104">Dette emne beskriver den status for rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="27fd3-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="27fd3-105">Fysisk navn: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="27fd3-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="27fd3-106">Denne fasttekst indeholder den indstilling, der er angivet for statusværdier for en rekrutteringsanmodning.</span><span class="sxs-lookup"><span data-stu-id="27fd3-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="27fd3-107">Værdi</span><span class="sxs-lookup"><span data-stu-id="27fd3-107">Value</span></span> | <span data-ttu-id="27fd3-108">Mærkat</span><span class="sxs-lookup"><span data-stu-id="27fd3-108">Label</span></span> | <span data-ttu-id="27fd3-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="27fd3-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="27fd3-110">200000000</span><span class="sxs-lookup"><span data-stu-id="27fd3-110">200000000</span></span> | <span data-ttu-id="27fd3-111">Udkast</span><span class="sxs-lookup"><span data-stu-id="27fd3-111">Draft</span></span> | <span data-ttu-id="27fd3-112">Anmodningen er kladde og klar til aktiv rekruttering.</span><span class="sxs-lookup"><span data-stu-id="27fd3-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="27fd3-113">200000001</span><span class="sxs-lookup"><span data-stu-id="27fd3-113">200000001</span></span> | <span data-ttu-id="27fd3-114">Til gennemsyn</span><span class="sxs-lookup"><span data-stu-id="27fd3-114">In Review</span></span> | <span data-ttu-id="27fd3-115">Anmodningen er sendt og dirigeres til godkendelse via arbejdsflow.</span><span class="sxs-lookup"><span data-stu-id="27fd3-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="27fd3-116">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="27fd3-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="27fd3-117">200000002</span><span class="sxs-lookup"><span data-stu-id="27fd3-117">200000002</span></span> | <span data-ttu-id="27fd3-118">Udestående</span><span class="sxs-lookup"><span data-stu-id="27fd3-118">Pending</span></span> | <span data-ttu-id="27fd3-119">Anmodningen afventer en arbejdsflowhandling.</span><span class="sxs-lookup"><span data-stu-id="27fd3-119">The request is pending workflow action.</span></span> <span data-ttu-id="27fd3-120">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="27fd3-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="27fd3-121">200000003</span><span class="sxs-lookup"><span data-stu-id="27fd3-121">200000003</span></span> | <span data-ttu-id="27fd3-122">Annulleret</span><span class="sxs-lookup"><span data-stu-id="27fd3-122">Canceled</span></span> | <span data-ttu-id="27fd3-123">Anmodningen blev annulleret.</span><span class="sxs-lookup"><span data-stu-id="27fd3-123">The request has been canceled.</span></span> <span data-ttu-id="27fd3-124">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="27fd3-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="27fd3-125">200000004</span><span class="sxs-lookup"><span data-stu-id="27fd3-125">200000004</span></span> | <span data-ttu-id="27fd3-126">Afvist</span><span class="sxs-lookup"><span data-stu-id="27fd3-126">Denied</span></span> | <span data-ttu-id="27fd3-127">Anmodningen er ikke godkendt.</span><span class="sxs-lookup"><span data-stu-id="27fd3-127">The request has been denied.</span></span> <span data-ttu-id="27fd3-128">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="27fd3-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="27fd3-129">200000005</span><span class="sxs-lookup"><span data-stu-id="27fd3-129">200000005</span></span> | <span data-ttu-id="27fd3-130">Aktive</span><span class="sxs-lookup"><span data-stu-id="27fd3-130">Active</span></span> | <span data-ttu-id="27fd3-131">Alle arbejdsflow er fuldført og godkendt, og anmodningen er klar til aktiv rekruttering.</span><span class="sxs-lookup"><span data-stu-id="27fd3-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="27fd3-132">200000006</span><span class="sxs-lookup"><span data-stu-id="27fd3-132">200000006</span></span> | <span data-ttu-id="27fd3-133">Lukkede</span><span class="sxs-lookup"><span data-stu-id="27fd3-133">Closed</span></span> | <span data-ttu-id="27fd3-134">Rekrutteringsanmodningen er lukket.</span><span class="sxs-lookup"><span data-stu-id="27fd3-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="27fd3-135">Se også</span><span class="sxs-lookup"><span data-stu-id="27fd3-135">See also</span></span>

[<span data-ttu-id="27fd3-136">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="27fd3-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="27fd3-137">Eksempelforespørgsel til anmodning om rekruttering</span><span class="sxs-lookup"><span data-stu-id="27fd3-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]