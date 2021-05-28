---
title: Plan for fast løn
description: Dette emne indeholder detaljer og en eksempelforespørgsel til enheden Plan for fast løn i Dynamics 365 Human Resources.
author: jcart
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
ms.openlocfilehash: 85cfce6f626090adab422ea6c60fc0778fd1ac67
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021290"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="1fb9c-103">Plan for fast løn</span><span class="sxs-lookup"><span data-stu-id="1fb9c-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1fb9c-104">Dette emne indeholder detaljer og en eksempelforespørgsel til enheden Plan for fast løn i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1fb9c-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="1fb9c-105">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="1fb9c-105">Properties</span></span>

| <span data-ttu-id="1fb9c-106">Egenskab</span><span class="sxs-lookup"><span data-stu-id="1fb9c-106">Property</span></span><br><span data-ttu-id="1fb9c-107">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="1fb9c-107">**Physical name**</span></span><br><span data-ttu-id="1fb9c-108">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="1fb9c-108">**_Type_**</span></span> | <span data-ttu-id="1fb9c-109">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="1fb9c-109">Use</span></span> | <span data-ttu-id="1fb9c-110">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="1fb9c-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1fb9c-111">**Medarbejder-id**</span><span class="sxs-lookup"><span data-stu-id="1fb9c-111">**Employee ID**</span></span><br><span data-ttu-id="1fb9c-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="1fb9c-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="1fb9c-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="1fb9c-113">*GUID*</span></span> | <span data-ttu-id="1fb9c-114">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-114">Read-only</span></span><br><span data-ttu-id="1fb9c-115">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-115">Required</span></span><br><span data-ttu-id="1fb9c-116">Fremmednøgle: mshr_Employee_id for mshr_payrollemployeeentity enhed</span><span class="sxs-lookup"><span data-stu-id="1fb9c-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="1fb9c-117">Medarbejder-id</span><span class="sxs-lookup"><span data-stu-id="1fb9c-117">Employee ID</span></span> |
| <span data-ttu-id="1fb9c-118">**Lønsats**</span><span class="sxs-lookup"><span data-stu-id="1fb9c-118">**Pay rate**</span></span><br><span data-ttu-id="1fb9c-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="1fb9c-119">mshr_payrate</span></span><br><span data-ttu-id="1fb9c-120">*Decimal*</span><span class="sxs-lookup"><span data-stu-id="1fb9c-120">*Decimal*</span></span> | <span data-ttu-id="1fb9c-121">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-121">Read-only</span></span><br><span data-ttu-id="1fb9c-122">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-122">Required</span></span> | <span data-ttu-id="1fb9c-123">Lønsats, der er defineret i Plan for fast løn.</span><span class="sxs-lookup"><span data-stu-id="1fb9c-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="1fb9c-124">**Plan-id**</span><span class="sxs-lookup"><span data-stu-id="1fb9c-124">**Plan ID**</span></span><br><span data-ttu-id="1fb9c-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="1fb9c-125">mshr_planid</span></span><br><span data-ttu-id="1fb9c-126">*Streng*</span><span class="sxs-lookup"><span data-stu-id="1fb9c-126">*String*</span></span> | <span data-ttu-id="1fb9c-127">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-127">Read-only</span></span><br><span data-ttu-id="1fb9c-128">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-128">Required</span></span> |<span data-ttu-id="1fb9c-129">Angiver lønplanen.</span><span class="sxs-lookup"><span data-stu-id="1fb9c-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="1fb9c-130">**Gyldig fra**</span><span class="sxs-lookup"><span data-stu-id="1fb9c-130">**Valid from**</span></span><br><span data-ttu-id="1fb9c-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="1fb9c-131">mshr_validfrom</span></span><br><span data-ttu-id="1fb9c-132">*Dato- og klokkeslætsforskydning*</span><span class="sxs-lookup"><span data-stu-id="1fb9c-132">*Date Time Offset*</span></span> |  <span data-ttu-id="1fb9c-133">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-133">Read-only</span></span><br><span data-ttu-id="1fb9c-134">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-134">Required</span></span> |<span data-ttu-id="1fb9c-135">Dato, hvorfra medarbejderens faste løn er gyldig.</span><span class="sxs-lookup"><span data-stu-id="1fb9c-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="1fb9c-136">**Enheden Plan for fast løn**</span><span class="sxs-lookup"><span data-stu-id="1fb9c-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="1fb9c-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="1fb9c-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="1fb9c-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="1fb9c-138">*GUID*</span></span> | <span data-ttu-id="1fb9c-139">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-139">Required</span></span><br><span data-ttu-id="1fb9c-140">Systemgenereret</span><span class="sxs-lookup"><span data-stu-id="1fb9c-140">Sytem generated</span></span> | <span data-ttu-id="1fb9c-141">Systemgenereret GUID-værdi, der entydigt identificerer lønplanen.</span><span class="sxs-lookup"><span data-stu-id="1fb9c-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="1fb9c-142">**Lønfrekvens**</span><span class="sxs-lookup"><span data-stu-id="1fb9c-142">**Pay frequency**</span></span><br><span data-ttu-id="1fb9c-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="1fb9c-143">mshr_payfrequency</span></span><br><span data-ttu-id="1fb9c-144">*Streng*</span><span class="sxs-lookup"><span data-stu-id="1fb9c-144">*String*</span></span> | <span data-ttu-id="1fb9c-145">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-145">Read-only</span></span><br><span data-ttu-id="1fb9c-146">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-146">Required</span></span> |<span data-ttu-id="1fb9c-147">Hvor ofte medarbejderen bliver betalt.</span><span class="sxs-lookup"><span data-stu-id="1fb9c-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="1fb9c-148">**Gyldig til**</span><span class="sxs-lookup"><span data-stu-id="1fb9c-148">**Valid to**</span></span><br><span data-ttu-id="1fb9c-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="1fb9c-149">mshr_validto</span></span><br><span data-ttu-id="1fb9c-150">*Dato- og klokkeslætsforskydning*</span><span class="sxs-lookup"><span data-stu-id="1fb9c-150">*Date Time Offset*</span></span> | <span data-ttu-id="1fb9c-151">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-151">Read-only</span></span> <br><span data-ttu-id="1fb9c-152">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-152">Required</span></span> | <span data-ttu-id="1fb9c-153">Dato, hvortil medarbejderens faste løn er gyldig.</span><span class="sxs-lookup"><span data-stu-id="1fb9c-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="1fb9c-154">**Stillings-id**</span><span class="sxs-lookup"><span data-stu-id="1fb9c-154">**Position ID**</span></span><br><span data-ttu-id="1fb9c-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="1fb9c-155">mshr_positionid</span></span><br><span data-ttu-id="1fb9c-156">*Streng*</span><span class="sxs-lookup"><span data-stu-id="1fb9c-156">*String*</span></span> | <span data-ttu-id="1fb9c-157">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-157">Read-only</span></span> <br><span data-ttu-id="1fb9c-158">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-158">Required</span></span> | <span data-ttu-id="1fb9c-159">Stillings-id, der er tilknyttet medarbejderen og tilmelding til Plan for fast løn.</span><span class="sxs-lookup"><span data-stu-id="1fb9c-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="1fb9c-160">**Valuta**</span><span class="sxs-lookup"><span data-stu-id="1fb9c-160">**Currency**</span></span><br><span data-ttu-id="1fb9c-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="1fb9c-161">mshr_currency</span></span><br><span data-ttu-id="1fb9c-162">*Streng*</span><span class="sxs-lookup"><span data-stu-id="1fb9c-162">*String*</span></span> | <span data-ttu-id="1fb9c-163">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-163">Read-only</span></span> <br><span data-ttu-id="1fb9c-164">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-164">Required</span></span> |<span data-ttu-id="1fb9c-165">Den valuta, der er defineret for Plan for fast løn</span><span class="sxs-lookup"><span data-stu-id="1fb9c-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="1fb9c-166">**Personalenummer**</span><span class="sxs-lookup"><span data-stu-id="1fb9c-166">**Personnel number**</span></span><br><span data-ttu-id="1fb9c-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="1fb9c-167">mshr_personnelnumber</span></span><br><span data-ttu-id="1fb9c-168">*Streng*</span><span class="sxs-lookup"><span data-stu-id="1fb9c-168">*String*</span></span> | <span data-ttu-id="1fb9c-169">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-169">Read-only</span></span><br><span data-ttu-id="1fb9c-170">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="1fb9c-170">Required</span></span> |<span data-ttu-id="1fb9c-171">Medarbejderens entydige personalenummer.</span><span class="sxs-lookup"><span data-stu-id="1fb9c-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="1fb9c-172">**Forespørgsel**</span><span class="sxs-lookup"><span data-stu-id="1fb9c-172">**Query**</span></span>

<span data-ttu-id="1fb9c-173">**Anmodning**</span><span class="sxs-lookup"><span data-stu-id="1fb9c-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="1fb9c-174">**Svar**</span><span class="sxs-lookup"><span data-stu-id="1fb9c-174">**Response**</span></span>

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
