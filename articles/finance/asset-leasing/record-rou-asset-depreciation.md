---
title: Registrere afskrivning af brugsretsaktiver (prøveversion)
description: I dette emne forklares det, hvordan du opretter kladdeposteringen til den amortisering, der kræves til rettigheder, som genkendes i en organisationsbalance.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0dd8308acb875affc96ca6d9ed856d74d4b2eb37
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441752"
---
# <a name="record-right-of-use-asset-depreciation-preview"></a><span data-ttu-id="c4c43-103">Registrere afskrivning af brugsretsaktiver (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="c4c43-103">Record right-of-use asset depreciation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4c43-104">For rettigheder, der anerkendes i en organisationsbalance, amortiseres ROU-aktivet på månedsbasis.</span><span class="sxs-lookup"><span data-stu-id="c4c43-104">For leases that are recognized on an organization's balance sheet, the right-of-use (ROU) asset is amortized on a monthly basis.</span></span> <span data-ttu-id="c4c43-105">Dette emne forklarer, hvordan du opretter kladdeposteringen til amortiseringen.</span><span class="sxs-lookup"><span data-stu-id="c4c43-105">This topic explains how to create the journal entry for the amortization.</span></span> <span data-ttu-id="c4c43-106">Amortisering debiterer udgiftsfinanskontoen og krediterer finanskontoen for den akkumulerede afskrivning ud fra opsætningen af posteringsprofilen og leasingaftaletypen.</span><span class="sxs-lookup"><span data-stu-id="c4c43-106">The amortization debits the expense ledger account and credits the accumulated depreciation ledger account, based on the setup of your posting profile and the lease type.</span></span> <span data-ttu-id="c4c43-107">Disse poster kan oprettes for hver leasingaftale, eller de kan oprettes til flere leasingaftaler ved hjælp af batchkladdefunktionen.</span><span class="sxs-lookup"><span data-stu-id="c4c43-107">These entries can be created for each lease, or they can be created for multiple leases by using the batch journal functionality.</span></span>

## <a name="asset-depreciation-schedule"></a><span data-ttu-id="c4c43-108">Afskrivningstidsplan for aktiv</span><span class="sxs-lookup"><span data-stu-id="c4c43-108">Asset depreciation schedule</span></span>

