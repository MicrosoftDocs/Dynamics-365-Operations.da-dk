---
title: Oversigt over administration af frynsegoder
description: Prøveversionsfunktion til oversigt over administration af frynsegoder i Dynamics 365 Human Resources. Tilbyd dine medarbejdere mulighed for ekstra frynsegoder via en brugervenlig onlineoplevelse.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029457"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="43f5e-104">Oversigt over administration af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="43f5e-104">Benefits management overview</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="43f5e-105">Hvis du vil forblive konkurrencedygtig, skal du tilbyde en lang række frynsegoder for at tiltrække og holde på dine bedste medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="43f5e-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="43f5e-106">Ud over standardfrynsekoder som sundhedsforsikring og tandlægedækning kan det også være en god idé at tilbyde udvidede tjenester som hjælp til adoption, rekreative ordninger og beklædningsgodtgørelse.</span><span class="sxs-lookup"><span data-stu-id="43f5e-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="43f5e-107">Prøveversionsfunktionen til Administration af frynsegoder i Microsoft Dynamics 365 Human Resources giver dig en fleksibel løsning, som understøtter en lang række frynsegodemuligheder.</span><span class="sxs-lookup"><span data-stu-id="43f5e-107">The Benefits management preview feature in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="43f5e-108">Personale inkluderer også en brugervenlig medarbejderoplevelse, der viser det, du tilbyder.</span><span class="sxs-lookup"><span data-stu-id="43f5e-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="43f5e-109">Forbedrede frynsegodeplaner giver dig mulighed for at oprette og administrere unikke frynsegodeplaner og understøtte komplekse satstabeller for frynsegoder og indlejrede niveauer.</span><span class="sxs-lookup"><span data-stu-id="43f5e-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="43f5e-110">Du kan nemt oprette frynsegodeprogrammer, pakker og regler for automatisk registrering, der gør det nemmere for medarbejderne.</span><span class="sxs-lookup"><span data-stu-id="43f5e-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="43f5e-111">Med flekskreditprogrammer kan du gøre det muligt at understøtte pension og andre levetidshændelser.</span><span class="sxs-lookup"><span data-stu-id="43f5e-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="43f5e-112">Omfattende berettigelsesregler sikrer, at de rigtige fordele stilles til rådighed for de rette medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="43f5e-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="43f5e-113">Onlinetilmeldinger til frynsegoder giver medarbejderne en nem oplevelse.</span><span class="sxs-lookup"><span data-stu-id="43f5e-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="43f5e-114">Behandling af kvalificerede levetidshændelser integreres med Medarbejderselvbetjening og understøtter også fremtidige livshændelser.</span><span class="sxs-lookup"><span data-stu-id="43f5e-114">Qualified life event processing integrates with Employee self service, and also supports future life events.</span></span>

<span data-ttu-id="43f5e-115">Hvis du vil have adgang til demodataene, skal du geninstallere dit sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="43f5e-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

<span data-ttu-id="43f5e-116">Du kan angive direkte feedback eller rapportere problemer til: D365BenefitsPreview@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="43f5e-116">You can provide direct feedback or report issues to:  D365BenefitsPreview@microsoft.com.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="43f5e-117">Kendte problemer i forbindelse med Administration af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="43f5e-117">Benefits management known issues</span></span>

### <a name="eligibility-processing"></a><span data-ttu-id="43f5e-118">Berettigelsesbehandling</span><span class="sxs-lookup"><span data-stu-id="43f5e-118">Eligibility processing</span></span>

