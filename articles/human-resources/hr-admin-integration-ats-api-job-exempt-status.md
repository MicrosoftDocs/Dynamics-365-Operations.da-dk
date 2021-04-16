---
title: Status for jobfritagelse
description: Dette emne beskriver den indstilling for status for jobfritagelse, der er angivet for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 4765858f389f28467ae2ac71084c15d2ba0cbe8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798291"
---
# <a name="job-exempt-status"></a><span data-ttu-id="02b5c-103">Status for jobfritagelse</span><span class="sxs-lookup"><span data-stu-id="02b5c-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="02b5c-104">Dette emne beskriver den indstilling for status for jobfritagelse, der er angivet for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="02b5c-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="02b5c-105">Fysisk navn: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="02b5c-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="02b5c-106">Denne fasttekst beskriver den indstilling der er angivet for statusværdier for FLSA-jobfritagelse.</span><span class="sxs-lookup"><span data-stu-id="02b5c-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="02b5c-107">Dette findes i den eksisterende cdm_jobexemptstatus indstilling.</span><span class="sxs-lookup"><span data-stu-id="02b5c-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="02b5c-108">Værdi</span><span class="sxs-lookup"><span data-stu-id="02b5c-108">Value</span></span> | <span data-ttu-id="02b5c-109">Mærkat</span><span class="sxs-lookup"><span data-stu-id="02b5c-109">Label</span></span> | <span data-ttu-id="02b5c-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="02b5c-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="02b5c-111">200000000</span><span class="sxs-lookup"><span data-stu-id="02b5c-111">200000000</span></span> | <span data-ttu-id="02b5c-112">Frit</span><span class="sxs-lookup"><span data-stu-id="02b5c-112">Exempt</span></span> | <span data-ttu-id="02b5c-113">Jobbet har eksempel på status på baggrund af FLSA-retningslinjer.</span><span class="sxs-lookup"><span data-stu-id="02b5c-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="02b5c-114">200000001</span><span class="sxs-lookup"><span data-stu-id="02b5c-114">200000001</span></span> | <span data-ttu-id="02b5c-115">Ikke-eksisterende</span><span class="sxs-lookup"><span data-stu-id="02b5c-115">NonExempt</span></span> | <span data-ttu-id="02b5c-116">Jobbet har eksempel på ikke-eksisterende status på baggrund af FLSA-retningslinjer.</span><span class="sxs-lookup"><span data-stu-id="02b5c-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="02b5c-117">200000002</span><span class="sxs-lookup"><span data-stu-id="02b5c-117">200000002</span></span> | <span data-ttu-id="02b5c-118">Gælder ikke</span><span class="sxs-lookup"><span data-stu-id="02b5c-118">Does Not Apply</span></span> | <span data-ttu-id="02b5c-119">FLSA-statusretningslinjer gælder ikke for jobbet.</span><span class="sxs-lookup"><span data-stu-id="02b5c-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="02b5c-120">Se også</span><span class="sxs-lookup"><span data-stu-id="02b5c-120">See also</span></span>

[<span data-ttu-id="02b5c-121">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="02b5c-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="02b5c-122">Eksempelforespørgsel til anmodning om rekruttering</span><span class="sxs-lookup"><span data-stu-id="02b5c-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]