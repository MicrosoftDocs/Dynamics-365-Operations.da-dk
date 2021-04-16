---
title: Konfigurere orlovs- og fraværstyper
description: Konfigurer de orlovstyper, medarbejderne kan tage i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf868ad44e52b0ed7d0ca6e1f133efa030f3c4a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794559"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="f6a96-103">Konfigurere orlovs- og fraværstyper</span><span class="sxs-lookup"><span data-stu-id="f6a96-103">Configure leave and absence types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f6a96-104">Orlovstyper i Dynamics 365 Human Resources bruges til at definere de forskellige typer fravær, som medarbejdere kan rapportere.</span><span class="sxs-lookup"><span data-stu-id="f6a96-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="f6a96-105">Du kan skræddersy orlovstyper i henhold til organisationens behov.</span><span class="sxs-lookup"><span data-stu-id="f6a96-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="f6a96-106">Eksempler på orlovstyper omfatter:</span><span class="sxs-lookup"><span data-stu-id="f6a96-106">Examples of leave types include:</span></span>

- <span data-ttu-id="f6a96-107">Betalt fravær (PTO)</span><span class="sxs-lookup"><span data-stu-id="f6a96-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="f6a96-108">Orlov uden løn</span><span class="sxs-lookup"><span data-stu-id="f6a96-108">Unpaid leave</span></span>
- <span data-ttu-id="f6a96-109">Ferie med løn</span><span class="sxs-lookup"><span data-stu-id="f6a96-109">Paid vacation</span></span>
- <span data-ttu-id="f6a96-110">Sygeorlov</span><span class="sxs-lookup"><span data-stu-id="f6a96-110">Sick leave</span></span>
- <span data-ttu-id="f6a96-111">Sygeorlov</span><span class="sxs-lookup"><span data-stu-id="f6a96-111">Medical leave</span></span>
- <span data-ttu-id="f6a96-112">Forældreorlov</span><span class="sxs-lookup"><span data-stu-id="f6a96-112">Family leave</span></span>
- <span data-ttu-id="f6a96-113">Kortvarigt handicap</span><span class="sxs-lookup"><span data-stu-id="f6a96-113">Short-term disability</span></span>
- <span data-ttu-id="f6a96-114">Tjenestefrihed ved dødsfald</span><span class="sxs-lookup"><span data-stu-id="f6a96-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="f6a96-115">Tilføje en orlovstype</span><span class="sxs-lookup"><span data-stu-id="f6a96-115">Add a leave type</span></span>

1. <span data-ttu-id="f6a96-116">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="f6a96-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="f6a96-117">Vælg **Orlovs- og fraværstyper** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f6a96-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="f6a96-118">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f6a96-118">Select **New**.</span></span>

4. <span data-ttu-id="f6a96-119">Angiv et navn til orlovstypen under **Type**, vælg en arbejdsgang fra **Arbejdsgangs-id**, og indtast en **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f6a96-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="f6a96-120">I **Generelt** skal du vælge **Ingen**, **Planlagt** eller **Ikke planlagt** på rullelisten **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="f6a96-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="f6a96-121">Vælg en lønkode på rullelisten **Lønkode**.</span><span class="sxs-lookup"><span data-stu-id="f6a96-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="f6a96-122">Under **Årsagskode skal angives** skal du vælge, om du vil kræve en årsagskode.</span><span class="sxs-lookup"><span data-stu-id="f6a96-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="f6a96-123">Hvis du vil kræve årsagskoder, skal du muligvis tilføje dem.</span><span class="sxs-lookup"><span data-stu-id="f6a96-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="f6a96-124">Under **Årsagskoder** skal du vælge **Tilføj**, vælge en årsagskode og derefter markere afkrydsningsfeltet **Aktiveret** ved siden af.</span><span class="sxs-lookup"><span data-stu-id="f6a96-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="f6a96-125">Under **Begræns adgangen til valgte roller** skal du vælge, om du vil begrænse adgangen.</span><span class="sxs-lookup"><span data-stu-id="f6a96-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="f6a96-126">Vælg derefter sikkerhedsrollerne under **Sikkerhedsroller for denne orlovstype**.</span><span class="sxs-lookup"><span data-stu-id="f6a96-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="f6a96-127">Sikkerhedsrollerne defineres i den arbejdsgang, du valgte under **Arbejdsgangs-id** tidligere i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="f6a96-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="f6a96-128">Vælg den farve, der skal vises på orlovs- og fraværskalendere for denne orlovstype, under **Kalenderfarve**.</span><span class="sxs-lookup"><span data-stu-id="f6a96-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="f6a96-129">Under **Suspensionsforhold** skal du vælge, om du ønsker, at denne orlovstype enten skal suspendere en anden orlovstype, eller den skal suspenderes af en anden orlovstype.</span><span class="sxs-lookup"><span data-stu-id="f6a96-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="f6a96-130">Når der sendes en orlovsanmodning for den suspenderende orlovstype, oprettes der automatisk en orlovssuspendering for den suspenderede orlovstype.</span><span class="sxs-lookup"><span data-stu-id="f6a96-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="f6a96-131">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f6a96-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="f6a96-132">Konfigurere regler for orlovstype</span><span class="sxs-lookup"><span data-stu-id="f6a96-132">Configure leave type rules</span></span>

