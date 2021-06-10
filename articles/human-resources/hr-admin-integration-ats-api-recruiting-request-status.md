---
title: Status for rekrutteringsanmodning
description: Dette emne beskriver den status for rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059178"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="7859d-103">Status for rekrutteringsanmodning</span><span class="sxs-lookup"><span data-stu-id="7859d-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7859d-104">Dette emne beskriver den status for rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7859d-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="7859d-105">Fysisk navn: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="7859d-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="7859d-106">Denne fasttekst indeholder den indstilling, der er angivet for statusværdier for en rekrutteringsanmodning.</span><span class="sxs-lookup"><span data-stu-id="7859d-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="7859d-107">Værdi</span><span class="sxs-lookup"><span data-stu-id="7859d-107">Value</span></span> | <span data-ttu-id="7859d-108">Mærkat</span><span class="sxs-lookup"><span data-stu-id="7859d-108">Label</span></span> | <span data-ttu-id="7859d-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="7859d-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7859d-110">200000000</span><span class="sxs-lookup"><span data-stu-id="7859d-110">200000000</span></span> | <span data-ttu-id="7859d-111">Udkast</span><span class="sxs-lookup"><span data-stu-id="7859d-111">Draft</span></span> | <span data-ttu-id="7859d-112">Anmodningen er kladde og klar til aktiv rekruttering.</span><span class="sxs-lookup"><span data-stu-id="7859d-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="7859d-113">200000001</span><span class="sxs-lookup"><span data-stu-id="7859d-113">200000001</span></span> | <span data-ttu-id="7859d-114">Til gennemsyn</span><span class="sxs-lookup"><span data-stu-id="7859d-114">In Review</span></span> | <span data-ttu-id="7859d-115">Anmodningen er sendt og dirigeres til godkendelse via arbejdsflow.</span><span class="sxs-lookup"><span data-stu-id="7859d-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="7859d-116">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="7859d-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="7859d-117">200000002</span><span class="sxs-lookup"><span data-stu-id="7859d-117">200000002</span></span> | <span data-ttu-id="7859d-118">Udestående</span><span class="sxs-lookup"><span data-stu-id="7859d-118">Pending</span></span> | <span data-ttu-id="7859d-119">Anmodningen afventer en arbejdsflowhandling.</span><span class="sxs-lookup"><span data-stu-id="7859d-119">The request is pending workflow action.</span></span> <span data-ttu-id="7859d-120">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="7859d-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="7859d-121">200000003</span><span class="sxs-lookup"><span data-stu-id="7859d-121">200000003</span></span> | <span data-ttu-id="7859d-122">Annulleret</span><span class="sxs-lookup"><span data-stu-id="7859d-122">Canceled</span></span> | <span data-ttu-id="7859d-123">Anmodningen blev annulleret.</span><span class="sxs-lookup"><span data-stu-id="7859d-123">The request has been canceled.</span></span> <span data-ttu-id="7859d-124">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="7859d-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="7859d-125">200000004</span><span class="sxs-lookup"><span data-stu-id="7859d-125">200000004</span></span> | <span data-ttu-id="7859d-126">Afvist</span><span class="sxs-lookup"><span data-stu-id="7859d-126">Denied</span></span> | <span data-ttu-id="7859d-127">Anmodningen er ikke godkendt.</span><span class="sxs-lookup"><span data-stu-id="7859d-127">The request has been denied.</span></span> <span data-ttu-id="7859d-128">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="7859d-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="7859d-129">200000005</span><span class="sxs-lookup"><span data-stu-id="7859d-129">200000005</span></span> | <span data-ttu-id="7859d-130">Aktive</span><span class="sxs-lookup"><span data-stu-id="7859d-130">Active</span></span> | <span data-ttu-id="7859d-131">Alle arbejdsflow er fuldført og godkendt, og anmodningen er klar til aktiv rekruttering.</span><span class="sxs-lookup"><span data-stu-id="7859d-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="7859d-132">200000006</span><span class="sxs-lookup"><span data-stu-id="7859d-132">200000006</span></span> | <span data-ttu-id="7859d-133">Lukkede</span><span class="sxs-lookup"><span data-stu-id="7859d-133">Closed</span></span> | <span data-ttu-id="7859d-134">Rekrutteringsanmodningen er lukket.</span><span class="sxs-lookup"><span data-stu-id="7859d-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7859d-135">Se også</span><span class="sxs-lookup"><span data-stu-id="7859d-135">See also</span></span>

[<span data-ttu-id="7859d-136">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="7859d-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="7859d-137">Eksempelforespørgsel til anmodning om rekruttering</span><span class="sxs-lookup"><span data-stu-id="7859d-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]