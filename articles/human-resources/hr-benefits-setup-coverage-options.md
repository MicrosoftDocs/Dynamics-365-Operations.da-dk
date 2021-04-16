---
title: Oprette disponeringsindstillinger
description: Dækningsindstillinger i Microsoft Dynamics 365 Human Resources er niveauer for en deltagers valg i en frynsegodeplan eller et program.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d304b0cf65c7833ebc7f21323efc59540289de8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803675"
---
# <a name="create-coverage-options"></a><span data-ttu-id="0a75a-103">Oprette disponeringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="0a75a-103">Create coverage options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0a75a-104">Dækningsindstillinger i Microsoft Dynamics 365 Human Resources er niveauer for en deltagers valg i en frynsegodeplan eller et program.</span><span class="sxs-lookup"><span data-stu-id="0a75a-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="0a75a-105">Dækningsindstillinger kan f.eks. omfatte **Kun medarbejder** for en medicinsk plan eller **2 x løn** til en livsforsikring.</span><span class="sxs-lookup"><span data-stu-id="0a75a-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="0a75a-106">Når den er defineret, kan du genbruge indstillingerne for frynsegodedækning.</span><span class="sxs-lookup"><span data-stu-id="0a75a-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="0a75a-107">Du kan knytte en indstilling til en eller flere planer.</span><span class="sxs-lookup"><span data-stu-id="0a75a-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="0a75a-108">Når du har defineret dækningsindstillingerne, skal du knytte dækningsindstillingerne til en type af frynsegodeplan.</span><span class="sxs-lookup"><span data-stu-id="0a75a-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="0a75a-109">Plantypen knyttes derefter til en frynsegodeplan eller et frynsegodeprogram.</span><span class="sxs-lookup"><span data-stu-id="0a75a-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="0a75a-110">Dækningsindstillinger, der er knyttet til plantype, vil være tilgængelige for alle de planer, der oprettes med den pågældende plantype.</span><span class="sxs-lookup"><span data-stu-id="0a75a-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="0a75a-111">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Disponeringsindstillinger** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="0a75a-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="0a75a-112">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0a75a-112">Select **New**.</span></span>

