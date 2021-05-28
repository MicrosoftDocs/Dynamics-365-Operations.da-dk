---
title: Momsen beregnes ikke, eller momsbeløbet er nul
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig, når momsbeløbet er 0 (nul) eller ikke er beregnet.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: c398579a0a408e7f5625a3e801a967955c4b1e5b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020109"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="1e256-103">Momsen beregnes ikke, eller momsbeløbet er nul</span><span class="sxs-lookup"><span data-stu-id="1e256-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e256-104">En transaktion kan have et linjebeløb, der ikke er 0 (nul), men enten er momsbeløbet ikke beregnet, eller det beregnede momsbeløb er 0.</span><span class="sxs-lookup"><span data-stu-id="1e256-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="1e256-105">Du kan udføre fejlfinding af dette problem ved at følge trinnene i følgende afsnit efter behov.</span><span class="sxs-lookup"><span data-stu-id="1e256-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="1e256-106">Kontrollér, at momskoderne er valgt korrekt af transaktionen</span><span class="sxs-lookup"><span data-stu-id="1e256-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="1e256-107">Hvis transaktionen ikke vælger de rette momskoder, eller hvis den ikke vælger nogen momskoder, beregnes der ikke moms af den.</span><span class="sxs-lookup"><span data-stu-id="1e256-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="1e256-108">Benyt denne fremgangsmåde for at kontrollere, at momskoderne er valgt korrekt af transaktionen.</span><span class="sxs-lookup"><span data-stu-id="1e256-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="1e256-109">På posteringslinjen i oversigtspanelet **Linjedetaljer** under fanen **Opsætning** i sektionen **Moms** skal du kontrollere, at de korrekte momsgrupper er valgt i felterne **Varemomsgruppe** og **Momsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="1e256-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="1e256-110">Hvis de korrekte momsgrupper ikke er valgt, skal du vælge dem.</span><span class="sxs-lookup"><span data-stu-id="1e256-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="1e256-111">[![Felterne Varemomsgruppe og Momsgruppe](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="1e256-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="1e256-112">Gå til **Moms** \> **Indirekte skatter** \> **Moms** \> **Momsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="1e256-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="1e256-113">Vælg den relevante momsgruppe, og noter derefter momskoden i feltet **Momskode** i oversigtspanelet **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="1e256-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="1e256-114">[![Siden Momsgrupper](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="1e256-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="1e256-115">Gå til **Moms** \> **Indirekte skatter** \> **Moms** \> **Varemomsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="1e256-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="1e256-116">Vælg den relevante varemomsgruppe, og kontroller derefter, at momskoden i feltet **Momskode** svarer til momsgruppens momskode i oversigtspanelet **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="1e256-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="1e256-117">[![Siden Varemomsgrupper](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="1e256-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="1e256-118">Hvis momskoderne ikke stemmer overens, skal du opdatere momskoden for en af grupperne.</span><span class="sxs-lookup"><span data-stu-id="1e256-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="1e256-119">Kontrollér, at de valgte momskoder ikke er fritaget for moms, og at de har den rette momssatsværdi</span><span class="sxs-lookup"><span data-stu-id="1e256-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="1e256-120">Hvis momskoderne er fritaget for moms, eller hvis momssatsen er 0 (nul), vil resultatet af momsberegningen være 0.</span><span class="sxs-lookup"><span data-stu-id="1e256-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="1e256-121">Benyt følgende fremgangsmåde for at finde ud af, om de valgte momskoder er fritaget for moms, og for at kontrollere, at den rette momssats er anvendt til dem.</span><span class="sxs-lookup"><span data-stu-id="1e256-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="1e256-122">Gå til **Moms** \> **Indirekte skatter** \> **Moms** \> **Momsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="1e256-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="1e256-123">Vælg den relevante momsgruppe, og kontroller derefter, at afkrydsningsfeltet **Momsfritagelse** ikke er markeret, i oversigtspanelet **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="1e256-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="1e256-124">Hvis feltet er markeret, skal du fjerne markeringen.</span><span class="sxs-lookup"><span data-stu-id="1e256-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="1e256-125">[![Afkrydsningsfeltet Momsfritagelse på siden Momsgrupper](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="1e256-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="1e256-126">Gå til **Moms** \> **Indirekte skatter** \> **Moms** \> **Momskoder**.</span><span class="sxs-lookup"><span data-stu-id="1e256-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="1e256-127">Vælg den relevante momskode, og kontroller derefter, at momssatsværdien i **feltet Værdi** ikke er 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="1e256-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="1e256-128">Hvis værdien er 0, skal du opdatere feltet, så det er indstillet til den rette momssats.</span><span class="sxs-lookup"><span data-stu-id="1e256-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="1e256-129">[![Feltet Værdi på siden Momskodeværdier](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="1e256-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="1e256-130">Afgøre, om nul er det korrekte momsbeløb</span><span class="sxs-lookup"><span data-stu-id="1e256-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="1e256-131">I nogle tilfælde er et momsbeløb på 0 (nul) korrekt.</span><span class="sxs-lookup"><span data-stu-id="1e256-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="1e256-132">Benyt denne fremgangsmåde for at finde ud af, om 0 er det korrekte momsbeløb for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="1e256-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="1e256-133">Gå til **Finans** \> **Opsætning Finans** \> **Finansparametre**.</span><span class="sxs-lookup"><span data-stu-id="1e256-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="1e256-134">Kontrollér, at **Total** er valgt i feltet **Beregningsmetode** under fanen **Moms**.</span><span class="sxs-lookup"><span data-stu-id="1e256-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="1e256-135">[![Feltet Beregningsmetode på siden Finansparametre](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="1e256-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="1e256-136">Gå til **Moms** \> **Indirekte skatter** \> **Moms** \> **Momskoder**.</span><span class="sxs-lookup"><span data-stu-id="1e256-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="1e256-137">Vælg den relevante momskode, vælg **Beregning** \> **Beregningsgrundlag**, og kontrollér, at beregningsgrundlaget er angivet til **Nettobeløb for fakturasaldo** eller **Fakturatotal inkl. andre momsbeløb**.</span><span class="sxs-lookup"><span data-stu-id="1e256-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="1e256-138">Yderligere oplysninger finder du i [Fakturatotal inkl. andre momsbeløb](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span><span class="sxs-lookup"><span data-stu-id="1e256-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="1e256-139">Hvis de korrekte værdier er angivet i trin 2 og 4, skal du afgøre, om det samlede beløb for transaktionen er 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="1e256-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="1e256-140">Hvis totalbeløbet er 0, er et momsbeløb på 0 det forventede resultat.</span><span class="sxs-lookup"><span data-stu-id="1e256-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="1e256-141">Da momsberegningen er baseret på fakturasaldoens totalbeløb, og ikke beløbet linje for linje, fordeles momsbeløbet på 0 til hver linje efter momsberegningen.</span><span class="sxs-lookup"><span data-stu-id="1e256-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="1e256-142">Afgøre, om der findes tilpasninger</span><span class="sxs-lookup"><span data-stu-id="1e256-142">Determine whether customization exists</span></span>

<span data-ttu-id="1e256-143">Hvis du har udført trinnene i de forrige afsnit, men ikke har fundet nogen problemer, skal du afgøre, om der er foretaget tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="1e256-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="1e256-144">Hvis der ikke er foretaget tilpasninger, skal du oprette en Microsoft-serviceanmodning for at få yderligere support.</span><span class="sxs-lookup"><span data-stu-id="1e256-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
