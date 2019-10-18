---
title: Periodisering af projektomkostninger på købsleverancer
description: Dette emne beskriver, hvordan periodiserede projektomkostninger fra købsleverancer kan spores i Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9200b0e4bc3862abdb3ecacb6539f7ba0d619b2f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189608"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="d1bbd-103">Periodisering af projektomkostninger på købsleverancer</span><span class="sxs-lookup"><span data-stu-id="d1bbd-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1bbd-104">Dette emne beskriver, hvordan periodiserede projektomkostninger fra købsleverancer kan spores i Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 Finance.</span></span> 

<span data-ttu-id="d1bbd-105">Fakturaer for et projekt ankommer ofte senere end varerne og tjenesterne er leveret, og det kan have betydelig indvirkning på projektets nøgletal (KPI'er).</span><span class="sxs-lookup"><span data-stu-id="d1bbd-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="d1bbd-106">Det er vigtigt at være i stand til at spore disse transaktioner i både finansielle rapporter og projektrapporter.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="d1bbd-107">Følgende eksempelscenarie illustrerer dette.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="d1bbd-108">Contoso Consulting har startet et nyt projekt med skyinstallation.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="d1bbd-109">Der oprettes en indkøbsordre til køb af en computer til projektet.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="d1bbd-110">Computeren koster $1500, og installationsservices koster $150.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="d1bbd-111">Leverandøren har leveret og installeret på computeren, men fakturaen er endnu ikke har nået frem til Contoso Consulting.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="d1bbd-112">Projektlederen vil gerne se periodiserede projektomkostninger på $1650, før fakturaen er leveret.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="d1bbd-113">Denne omkostning skal også afspejles i virksomhedens regnskab ved månedsafslutningen.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="d1bbd-114">De påløbne omkostninger skal registreres både på økonomisk niveau og projektniveau til rapporteringsformål.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="d1bbd-115">Den økonomiske opdatering af produktkvitteringen kan spores for vare- og indkøbskategorierne.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-115">The financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="d1bbd-116">For varer skal du på siden **Kreditorparametre** vælge indstillingen **Bogfør produktkvittering i finans**.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="d1bbd-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="d1bbd-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="d1bbd-118">For indkøbskategorier skal du på siden **Kategoripolitikregel** vælge politikkerne **Indkøb** og derefter vælge **Periodiser indkøbsudgifter på kvittering** for hver indkøbskategori.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="d1bbd-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="d1bbd-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="d1bbd-120">Kontiene **Udgifter til indkøb, ikke-faktureret** og **Købsperiodisering** i **Opsætning af bogføring** bruges til bogføring af bilag, der er knyttet til produktkvitteringen.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>
<span data-ttu-id="d1bbd-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span><span class="sxs-lookup"><span data-stu-id="d1bbd-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span></span> 

<span data-ttu-id="d1bbd-122">Når vi bruger det samme scenarie, så lad os se, hvordan bogføring af en produktkvittering påvirker finans og projektoplysninger.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-122">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="d1bbd-123">**Trin 1:** Opret og Bekræft en ny indkøbsordre for projektet for at registrere købet af en computer til $1500 og installationsservices for $150.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-123">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="d1bbd-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="d1bbd-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="d1bbd-125">Når indkøbsordren er bekræftet, oprettes der posteringer for den bindende omkostning for projektet.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-125">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="d1bbd-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="d1bbd-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="d1bbd-127">Posteringerne for den bindende omkostning vil have feltet **Posteringsgrundlag** indstillet til **Indkøbsordre**.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-127">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="d1bbd-128">Oprettelse og bekræftelse af en indkøbsordre opretter ikke posteringer for et projekt.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-128">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="d1bbd-129">**Trin 2:** Varer og tjenesteydelser leveres, og en produktkvittering registreres.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-129">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="d1bbd-130">Bogføring af en produktkvittering genererer og bogfører et bilag til finans.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-130">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="d1bbd-131">Bilaget debiteres kontoen Udgifter til indkøb, ikke-faktureret og krediteres kontoen Periodisering af køb.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-131">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="d1bbd-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="d1bbd-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="d1bbd-133">Bogføring af en produktkvittering vil bruge posteringsopsætningen for indkøbskategorier og produkter og ikke posteringsopsætningen til projektkategorier.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-133">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="d1bbd-134">Denne opsætning skal justeres for korrekt at afspejle den økonomiske virkning af købsperiodiseringer.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-134">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="d1bbd-135">Det er muligt at knytte indkøbskategorier til projektkategorier på siden **Indkøbskategori**.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-135">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="d1bbd-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="d1bbd-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="d1bbd-137">**Trin 3:** Opret en kladdekreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-137">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="d1bbd-138">Bogføring af en produktkvittering påvirker ikke projektoplysninger.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-138">Posting a product receipt does not impact project information.</span></span> <span data-ttu-id="d1bbd-139">Som en løsning kan du generere en kladdekreditorfaktura lige efter bogføringen af købskvitteringen.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-139">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="d1bbd-140">Gå til siden **indkøbsordre** &gt; **fanen Faktura** &gt; **Generer** &gt; **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-140">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="d1bbd-141">Dette opretter et ventende fakturadokument, der opdaterer projektoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-141">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="d1bbd-142">Oprettelse af en kladdekreditorfaktura genererer ventende projektposteringer.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-142">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="d1bbd-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="d1bbd-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="d1bbd-144">På siden **Bindende omkostning** lukkes poster, der er oprettet i trin 1, og nye poster oprettes for at afspejle en omkostningsbinding, der kommer fra den ventende kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-144">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="d1bbd-145">Feltet **Posteringsgrundlag** for den bindende omkostning angives til **Kreditorfaktura**.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-145">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="d1bbd-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="d1bbd-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="d1bbd-147">Kreditorfakturaen forbliver i tilstanden Afventer, indtil den faktiske kreditorfaktura ankommer.</span><span class="sxs-lookup"><span data-stu-id="d1bbd-147">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>



