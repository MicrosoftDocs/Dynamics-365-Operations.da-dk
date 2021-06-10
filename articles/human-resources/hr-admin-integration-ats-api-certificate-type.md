---
title: Certifikattype
description: Dette emne beskriver certifikatstypeenheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: b8e979f242eb689b730b7f8a8684b3e697adbee6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054686"
---
# <a name="certificate-type"></a><span data-ttu-id="78d40-103">Certifikattype</span><span class="sxs-lookup"><span data-stu-id="78d40-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="78d40-104">Dette emne beskriver certifikatstypeenheden til Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="78d40-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="78d40-105">Fysisk navn: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="78d40-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="78d40-106">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="78d40-106">Description</span></span>

<span data-ttu-id="78d40-107">Denne enhed definerer listen over typer af professionelle certifikater, der er defineret i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="78d40-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="78d40-108">Enheden er ikke specifik for en juridisk enhed (firma).</span><span class="sxs-lookup"><span data-stu-id="78d40-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="78d40-109">JSON-repræsentation</span><span class="sxs-lookup"><span data-stu-id="78d40-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="78d40-110">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="78d40-110">Properties</span></span>

| <span data-ttu-id="78d40-111">Egenskab</span><span class="sxs-lookup"><span data-stu-id="78d40-111">Property</span></span><br><span data-ttu-id="78d40-112">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="78d40-112">**Physical name**</span></span><br><span data-ttu-id="78d40-113">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="78d40-113">**_Type_**</span></span> | <span data-ttu-id="78d40-114">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="78d40-114">Use</span></span> | <span data-ttu-id="78d40-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="78d40-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="78d40-116">**Enheds-id for certifikattype**</span><span class="sxs-lookup"><span data-stu-id="78d40-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="78d40-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="78d40-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="78d40-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="78d40-118">*GUID*</span></span> | <span data-ttu-id="78d40-119">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="78d40-119">Read-only</span></span><br><span data-ttu-id="78d40-120">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="78d40-120">Required</span></span> 
<span data-ttu-id="78d40-121">Systemgenereret</span><span class="sxs-lookup"><span data-stu-id="78d40-121">System-generated</span></span> | <span data-ttu-id="78d40-122">Entydig primær identifikation af certifikattype.</span><span class="sxs-lookup"><span data-stu-id="78d40-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="78d40-123">**Certifikattype**</span><span class="sxs-lookup"><span data-stu-id="78d40-123">**Certificate Type**</span></span><br><span data-ttu-id="78d40-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="78d40-124">mshr_certificatetype</span></span><br><span data-ttu-id="78d40-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="78d40-125">*String*</span></span> | <span data-ttu-id="78d40-126">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="78d40-126">Read/write</span></span><br><span data-ttu-id="78d40-127">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="78d40-127">Required</span></span> | <span data-ttu-id="78d40-128">Entydig brugerlæsbar identifikation af certifikattype.</span><span class="sxs-lookup"><span data-stu-id="78d40-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="78d40-129">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="78d40-129">**Description**</span></span><br><span data-ttu-id="78d40-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="78d40-130">mshr_description</span></span><br><span data-ttu-id="78d40-131">*Streng*</span><span class="sxs-lookup"><span data-stu-id="78d40-131">*String*</span></span> | <span data-ttu-id="78d40-132">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="78d40-132">Read/write</span></span><br><span data-ttu-id="78d40-133">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="78d40-133">Required</span></span> | <span data-ttu-id="78d40-134">Beskrivelse af certifikattype.</span><span class="sxs-lookup"><span data-stu-id="78d40-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="78d40-135">**Fornyelse påkrævet**</span><span class="sxs-lookup"><span data-stu-id="78d40-135">**Require Renewal**</span></span><br><span data-ttu-id="78d40-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="78d40-136">mshr_requirerenewal</span></span><br><span data-ttu-id="78d40-137">*mshr_noyes indstilling*</span><span class="sxs-lookup"><span data-stu-id="78d40-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="78d40-138">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="78d40-138">Read/write</span></span><br><span data-ttu-id="78d40-139">Valgfri</span><span class="sxs-lookup"><span data-stu-id="78d40-139">Optional</span></span> | <span data-ttu-id="78d40-140">Angiver, om certifikatet skal fornys.</span><span class="sxs-lookup"><span data-stu-id="78d40-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="78d40-141">Se også</span><span class="sxs-lookup"><span data-stu-id="78d40-141">See also</span></span>

[<span data-ttu-id="78d40-142">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="78d40-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="78d40-143">Eksempelforespørgsel til ansøger til ansættelse</span><span class="sxs-lookup"><span data-stu-id="78d40-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]