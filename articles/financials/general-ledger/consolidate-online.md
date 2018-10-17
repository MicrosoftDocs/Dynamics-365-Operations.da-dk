---
title: "Økonomiske konsolideringer online"
description: "I dette emne beskrives økonomiske onlinekonsolideringer i Finans."
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.translationtype: HT
ms.sourcegitcommit: 2a9ceb774a8f205e39abe6a12a0deb69dd4cb69b
ms.openlocfilehash: fd29dc5f932c9cd274a42923e1ff659dd5d8e9d6
ms.contentlocale: da-dk
ms.lasthandoff: 08/20/2018

---

# <a name="consolidate-online"></a><span data-ttu-id="89ea4-103">Konsolider online</span><span class="sxs-lookup"><span data-stu-id="89ea4-103">Consolidate online</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89ea4-104">I dette emne beskrives økonomiske onlinekonsolideringer i Finans.</span><span class="sxs-lookup"><span data-stu-id="89ea4-104">This topic describes online financial consolidations in General ledger.</span></span> <span data-ttu-id="89ea4-105">Inden du læser dette emne, skal du læse [Økonomiske konsolideringer og valutaomregning](financial-consolidations-currency-translation.md) emne.</span><span class="sxs-lookup"><span data-stu-id="89ea4-105">Before you read this topic, be sure to read the [Financial consolidations and currency translation](financial-consolidations-currency-translation.md) topic.</span></span>

<span data-ttu-id="89ea4-106">Når du har fuldført opsætningen, kan du angive detaljerne om konsolideringen på siden **Konsolider [Online]**.</span><span class="sxs-lookup"><span data-stu-id="89ea4-106">After you've completed your setup, you enter the details of the consolidation on the **Consolidate [Online]** page.</span></span> <span data-ttu-id="89ea4-107">Når du er færdig, kan du klikke på **OK** eller **Batch** for at behandle konsolideringen.</span><span class="sxs-lookup"><span data-stu-id="89ea4-107">When you've finished, you can click **OK** or **Batch** to process the consolidation.</span></span>

## <a name="criteria"></a><span data-ttu-id="89ea4-108">Afgrænsning</span><span class="sxs-lookup"><span data-stu-id="89ea4-108">Criteria</span></span>
<span data-ttu-id="89ea4-109">Under fanen **Kriterier** på siden **Konsolider [Online]** kan du definere kontiene, perioderne og typen af data, der konsolideres.</span><span class="sxs-lookup"><span data-stu-id="89ea4-109">On the **Criteria** tab of the **Consolidate [Online]** page, you define the accounts, the periods, and the type of data that is being consolidated.</span></span>

<span data-ttu-id="89ea4-110">![Fanen Kriterier](./media/criteria-consolidate-online.png "Fanen Kriterier")</span><span class="sxs-lookup"><span data-stu-id="89ea4-110">![Criteria tab](./media/criteria-consolidate-online.png "Criteria tab")</span></span>

<span data-ttu-id="89ea4-111">Her er en forklaring på de forskellige felter under denne fane:</span><span class="sxs-lookup"><span data-stu-id="89ea4-111">Here is an explanation of the various fields on this tab:</span></span>

