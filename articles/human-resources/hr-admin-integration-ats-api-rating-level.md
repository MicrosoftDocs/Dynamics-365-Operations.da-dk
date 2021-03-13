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
ms.openlocfilehash: 1ad37c7a5b961bb03d37775168dac91e606d2b08
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125251"
---
# <a name="rating-level"></a><span data-ttu-id="ad78a-103">Rangeringsniveau</span><span class="sxs-lookup"><span data-stu-id="ad78a-103">Rating level</span></span>

<span data-ttu-id="ad78a-104">Dette emne beskriver vurderingsniveauenheden for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ad78a-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ad78a-105">Fysisk navn: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="ad78a-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="ad78a-106">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="ad78a-106">Description</span></span>

<span data-ttu-id="ad78a-107">Denne enhed giver de tilgængelige vurderingsniveauer for færdigheder.</span><span class="sxs-lookup"><span data-stu-id="ad78a-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="ad78a-108">Vurderingsniveauer gælder på tværs af alle juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="ad78a-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ad78a-109">JSON-repræsentation</span><span class="sxs-lookup"><span data-stu-id="ad78a-109">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="ad78a-110">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="ad78a-110">Properties</span></span>

| <span data-ttu-id="ad78a-111">Egenskab</span><span class="sxs-lookup"><span data-stu-id="ad78a-111">Property</span></span><br><span data-ttu-id="ad78a-112">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="ad78a-112">**Physical name**</span></span><br><span data-ttu-id="ad78a-113">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="ad78a-113">**_Type_**</span></span> | <span data-ttu-id="ad78a-114">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="ad78a-114">Use</span></span> | <span data-ttu-id="ad78a-115">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="ad78a-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ad78a-116">**Vurdering for enheds-id**</span><span class="sxs-lookup"><span data-stu-id="ad78a-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="ad78a-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="ad78a-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="ad78a-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ad78a-118">*GUID*</span></span> | <span data-ttu-id="ad78a-119">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="ad78a-119">Read-only</span></span><br><span data-ttu-id="ad78a-120">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad78a-120">Required</span></span><br><span data-ttu-id="ad78a-121">Systemgenereret</span><span class="sxs-lookup"><span data-stu-id="ad78a-121">System-generated</span></span> | <span data-ttu-id="ad78a-122">Systemgenereret entydigt id til niveauet.</span><span class="sxs-lookup"><span data-stu-id="ad78a-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="ad78a-123">**Vurderingsniveau-id**</span><span class="sxs-lookup"><span data-stu-id="ad78a-123">**Rating Level ID**</span></span><br><span data-ttu-id="ad78a-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="ad78a-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="ad78a-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ad78a-125">*String*</span></span> | <span data-ttu-id="ad78a-126">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="ad78a-126">Read/write</span></span><br><span data-ttu-id="ad78a-127">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad78a-127">Required</span></span> | <span data-ttu-id="ad78a-128">Brugerlæsbar entydig identifikation af niveau.</span><span class="sxs-lookup"><span data-stu-id="ad78a-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="ad78a-129">**Vurderingsmodel-id**</span><span class="sxs-lookup"><span data-stu-id="ad78a-129">**Rating Model ID**</span></span><br><span data-ttu-id="ad78a-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="ad78a-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="ad78a-131">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ad78a-131">*String*</span></span> | <span data-ttu-id="ad78a-132">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="ad78a-132">Read/write</span></span><br><span data-ttu-id="ad78a-133">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad78a-133">Required</span></span> | <span data-ttu-id="ad78a-134">Den vurderingsmodel, som vurderingsniveauet tilhører.</span><span class="sxs-lookup"><span data-stu-id="ad78a-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="ad78a-135">**Vurderingsmodel for enheds-id**</span><span class="sxs-lookup"><span data-stu-id="ad78a-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="ad78a-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="ad78a-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="ad78a-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ad78a-137">*GUID*</span></span> | <span data-ttu-id="ad78a-138">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="ad78a-138">Read-only</span></span><br><span data-ttu-id="ad78a-139">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad78a-139">Required</span></span><br><span data-ttu-id="ad78a-140">Fremmed nøgle: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="ad78a-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="ad78a-141">Det systemgenererede id for den vurderingsmodel, som vurderingsniveauet tilhører.</span><span class="sxs-lookup"><span data-stu-id="ad78a-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="ad78a-142">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="ad78a-142">**Description**</span></span><br><span data-ttu-id="ad78a-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="ad78a-143">mshr_description</span></span><br><span data-ttu-id="ad78a-144">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ad78a-144">*String*</span></span> | <span data-ttu-id="ad78a-145">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="ad78a-145">Read/write</span></span><br><span data-ttu-id="ad78a-146">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad78a-146">Required</span></span> | <span data-ttu-id="ad78a-147">Beskrivelsen af vurderingsniveauet.</span><span class="sxs-lookup"><span data-stu-id="ad78a-147">The description of the rating level.</span></span> |
| <span data-ttu-id="ad78a-148">**Faktor**</span><span class="sxs-lookup"><span data-stu-id="ad78a-148">**Factor**</span></span><br><span data-ttu-id="ad78a-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="ad78a-149">mshr_factor</span></span><br><span data-ttu-id="ad78a-150">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="ad78a-150">*Integer*</span></span> | <span data-ttu-id="ad78a-151">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="ad78a-151">Read/write</span></span><br><span data-ttu-id="ad78a-152">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad78a-152">Required</span></span> | <span data-ttu-id="ad78a-153">Faktoren for vurderingsniveauet.</span><span class="sxs-lookup"><span data-stu-id="ad78a-153">The factor for the rating level.</span></span> <span data-ttu-id="ad78a-154">Når du sammenligner varer med et andet antal vurderingsniveauer, anvendes faktoren til at normalisere resultaterne.</span><span class="sxs-lookup"><span data-stu-id="ad78a-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="ad78a-155">Værdien skal være et heltal mellem 0 og 9.</span><span class="sxs-lookup"><span data-stu-id="ad78a-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="ad78a-156">**Bemærk!**</span><span class="sxs-lookup"><span data-stu-id="ad78a-156">**Note**</span></span><br><span data-ttu-id="ad78a-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="ad78a-157">mshr_note</span></span><br><span data-ttu-id="ad78a-158">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ad78a-158">*String*</span></span> | <span data-ttu-id="ad78a-159">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="ad78a-159">Read/write</span></span><br><span data-ttu-id="ad78a-160">Valgfri</span><span class="sxs-lookup"><span data-stu-id="ad78a-160">Optional</span></span> | <span data-ttu-id="ad78a-161">Eventuelle notater, der er tilknyttet vurderingsniveauet.</span><span class="sxs-lookup"><span data-stu-id="ad78a-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="ad78a-162">**Primært felt**</span><span class="sxs-lookup"><span data-stu-id="ad78a-162">**Primary Field**</span></span><br><span data-ttu-id="ad78a-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="ad78a-163">mshr_primaryfield</span></span><br><span data-ttu-id="ad78a-164">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ad78a-164">*String*</span></span> | <span data-ttu-id="ad78a-165">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="ad78a-165">Read-only</span></span><br><span data-ttu-id="ad78a-166">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad78a-166">Required</span></span> | <span data-ttu-id="ad78a-167">Felt, der bruges som id for enhedsposten.</span><span class="sxs-lookup"><span data-stu-id="ad78a-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="ad78a-168">Kombination af vurderingsniveau-id og vurderingsmodel-id.</span><span class="sxs-lookup"><span data-stu-id="ad78a-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ad78a-169">Se også</span><span class="sxs-lookup"><span data-stu-id="ad78a-169">See also</span></span>

[<span data-ttu-id="ad78a-170">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="ad78a-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ad78a-171">Eksempelforespørgsel til ansøger til ansættelse</span><span class="sxs-lookup"><span data-stu-id="ad78a-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

