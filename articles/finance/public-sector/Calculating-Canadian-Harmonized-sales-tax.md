---
title: Canadisk harmoniseret moms (Harmonized Sales Tax - HST)
description: Dette emne giver oplysninger om funktionerne til at understøtte harmoniseret moms for den offentlige sektor.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNCanadianHSTTaxFeature
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: roschlom
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 777429c616c7c198f60eec2475012fe831fd26fe
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407664"
---
# <a name="calculating-canadian-harmonized-sales-tax"></a><span data-ttu-id="1ea1f-103">Beregning af canadisk harmoniseret moms</span><span class="sxs-lookup"><span data-stu-id="1ea1f-103">Calculating Canadian Harmonized Sales Tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ea1f-104">Denne funktion giver din organisation mulighed for at overholde de canadiske harmoniserede momsregler (HST).</span><span class="sxs-lookup"><span data-stu-id="1ea1f-104">This feature lets your organization comply with Canadian Harmonized Sales Tax (HST) rules.</span></span> <span data-ttu-id="1ea1f-105">HST hjælper offentlige institutioner med at overholde canadiske momspolitikker.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-105">The HST helps public sector entities maintain compliance with Canadian tax policies.</span></span> <span data-ttu-id="1ea1f-106">HST bruges af visse canadiske provinser og er en kombination af moms på varer og ydelser og provinsmoms.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-106">The HST is used by some Canadian provinces and is a combination of the Goods and Services Tax and the Provincial Sales Tax.</span></span>
<span data-ttu-id="1ea1f-107">Dele af HST kan genvindes af offentlige myndigheder, hvis momsen er betalt til kreditorer, afhængigt af købets formål.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-107">Portions of the HST can be recovered by public sector entities if the tax has been paid to vendors, depending on the intent of the purchase.</span></span> <span data-ttu-id="1ea1f-108">Formålet er angivet af de økonomiske dimensionsværdier og hovedkontoen på en posteringslinje i et købsdokument (f.eks. en indkøbsrekvisition, en indkøbsordre eller en kreditorfaktura).</span><span class="sxs-lookup"><span data-stu-id="1ea1f-108">The intent is designated by the financial dimension values and main account on a transaction line on a purchase document (for example, a purchase requisition, purchase order, or vendor invoice).</span></span>
<span data-ttu-id="1ea1f-109">Bemærk! Denne funktionalitet gælder ikke for kreditorfakturakladden.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-109">Note: This functionality does not apply to the Accounts payable Invoice journal.</span></span>

## <a name="enabling-the-hst-feature"></a><span data-ttu-id="1ea1f-110">Aktivere funktionen HST</span><span class="sxs-lookup"><span data-stu-id="1ea1f-110">Enabling the HST feature</span></span>

1. <span data-ttu-id="1ea1f-111">Gå til **Finans > Opsætning Finans > Finansparametre > Momsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-111">Go to **General ledger > Ledger setup >General ledger parameters > Sales tax group**.</span></span>
2. <span data-ttu-id="1ea1f-112">Indstil **Anvend canadiske harmoniserede momsregler** til **Ja**, hvis du vil aktivere funktionen.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-112">Set the **Apply Canadian harmonized sales tax rules** to **Yes** to enable the feature.</span></span>

## <a name="define-the-dimensions-for-hst-rules"></a><span data-ttu-id="1ea1f-113">Definere dimensionerne for HST-regler</span><span class="sxs-lookup"><span data-stu-id="1ea1f-113">Define the dimensions for HST rules</span></span>

1. <span data-ttu-id="1ea1f-114">Gå til **Moms > Indirekte moms > Moms**, og klik derefter på **Harmoniserede momsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-114">Go to **Tax > Indirect taxes > Sales tax**, and then click **Harmonized sales tax dimensions**.</span></span> 
2. <span data-ttu-id="1ea1f-115">På siden **Harmoniserede momsdimensioner** skal du vælge og prioritere de økonomiske dimensioner (sammen med hovedkontoen, hvis det er relevant), du vil bruge til HST.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-115">In the **Harmonized sales tax dimensions** page, select and prioritize the financial dimensions (along with the main account, if appropriate) that you want to use for HST.</span></span> <span data-ttu-id="1ea1f-116">De økonomiske dimensioner i kontostrukturer knyttes til kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-116">The financial dimensions in the account structures are associated with the chart of accounts.</span></span> <span data-ttu-id="1ea1f-117">Dimensionernes prioritet er en hjælp til at diktere den moms, der anvendes, hvis der er flere muligheder.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-117">The priority of dimensions helps dictate which tax gets applied if there are multiple possibilities.</span></span> 



