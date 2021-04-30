---
title: Plan for fast løn
description: Dette emne indeholder detaljer og en eksempelforespørgsel til enheden Plan for fast løn i Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 78a274cc491041d3d917a50bfb433f667cd8c255
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881953"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="ad0bc-103">Plan for fast løn</span><span class="sxs-lookup"><span data-stu-id="ad0bc-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ad0bc-104">Dette emne indeholder detaljer og en eksempelforespørgsel til enheden Plan for fast løn i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ad0bc-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="ad0bc-105">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="ad0bc-105">Properties</span></span>

| <span data-ttu-id="ad0bc-106">Egenskab</span><span class="sxs-lookup"><span data-stu-id="ad0bc-106">Property</span></span><br><span data-ttu-id="ad0bc-107">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="ad0bc-107">**Physical name**</span></span><br><span data-ttu-id="ad0bc-108">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="ad0bc-108">**_Type_**</span></span> | <span data-ttu-id="ad0bc-109">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="ad0bc-109">Use</span></span> | <span data-ttu-id="ad0bc-110">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="ad0bc-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ad0bc-111">**Medarbejder-id**</span><span class="sxs-lookup"><span data-stu-id="ad0bc-111">**Employee ID**</span></span><br><span data-ttu-id="ad0bc-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="ad0bc-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="ad0bc-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ad0bc-113">*GUID*</span></span> | <span data-ttu-id="ad0bc-114">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-114">Read-only</span></span><br><span data-ttu-id="ad0bc-115">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-115">Required</span></span><br><span data-ttu-id="ad0bc-116">Fremmednøgle: mshr_Employee_id for mshr_payrollemployeeentity enhed</span><span class="sxs-lookup"><span data-stu-id="ad0bc-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="ad0bc-117">Medarbejder-id</span><span class="sxs-lookup"><span data-stu-id="ad0bc-117">Employee ID</span></span> |
| <span data-ttu-id="ad0bc-118">**Lønsats**</span><span class="sxs-lookup"><span data-stu-id="ad0bc-118">**Pay rate**</span></span><br><span data-ttu-id="ad0bc-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="ad0bc-119">mshr_payrate</span></span><br><span data-ttu-id="ad0bc-120">*Decimal*</span><span class="sxs-lookup"><span data-stu-id="ad0bc-120">*Decimal*</span></span> | <span data-ttu-id="ad0bc-121">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-121">Read-only</span></span><br><span data-ttu-id="ad0bc-122">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-122">Required</span></span> | <span data-ttu-id="ad0bc-123">Lønsats, der er defineret i Plan for fast løn.</span><span class="sxs-lookup"><span data-stu-id="ad0bc-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="ad0bc-124">**Plan-id**</span><span class="sxs-lookup"><span data-stu-id="ad0bc-124">**Plan ID**</span></span><br><span data-ttu-id="ad0bc-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="ad0bc-125">mshr_planid</span></span><br><span data-ttu-id="ad0bc-126">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ad0bc-126">*String*</span></span> | <span data-ttu-id="ad0bc-127">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-127">Read-only</span></span><br><span data-ttu-id="ad0bc-128">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-128">Required</span></span> |<span data-ttu-id="ad0bc-129">Angiver lønplanen.</span><span class="sxs-lookup"><span data-stu-id="ad0bc-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="ad0bc-130">**Gyldig fra**</span><span class="sxs-lookup"><span data-stu-id="ad0bc-130">**Valid from**</span></span><br><span data-ttu-id="ad0bc-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="ad0bc-131">mshr_validfrom</span></span><br><span data-ttu-id="ad0bc-132">*Dato- og klokkeslætsforskydning*</span><span class="sxs-lookup"><span data-stu-id="ad0bc-132">*Date Time Offset*</span></span> |  <span data-ttu-id="ad0bc-133">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-133">Read-only</span></span><br><span data-ttu-id="ad0bc-134">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-134">Required</span></span> |<span data-ttu-id="ad0bc-135">Dato, hvorfra medarbejderens faste løn er gyldig.</span><span class="sxs-lookup"><span data-stu-id="ad0bc-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="ad0bc-136">**Enheden Plan for fast løn**</span><span class="sxs-lookup"><span data-stu-id="ad0bc-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="ad0bc-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="ad0bc-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="ad0bc-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ad0bc-138">*GUID*</span></span> | <span data-ttu-id="ad0bc-139">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-139">Required</span></span><br><span data-ttu-id="ad0bc-140">Systemgenereret</span><span class="sxs-lookup"><span data-stu-id="ad0bc-140">Sytem generated</span></span> | <span data-ttu-id="ad0bc-141">Systemgenereret GUID-værdi, der entydigt identificerer lønplanen.</span><span class="sxs-lookup"><span data-stu-id="ad0bc-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="ad0bc-142">**Lønfrekvens**</span><span class="sxs-lookup"><span data-stu-id="ad0bc-142">**Pay frequency**</span></span><br><span data-ttu-id="ad0bc-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="ad0bc-143">mshr_payfrequency</span></span><br><span data-ttu-id="ad0bc-144">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ad0bc-144">*String*</span></span> | <span data-ttu-id="ad0bc-145">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-145">Read-only</span></span><br><span data-ttu-id="ad0bc-146">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-146">Required</span></span> |<span data-ttu-id="ad0bc-147">Hvor ofte medarbejderen bliver betalt.</span><span class="sxs-lookup"><span data-stu-id="ad0bc-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="ad0bc-148">**Gyldig til**</span><span class="sxs-lookup"><span data-stu-id="ad0bc-148">**Valid to**</span></span><br><span data-ttu-id="ad0bc-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="ad0bc-149">mshr_validto</span></span><br><span data-ttu-id="ad0bc-150">*Dato- og klokkeslætsforskydning*</span><span class="sxs-lookup"><span data-stu-id="ad0bc-150">*Date Time Offset*</span></span> | <span data-ttu-id="ad0bc-151">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-151">Read-only</span></span> <br><span data-ttu-id="ad0bc-152">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-152">Required</span></span> | <span data-ttu-id="ad0bc-153">Dato, hvortil medarbejderens faste løn er gyldig.</span><span class="sxs-lookup"><span data-stu-id="ad0bc-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="ad0bc-154">**Stillings-id**</span><span class="sxs-lookup"><span data-stu-id="ad0bc-154">**Position ID**</span></span><br><span data-ttu-id="ad0bc-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="ad0bc-155">mshr_positionid</span></span><br><span data-ttu-id="ad0bc-156">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ad0bc-156">*String*</span></span> | <span data-ttu-id="ad0bc-157">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-157">Read-only</span></span> <br><span data-ttu-id="ad0bc-158">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-158">Required</span></span> | <span data-ttu-id="ad0bc-159">Stillings-id, der er tilknyttet medarbejderen og tilmelding til Plan for fast løn.</span><span class="sxs-lookup"><span data-stu-id="ad0bc-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="ad0bc-160">**Valuta**</span><span class="sxs-lookup"><span data-stu-id="ad0bc-160">**Currency**</span></span><br><span data-ttu-id="ad0bc-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="ad0bc-161">mshr_currency</span></span><br><span data-ttu-id="ad0bc-162">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ad0bc-162">*String*</span></span> | <span data-ttu-id="ad0bc-163">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-163">Read-only</span></span> <br><span data-ttu-id="ad0bc-164">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-164">Required</span></span> |<span data-ttu-id="ad0bc-165">Den valuta, der er defineret for Plan for fast løn</span><span class="sxs-lookup"><span data-stu-id="ad0bc-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="ad0bc-166">**Personalenummer**</span><span class="sxs-lookup"><span data-stu-id="ad0bc-166">**Personnel number**</span></span><br><span data-ttu-id="ad0bc-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="ad0bc-167">mshr_personnelnumber</span></span><br><span data-ttu-id="ad0bc-168">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ad0bc-168">*String*</span></span> | <span data-ttu-id="ad0bc-169">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-169">Read-only</span></span><br><span data-ttu-id="ad0bc-170">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ad0bc-170">Required</span></span> |<span data-ttu-id="ad0bc-171">Medarbejderens entydige personalenummer.</span><span class="sxs-lookup"><span data-stu-id="ad0bc-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="ad0bc-172">**Forespørgsel**</span><span class="sxs-lookup"><span data-stu-id="ad0bc-172">**Query**</span></span>

<span data-ttu-id="ad0bc-173">**Anmodning**</span><span class="sxs-lookup"><span data-stu-id="ad0bc-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="ad0bc-174">**Svar**</span><span class="sxs-lookup"><span data-stu-id="ad0bc-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
