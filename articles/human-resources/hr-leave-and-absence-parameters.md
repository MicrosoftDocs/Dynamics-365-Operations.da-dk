---
title: Konfigurere parametre for orlov og fravær
description: Definer personaleparametre for orlov og fravær i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
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
ms.openlocfilehash: e1b2de94f9d9ac1ada16b6ef0e7628edbc9d683f
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "4997095"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="7eaca-103">Konfigurere parametre for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="7eaca-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="7eaca-104">Før du opretter orlovs- og fraværsplaner i Dynamics 365 Human Resources, er det en god ide at kontrollere indstillingerne for alle relaterede personaleparametre, herunder:</span><span class="sxs-lookup"><span data-stu-id="7eaca-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="7eaca-105">Nummerserie for orlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="7eaca-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="7eaca-106">FMLA-indstillinger (Family Medical and Leave Act)</span><span class="sxs-lookup"><span data-stu-id="7eaca-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="7eaca-107">Indstillinger for medarbejderselvbetjening for anmodninger om orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="7eaca-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="7eaca-108">Parametre for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="7eaca-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="7eaca-109">Få vist og skift personaleparametre</span><span class="sxs-lookup"><span data-stu-id="7eaca-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="7eaca-110">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="7eaca-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7eaca-111">Vælg **Human Resourcesparametre** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="7eaca-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="7eaca-112">Under fanen **Nummerserier** skal du kontrollere **Nummerseriekode** for **Orlovsanmodnings-id** og ændre den efter behov.</span><span class="sxs-lookup"><span data-stu-id="7eaca-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="7eaca-113">Denne indstilling bestemmer den rækkefølge, der bruges til automatisk tildeling af id'er til orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="7eaca-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="7eaca-114">Under fanen **FMLA** skal du kontrollere FMLA-indstillingerne og ændre dem efter behov.</span><span class="sxs-lookup"><span data-stu-id="7eaca-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="7eaca-115">Under fanen **Medarbejderselvbetjening** skal du angive, om ledere kan angive orlovs- og fraværsanmodninger på vegne af deres medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="7eaca-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="7eaca-116">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7eaca-116">Select **Save**.</span></span>

>[!IMPORTANT]
><span data-ttu-id="7eaca-117">Visning af orlov og fravær på tværs af firmaer er i øjeblikket i prøveversion.</span><span class="sxs-lookup"><span data-stu-id="7eaca-117">Viewing leave and absence across companies is currently in preview.</span></span> <span data-ttu-id="7eaca-118">Du skal aktivere det i dit **Sandkasse**-miljøet for at få vist indstillingen for orlov og fravær.</span><span class="sxs-lookup"><span data-stu-id="7eaca-118">You'll need to enable it in your **Sandbox** environment to display the option for leave and absence.</span></span> <span data-ttu-id="7eaca-119">Du kan finde flere oplysninger om aktivering af prøveversionsfunktioner i [Administrere funktioner](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="7eaca-119">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="view-and-change-human-resources-shared-parameters"></a><span data-ttu-id="7eaca-120">Få vist og skift delte parametre for personale</span><span class="sxs-lookup"><span data-stu-id="7eaca-120">View and change Human resources shared parameters</span></span>

1. <span data-ttu-id="7eaca-121">Vælg fanen **Links** på siden **Personalestyring**.</span><span class="sxs-lookup"><span data-stu-id="7eaca-121">On the **Personnel management** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7eaca-122">Vælg **Delte parametre for personale** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="7eaca-122">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="7eaca-123">Vælg **Ja** under fanen **Forhåndsadgang** i **Visning af orlov på tværs af firmaet**, hvis du vil have, at orlov skal vises på tværs af firmaet.</span><span class="sxs-lookup"><span data-stu-id="7eaca-123">On the **Advance access** tab, select **Yes** for **Enable cross company leave view** to allow leave to be viewed across company.</span></span>

4. <span data-ttu-id="7eaca-124">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7eaca-124">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="7eaca-125">Få vist og ændre parametre for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="7eaca-125">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="7eaca-126">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="7eaca-126">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7eaca-127">Vælg **Parametre for orlov og fravær** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="7eaca-127">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="7eaca-128">På fanen **Generelt** kan du angive følgende parametre:</span><span class="sxs-lookup"><span data-stu-id="7eaca-128">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="7eaca-129">Angiv **Enhed for orlov og fravær** til timer eller dage.</span><span class="sxs-lookup"><span data-stu-id="7eaca-129">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="7eaca-130">Hvis du angiver dage, kan du vælge **Aktiver halv-dags definition**, så medarbejderne kan vælge første eller anden halvdel af dagen i deres anmodninger om fritid.</span><span class="sxs-lookup"><span data-stu-id="7eaca-130">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="7eaca-131">Vælg **Ikrafttrædelsesdato for måneders tjeneste** for at indstille, hvornår periodiseringssatserne træder i kraft for orlovsplaner vha. måneders tjeneste.</span><span class="sxs-lookup"><span data-stu-id="7eaca-131">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="7eaca-132">Vælg **Saldoberegning** for at få vist saldi pr. dags dato eller pr. periodiseringsperiode.</span><span class="sxs-lookup"><span data-stu-id="7eaca-132">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="7eaca-133">Hvis du vælger **Saldo pr. dags dato**, viser saldoen totalen for alle periodiseringer, justeringer og anmodninger pr. i dag.</span><span class="sxs-lookup"><span data-stu-id="7eaca-133">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="7eaca-134">Hvis du vælger **Saldo pr. periodiseringsperiode**, viser saldoen totalen for alle periodiseringer, reguleringer og anmodninger pr. den periodiseringsperiode, der er defineret af frekvensen i orlovsplanen.</span><span class="sxs-lookup"><span data-stu-id="7eaca-134">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="7eaca-135">Angiv starttidspunktet for at overføre udløb af batchjob.</span><span class="sxs-lookup"><span data-stu-id="7eaca-135">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="7eaca-136">Vælg **Ja** for **Tillad medarbejderne at købe orlov** og **Tillad medarbejderne at sælge orlov**.</span><span class="sxs-lookup"><span data-stu-id="7eaca-136">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="7eaca-137">Hvis du vælger **Ja** for disse indstillinger, kan du oprette politikker for køb og salg af orlov og give medarbejdere mulighed for at sende anmodninger om køb og salg af orlov.</span><span class="sxs-lookup"><span data-stu-id="7eaca-137">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="7eaca-138">Konfigurere kalenderparametre</span><span class="sxs-lookup"><span data-stu-id="7eaca-138">Configure calendar parameters</span></span>

1. <span data-ttu-id="7eaca-139">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="7eaca-139">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7eaca-140">Vælg **Parametre for orlov og fravær** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="7eaca-140">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="7eaca-141">Under fanen **Kalender** skal du ændre kalenderindstillingerne efter behov.</span><span class="sxs-lookup"><span data-stu-id="7eaca-141">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="7eaca-142">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7eaca-142">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="7eaca-143">Se også</span><span class="sxs-lookup"><span data-stu-id="7eaca-143">See also</span></span>

- [<span data-ttu-id="7eaca-144">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="7eaca-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
