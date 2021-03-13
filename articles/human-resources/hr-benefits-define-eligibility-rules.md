---
title: Definere regler og politikker for frynsegodeberettigelse
description: Denne artikel viser dig, hvordan du kan oprette regler og politikker for frynsegodeberettigelse og derefter tildele regler til frynsegoderne.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: cc80549eaffa72a22dec51829c86d04a763de96a
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111897"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="95d16-103">Definere regler og politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="95d16-103">Define benefit eligibility rules and policies</span></span>

<span data-ttu-id="95d16-104">Dette emne viser dig, hvordan du kan oprette regler og politikker for frynsegodeberettigelse og derefter tildele regler til frynsegoderne.</span><span class="sxs-lookup"><span data-stu-id="95d16-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="95d16-105">Opret politikregeltyper for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="95d16-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="95d16-106">Gå til **Human Resources > Frynsegoder > Berettigelse > Politikregeltyper for frynsegodeberettigelse**.</span><span class="sxs-lookup"><span data-stu-id="95d16-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="95d16-107">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="95d16-107">Select **New**.</span></span>
3. <span data-ttu-id="95d16-108">Angiv en værdi i feltet **Regelnavn**.</span><span class="sxs-lookup"><span data-stu-id="95d16-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="95d16-109">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="95d16-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="95d16-110">Klik på rullelisten i feltet **Forespørgselsnavn** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="95d16-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="95d16-111">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="95d16-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="95d16-112">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="95d16-112">Select **Save**.</span></span>
8. <span data-ttu-id="95d16-113">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="95d16-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="95d16-114">Politik for personalegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="95d16-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="95d16-115">Gå til **Human Resources > Frynsegoder > Berettigelse > Politikker for frynsegodeberettigelse**.</span><span class="sxs-lookup"><span data-stu-id="95d16-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="95d16-116">Vælg en eksisterende frynsegodepolitik.</span><span class="sxs-lookup"><span data-stu-id="95d16-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="95d16-117">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="95d16-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="95d16-118">Slå udvidelsen af sektionerne **Politikorganisationer** til/fra.</span><span class="sxs-lookup"><span data-stu-id="95d16-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="95d16-119">Du kan tilføje eller fjerne de organisationer, du vil medtage i politikken.</span><span class="sxs-lookup"><span data-stu-id="95d16-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="95d16-120">Udvid eller skjul sektionen **Politikregler**.</span><span class="sxs-lookup"><span data-stu-id="95d16-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="95d16-121">Find den politikregel, som blev oprettet tidligere, på listen.</span><span class="sxs-lookup"><span data-stu-id="95d16-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="95d16-122">Vælg **Opret politikregel**.</span><span class="sxs-lookup"><span data-stu-id="95d16-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="95d16-123">Angiv den dato, hvor politikken skal træde i kraft, i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="95d16-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="95d16-124">Angivelse af gældende slutdatoer gør det muligt at foretage fremtidige ændringer i politikregler, så det ikke er nødvendigt at vende tilbage til politikken, når disse ændringer skal træde i kraft.</span><span class="sxs-lookup"><span data-stu-id="95d16-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="95d16-125">Tilføj om nødvendigt en where-sætning i feltet **Tilføj betingelse**.</span><span class="sxs-lookup"><span data-stu-id="95d16-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="95d16-126">Hvis du f.eks. ønsker, at reglen kun gælder for salgschefer, kan du oprette en Where-sætning for at sige: hvor stillingsbeskrivelsen er lig med salgschef.</span><span class="sxs-lookup"><span data-stu-id="95d16-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="95d16-127">Du kan tilføje flere Where-sætninger sammen i reglen.</span><span class="sxs-lookup"><span data-stu-id="95d16-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="95d16-128">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="95d16-128">Select **OK**.</span></span>
11. <span data-ttu-id="95d16-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="95d16-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="95d16-130">Tildel reglen til frynsegodet</span><span class="sxs-lookup"><span data-stu-id="95d16-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="95d16-131">Gå til **Human resources > Frynsegoder > Frynsegoder**.</span><span class="sxs-lookup"><span data-stu-id="95d16-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="95d16-132">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="95d16-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="95d16-133">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="95d16-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="95d16-134">Udvid eller skjul sektionen **Berettigelsesregler**.</span><span class="sxs-lookup"><span data-stu-id="95d16-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="95d16-135">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="95d16-135">Select **Edit**.</span></span>
6. <span data-ttu-id="95d16-136">Vælg Regel i feltet **Berettigelse**.</span><span class="sxs-lookup"><span data-stu-id="95d16-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="95d16-137">Vælg den regel, som du oprettede tidligere, i feltet **Regeltype**.</span><span class="sxs-lookup"><span data-stu-id="95d16-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="95d16-138">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="95d16-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="95d16-139">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="95d16-139">Select **Save**.</span></span>
11. <span data-ttu-id="95d16-140">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="95d16-140">Close the form.</span></span>

