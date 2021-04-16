---
title: Oversigt over administration af frynsegoder
description: Oversigt over funktionen Administration af frynsegoder i Dynamics 365 Human Resources. Tilbyd dine medarbejdere mulighed for ekstra frynsegoder via en brugervenlig onlineoplevelse.
author: andreabichsel
ms.date: 09/17/2020
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
ms.openlocfilehash: 34b0916e0bf618590bcc56a9a3bc7c61576361cc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805772"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="2410d-104">Oversigt over administration af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="2410d-104">Benefits management overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2410d-105">Hvis du vil forblive konkurrencedygtig, skal du tilbyde en lang række frynsegoder for at tiltrække og holde på dine bedste medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="2410d-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="2410d-106">Ud over standardfrynsekoder som sundhedsforsikring og tandlægedækning kan det også være en god idé at tilbyde udvidede tjenester som hjælp til adoption, rekreative ordninger og beklædningsgodtgørelse.</span><span class="sxs-lookup"><span data-stu-id="2410d-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="2410d-107">Administration af frynsegoder i Microsoft Dynamics 365 Human Resources giver dig en fleksibel løsning, som understøtter en lang række frynsegodemuligheder.</span><span class="sxs-lookup"><span data-stu-id="2410d-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="2410d-108">Human Resources inkluderer også en brugervenlig medarbejderoplevelse, der viser det, du tilbyder.</span><span class="sxs-lookup"><span data-stu-id="2410d-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="2410d-109">Forbedrede frynsegodeplaner giver dig mulighed for at oprette og administrere unikke frynsegodeplaner og understøtte komplekse satstabeller for frynsegoder og indlejrede niveauer.</span><span class="sxs-lookup"><span data-stu-id="2410d-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="2410d-110">Du kan nemt oprette frynsegodeprogrammer, pakker og regler for automatisk registrering, der gør det nemmere for medarbejderne.</span><span class="sxs-lookup"><span data-stu-id="2410d-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="2410d-111">Med flekskreditprogrammer kan du gøre det muligt at understøtte pension og andre levetidshændelser.</span><span class="sxs-lookup"><span data-stu-id="2410d-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="2410d-112">Omfattende berettigelsesregler sikrer, at de rigtige fordele stilles til rådighed for de rette medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="2410d-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="2410d-113">Onlinetilmeldinger til frynsegoder giver medarbejderne en nem oplevelse.</span><span class="sxs-lookup"><span data-stu-id="2410d-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="2410d-114">Den kvalificerede levetidshændelsesproces understøtter fremtidige levetidshændelser.</span><span class="sxs-lookup"><span data-stu-id="2410d-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="2410d-115">Hvis du vil have adgang til demodataene, skal du geninstallere dit sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="2410d-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="2410d-116">Aktivere Administration af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="2410d-116">Enable Benefits management</span></span>

<span data-ttu-id="2410d-117">I dette emne beskrives, hvordan du slår funktioner til i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2410d-117">This topic describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="2410d-118">Den angiver også, hvilke eksisterende funktioner i Human Resources som Administration af frynsegoder erstatter, eller der deaktiveres, når du aktiverer Administration af frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="2410d-118">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2410d-119">Når du aktiverer Administration af frynsegoder i et **produktionsmiljø**, kan du ikke deaktivere det.</span><span class="sxs-lookup"><span data-stu-id="2410d-119">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="2410d-120">Vi anbefaler, at du aktiverer og tester Administration af frynsegoder i et **sandkassemiljø**, før du aktiverer det i et **produktionsmiljø**.</span><span class="sxs-lookup"><span data-stu-id="2410d-120">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="2410d-121">Der er betydelige forskelle mellem den gamle frynsegodefunktionalitet og de nye funktioner til administration af frynsegoder, der kræver yderligere opsætning, og som skal testes, før de bringes i produktion.</span><span class="sxs-lookup"><span data-stu-id="2410d-121">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="2410d-122">Administrere funktioner</span><span class="sxs-lookup"><span data-stu-id="2410d-122">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="2410d-123">Konfigurer medarbejderoplysninger</span><span class="sxs-lookup"><span data-stu-id="2410d-123">Configure employee information</span></span>

