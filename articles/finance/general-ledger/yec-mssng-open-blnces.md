---
title: Årsafslutning mangler startsaldi
description: I dette emne beskrives det, hvorfor der muligvis mangler startsaldi, når du lukker et år, og hvordan du kan gendanne disse saldi, hvis de mangler.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028555"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="894b5-103">Årsafslutning mangler startsaldi</span><span class="sxs-lookup"><span data-stu-id="894b5-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="894b5-104">I dette emne beskrives det, hvorfor der muligvis mangler startsaldi, når du lukker et år, og hvordan du kan gendanne disse saldi, hvis de mangler.</span><span class="sxs-lookup"><span data-stu-id="894b5-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="894b5-105">Symptom</span><span class="sxs-lookup"><span data-stu-id="894b5-105">Symptom</span></span>

<span data-ttu-id="894b5-106">Hvorfor findes der ingen startsaldi, efter at du har kørt afslutning af finansåret?</span><span class="sxs-lookup"><span data-stu-id="894b5-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="894b5-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="894b5-107">Resolution</span></span>

<span data-ttu-id="894b5-108">Du skal kontrollere følgende, hvis du har lukket et år i Finans og derefter genereret en råbalance, der ikke viser startsaldi for det næste regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="894b5-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="894b5-109">Hvis feltet **Fortryd forrige afslutning** er angivet til **Ja**, tilbageføres den forrige ultimoafslutning for det samme regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="894b5-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="894b5-110">Når du kører en proces til at fortryde årsafslutningen, slettes alle poster for ultimo- og startsaldierne, som om året aldrig er blevet lukket.</span><span class="sxs-lookup"><span data-stu-id="894b5-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="894b5-111">Bilagene slettes også.</span><span class="sxs-lookup"><span data-stu-id="894b5-111">The vouchers are also deleted.</span></span> <span data-ttu-id="894b5-112">Årsafslutningen køres ikke automatisk igen.</span><span class="sxs-lookup"><span data-stu-id="894b5-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="894b5-113">Du skal starte processen igen, og denne gang skal du opdatere valget **Fortryd forrige lukning** til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="894b5-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="894b5-114">Dette scenario er dækket i emnet for ofte stillede spørgsmål om årsafslutning.</span><span class="sxs-lookup"><span data-stu-id="894b5-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="894b5-115">Du kan finde yderligere oplysninger i [Ofte stillede spørgsmål om årsafslutning](faq-year-end-activities.md).</span><span class="sxs-lookup"><span data-stu-id="894b5-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="894b5-116">Symptom</span><span class="sxs-lookup"><span data-stu-id="894b5-116">Symptom</span></span>

<span data-ttu-id="894b5-117">Jeg har kørt årsafslutningen med indstillingen **Fortryd forrige lukning** angivet til **Nej**, og jeg har stadig ikke startsaldi for mit regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="894b5-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="894b5-118">Løsning</span><span class="sxs-lookup"><span data-stu-id="894b5-118">Resolution</span></span>

<span data-ttu-id="894b5-119">Kontrollér først status af det valgte batchjob.</span><span class="sxs-lookup"><span data-stu-id="894b5-119">First check the status of the batch job.</span></span> <span data-ttu-id="894b5-120">Lukning af et år omfatter et antal separate opgaver, men det vigtigste trin er batchopgaven med opgavebeskrivelsen **Trin 5.0.0**.</span><span class="sxs-lookup"><span data-stu-id="894b5-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="894b5-121">Bogføring af primotransaktionerne, og eventuelt ultimotransaktionerne, til Finans, sker i løbet af dette trin.</span><span class="sxs-lookup"><span data-stu-id="894b5-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="894b5-122">[![Liste over batchhistorik](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="894b5-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="894b5-123">Hvis dette trin blev afsluttet uden fejl, men startsaldi ikke vises på siden **Forespørgsel om råbalance** (**Finans > Forespørgsler og rapporter > Prøvesaldo**), kan du gennemse resultaterne af batchjobbet for årsafslutning for at se, om trinnet Genberegn saldi er fuldført korrekt.</span><span class="sxs-lookup"><span data-stu-id="894b5-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="894b5-124">[![Resultater af batchjob for årsafslutning](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="894b5-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="894b5-125">Hvis dette trin af en eller anden grund ikke er lykkedes, er det sandsynligt, at primotransaktionerne (og eventuelt lukningen) er blevet bogført korrekt.</span><span class="sxs-lookup"><span data-stu-id="894b5-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="894b5-126">Du kan kontrollere, at finanstransaktionerne er bogført korrekt ved hjælp af siden **Forespørgsel om bilagstransaktioner** ved at angive det bilagsnummer og den dato, der er angivet i dialogboksen for årsafslutningen af det år, du lukkede, (**Finans > Forespørgsler og rapporter > Bilagstransaktioner**).</span><span class="sxs-lookup"><span data-stu-id="894b5-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="894b5-127">[![Forespørgsel om bilagstransaktioner](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="894b5-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="894b5-128">Hvis der findes primobilag (og eventuelt lukningsbilag), behøver du ikke at køre årsafslutningen igen.</span><span class="sxs-lookup"><span data-stu-id="894b5-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="894b5-129">Du kan i stedet gå til næste afsnit for at få oplysninger om, hvad du skal gøre herefter.</span><span class="sxs-lookup"><span data-stu-id="894b5-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="894b5-130">Symptom</span><span class="sxs-lookup"><span data-stu-id="894b5-130">Symptom</span></span>

<span data-ttu-id="894b5-131">Trinnet "Gendan saldi" i årsafslutningen mislykkedes. Skal jeg køre hele årsafslutningen igen?</span><span class="sxs-lookup"><span data-stu-id="894b5-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="894b5-132">Løsning</span><span class="sxs-lookup"><span data-stu-id="894b5-132">Resolution</span></span>

<span data-ttu-id="894b5-133">I trinnet Generer saldi opdateres de finanssaldi, der bruges, når der genereres en forespørgsel om råbalance.</span><span class="sxs-lookup"><span data-stu-id="894b5-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="894b5-134">Det er det sidste trin i årsafslutningen.</span><span class="sxs-lookup"><span data-stu-id="894b5-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="894b5-135">Hvis dette trin er det eneste trin, der mislykkes, er bogføringen af finanstransaktionerne gennemført.</span><span class="sxs-lookup"><span data-stu-id="894b5-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="894b5-136">Du behøver ikke at køre årsafslutningen igen.</span><span class="sxs-lookup"><span data-stu-id="894b5-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="894b5-137">Du kan køre processen for at gendanne saldi manuelt ved hjælp af siden **Økonomiske dimensionsopsætninger** (**Finans > Kontoplan > Dimensioner > Økonomiske dimensionssæt**).</span><span class="sxs-lookup"><span data-stu-id="894b5-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="894b5-138">[![Knappen Gendan saldi på siden Økonomiske dimensionssæt](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="894b5-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="894b5-139">Hvis det tager lang tid at behandle dette trin, anbefaler vi, at du gennemser de bedste praksis for økonomiske dimensionssæt som beskrevet i [Bedste praksis til opdatering af økonomiske dimensionssæt](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span><span class="sxs-lookup"><span data-stu-id="894b5-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 

