---
title: Definere regler og politikker for frynsegodeberettigelse
description: Denne artikel viser dig, hvordan du kan oprette regler og politikker for frynsegodeberettigelse og derefter tildele regler til frynsegoderne.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: f46437fef342ab1a4e368063d8b74205ca8e8c05
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430871"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="72902-103">Definere regler og politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="72902-103">Define benefit eligibility rules and policies</span></span>

<span data-ttu-id="72902-104">Denne artikel viser dig, hvordan du kan oprette regler og politikker for frynsegodeberettigelse og derefter tildele regler til frynsegoderne.</span><span class="sxs-lookup"><span data-stu-id="72902-104">This article shows you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="72902-105">Det demodatafirma, der bruges til at oprette denne post, er USMF.</span><span class="sxs-lookup"><span data-stu-id="72902-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="72902-106">Opret politikregeltyper for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="72902-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="72902-107">Gå til Personale > Frynsegoder > Berettigelse > Politikregeltyper for frynsegodeberettigelse.</span><span class="sxs-lookup"><span data-stu-id="72902-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="72902-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="72902-108">Click New.</span></span>
3. <span data-ttu-id="72902-109">Skriv en værdi i feltet Regelnavn.</span><span class="sxs-lookup"><span data-stu-id="72902-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="72902-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="72902-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="72902-111">Klik på rullelisten i feltet Forespørgselsnavn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="72902-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="72902-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="72902-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="72902-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="72902-113">Click Save.</span></span>
8. <span data-ttu-id="72902-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="72902-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="72902-115">Politik for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="72902-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="72902-116">Gå til Personale > Frynsegoder > Berettigelse > Politikker for frynsegodeberettigelse.</span><span class="sxs-lookup"><span data-stu-id="72902-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="72902-117">Vælg en eksisterende frynsegodepolitik.</span><span class="sxs-lookup"><span data-stu-id="72902-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="72902-118">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="72902-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="72902-119">Slå udvidelsen af sektionerne Politikorganisationer til/fra.</span><span class="sxs-lookup"><span data-stu-id="72902-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="72902-120">Her kan du tilføje eller fjerne de organisationer, du vil medtage i politikken.</span><span class="sxs-lookup"><span data-stu-id="72902-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="72902-121">Udvid eller skjul sektionen Politikregler.</span><span class="sxs-lookup"><span data-stu-id="72902-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="72902-122">Find den politikregel, som blev oprettet tidligere, på listen.</span><span class="sxs-lookup"><span data-stu-id="72902-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="72902-123">Klik på Opret politikregel.</span><span class="sxs-lookup"><span data-stu-id="72902-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="72902-124">Angiv den dato, hvor politikken skal træde i kraft, i feltet ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="72902-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="72902-125">Angivelse af ikrafttrædelses- og slutdatoer gør det muligt at foretage fremtidige ændringer i politikregler og fjerner behovet for at vende tilbage til politikken, når disse ændringer skal træde i kraft.</span><span class="sxs-lookup"><span data-stu-id="72902-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="72902-126">Hvis du f.eks. ønsker, at reglen kun gælder for salgschefer, kan du oprette en Where-sætning for at sige: hvor stillingsbeskrivelsen er lig med salgschef.</span><span class="sxs-lookup"><span data-stu-id="72902-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="72902-127">Du kan bruge And eller Or i flere Where-sætninger sammen i reglen.</span><span class="sxs-lookup"><span data-stu-id="72902-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="72902-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="72902-128">Click OK.</span></span>
11. <span data-ttu-id="72902-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="72902-129">Close the page.</span></span>
12. <span data-ttu-id="72902-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="72902-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="72902-131">Tildel reglen til frynsegodet</span><span class="sxs-lookup"><span data-stu-id="72902-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="72902-132">Gå til Personale > Frynsegoder > Frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="72902-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="72902-133">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="72902-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="72902-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="72902-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="72902-135">Udvid eller skjul sektionen Berettigelsesregler.</span><span class="sxs-lookup"><span data-stu-id="72902-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="72902-136">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="72902-136">Click Edit.</span></span>
6. <span data-ttu-id="72902-137">Vælg Regelbaseret på listen i feltet Berettigelse.</span><span class="sxs-lookup"><span data-stu-id="72902-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="72902-138">Klik på rullelisten i feltet Regeltype for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="72902-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="72902-139">Find og vælg den regel, som blev oprettet tidligere, på listen.</span><span class="sxs-lookup"><span data-stu-id="72902-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="72902-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="72902-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="72902-141">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="72902-141">Click Save.</span></span>
11. <span data-ttu-id="72902-142">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="72902-142">Close the form.</span></span>

