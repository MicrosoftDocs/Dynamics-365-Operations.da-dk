---
title: Bekræft udgående forsendelser fra batchjob
description: Dette emne beskriver, hvordan du opretter et batchjob, der automatisk bekræfter udgående overførselsordre forsendelser, der er til klar til afsendelse.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 41dbfb90b7b19c964e725ee0a4c769402414fb17
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424393"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="790a0-103">Bekræft udgående forsendelser fra batchjob</span><span class="sxs-lookup"><span data-stu-id="790a0-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="790a0-104">Dette emne beskriver, hvordan du opretter et batchjob, der automatisk bekræfter udgående overførselsordre forsendelser, der er til klar til afsendelse.</span><span class="sxs-lookup"><span data-stu-id="790a0-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="790a0-105">Det batchjob, der er beskrevet her, gælder kun for flytteordreforsendelser, ikke for salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="790a0-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="790a0-106">Aktivere funktionen Bekræft udgående forsendelser fra batchjob</span><span class="sxs-lookup"><span data-stu-id="790a0-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="790a0-107">Før du kan bruge denne funktion, skal den aktiveres i dit system.</span><span class="sxs-lookup"><span data-stu-id="790a0-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="790a0-108">Administratorer kan bruge siden [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionsstatus og aktivere den, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="790a0-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="790a0-109">Funktionen er angivet som:</span><span class="sxs-lookup"><span data-stu-id="790a0-109">The feature is listed as:</span></span>

- <span data-ttu-id="790a0-110">**Modul** - *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="790a0-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="790a0-111">**Funktionsnavn** - *Bekræft udgående forsendelser fra batchjob*</span><span class="sxs-lookup"><span data-stu-id="790a0-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="790a0-112">Udfør behandling af udgående forsendelser</span><span class="sxs-lookup"><span data-stu-id="790a0-112">Process outbound shipments</span></span>

<span data-ttu-id="790a0-113">Sådan konfigureres et planlagt batchjob til at køre bekræftelse af udgående forsendelse for belastninger, der er klar til afsendelse:</span><span class="sxs-lookup"><span data-stu-id="790a0-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="790a0-114">Gå til **Lokationsstyring \> Periodiske opgaver \> Behandle udgående forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="790a0-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="790a0-115">Dialogboksen **Bekræft forsendelse** åbnes.</span><span class="sxs-lookup"><span data-stu-id="790a0-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="790a0-116">I oversigtspanelet **Medtagne poster** skal du vælge **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="790a0-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="790a0-117">Dialogboksen for forespørgselseditoren åbnes.</span><span class="sxs-lookup"><span data-stu-id="790a0-117">The query editor dialog box opens.</span></span> <span data-ttu-id="790a0-118">Gå til fanen **Område**, og tilføj en række med følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="790a0-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="790a0-119">**Tabel** - *Laster*</span><span class="sxs-lookup"><span data-stu-id="790a0-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="790a0-120">**Afledt tabel** - *Laster*</span><span class="sxs-lookup"><span data-stu-id="790a0-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="790a0-121">**Felt** - *Laststatus*</span><span class="sxs-lookup"><span data-stu-id="790a0-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="790a0-122">**Kriterier** - *Lastet*</span><span class="sxs-lookup"><span data-stu-id="790a0-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="790a0-123">Vælg **OK** for at vende tilbage til dialogboksen **Bekræft forsendelse**.</span><span class="sxs-lookup"><span data-stu-id="790a0-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="790a0-124">Angiv **Batchbehandling** til **Ja** i oversigtspanelet **Kør i baggrunden**.</span><span class="sxs-lookup"><span data-stu-id="790a0-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="790a0-125">Vælg **Gentagelse** i oversigtspanelet **Kør i baggrunden**.</span><span class="sxs-lookup"><span data-stu-id="790a0-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="790a0-126">Dialogboksen **Definer gentagelse** åbnes.</span><span class="sxs-lookup"><span data-stu-id="790a0-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="790a0-127">Angiv kørselsplanen efter behov for din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="790a0-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="790a0-128">Vælg **OK** for at vende tilbage til dialogboksen **Bekræft forsendelse**.</span><span class="sxs-lookup"><span data-stu-id="790a0-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="790a0-129">Vælg **OK** i dialogboksen **Bekræft forsendelse** for at føje batchjobbet til batchkøen.</span><span class="sxs-lookup"><span data-stu-id="790a0-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="790a0-130">Du kan finde flere oplysninger under [Oversigt over batchbehandling](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="790a0-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>
