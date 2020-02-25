---
title: Konfigurere orlovs- og fraværstyper
description: Konfigurer de orlovstyper, medarbejderne kan tage i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1748ec2a888a50af9b9260720dfd439adc4686f9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008526"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="322b9-103">Konfigurere orlovs- og fraværstyper</span><span class="sxs-lookup"><span data-stu-id="322b9-103">Configure leave and absence types</span></span>

<span data-ttu-id="322b9-104">Orlovstyper i Dynamics 365 Human Resources bruges til at definere de forskellige typer fravær, som medarbejdere kan rapportere.</span><span class="sxs-lookup"><span data-stu-id="322b9-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="322b9-105">Du kan skræddersy orlovstyper i henhold til organisationens behov.</span><span class="sxs-lookup"><span data-stu-id="322b9-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="322b9-106">Eksempler på orlovstyper omfatter:</span><span class="sxs-lookup"><span data-stu-id="322b9-106">Examples of leave types include:</span></span>

- <span data-ttu-id="322b9-107">Betalt fravær (PTO)</span><span class="sxs-lookup"><span data-stu-id="322b9-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="322b9-108">Orlov uden løn</span><span class="sxs-lookup"><span data-stu-id="322b9-108">Unpaid leave</span></span>
- <span data-ttu-id="322b9-109">Ferie med løn</span><span class="sxs-lookup"><span data-stu-id="322b9-109">Paid vacation</span></span>
- <span data-ttu-id="322b9-110">Sygeorlov</span><span class="sxs-lookup"><span data-stu-id="322b9-110">Sick leave</span></span>
- <span data-ttu-id="322b9-111">Sygeorlov</span><span class="sxs-lookup"><span data-stu-id="322b9-111">Medical leave</span></span>
- <span data-ttu-id="322b9-112">Forældreorlov</span><span class="sxs-lookup"><span data-stu-id="322b9-112">Family leave</span></span>
- <span data-ttu-id="322b9-113">Kortvarigt handicap</span><span class="sxs-lookup"><span data-stu-id="322b9-113">Short-term disability</span></span>
- <span data-ttu-id="322b9-114">Tjenestefrihed ved dødsfald</span><span class="sxs-lookup"><span data-stu-id="322b9-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="322b9-115">Tilføje en orlovstype</span><span class="sxs-lookup"><span data-stu-id="322b9-115">Add a leave type</span></span>

1. <span data-ttu-id="322b9-116">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="322b9-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="322b9-117">Vælg **Orlovs- og fraværstyper** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="322b9-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="322b9-118">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="322b9-118">Select **New**.</span></span>

4. <span data-ttu-id="322b9-119">Angiv et navn til orlovstypen under **Type**, vælg en arbejdsgang fra **Arbejdsgangs-id**, og indtast en **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="322b9-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="322b9-120">I **Generelt** skal du vælge **Ingen**, **Planlagt** eller **Ikke planlagt** på rullelisten **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="322b9-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="322b9-121">Vælg en lønkode på rullelisten **Lønkode**.</span><span class="sxs-lookup"><span data-stu-id="322b9-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="322b9-122">Under **Årsagskode skal angives** skal du vælge, om du vil kræve en årsagskode.</span><span class="sxs-lookup"><span data-stu-id="322b9-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="322b9-123">Hvis du vil kræve årsagskoder, skal du muligvis tilføje dem.</span><span class="sxs-lookup"><span data-stu-id="322b9-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="322b9-124">Under **Årsagskoder** skal du vælge **Tilføj**, vælge en årsagskode og derefter markere afkrydsningsfeltet **Aktiveret** ved siden af.</span><span class="sxs-lookup"><span data-stu-id="322b9-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="322b9-125">Under **Begræns adgangen til valgte roller** skal du vælge, om du vil begrænse adgangen.</span><span class="sxs-lookup"><span data-stu-id="322b9-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="322b9-126">Vælg derefter sikkerhedsrollerne under **Sikkerhedsroller for denne orlovstype**.</span><span class="sxs-lookup"><span data-stu-id="322b9-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="322b9-127">Sikkerhedsrollerne defineres i den arbejdsgang, du valgte under **Arbejdsgangs-id** tidligere i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="322b9-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="322b9-128">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="322b9-128">Select **Save**.</span></span>

## <a name="configure-preview-features"></a><span data-ttu-id="322b9-129">Konfigurere prøveversioner</span><span class="sxs-lookup"><span data-stu-id="322b9-129">Configure preview features</span></span>

<span data-ttu-id="322b9-130">Hvis du har aktiveret prøvefunktioner for orlov og fravær, skal du også konfigurere indstillingerne for dem.</span><span class="sxs-lookup"><span data-stu-id="322b9-130">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="322b9-131">Angiv afrundingsindstillinger for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="322b9-131">Set rounding options for the leave type.</span></span> <span data-ttu-id="322b9-132">Indstillingerne omfatter **Ingen**, **Op**, **Ned** og **Nærmeste**.</span><span class="sxs-lookup"><span data-stu-id="322b9-132">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="322b9-133">Du kan også angive afrundingspræcision for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="322b9-133">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="322b9-134">Angiv **Helligdagskorrektion** for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="322b9-134">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="322b9-135">Når du vælger denne indstilling, bruger Personale det antal helligdage, der falder på en arbejdsdag, til at bestemme, hvordan der skal periodiseres tid for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="322b9-135">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="322b9-136">Hvis juledag f.eks. falder på en mandag, trækker Personale én dag fra orlovstypen ved behandling af periodiseringer.</span><span class="sxs-lookup"><span data-stu-id="322b9-136">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="322b9-137">Du kan angive helligdage i arbejdstidskalenderen.</span><span class="sxs-lookup"><span data-stu-id="322b9-137">You set holidays in the working time calendar.</span></span> <span data-ttu-id="322b9-138">Du kan finde flere oplysninger under [Oprette en arbejdstidskalender](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="322b9-138">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="322b9-139">Se også</span><span class="sxs-lookup"><span data-stu-id="322b9-139">See also</span></span>

- [<span data-ttu-id="322b9-140">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="322b9-140">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="322b9-141">Oprette en orlovs- og fraværsplan</span><span class="sxs-lookup"><span data-stu-id="322b9-141">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="322b9-142">Oprette en arbejdstidskalender</span><span class="sxs-lookup"><span data-stu-id="322b9-142">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)