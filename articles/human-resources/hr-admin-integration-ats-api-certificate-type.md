---
title: Certifikattype
description: Dette emne beskriver certifikatstypeenheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: fe5713b6b5f38ad7f6857b36c6b2f63a1dc0c320
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798386"
---
# <a name="certificate-type"></a><span data-ttu-id="ef7fb-103">Certifikattype</span><span class="sxs-lookup"><span data-stu-id="ef7fb-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ef7fb-104">Dette emne beskriver certifikatstypeenheden til Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ef7fb-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ef7fb-105">Fysisk navn: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="ef7fb-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="ef7fb-106">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ef7fb-106">Description</span></span>

<span data-ttu-id="ef7fb-107">Denne enhed definerer listen over typer af professionelle certifikater, der er defineret i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ef7fb-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="ef7fb-108">Enheden er ikke specifik for en juridisk enhed (firma).</span><span class="sxs-lookup"><span data-stu-id="ef7fb-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="ef7fb-109">JSON-repræsentation</span><span class="sxs-lookup"><span data-stu-id="ef7fb-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="ef7fb-110">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="ef7fb-110">Properties</span></span>

| <span data-ttu-id="ef7fb-111">Egenskab</span><span class="sxs-lookup"><span data-stu-id="ef7fb-111">Property</span></span><br><span data-ttu-id="ef7fb-112">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="ef7fb-112">**Physical name**</span></span><br><span data-ttu-id="ef7fb-113">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="ef7fb-113">**_Type_**</span></span> | <span data-ttu-id="ef7fb-114">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="ef7fb-114">Use</span></span> | <span data-ttu-id="ef7fb-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ef7fb-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ef7fb-116">**Enheds-id for certifikattype**</span><span class="sxs-lookup"><span data-stu-id="ef7fb-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="ef7fb-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="ef7fb-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="ef7fb-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ef7fb-118">*GUID*</span></span> | <span data-ttu-id="ef7fb-119">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="ef7fb-119">Read-only</span></span><br><span data-ttu-id="ef7fb-120">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ef7fb-120">Required</span></span> 
<span data-ttu-id="ef7fb-121">Systemgenereret</span><span class="sxs-lookup"><span data-stu-id="ef7fb-121">System-generated</span></span> | <span data-ttu-id="ef7fb-122">Entydig primær identifikation af certifikattype.</span><span class="sxs-lookup"><span data-stu-id="ef7fb-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="ef7fb-123">**Certifikattype**</span><span class="sxs-lookup"><span data-stu-id="ef7fb-123">**Certificate Type**</span></span><br><span data-ttu-id="ef7fb-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="ef7fb-124">mshr_certificatetype</span></span><br><span data-ttu-id="ef7fb-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ef7fb-125">*String*</span></span> | <span data-ttu-id="ef7fb-126">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="ef7fb-126">Read/write</span></span><br><span data-ttu-id="ef7fb-127">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ef7fb-127">Required</span></span> | <span data-ttu-id="ef7fb-128">Entydig brugerlæsbar identifikation af certifikattype.</span><span class="sxs-lookup"><span data-stu-id="ef7fb-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="ef7fb-129">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="ef7fb-129">**Description**</span></span><br><span data-ttu-id="ef7fb-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="ef7fb-130">mshr_description</span></span><br><span data-ttu-id="ef7fb-131">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ef7fb-131">*String*</span></span> | <span data-ttu-id="ef7fb-132">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="ef7fb-132">Read/write</span></span><br><span data-ttu-id="ef7fb-133">Påkrævet</span><span class="sxs-lookup"><span data-stu-id="ef7fb-133">Required</span></span> | <span data-ttu-id="ef7fb-134">Beskrivelse af certifikattype.</span><span class="sxs-lookup"><span data-stu-id="ef7fb-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="ef7fb-135">**Fornyelse påkrævet**</span><span class="sxs-lookup"><span data-stu-id="ef7fb-135">**Require Renewal**</span></span><br><span data-ttu-id="ef7fb-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="ef7fb-136">mshr_requirerenewal</span></span><br><span data-ttu-id="ef7fb-137">*mshr_noyes indstilling*</span><span class="sxs-lookup"><span data-stu-id="ef7fb-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="ef7fb-138">Læse/skrive</span><span class="sxs-lookup"><span data-stu-id="ef7fb-138">Read/write</span></span><br><span data-ttu-id="ef7fb-139">Valgfri</span><span class="sxs-lookup"><span data-stu-id="ef7fb-139">Optional</span></span> | <span data-ttu-id="ef7fb-140">Angiver, om certifikatet skal fornys.</span><span class="sxs-lookup"><span data-stu-id="ef7fb-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ef7fb-141">Se også</span><span class="sxs-lookup"><span data-stu-id="ef7fb-141">See also</span></span>

[<span data-ttu-id="ef7fb-142">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="ef7fb-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ef7fb-143">Eksempelforespørgsel til ansøger til ansættelse</span><span class="sxs-lookup"><span data-stu-id="ef7fb-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]