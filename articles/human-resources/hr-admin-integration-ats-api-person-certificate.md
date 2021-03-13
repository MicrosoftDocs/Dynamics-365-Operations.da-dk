---
title: Personcertifikat
description: Dette emne beskriver personcertifikatenheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: fa4582dc00341a647f1ea43ed16d9dce8bfcf688
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125347"
---
# <a name="person-certificate"></a><span data-ttu-id="29606-103">Personcertifikat</span><span class="sxs-lookup"><span data-stu-id="29606-103">Person certificate</span></span>

<span data-ttu-id="29606-104">Dette emne beskriver personcertifikatenheden til Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="29606-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="29606-105">Fysisk navn: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="29606-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="29606-106">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="29606-106">Description</span></span>

<span data-ttu-id="29606-107">Denne enhed beskriver en kandidats faglige certifikater.</span><span class="sxs-lookup"><span data-stu-id="29606-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="29606-108">JSON-repræsentation</span><span class="sxs-lookup"><span data-stu-id="29606-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="29606-109">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="29606-109">Properties</span></span>

| <span data-ttu-id="29606-110">Egenskab</span><span class="sxs-lookup"><span data-stu-id="29606-110">Property</span></span><br><span data-ttu-id="29606-111">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="29606-111">**Physical name**</span></span><br><span data-ttu-id="29606-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="29606-112">**_Type_**</span></span> | <span data-ttu-id="29606-113">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="29606-113">Use</span></span> | <span data-ttu-id="29606-114">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="29606-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="29606-115">**Enheds-id for personcertifikat**</span><span class="sxs-lookup"><span data-stu-id="29606-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="29606-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="29606-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="29606-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="29606-117">*GUID*</span></span> | <span data-ttu-id="29606-118">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="29606-118">Read-only</span></span><br><span data-ttu-id="29606-119">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="29606-119">Required</span></span> | <span data-ttu-id="29606-120">Systemgenereret entydig identifikation af enhedsposten for personcertifikat.</span><span class="sxs-lookup"><span data-stu-id="29606-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="29606-121">**Partnummer**</span><span class="sxs-lookup"><span data-stu-id="29606-121">**Party Number**</span></span><br><span data-ttu-id="29606-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="29606-122">mshr_partynumber</span></span><br><span data-ttu-id="29606-123">*Streng*</span><span class="sxs-lookup"><span data-stu-id="29606-123">*String*</span></span> | <span data-ttu-id="29606-124">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="29606-124">Read/write</span></span><br><span data-ttu-id="29606-125">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="29606-125">Required</span></span> | <span data-ttu-id="29606-126">Part-id (person) for kandidaten.</span><span class="sxs-lookup"><span data-stu-id="29606-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="29606-127">**Værdi for person-id**</span><span class="sxs-lookup"><span data-stu-id="29606-127">**Person ID Value**</span></span><br><span data-ttu-id="29606-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="29606-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="29606-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="29606-129">*GUID*</span></span> | <span data-ttu-id="29606-130">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="29606-130">Read-only</span></span><br><span data-ttu-id="29606-131">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="29606-131">Required</span></span><br><span data-ttu-id="29606-132">Fremmed nøgle: mshr_dirpersonentityid of mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="29606-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="29606-133">Systemgenereret id til partpost (person).</span><span class="sxs-lookup"><span data-stu-id="29606-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="29606-134">**Certifikattype-id**</span><span class="sxs-lookup"><span data-stu-id="29606-134">**Certificate Type ID**</span></span><br><span data-ttu-id="29606-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="29606-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="29606-136">*Streng*</span><span class="sxs-lookup"><span data-stu-id="29606-136">*String*</span></span> | <span data-ttu-id="29606-137">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="29606-137">Read/write</span></span><br><span data-ttu-id="29606-138">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="29606-138">Required</span></span> |  <span data-ttu-id="29606-139">Id for den certifikattype, der er defineret i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="29606-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="29606-140">**Værdi for certifikattype-id**</span><span class="sxs-lookup"><span data-stu-id="29606-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="29606-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="29606-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="29606-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="29606-142">*GUID*</span></span> | <span data-ttu-id="29606-143">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="29606-143">Read-only</span></span><br><span data-ttu-id="29606-144">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="29606-144">Required</span></span><br><span data-ttu-id="29606-145">Fremmed nøgle: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="29606-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="29606-146">Systemgenereret entydig identifikation af certifikattypen i den tilknyttede enhed.</span><span class="sxs-lookup"><span data-stu-id="29606-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="29606-147">**Startdato**</span><span class="sxs-lookup"><span data-stu-id="29606-147">**Start Date**</span></span><br><span data-ttu-id="29606-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="29606-148">mshr_startdate</span></span><br><span data-ttu-id="29606-149">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="29606-149">*Datetime*</span></span> | <span data-ttu-id="29606-150">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="29606-150">Read/write</span></span><br><span data-ttu-id="29606-151">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="29606-151">Required</span></span> | <span data-ttu-id="29606-152">Den dato, hvor certifikatet blev udstedt.</span><span class="sxs-lookup"><span data-stu-id="29606-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="29606-153">**Slutdato**</span><span class="sxs-lookup"><span data-stu-id="29606-153">**End Date**</span></span><br><span data-ttu-id="29606-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="29606-154">mshr_enddate</span></span><br><span data-ttu-id="29606-155">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="29606-155">*Datetime*</span></span> | <span data-ttu-id="29606-156">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="29606-156">Read/write</span></span><br><span data-ttu-id="29606-157">Valgfri</span><span class="sxs-lookup"><span data-stu-id="29606-157">Optional</span></span> | <span data-ttu-id="29606-158">Den dato, hvor certifikatet udløber.</span><span class="sxs-lookup"><span data-stu-id="29606-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="29606-159">**Notater**</span><span class="sxs-lookup"><span data-stu-id="29606-159">**Notes**</span></span><br><span data-ttu-id="29606-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="29606-160">mshr_notes</span></span><br><span data-ttu-id="29606-161">*Streng*</span><span class="sxs-lookup"><span data-stu-id="29606-161">*String*</span></span> | <span data-ttu-id="29606-162">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="29606-162">Read/write</span></span><br><span data-ttu-id="29606-163">Valgfri</span><span class="sxs-lookup"><span data-stu-id="29606-163">Optional</span></span> | <span data-ttu-id="29606-164">Noter til brug af rekrutteringsmedarbejdere eller ansættelseschefer.</span><span class="sxs-lookup"><span data-stu-id="29606-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="29606-165">**Primært felt**</span><span class="sxs-lookup"><span data-stu-id="29606-165">**Primary Field**</span></span><br><span data-ttu-id="29606-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="29606-166">mshr_primaryfield</span></span><br><span data-ttu-id="29606-167">*Streng*</span><span class="sxs-lookup"><span data-stu-id="29606-167">*String*</span></span> | <span data-ttu-id="29606-168">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="29606-168">Read-only</span></span><br><span data-ttu-id="29606-169">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="29606-169">Required</span></span> |  <span data-ttu-id="29606-170">Felt, der bruges som id for enhedsposten.</span><span class="sxs-lookup"><span data-stu-id="29606-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="29606-171">Kombination af partnummer, certifikattype-id og startdato.</span><span class="sxs-lookup"><span data-stu-id="29606-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="29606-172">Se også</span><span class="sxs-lookup"><span data-stu-id="29606-172">See also</span></span>

[<span data-ttu-id="29606-173">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="29606-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="29606-174">Eksempelforespørgsel til ansøger til ansættelse</span><span class="sxs-lookup"><span data-stu-id="29606-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

