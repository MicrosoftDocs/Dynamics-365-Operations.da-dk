---
title: Konfigurere berettigelsesindstillinger for personlige kontakter
description: Konfigurer indstillinger for berettigelse for personlige kontakter i Microsoft Dynamics 365 Human Resources. Personlige kontakter kan være modtagere eller afhængige.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a50c5e54d224a2f8607284eb105381ffb6ef7ad9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008509"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="ee1c3-104">Konfigurere berettigelsesindstillinger for personlige kontakter</span><span class="sxs-lookup"><span data-stu-id="ee1c3-104">Configure personal contact eligibility options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="ee1c3-105">I denne artikel kan du se, hvordan du kan konfigurere typer af personlige kontakter, der skal bruges i frynsegoder i Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ee1c3-106">Personlige kontakter kan være modtagere eller afhængige.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="ee1c3-107">Vælg **Indstillinger for berettigelse for personlige kontakter** under **Konfiguration** i arbejdsområdet **Frynsegodeadministration**.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="ee1c3-108">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-108">Select **New**.</span></span>

3. <span data-ttu-id="ee1c3-109">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="ee1c3-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="ee1c3-110">Felt</span><span class="sxs-lookup"><span data-stu-id="ee1c3-110">Field</span></span> | <span data-ttu-id="ee1c3-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ee1c3-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ee1c3-112">**Berettigelsesindstilling**</span><span class="sxs-lookup"><span data-stu-id="ee1c3-112">**Eligibility option**</span></span> | <span data-ttu-id="ee1c3-113">Et entydigt navn eller en entydig kode, der identificerer indstillingen for berettigelse.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="ee1c3-114">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="ee1c3-114">**Description**</span></span> | <span data-ttu-id="ee1c3-115">En kort beskrivelse af indstillingen for berettigelse.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="ee1c3-116">**Kode for kontaktberettigelse**</span><span class="sxs-lookup"><span data-stu-id="ee1c3-116">**Contact eligibility code**</span></span> | <span data-ttu-id="ee1c3-117">Den systemkode, der bedst beskriver indstillingen for personlig berettigelse.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="ee1c3-118">Du kan vælge mellem følgende:</span><span class="sxs-lookup"><span data-stu-id="ee1c3-118">You can choose from:</span></span> <ul><li><span data-ttu-id="ee1c3-119">Relation</span><span class="sxs-lookup"><span data-stu-id="ee1c3-119">Relationship</span></span></li><li><span data-ttu-id="ee1c3-120">Studerende</span><span class="sxs-lookup"><span data-stu-id="ee1c3-120">Student</span></span></li><li><span data-ttu-id="ee1c3-121">Afhængigt af overskydende beløb</span><span class="sxs-lookup"><span data-stu-id="ee1c3-121">Overage dependent</span></span></li><li><span data-ttu-id="ee1c3-122">For gammel deaktiveret afhængig</span><span class="sxs-lookup"><span data-stu-id="ee1c3-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="ee1c3-123">**Status**</span><span class="sxs-lookup"><span data-stu-id="ee1c3-123">**Status**</span></span> | <span data-ttu-id="ee1c3-124">Statussen for berettigelsesindstillingen.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-124">The status of the eligibility option.</span></span> <span data-ttu-id="ee1c3-125">Hvis status for en berettigelsesindstilling er angivet til inaktiv, kan du ikke vælge denne indstilling for berettigelse for personlig kontakt for personlige kontaktpersoner.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="ee1c3-126">**Relation**</span><span class="sxs-lookup"><span data-stu-id="ee1c3-126">**Relationship**</span></span> | <span data-ttu-id="ee1c3-127">Angiver forholdet mellem den personlige kontaktperson og medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="ee1c3-128">Dette felt er kun aktivt, hvis koden for kontaktberettigelse er angivet til Relation.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="ee1c3-129">**Alder**</span><span class="sxs-lookup"><span data-stu-id="ee1c3-129">**Age**</span></span> | <span data-ttu-id="ee1c3-130">Den maksimale alder for en berettiget personlige kontaktperson for frynsegodeplanen.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="ee1c3-131">Dette felt er kun aktivt, hvis du vælger en relation.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="ee1c3-132">Denne alder sammenlignes med den beregnede alder for den personlige kontakt.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="ee1c3-133">Beregnet alder er: (dækningsdato – personlig kontakts fødselsdato/365).</span><span class="sxs-lookup"><span data-stu-id="ee1c3-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="ee1c3-134">Dette tal er altid et heltal.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="ee1c3-135">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-135">Select **Save**.</span></span> 