3. <span data-ttu-id="0a75a-113">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="0a75a-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="0a75a-114">Felt</span><span class="sxs-lookup"><span data-stu-id="0a75a-114">Field</span></span> | <span data-ttu-id="0a75a-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0a75a-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="0a75a-116">**Disponeringsindstilling**</span><span class="sxs-lookup"><span data-stu-id="0a75a-116">**Coverage option**</span></span> | <span data-ttu-id="0a75a-117">Et entydigt navn på en disponeringsindstilling.</span><span class="sxs-lookup"><span data-stu-id="0a75a-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="0a75a-118">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="0a75a-118">**Description**</span></span> | <span data-ttu-id="0a75a-119">En beskrivelse af disponeringsindstillingen.</span><span class="sxs-lookup"><span data-stu-id="0a75a-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="0a75a-120">**Dækningskode**</span><span class="sxs-lookup"><span data-stu-id="0a75a-120">**Coverage code**</span></span> | <span data-ttu-id="0a75a-121">Disponeringskoder tilknytter minimum- og maksimumbeløb for alle berettigede disponerede persontyper.</span><span class="sxs-lookup"><span data-stu-id="0a75a-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="0a75a-122">En disponeringskode angiver, hvem der er disponeret, eller disponeringsbeløbet, der er tilladt for en plantype.</span><span class="sxs-lookup"><span data-stu-id="0a75a-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="0a75a-123">Du kan udtrykke beløbet for disponering som et kronebeløb eller en procentdel.</span><span class="sxs-lookup"><span data-stu-id="0a75a-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="0a75a-124">F.eks.:</span><span class="sxs-lookup"><span data-stu-id="0a75a-124">For example:</span></span></br></br><span data-ttu-id="0a75a-125">- **EMP+1** – for at blive kvalificeret skal medarbejderen have valgt én afhængig (hvis der er valgt mere end én, er de ikke længere kvalificeret).</span><span class="sxs-lookup"><span data-stu-id="0a75a-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="0a75a-126">- **EMP+familie** – for at blive kvalificeret skal medarbejderen have valgt mindst to afhængige.</span><span class="sxs-lookup"><span data-stu-id="0a75a-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="0a75a-127">**Maks. antal**</span><span class="sxs-lookup"><span data-stu-id="0a75a-127">**Maximum number**</span></span> | <span data-ttu-id="0a75a-128">Maks. antal af afhængige.</span><span class="sxs-lookup"><span data-stu-id="0a75a-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="0a75a-129">**Status**</span><span class="sxs-lookup"><span data-stu-id="0a75a-129">**Status**</span></span> | <span data-ttu-id="0a75a-130">Statussen for disponeringsindstillingen.</span><span class="sxs-lookup"><span data-stu-id="0a75a-130">The status of the coverage option.</span></span> <span data-ttu-id="0a75a-131">Hvis status for disponeringsindstillingen er angivet til Inaktiv, kan indstillingen Disponering ikke vælges for plantyper.</span><span class="sxs-lookup"><span data-stu-id="0a75a-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="0a75a-132">**Procent**</span><span class="sxs-lookup"><span data-stu-id="0a75a-132">**Percent**</span></span> | <span data-ttu-id="0a75a-133">Beløb i procent.</span><span class="sxs-lookup"><span data-stu-id="0a75a-133">The percent amount.</span></span> <span data-ttu-id="0a75a-134">Dette felt er kun aktivt, hvis % x løn blev valgt i feltet Disponeringskode.</span><span class="sxs-lookup"><span data-stu-id="0a75a-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="0a75a-135">**Nævner**</span><span class="sxs-lookup"><span data-stu-id="0a75a-135">**Divisor**</span></span> | <span data-ttu-id="0a75a-136">Den divisor, der skal bruges i beregningen, når du vælger disponeringskode % x løn.</span><span class="sxs-lookup"><span data-stu-id="0a75a-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="0a75a-137">**Min. procentdel**</span><span class="sxs-lookup"><span data-stu-id="0a75a-137">**Percent minimum**</span></span> | <span data-ttu-id="0a75a-138">Den minimale procentdel, når du vælger Procentdisponeringskode.</span><span class="sxs-lookup"><span data-stu-id="0a75a-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="0a75a-139">**Maks. procent**</span><span class="sxs-lookup"><span data-stu-id="0a75a-139">**Percent maximum**</span></span> | <span data-ttu-id="0a75a-140">Den maksimale procentdel, når du vælger Procentdisponeringskode.</span><span class="sxs-lookup"><span data-stu-id="0a75a-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="0a75a-141">Under **Indstillinger for berettigelse for personlige kontakter** skal du knytte den relevante indstilling for personlig kontaktberettigelse til de enkelte disponeringsindstillinger.</span><span class="sxs-lookup"><span data-stu-id="0a75a-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="0a75a-142">Under **Selvbetjening** skal du angive værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="0a75a-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="0a75a-143">Felt</span><span class="sxs-lookup"><span data-stu-id="0a75a-143">Field</span></span> | <span data-ttu-id="0a75a-144">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0a75a-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="0a75a-145">**Tillad medarbejderbidragsbeløb**</span><span class="sxs-lookup"><span data-stu-id="0a75a-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="0a75a-146">Angiver, om medarbejdere skal kunne redigere bidragsbeløbet via selvbetjening for frynsegoder, når de vælger frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="0a75a-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="0a75a-147">Hvis du markerer dette afkrydsningsfelt, beregner systemet parametre for frynsegodeplanen baseret på det bidragsbeløb, som medarbejderen indtaster i selvbetjeningstjenesten for frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="0a75a-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="0a75a-148">**Tillad medarbejderdækningsbeløb**</span><span class="sxs-lookup"><span data-stu-id="0a75a-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="0a75a-149">Angiver, om medarbejdere skal kunne redigere disponeringsbeløbet via selvbetjening for frynsegoder, når de vælger frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="0a75a-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="0a75a-150">Hvis du markerer dette afkrydsningsfelt, beregner systemet parametre for frynsegodeplanen baseret på det disponeringsbeløb, som medarbejderen indtaster i selvbetjeningstjenesten for medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="0a75a-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="0a75a-151">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0a75a-151">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]