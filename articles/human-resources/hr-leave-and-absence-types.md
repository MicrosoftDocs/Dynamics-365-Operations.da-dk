---
title: Konfigurere orlovs- og fraværstyper
description: Konfigurer de orlovstyper, medarbejderne kan tage i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 6b21d4d631bcdf603b38212f5f76bb78937d3d3c
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115070"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="e02a5-103">Konfigurere orlovs- og fraværstyper</span><span class="sxs-lookup"><span data-stu-id="e02a5-103">Configure leave and absence types</span></span>

<span data-ttu-id="e02a5-104">Orlovstyper i Dynamics 365 Human Resources bruges til at definere de forskellige typer fravær, som medarbejdere kan rapportere.</span><span class="sxs-lookup"><span data-stu-id="e02a5-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="e02a5-105">Du kan skræddersy orlovstyper i henhold til organisationens behov.</span><span class="sxs-lookup"><span data-stu-id="e02a5-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="e02a5-106">Eksempler på orlovstyper omfatter:</span><span class="sxs-lookup"><span data-stu-id="e02a5-106">Examples of leave types include:</span></span>

- <span data-ttu-id="e02a5-107">Betalt fravær (PTO)</span><span class="sxs-lookup"><span data-stu-id="e02a5-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="e02a5-108">Orlov uden løn</span><span class="sxs-lookup"><span data-stu-id="e02a5-108">Unpaid leave</span></span>
- <span data-ttu-id="e02a5-109">Ferie med løn</span><span class="sxs-lookup"><span data-stu-id="e02a5-109">Paid vacation</span></span>
- <span data-ttu-id="e02a5-110">Sygeorlov</span><span class="sxs-lookup"><span data-stu-id="e02a5-110">Sick leave</span></span>
- <span data-ttu-id="e02a5-111">Sygeorlov</span><span class="sxs-lookup"><span data-stu-id="e02a5-111">Medical leave</span></span>
- <span data-ttu-id="e02a5-112">Forældreorlov</span><span class="sxs-lookup"><span data-stu-id="e02a5-112">Family leave</span></span>
- <span data-ttu-id="e02a5-113">Kortvarigt handicap</span><span class="sxs-lookup"><span data-stu-id="e02a5-113">Short-term disability</span></span>
- <span data-ttu-id="e02a5-114">Tjenestefrihed ved dødsfald</span><span class="sxs-lookup"><span data-stu-id="e02a5-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="e02a5-115">Tilføje en orlovstype</span><span class="sxs-lookup"><span data-stu-id="e02a5-115">Add a leave type</span></span>

1. <span data-ttu-id="e02a5-116">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="e02a5-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="e02a5-117">Vælg **Orlovs- og fraværstyper** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e02a5-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="e02a5-118">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e02a5-118">Select **New**.</span></span>

4. <span data-ttu-id="e02a5-119">Angiv et navn til orlovstypen under **Type**, vælg en arbejdsgang fra **Arbejdsgangs-id**, og indtast en **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="e02a5-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="e02a5-120">I **Generelt** skal du vælge **Ingen**, **Planlagt** eller **Ikke planlagt** på rullelisten **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="e02a5-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="e02a5-121">Vælg en lønkode på rullelisten **Lønkode**.</span><span class="sxs-lookup"><span data-stu-id="e02a5-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="e02a5-122">Under **Årsagskode skal angives** skal du vælge, om du vil kræve en årsagskode.</span><span class="sxs-lookup"><span data-stu-id="e02a5-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="e02a5-123">Hvis du vil kræve årsagskoder, skal du muligvis tilføje dem.</span><span class="sxs-lookup"><span data-stu-id="e02a5-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="e02a5-124">Under **Årsagskoder** skal du vælge **Tilføj**, vælge en årsagskode og derefter markere afkrydsningsfeltet **Aktiveret** ved siden af.</span><span class="sxs-lookup"><span data-stu-id="e02a5-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="e02a5-125">Under **Begræns adgangen til valgte roller** skal du vælge, om du vil begrænse adgangen.</span><span class="sxs-lookup"><span data-stu-id="e02a5-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="e02a5-126">Vælg derefter sikkerhedsrollerne under **Sikkerhedsroller for denne orlovstype**.</span><span class="sxs-lookup"><span data-stu-id="e02a5-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="e02a5-127">Sikkerhedsrollerne defineres i den arbejdsgang, du valgte under **Arbejdsgangs-id** tidligere i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="e02a5-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="e02a5-128">Vælg den farve, der skal vises på orlovs- og fraværskalendere for denne orlovstype, under **Kalenderfarve**.</span><span class="sxs-lookup"><span data-stu-id="e02a5-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="e02a5-129">Under **Suspensionsforhold** skal du vælge, om du ønsker, at denne orlovstype enten skal suspendere en anden orlovstype, eller den skal suspenderes af en anden orlovstype.</span><span class="sxs-lookup"><span data-stu-id="e02a5-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="e02a5-130">Når der sendes en orlovsanmodning for den suspenderende orlovstype, oprettes der automatisk en orlovssuspendering for den suspenderede orlovstype.</span><span class="sxs-lookup"><span data-stu-id="e02a5-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="e02a5-131">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e02a5-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="e02a5-132">Konfigurere regler for orlovstype</span><span class="sxs-lookup"><span data-stu-id="e02a5-132">Configure leave type rules</span></span>

