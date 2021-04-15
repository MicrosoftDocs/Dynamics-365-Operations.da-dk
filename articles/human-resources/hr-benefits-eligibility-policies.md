---
title: Politikker for frynsegodeberettigelse
description: Denne artikel indeholder oplysninger om politikker for frynsegodeberettigelse, som gør det lettere at definere, hvem der er berettiget til særlige frynsegoder.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a5046f1d32fb965c7cb3793daf1ba40b9c2a1d10
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805892"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="53fad-103">Politikker for berettigelse til frynsegoder</span><span class="sxs-lookup"><span data-stu-id="53fad-103">Benefit eligibility policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="53fad-104">Denne artikel indeholder oplysninger om politikker for frynsegodeberettigelse, som gør det lettere at definere, hvem der er berettiget til særlige frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="53fad-104">This article provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="53fad-105">Når du opretter fordele, kan du beslutte, hvilke fordele der er tilgængelige for hvilke medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="53fad-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="53fad-106">I følgende tabel vises eksempler på fordele, som du kan gøre tilgængelige for bestemte medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="53fad-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="53fad-107">Frynsegode</span><span class="sxs-lookup"><span data-stu-id="53fad-107">Benefit</span></span>          | <span data-ttu-id="53fad-108">Hvem frynsegodet er tilgængeligt for</span><span class="sxs-lookup"><span data-stu-id="53fad-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="53fad-109">Sygesikring</span><span class="sxs-lookup"><span data-stu-id="53fad-109">Health insurance</span></span> | <span data-ttu-id="53fad-110">Alle medarbejdere</span><span class="sxs-lookup"><span data-stu-id="53fad-110">All employees</span></span>                   |
| <span data-ttu-id="53fad-111">Mobiltelefon</span><span class="sxs-lookup"><span data-stu-id="53fad-111">Mobile phone</span></span>     | <span data-ttu-id="53fad-112">Salgsmedarbejdere, ledere</span><span class="sxs-lookup"><span data-stu-id="53fad-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="53fad-113">Parkeringskort</span><span class="sxs-lookup"><span data-stu-id="53fad-113">Parking passes</span></span>   | <span data-ttu-id="53fad-114">Ledere</span><span class="sxs-lookup"><span data-stu-id="53fad-114">Executives</span></span>                      |

<span data-ttu-id="53fad-115">Følgende komponenter bruges til at oprette politikker for frynsegodeberettigelse:</span><span class="sxs-lookup"><span data-stu-id="53fad-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="53fad-116">Typer politikregler</span><span class="sxs-lookup"><span data-stu-id="53fad-116">Policy rule types</span></span>
-   <span data-ttu-id="53fad-117">Politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="53fad-117">Benefit eligibility policies</span></span>

<span data-ttu-id="53fad-118">Politikregeltyper definerer de forespørgselsparametre, der bruges til udvikling af specifikke politikregler.</span><span class="sxs-lookup"><span data-stu-id="53fad-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="53fad-119">Når du opretter politikregeltyper, kan du oprette politikker for frynsegodeberettigelse.</span><span class="sxs-lookup"><span data-stu-id="53fad-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="53fad-120">Ved hjælp af politikkerne kan du oprette en samling regler, der gælder for en eller flere juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="53fad-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="53fad-121">Inden for hver politik kan du se nogle af de politikregeltyper for frynsegodeberettigelse, som du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="53fad-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="53fad-122">Du kan definere omfanget af reglen i politikken.</span><span class="sxs-lookup"><span data-stu-id="53fad-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="53fad-123">For eksempel, hvis du opretter en politikregeltype for frynsegodeberettigelse, som hedder **Leder**, kan du angive, hvad reglen er inden for denne politik.</span><span class="sxs-lookup"><span data-stu-id="53fad-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="53fad-124">I dette eksempel kan reglen angive, at enhver stilling, der indeholder ordet "leder", skal være omfattet af reglen.</span><span class="sxs-lookup"><span data-stu-id="53fad-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="53fad-125">Når du har defineret parametrene for reglen eller regler, der er inkluderet i politikken, kan du tildele en bestemt regel for frynsegodet.</span><span class="sxs-lookup"><span data-stu-id="53fad-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>






[!INCLUDE[footer-include](../includes/footer-banner.md)]