<span data-ttu-id="43f5e-119">Når du kører frynsegodeberettigelse, der bruger en 1-5X løn, % af løn og dækningsbeløb med fladt beløb, skal datoen for **frynsegodedetaljer** angives til **startdatoen for medarbejder** i **Ansættelseshistorik**.</span><span class="sxs-lookup"><span data-stu-id="43f5e-119">When running eligibility for benefits that use a 1-5X Salary, % of Salary, and Flat Amount coverage amount, you must set the **Benefit details** date to the **Employee start date** in **Employment history**.</span></span> <span data-ttu-id="43f5e-120">Du skal også inkludere **Antal arbejdstimer**, **Betalingshyppighed**og **Årlig frynsegodeløn**.</span><span class="sxs-lookup"><span data-stu-id="43f5e-120">You must also include **Hours worked**, **Payment frequency**, and **Annual benefits salary amount**.</span></span> <span data-ttu-id="43f5e-121">Hvis arbejderen har fast løn, skal du angive **Antal arbejdstimer** og **Betalingshyppighed**.</span><span class="sxs-lookup"><span data-stu-id="43f5e-121">If the worker has fixed compensation, enter **Hours worked** and **Payment frequency**.</span></span> <span data-ttu-id="43f5e-122">Det årlige lønbeløb beregnes.</span><span class="sxs-lookup"><span data-stu-id="43f5e-122">The annual salary amount will calculate.</span></span> <span data-ttu-id="43f5e-123">Hvis medarbejderen er fastansat, er der ikke behov for at angive **Antal arbejdstimer**.</span><span class="sxs-lookup"><span data-stu-id="43f5e-123">If the employee is salaried, you don't need to enter **Hours worked**.</span></span> <span data-ttu-id="43f5e-124">Det anbefales, at du angiver fast løn først, når du opretter nye arbejdere.</span><span class="sxs-lookup"><span data-stu-id="43f5e-124">We recommend that when creating new workers, enter fixed compensation first.</span></span> <span data-ttu-id="43f5e-125">Når du vil opdatere posten med frynsegodedetaljer skal du navigere til **Arbejder > Historik for arbejder > Detaljer om ansættelse**.</span><span class="sxs-lookup"><span data-stu-id="43f5e-125">To update the benefit details record, navigate to **Worker > Worker history > Employment details**.</span></span> <span data-ttu-id="43f5e-126">Juster datoen efter arbejderens startdato.</span><span class="sxs-lookup"><span data-stu-id="43f5e-126">Adjust the date to the worker's start date.</span></span>

### <a name="employee-self-service"></a><span data-ttu-id="43f5e-127">Medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="43f5e-127">Employee self-service</span></span>

<span data-ttu-id="43f5e-128">Medarbejderbeløbet beregnes ikke ved opdatering af dækningsbeløbet for livsforsikring.</span><span class="sxs-lookup"><span data-stu-id="43f5e-128">Employee amount doesn't calculate when updating the coverage amount for life insurance.</span></span> <span data-ttu-id="43f5e-129">Når en medarbejder f.eks. tilbydes en livsforsikringsplan, kan de vælge dækning på op til $50.000 til en pris af $,36 pr. dækning på $1.000.</span><span class="sxs-lookup"><span data-stu-id="43f5e-129">For example, when an employee is offered a life insurance plan, they can select up to $50,000 in coverage at a cost of $.36 per $1,000 of coverage.</span></span>  <span data-ttu-id="43f5e-130">Når medarbejderen opdaterer dækningsbeløbet, forbliver medarbejderens tilknyttede omkostninger nul.</span><span class="sxs-lookup"><span data-stu-id="43f5e-130">When the employee updates the coverage amount, the employee’s associated cost remains at zero.</span></span>

<span data-ttu-id="43f5e-131">For en frynsegodeplan, der kun tillader en enkelt markering af denne plantype, vil brugeren modtage en fejlmeddelelse, hvis de forsøger at frafalde en plan, efter at der er valgt en plan.</span><span class="sxs-lookup"><span data-stu-id="43f5e-131">For a benefit plan that only allows a single selection of that plan type, the user receives an error if they attempt to waive a plan after selecting a plan.</span></span> <span data-ttu-id="43f5e-132">En bruger vælger f.eks. en medicinsk plan og anbringer den i sin indkøbsvogn.</span><span class="sxs-lookup"><span data-stu-id="43f5e-132">For example, a user selects a medical plan and places it in their cart.</span></span> <span data-ttu-id="43f5e-133">Brugeren vælger derefter **Frafald** for en anden medicinsk plan.</span><span class="sxs-lookup"><span data-stu-id="43f5e-133">The user then selects **Waive** for another medical plan.</span></span> <span data-ttu-id="43f5e-134">Brugeren vil modtage en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="43f5e-134">The user will receive an error.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="43f5e-135">Aktivere Administration af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="43f5e-135">Enable Benefits management</span></span>

<span data-ttu-id="43f5e-136">Administration af frynsegoder er en prøveversionsfunktion, og den er kun tilgængelig i **sandkassemiljøer**.</span><span class="sxs-lookup"><span data-stu-id="43f5e-136">Benefits management is a preview feature, and is only available in **Sandbox** environments.</span></span> <span data-ttu-id="43f5e-137">I disse artikler beskrives det, hvordan du kan aktivere prøveversionsfunktioner i Personale.</span><span class="sxs-lookup"><span data-stu-id="43f5e-137">These articles describe how to turn on preview features in Human Resources.</span></span> <span data-ttu-id="43f5e-138">De angiver også, hvilke eksisterende funktioner i Personale, som Administration af frynsegoder erstatter, eller som deaktiveres, når du aktiverer Administration af frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="43f5e-138">They also tell which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

