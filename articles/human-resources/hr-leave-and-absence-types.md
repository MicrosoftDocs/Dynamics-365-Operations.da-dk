---
title: Konfigurere orlovs- og fraværstyper
description: Konfigurer de orlovstyper, medarbejderne kan tage i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39e4c4b9c83ca648c21ac20bd20b739af8a6b9ed
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271121"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="936d7-103">Konfigurere orlovs- og fraværstyper</span><span class="sxs-lookup"><span data-stu-id="936d7-103">Configure leave and absence types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="936d7-104">Orlovstyper i Dynamics 365 Human Resources bruges til at definere de forskellige typer fravær, som medarbejdere kan rapportere.</span><span class="sxs-lookup"><span data-stu-id="936d7-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="936d7-105">Du kan skræddersy orlovstyper i henhold til organisationens behov.</span><span class="sxs-lookup"><span data-stu-id="936d7-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="936d7-106">Eksempler på orlovstyper omfatter:</span><span class="sxs-lookup"><span data-stu-id="936d7-106">Examples of leave types include:</span></span>

- <span data-ttu-id="936d7-107">Betalt fravær (PTO)</span><span class="sxs-lookup"><span data-stu-id="936d7-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="936d7-108">Orlov uden løn</span><span class="sxs-lookup"><span data-stu-id="936d7-108">Unpaid leave</span></span>
- <span data-ttu-id="936d7-109">Ferie med løn</span><span class="sxs-lookup"><span data-stu-id="936d7-109">Paid vacation</span></span>
- <span data-ttu-id="936d7-110">Sygeorlov</span><span class="sxs-lookup"><span data-stu-id="936d7-110">Sick leave</span></span>
- <span data-ttu-id="936d7-111">Sygeorlov</span><span class="sxs-lookup"><span data-stu-id="936d7-111">Medical leave</span></span>
- <span data-ttu-id="936d7-112">Forældreorlov</span><span class="sxs-lookup"><span data-stu-id="936d7-112">Family leave</span></span>
- <span data-ttu-id="936d7-113">Kortvarigt handicap</span><span class="sxs-lookup"><span data-stu-id="936d7-113">Short-term disability</span></span>
- <span data-ttu-id="936d7-114">Tjenestefrihed ved dødsfald</span><span class="sxs-lookup"><span data-stu-id="936d7-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="936d7-115">Tilføje en orlovstype</span><span class="sxs-lookup"><span data-stu-id="936d7-115">Add a leave type</span></span>

1. <span data-ttu-id="936d7-116">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="936d7-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="936d7-117">Vælg **Orlovs- og fraværstyper** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="936d7-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="936d7-118">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="936d7-118">Select **New**.</span></span>

4. <span data-ttu-id="936d7-119">Angiv et navn til orlovstypen under **Type**, vælg en arbejdsgang fra **Arbejdsgangs-id**, og indtast en **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="936d7-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="936d7-120">I **Generelt** skal du vælge **Ingen**, **Planlagt** eller **Ikke planlagt** på rullelisten **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="936d7-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="936d7-121">Vælg en lønkode på rullelisten **Lønkode**.</span><span class="sxs-lookup"><span data-stu-id="936d7-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="936d7-122">Under **Årsagskode skal angives** skal du vælge, om du vil kræve en årsagskode.</span><span class="sxs-lookup"><span data-stu-id="936d7-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="936d7-123">Hvis du vil kræve årsagskoder, skal du muligvis tilføje dem.</span><span class="sxs-lookup"><span data-stu-id="936d7-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="936d7-124">Under **Årsagskoder** skal du vælge **Tilføj**, vælge en årsagskode og derefter markere afkrydsningsfeltet **Aktiveret** ved siden af.</span><span class="sxs-lookup"><span data-stu-id="936d7-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="936d7-125">Under **Begræns adgangen til valgte roller** skal du vælge, om du vil begrænse adgangen.</span><span class="sxs-lookup"><span data-stu-id="936d7-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="936d7-126">Vælg derefter sikkerhedsrollerne under **Sikkerhedsroller for denne orlovstype**.</span><span class="sxs-lookup"><span data-stu-id="936d7-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="936d7-127">Sikkerhedsrollerne defineres i den arbejdsgang, du valgte under **Arbejdsgangs-id** tidligere i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="936d7-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="936d7-128">Vælg den farve, der skal vises på orlovs- og fraværskalendere for denne orlovstype, under **Kalenderfarve**.</span><span class="sxs-lookup"><span data-stu-id="936d7-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="936d7-129">Under **Suspensionsforhold** skal du vælge, om du ønsker, at denne orlovstype enten skal suspendere en anden orlovstype, eller den skal suspenderes af en anden orlovstype.</span><span class="sxs-lookup"><span data-stu-id="936d7-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="936d7-130">Når der sendes en orlovsanmodning for den suspenderende orlovstype, oprettes der automatisk en orlovssuspendering for den suspenderede orlovstype.</span><span class="sxs-lookup"><span data-stu-id="936d7-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="936d7-131">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="936d7-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="936d7-132">Konfigurere regler for orlovstype</span><span class="sxs-lookup"><span data-stu-id="936d7-132">Configure leave type rules</span></span>

