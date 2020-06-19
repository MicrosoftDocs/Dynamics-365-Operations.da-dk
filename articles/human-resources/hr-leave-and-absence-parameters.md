---
title: Konfigurere parametre for orlov og fravær
description: Definer personaleparametre for orlov og fravær i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
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
ms.openlocfilehash: 5e4d3b3e4b373631bed5e2d7e3c3a4e14f0c5c98
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428938"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="91dd6-103">Konfigurere parametre for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="91dd6-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="91dd6-104">Før du opretter orlovs- og fraværsplaner i Dynamics 365 Human Resources, er det en god ide at kontrollere indstillingerne for alle relaterede personaleparametre, herunder:</span><span class="sxs-lookup"><span data-stu-id="91dd6-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="91dd6-105">Nummerserie for orlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="91dd6-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="91dd6-106">FMLA-indstillinger (Family Medical and Leave Act)</span><span class="sxs-lookup"><span data-stu-id="91dd6-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="91dd6-107">Indstillinger for medarbejderselvbetjening for anmodninger om orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="91dd6-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="91dd6-108">Parametre for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="91dd6-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="91dd6-109">Få vist og skift personaleparametre</span><span class="sxs-lookup"><span data-stu-id="91dd6-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="91dd6-110">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="91dd6-111">Vælg **Personaleparametre** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="91dd6-112">Under fanen **Nummerserier** skal du kontrollere **Nummerseriekode** for **Orlovsanmodnings-id** og ændre den efter behov.</span><span class="sxs-lookup"><span data-stu-id="91dd6-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="91dd6-113">Denne indstilling bestemmer den rækkefølge, der bruges til automatisk tildeling af id'er til orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="91dd6-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="91dd6-114">Under fanen **FMLA** skal du kontrollere FMLA-indstillingerne og ændre dem efter behov.</span><span class="sxs-lookup"><span data-stu-id="91dd6-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="91dd6-115">Under fanen **Medarbejderselvbetjening** skal du angive, om ledere kan angive orlovs- og fraværsanmodninger på vegne af deres medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="91dd6-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="91dd6-116">Under fanen **Orlov og fravær** skal du kontrollere FMLA-indstillingerne og ændre dem efter behov.</span><span class="sxs-lookup"><span data-stu-id="91dd6-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="91dd6-117">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-117">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="91dd6-118">Få vist og ændre parametre for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="91dd6-118">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="91dd6-119">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-119">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="91dd6-120">Vælg **Parametre for orlov og fravær** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-120">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="91dd6-121">På fanen **Generelt** kan du angive følgende parametre:</span><span class="sxs-lookup"><span data-stu-id="91dd6-121">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="91dd6-122">Angiv **Enhed for orlov og fravær** til timer eller dage.</span><span class="sxs-lookup"><span data-stu-id="91dd6-122">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="91dd6-123">Hvis du angiver dage, kan du vælge **Aktiver halv-dags definition**, så medarbejderne kan vælge første eller anden halvdel af dagen i deres anmodninger om fritid.</span><span class="sxs-lookup"><span data-stu-id="91dd6-123">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="91dd6-124">Vælg **Ikrafttrædelsesdato for måneders tjeneste** for at indstille, hvornår periodiseringssatserne træder i kraft for orlovsplaner vha. måneders tjeneste.</span><span class="sxs-lookup"><span data-stu-id="91dd6-124">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="91dd6-125">Vælg **Saldoberegning** for at få vist saldi pr. dags dato eller pr. periodiseringsperiode.</span><span class="sxs-lookup"><span data-stu-id="91dd6-125">Select **Balance calculation** to display balances display as of today or as of the accrual period.</span></span> <span data-ttu-id="91dd6-126">Hvis du vælger **Saldo pr. dags dato**, viser saldoen totalen for alle periodiseringer, justeringer og anmodninger pr. i dag.</span><span class="sxs-lookup"><span data-stu-id="91dd6-126">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="91dd6-127">Hvis du vælger **Saldo pr. periodiseringsperiode**, viser saldoen totalen for alle periodiseringer, reguleringer og anmodninger pr. den periodiseringsperiode, der er defineret af frekvensen i orlovsplanen.</span><span class="sxs-lookup"><span data-stu-id="91dd6-127">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

## <a name="configure-calendar-parameters"></a><span data-ttu-id="91dd6-128">Konfigurere kalenderparametre</span><span class="sxs-lookup"><span data-stu-id="91dd6-128">Configure calendar parameters</span></span>

1. <span data-ttu-id="91dd6-129">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-129">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="91dd6-130">Vælg **Parametre for orlov og fravær** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-130">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="91dd6-131">Under fanen **Kalender** skal du ændre kalenderindstillingerne efter behov.</span><span class="sxs-lookup"><span data-stu-id="91dd6-131">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="91dd6-132">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="91dd6-132">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="91dd6-133">Se også</span><span class="sxs-lookup"><span data-stu-id="91dd6-133">See also</span></span>

- [<span data-ttu-id="91dd6-134">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="91dd6-134">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