- <span data-ttu-id="89ea4-112">**Beskrivelse** – Angiv en præcis beskrivelse af den periode, som du konsoliderer.</span><span class="sxs-lookup"><span data-stu-id="89ea4-112">**Description** – Enter a precise description for the period that you're consolidating.</span></span>
- <span data-ttu-id="89ea4-113">**Hovedkonto** – Brug felterne i denne sektion til at definere de hovedkonti, som vil blive behandlet.</span><span class="sxs-lookup"><span data-stu-id="89ea4-113">**Main account** – Use the fields in this section to define the main accounts that will be processed.</span></span>

    - <span data-ttu-id="89ea4-114">**Fra** og **Til** – Angiv et interval af konti, der skal behandle.</span><span class="sxs-lookup"><span data-stu-id="89ea4-114">**From** and **To** – Specify a range of accounts to process.</span></span> <span data-ttu-id="89ea4-115">Hvis du ikke udfylder disse felter, flyttes alle konti fra alle firmaer til det konsoliderede regnskab.</span><span class="sxs-lookup"><span data-stu-id="89ea4-115">If you leave these fields blank, all accounts from all companies will be moved to the consolidation company.</span></span> <span data-ttu-id="89ea4-116">Derfor, hvis du konsoliderer fire firmaer, og hvert firma har en anden kontoplan, oprettes alle konti fra alle fire firmaer i det konsoliderede regnskab.</span><span class="sxs-lookup"><span data-stu-id="89ea4-116">Therefore, if you're consolidating four companies, and each company has a different chart of accounts, all accounts from all four companies will be created in the consolidation company.</span></span>
    - <span data-ttu-id="89ea4-117">**Brug koncernkonto** – Hvis du angiver denne indstilling til **Ja**, bliver feltet **Vælg koncernkonto fra** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="89ea4-117">**Use consolidation account** – If you set this option to **Yes**, the **Select consolidation account from** field becomes available.</span></span> <span data-ttu-id="89ea4-118">I dette felt kan du vælge, om alle konti skal konsolideres til den konsoliderede konto, der er angivet på siden **Hovedkonti**, eller om du vil vælge kontoen i en af koncernkontogrupperne.</span><span class="sxs-lookup"><span data-stu-id="89ea4-118">In this field, select whether all accounts should be consolidated to the consolidation account that is set on the **Main accounts** page, or whether you want to select the account from one of the consolidation account groups.</span></span>
    - <span data-ttu-id="89ea4-119">**Koncernkontogruppe** – Vælg den gruppe, der skal bruges til tilknytningen af hovedkontoen for konsolideringen.</span><span class="sxs-lookup"><span data-stu-id="89ea4-119">**Consolidation account group** – Select the group to use for the main account mapping for the consolidation.</span></span>

- <span data-ttu-id="89ea4-120">**Konsolideringsperiode** – Brug felterne i denne sektion til at definere konsolideringsperioden.</span><span class="sxs-lookup"><span data-stu-id="89ea4-120">**Consolidation period** – Use the fields in this section to define the consolidation period.</span></span>

    - <span data-ttu-id="89ea4-121">**Fra** og **Til** – Angiv et datointerval for konsolideringen.</span><span class="sxs-lookup"><span data-stu-id="89ea4-121">**From** and **To** – Specify a range of dates for the consolidation.</span></span> <span data-ttu-id="89ea4-122">Hvis du ikke udfylder disse felter, bliver konsolideringen behandlet for alle perioder, der er defineret i finanskalenderen for firmaet.</span><span class="sxs-lookup"><span data-stu-id="89ea4-122">If you leave these fields blank, the consolidation will be processed for all periods that are defined in the ledger calendar for the company.</span></span> <span data-ttu-id="89ea4-123">Det anbefales ikke at udfylde disse felter.</span><span class="sxs-lookup"><span data-stu-id="89ea4-123">We don't recommend that you leave these fields blank.</span></span>
    - <span data-ttu-id="89ea4-124">**Medtag faktiske beløb** – Angiv denne indstilling til **Ja** for at konsolidere dine faktiske data.</span><span class="sxs-lookup"><span data-stu-id="89ea4-124">**Include actual amounts** – Set this option to **Yes** to consolidate your actual data.</span></span>
    - <span data-ttu-id="89ea4-125">**Medtag budgetbeløb** – Angiv denne indstilling til **Ja** for at konsolidere data fra budgetregisteret.</span><span class="sxs-lookup"><span data-stu-id="89ea4-125">**Include budget amounts** – Set this option to **Yes** to consolidate data from the budget register.</span></span>
    - <span data-ttu-id="89ea4-126">**Gendan saldi under konsolidering** – Vi anbefaler, at du ikke vælger **Ja** i denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="89ea4-126">**Rebuild balances during consolidation** – We don't recommend that you set this option to **Yes**.</span></span> <span data-ttu-id="89ea4-127">Gendan i stedet saldi som et separat batchjob.</span><span class="sxs-lookup"><span data-stu-id="89ea4-127">Instead, rebuild balances as a separate batch job.</span></span>

