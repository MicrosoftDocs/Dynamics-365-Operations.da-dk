---
title: Politikker for frynsegodeberettigelse
description: Denne artikel indeholder oplysninger om politikker for frynsegodeberettigelse, som gør det lettere at definere, hvem der er berettiget til særlige frynsegoder.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 7b35d3f9a8afd3be44b648f6e138afd5f143ba55
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008561"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="c47d5-103">Politikker for berettigelse til frynsegoder</span><span class="sxs-lookup"><span data-stu-id="c47d5-103">Benefit eligibility policies</span></span>

<span data-ttu-id="c47d5-104">Denne artikel indeholder oplysninger om politikker for frynsegodeberettigelse, som gør det lettere at definere, hvem der er berettiget til særlige frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="c47d5-104">This article provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="c47d5-105">Når du opretter fordele, kan du beslutte, hvilke fordele der er tilgængelige for hvilke medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="c47d5-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="c47d5-106">I følgende tabel vises eksempler på fordele, som du kan gøre tilgængelige for bestemte medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="c47d5-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="c47d5-107">Frynsegode</span><span class="sxs-lookup"><span data-stu-id="c47d5-107">Benefit</span></span>          | <span data-ttu-id="c47d5-108">Hvem frynsegodet er tilgængeligt for</span><span class="sxs-lookup"><span data-stu-id="c47d5-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="c47d5-109">Sygesikring</span><span class="sxs-lookup"><span data-stu-id="c47d5-109">Health insurance</span></span> | <span data-ttu-id="c47d5-110">Alle medarbejdere</span><span class="sxs-lookup"><span data-stu-id="c47d5-110">All employees</span></span>                   |
| <span data-ttu-id="c47d5-111">Mobiltelefon</span><span class="sxs-lookup"><span data-stu-id="c47d5-111">Mobile phone</span></span>     | <span data-ttu-id="c47d5-112">Salgsmedarbejdere, ledere</span><span class="sxs-lookup"><span data-stu-id="c47d5-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="c47d5-113">Parkeringskort</span><span class="sxs-lookup"><span data-stu-id="c47d5-113">Parking passes</span></span>   | <span data-ttu-id="c47d5-114">Ledere</span><span class="sxs-lookup"><span data-stu-id="c47d5-114">Executives</span></span>                      |

<span data-ttu-id="c47d5-115">Følgende komponenter bruges til at oprette politikker for frynsegodeberettigelse:</span><span class="sxs-lookup"><span data-stu-id="c47d5-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="c47d5-116">Typer politikregler</span><span class="sxs-lookup"><span data-stu-id="c47d5-116">Policy rule types</span></span>
-   <span data-ttu-id="c47d5-117">Politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="c47d5-117">Benefit eligibility policies</span></span>

<span data-ttu-id="c47d5-118">Politikregeltyper definerer de forespørgselsparametre, der bruges til udvikling af specifikke politikregler.</span><span class="sxs-lookup"><span data-stu-id="c47d5-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="c47d5-119">Når du opretter politikregeltyper, kan du oprette politikker for frynsegodeberettigelse.</span><span class="sxs-lookup"><span data-stu-id="c47d5-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="c47d5-120">Ved hjælp af politikkerne kan du oprette en samling regler, der gælder for en eller flere juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="c47d5-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="c47d5-121">Inden for hver politik kan du se nogle af de politikregeltyper for frynsegodeberettigelse, som du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="c47d5-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="c47d5-122">Du kan definere omfanget af reglen i politikken.</span><span class="sxs-lookup"><span data-stu-id="c47d5-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="c47d5-123">For eksempel, hvis du opretter en politikregeltype for frynsegodeberettigelse, som hedder **Leder**, kan du angive, hvad reglen er inden for denne politik.</span><span class="sxs-lookup"><span data-stu-id="c47d5-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="c47d5-124">I dette eksempel kan reglen angive, at enhver stilling, der indeholder ordet "leder", skal være omfattet af reglen.</span><span class="sxs-lookup"><span data-stu-id="c47d5-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="c47d5-125">Når du har defineret parametrene for reglen eller regler, der er inkluderet i politikken, kan du tildele en bestemt regel for frynsegodet.</span><span class="sxs-lookup"><span data-stu-id="c47d5-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>



