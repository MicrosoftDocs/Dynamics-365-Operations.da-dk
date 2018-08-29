---
title: Definere og administrere et frynsegodeprogram
description: "Personale indeholder en række værktøjer, der kan bruges til at konfigurere og vedligeholde frynsegoder, fradrag og arbejderes kompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte. Denne artikel indeholder oplysninger om, hvordan du konfigurerer og administrerer frynsegoder."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fc325b519299098a4f8257c013bce0842237f9ea
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---

# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="86a33-104">Definere og administrere et frynsegodeprogram</span><span class="sxs-lookup"><span data-stu-id="86a33-104">Define and manage a benefits program</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="86a33-105">Personale indeholder en række værktøjer, der kan bruges til at konfigurere og vedligeholde frynsegoder, fradrag og arbejderes kompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte.</span><span class="sxs-lookup"><span data-stu-id="86a33-105">Human resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="86a33-106">Dette emne indeholder oplysninger om, hvordan du konfigurerer og administrerer frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="86a33-106">This topic provides information about how to set up and manage benefits.</span></span>

<a name="benefit-setup"></a><span data-ttu-id="86a33-107">Frynsegodeopsætning</span><span class="sxs-lookup"><span data-stu-id="86a33-107">Benefit setup</span></span>
-------------

<span data-ttu-id="86a33-108">Før arbejdere kan tilmeldes frynsegoder, skal du oprette elementer for hvert frynsegode.</span><span class="sxs-lookup"><span data-stu-id="86a33-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="86a33-109">Disse elementer kombinerer lignende frynsegodeplaner og definerer standardindstillinger, som satser for fradrag og regnskabsmæssige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="86a33-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="86a33-110">Mange af disse indstillinger kan justeres, når arbejdere senere er tilmeldt frynsegodet.</span><span class="sxs-lookup"><span data-stu-id="86a33-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="86a33-111">En organisation kan tilbyde flere tilmeldingsmuligheder til hver frynsegodeplan, eller en arbejder kan melde sig ud af planen.</span><span class="sxs-lookup"><span data-stu-id="86a33-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="86a33-112">[![Procesforløb for frynsegoder](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="86a33-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="86a33-113">Frynsegodeelementer</span><span class="sxs-lookup"><span data-stu-id="86a33-113">Benefit elements</span></span>
<span data-ttu-id="86a33-114">Før du begynder at oprette for at oprette fordele og tilmelde arbejdere til dem, skal du definere de elementer, der udgør et frynsegode: type, plan og muligheder.</span><span class="sxs-lookup"><span data-stu-id="86a33-114">Before you begin to create to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="86a33-115">**Type** – en samling planer til et bestemt frynsegode, f.eks. sundhedsforsikring eller parkeringsplads.</span><span class="sxs-lookup"><span data-stu-id="86a33-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="86a33-116">**Plan** – et bestemt frynsegode, der er udført af en udbyder.</span><span class="sxs-lookup"><span data-stu-id="86a33-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="86a33-117">**Indstilling** – Disponeringsniveauet, f.eks. kun medarbejderen eller medarbejderen og ægtefællen/partneren.</span><span class="sxs-lookup"><span data-stu-id="86a33-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="86a33-118">For hver type ydelse, f.eks. briller eller tandlæge, kan en organisation tilbyde en eller flere planer til sine ansatte.</span><span class="sxs-lookup"><span data-stu-id="86a33-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="86a33-119">Organisationen kan tilbyde forskellige muligheder for hver enkelt plan.</span><span class="sxs-lookup"><span data-stu-id="86a33-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="86a33-120">Arbejdere kan for eksempel købe ekstra livsforsikringsdækning på én, to eller tre gange deres årlige løn.</span><span class="sxs-lookup"><span data-stu-id="86a33-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="86a33-121">Hver kombination af en plan og muligheder bliver et frynsegode, som medarbejdere kan tilmeldes.</span><span class="sxs-lookup"><span data-stu-id="86a33-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="86a33-122">[![billede af frynsegode](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="86a33-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="86a33-123">Berettigelse</span><span class="sxs-lookup"><span data-stu-id="86a33-123">Eligibility</span></span>
<span data-ttu-id="86a33-124">Medarbejderens berettigelse til forskellige former for frynsegoder, som en arbejdsgiver tilbyder, afhænger af mange faktorer.</span><span class="sxs-lookup"><span data-stu-id="86a33-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="86a33-125">Når du opretter et frynsegode i Microsoft Talent, kan du angive typen af berettigelse, der gælder for dette frynsegode.</span><span class="sxs-lookup"><span data-stu-id="86a33-125">When you create a benefit in Microsoft Talent, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="86a33-126">Du kan gøre et frynsegode tilgængelig for alle arbejdere.</span><span class="sxs-lookup"><span data-stu-id="86a33-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="86a33-127">For eksempel tilbyder nogle firmaer parkeringskort til alle medarbejdere som et frynsegode.</span><span class="sxs-lookup"><span data-stu-id="86a33-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="86a33-128">Når du opretter dette frynsegode, angiver du berettigelsen til **Alle arbejdere er berettigede**.</span><span class="sxs-lookup"><span data-stu-id="86a33-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="86a33-129">For andre frynsegoder, f.eks. udlæg og afgifter, kan berettigelse ikke anvendes.</span><span class="sxs-lookup"><span data-stu-id="86a33-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="86a33-130">Når du opretter disse typer af frynsegoder, kan du indstille berettigelse til **Tilsidesæt berettigelsesprocessen**.</span><span class="sxs-lookup"><span data-stu-id="86a33-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="86a33-131">Endelig kan frynsegodeberettigelse være baseret på regler.</span><span class="sxs-lookup"><span data-stu-id="86a33-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="86a33-132">Eksempelvis tilbyder en virksomhed frynsegoder i form af to typer af livsforsikring for medarbejderne.</span><span class="sxs-lookup"><span data-stu-id="86a33-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="86a33-133">Ledende medarbejdere er berettiget til en livsforsikringsplan, mens andre fuldtidsansatte er berettiget til den anden livsforsikringsplan.</span><span class="sxs-lookup"><span data-stu-id="86a33-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="86a33-134">I Talent kan du oprette en frynsegodeberettigelsesregel for at finde alle ledende medarbejdere og en anden regel for at finde andre fuldtidsansatte og derefter anvende disse regler på den relevante frynsegode.</span><span class="sxs-lookup"><span data-stu-id="86a33-134">In Talent, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="86a33-135">Tilmelding</span><span class="sxs-lookup"><span data-stu-id="86a33-135">Enrollment</span></span>
<span data-ttu-id="86a33-136">Når du har oprettet de fordele, din virksomhed tilbyder, og fastsat berettigelse, kan du tilmelde din arbejdere frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="86a33-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="86a33-137">Du kan tilmelde en enkelt arbejder frynsegoder, eller du kan tilmelde mange arbejdere en eller flere frynsegoder i én enkelt proces.</span><span class="sxs-lookup"><span data-stu-id="86a33-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="86a33-138">Nogle gange holder en organisation op med at tilbyde bestemte fordele.</span><span class="sxs-lookup"><span data-stu-id="86a33-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="86a33-139">I så fald skal du opdatere frynsegodet og de arbejdere, der er tilmeldt.</span><span class="sxs-lookup"><span data-stu-id="86a33-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="86a33-140">Med massefrynsegodeudløb kan du ændre udløbsdatoen for et frynsegode og arbejdertilmeldingerne for dette frynsegode samtidig.</span><span class="sxs-lookup"><span data-stu-id="86a33-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="86a33-141">Du kan også vælge flere medarbejdere, der er tilmeldt et frynsegode, og ændre slutdatoen for deres disponering.</span><span class="sxs-lookup"><span data-stu-id="86a33-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="86a33-142">På samme måde gør massefrynsegodeforlængelse det muligt at forlænge udløbsdatoen for både et frynsegode og arbejdertilmeldinger til det pågældende frynsegode, hvis du beslutter at tilbyde et frynsegode i længere tid end oprindeligt planlagt.</span><span class="sxs-lookup"><span data-stu-id="86a33-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>

<a name="additional-resources"></a><span data-ttu-id="86a33-143">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="86a33-143">Additional resources</span></span>
--------

[<span data-ttu-id="86a33-144">Politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="86a33-144">Benefit eligibility policies</span></span>](benefit-eligibility-policies.md)




