---
title: Konfigurere parametre for orlov og fravær
description: Definer personaleparametre for orlov og fravær i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
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
ms.openlocfilehash: 196c3901b5bc19f73b882bac7d3361e5bcc37e07
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712370"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="003d5-103">Konfigurere parametre for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="003d5-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="003d5-104">Før du opretter orlovs- og fraværsplaner i Dynamics 365 Human Resources, er det en god ide at kontrollere indstillingerne for alle relaterede personaleparametre, herunder:</span><span class="sxs-lookup"><span data-stu-id="003d5-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="003d5-105">Nummerserie for orlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="003d5-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="003d5-106">FMLA-indstillinger (Family Medical and Leave Act)</span><span class="sxs-lookup"><span data-stu-id="003d5-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="003d5-107">Indstillinger for medarbejderselvbetjening for anmodninger om orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="003d5-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="003d5-108">Parametre for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="003d5-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="003d5-109">Få vist og skift personaleparametre</span><span class="sxs-lookup"><span data-stu-id="003d5-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="003d5-110">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="003d5-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="003d5-111">Vælg **Personaleparametre** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="003d5-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="003d5-112">Under fanen **Nummerserier** skal du kontrollere **Nummerseriekode** for **Orlovsanmodnings-id** og ændre den efter behov.</span><span class="sxs-lookup"><span data-stu-id="003d5-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="003d5-113">Denne indstilling bestemmer den rækkefølge, der bruges til automatisk tildeling af id'er til orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="003d5-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="003d5-114">Under fanen **FMLA** skal du kontrollere FMLA-indstillingerne og ændre dem efter behov.</span><span class="sxs-lookup"><span data-stu-id="003d5-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="003d5-115">Under fanen **Medarbejderselvbetjening** skal du angive, om ledere kan angive orlovs- og fraværsanmodninger på vegne af deres medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="003d5-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="003d5-116">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="003d5-116">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="003d5-117">Få vist og ændre parametre for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="003d5-117">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="003d5-118">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="003d5-118">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="003d5-119">Vælg **Parametre for orlov og fravær** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="003d5-119">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="003d5-120">På fanen **Generelt** kan du angive følgende parametre:</span><span class="sxs-lookup"><span data-stu-id="003d5-120">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="003d5-121">Angiv **Enhed for orlov og fravær** til timer eller dage.</span><span class="sxs-lookup"><span data-stu-id="003d5-121">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="003d5-122">Hvis du angiver dage, kan du vælge **Aktiver halv-dags definition**, så medarbejderne kan vælge første eller anden halvdel af dagen i deres anmodninger om fritid.</span><span class="sxs-lookup"><span data-stu-id="003d5-122">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="003d5-123">Vælg **Ikrafttrædelsesdato for måneders tjeneste** for at indstille, hvornår periodiseringssatserne træder i kraft for orlovsplaner vha. måneders tjeneste.</span><span class="sxs-lookup"><span data-stu-id="003d5-123">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="003d5-124">Vælg **Saldoberegning** for at få vist saldi pr. dags dato eller pr. periodiseringsperiode.</span><span class="sxs-lookup"><span data-stu-id="003d5-124">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="003d5-125">Hvis du vælger **Saldo pr. dags dato**, viser saldoen totalen for alle periodiseringer, justeringer og anmodninger pr. i dag.</span><span class="sxs-lookup"><span data-stu-id="003d5-125">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="003d5-126">Hvis du vælger **Saldo pr. periodiseringsperiode**, viser saldoen totalen for alle periodiseringer, reguleringer og anmodninger pr. den periodiseringsperiode, der er defineret af frekvensen i orlovsplanen.</span><span class="sxs-lookup"><span data-stu-id="003d5-126">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="003d5-127">Angiv starttidspunktet for at overføre udløb af batchjob.</span><span class="sxs-lookup"><span data-stu-id="003d5-127">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="003d5-128">Vælg **Ja** for **Tillad medarbejderne at købe orlov** og **Tillad medarbejderne at sælge orlov**.</span><span class="sxs-lookup"><span data-stu-id="003d5-128">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="003d5-129">Hvis du vælger **Ja** for disse indstillinger, kan du oprette politikker for køb og salg af orlov og give medarbejdere mulighed for at sende anmodninger om køb og salg af orlov.</span><span class="sxs-lookup"><span data-stu-id="003d5-129">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="003d5-130">Konfigurere kalenderparametre</span><span class="sxs-lookup"><span data-stu-id="003d5-130">Configure calendar parameters</span></span>

1. <span data-ttu-id="003d5-131">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="003d5-131">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="003d5-132">Vælg **Parametre for orlov og fravær** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="003d5-132">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="003d5-133">Under fanen **Kalender** skal du ændre kalenderindstillingerne efter behov.</span><span class="sxs-lookup"><span data-stu-id="003d5-133">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="003d5-134">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="003d5-134">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="003d5-135">Se også</span><span class="sxs-lookup"><span data-stu-id="003d5-135">See also</span></span>

- [<span data-ttu-id="003d5-136">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="003d5-136">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
