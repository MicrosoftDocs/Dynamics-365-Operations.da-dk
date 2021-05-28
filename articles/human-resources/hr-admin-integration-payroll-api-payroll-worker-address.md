---
title: Lønarbejderadresse
description: Dette emne indeholder detaljer og en eksempelforespørgsel til enheden Lønarbejderadresse i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 964f04261ea95ee6fa2880b0905a669855f6c58a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020699"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="bcddb-103">Lønarbejderadresse</span><span class="sxs-lookup"><span data-stu-id="bcddb-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bcddb-104">Dette emne indeholder detaljer og en eksempelforespørgsel til enheden Lønarbejderadresse i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bcddb-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="bcddb-105">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="bcddb-105">Properties</span></span>

| <span data-ttu-id="bcddb-106">Egenskab</span><span class="sxs-lookup"><span data-stu-id="bcddb-106">Property</span></span><br><span data-ttu-id="bcddb-107">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="bcddb-107">**Physical name**</span></span><br><span data-ttu-id="bcddb-108">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="bcddb-108">**_Type_**</span></span> | <span data-ttu-id="bcddb-109">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="bcddb-109">Use</span></span> | <span data-ttu-id="bcddb-110">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="bcddb-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="bcddb-111">**By**</span><span class="sxs-lookup"><span data-stu-id="bcddb-111">**City**</span></span><br><span data-ttu-id="bcddb-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="bcddb-112">mshr_city</span></span><br><span data-ttu-id="bcddb-113">*Streng*</span><span class="sxs-lookup"><span data-stu-id="bcddb-113">*String*</span></span> | <span data-ttu-id="bcddb-114">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="bcddb-114">Read-only</span></span><br><span data-ttu-id="bcddb-115">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="bcddb-115">Required</span></span> | <span data-ttu-id="bcddb-116">Byen, der er defineret for adressen.</span><span class="sxs-lookup"><span data-stu-id="bcddb-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="bcddb-117">**Personalenummer**</span><span class="sxs-lookup"><span data-stu-id="bcddb-117">**Personnel number**</span></span><br><span data-ttu-id="bcddb-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="bcddb-118">mshr_personnelnumber</span></span><br><span data-ttu-id="bcddb-119">*Streng*</span><span class="sxs-lookup"><span data-stu-id="bcddb-119">*String*</span></span> | <span data-ttu-id="bcddb-120">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="bcddb-120">Read-only</span></span><br><span data-ttu-id="bcddb-121">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="bcddb-121">Required</span></span> | <span data-ttu-id="bcddb-122">Medarbejderens entydige personalenummer.</span><span class="sxs-lookup"><span data-stu-id="bcddb-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="bcddb-123">**Land og område**</span><span class="sxs-lookup"><span data-stu-id="bcddb-123">**Country region**</span></span><br><span data-ttu-id="bcddb-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="bcddb-124">mshr_countryregionid</span></span><br><span data-ttu-id="bcddb-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="bcddb-125">*String*</span></span> | <span data-ttu-id="bcddb-126">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="bcddb-126">Read-only</span></span><br><span data-ttu-id="bcddb-127">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="bcddb-127">Required</span></span> | <span data-ttu-id="bcddb-128">Det land og område, der er defineret til adressen</span><span class="sxs-lookup"><span data-stu-id="bcddb-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="bcddb-129">**Gyldig fra**</span><span class="sxs-lookup"><span data-stu-id="bcddb-129">**Valid from**</span></span><br><span data-ttu-id="bcddb-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="bcddb-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="bcddb-131">*Dato- og klokkeslætsforskydning*</span><span class="sxs-lookup"><span data-stu-id="bcddb-131">*Date Time Offset*</span></span> | <span data-ttu-id="bcddb-132">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="bcddb-132">Read-only</span></span> <br><span data-ttu-id="bcddb-133">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="bcddb-133">Required</span></span> | <span data-ttu-id="bcddb-134">Den dato, som adressen gælder fra.</span><span class="sxs-lookup"><span data-stu-id="bcddb-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="bcddb-135">**Arbejdsadresse**</span><span class="sxs-lookup"><span data-stu-id="bcddb-135">**Worked in address**</span></span><br><span data-ttu-id="bcddb-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="bcddb-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="bcddb-137">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="bcddb-137">Read-only</span></span><br><span data-ttu-id="bcddb-138">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="bcddb-138">Required</span></span> | <span data-ttu-id="bcddb-139">Angiver, om adressen er der, hvor medarbejderen arbejder.</span><span class="sxs-lookup"><span data-stu-id="bcddb-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="bcddb-140">**Region**</span><span class="sxs-lookup"><span data-stu-id="bcddb-140">**County**</span></span><br><span data-ttu-id="bcddb-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="bcddb-141">mshr_county</span></span><br><span data-ttu-id="bcddb-142">*Streng*</span><span class="sxs-lookup"><span data-stu-id="bcddb-142">*String*</span></span> | <span data-ttu-id="bcddb-143">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="bcddb-143">Read-only</span></span><br><span data-ttu-id="bcddb-144">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="bcddb-144">Required</span></span> | <span data-ttu-id="bcddb-145">Regionen, der er defineret for adressen.</span><span class="sxs-lookup"><span data-stu-id="bcddb-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="bcddb-146">**Lønarbejderadresse-id**</span><span class="sxs-lookup"><span data-stu-id="bcddb-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="bcddb-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="bcddb-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="bcddb-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="bcddb-148">*GUID*</span></span> | <span data-ttu-id="bcddb-149">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="bcddb-149">Required</span></span><br><span data-ttu-id="bcddb-150">Systemgenereret</span><span class="sxs-lookup"><span data-stu-id="bcddb-150">System generated</span></span> | <span data-ttu-id="bcddb-151">Systemgenereret GUID-værdi, der entydigt identificerer adressen.</span><span class="sxs-lookup"><span data-stu-id="bcddb-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="bcddb-152">**Primært felt**</span><span class="sxs-lookup"><span data-stu-id="bcddb-152">**Primary field**</span></span><br><span data-ttu-id="bcddb-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="bcddb-153">mshr_primaryfield</span></span><br><span data-ttu-id="bcddb-154">*Streng*</span><span class="sxs-lookup"><span data-stu-id="bcddb-154">*String*</span></span> | <span data-ttu-id="bcddb-155">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="bcddb-155">Read-only</span></span><br><span data-ttu-id="bcddb-156">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="bcddb-156">Required</span></span> |  |
| <span data-ttu-id="bcddb-157">**Gade**</span><span class="sxs-lookup"><span data-stu-id="bcddb-157">**Street**</span></span><br><span data-ttu-id="bcddb-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="bcddb-158">mshr_street</span></span><br><span data-ttu-id="bcddb-159">*Streng*</span><span class="sxs-lookup"><span data-stu-id="bcddb-159">*String*</span></span> | <span data-ttu-id="bcddb-160">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="bcddb-160">Read-only</span></span><br><span data-ttu-id="bcddb-161">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="bcddb-161">Required</span></span> | <span data-ttu-id="bcddb-162">Gaden, der er defineret for adressen.</span><span class="sxs-lookup"><span data-stu-id="bcddb-162">The street defined for the address.</span></span> |
| <span data-ttu-id="bcddb-163">**Gyldig til**</span><span class="sxs-lookup"><span data-stu-id="bcddb-163">**Valid to**</span></span><br><span data-ttu-id="bcddb-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="bcddb-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="bcddb-165">*Dato- og klokkeslætsforskydning*</span><span class="sxs-lookup"><span data-stu-id="bcddb-165">*Date Time Offset*</span></span> | <span data-ttu-id="bcddb-166">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="bcddb-166">Read-only</span></span> <br><span data-ttu-id="bcddb-167">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="bcddb-167">Required</span></span> | <span data-ttu-id="bcddb-168">Den dato, som adressen gælder til.</span><span class="sxs-lookup"><span data-stu-id="bcddb-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="bcddb-169">**Lokations-id**</span><span class="sxs-lookup"><span data-stu-id="bcddb-169">**Location ID**</span></span><br><span data-ttu-id="bcddb-170">mshr_locationidbr>*Streng*</span><span class="sxs-lookup"><span data-stu-id="bcddb-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="bcddb-171">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="bcddb-171">Read-only</span></span> <br><span data-ttu-id="bcddb-172">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="bcddb-172">Required</span></span> | <span data-ttu-id="bcddb-173">Adressens id.</span><span class="sxs-lookup"><span data-stu-id="bcddb-173">The ID for the address.</span></span>  |
| <span data-ttu-id="bcddb-174">**Postnummer**</span><span class="sxs-lookup"><span data-stu-id="bcddb-174">**Postal code**</span></span><br><span data-ttu-id="bcddb-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="bcddb-175">mshr_zipcode</span></span><br><span data-ttu-id="bcddb-176">*Streng*</span><span class="sxs-lookup"><span data-stu-id="bcddb-176">*String*</span></span> | <span data-ttu-id="bcddb-177">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="bcddb-177">Read-only</span></span> <br><span data-ttu-id="bcddb-178">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="bcddb-178">Required</span></span> |<span data-ttu-id="bcddb-179">Det identifikationsnummer, der er defineret for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="bcddb-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="bcddb-180">**Bopælsadresse**</span><span class="sxs-lookup"><span data-stu-id="bcddb-180">**Lived in address**</span></span><br><span data-ttu-id="bcddb-181">mshr_islivedinaddressbr>*Streng*</span><span class="sxs-lookup"><span data-stu-id="bcddb-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="bcddb-182">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="bcddb-182">Read-only</span></span><br><span data-ttu-id="bcddb-183">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="bcddb-183">Required</span></span> | <span data-ttu-id="bcddb-184">Angiver, om adressen er der, hvor medarbejderen bor.</span><span class="sxs-lookup"><span data-stu-id="bcddb-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="bcddb-185">**Stat**</span><span class="sxs-lookup"><span data-stu-id="bcddb-185">**State**</span></span><br><span data-ttu-id="bcddb-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="bcddb-186">mshr_state</span></span><br><span data-ttu-id="bcddb-187">*Streng*</span><span class="sxs-lookup"><span data-stu-id="bcddb-187">*String*</span></span> | <span data-ttu-id="bcddb-188">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="bcddb-188">Read-only</span></span><br><span data-ttu-id="bcddb-189">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="bcddb-189">Required</span></span> | <span data-ttu-id="bcddb-190">Delstaten, der er defineret for adressen.</span><span class="sxs-lookup"><span data-stu-id="bcddb-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="bcddb-191">Eksempelforespørgsel</span><span class="sxs-lookup"><span data-stu-id="bcddb-191">Example query</span></span>

<span data-ttu-id="bcddb-192">**Anmodning**</span><span class="sxs-lookup"><span data-stu-id="bcddb-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="bcddb-193">**Svar**</span><span class="sxs-lookup"><span data-stu-id="bcddb-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