<span data-ttu-id="2410d-124">Før du kan tilmelde medarbejdere til frynsegoder, skal du angive de nødvendige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="2410d-124">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="2410d-125">Du skal melde en medarbejder til en **Fast lønstruktur** på medarbejderens startdato, og du skal vælge en **Frekvens for udbetaling af frynsegoder** i **Ansættelsesoplysninger** i formularen **Arbejder**.</span><span class="sxs-lookup"><span data-stu-id="2410d-125">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="2410d-126">Hvis du har en medarbejder, der modtager supplerende kompensation såsom provision, kan du tilføje et beløb for **Årlig frynsegodeløn** fra medarbejderposten.</span><span class="sxs-lookup"><span data-stu-id="2410d-126">If you have an employee who receives supplemental compensation like commissions, you can add a **Benefits annual salary** amount from the employee record.</span></span> <span data-ttu-id="2410d-127">Human Resources skal bruge beløbet for **Årlig frynsegodeløn** til bestemmelse af dækningsbeløb i stedet for det årlige beløb for fast løn.</span><span class="sxs-lookup"><span data-stu-id="2410d-127">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> <span data-ttu-id="2410d-128">**Årlig frynsegodeløn** skal være gyldig pr. medarbejderens startdato eller starten af frynsegodeperioden, afhængigt af hvad der er den seneste.</span><span class="sxs-lookup"><span data-stu-id="2410d-128">The **Benefits annual salary** must be valid as of the employee’s start date or the beginning of the benefit period, whichever is latest.</span></span> <span data-ttu-id="2410d-129">Hvis der registreres både en fast løn og et årligt frynsegodebeløb for medarbejderen, vil de årlige frynsegoder blive brugt til at fastlægge dækningsbeløbene.</span><span class="sxs-lookup"><span data-stu-id="2410d-129">If both a fixed compensation and benefits annual salary amount is recorded for an employee, the benefits annual salary will be used in determining coverage amounts.</span></span>

<span data-ttu-id="2410d-130">Når du opretter en frynsegodeplan, som bruger satser, der er baseret på køn eller alder, skal du angive medarbejderens fødselsdato og køn, som kan bruges til at beregne frynsegodeomkostningerne.</span><span class="sxs-lookup"><span data-stu-id="2410d-130">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="2410d-131">Konfigurere administration af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="2410d-131">Configure Benefits management</span></span>

<span data-ttu-id="2410d-132">Før du kan oprette frynsegodeplaner for dine medarbejdere, skal du konfigurere indstillinger for planerne.</span><span class="sxs-lookup"><span data-stu-id="2410d-132">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="2410d-133">Angive parametre for administration af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="2410d-133">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="2410d-134">Konfigurere berettigelsesregler og -indstillinger</span><span class="sxs-lookup"><span data-stu-id="2410d-134">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="2410d-135">Konfigurere indstillinger for personlig kontaktberettigelse</span><span class="sxs-lookup"><span data-stu-id="2410d-135">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="2410d-136">Oprette disponeringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="2410d-136">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="2410d-137">Konfigurere betalingshyppigheder</span><span class="sxs-lookup"><span data-stu-id="2410d-137">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="2410d-138">Konfigurere livsbegivenhedstyper</span><span class="sxs-lookup"><span data-stu-id="2410d-138">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="2410d-139">Oprette plantyper</span><span class="sxs-lookup"><span data-stu-id="2410d-139">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="2410d-140">Konfigurere årsagskoder</span><span class="sxs-lookup"><span data-stu-id="2410d-140">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="2410d-141">Konfigurere niveaukoder</span><span class="sxs-lookup"><span data-stu-id="2410d-141">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="2410d-142">Konfigurere satser</span><span class="sxs-lookup"><span data-stu-id="2410d-142">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="2410d-143">Konfigurere fradrag</span><span class="sxs-lookup"><span data-stu-id="2410d-143">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="2410d-144">Konfigurere ventedage</span><span class="sxs-lookup"><span data-stu-id="2410d-144">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="2410d-145">Konfigurere venteperioder</span><span class="sxs-lookup"><span data-stu-id="2410d-145">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="2410d-146">Konfigurere afrundingsregler</span><span class="sxs-lookup"><span data-stu-id="2410d-146">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="2410d-147">Oprette ansættelseskategorier</span><span class="sxs-lookup"><span data-stu-id="2410d-147">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="2410d-148">Konfigurere ansættelsestyper</span><span class="sxs-lookup"><span data-stu-id="2410d-148">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="2410d-149">Konfigurere medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="2410d-149">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="2410d-150">Oprette frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="2410d-150">Create benefit plans</span></span>

<span data-ttu-id="2410d-151">Disse artikler viser, hvordan du opretter frynsegodeplaner, herunder pakker og flekskreditprogrammer.</span><span class="sxs-lookup"><span data-stu-id="2410d-151">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="2410d-152">Konfigurere frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="2410d-152">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="2410d-153">Konfigurere flekskreditprogrammer</span><span class="sxs-lookup"><span data-stu-id="2410d-153">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="2410d-154">Behandle frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="2410d-154">Process benefit plans</span></span>

<span data-ttu-id="2410d-155">Du skal behandle nogle af ændringerne for at gøre dem aktive.</span><span class="sxs-lookup"><span data-stu-id="2410d-155">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="2410d-156">Behandle tilmeldingsberettigelse</span><span class="sxs-lookup"><span data-stu-id="2410d-156">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="2410d-157">Behandle livshændelser</span><span class="sxs-lookup"><span data-stu-id="2410d-157">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="2410d-158">Behandle ændringer af livshændelse</span><span class="sxs-lookup"><span data-stu-id="2410d-158">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="2410d-159">Behandle berettigelse til livshændelse</span><span class="sxs-lookup"><span data-stu-id="2410d-159">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="2410d-160">Behandle satsændringer</span><span class="sxs-lookup"><span data-stu-id="2410d-160">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]