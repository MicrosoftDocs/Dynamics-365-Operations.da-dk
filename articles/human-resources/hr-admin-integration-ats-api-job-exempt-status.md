---
title: Status for jobfritagelse
description: Dette emne beskriver den indstilling for status for jobfritagelse, der er angivet for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053845"
---
# <a name="job-exempt-status"></a><span data-ttu-id="27a30-103">Status for jobfritagelse</span><span class="sxs-lookup"><span data-stu-id="27a30-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="27a30-104">Dette emne beskriver den indstilling for status for jobfritagelse, der er angivet for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="27a30-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="27a30-105">Fysisk navn: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="27a30-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="27a30-106">Denne fasttekst beskriver den indstilling der er angivet for statusværdier for FLSA-jobfritagelse.</span><span class="sxs-lookup"><span data-stu-id="27a30-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="27a30-107">Dette findes i den eksisterende cdm_jobexemptstatus indstilling.</span><span class="sxs-lookup"><span data-stu-id="27a30-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="27a30-108">Værdi</span><span class="sxs-lookup"><span data-stu-id="27a30-108">Value</span></span> | <span data-ttu-id="27a30-109">Mærkat</span><span class="sxs-lookup"><span data-stu-id="27a30-109">Label</span></span> | <span data-ttu-id="27a30-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="27a30-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="27a30-111">200000000</span><span class="sxs-lookup"><span data-stu-id="27a30-111">200000000</span></span> | <span data-ttu-id="27a30-112">Frit</span><span class="sxs-lookup"><span data-stu-id="27a30-112">Exempt</span></span> | <span data-ttu-id="27a30-113">Jobbet har eksempel på status på baggrund af FLSA-retningslinjer.</span><span class="sxs-lookup"><span data-stu-id="27a30-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="27a30-114">200000001</span><span class="sxs-lookup"><span data-stu-id="27a30-114">200000001</span></span> | <span data-ttu-id="27a30-115">Ikke-eksisterende</span><span class="sxs-lookup"><span data-stu-id="27a30-115">NonExempt</span></span> | <span data-ttu-id="27a30-116">Jobbet har eksempel på ikke-eksisterende status på baggrund af FLSA-retningslinjer.</span><span class="sxs-lookup"><span data-stu-id="27a30-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="27a30-117">200000002</span><span class="sxs-lookup"><span data-stu-id="27a30-117">200000002</span></span> | <span data-ttu-id="27a30-118">Gælder ikke</span><span class="sxs-lookup"><span data-stu-id="27a30-118">Does Not Apply</span></span> | <span data-ttu-id="27a30-119">FLSA-statusretningslinjer gælder ikke for jobbet.</span><span class="sxs-lookup"><span data-stu-id="27a30-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="27a30-120">Se også</span><span class="sxs-lookup"><span data-stu-id="27a30-120">See also</span></span>

[<span data-ttu-id="27a30-121">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="27a30-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="27a30-122">Eksempelforespørgsel til anmodning om rekruttering</span><span class="sxs-lookup"><span data-stu-id="27a30-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]