- <span data-ttu-id="89ea4-128">**Budgetmodeller** – Hvis du har valgt at konsolidere budgetdata, skal du bruge felterne i denne sektion til at definere budgetmodellerne.</span><span class="sxs-lookup"><span data-stu-id="89ea4-128">**Budget models** – If you've selected to consolidate budget data, use the fields in this section to define the budget models.</span></span>

    - <span data-ttu-id="89ea4-129">**Fra** og **Til** – Angiv det interval af konti, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="89ea4-129">**From** and **To** – Specify the range of models to use.</span></span>
    - <span data-ttu-id="89ea4-130">**Budgetkurstype** – Vælg den budgettype, der skal bruges til valutaomregning for budgetdata.</span><span class="sxs-lookup"><span data-stu-id="89ea4-130">**Budget rate type** – Select the type of budget rate to use for currency translation of budget data.</span></span>

## <a name="financial-dimensions"></a><span data-ttu-id="89ea4-131">Økonomiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="89ea4-131">Financial dimensions</span></span>
<span data-ttu-id="89ea4-132">Under fanen **Økonomiske dimensioner** skal du definere de dimensioner, der skal medtages i det konsoliderede regnskab.</span><span class="sxs-lookup"><span data-stu-id="89ea4-132">On the **Financial dimensions** tab, you define the dimensions that should be included in the consolidation company.</span></span> <span data-ttu-id="89ea4-133">Du kan vælge en dimension ved at indstille feltet **Specifikation** til **Dimension** og derefter definere rækkefølgen for dimensionen i det konsoliderede regnskab.</span><span class="sxs-lookup"><span data-stu-id="89ea4-133">To select a dimension, set the **Specification** field to **Dimension**, and then define the order of the dimension in the consolidation company.</span></span>

<span data-ttu-id="89ea4-134">![Fanen Økonomiske dimensioner](./media/financial-dimensions-cons.png "Fanen Økonomiske dimensioner")</span><span class="sxs-lookup"><span data-stu-id="89ea4-134">![Financial dimensions tab](./media/financial-dimensions-cons.png "Financial dimensions tab")</span></span>

<span data-ttu-id="89ea4-135">Uanset hvilken rækkefølge du definerer, er **Hovedkonto** altid det første segment.</span><span class="sxs-lookup"><span data-stu-id="89ea4-135">Regardless of the order that you define, **Main account** will always be the first segment.</span></span>

## <a name="legal-entities"></a><span data-ttu-id="89ea4-136">Juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="89ea4-136">Legal entities</span></span>
<span data-ttu-id="89ea4-137">Under fanen **Juridiske enheder** skal du definere de firmaer, der skal medtages i det konsoliderede regnskab.</span><span class="sxs-lookup"><span data-stu-id="89ea4-137">On the **Legal entities** tab, you define the companies that should be included in the consolidation company.</span></span> <span data-ttu-id="89ea4-138">Du kan også definere ejerskabsprocentdelen for disse firmaer.</span><span class="sxs-lookup"><span data-stu-id="89ea4-138">You also define the ownership percentage of those companies.</span></span> <span data-ttu-id="89ea4-139">Hvis du angiver mindre end 100 procent ejerskab, bliver den angivne procentdel aggregeret til det konsoliderede regnskab.</span><span class="sxs-lookup"><span data-stu-id="89ea4-139">If you specify less than 100-percent ownership, the specified percentage will be rolled up to the consolidation company.</span></span> <span data-ttu-id="89ea4-140">For enhver omregningsdifference bruges feltet **Kontotype til omregningsdifferencer** til at vælge hovedkontoen fra opsætningen på siden **Konti til automatisk posteringer**.</span><span class="sxs-lookup"><span data-stu-id="89ea4-140">For any translation differences, the **Account type for conversion differences** field is used to select the main account from the setup on the **Accounts for automatic transactions** page.</span></span>

