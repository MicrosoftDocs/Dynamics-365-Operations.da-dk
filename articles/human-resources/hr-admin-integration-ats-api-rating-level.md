---
title: Rangeringsniveau
description: Dette emne beskriver vurderingsniveauenheden for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 2dbdbea7087d8bca8563da10d1bf9a97df24e8b3
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464736"
---
# <a name="rating-level"></a><span data-ttu-id="b37ee-103">Rangeringsniveau</span><span class="sxs-lookup"><span data-stu-id="b37ee-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b37ee-104">Dette emne beskriver vurderingsniveauenheden for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b37ee-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="b37ee-105">Fysisk navn: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="b37ee-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="b37ee-106">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b37ee-106">Description</span></span>

<span data-ttu-id="b37ee-107">Denne enhed giver de tilgængelige vurderingsniveauer for færdigheder.</span><span class="sxs-lookup"><span data-stu-id="b37ee-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="b37ee-108">Vurderingsniveauer gælder på tværs af alle juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="b37ee-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b37ee-109">JSON-repræsentation</span><span class="sxs-lookup"><span data-stu-id="b37ee-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="b37ee-110">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="b37ee-110">Properties</span></span>

| <span data-ttu-id="b37ee-111">Egenskab</span><span class="sxs-lookup"><span data-stu-id="b37ee-111">Property</span></span><br><span data-ttu-id="b37ee-112">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="b37ee-112">**Physical name**</span></span><br><span data-ttu-id="b37ee-113">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="b37ee-113">**_Type_**</span></span> | <span data-ttu-id="b37ee-114">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="b37ee-114">Use</span></span> | <span data-ttu-id="b37ee-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b37ee-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b37ee-116">**Vurdering for enheds-id**</span><span class="sxs-lookup"><span data-stu-id="b37ee-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="b37ee-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="b37ee-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="b37ee-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b37ee-118">*GUID*</span></span> | <span data-ttu-id="b37ee-119">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="b37ee-119">Read-only</span></span><br><span data-ttu-id="b37ee-120">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="b37ee-120">Required</span></span><br><span data-ttu-id="b37ee-121">Systemgenereret</span><span class="sxs-lookup"><span data-stu-id="b37ee-121">System-generated</span></span> | <span data-ttu-id="b37ee-122">Systemgenereret entydigt id til niveauet.</span><span class="sxs-lookup"><span data-stu-id="b37ee-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="b37ee-123">**Vurderingsniveau-id**</span><span class="sxs-lookup"><span data-stu-id="b37ee-123">**Rating Level ID**</span></span><br><span data-ttu-id="b37ee-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="b37ee-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="b37ee-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="b37ee-125">*String*</span></span> | <span data-ttu-id="b37ee-126">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="b37ee-126">Read/write</span></span><br><span data-ttu-id="b37ee-127">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="b37ee-127">Required</span></span> | <span data-ttu-id="b37ee-128">Brugerlæsbar entydig identifikation af niveau.</span><span class="sxs-lookup"><span data-stu-id="b37ee-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="b37ee-129">**Vurderingsmodel-id**</span><span class="sxs-lookup"><span data-stu-id="b37ee-129">**Rating Model ID**</span></span><br><span data-ttu-id="b37ee-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="b37ee-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="b37ee-131">*Streng*</span><span class="sxs-lookup"><span data-stu-id="b37ee-131">*String*</span></span> | <span data-ttu-id="b37ee-132">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="b37ee-132">Read/write</span></span><br><span data-ttu-id="b37ee-133">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="b37ee-133">Required</span></span> | <span data-ttu-id="b37ee-134">Den vurderingsmodel, som vurderingsniveauet tilhører.</span><span class="sxs-lookup"><span data-stu-id="b37ee-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="b37ee-135">**Vurderingsmodel for enheds-id**</span><span class="sxs-lookup"><span data-stu-id="b37ee-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="b37ee-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="b37ee-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="b37ee-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b37ee-137">*GUID*</span></span> | <span data-ttu-id="b37ee-138">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="b37ee-138">Read-only</span></span><br><span data-ttu-id="b37ee-139">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="b37ee-139">Required</span></span><br><span data-ttu-id="b37ee-140">Fremmed nøgle: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="b37ee-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="b37ee-141">Det systemgenererede id for den vurderingsmodel, som vurderingsniveauet tilhører.</span><span class="sxs-lookup"><span data-stu-id="b37ee-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="b37ee-142">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="b37ee-142">**Description**</span></span><br><span data-ttu-id="b37ee-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="b37ee-143">mshr_description</span></span><br><span data-ttu-id="b37ee-144">*Streng*</span><span class="sxs-lookup"><span data-stu-id="b37ee-144">*String*</span></span> | <span data-ttu-id="b37ee-145">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="b37ee-145">Read/write</span></span><br><span data-ttu-id="b37ee-146">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="b37ee-146">Required</span></span> | <span data-ttu-id="b37ee-147">Beskrivelsen af vurderingsniveauet.</span><span class="sxs-lookup"><span data-stu-id="b37ee-147">The description of the rating level.</span></span> |
| <span data-ttu-id="b37ee-148">**Faktor**</span><span class="sxs-lookup"><span data-stu-id="b37ee-148">**Factor**</span></span><br><span data-ttu-id="b37ee-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="b37ee-149">mshr_factor</span></span><br><span data-ttu-id="b37ee-150">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="b37ee-150">*Integer*</span></span> | <span data-ttu-id="b37ee-151">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="b37ee-151">Read/write</span></span><br><span data-ttu-id="b37ee-152">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="b37ee-152">Required</span></span> | <span data-ttu-id="b37ee-153">Faktoren for vurderingsniveauet.</span><span class="sxs-lookup"><span data-stu-id="b37ee-153">The factor for the rating level.</span></span> <span data-ttu-id="b37ee-154">Når du sammenligner varer med et andet antal vurderingsniveauer, anvendes faktoren til at normalisere resultaterne.</span><span class="sxs-lookup"><span data-stu-id="b37ee-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="b37ee-155">Værdien skal være et heltal mellem 0 og 9.</span><span class="sxs-lookup"><span data-stu-id="b37ee-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="b37ee-156">**Bemærk!**</span><span class="sxs-lookup"><span data-stu-id="b37ee-156">**Note**</span></span><br><span data-ttu-id="b37ee-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="b37ee-157">mshr_note</span></span><br><span data-ttu-id="b37ee-158">*Streng*</span><span class="sxs-lookup"><span data-stu-id="b37ee-158">*String*</span></span> | <span data-ttu-id="b37ee-159">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="b37ee-159">Read/write</span></span><br><span data-ttu-id="b37ee-160">Valgfri</span><span class="sxs-lookup"><span data-stu-id="b37ee-160">Optional</span></span> | <span data-ttu-id="b37ee-161">Eventuelle notater, der er tilknyttet vurderingsniveauet.</span><span class="sxs-lookup"><span data-stu-id="b37ee-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="b37ee-162">**Primært felt**</span><span class="sxs-lookup"><span data-stu-id="b37ee-162">**Primary Field**</span></span><br><span data-ttu-id="b37ee-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="b37ee-163">mshr_primaryfield</span></span><br><span data-ttu-id="b37ee-164">*Streng*</span><span class="sxs-lookup"><span data-stu-id="b37ee-164">*String*</span></span> | <span data-ttu-id="b37ee-165">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="b37ee-165">Read-only</span></span><br><span data-ttu-id="b37ee-166">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="b37ee-166">Required</span></span> | <span data-ttu-id="b37ee-167">Felt, der bruges som id for enhedsposten.</span><span class="sxs-lookup"><span data-stu-id="b37ee-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="b37ee-168">Kombination af vurderingsniveau-id og vurderingsmodel-id.</span><span class="sxs-lookup"><span data-stu-id="b37ee-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="b37ee-169">Se også</span><span class="sxs-lookup"><span data-stu-id="b37ee-169">See also</span></span>

[<span data-ttu-id="b37ee-170">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="b37ee-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="b37ee-171">Eksempelforespørgsel til ansøger til ansættelse</span><span class="sxs-lookup"><span data-stu-id="b37ee-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]