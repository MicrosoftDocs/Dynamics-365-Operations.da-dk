---
title: Lønoplysninger for stillinger
description: Dette emne indeholder detaljer og en eksempelforespørgsel til stillingsenhedens lønoplysninger i Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8918044dbf84e79015dc3bca904f204123a37db8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056774"
---
# <a name="payroll-position"></a><span data-ttu-id="8bda1-103">Lønstilling</span><span class="sxs-lookup"><span data-stu-id="8bda1-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8bda1-104">Dette emne indeholder detaljer og en eksempelforespørgsel til stillingsenhedens lønoplysninger i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8bda1-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="8bda1-105">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="8bda1-105">Properties</span></span>

| <span data-ttu-id="8bda1-106">Egenskab</span><span class="sxs-lookup"><span data-stu-id="8bda1-106">Property</span></span><br><span data-ttu-id="8bda1-107">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="8bda1-107">**Physical name**</span></span><br><span data-ttu-id="8bda1-108">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="8bda1-108">**_Type_**</span></span> | <span data-ttu-id="8bda1-109">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="8bda1-109">Use</span></span> | <span data-ttu-id="8bda1-110">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="8bda1-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8bda1-111">**Normaltimer på årsbasis**</span><span class="sxs-lookup"><span data-stu-id="8bda1-111">**Annual regular hours**</span></span><br><span data-ttu-id="8bda1-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="8bda1-112">annualregularhours</span></span><br><span data-ttu-id="8bda1-113">*Decimal*</span><span class="sxs-lookup"><span data-stu-id="8bda1-113">*Decimal*</span></span> | <span data-ttu-id="8bda1-114">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="8bda1-114">Read-only</span></span><br><span data-ttu-id="8bda1-115">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="8bda1-115">Required</span></span> | <span data-ttu-id="8bda1-116">Årlige regelmæssige timer, der er defineret på stillingen.</span><span class="sxs-lookup"><span data-stu-id="8bda1-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="8bda1-117">**Enheds-id til lønoplysninger for stillinger**</span><span class="sxs-lookup"><span data-stu-id="8bda1-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="8bda1-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="8bda1-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="8bda1-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="8bda1-119">*Guid*</span></span> | <span data-ttu-id="8bda1-120">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="8bda1-120">Required</span></span><br><span data-ttu-id="8bda1-121">Systemgenereret.</span><span class="sxs-lookup"><span data-stu-id="8bda1-121">System generated.</span></span> | <span data-ttu-id="8bda1-122">Systemgenereret GUID-værdi, der entydigt identificerer stillingen.</span><span class="sxs-lookup"><span data-stu-id="8bda1-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="8bda1-123">**Primært felt**</span><span class="sxs-lookup"><span data-stu-id="8bda1-123">**Primary field**</span></span><br><span data-ttu-id="8bda1-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="8bda1-124">mshr_primaryfield</span></span><br><span data-ttu-id="8bda1-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="8bda1-125">*String*</span></span> | <span data-ttu-id="8bda1-126">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="8bda1-126">Required</span></span><br><span data-ttu-id="8bda1-127">Systemgenereret</span><span class="sxs-lookup"><span data-stu-id="8bda1-127">System generated</span></span> |  |
| <span data-ttu-id="8bda1-128">**Stillingsjob-id-værdi**</span><span class="sxs-lookup"><span data-stu-id="8bda1-128">**Position job ID value**</span></span><br><span data-ttu-id="8bda1-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="8bda1-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="8bda1-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="8bda1-130">*GUID*</span></span> | <span data-ttu-id="8bda1-131">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="8bda1-131">Read-only</span></span><br><span data-ttu-id="8bda1-132">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="8bda1-132">Required</span></span><br><span data-ttu-id="8bda1-133">Fremmed nøgle: mshr_PayrollPositionJobEntity for mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="8bda1-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="8bda1-134">Id for det job, der er tilknyttet stillingen.</span><span class="sxs-lookup"><span data-stu-id="8bda1-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="8bda1-135">**Id-værdi til plan for fast løn**</span><span class="sxs-lookup"><span data-stu-id="8bda1-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="8bda1-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="8bda1-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="8bda1-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="8bda1-137">*GUID*</span></span> | <span data-ttu-id="8bda1-138">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="8bda1-138">Read-only</span></span><br><span data-ttu-id="8bda1-139">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="8bda1-139">Required</span></span><br><span data-ttu-id="8bda1-140">Fremmed nøgle: mshr_FixedCompPlan_id for mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="8bda1-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="8bda1-141">Id for planen for fast løn, der er tilknyttet stillingen.</span><span class="sxs-lookup"><span data-stu-id="8bda1-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="8bda1-142">**Betalingscyklus-id**</span><span class="sxs-lookup"><span data-stu-id="8bda1-142">**Pay cycle ID**</span></span><br><span data-ttu-id="8bda1-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="8bda1-143">mshr_primaryfield</span></span><br><span data-ttu-id="8bda1-144">*Streng*</span><span class="sxs-lookup"><span data-stu-id="8bda1-144">*String*</span></span> | <span data-ttu-id="8bda1-145">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="8bda1-145">Read-only</span></span><br><span data-ttu-id="8bda1-146">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="8bda1-146">Required</span></span> | <span data-ttu-id="8bda1-147">Den løncyklus, der er defineret på stillingen.</span><span class="sxs-lookup"><span data-stu-id="8bda1-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="8bda1-148">**Betalt af juridisk enhed**</span><span class="sxs-lookup"><span data-stu-id="8bda1-148">**Paid by legal entity**</span></span><br><span data-ttu-id="8bda1-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="8bda1-149">paidbylegalentity</span></span><br><span data-ttu-id="8bda1-150">*Streng*</span><span class="sxs-lookup"><span data-stu-id="8bda1-150">*String*</span></span> | <span data-ttu-id="8bda1-151">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="8bda1-151">Read-only</span></span><br><span data-ttu-id="8bda1-152">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="8bda1-152">Required</span></span> | <span data-ttu-id="8bda1-153">Den juridiske enhed, der er defineret på den stilling, der er ansvarlig for udstedelse af betaling.</span><span class="sxs-lookup"><span data-stu-id="8bda1-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="8bda1-154">**Stillings-id**</span><span class="sxs-lookup"><span data-stu-id="8bda1-154">**Position ID**</span></span><br><span data-ttu-id="8bda1-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="8bda1-155">mshr_positionid</span></span><br><span data-ttu-id="8bda1-156">*Streng*</span><span class="sxs-lookup"><span data-stu-id="8bda1-156">*String*</span></span> | <span data-ttu-id="8bda1-157">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="8bda1-157">Read-only</span></span><br><span data-ttu-id="8bda1-158">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="8bda1-158">Required</span></span> | <span data-ttu-id="8bda1-159">Stillingens id.</span><span class="sxs-lookup"><span data-stu-id="8bda1-159">The ID of the position.</span></span> |
| <span data-ttu-id="8bda1-160">**Gyldig til**</span><span class="sxs-lookup"><span data-stu-id="8bda1-160">**Valid to**</span></span><br><span data-ttu-id="8bda1-161">validto</span><span class="sxs-lookup"><span data-stu-id="8bda1-161">validto</span></span><br><span data-ttu-id="8bda1-162">*Dato- og klokkeslætsforskydning*</span><span class="sxs-lookup"><span data-stu-id="8bda1-162">*Date Time Offset*</span></span> | <span data-ttu-id="8bda1-163">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="8bda1-163">Read-only</span></span><br><span data-ttu-id="8bda1-164">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="8bda1-164">Required</span></span> |<span data-ttu-id="8bda1-165">Den dato, hvor stillingsoplysningerne er gyldige fra.</span><span class="sxs-lookup"><span data-stu-id="8bda1-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="8bda1-166">**Gyldig fra**</span><span class="sxs-lookup"><span data-stu-id="8bda1-166">**Valid from**</span></span><br><span data-ttu-id="8bda1-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="8bda1-167">validfrom</span></span><br><span data-ttu-id="8bda1-168">*Dato- og klokkeslætsforskydning*</span><span class="sxs-lookup"><span data-stu-id="8bda1-168">*Date Time Offset*</span></span> | <span data-ttu-id="8bda1-169">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="8bda1-169">Read-only</span></span><br><span data-ttu-id="8bda1-170">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="8bda1-170">Required</span></span> |<span data-ttu-id="8bda1-171">Den dato, hvor stillingsoplysningerne er gyldige til.</span><span class="sxs-lookup"><span data-stu-id="8bda1-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="8bda1-172">**Forespørgsel**</span><span class="sxs-lookup"><span data-stu-id="8bda1-172">**Query**</span></span>

<span data-ttu-id="8bda1-173">**Anmodning**</span><span class="sxs-lookup"><span data-stu-id="8bda1-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="8bda1-174">**Svar**</span><span class="sxs-lookup"><span data-stu-id="8bda1-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
