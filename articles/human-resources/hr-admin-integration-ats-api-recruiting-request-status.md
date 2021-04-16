---
title: Status for rekrutteringsanmodning
description: Dette emne beskriver den status for rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 888fbc511bffbecd837c929049006266191da5ba
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5806036"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="e2a6a-103">Status for rekrutteringsanmodning</span><span class="sxs-lookup"><span data-stu-id="e2a6a-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e2a6a-104">Dette emne beskriver den status for rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e2a6a-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="e2a6a-105">Fysisk navn: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="e2a6a-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="e2a6a-106">Denne fasttekst indeholder den indstilling, der er angivet for statusværdier for en rekrutteringsanmodning.</span><span class="sxs-lookup"><span data-stu-id="e2a6a-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="e2a6a-107">Værdi</span><span class="sxs-lookup"><span data-stu-id="e2a6a-107">Value</span></span> | <span data-ttu-id="e2a6a-108">Mærkat</span><span class="sxs-lookup"><span data-stu-id="e2a6a-108">Label</span></span> | <span data-ttu-id="e2a6a-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e2a6a-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e2a6a-110">200000000</span><span class="sxs-lookup"><span data-stu-id="e2a6a-110">200000000</span></span> | <span data-ttu-id="e2a6a-111">Udkast</span><span class="sxs-lookup"><span data-stu-id="e2a6a-111">Draft</span></span> | <span data-ttu-id="e2a6a-112">Anmodningen er kladde og klar til aktiv rekruttering.</span><span class="sxs-lookup"><span data-stu-id="e2a6a-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="e2a6a-113">200000001</span><span class="sxs-lookup"><span data-stu-id="e2a6a-113">200000001</span></span> | <span data-ttu-id="e2a6a-114">Til gennemsyn</span><span class="sxs-lookup"><span data-stu-id="e2a6a-114">In Review</span></span> | <span data-ttu-id="e2a6a-115">Anmodningen er sendt og dirigeres til godkendelse via arbejdsflow.</span><span class="sxs-lookup"><span data-stu-id="e2a6a-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="e2a6a-116">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="e2a6a-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e2a6a-117">200000002</span><span class="sxs-lookup"><span data-stu-id="e2a6a-117">200000002</span></span> | <span data-ttu-id="e2a6a-118">Udestående</span><span class="sxs-lookup"><span data-stu-id="e2a6a-118">Pending</span></span> | <span data-ttu-id="e2a6a-119">Anmodningen afventer en arbejdsflowhandling.</span><span class="sxs-lookup"><span data-stu-id="e2a6a-119">The request is pending workflow action.</span></span> <span data-ttu-id="e2a6a-120">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="e2a6a-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e2a6a-121">200000003</span><span class="sxs-lookup"><span data-stu-id="e2a6a-121">200000003</span></span> | <span data-ttu-id="e2a6a-122">Annulleret</span><span class="sxs-lookup"><span data-stu-id="e2a6a-122">Canceled</span></span> | <span data-ttu-id="e2a6a-123">Anmodningen blev annulleret.</span><span class="sxs-lookup"><span data-stu-id="e2a6a-123">The request has been canceled.</span></span> <span data-ttu-id="e2a6a-124">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="e2a6a-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e2a6a-125">200000004</span><span class="sxs-lookup"><span data-stu-id="e2a6a-125">200000004</span></span> | <span data-ttu-id="e2a6a-126">Afvist</span><span class="sxs-lookup"><span data-stu-id="e2a6a-126">Denied</span></span> | <span data-ttu-id="e2a6a-127">Anmodningen er ikke godkendt.</span><span class="sxs-lookup"><span data-stu-id="e2a6a-127">The request has been denied.</span></span> <span data-ttu-id="e2a6a-128">Kun tilgængelig, når arbejdsflow er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="e2a6a-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e2a6a-129">200000005</span><span class="sxs-lookup"><span data-stu-id="e2a6a-129">200000005</span></span> | <span data-ttu-id="e2a6a-130">Aktive</span><span class="sxs-lookup"><span data-stu-id="e2a6a-130">Active</span></span> | <span data-ttu-id="e2a6a-131">Alle arbejdsflow er fuldført og godkendt, og anmodningen er klar til aktiv rekruttering.</span><span class="sxs-lookup"><span data-stu-id="e2a6a-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="e2a6a-132">200000006</span><span class="sxs-lookup"><span data-stu-id="e2a6a-132">200000006</span></span> | <span data-ttu-id="e2a6a-133">Lukkede</span><span class="sxs-lookup"><span data-stu-id="e2a6a-133">Closed</span></span> | <span data-ttu-id="e2a6a-134">Rekrutteringsanmodningen er lukket.</span><span class="sxs-lookup"><span data-stu-id="e2a6a-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e2a6a-135">Se også</span><span class="sxs-lookup"><span data-stu-id="e2a6a-135">See also</span></span>

[<span data-ttu-id="e2a6a-136">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="e2a6a-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="e2a6a-137">Eksempelforespørgsel til anmodning om rekruttering</span><span class="sxs-lookup"><span data-stu-id="e2a6a-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]