### <a name="note-only-the-financial-dimensions-that-are-used-in-the-current-legal-entity-will-be-available"></a><span data-ttu-id="1ea1f-118">Bemærk! Kun de økonomiske dimensioner, der bruges i den aktuelle juridiske enhed, vil være tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-118">Note: Only the financial dimensions that are used in the current legal entity will be available.</span></span>

## <a name="set-up-hst-rules"></a><span data-ttu-id="1ea1f-119">Konfigurere HST-regler</span><span class="sxs-lookup"><span data-stu-id="1ea1f-119">Set up HST rules</span></span>

<span data-ttu-id="1ea1f-120">Når du har defineret dimensionerne for HST, skal du konfigurere de finansdimensionsregler, der gælder.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-120">After you define dimensions for HST, you set up ledger dimension rules that apply.</span></span> <span data-ttu-id="1ea1f-121">HST-regler tildeler momskoder ud fra dokumentlinjers kontofordelinger.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-121">HST rules assign tax codes based on a document line’s account distributions.</span></span> <span data-ttu-id="1ea1f-122">Det skyldes, at der kan anvendes forskellige momskoder baseret på formålet med købet.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-122">This is because different tax codes might be applied, based on the purpose of the purchase.</span></span>
1. <span data-ttu-id="1ea1f-123">Gå til **Moms > Indirekte moms > Moms**, og klik derefter på **Harmoniserede momsregler**.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-123">Go to **Tax > Indirect taxes > Sales tax**, and then click **Harmonized sales tax rules**.</span></span> 
2. <span data-ttu-id="1ea1f-124">På siden **Harmoniserede momsregler** vises de dimensioner, du har valgt til HST, i prioriteret rækkefølge fra venstre mod højre.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-124">In the **Harmonized sales tax rules** page, the dimensions that you selected for HST appear in order of priority from left to right.</span></span> <span data-ttu-id="1ea1f-125">De resterende kolonner gælder for momskoder, der er tilknyttet denne dimensionskombination.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-125">The remaining columns are for sales tax codes associated with that dimension combination.</span></span> 
3. <span data-ttu-id="1ea1f-126">Vælg **Ny** i handlingsruden for at oprette en ny post.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-126">On the Action Pane, click **New** to create a new record.</span></span>
4. <span data-ttu-id="1ea1f-127">Definer dimensionsværdierne.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-127">Define the dimension values.</span></span> 

### <a name="notes"></a><span data-ttu-id="1ea1f-128">Noter:</span><span class="sxs-lookup"><span data-stu-id="1ea1f-128">Notes:</span></span>
- <span data-ttu-id="1ea1f-129">Der kan ikke være identiske indstillinger for to rækker.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-129">No two rows can have identical settings.</span></span>
- <span data-ttu-id="1ea1f-130">Du kan slette eller redigere eksisterende regler.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-130">You can delete or modify existing rules.</span></span>
- <span data-ttu-id="1ea1f-131">Du kan vælge at lade et segment være tomt.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-131">You can choose to leave a segment blank.</span></span> <span data-ttu-id="1ea1f-132">Det fungerer som "joker".</span><span class="sxs-lookup"><span data-stu-id="1ea1f-132">It will function as a “wild card.”</span></span> <span data-ttu-id="1ea1f-133">En fuldstændigt tom række gælder for alle kontokombinationer, hvor der ikke er anvendt en mere specifik regel.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-133">A totally blank row applies to all account combinations that do not have a more specific rule applied.</span></span> <span data-ttu-id="1ea1f-134">Du kan tilføje én række med alle tomme økonomiske dimensioner, hvis der er momskoder, som skal anvendes, når ingen regler matcher.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-134">You may want to add one row with all blank financial dimensions if there are sales tax codes which should apply when no rules match.</span></span>

5. <span data-ttu-id="1ea1f-135">Vælg op til fem momskoder, der kan anvendes i forhold til de dimensioner, der er valgt til HST.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-135">Select up to five sales tax codes that can be applied against the dimensions that have been selected for HST.</span></span> <span data-ttu-id="1ea1f-136">Bemærk! For at kunne anvendes skal de momskoder, der er defineret her, være til stede i HST-reglen og i både den **Momsgruppe** og **Varemomsgruppe**, der er valgt på linjerne i transaktionsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-136">Note To be applied, the sales tax codes defined here must be present in the HST rule and in both the **Sales tax group** and **Item sales tax group** that are selected on the transaction document lines.</span></span> 
6. <span data-ttu-id="1ea1f-137">Klik på **Gem** for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-137">Click **Save** to save your changes.</span></span> 

