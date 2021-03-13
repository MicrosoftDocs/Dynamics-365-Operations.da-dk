---
title: Screeningstyper
description: Dette emne beskriver enheden Screeningtyper til Dynamics 365 Human Resources.
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
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126164"
---
# <a name="screening-types"></a><span data-ttu-id="ff555-103">Screeningstyper</span><span class="sxs-lookup"><span data-stu-id="ff555-103">Screening types</span></span>

<span data-ttu-id="ff555-104">Dette emne beskriver enheden Screeningtyper til Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ff555-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ff555-105">Fysisk navn: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="ff555-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="ff555-106">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="ff555-106">Description</span></span>

<span data-ttu-id="ff555-107">Denne enhed beskriver de screeningtyper, firmaet har konfigureret for præ-ansættelse og igangværende medarbejder-screeningprocesser.</span><span class="sxs-lookup"><span data-stu-id="ff555-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ff555-108">JSON-repræsentation</span><span class="sxs-lookup"><span data-stu-id="ff555-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="ff555-109">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="ff555-109">Properties</span></span>

| <span data-ttu-id="ff555-110">Egenskab</span><span class="sxs-lookup"><span data-stu-id="ff555-110">Property</span></span><br><span data-ttu-id="ff555-111">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="ff555-111">**Physical name**</span></span><br><span data-ttu-id="ff555-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="ff555-112">**_Type_**</span></span> | <span data-ttu-id="ff555-113">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="ff555-113">Use</span></span> | <span data-ttu-id="ff555-114">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="ff555-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ff555-115">**Enheds-id for screeningstype**</span><span class="sxs-lookup"><span data-stu-id="ff555-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="ff555-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="ff555-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="ff555-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ff555-117">*GUID*</span></span> | <span data-ttu-id="ff555-118">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="ff555-118">Read-only</span></span><br><span data-ttu-id="ff555-119">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ff555-119">Required</span></span><br><span data-ttu-id="ff555-120">Systemgenereret</span><span class="sxs-lookup"><span data-stu-id="ff555-120">System-generated</span></span> | <span data-ttu-id="ff555-121">Entydigt primært id for screeningtypepost.</span><span class="sxs-lookup"><span data-stu-id="ff555-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="ff555-122">**Screeningstype-id**</span><span class="sxs-lookup"><span data-stu-id="ff555-122">**Screening Type ID**</span></span><br><span data-ttu-id="ff555-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="ff555-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="ff555-124">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ff555-124">*String*</span></span> | <span data-ttu-id="ff555-125">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="ff555-125">Read/write</span></span><br><span data-ttu-id="ff555-126">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ff555-126">Required</span></span> | <span data-ttu-id="ff555-127">Brugerdefineret entydig id for screeningtype.</span><span class="sxs-lookup"><span data-stu-id="ff555-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="ff555-128">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="ff555-128">**Description**</span></span><br><span data-ttu-id="ff555-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="ff555-129">mshr_description</span></span><br><span data-ttu-id="ff555-130">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ff555-130">*String*</span></span> | <span data-ttu-id="ff555-131">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="ff555-131">Read/write</span></span><br><span data-ttu-id="ff555-132">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ff555-132">Required</span></span> | <span data-ttu-id="ff555-133">Beskrivelsen af screeningtypen.</span><span class="sxs-lookup"><span data-stu-id="ff555-133">The description of the screening type.</span></span> |
| <span data-ttu-id="ff555-134">**Frekvensenhed**</span><span class="sxs-lookup"><span data-stu-id="ff555-134">**Frequency Unit**</span></span><br><span data-ttu-id="ff555-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="ff555-135">mshr_frequencyunit</span></span><br><span data-ttu-id="ff555-136">*mshr_hcmfrequencyunit-indstilling*</span><span class="sxs-lookup"><span data-stu-id="ff555-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="ff555-137">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="ff555-137">Read/write</span></span><br><span data-ttu-id="ff555-138">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ff555-138">Required</span></span> | <span data-ttu-id="ff555-139">Beskriver, hvor ofte screeningen skal fuldføres for den tildelte person.</span><span class="sxs-lookup"><span data-stu-id="ff555-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="ff555-140">**Generér fra**</span><span class="sxs-lookup"><span data-stu-id="ff555-140">**Generate From**</span></span><br><span data-ttu-id="ff555-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="ff555-141">mshr_generatefrom</span></span><br><span data-ttu-id="ff555-142">*mshr_hcmfrequencygeneratefrom-indstilling*</span><span class="sxs-lookup"><span data-stu-id="ff555-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="ff555-143">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="ff555-143">Read-write</span></span><br><span data-ttu-id="ff555-144">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ff555-144">Required</span></span> | <span data-ttu-id="ff555-145">Hvis værdien for Frekvens er en anden værdi end "Kun én gang", bestemmer Værdien GenerateFrom den dato, den næste screeninghændelse skal beregnes fra.</span><span class="sxs-lookup"><span data-stu-id="ff555-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="ff555-146">**Frekvensinterval**</span><span class="sxs-lookup"><span data-stu-id="ff555-146">**Frequency Interval**</span></span><br><span data-ttu-id="ff555-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="ff555-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="ff555-148">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="ff555-148">*Integer*</span></span> | <span data-ttu-id="ff555-149">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="ff555-149">Read-write</span></span><br><span data-ttu-id="ff555-150">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ff555-150">Required</span></span> | <span data-ttu-id="ff555-151">Hvis frekvensværdien har en anden værdi end "Kun én gang", skal du definere et interval for tidsenhederne mellem hver enkelt screeninghændelse.</span><span class="sxs-lookup"><span data-stu-id="ff555-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ff555-152">Se også</span><span class="sxs-lookup"><span data-stu-id="ff555-152">See also</span></span>

[<span data-ttu-id="ff555-153">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="ff555-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ff555-154">Eksempelforespørgsel til ansøger til ansættelse</span><span class="sxs-lookup"><span data-stu-id="ff555-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