<span data-ttu-id="89ea4-141">![Fanen Juridiske enheder](./media/legal-entities-cons.png "Fanen Juridiske enheder")</span><span class="sxs-lookup"><span data-stu-id="89ea4-141">![Legal entities tab](./media/legal-entities-cons.png "Legal entities tab")</span></span>

<span data-ttu-id="89ea4-142">![Siden Konti til automatiske posteringer](./media/accounts%20for%20automatic%20(cons).png "Siden Konti til automatiske posteringer")</span><span class="sxs-lookup"><span data-stu-id="89ea4-142">![Accounts for automatic transactions page](./media/accounts%20for%20automatic%20(cons).png "Accounts for automatic transactions page")</span></span>

## <a name="elimination"></a><span data-ttu-id="89ea4-143">Eliminering</span><span class="sxs-lookup"><span data-stu-id="89ea4-143">Elimination</span></span>
<span data-ttu-id="89ea4-144">Under fanen **Eliminering** har du tre muligheder for at behandle elimineringer:</span><span class="sxs-lookup"><span data-stu-id="89ea4-144">On the **Elimination** tab, you have three options for processing eliminations:</span></span>

- <span data-ttu-id="89ea4-145">Vælg elimineringsreglen, og vælg derefter **Kun forslag** i feltet **Forslagsmuligheder**.</span><span class="sxs-lookup"><span data-stu-id="89ea4-145">Select the elimination rule, and then, in the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="89ea4-146">Denne indstilling vil behandle elimineringen under konsolideringsprocessen, men den kan ikke bogføre alt på én gang.</span><span class="sxs-lookup"><span data-stu-id="89ea4-146">This option will process the elimination during the consolidation process, but it won't post everything in one step.</span></span> <span data-ttu-id="89ea4-147">Du kan bogføre kladden senere.</span><span class="sxs-lookup"><span data-stu-id="89ea4-147">You can post the journal later.</span></span>
- <span data-ttu-id="89ea4-148">Vælg elimineringsreglen, og vælg derefter **Kun bogføring** i feltet **Forslagsmuligheder**.</span><span class="sxs-lookup"><span data-stu-id="89ea4-148">Select the elimination rule, and then, in the **Proposal options** field, select **Post only**.</span></span> <span data-ttu-id="89ea4-149">Denne indstilling vil behandle elimineringen under konsolideringsprocessen og bogfører alt på én gang.</span><span class="sxs-lookup"><span data-stu-id="89ea4-149">This option will process the elimination during the consolidation process and will post everything in one step.</span></span>
- <span data-ttu-id="89ea4-150">Kør et elimineringsforslag separat fra konsolideringsprocessen ved hjælp af elimineringskladden.</span><span class="sxs-lookup"><span data-stu-id="89ea4-150">Run an elimination proposal separately from the consolidation process by using the elimination journal.</span></span>

<span data-ttu-id="89ea4-151">![Fanen Eliminering](./media/elimination-cons-onl.png "Fanen Eliminering")</span><span class="sxs-lookup"><span data-stu-id="89ea4-151">![Elimination tab](./media/elimination-cons-onl.png "Elimination tab")</span></span>

<span data-ttu-id="89ea4-152">Du kan finde flere oplysninger om elimineringer i [Elimineringsregler](./elimination-rules.md).</span><span class="sxs-lookup"><span data-stu-id="89ea4-152">For more information about eliminations, see [Elimination rules](./elimination-rules.md).</span></span>

## <a name="currency-translation"></a><span data-ttu-id="89ea4-153">Valutaomregning</span><span class="sxs-lookup"><span data-stu-id="89ea4-153">Currency translation</span></span>
<span data-ttu-id="89ea4-154">Under fanen **Valutaomregning** kan du definere den juridiske enhed, kontoen og valutakurstypen og kursen.</span><span class="sxs-lookup"><span data-stu-id="89ea4-154">On the **Currency translation** tab, you define the legal entity, account and exchange rate type, and rate.</span></span> <span data-ttu-id="89ea4-155">Der findes tre muligheder i feltet **Anvend valutakurs fra**:</span><span class="sxs-lookup"><span data-stu-id="89ea4-155">Three options are available in the **Apply exchange rate from** field:</span></span>