1. <span data-ttu-id="e02a5-133">Angiv afrundingsindstillinger for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="e02a5-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="e02a5-134">Indstillingerne omfatter **Ingen**, **Op**, **Ned** og **Nærmeste**.</span><span class="sxs-lookup"><span data-stu-id="e02a5-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="e02a5-135">Du kan også angive afrundingspræcision for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="e02a5-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="e02a5-136">Angiv **Helligdagskorrektion** for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="e02a5-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="e02a5-137">Når du vælger denne indstilling, bruger Human Resources det antal helligdage, der falder på en arbejdsdag, til at bestemme, hvordan der skal periodiseres tid for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="e02a5-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="e02a5-138">Hvis juledag f.eks. falder på en mandag, trækker Human Resources én dag fra orlovstypen ved behandling af periodiseringer.</span><span class="sxs-lookup"><span data-stu-id="e02a5-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="e02a5-139">Du kan angive helligdage i arbejdstidskalenderen.</span><span class="sxs-lookup"><span data-stu-id="e02a5-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="e02a5-140">Du kan finde flere oplysninger under [Oprette en arbejdstidskalender](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="e02a5-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="e02a5-141">Angiv **Overført orlovstype** for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="e02a5-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="e02a5-142">Når du vælger denne indstilling, overføres eventuelle overførte saldi til den angivne orlovstype.</span><span class="sxs-lookup"><span data-stu-id="e02a5-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="e02a5-143">Type overført orlov skal også medtages i orlovs- og fraværsplanen.</span><span class="sxs-lookup"><span data-stu-id="e02a5-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="e02a5-144">Definer **Udløbsregler** for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="e02a5-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="e02a5-145">Når du konfigurerer denne indstilling, kan du vælge enheden dage eller måneder og angive varigheden for udløbet.</span><span class="sxs-lookup"><span data-stu-id="e02a5-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="e02a5-146">Du kan også angive ikrafttrædelsesdatoen for udløbsreglen.</span><span class="sxs-lookup"><span data-stu-id="e02a5-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="e02a5-147">De orlovssaldi, der findes på tidspunktet for udløbet, trækkes fra orlovstypen og afspejles i orloven.</span><span class="sxs-lookup"><span data-stu-id="e02a5-147">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
 
## <a name="see-also"></a><span data-ttu-id="e02a5-148">Se også</span><span class="sxs-lookup"><span data-stu-id="e02a5-148">See also</span></span>

- [<span data-ttu-id="e02a5-149">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="e02a5-149">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="e02a5-150">Oprette en plan for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="e02a5-150">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="e02a5-151">Oprette en arbejdstidskalender</span><span class="sxs-lookup"><span data-stu-id="e02a5-151">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="e02a5-152">Stoppe orlov midlertidigt</span><span class="sxs-lookup"><span data-stu-id="e02a5-152">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)