1. <span data-ttu-id="c4c43-109">Vælg en leasingaftale på siden **Leasingoversigt**.</span><span class="sxs-lookup"><span data-stu-id="c4c43-109">On the **Lease summary** page, select a lease.</span></span> <span data-ttu-id="c4c43-110">Vælg derefter **Kartotek \> planlægning af afskrivningsplan** for at åbne siden **Aktivafskrivningsplan**.</span><span class="sxs-lookup"><span data-stu-id="c4c43-110">Then select **Books \> Asset depreciation schedule** to open the **Asset depreciation schedule** page.</span></span>

    <span data-ttu-id="c4c43-111">Kladdeposten til ROU for aktivafskrivning er baseret på beløbet i kolonnen **Afskrivningsudgifter**.</span><span class="sxs-lookup"><span data-stu-id="c4c43-111">The ROU asset depreciation expense journal entry is based on the amount in the **Depreciation Expense** column.</span></span> <span data-ttu-id="c4c43-112">Du kan se et eksempel på retningslinjerne for kontering af standardoverholdelse under [Beregning af ROU for afskrivning af aktiver for finansieringsleasingaftaler](#calculation-of-rou-asset-amortization-expense-for-finance-leases) senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="c4c43-112">For an example of the guidance for accounting standard compliance, see the [Calculation of ROU asset amortization expense for finance leases](#calculation-of-rou-asset-amortization-expense-for-finance-leases) section later in this topic.</span></span>

2. <span data-ttu-id="c4c43-113">Vælg afskrivningsperioden, og vælg derefter **Opret kladde**.</span><span class="sxs-lookup"><span data-stu-id="c4c43-113">Select the period of depreciation, and then select **Create journal**.</span></span> <span data-ttu-id="c4c43-114">Du får vist en meddelelse, hvor det angives, at den kladde, der skal bruges til registrering af afskrivningen, blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="c4c43-114">You receive a message that states that the journal that will be used to record depreciation was created.</span></span>
3. <span data-ttu-id="c4c43-115">Vælg **Kladder \> Aktivleasingkladder** for at åbne siden **Aktivleasingkladde**, hvor du kan få vist den kladdepost for afskrivning, der er oprettet.</span><span class="sxs-lookup"><span data-stu-id="c4c43-115">Select **Journals \> Asset leasing journals** to open the **Asset leasing journal** page, where you can view the depreciation expense journal entry that was created.</span></span>
4. <span data-ttu-id="c4c43-116">Vælg kladdeposteringen, og vælg derefter **Bogfør** for at registrere afskrivningsposten i Finans.</span><span class="sxs-lookup"><span data-stu-id="c4c43-116">Select the journal entry, and then select **Post** to record the depreciation entry to General ledger.</span></span>

## <a name="calculation-of-rou-asset-amortization-expense-for-operating-leases"></a><span data-ttu-id="c4c43-117">Beregning af ROU-aktiver for driftsleasingaftaler</span><span class="sxs-lookup"><span data-stu-id="c4c43-117">Calculation of ROU asset amortization expense for operating leases</span></span>

<span data-ttu-id="c4c43-118">Afskrivningsudgifterne for en driftsleasingaftale beregnes som forskellen mellem den månedlige lineære leasingudgift og de månedlige renteudgifter i forbindelse med leasingpassiver i overensstemmelse med regnskabsstandarderne Codification Topic 842 (ASC 842), som er standarden i almindeligt anerkendte regnskabsprincipper i USA (US GAAP).</span><span class="sxs-lookup"><span data-stu-id="c4c43-118">The depreciation expense of an operating lease is calculated as the difference between the monthly straight-line lease expense and the monthly interest expense on the lease liability, in accordance with Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP).</span></span> <span data-ttu-id="c4c43-119">Den lineære leasingomkostning beregnes som summen af alle leasingbetalinger divideret med leasingperioden i måneder.</span><span class="sxs-lookup"><span data-stu-id="c4c43-119">The straight-line lease expense is calculated as the sum of all lease payments divided by the lease term in months.</span></span> <span data-ttu-id="c4c43-120">(Summen af leasingbetalinger omfatter eventuelle forudbetalinger, indledende direkte omkostninger, afmonteringsomkostninger og incitamenter.) I følgende tabel vises et eksempel på en driftsleasingaftale, der indeholder et eksempler på amortiseringsudgifterne.</span><span class="sxs-lookup"><span data-stu-id="c4c43-120">(The sum of lease payments includes any prepayments, initial direct costs, dismantling costs, and lease incentives.) The following table shows an example of the amortization expense for an operating lease.</span></span>

### <a name="example-of-rou-asset-amortization-expense-for-operating-leases"></a><span data-ttu-id="c4c43-121">Eksempel på ROU-aktiver for driftsleasingaftaler</span><span class="sxs-lookup"><span data-stu-id="c4c43-121">Example of ROU asset amortization expense for operating leases</span></span>

