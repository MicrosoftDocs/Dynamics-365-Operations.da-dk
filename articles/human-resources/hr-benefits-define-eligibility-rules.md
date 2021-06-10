---
title: Definere regler og politikker for frynsegodeberettigelse
description: Denne artikel viser dig, hvordan du kan oprette regler og politikker for frynsegodeberettigelse og derefter tildele regler til frynsegoderne.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 046b045fbdda125c5a2259783c0347f687453528
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053147"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="0d84d-103">Definere regler og politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="0d84d-103">Define benefit eligibility rules and policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0d84d-104">Dette emne viser dig, hvordan du kan oprette regler og politikker for frynsegodeberettigelse og derefter tildele regler til frynsegoderne.</span><span class="sxs-lookup"><span data-stu-id="0d84d-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="0d84d-105">Opret politikregeltyper for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="0d84d-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="0d84d-106">Gå til **Human Resources > Frynsegoder > Berettigelse > Politikregeltyper for frynsegodeberettigelse**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="0d84d-107">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-107">Select **New**.</span></span>
3. <span data-ttu-id="0d84d-108">Angiv en værdi i feltet **Regelnavn**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="0d84d-109">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="0d84d-110">Klik på rullelisten i feltet **Forespørgselsnavn** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0d84d-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0d84d-111">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0d84d-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="0d84d-112">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-112">Select **Save**.</span></span>
8. <span data-ttu-id="0d84d-113">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d84d-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="0d84d-114">Politik for personalegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="0d84d-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="0d84d-115">Gå til **Human Resources > Frynsegoder > Berettigelse > Politikker for frynsegodeberettigelse**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="0d84d-116">Vælg en eksisterende frynsegodepolitik.</span><span class="sxs-lookup"><span data-stu-id="0d84d-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="0d84d-117">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0d84d-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="0d84d-118">Slå udvidelsen af sektionerne **Politikorganisationer** til/fra.</span><span class="sxs-lookup"><span data-stu-id="0d84d-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="0d84d-119">Du kan tilføje eller fjerne de organisationer, du vil medtage i politikken.</span><span class="sxs-lookup"><span data-stu-id="0d84d-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="0d84d-120">Udvid eller skjul sektionen **Politikregler**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="0d84d-121">Find den politikregel, som blev oprettet tidligere, på listen.</span><span class="sxs-lookup"><span data-stu-id="0d84d-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="0d84d-122">Vælg **Opret politikregel**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="0d84d-123">Angiv den dato, hvor politikken skal træde i kraft, i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="0d84d-124">Angivelse af gældende slutdatoer gør det muligt at foretage fremtidige ændringer i politikregler, så det ikke er nødvendigt at vende tilbage til politikken, når disse ændringer skal træde i kraft.</span><span class="sxs-lookup"><span data-stu-id="0d84d-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="0d84d-125">Tilføj om nødvendigt en where-sætning i feltet **Tilføj betingelse**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="0d84d-126">Hvis du f.eks. ønsker, at reglen kun gælder for salgschefer, kan du oprette en Where-sætning for at sige: hvor stillingsbeskrivelsen er lig med salgschef.</span><span class="sxs-lookup"><span data-stu-id="0d84d-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="0d84d-127">Du kan tilføje flere Where-sætninger sammen i reglen.</span><span class="sxs-lookup"><span data-stu-id="0d84d-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="0d84d-128">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-128">Select **OK**.</span></span>
11. <span data-ttu-id="0d84d-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d84d-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="0d84d-130">Tildel reglen til frynsegodet</span><span class="sxs-lookup"><span data-stu-id="0d84d-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="0d84d-131">Gå til **Human resources > Frynsegoder > Frynsegoder**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="0d84d-132">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="0d84d-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0d84d-133">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0d84d-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="0d84d-134">Udvid eller skjul sektionen **Berettigelsesregler**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="0d84d-135">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-135">Select **Edit**.</span></span>
6. <span data-ttu-id="0d84d-136">Vælg Regel i feltet **Berettigelse**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="0d84d-137">Vælg den regel, som du oprettede tidligere, i feltet **Regeltype**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="0d84d-138">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0d84d-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="0d84d-139">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-139">Select **Save**.</span></span>
11. <span data-ttu-id="0d84d-140">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="0d84d-140">Close the form.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]