1. <span data-ttu-id="f6a96-133">Angiv afrundingsindstillinger for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="f6a96-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="f6a96-134">Indstillingerne omfatter **Ingen**, **Op**, **Ned** og **Nærmeste**.</span><span class="sxs-lookup"><span data-stu-id="f6a96-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="f6a96-135">Du kan også angive afrundingspræcision for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="f6a96-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="f6a96-136">Angiv **Helligdagskorrektion** for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="f6a96-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="f6a96-137">Når du vælger denne indstilling, bruger Human Resources det antal helligdage, der falder på en arbejdsdag, til at bestemme, hvordan der skal periodiseres tid for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="f6a96-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="f6a96-138">Hvis juledag f.eks. falder på en mandag, trækker Human Resources én dag fra orlovstypen ved behandling af periodiseringer.</span><span class="sxs-lookup"><span data-stu-id="f6a96-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="f6a96-139">Du kan angive helligdage i arbejdstidskalenderen.</span><span class="sxs-lookup"><span data-stu-id="f6a96-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="f6a96-140">Du kan finde flere oplysninger under [Oprette en arbejdstidskalender](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="f6a96-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="f6a96-141">Angiv **Overført orlovstype** for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="f6a96-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="f6a96-142">Når du vælger denne indstilling, overføres eventuelle overførte saldi til den angivne orlovstype.</span><span class="sxs-lookup"><span data-stu-id="f6a96-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="f6a96-143">Type overført orlov skal også medtages i orlovs- og fraværsplanen.</span><span class="sxs-lookup"><span data-stu-id="f6a96-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="f6a96-144">Definer **Udløbsregler** for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="f6a96-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="f6a96-145">Når du konfigurerer denne indstilling, kan du vælge enheden dage eller måneder og angive varigheden for udløbet.</span><span class="sxs-lookup"><span data-stu-id="f6a96-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="f6a96-146">Du kan også angive ikrafttrædelsesdatoen for udløbsreglen.</span><span class="sxs-lookup"><span data-stu-id="f6a96-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="f6a96-147">Ikrafttrædelsesdatoen bruges til at bestemme, hvornår du skal begynde at køre det batchjob, der behandler udløbet af orlov, eller den dato, hvor reglen træder i kraft.</span><span class="sxs-lookup"><span data-stu-id="f6a96-147">The effective date is used to determine when to start running the batch job that processes the leave expiration, or the date when the rule takes effect.</span></span> <span data-ttu-id="f6a96-148">Selve udløbet finder altid sted på startdatoen for orlovsplanen, når batchjobbet er indstillet til at blive behandlet.</span><span class="sxs-lookup"><span data-stu-id="f6a96-148">The expiration itself will always happen on the leave plan start date once the batch job is set to process.</span></span> <span data-ttu-id="f6a96-149">Planens startdato kan f.eks. være den 1. januar 2020, men reglen blev først oprettet den 1. juni 2020.</span><span class="sxs-lookup"><span data-stu-id="f6a96-149">For example, the plan start date may be 1/1/2020, but the rule wasn't created until 6/1/2020.</span></span> <span data-ttu-id="f6a96-150">Hvis ikrafttrædelsesdatoen angives til 1. juni 2020, behandles reglen ved den næste årsgrænse, dvs. 1. januar 2021.</span><span class="sxs-lookup"><span data-stu-id="f6a96-150">By setting the effective date to 6/1/2020, the rule will be processed on the next year boundary, so 1/1/2021.</span></span> <span data-ttu-id="f6a96-151">De orlovssaldi, der findes på tidspunktet for udløbet, trækkes fra orlovstypen og afspejles i orloven.</span><span class="sxs-lookup"><span data-stu-id="f6a96-151">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
## <a name="see-also"></a><span data-ttu-id="f6a96-152">Se også</span><span class="sxs-lookup"><span data-stu-id="f6a96-152">See also</span></span>

- [<span data-ttu-id="f6a96-153">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="f6a96-153">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="f6a96-154">Oprette en plan for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="f6a96-154">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="f6a96-155">Oprette en arbejdstidskalender</span><span class="sxs-lookup"><span data-stu-id="f6a96-155">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="f6a96-156">Stoppe orlov midlertidigt</span><span class="sxs-lookup"><span data-stu-id="f6a96-156">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
