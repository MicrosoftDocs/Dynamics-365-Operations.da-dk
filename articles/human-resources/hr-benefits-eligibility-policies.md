---
title: Politikker for frynsegodeberettigelse
description: Denne artikel indeholder oplysninger om politikker for frynsegodeberettigelse, som gør det lettere at definere, hvem der er berettiget til særlige frynsegoder.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: cc5dfedc0022cbf9bdbc636bbe96971422c29838
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111895"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="09cee-103">Politikker for berettigelse til frynsegoder</span><span class="sxs-lookup"><span data-stu-id="09cee-103">Benefit eligibility policies</span></span>

<span data-ttu-id="09cee-104">Denne artikel indeholder oplysninger om politikker for frynsegodeberettigelse, som gør det lettere at definere, hvem der er berettiget til særlige frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="09cee-104">This article provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="09cee-105">Når du opretter fordele, kan du beslutte, hvilke fordele der er tilgængelige for hvilke medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="09cee-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="09cee-106">I følgende tabel vises eksempler på fordele, som du kan gøre tilgængelige for bestemte medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="09cee-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="09cee-107">Frynsegode</span><span class="sxs-lookup"><span data-stu-id="09cee-107">Benefit</span></span>          | <span data-ttu-id="09cee-108">Hvem frynsegodet er tilgængeligt for</span><span class="sxs-lookup"><span data-stu-id="09cee-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="09cee-109">Sygesikring</span><span class="sxs-lookup"><span data-stu-id="09cee-109">Health insurance</span></span> | <span data-ttu-id="09cee-110">Alle medarbejdere</span><span class="sxs-lookup"><span data-stu-id="09cee-110">All employees</span></span>                   |
| <span data-ttu-id="09cee-111">Mobiltelefon</span><span class="sxs-lookup"><span data-stu-id="09cee-111">Mobile phone</span></span>     | <span data-ttu-id="09cee-112">Salgsmedarbejdere, ledere</span><span class="sxs-lookup"><span data-stu-id="09cee-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="09cee-113">Parkeringskort</span><span class="sxs-lookup"><span data-stu-id="09cee-113">Parking passes</span></span>   | <span data-ttu-id="09cee-114">Ledere</span><span class="sxs-lookup"><span data-stu-id="09cee-114">Executives</span></span>                      |

<span data-ttu-id="09cee-115">Følgende komponenter bruges til at oprette politikker for frynsegodeberettigelse:</span><span class="sxs-lookup"><span data-stu-id="09cee-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="09cee-116">Typer politikregler</span><span class="sxs-lookup"><span data-stu-id="09cee-116">Policy rule types</span></span>
-   <span data-ttu-id="09cee-117">Politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="09cee-117">Benefit eligibility policies</span></span>

<span data-ttu-id="09cee-118">Politikregeltyper definerer de forespørgselsparametre, der bruges til udvikling af specifikke politikregler.</span><span class="sxs-lookup"><span data-stu-id="09cee-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="09cee-119">Når du opretter politikregeltyper, kan du oprette politikker for frynsegodeberettigelse.</span><span class="sxs-lookup"><span data-stu-id="09cee-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="09cee-120">Ved hjælp af politikkerne kan du oprette en samling regler, der gælder for en eller flere juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="09cee-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="09cee-121">Inden for hver politik kan du se nogle af de politikregeltyper for frynsegodeberettigelse, som du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="09cee-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="09cee-122">Du kan definere omfanget af reglen i politikken.</span><span class="sxs-lookup"><span data-stu-id="09cee-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="09cee-123">For eksempel, hvis du opretter en politikregeltype for frynsegodeberettigelse, som hedder **Leder**, kan du angive, hvad reglen er inden for denne politik.</span><span class="sxs-lookup"><span data-stu-id="09cee-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="09cee-124">I dette eksempel kan reglen angive, at enhver stilling, der indeholder ordet "leder", skal være omfattet af reglen.</span><span class="sxs-lookup"><span data-stu-id="09cee-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="09cee-125">Når du har defineret parametrene for reglen eller regler, der er inkluderet i politikken, kan du tildele en bestemt regel for frynsegodet.</span><span class="sxs-lookup"><span data-stu-id="09cee-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>




