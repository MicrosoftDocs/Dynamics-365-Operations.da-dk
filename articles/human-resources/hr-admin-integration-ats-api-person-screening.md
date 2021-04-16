---
title: Personscreening
description: Dette emne beskriver personscreeningenheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: 4bc32eb948f4a4966a927b0907b8d499486e43dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798027"
---
# <a name="person-screening"></a><span data-ttu-id="4201d-103">Personscreening</span><span class="sxs-lookup"><span data-stu-id="4201d-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4201d-104">Dette emne beskriver personscreeningenheden til Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4201d-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="4201d-105">Fysisk navn: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="4201d-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="4201d-106">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="4201d-106">Description</span></span>

<span data-ttu-id="4201d-107">Denne enhed beskriver de screeninger, som en kandidat har bestået eller skal bestået for ansættelsen.</span><span class="sxs-lookup"><span data-stu-id="4201d-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="4201d-108">JSON-repræsentation</span><span class="sxs-lookup"><span data-stu-id="4201d-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="4201d-109">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="4201d-109">Properties</span></span>

| <span data-ttu-id="4201d-110">Egenskab</span><span class="sxs-lookup"><span data-stu-id="4201d-110">Property</span></span><br><span data-ttu-id="4201d-111">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="4201d-111">**Physical name**</span></span><br><span data-ttu-id="4201d-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="4201d-112">**_Type_**</span></span> | <span data-ttu-id="4201d-113">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="4201d-113">Use</span></span> | <span data-ttu-id="4201d-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="4201d-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4201d-115">**Enheds-id for personscreening**</span><span class="sxs-lookup"><span data-stu-id="4201d-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="4201d-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="4201d-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="4201d-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4201d-117">*GUID*</span></span> | <span data-ttu-id="4201d-118">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="4201d-118">Read-only</span></span><br><span data-ttu-id="4201d-119">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="4201d-119">Required</span></span><br><span data-ttu-id="4201d-120">Systemgenereret</span><span class="sxs-lookup"><span data-stu-id="4201d-120">System-generated</span></span> | <span data-ttu-id="4201d-121">Entydigt primært id for personscreeningpost.</span><span class="sxs-lookup"><span data-stu-id="4201d-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="4201d-122">**Partnummer**</span><span class="sxs-lookup"><span data-stu-id="4201d-122">**Party Number**</span></span><br><span data-ttu-id="4201d-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="4201d-123">mshr_partynumber</span></span><br><span data-ttu-id="4201d-124">*Streng*</span><span class="sxs-lookup"><span data-stu-id="4201d-124">*String*</span></span> | <span data-ttu-id="4201d-125">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="4201d-125">Read/write</span></span><br><span data-ttu-id="4201d-126">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="4201d-126">Required</span></span> | <span data-ttu-id="4201d-127">Det partnummer (person), der er tilknyttet kandidaten.</span><span class="sxs-lookup"><span data-stu-id="4201d-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="4201d-128">**Værdi for person-id**</span><span class="sxs-lookup"><span data-stu-id="4201d-128">**Person ID Value**</span></span><br><span data-ttu-id="4201d-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="4201d-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="4201d-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4201d-130">*GUID*</span></span> | <span data-ttu-id="4201d-131">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="4201d-131">Read-only</span></span><br><span data-ttu-id="4201d-132">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="4201d-132">Required</span></span><br><span data-ttu-id="4201d-133">Fremmed nøgle: mshr_dirpersonentityid of mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="4201d-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="4201d-134">Systemgenereret id til partpost (person).</span><span class="sxs-lookup"><span data-stu-id="4201d-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="4201d-135">**Screeningstype-id**</span><span class="sxs-lookup"><span data-stu-id="4201d-135">**Screening Type ID**</span></span><br><span data-ttu-id="4201d-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="4201d-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="4201d-137">*Streng*</span><span class="sxs-lookup"><span data-stu-id="4201d-137">*String*</span></span> | <span data-ttu-id="4201d-138">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="4201d-138">Read/write</span></span><br><span data-ttu-id="4201d-139">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="4201d-139">Required</span></span><br><span data-ttu-id="4201d-140">Fremmed nøgle: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="4201d-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="4201d-141">Id for den screeningtype, der er defineret i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4201d-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="4201d-142">**Værdi for screeningstype-id**</span><span class="sxs-lookup"><span data-stu-id="4201d-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="4201d-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="4201d-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="4201d-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4201d-144">*GUID*</span></span> | <span data-ttu-id="4201d-145">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="4201d-145">Read-only</span></span><br><span data-ttu-id="4201d-146">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="4201d-146">Required</span></span><br><span data-ttu-id="4201d-147">Fremmed nøgle: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="4201d-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="4201d-148">Systemgenereret entydig identifikation for screeningstypeposten i den tilknyttede enhed.</span><span class="sxs-lookup"><span data-stu-id="4201d-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="4201d-149">**Ønsket af**</span><span class="sxs-lookup"><span data-stu-id="4201d-149">**Required By**</span></span><br><span data-ttu-id="4201d-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="4201d-150">mshr_requiredby</span></span><br><span data-ttu-id="4201d-151">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="4201d-151">*Datetime*</span></span> | <span data-ttu-id="4201d-152">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="4201d-152">Read/write</span></span><br><span data-ttu-id="4201d-153">Valgfri</span><span class="sxs-lookup"><span data-stu-id="4201d-153">Optional</span></span> | <span data-ttu-id="4201d-154">Den dato, hvor screeningen skal være fuldført.</span><span class="sxs-lookup"><span data-stu-id="4201d-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="4201d-155">**Status**</span><span class="sxs-lookup"><span data-stu-id="4201d-155">**Status**</span></span><br><span data-ttu-id="4201d-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="4201d-156">mshr_status</span></span><br><span data-ttu-id="4201d-157">*mshr_hcmcompletionstatus indstilling*</span><span class="sxs-lookup"><span data-stu-id="4201d-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="4201d-158">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="4201d-158">Read/write</span></span><br><span data-ttu-id="4201d-159">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="4201d-159">Required</span></span> | <span data-ttu-id="4201d-160">Angiver kandidatens status for screeningen.</span><span class="sxs-lookup"><span data-stu-id="4201d-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="4201d-161">**Fuldførelsesdato**</span><span class="sxs-lookup"><span data-stu-id="4201d-161">**Completed Date**</span></span><br><span data-ttu-id="4201d-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="4201d-162">mshr_completeddate</span></span><br><span data-ttu-id="4201d-163">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="4201d-163">*Datetime*</span></span> | <span data-ttu-id="4201d-164">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="4201d-164">Read/write</span></span><br><span data-ttu-id="4201d-165">Valgfri</span><span class="sxs-lookup"><span data-stu-id="4201d-165">Optional</span></span> | <span data-ttu-id="4201d-166">Datoen, hvor screeningen blev fuldført.</span><span class="sxs-lookup"><span data-stu-id="4201d-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="4201d-167">**Notater**</span><span class="sxs-lookup"><span data-stu-id="4201d-167">**Notes**</span></span><br><span data-ttu-id="4201d-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="4201d-168">mshr_note</span></span><br><span data-ttu-id="4201d-169">*Streng*</span><span class="sxs-lookup"><span data-stu-id="4201d-169">*String*</span></span> | <span data-ttu-id="4201d-170">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="4201d-170">Read/write</span></span><br><span data-ttu-id="4201d-171">Valgfri</span><span class="sxs-lookup"><span data-stu-id="4201d-171">Optional</span></span> | <span data-ttu-id="4201d-172">Noter til brug af rekrutteringsmedarbejdere eller ansættelseschefer.</span><span class="sxs-lookup"><span data-stu-id="4201d-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4201d-173">Se også</span><span class="sxs-lookup"><span data-stu-id="4201d-173">See also</span></span>

[<span data-ttu-id="4201d-174">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="4201d-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="4201d-175">Eksempelforespørgsel til ansøger til ansættelse</span><span class="sxs-lookup"><span data-stu-id="4201d-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]