1. <span data-ttu-id="936d7-133">Angiv afrundingsindstillinger for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="936d7-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="936d7-134">Indstillingerne omfatter **Ingen**, **Op**, **Ned** og **Nærmeste**.</span><span class="sxs-lookup"><span data-stu-id="936d7-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="936d7-135">Du kan også angive afrundingspræcision for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="936d7-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="936d7-136">Angiv **Helligdagskorrektion** for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="936d7-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="936d7-137">Når du vælger denne indstilling, bruger Human Resources det antal helligdage, der falder på en arbejdsdag, til at bestemme, hvordan der skal periodiseres tid for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="936d7-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="936d7-138">Hvis juledag f.eks. falder på en mandag, trækker Human Resources én dag fra orlovstypen ved behandling af periodiseringer.</span><span class="sxs-lookup"><span data-stu-id="936d7-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="936d7-139">Du kan angive helligdage i arbejdstidskalenderen.</span><span class="sxs-lookup"><span data-stu-id="936d7-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="936d7-140">Du kan finde flere oplysninger under [Oprette en arbejdstidskalender](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="936d7-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="936d7-141">Angiv **Overført orlovstype** for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="936d7-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="936d7-142">Når du vælger denne indstilling, overføres eventuelle overførte saldi til den angivne orlovstype.</span><span class="sxs-lookup"><span data-stu-id="936d7-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="936d7-143">Type overført orlov skal også medtages i orlovs- og fraværsplanen.</span><span class="sxs-lookup"><span data-stu-id="936d7-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
4. <span data-ttu-id="936d7-144">Definer **Udløbsregler** for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="936d7-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="936d7-145">Når du konfigurerer denne indstilling, kan du vælge enheden dage eller måneder og angive varigheden for udløbet.</span><span class="sxs-lookup"><span data-stu-id="936d7-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiration.</span></span> <span data-ttu-id="936d7-146">Ikrafttrædelsesdatoen for udløbsreglen bruges til at bestemme, hvornår du skal begynde at køre det batchjob, der behandler udløbet af orlov, eller den dato, hvor reglen træder i kraft.</span><span class="sxs-lookup"><span data-stu-id="936d7-146">The effective date of the expiration rule is used to determine when to start running the batch job that processes the leave expiration, or the date when the rule takes effect.</span></span> <span data-ttu-id="936d7-147">Selve udløbet finder altid sted på startdatoen for periodiseringsperioden.</span><span class="sxs-lookup"><span data-stu-id="936d7-147">The expiration itself will always occur on the accrual period start date.</span></span> <span data-ttu-id="936d7-148">Hvis startdatoen for periodiseringsperioden f.eks. er 3. august 2021, og udløbsreglen er angivet til 6 måneder, behandles reglen på baggrund af udløbsforskydningen fra startdatoen for periodiseringsperioden, så den udføres den 3. februar 2022.</span><span class="sxs-lookup"><span data-stu-id="936d7-148">For example, if the accrual period start date is August 3, 2021, and the expiration rule was set at 6 months, the rule will be processed based on the expiration offset from the accrual period start date, so it would be executed on February 3, 2022.</span></span> <span data-ttu-id="936d7-149">De orlovssaldi, der findes på tidspunktet for udløbet, trækkes fra orlovstypen og afspejles i orloven.</span><span class="sxs-lookup"><span data-stu-id="936d7-149">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span>
 
## <a name="see-also"></a><span data-ttu-id="936d7-150">Se også</span><span class="sxs-lookup"><span data-stu-id="936d7-150">See also</span></span>

- [<span data-ttu-id="936d7-151">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="936d7-151">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="936d7-152">Oprette en plan for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="936d7-152">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="936d7-153">Oprette en arbejdstidskalender</span><span class="sxs-lookup"><span data-stu-id="936d7-153">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="936d7-154">Stop orlov midlertidigt</span><span class="sxs-lookup"><span data-stu-id="936d7-154">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)
- [<span data-ttu-id="936d7-155">Oprette en arbejdsproces for køb og salg af orlov</span><span class="sxs-lookup"><span data-stu-id="936d7-155">Create a buy and sell leave request workflow</span></span>](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
