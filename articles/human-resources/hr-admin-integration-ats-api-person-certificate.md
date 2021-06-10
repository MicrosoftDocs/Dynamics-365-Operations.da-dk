---
title: Personcertifikat
description: Dette emne beskriver personcertifikatenheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: 5cdd742d6d36ccd7136f95e416507ed6e5e5a75a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055190"
---
# <a name="person-certificate"></a><span data-ttu-id="402a6-103">Personcertifikat</span><span class="sxs-lookup"><span data-stu-id="402a6-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="402a6-104">Dette emne beskriver personcertifikatenheden til Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="402a6-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="402a6-105">Fysisk navn: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="402a6-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="402a6-106">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="402a6-106">Description</span></span>

<span data-ttu-id="402a6-107">Denne enhed beskriver en kandidats faglige certifikater.</span><span class="sxs-lookup"><span data-stu-id="402a6-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="402a6-108">JSON-repræsentation</span><span class="sxs-lookup"><span data-stu-id="402a6-108">JSON representation</span></span>

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="402a6-109">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="402a6-109">Properties</span></span>

| <span data-ttu-id="402a6-110">Egenskab</span><span class="sxs-lookup"><span data-stu-id="402a6-110">Property</span></span><br><span data-ttu-id="402a6-111">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="402a6-111">**Physical name**</span></span><br><span data-ttu-id="402a6-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="402a6-112">**_Type_**</span></span> | <span data-ttu-id="402a6-113">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="402a6-113">Use</span></span> | <span data-ttu-id="402a6-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="402a6-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="402a6-115">**Enheds-id for personcertifikat**</span><span class="sxs-lookup"><span data-stu-id="402a6-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="402a6-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="402a6-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="402a6-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="402a6-117">*GUID*</span></span> | <span data-ttu-id="402a6-118">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="402a6-118">Read-only</span></span><br><span data-ttu-id="402a6-119">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="402a6-119">Required</span></span> | <span data-ttu-id="402a6-120">Systemgenereret entydig identifikation af enhedsposten for personcertifikat.</span><span class="sxs-lookup"><span data-stu-id="402a6-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="402a6-121">**Partnummer**</span><span class="sxs-lookup"><span data-stu-id="402a6-121">**Party Number**</span></span><br><span data-ttu-id="402a6-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="402a6-122">mshr_partynumber</span></span><br><span data-ttu-id="402a6-123">*Streng*</span><span class="sxs-lookup"><span data-stu-id="402a6-123">*String*</span></span> | <span data-ttu-id="402a6-124">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="402a6-124">Read/write</span></span><br><span data-ttu-id="402a6-125">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="402a6-125">Required</span></span> | <span data-ttu-id="402a6-126">Part-id (person) for kandidaten.</span><span class="sxs-lookup"><span data-stu-id="402a6-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="402a6-127">**Værdi for person-id**</span><span class="sxs-lookup"><span data-stu-id="402a6-127">**Person ID Value**</span></span><br><span data-ttu-id="402a6-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="402a6-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="402a6-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="402a6-129">*GUID*</span></span> | <span data-ttu-id="402a6-130">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="402a6-130">Read-only</span></span><br><span data-ttu-id="402a6-131">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="402a6-131">Required</span></span><br><span data-ttu-id="402a6-132">Fremmed nøgle: mshr_dirpersonentityid of mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="402a6-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="402a6-133">Systemgenereret id til partpost (person).</span><span class="sxs-lookup"><span data-stu-id="402a6-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="402a6-134">**Certifikattype-id**</span><span class="sxs-lookup"><span data-stu-id="402a6-134">**Certificate Type ID**</span></span><br><span data-ttu-id="402a6-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="402a6-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="402a6-136">*Streng*</span><span class="sxs-lookup"><span data-stu-id="402a6-136">*String*</span></span> | <span data-ttu-id="402a6-137">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="402a6-137">Read/write</span></span><br><span data-ttu-id="402a6-138">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="402a6-138">Required</span></span> |  <span data-ttu-id="402a6-139">Id for den certifikattype, der er defineret i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="402a6-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="402a6-140">**Værdi for certifikattype-id**</span><span class="sxs-lookup"><span data-stu-id="402a6-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="402a6-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="402a6-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="402a6-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="402a6-142">*GUID*</span></span> | <span data-ttu-id="402a6-143">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="402a6-143">Read-only</span></span><br><span data-ttu-id="402a6-144">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="402a6-144">Required</span></span><br><span data-ttu-id="402a6-145">Fremmed nøgle: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="402a6-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="402a6-146">Systemgenereret entydig identifikation af certifikattypen i den tilknyttede enhed.</span><span class="sxs-lookup"><span data-stu-id="402a6-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="402a6-147">**Startdato**</span><span class="sxs-lookup"><span data-stu-id="402a6-147">**Start Date**</span></span><br><span data-ttu-id="402a6-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="402a6-148">mshr_startdate</span></span><br><span data-ttu-id="402a6-149">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="402a6-149">*Datetime*</span></span> | <span data-ttu-id="402a6-150">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="402a6-150">Read/write</span></span><br><span data-ttu-id="402a6-151">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="402a6-151">Required</span></span> | <span data-ttu-id="402a6-152">Den dato, hvor certifikatet blev udstedt.</span><span class="sxs-lookup"><span data-stu-id="402a6-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="402a6-153">**Slutdato**</span><span class="sxs-lookup"><span data-stu-id="402a6-153">**End Date**</span></span><br><span data-ttu-id="402a6-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="402a6-154">mshr_enddate</span></span><br><span data-ttu-id="402a6-155">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="402a6-155">*Datetime*</span></span> | <span data-ttu-id="402a6-156">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="402a6-156">Read/write</span></span><br><span data-ttu-id="402a6-157">Valgfri</span><span class="sxs-lookup"><span data-stu-id="402a6-157">Optional</span></span> | <span data-ttu-id="402a6-158">Den dato, hvor certifikatet udløber.</span><span class="sxs-lookup"><span data-stu-id="402a6-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="402a6-159">**Notater**</span><span class="sxs-lookup"><span data-stu-id="402a6-159">**Notes**</span></span><br><span data-ttu-id="402a6-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="402a6-160">mshr_notes</span></span><br><span data-ttu-id="402a6-161">*Streng*</span><span class="sxs-lookup"><span data-stu-id="402a6-161">*String*</span></span> | <span data-ttu-id="402a6-162">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="402a6-162">Read/write</span></span><br><span data-ttu-id="402a6-163">Valgfri</span><span class="sxs-lookup"><span data-stu-id="402a6-163">Optional</span></span> | <span data-ttu-id="402a6-164">Noter til brug af rekrutteringsmedarbejdere eller ansættelseschefer.</span><span class="sxs-lookup"><span data-stu-id="402a6-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="402a6-165">**Primært felt**</span><span class="sxs-lookup"><span data-stu-id="402a6-165">**Primary Field**</span></span><br><span data-ttu-id="402a6-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="402a6-166">mshr_primaryfield</span></span><br><span data-ttu-id="402a6-167">*Streng*</span><span class="sxs-lookup"><span data-stu-id="402a6-167">*String*</span></span> | <span data-ttu-id="402a6-168">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="402a6-168">Read-only</span></span><br><span data-ttu-id="402a6-169">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="402a6-169">Required</span></span> |  <span data-ttu-id="402a6-170">Felt, der bruges som id for enhedsposten.</span><span class="sxs-lookup"><span data-stu-id="402a6-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="402a6-171">Kombination af partnummer, certifikattype-id og startdato.</span><span class="sxs-lookup"><span data-stu-id="402a6-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="402a6-172">Se også</span><span class="sxs-lookup"><span data-stu-id="402a6-172">See also</span></span>

[<span data-ttu-id="402a6-173">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="402a6-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="402a6-174">Eksempelforespørgsel til ansøger til ansættelse</span><span class="sxs-lookup"><span data-stu-id="402a6-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]