### <a name="notes"></a><span data-ttu-id="1ea1f-138">Noter:</span><span class="sxs-lookup"><span data-stu-id="1ea1f-138">Notes:</span></span>
- <span data-ttu-id="1ea1f-139">Når du har defineret reglerne for HST, kan du ikke redigere eksisterende dimensioner for HST.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-139">After you define rules for HST, you cannot modify the pre-existing dimensions for HST.</span></span> <span data-ttu-id="1ea1f-140">Hvis du vil foretage ændringer, skal du først fjerne alle regler og momskoder i formularen **Harmoniserede momsregler**.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-140">To make changes, you must first remove all rules and sales tax codes in the **Harmonized sales tax rules** form.</span></span>
- <span data-ttu-id="1ea1f-141">Der kan anvendes mere end én momskode på en regel.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-141">More than one tax code can apply to a rule.</span></span>
- <span data-ttu-id="1ea1f-142">Der gælder kun én regel for en kontofordeling.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-142">Only one rule applies to an account distribution.</span></span>
- <span data-ttu-id="1ea1f-143">Der kan gælde mere end én regel for en linje i et transaktionsdokument med flere fordelinger.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-143">More than one rule can apply to a line in a transaction document that has multiple distributions.</span></span>

## <a name="how-rules-are-applied"></a><span data-ttu-id="1ea1f-144">Sådan anvendes regler</span><span class="sxs-lookup"><span data-stu-id="1ea1f-144">How rules are applied</span></span>

<span data-ttu-id="1ea1f-145">Den rækkefølge, som reglerne anvendes i, er noget kompleks.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-145">The order in which rules are applied are somewhat complex.</span></span> <span data-ttu-id="1ea1f-146">Følgende grafik viser princippet:</span><span class="sxs-lookup"><span data-stu-id="1ea1f-146">The following graphic illustrates the principle:</span></span>

> <span data-ttu-id="1ea1f-147">[![Definere HST-regler](./media/define-hst-rules.png)](./media/define-hst-rules.png)</span><span class="sxs-lookup"><span data-stu-id="1ea1f-147">[![Define HST rules](./media/define-hst-rules.png)](./media/define-hst-rules.png)</span></span>

<span data-ttu-id="1ea1f-148">De momskoder, der er valgt for dimensionslinjen, er som følger, hvis posteringen bruger en momsgruppe og varemomsgruppe med alle de momskoder, der er medtaget.</span><span class="sxs-lookup"><span data-stu-id="1ea1f-148">The sales tax codes selected for the dimension line will be following if the transaction uses a Sales tax group and Item sales tax group with all of the tax codes included.</span></span>

|<span data-ttu-id="1ea1f-149">Økonomiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="1ea1f-149">Financial Dimensions</span></span>                     | <span data-ttu-id="1ea1f-150">Momskoder</span><span class="sxs-lookup"><span data-stu-id="1ea1f-150">Sales tax codes</span></span>|
|-----------------------------------------|-----------------|   
|<span data-ttu-id="1ea1f-151">Fond 101, enhver division med undtagelse af 111 og 121</span><span class="sxs-lookup"><span data-stu-id="1ea1f-151">Fund 101, Any Division except 111 and 121</span></span>| <span data-ttu-id="1ea1f-152">Tax1</span><span class="sxs-lookup"><span data-stu-id="1ea1f-152">Tax1</span></span>            |
|   <span data-ttu-id="1ea1f-153">Fond 101, division 111</span><span class="sxs-lookup"><span data-stu-id="1ea1f-153">Fund 101, Division 111</span></span>                  |   <span data-ttu-id="1ea1f-154">Tax1, Tax2, Tax3</span><span class="sxs-lookup"><span data-stu-id="1ea1f-154">Tax1, Tax2, Tax3</span></span>|
|   <span data-ttu-id="1ea1f-155">Fond 101, division 121</span><span class="sxs-lookup"><span data-stu-id="1ea1f-155">Fund 101, Division 121</span></span>                  | <span data-ttu-id="1ea1f-156">Tax2, Tax3</span><span class="sxs-lookup"><span data-stu-id="1ea1f-156">Tax2, Tax3</span></span>      |
|   <span data-ttu-id="1ea1f-157">Fond 303, enhver division med undtagelse af 141</span><span class="sxs-lookup"><span data-stu-id="1ea1f-157">Fund 303, Any Division except 141</span></span>         | <span data-ttu-id="1ea1f-158">Tax1, Tax2, Tax3</span><span class="sxs-lookup"><span data-stu-id="1ea1f-158">Tax1, Tax2, Tax3</span></span>|
|   <span data-ttu-id="1ea1f-159">Fond 303, division 141</span><span class="sxs-lookup"><span data-stu-id="1ea1f-159">Fund 303, Division 141</span></span>                  | <span data-ttu-id="1ea1f-160">Tax1</span><span class="sxs-lookup"><span data-stu-id="1ea1f-160">Tax1</span></span>            |
