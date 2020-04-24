---
title: Konfigurere orlovs- og fraværstyper
description: Konfigurer de orlovstyper, medarbejderne kan tage i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
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
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198044"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="1e1c0-103">Konfigurere orlovs- og fraværstyper</span><span class="sxs-lookup"><span data-stu-id="1e1c0-103">Configure leave and absence types</span></span>

<span data-ttu-id="1e1c0-104">Orlovstyper i Dynamics 365 Human Resources bruges til at definere de forskellige typer fravær, som medarbejdere kan rapportere.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="1e1c0-105">Du kan skræddersy orlovstyper i henhold til organisationens behov.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="1e1c0-106">Eksempler på orlovstyper omfatter:</span><span class="sxs-lookup"><span data-stu-id="1e1c0-106">Examples of leave types include:</span></span>

- <span data-ttu-id="1e1c0-107">Betalt fravær (PTO)</span><span class="sxs-lookup"><span data-stu-id="1e1c0-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="1e1c0-108">Orlov uden løn</span><span class="sxs-lookup"><span data-stu-id="1e1c0-108">Unpaid leave</span></span>
- <span data-ttu-id="1e1c0-109">Ferie med løn</span><span class="sxs-lookup"><span data-stu-id="1e1c0-109">Paid vacation</span></span>
- <span data-ttu-id="1e1c0-110">Sygeorlov</span><span class="sxs-lookup"><span data-stu-id="1e1c0-110">Sick leave</span></span>
- <span data-ttu-id="1e1c0-111">Sygeorlov</span><span class="sxs-lookup"><span data-stu-id="1e1c0-111">Medical leave</span></span>
- <span data-ttu-id="1e1c0-112">Forældreorlov</span><span class="sxs-lookup"><span data-stu-id="1e1c0-112">Family leave</span></span>
- <span data-ttu-id="1e1c0-113">Kortvarigt handicap</span><span class="sxs-lookup"><span data-stu-id="1e1c0-113">Short-term disability</span></span>
- <span data-ttu-id="1e1c0-114">Tjenestefrihed ved dødsfald</span><span class="sxs-lookup"><span data-stu-id="1e1c0-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="1e1c0-115">Tilføje en orlovstype</span><span class="sxs-lookup"><span data-stu-id="1e1c0-115">Add a leave type</span></span>

1. <span data-ttu-id="1e1c0-116">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="1e1c0-117">Vælg **Orlovs- og fraværstyper** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="1e1c0-118">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-118">Select **New**.</span></span>

4. <span data-ttu-id="1e1c0-119">Angiv et navn til orlovstypen under **Type**, vælg en arbejdsgang fra **Arbejdsgangs-id**, og indtast en **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="1e1c0-120">I **Generelt** skal du vælge **Ingen**, **Planlagt** eller **Ikke planlagt** på rullelisten **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="1e1c0-121">Vælg en lønkode på rullelisten **Lønkode**.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="1e1c0-122">Under **Årsagskode skal angives** skal du vælge, om du vil kræve en årsagskode.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="1e1c0-123">Hvis du vil kræve årsagskoder, skal du muligvis tilføje dem.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="1e1c0-124">Under **Årsagskoder** skal du vælge **Tilføj**, vælge en årsagskode og derefter markere afkrydsningsfeltet **Aktiveret** ved siden af.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="1e1c0-125">Under **Begræns adgangen til valgte roller** skal du vælge, om du vil begrænse adgangen.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="1e1c0-126">Vælg derefter sikkerhedsrollerne under **Sikkerhedsroller for denne orlovstype**.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="1e1c0-127">Sikkerhedsrollerne defineres i den arbejdsgang, du valgte under **Arbejdsgangs-id** tidligere i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="1e1c0-128">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-128">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="1e1c0-129">Konfigurere regler for orlovstype</span><span class="sxs-lookup"><span data-stu-id="1e1c0-129">Configure leave type rules</span></span>

1. <span data-ttu-id="1e1c0-130">Angiv afrundingsindstillinger for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-130">Set rounding options for the leave type.</span></span> <span data-ttu-id="1e1c0-131">Indstillingerne omfatter **Ingen**, **Op**, **Ned** og **Nærmeste**.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-131">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="1e1c0-132">Du kan også angive afrundingspræcision for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-132">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="1e1c0-133">Angiv **Helligdagskorrektion** for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-133">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="1e1c0-134">Når du vælger denne indstilling, bruger Personale det antal helligdage, der falder på en arbejdsdag, til at bestemme, hvordan der skal periodiseres tid for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-134">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="1e1c0-135">Hvis juledag f.eks. falder på en mandag, trækker Personale én dag fra orlovstypen ved behandling af periodiseringer.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-135">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="1e1c0-136">Du kan angive helligdage i arbejdstidskalenderen.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-136">You set holidays in the working time calendar.</span></span> <span data-ttu-id="1e1c0-137">Du kan finde flere oplysninger under [Oprette en arbejdstidskalender](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="1e1c0-137">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
## <a name="configure-preview-features"></a><span data-ttu-id="1e1c0-138">Konfigurere prøveversioner</span><span class="sxs-lookup"><span data-stu-id="1e1c0-138">Configure preview features</span></span>

<span data-ttu-id="1e1c0-139">Hvis du har aktiveret prøvefunktioner for orlov og fravær, skal du også konfigurere indstillingerne for dem.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-139">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="1e1c0-140">Vælg orlovstypen for de overførselssaldi, der skal overføres til.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-140">Choose the leave type for carry forward balances to be transferred to.</span></span> <span data-ttu-id="1e1c0-141">Du kan også oprette en ny orlovstype til overførsel.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-141">You can also create a new leave type for carry forward.</span></span> 

## <a name="see-also"></a><span data-ttu-id="1e1c0-142">Se også</span><span class="sxs-lookup"><span data-stu-id="1e1c0-142">See also</span></span>

- [<span data-ttu-id="1e1c0-143">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="1e1c0-143">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="1e1c0-144">Oprette en plan for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="1e1c0-144">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="1e1c0-145">Oprette en arbejdstidskalender</span><span class="sxs-lookup"><span data-stu-id="1e1c0-145">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
