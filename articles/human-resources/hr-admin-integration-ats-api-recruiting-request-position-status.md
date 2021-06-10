---
title: Status for rekrutteringsanmodningsstilling
description: Dette emne beskriver status for stillingen i en rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.
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
ms.openlocfilehash: e287ec4b9b78194b76ef3c993c6ce32f808e26f9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051875"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="8b899-103">Status for rekrutteringsanmodningsstilling</span><span class="sxs-lookup"><span data-stu-id="8b899-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8b899-104">Dette emne beskriver status for stillingen i en rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8b899-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="8b899-105">Fysisk navn: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="8b899-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="8b899-106">Denne fasttekst indeholder den indstilling, der er angivet for statusværdierne for hver enkelt stilling, en rekrutteringsanmodning i enheden RecruitingRequestPosition.</span><span class="sxs-lookup"><span data-stu-id="8b899-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="8b899-107">Værdi</span><span class="sxs-lookup"><span data-stu-id="8b899-107">Value</span></span> | <span data-ttu-id="8b899-108">Mærkat</span><span class="sxs-lookup"><span data-stu-id="8b899-108">Label</span></span> | <span data-ttu-id="8b899-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="8b899-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8b899-110">200000000</span><span class="sxs-lookup"><span data-stu-id="8b899-110">200000000</span></span> | <span data-ttu-id="8b899-111">Åbnet</span><span class="sxs-lookup"><span data-stu-id="8b899-111">Open</span></span> | <span data-ttu-id="8b899-112">Stillingen i rekrutteringsanmodningen er åben for rekruttering.</span><span class="sxs-lookup"><span data-stu-id="8b899-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="8b899-113">Det betyder ikke, at der ikke aktuelt er nogen aktiv stillingstildeling for stillingen.</span><span class="sxs-lookup"><span data-stu-id="8b899-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="8b899-114">Der kan være en medarbejder i stillingen på tidspunktet for rekruttering.</span><span class="sxs-lookup"><span data-stu-id="8b899-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="8b899-115">Det angiver kun, at stillingen er tilgængelig for rekruttering i forbindelse med rekrutteringsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="8b899-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="8b899-116">200000001</span><span class="sxs-lookup"><span data-stu-id="8b899-116">200000001</span></span> | <span data-ttu-id="8b899-117">Besat</span><span class="sxs-lookup"><span data-stu-id="8b899-117">Filled</span></span> | <span data-ttu-id="8b899-118">Der er valgt en arbejder til tildeling til stillingen.</span><span class="sxs-lookup"><span data-stu-id="8b899-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="8b899-119">200000002</span><span class="sxs-lookup"><span data-stu-id="8b899-119">200000002</span></span> | <span data-ttu-id="8b899-120">Annulleret</span><span class="sxs-lookup"><span data-stu-id="8b899-120">Canceled</span></span> | <span data-ttu-id="8b899-121">Anmodningen om at rekruttere til denne stilling er annulleret.</span><span class="sxs-lookup"><span data-stu-id="8b899-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8b899-122">Se også</span><span class="sxs-lookup"><span data-stu-id="8b899-122">See also</span></span>

[<span data-ttu-id="8b899-123">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="8b899-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="8b899-124">Eksempelforespørgsel til anmodning om rekruttering</span><span class="sxs-lookup"><span data-stu-id="8b899-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]