- <span data-ttu-id="89ea4-156">**Konsolideringsdato** – Datoen for konsolideringen bruges til at hente valutakursen.</span><span class="sxs-lookup"><span data-stu-id="89ea4-156">**Consolidation date** – The date of the consolidation will be used to get the exchange rate.</span></span> <span data-ttu-id="89ea4-157">Denne kurs svarer til spotsatsen eller kursen ved månedens afslutning.</span><span class="sxs-lookup"><span data-stu-id="89ea4-157">This rate is equivalent to the spot or month-end rate.</span></span> <span data-ttu-id="89ea4-158">Du kan se en forhåndsvisning af kursen, men du kan ikke redigere den.</span><span class="sxs-lookup"><span data-stu-id="89ea4-158">You will see a preview of the rate, but you can't edit it.</span></span>
- <span data-ttu-id="89ea4-159">**Posteringsdato** – Datoen for hver postering, der skal bruges til at vælge en valutakurs.</span><span class="sxs-lookup"><span data-stu-id="89ea4-159">**Transaction date** – The date of each transaction will be used to select an exchange rate.</span></span> <span data-ttu-id="89ea4-160">Denne indstilling bruges oftest til anlægsaktiver og kaldes ofte en historisk kurs.</span><span class="sxs-lookup"><span data-stu-id="89ea4-160">This option is most often used for fixed assets and is often referred to as a historical rate.</span></span> <span data-ttu-id="89ea4-161">Du kan ikke se en forhåndsvisning af satsen, fordi der vil være mange satser for de forskellige transaktioner i kontointervallet.</span><span class="sxs-lookup"><span data-stu-id="89ea4-161">You can't see a preview of the rate, because there will be many rates for the various transactions in the account range.</span></span>
- <span data-ttu-id="89ea4-162">**Brugerdefineret sats** – Når du vælger denne indstilling, kan du angive den valutakurs, som du ønsker.</span><span class="sxs-lookup"><span data-stu-id="89ea4-162">**User defined rate** – After you select this option, you can enter the exchange rate that you want.</span></span> <span data-ttu-id="89ea4-163">Denne indstilling kan være praktisk ved gennemsnitlige valutakurser, eller hvis du konsoliderer mod en fast valutakurs.</span><span class="sxs-lookup"><span data-stu-id="89ea4-163">This option can be useful for average exchange rates or if you're consolidating against a fixed exchange rate.</span></span>

<span data-ttu-id="89ea4-164">![Fanen Valutaomregning](./media/currency-translation-cons-online.png "Fanen Valutaomregning")</span><span class="sxs-lookup"><span data-stu-id="89ea4-164">![Currency translation tab](./media/currency-translation-cons-online.png "Currency translation tab")</span></span>

## <a name="additional-resources"></a><span data-ttu-id="89ea4-165">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="89ea4-165">Additional resources</span></span>

<span data-ttu-id="89ea4-166">Du kan finde flere oplysninger om konsolidering og valutaomregning i det overordnede emne til dette emne, [Økonomiske konsolideringer og valutaomregning](./financial-consolidations-currency-translation.md).</span><span class="sxs-lookup"><span data-stu-id="89ea4-166">For more information about consolidation and currency translations, see the parent topic of this topic, [Financial consolidations and currency translation](./financial-consolidations-currency-translation.md).</span></span>

<span data-ttu-id="89ea4-167">Oplysninger om scenarier, hvor du kan generere konsoliderede regnskaber, finder du i [Generere konsoliderede regnskaber](./generating-consolidated-financial-statements.md).</span><span class="sxs-lookup"><span data-stu-id="89ea4-167">For information about scenarios where you might generate consolidate financial statements, see [Generate consolidated financial statements](./generating-consolidated-financial-statements.md).</span></span>
