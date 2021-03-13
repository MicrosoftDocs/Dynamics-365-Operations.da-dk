---
title: Personscreening
description: Dette emne beskriver personscreeningenheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: d76bb57d85ee16f4faa0bb9cfec77047feb7df5f
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125371"
---
# <a name="person-screening"></a><span data-ttu-id="66c49-103">Personscreening</span><span class="sxs-lookup"><span data-stu-id="66c49-103">Person screening</span></span>

<span data-ttu-id="66c49-104">Dette emne beskriver personscreeningenheden til Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="66c49-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="66c49-105">Fysisk navn: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="66c49-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="66c49-106">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="66c49-106">Description</span></span>

<span data-ttu-id="66c49-107">Denne enhed beskriver de screeninger, som en kandidat har bestået eller skal bestået for ansættelsen.</span><span class="sxs-lookup"><span data-stu-id="66c49-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="66c49-108">JSON-repræsentation</span><span class="sxs-lookup"><span data-stu-id="66c49-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="66c49-109">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="66c49-109">Properties</span></span>

| <span data-ttu-id="66c49-110">Egenskab</span><span class="sxs-lookup"><span data-stu-id="66c49-110">Property</span></span><br><span data-ttu-id="66c49-111">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="66c49-111">**Physical name**</span></span><br><span data-ttu-id="66c49-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="66c49-112">**_Type_**</span></span> | <span data-ttu-id="66c49-113">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="66c49-113">Use</span></span> | <span data-ttu-id="66c49-114">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="66c49-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="66c49-115">**Enheds-id for personscreening**</span><span class="sxs-lookup"><span data-stu-id="66c49-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="66c49-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="66c49-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="66c49-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="66c49-117">*GUID*</span></span> | <span data-ttu-id="66c49-118">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="66c49-118">Read-only</span></span><br><span data-ttu-id="66c49-119">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="66c49-119">Required</span></span><br><span data-ttu-id="66c49-120">Systemgenereret</span><span class="sxs-lookup"><span data-stu-id="66c49-120">System-generated</span></span> | <span data-ttu-id="66c49-121">Entydigt primært id for personscreeningpost.</span><span class="sxs-lookup"><span data-stu-id="66c49-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="66c49-122">**Partnummer**</span><span class="sxs-lookup"><span data-stu-id="66c49-122">**Party Number**</span></span><br><span data-ttu-id="66c49-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="66c49-123">mshr_partynumber</span></span><br><span data-ttu-id="66c49-124">*Streng*</span><span class="sxs-lookup"><span data-stu-id="66c49-124">*String*</span></span> | <span data-ttu-id="66c49-125">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="66c49-125">Read/write</span></span><br><span data-ttu-id="66c49-126">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="66c49-126">Required</span></span> | <span data-ttu-id="66c49-127">Det partnummer (person), der er tilknyttet kandidaten.</span><span class="sxs-lookup"><span data-stu-id="66c49-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="66c49-128">**Værdi for person-id**</span><span class="sxs-lookup"><span data-stu-id="66c49-128">**Person ID Value**</span></span><br><span data-ttu-id="66c49-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="66c49-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="66c49-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="66c49-130">*GUID*</span></span> | <span data-ttu-id="66c49-131">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="66c49-131">Read-only</span></span><br><span data-ttu-id="66c49-132">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="66c49-132">Required</span></span><br><span data-ttu-id="66c49-133">Fremmed nøgle: mshr_dirpersonentityid of mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="66c49-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="66c49-134">Systemgenereret id til partpost (person).</span><span class="sxs-lookup"><span data-stu-id="66c49-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="66c49-135">**Screeningstype-id**</span><span class="sxs-lookup"><span data-stu-id="66c49-135">**Screening Type ID**</span></span><br><span data-ttu-id="66c49-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="66c49-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="66c49-137">*Streng*</span><span class="sxs-lookup"><span data-stu-id="66c49-137">*String*</span></span> | <span data-ttu-id="66c49-138">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="66c49-138">Read/write</span></span><br><span data-ttu-id="66c49-139">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="66c49-139">Required</span></span><br><span data-ttu-id="66c49-140">Fremmed nøgle: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="66c49-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="66c49-141">Id for den screeningtype, der er defineret i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="66c49-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="66c49-142">**Værdi for screeningstype-id**</span><span class="sxs-lookup"><span data-stu-id="66c49-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="66c49-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="66c49-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="66c49-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="66c49-144">*GUID*</span></span> | <span data-ttu-id="66c49-145">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="66c49-145">Read-only</span></span><br><span data-ttu-id="66c49-146">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="66c49-146">Required</span></span><br><span data-ttu-id="66c49-147">Fremmed nøgle: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="66c49-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="66c49-148">Systemgenereret entydig identifikation for screeningstypeposten i den tilknyttede enhed.</span><span class="sxs-lookup"><span data-stu-id="66c49-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="66c49-149">**Ønsket af**</span><span class="sxs-lookup"><span data-stu-id="66c49-149">**Required By**</span></span><br><span data-ttu-id="66c49-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="66c49-150">mshr_requiredby</span></span><br><span data-ttu-id="66c49-151">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="66c49-151">*Datetime*</span></span> | <span data-ttu-id="66c49-152">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="66c49-152">Read/write</span></span><br><span data-ttu-id="66c49-153">Valgfri</span><span class="sxs-lookup"><span data-stu-id="66c49-153">Optional</span></span> | <span data-ttu-id="66c49-154">Den dato, hvor screeningen skal være fuldført.</span><span class="sxs-lookup"><span data-stu-id="66c49-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="66c49-155">**Status**</span><span class="sxs-lookup"><span data-stu-id="66c49-155">**Status**</span></span><br><span data-ttu-id="66c49-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="66c49-156">mshr_status</span></span><br><span data-ttu-id="66c49-157">*mshr_hcmcompletionstatus indstilling*</span><span class="sxs-lookup"><span data-stu-id="66c49-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="66c49-158">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="66c49-158">Read/write</span></span><br><span data-ttu-id="66c49-159">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="66c49-159">Required</span></span> | <span data-ttu-id="66c49-160">Angiver kandidatens status for screeningen.</span><span class="sxs-lookup"><span data-stu-id="66c49-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="66c49-161">**Fuldførelsesdato**</span><span class="sxs-lookup"><span data-stu-id="66c49-161">**Completed Date**</span></span><br><span data-ttu-id="66c49-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="66c49-162">mshr_completeddate</span></span><br><span data-ttu-id="66c49-163">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="66c49-163">*Datetime*</span></span> | <span data-ttu-id="66c49-164">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="66c49-164">Read/write</span></span><br><span data-ttu-id="66c49-165">Valgfri</span><span class="sxs-lookup"><span data-stu-id="66c49-165">Optional</span></span> | <span data-ttu-id="66c49-166">Datoen, hvor screeningen blev fuldført.</span><span class="sxs-lookup"><span data-stu-id="66c49-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="66c49-167">**Notater**</span><span class="sxs-lookup"><span data-stu-id="66c49-167">**Notes**</span></span><br><span data-ttu-id="66c49-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="66c49-168">mshr_note</span></span><br><span data-ttu-id="66c49-169">*Streng*</span><span class="sxs-lookup"><span data-stu-id="66c49-169">*String*</span></span> | <span data-ttu-id="66c49-170">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="66c49-170">Read/write</span></span><br><span data-ttu-id="66c49-171">Valgfri</span><span class="sxs-lookup"><span data-stu-id="66c49-171">Optional</span></span> | <span data-ttu-id="66c49-172">Noter til brug af rekrutteringsmedarbejdere eller ansættelseschefer.</span><span class="sxs-lookup"><span data-stu-id="66c49-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="66c49-173">Se også</span><span class="sxs-lookup"><span data-stu-id="66c49-173">See also</span></span>

[<span data-ttu-id="66c49-174">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="66c49-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="66c49-175">Eksempelforespørgsel til ansøger til ansættelse</span><span class="sxs-lookup"><span data-stu-id="66c49-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