| <span data-ttu-id="c4c43-122">Felt</span><span class="sxs-lookup"><span data-stu-id="c4c43-122">Field</span></span>                                          | <span data-ttu-id="c4c43-123">Værdi</span><span class="sxs-lookup"><span data-stu-id="c4c43-123">Value</span></span>       |
|------------------------------------------------|-------------|
| <span data-ttu-id="c4c43-124">Betalingsbeløb</span><span class="sxs-lookup"><span data-stu-id="c4c43-124">Payment amount</span></span>                                 | <span data-ttu-id="c4c43-125">1.000</span><span class="sxs-lookup"><span data-stu-id="c4c43-125">1,000</span></span>       |
| <span data-ttu-id="c4c43-126">Betalingshyppighed</span><span class="sxs-lookup"><span data-stu-id="c4c43-126">Payment frequency</span></span>                              | <span data-ttu-id="c4c43-127">Månedligt</span><span class="sxs-lookup"><span data-stu-id="c4c43-127">Monthly</span></span>     |
| <span data-ttu-id="c4c43-128">Leasingperiode (måneder)</span><span class="sxs-lookup"><span data-stu-id="c4c43-128">Lease term (months)</span></span>                            | <span data-ttu-id="c4c43-129">24</span><span class="sxs-lookup"><span data-stu-id="c4c43-129">24</span></span>          |
| <span data-ttu-id="c4c43-130">Samlede leasingbetalinger</span><span class="sxs-lookup"><span data-stu-id="c4c43-130">Total lease payments</span></span>                           | <span data-ttu-id="c4c43-131">24,000</span><span class="sxs-lookup"><span data-stu-id="c4c43-131">24,000</span></span>      |
| <span data-ttu-id="c4c43-132">Trinvis lånesats</span><span class="sxs-lookup"><span data-stu-id="c4c43-132">Incremental borrowing rate</span></span>                     | <span data-ttu-id="c4c43-133">5 %</span><span class="sxs-lookup"><span data-stu-id="c4c43-133">5%</span></span>          |
| <span data-ttu-id="c4c43-134">Annuitetstype</span><span class="sxs-lookup"><span data-stu-id="c4c43-134">Annuity type</span></span>                                   | <span data-ttu-id="c4c43-135">Forfalden annuitet</span><span class="sxs-lookup"><span data-stu-id="c4c43-135">Annuity due</span></span> |
| <span data-ttu-id="c4c43-136">Sammensætningsinterval</span><span class="sxs-lookup"><span data-stu-id="c4c43-136">Compounding Interval</span></span>                           | <span data-ttu-id="c4c43-137">Månedligt</span><span class="sxs-lookup"><span data-stu-id="c4c43-137">Monthly</span></span>     |
| <span data-ttu-id="c4c43-138">Nutidsværdi af fremtidige minimumsleasingbetalinger</span><span class="sxs-lookup"><span data-stu-id="c4c43-138">Present value of future minimum lease payments</span></span> | <span data-ttu-id="c4c43-139">22,888.87</span><span class="sxs-lookup"><span data-stu-id="c4c43-139">22,888.87</span></span>   |

<span data-ttu-id="c4c43-140">Som tidligere nævnt beregnes lineære leasingomkostninger som summen af alle leasingbetalinger divideret med leasingperioden.</span><span class="sxs-lookup"><span data-stu-id="c4c43-140">As was previously mentioned, the straight-line lease expense is calculated as the sum of all payments divided by the lease term.</span></span> <span data-ttu-id="c4c43-141">De månedlige renteudgifter beregnes automatisk på basis af planlægningen af passivafskrivning.</span><span class="sxs-lookup"><span data-stu-id="c4c43-141">The system automatically calculates the monthly interest expense on the liability amortization schedule.</span></span> <span data-ttu-id="c4c43-142">Renteudgiften beregnes ved hjælp af metoden faktisk rentesats.</span><span class="sxs-lookup"><span data-stu-id="c4c43-142">The interest expense is calculated by using the effective interest rate method.</span></span> <span data-ttu-id="c4c43-143">Systemet vil bruge den lineære leasingomkostning til at trække renteudgiften fra for hver måned.</span><span class="sxs-lookup"><span data-stu-id="c4c43-143">The system will use the straight-line lease cost to subtract the interest expense for each month.</span></span> <span data-ttu-id="c4c43-144">Værdien bruges til at reducere ROU-aktivet.</span><span class="sxs-lookup"><span data-stu-id="c4c43-144">The value is used to reduce the ROU asset.</span></span>

