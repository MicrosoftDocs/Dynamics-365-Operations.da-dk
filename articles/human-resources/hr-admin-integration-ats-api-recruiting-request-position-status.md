---
title: Status for rekrutteringsanmodningsstilling
description: Dette emne beskriver status for stillingen i en rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126044"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="05779-103">Status for rekrutteringsanmodningsstilling</span><span class="sxs-lookup"><span data-stu-id="05779-103">Recruiting request position status</span></span>

<span data-ttu-id="05779-104">Dette emne beskriver status for stillingen i en rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="05779-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="05779-105">Fysisk navn: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="05779-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="05779-106">Denne fasttekst indeholder den indstilling, der er angivet for statusværdierne for hver enkelt stilling, en rekrutteringsanmodning i enheden RecruitingRequestPosition.</span><span class="sxs-lookup"><span data-stu-id="05779-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="05779-107">Værdi</span><span class="sxs-lookup"><span data-stu-id="05779-107">Value</span></span> | <span data-ttu-id="05779-108">Mærkat</span><span class="sxs-lookup"><span data-stu-id="05779-108">Label</span></span> | <span data-ttu-id="05779-109">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="05779-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="05779-110">200000000</span><span class="sxs-lookup"><span data-stu-id="05779-110">200000000</span></span> | <span data-ttu-id="05779-111">Åbnet</span><span class="sxs-lookup"><span data-stu-id="05779-111">Open</span></span> | <span data-ttu-id="05779-112">Stillingen i rekrutteringsanmodningen er åben for rekruttering.</span><span class="sxs-lookup"><span data-stu-id="05779-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="05779-113">Det betyder ikke, at der ikke aktuelt er nogen aktiv stillingstildeling for stillingen.</span><span class="sxs-lookup"><span data-stu-id="05779-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="05779-114">Der kan være en medarbejder i stillingen på tidspunktet for rekruttering.</span><span class="sxs-lookup"><span data-stu-id="05779-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="05779-115">Det angiver kun, at stillingen er tilgængelig for rekruttering i forbindelse med rekrutteringsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="05779-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="05779-116">200000001</span><span class="sxs-lookup"><span data-stu-id="05779-116">200000001</span></span> | <span data-ttu-id="05779-117">Besat</span><span class="sxs-lookup"><span data-stu-id="05779-117">Filled</span></span> | <span data-ttu-id="05779-118">Der er valgt en arbejder til tildeling til stillingen.</span><span class="sxs-lookup"><span data-stu-id="05779-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="05779-119">200000002</span><span class="sxs-lookup"><span data-stu-id="05779-119">200000002</span></span> | <span data-ttu-id="05779-120">Annulleret</span><span class="sxs-lookup"><span data-stu-id="05779-120">Canceled</span></span> | <span data-ttu-id="05779-121">Anmodningen om at rekruttere til denne stilling er annulleret.</span><span class="sxs-lookup"><span data-stu-id="05779-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="05779-122">Se også</span><span class="sxs-lookup"><span data-stu-id="05779-122">See also</span></span>

[<span data-ttu-id="05779-123">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="05779-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="05779-124">Eksempelforespørgsel til anmodning om rekruttering</span><span class="sxs-lookup"><span data-stu-id="05779-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
