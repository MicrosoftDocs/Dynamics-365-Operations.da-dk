---
title: Screeningstyper
description: Dette emne beskriver enheden Screeningtyper til Dynamics 365 Human Resources.
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
ms.openlocfilehash: 361f8c866abb9d34eb3e2be7ea42626e98e34779
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805124"
---
# <a name="screening-types"></a><span data-ttu-id="83574-103">Screeningstyper</span><span class="sxs-lookup"><span data-stu-id="83574-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="83574-104">Dette emne beskriver enheden Screeningtyper til Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="83574-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="83574-105">Fysisk navn: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="83574-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="83574-106">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="83574-106">Description</span></span>

<span data-ttu-id="83574-107">Denne enhed beskriver de screeningtyper, firmaet har konfigureret for præ-ansættelse og igangværende medarbejder-screeningprocesser.</span><span class="sxs-lookup"><span data-stu-id="83574-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="83574-108">JSON-repræsentation</span><span class="sxs-lookup"><span data-stu-id="83574-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="83574-109">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="83574-109">Properties</span></span>

| <span data-ttu-id="83574-110">Egenskab</span><span class="sxs-lookup"><span data-stu-id="83574-110">Property</span></span><br><span data-ttu-id="83574-111">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="83574-111">**Physical name**</span></span><br><span data-ttu-id="83574-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="83574-112">**_Type_**</span></span> | <span data-ttu-id="83574-113">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="83574-113">Use</span></span> | <span data-ttu-id="83574-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="83574-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="83574-115">**Enheds-id for screeningstype**</span><span class="sxs-lookup"><span data-stu-id="83574-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="83574-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="83574-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="83574-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="83574-117">*GUID*</span></span> | <span data-ttu-id="83574-118">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="83574-118">Read-only</span></span><br><span data-ttu-id="83574-119">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="83574-119">Required</span></span><br><span data-ttu-id="83574-120">Systemgenereret</span><span class="sxs-lookup"><span data-stu-id="83574-120">System-generated</span></span> | <span data-ttu-id="83574-121">Entydigt primært id for screeningtypepost.</span><span class="sxs-lookup"><span data-stu-id="83574-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="83574-122">**Screeningstype-id**</span><span class="sxs-lookup"><span data-stu-id="83574-122">**Screening Type ID**</span></span><br><span data-ttu-id="83574-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="83574-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="83574-124">*Streng*</span><span class="sxs-lookup"><span data-stu-id="83574-124">*String*</span></span> | <span data-ttu-id="83574-125">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="83574-125">Read/write</span></span><br><span data-ttu-id="83574-126">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="83574-126">Required</span></span> | <span data-ttu-id="83574-127">Brugerdefineret entydig id for screeningtype.</span><span class="sxs-lookup"><span data-stu-id="83574-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="83574-128">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="83574-128">**Description**</span></span><br><span data-ttu-id="83574-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="83574-129">mshr_description</span></span><br><span data-ttu-id="83574-130">*Streng*</span><span class="sxs-lookup"><span data-stu-id="83574-130">*String*</span></span> | <span data-ttu-id="83574-131">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="83574-131">Read/write</span></span><br><span data-ttu-id="83574-132">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="83574-132">Required</span></span> | <span data-ttu-id="83574-133">Beskrivelsen af screeningtypen.</span><span class="sxs-lookup"><span data-stu-id="83574-133">The description of the screening type.</span></span> |
| <span data-ttu-id="83574-134">**Frekvensenhed**</span><span class="sxs-lookup"><span data-stu-id="83574-134">**Frequency Unit**</span></span><br><span data-ttu-id="83574-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="83574-135">mshr_frequencyunit</span></span><br><span data-ttu-id="83574-136">*mshr_hcmfrequencyunit-indstilling*</span><span class="sxs-lookup"><span data-stu-id="83574-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="83574-137">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="83574-137">Read/write</span></span><br><span data-ttu-id="83574-138">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="83574-138">Required</span></span> | <span data-ttu-id="83574-139">Beskriver, hvor ofte screeningen skal fuldføres for den tildelte person.</span><span class="sxs-lookup"><span data-stu-id="83574-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="83574-140">**Generér fra**</span><span class="sxs-lookup"><span data-stu-id="83574-140">**Generate From**</span></span><br><span data-ttu-id="83574-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="83574-141">mshr_generatefrom</span></span><br><span data-ttu-id="83574-142">*mshr_hcmfrequencygeneratefrom-indstilling*</span><span class="sxs-lookup"><span data-stu-id="83574-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="83574-143">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="83574-143">Read-write</span></span><br><span data-ttu-id="83574-144">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="83574-144">Required</span></span> | <span data-ttu-id="83574-145">Hvis værdien for Frekvens er en anden værdi end "Kun én gang", bestemmer Værdien GenerateFrom den dato, den næste screeninghændelse skal beregnes fra.</span><span class="sxs-lookup"><span data-stu-id="83574-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="83574-146">**Frekvensinterval**</span><span class="sxs-lookup"><span data-stu-id="83574-146">**Frequency Interval**</span></span><br><span data-ttu-id="83574-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="83574-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="83574-148">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="83574-148">*Integer*</span></span> | <span data-ttu-id="83574-149">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="83574-149">Read-write</span></span><br><span data-ttu-id="83574-150">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="83574-150">Required</span></span> | <span data-ttu-id="83574-151">Hvis frekvensværdien har en anden værdi end "Kun én gang", skal du definere et interval for tidsenhederne mellem hver enkelt screeninghændelse.</span><span class="sxs-lookup"><span data-stu-id="83574-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="83574-152">Se også</span><span class="sxs-lookup"><span data-stu-id="83574-152">See also</span></span>

[<span data-ttu-id="83574-153">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="83574-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="83574-154">Eksempelforespørgsel til ansøger til ansættelse</span><span class="sxs-lookup"><span data-stu-id="83574-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]