- [<span data-ttu-id="43f5e-139">Administrere funktioner</span><span class="sxs-lookup"><span data-stu-id="43f5e-139">Manage features</span></span>](hr-admin-manage-features.md)
- [<span data-ttu-id="43f5e-140">Prøveversionsfunktion: Administration af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="43f5e-140">Preview feature: Benefits management</span></span>](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a><span data-ttu-id="43f5e-141">Konfigurere Administration af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="43f5e-141">Configure Benefits management</span></span>

<span data-ttu-id="43f5e-142">Før du kan oprette frynsegodeplaner for dine medarbejdere, skal du konfigurere indstillinger for planerne.</span><span class="sxs-lookup"><span data-stu-id="43f5e-142">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="43f5e-143">Angive parametre for administration af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="43f5e-143">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="43f5e-144">Konfigurere berettigelsesregler og -indstillinger</span><span class="sxs-lookup"><span data-stu-id="43f5e-144">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="43f5e-145">Konfigurere berettigelsesindstillinger for personlige kontakter</span><span class="sxs-lookup"><span data-stu-id="43f5e-145">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="43f5e-146">Oprette disponeringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="43f5e-146">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="43f5e-147">Konfigurere betalingsfrekvenser</span><span class="sxs-lookup"><span data-stu-id="43f5e-147">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="43f5e-148">Konfigurere typer af livshændelser</span><span class="sxs-lookup"><span data-stu-id="43f5e-148">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="43f5e-149">Oprette plantyper</span><span class="sxs-lookup"><span data-stu-id="43f5e-149">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="43f5e-150">Definer årsagskoder</span><span class="sxs-lookup"><span data-stu-id="43f5e-150">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="43f5e-151">Konfigurere niveaukoder</span><span class="sxs-lookup"><span data-stu-id="43f5e-151">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="43f5e-152">Konfigurere satser</span><span class="sxs-lookup"><span data-stu-id="43f5e-152">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="43f5e-153">Konfigurere fradrag</span><span class="sxs-lookup"><span data-stu-id="43f5e-153">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="43f5e-154">Konfigurere ventedage</span><span class="sxs-lookup"><span data-stu-id="43f5e-154">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="43f5e-155">Konfigurere venteperioder</span><span class="sxs-lookup"><span data-stu-id="43f5e-155">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="43f5e-156">Konfigurere afrundingsregler</span><span class="sxs-lookup"><span data-stu-id="43f5e-156">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="43f5e-157">Oprette ansættelseskategorier</span><span class="sxs-lookup"><span data-stu-id="43f5e-157">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="43f5e-158">Konfigurere ansættelsestyper</span><span class="sxs-lookup"><span data-stu-id="43f5e-158">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="43f5e-159">Konfigurere medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="43f5e-159">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="43f5e-160">Oprette frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="43f5e-160">Create benefit plans</span></span>

<span data-ttu-id="43f5e-161">Disse artikler viser, hvordan du opretter frynsegodeplaner, herunder pakker og flekskreditprogrammer.</span><span class="sxs-lookup"><span data-stu-id="43f5e-161">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="43f5e-162">Konfigurere frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="43f5e-162">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="43f5e-163">Oprette frynsegodeplaner for arbejdere</span><span class="sxs-lookup"><span data-stu-id="43f5e-163">Create worker benefit plans</span></span>](hr-benefits-plans-worker.md)
- [<span data-ttu-id="43f5e-164">Konfigurere flekskreditprogrammer</span><span class="sxs-lookup"><span data-stu-id="43f5e-164">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)
- [<span data-ttu-id="43f5e-165">Konfigurere fremtidige livshændelser</span><span class="sxs-lookup"><span data-stu-id="43f5e-165">Configure future life events</span></span>](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="43f5e-166">Behandle frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="43f5e-166">Process benefit plans</span></span>

<span data-ttu-id="43f5e-167">Du skal behandle nogle af ændringerne for at gøre dem aktive.</span><span class="sxs-lookup"><span data-stu-id="43f5e-167">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="43f5e-168">Behandle tilmeldingsberettigelse</span><span class="sxs-lookup"><span data-stu-id="43f5e-168">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="43f5e-169">Behandle livshændelser</span><span class="sxs-lookup"><span data-stu-id="43f5e-169">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="43f5e-170">Behandle ændringer af livshændelse</span><span class="sxs-lookup"><span data-stu-id="43f5e-170">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="43f5e-171">Behandle berettigelse til livshændelse</span><span class="sxs-lookup"><span data-stu-id="43f5e-171">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="43f5e-172">Behandle satsændringer</span><span class="sxs-lookup"><span data-stu-id="43f5e-172">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