| <span data-ttu-id="c4c43-145">Måned</span><span class="sxs-lookup"><span data-stu-id="c4c43-145">Month</span></span> | <span data-ttu-id="c4c43-146">Lineær leasingomkostninger</span><span class="sxs-lookup"><span data-stu-id="c4c43-146">Straight-line lease cost</span></span> | <span data-ttu-id="c4c43-147">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="c4c43-147">Interest expense</span></span>                        | <span data-ttu-id="c4c43-148">Beregning af udgifter til afskrivning af ROU-aktiver</span><span class="sxs-lookup"><span data-stu-id="c4c43-148">Calculation of ROU asset amortization expense</span></span> |
|-------|--------------------------|-----------------------------------------|-----------------------------------------------|
| <span data-ttu-id="c4c43-149">1</span><span class="sxs-lookup"><span data-stu-id="c4c43-149">1</span></span>     | <span data-ttu-id="c4c43-150">(24.000 ÷ 24) = 1.000,00</span><span class="sxs-lookup"><span data-stu-id="c4c43-150">(24,000 ÷ 24) = 1,000.00</span></span> | <span data-ttu-id="c4c43-151">(22.888.87 – 1.000) × (5 % ÷ 12) = 91,20</span><span class="sxs-lookup"><span data-stu-id="c4c43-151">(22,888.87 – 1,000) × (5% ÷ 12) = 91.20</span></span> | <span data-ttu-id="c4c43-152">1.000 – 91,20 = 908,80</span><span class="sxs-lookup"><span data-stu-id="c4c43-152">1,000 – 91.20 = 908.80</span></span>                        |
| <span data-ttu-id="c4c43-153">2</span><span class="sxs-lookup"><span data-stu-id="c4c43-153">2</span></span>     | <span data-ttu-id="c4c43-154">(24.000 ÷ 24) = 1.000,00</span><span class="sxs-lookup"><span data-stu-id="c4c43-154">(24,000 ÷ 24) = 1,000.00</span></span> | <span data-ttu-id="c4c43-155">(21.980,08 – 1.000) × (5 % ÷ 12) = 87,42</span><span class="sxs-lookup"><span data-stu-id="c4c43-155">(21,980.08 – 1,000) × (5% ÷ 12) = 87.42</span></span> | <span data-ttu-id="c4c43-156">1.000 – 87,42 = 912,58</span><span class="sxs-lookup"><span data-stu-id="c4c43-156">1,000 – 87.42 = 912.58</span></span>                        |
| <span data-ttu-id="c4c43-157">3</span><span class="sxs-lookup"><span data-stu-id="c4c43-157">3</span></span>     | <span data-ttu-id="c4c43-158">(24.000 ÷ 24) = 1.000,00</span><span class="sxs-lookup"><span data-stu-id="c4c43-158">(24,000 ÷ 24) = 1,000.00</span></span> | <span data-ttu-id="c4c43-159">(21.067,49 – 1.000) × (5 % ÷ 12) = 83,62</span><span class="sxs-lookup"><span data-stu-id="c4c43-159">(21,067.49 – 1,000) × (5% ÷ 12) = 83.62</span></span> | <span data-ttu-id="c4c43-160">1.000 – 83,62 = 916,39</span><span class="sxs-lookup"><span data-stu-id="c4c43-160">1,000 – 83.62 = 916.39</span></span>                        |

> [!NOTE]
> <span data-ttu-id="c4c43-161">Ifølge ASC 842 klassificeres afskrivningen af ROU-aktivet for en driftsleasingaftale som en leasingomkostning på resultatopgørelsen.</span><span class="sxs-lookup"><span data-stu-id="c4c43-161">According to ASC 842, the depreciation of the ROU asset for an operating lease is classified as a lease expense on the income statement.</span></span> <span data-ttu-id="c4c43-162">For synlighed beskriver aktivleasing posten som afskrivningen af ROU-aktivet.</span><span class="sxs-lookup"><span data-stu-id="c4c43-162">For visibility, Asset leasing describes the entry as the depreciation of the ROU asset.</span></span> <span data-ttu-id="c4c43-163">Debetposten skal dog tildeles en konto til driftsleasing, og kreditposten skal tildeles direkte til ROU-aktivet for driftsleasing.</span><span class="sxs-lookup"><span data-stu-id="c4c43-163">However, the debit entry should be assigned to an operating lease expense account, and the credit entry should be assigned directly to the ROU asset for the operating lease.</span></span> <span data-ttu-id="c4c43-164">Men i leasingparametrene kan du angive, at kreditposter skal oprettes til en akkumuleret afskrivningskonto for drifts ROU-aktiver.</span><span class="sxs-lookup"><span data-stu-id="c4c43-164">Nevertheless, in the lease parameters, you can specify that credit entries should be made to an accumulated depreciation account for operating ROU assets.</span></span>

## <a name="calculation-of-rou-asset-amortization-expense-for-finance-leases"></a><span data-ttu-id="c4c43-165">Beregning af ROU-aktiver for finansiel leasing</span><span class="sxs-lookup"><span data-stu-id="c4c43-165">Calculation of ROU asset amortization expense for finance leases</span></span>

<span data-ttu-id="c4c43-166">For leasingaftaler, der har en finansieringsklassifikation, beregner systemet anlægsaktivets amortisering på et lineært grundlag.</span><span class="sxs-lookup"><span data-stu-id="c4c43-166">For leases that have a finance classification, the system calculates the ROU asset amortization on a straight-line basis.</span></span> <span data-ttu-id="c4c43-167">Derfor vil afskrivningsudgiften være ens for hver måned.</span><span class="sxs-lookup"><span data-stu-id="c4c43-167">Therefore, the depreciation expense will be the same for each month.</span></span>

