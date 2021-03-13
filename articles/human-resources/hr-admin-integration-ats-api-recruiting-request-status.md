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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125948"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="d56bf-103">Status for rekrutteringsanmodning</span><span class="sxs-lookup"><span data-stu-id="d56bf-103">Recruiting request status</span></span>

<span data-ttu-id="d56bf-104">Dette emne beskriver den status for rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d56bf-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="d56bf-105">Fysisk navn: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="d56bf-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="d56bf-106">Denne fasttekst indeholder den indstilling, der er angivet for statusværdier for en rekrutteringsanmodning.</span><span class="sxs-lookup"><span data-stu-id="d56bf-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="d56bf-107">Værdi</span><span class="sxs-lookup"><span data-stu-id="d56bf-107">Value</span></span> | <span data-ttu-id="d56bf-108">Mærkat</span><span class="sxs-lookup"><span data-stu-id="d56bf-108">Label</span></span> | <span data-ttu-id="d56bf-109">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="d56bf-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d56bf-110">200000000</span><span class="sxs-lookup"><span data-stu-id="d56bf-110">200000000</span></span> | <span data-ttu-id="d56bf-111">Udkast</span><span class="sxs-lookup"><span data-stu-id="d56bf-111">Draft</span></span> | <span data-ttu-id="d56bf-112">Anmodningen er kladde og klar til aktiv rekruttering.</span><span class="sxs-lookup"><span data-stu-id="d56bf-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="d56bf-113">200000001</span><span class="sxs-lookup"><span data-stu-id="d56bf-113">200000001</span></span> | <span data-ttu-id="d56bf-114">Til gennemsyn</span><span class="sxs-lookup"><span data-stu-id="d56bf-114">In Review</span></span> | <span data-ttu-id="d56bf-115">Anmodningen er sendt og dirigeres til godkendelse via arbejdsflow.</span><span class="sxs-lookup"><span data-stu-id="d56bf-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="d56bf-116">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="d56bf-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="d56bf-117">200000002</span><span class="sxs-lookup"><span data-stu-id="d56bf-117">200000002</span></span> | <span data-ttu-id="d56bf-118">Udestående</span><span class="sxs-lookup"><span data-stu-id="d56bf-118">Pending</span></span> | <span data-ttu-id="d56bf-119">Anmodningen afventer en arbejdsflowhandling.</span><span class="sxs-lookup"><span data-stu-id="d56bf-119">The request is pending workflow action.</span></span> <span data-ttu-id="d56bf-120">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="d56bf-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="d56bf-121">200000003</span><span class="sxs-lookup"><span data-stu-id="d56bf-121">200000003</span></span> | <span data-ttu-id="d56bf-122">Annulleret</span><span class="sxs-lookup"><span data-stu-id="d56bf-122">Canceled</span></span> | <span data-ttu-id="d56bf-123">Anmodningen blev annulleret.</span><span class="sxs-lookup"><span data-stu-id="d56bf-123">The request has been canceled.</span></span> <span data-ttu-id="d56bf-124">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="d56bf-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="d56bf-125">200000004</span><span class="sxs-lookup"><span data-stu-id="d56bf-125">200000004</span></span> | <span data-ttu-id="d56bf-126">Afvist</span><span class="sxs-lookup"><span data-stu-id="d56bf-126">Denied</span></span> | <span data-ttu-id="d56bf-127">Anmodningen er ikke godkendt.</span><span class="sxs-lookup"><span data-stu-id="d56bf-127">The request has been denied.</span></span> <span data-ttu-id="d56bf-128">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="d56bf-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="d56bf-129">200000005</span><span class="sxs-lookup"><span data-stu-id="d56bf-129">200000005</span></span> | <span data-ttu-id="d56bf-130">Aktive</span><span class="sxs-lookup"><span data-stu-id="d56bf-130">Active</span></span> | <span data-ttu-id="d56bf-131">Alle arbejdsflow er fuldført og godkendt, og anmodningen er klar til aktiv rekruttering.</span><span class="sxs-lookup"><span data-stu-id="d56bf-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="d56bf-132">200000006</span><span class="sxs-lookup"><span data-stu-id="d56bf-132">200000006</span></span> | <span data-ttu-id="d56bf-133">Lukkede</span><span class="sxs-lookup"><span data-stu-id="d56bf-133">Closed</span></span> | <span data-ttu-id="d56bf-134">Rekrutteringsanmodningen er lukket.</span><span class="sxs-lookup"><span data-stu-id="d56bf-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d56bf-135">Se også</span><span class="sxs-lookup"><span data-stu-id="d56bf-135">See also</span></span>

[<span data-ttu-id="d56bf-136">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="d56bf-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="d56bf-137">Eksempelforespørgsel til anmodning om rekruttering</span><span class="sxs-lookup"><span data-stu-id="d56bf-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
