---
title: Afhænd et anlægsaktiv som kasseret
description: Emnet indeholder en beskrivelse af, hvordan du eliminerer posteringer for et anlægsaktiv, der er blevet afhændet som kasseret.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 20f5fe0f8f2654df5027c363ebf5922f8344d928
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241116"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="72ecb-103">Afhænd et anlægsaktiv som kasseret</span><span class="sxs-lookup"><span data-stu-id="72ecb-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72ecb-104">Emnet indeholder en beskrivelse af, hvordan du eliminerer posteringer for et anlægsaktiv, der er blevet afhændet som kasseret.</span><span class="sxs-lookup"><span data-stu-id="72ecb-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="72ecb-105">De posteringstyper, der kan fjernes, omfatter et anlægs anskaffelse og akkumulerede afskrivningsposteringer og andre anlægsaktivposteringer.</span><span class="sxs-lookup"><span data-stu-id="72ecb-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="72ecb-106">Eliminering af disse posteringer påvirker statuskonti, f.eks. anskaffelsesregulering, regulering af afskrivning, værdiregulering, opskrivnings- og nedskrivningskonti.</span><span class="sxs-lookup"><span data-stu-id="72ecb-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="72ecb-107">Postering</span><span class="sxs-lookup"><span data-stu-id="72ecb-107">Transaction</span></span>                                         | <span data-ttu-id="72ecb-108">Debet (D.)</span><span class="sxs-lookup"><span data-stu-id="72ecb-108">Debit (Dr.)</span></span> | <span data-ttu-id="72ecb-109">Kredit (K.)</span><span class="sxs-lookup"><span data-stu-id="72ecb-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="72ecb-110">D. Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="72ecb-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="72ecb-111">X</span><span class="sxs-lookup"><span data-stu-id="72ecb-111">X</span></span>           |              |
| <span data-ttu-id="72ecb-112">K. Anlægsaktiver gevinst/tab</span><span class="sxs-lookup"><span data-stu-id="72ecb-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="72ecb-113">X</span><span class="sxs-lookup"><span data-stu-id="72ecb-113">X</span></span>            |
| <span data-ttu-id="72ecb-114">D. Anlægsaktiver gevinst/tab</span><span class="sxs-lookup"><span data-stu-id="72ecb-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="72ecb-115">X</span><span class="sxs-lookup"><span data-stu-id="72ecb-115">X</span></span>           |              |
| <span data-ttu-id="72ecb-116">K. Konto for anskaffelse af anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="72ecb-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="72ecb-117">X</span><span class="sxs-lookup"><span data-stu-id="72ecb-117">X</span></span>            |
| <span data-ttu-id="72ecb-118">D. Anlægsaktiver gevinst/tab (bogført nettoværdi \[BNV\])</span><span class="sxs-lookup"><span data-stu-id="72ecb-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="72ecb-119">X</span><span class="sxs-lookup"><span data-stu-id="72ecb-119">X</span></span>           |              |
| <span data-ttu-id="72ecb-120">K. Anlægsaktiver gevinst/tab (BNV)</span><span class="sxs-lookup"><span data-stu-id="72ecb-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="72ecb-121">X</span><span class="sxs-lookup"><span data-stu-id="72ecb-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="72ecb-122">Det anbefales, at du arbejder tæt sammen med firmaets regnskabsdirektør eller controller for at identificere de korrekte konti, der skal bruges til hver enkelt posteringstype, og til at kontrollere, at kassationsprocessen og de transaktioner, den genererer, opdaterer disse konti korrekt.</span><span class="sxs-lookup"><span data-stu-id="72ecb-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="72ecb-123">Før du afhænder et anlægsaktiv som kasseret, skal du oprette finanskonti, der er knyttet til anlægsaktivets anskaffelsesværdi, afskrivning for indeværende år, afskrivning for tidligere år og anlægsaktivets BNV.</span><span class="sxs-lookup"><span data-stu-id="72ecb-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="72ecb-124">Posteringstyperne for anlægsaktiver vises på siden **Posteringsprofiler for anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="72ecb-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="72ecb-125">Gå til **Anlægsaktiver \> Opsætning \> Posteringsprofiler for anlægsaktiver**, og vælg derefter **Kasseres** i feltet over gitteret på oversigtspanelet **Kassation**.</span><span class="sxs-lookup"><span data-stu-id="72ecb-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles**, and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="72ecb-126">I følgende illustration vises listen over posteringstyper for anlægsaktiver på siden **Posteringsprofiler for anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="72ecb-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="72ecb-127">[![Afhændelse af et aktiv som kasseret, fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="72ecb-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="72ecb-128">I følgende eksempel blev der anskaffet et anlægsaktiv d. 1. januar 2018, og det vil blive kasseret den 31. marts 2019.</span><span class="sxs-lookup"><span data-stu-id="72ecb-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="72ecb-129">**Anskaffelsespris** : 24.000,00 amerikanske dollars (USD)</span><span class="sxs-lookup"><span data-stu-id="72ecb-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="72ecb-130">**Levetid:** To år</span><span class="sxs-lookup"><span data-stu-id="72ecb-130">**Service life:** Two years</span></span>
- <span data-ttu-id="72ecb-131">**Afskrivningsmetode:** Lineær afskrivning over servicelevetiden</span><span class="sxs-lookup"><span data-stu-id="72ecb-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="72ecb-132">**Afskrivningsbeløb:** 1.000,00 USD pr. måned</span><span class="sxs-lookup"><span data-stu-id="72ecb-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="72ecb-133">BNV for et anlægsaktiv beregnes ved hjælp af følgende formel:</span><span class="sxs-lookup"><span data-stu-id="72ecb-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="72ecb-134">Bogført nettoværdi = anskaffelsespris – afskrivning</span><span class="sxs-lookup"><span data-stu-id="72ecb-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="72ecb-135">I dette eksempel blev anlægsaktivet anskaffet og afskrevet over 15 måneder fra januar 2018 til og med marts 2019.</span><span class="sxs-lookup"><span data-stu-id="72ecb-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="72ecb-136">Derfor er anlægsaktivets BNV 9.000.00 USD (24.000,00 USD – 15.000,00 USD).</span><span class="sxs-lookup"><span data-stu-id="72ecb-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="72ecb-137">[![Eksempel på afskrivning af anlægsaktiv](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="72ecb-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="72ecb-138">Hvis du vil oprette en kassationskladde, skal du gå til **Anlægsaktiver \> Kladdeposteringer \> Anlægsaktivkladde** og derefter vælge **Linjer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="72ecb-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal**, and then, on the Action Pane, select **Lines**.</span></span> <span data-ttu-id="72ecb-139">Vælg **Kassation - spild**, og vælg derefter et anlægsaktiv-id.</span><span class="sxs-lookup"><span data-stu-id="72ecb-139">Select **Disposal – scrap**, and then select a fixed asset ID.</span></span> <span data-ttu-id="72ecb-140">Hvis du vil afhænde aktivet fuldstændigt, skal du ikke angive en værdi i hverken **Debet**- eller **Kredit**-feltet</span><span class="sxs-lookup"><span data-stu-id="72ecb-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="72ecb-141">[![Anlægsaktivkladde](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="72ecb-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="72ecb-142">Spildposteringen for kassation af anlægsaktiver ændrer feltværdierne for anlægsaktivkartoteket på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="72ecb-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="72ecb-143">I sektionen **Saldo** opdateres feltet **Status** til **Skrottet**.</span><span class="sxs-lookup"><span data-stu-id="72ecb-143">In the **Balance** section, the **Status** field is updated to **Scrapped**.</span></span>
- <span data-ttu-id="72ecb-144">Feltet **Afhændelsesdato** i sektionen **Afgang** angives til den dato, hvor aktivet blev kasseret.</span><span class="sxs-lookup"><span data-stu-id="72ecb-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="72ecb-145">[![Oplysninger om anlægsaktivkladde](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="72ecb-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="72ecb-146">I følgende illustration vises anlægsaktivets saldo.</span><span class="sxs-lookup"><span data-stu-id="72ecb-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="72ecb-147">[![Saldo for anlægsaktiver](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="72ecb-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="72ecb-148">I følgende illustration vises det bilag, der er bogført.</span><span class="sxs-lookup"><span data-stu-id="72ecb-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="72ecb-149">[![Bogført nettoværdi](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="72ecb-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]