<span data-ttu-id="c4c43-168">I overensstemmelse med International Financial Reporting Standard 16 (IFRS 16) og ASC 842 vil aktivet blive amortiseret i enten leasingperioden eller aktivets levetid, afhængigt af hvad der er mindre.</span><span class="sxs-lookup"><span data-stu-id="c4c43-168">In accordance with International Financial Reporting Standard 16 (IFRS 16) and ASC 842, the asset will be amortized over either the lease term or the asset's useful life, whichever is less.</span></span> <span data-ttu-id="c4c43-169">Hvis parameteren **Overdragelsen af ejerskab** også er slået til for leasingaftalen, vil leasingaftalen automatisk blive afskrevet over aktivets levetid.</span><span class="sxs-lookup"><span data-stu-id="c4c43-169">Additionally, if the **Transfer of ownership** parameter is turned on for the lease, the lease will automatically be depreciated over the asset's useful life.</span></span>

### <a name="example-of-rou-asset-amortization-expense-for-finance-leases"></a><span data-ttu-id="c4c43-170">Eksempel på ROU-aktiver for finansielle leasingaftaler</span><span class="sxs-lookup"><span data-stu-id="c4c43-170">Example of ROU asset amortization expense for finance leases</span></span>

| <span data-ttu-id="c4c43-171">Felt</span><span class="sxs-lookup"><span data-stu-id="c4c43-171">Field</span></span>                                | <span data-ttu-id="c4c43-172">Værdi</span><span class="sxs-lookup"><span data-stu-id="c4c43-172">Value</span></span>                                   |
|--------------------------------------|-----------------------------------------|
| <span data-ttu-id="c4c43-173">Startsaldo for brugsretsaktiver</span><span class="sxs-lookup"><span data-stu-id="c4c43-173">Beginning right-of-use asset balance</span></span> | <span data-ttu-id="c4c43-174">22,889.87</span><span class="sxs-lookup"><span data-stu-id="c4c43-174">22,889.87</span></span>                               |
| <span data-ttu-id="c4c43-175">Leasingperiode (måneder)</span><span class="sxs-lookup"><span data-stu-id="c4c43-175">Lease term (months)</span></span>                  | <span data-ttu-id="c4c43-176">24</span><span class="sxs-lookup"><span data-stu-id="c4c43-176">24</span></span>                                      |
| <span data-ttu-id="c4c43-177">Brugstid for aktiv (måneder)</span><span class="sxs-lookup"><span data-stu-id="c4c43-177">Asset useful life (months)</span></span>           | <span data-ttu-id="c4c43-178">36</span><span class="sxs-lookup"><span data-stu-id="c4c43-178">36</span></span>                                      |
| <span data-ttu-id="c4c43-179">Måned</span><span class="sxs-lookup"><span data-stu-id="c4c43-179">Month</span></span>                                | <span data-ttu-id="c4c43-180">Afskrivning af brugsretsaktiver</span><span class="sxs-lookup"><span data-stu-id="c4c43-180">Right-of-use asset amortization expense</span></span> |
| <span data-ttu-id="c4c43-181">1</span><span class="sxs-lookup"><span data-stu-id="c4c43-181">1</span></span>                                    | <span data-ttu-id="c4c43-182">22.889,87 ÷ 24 = 953,74</span><span class="sxs-lookup"><span data-stu-id="c4c43-182">22,889.87 ÷ 24 = 953.74</span></span>                 |
| <span data-ttu-id="c4c43-183">2</span><span class="sxs-lookup"><span data-stu-id="c4c43-183">2</span></span>                                    | <span data-ttu-id="c4c43-184">22.889,87 ÷ 24 = 953,74</span><span class="sxs-lookup"><span data-stu-id="c4c43-184">22,889.87 ÷ 24 = 953.74</span></span>                 |
| <span data-ttu-id="c4c43-185">3</span><span class="sxs-lookup"><span data-stu-id="c4c43-185">3</span></span>                                    | <span data-ttu-id="c4c43-186">22.889,87 ÷ 24 = 953,74</span><span class="sxs-lookup"><span data-stu-id="c4c43-186">22,889.87 ÷ 24 = 953.74</span></span>                 |