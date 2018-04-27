---
title: "Bogføringsdefinitioner"
description: "Denne artikel indeholder eksempler på, hvordan bogføringsdefinitioner bruges for behæftelser i indkøbsordrer og budgetdisponeringer."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 10015952773ce0ae6ab36912df636919b572704d
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="posting-definition-examples"></a><span data-ttu-id="68175-103">Eksempler på bogføringsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="68175-103">Posting definition examples</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="68175-104">Denne artikel indeholder eksempler på, hvordan bogføringsdefinitioner bruges for behæftelser i indkøbsordrer og budgetdisponeringer.</span><span class="sxs-lookup"><span data-stu-id="68175-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="68175-105">Inden du læser dette emne, skal du være fortrolig med bogføringsdefinitioner og posteringsbogføringsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="68175-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="68175-106">Du kan finde flere oplysninger i [Bogføringsdefinitioner](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="68175-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="68175-107">Følgende eksempler kan konfigureres på siden **Bogføringsdefinitioner**.</span><span class="sxs-lookup"><span data-stu-id="68175-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="68175-108">Hvert eksempel indeholder følgende områder:</span><span class="sxs-lookup"><span data-stu-id="68175-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="68175-109">Bogføringsdefinition – søgekriterier</span><span class="sxs-lookup"><span data-stu-id="68175-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="68175-110">Bogføringsdefinition – genererede poster</span><span class="sxs-lookup"><span data-stu-id="68175-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="68175-111">Posteringer med konti, dimensionsværdier og beløb</span><span class="sxs-lookup"><span data-stu-id="68175-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="68175-112">Finansposter genereret fra bogføringsdefinitionen</span><span class="sxs-lookup"><span data-stu-id="68175-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="68175-113">Når der er en match mellem kontiene og dimensionsværdierne i ruden **Sammenlign kriterier** for bogføringsdefinitionen og dimensionsværdierne i posteringen, genereres der finansposter med udgangspunkt i ruden **Genererede poster** for bogføringsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="68175-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="68175-114">Knyt en bogføringsdefinition til en bestemt posteringstype ved brug af siden **Definitioner af posteringsbogføring**.</span><span class="sxs-lookup"><span data-stu-id="68175-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="68175-115">Efter at du har knyttet en bogføringsdefinition til en posteringstype og valgt **Brug bogføringsdefinitioner** på siden **Finansparametre**, skal alle posteringer med den valgte posteringstype bruge bogføringsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="68175-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="68175-116">Eksempel: Behæftelser for indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="68175-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="68175-117">Når du aktiverer behandling af behæftelser ved at vælge **Aktivér behæftelse** på siden **Finansparametre**, skal der bruges bogføringsposteringer til registrering af behæftelser i finans for alle konti, der skal hensættes.</span><span class="sxs-lookup"><span data-stu-id="68175-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="68175-118">I de fleste tilfælde hensættes alle udgiftskonti på balancen.</span><span class="sxs-lookup"><span data-stu-id="68175-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="68175-119">Bogføringsdefinitioner for behæftelser konfigureres for modulet **Køb** på siden **Bogføringsdefinitioner**.</span><span class="sxs-lookup"><span data-stu-id="68175-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="68175-120">I området **Køb** på siden **Definitioner af posteringsbogføring** kan du derefter vælge den posteringstype for **Indkøbsordre**, der skal bruges for at knytte bogføringsdefinitionen til indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="68175-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="68175-121">Alle bilagsposteringer for indkøbsordrebehæftelser skal være afstemt (dvs. debet skal være lig med kredit) inden for hver enkelt dimension på et bilag.</span><span class="sxs-lookup"><span data-stu-id="68175-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="68175-122">Bogføringsdefinition – søgekriterier</span><span class="sxs-lookup"><span data-stu-id="68175-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="68175-123">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="68175-123">Account structure</span></span>       | <span data-ttu-id="68175-124">Sammenlign kontonummer</span><span class="sxs-lookup"><span data-stu-id="68175-124">Match account number</span></span> | <span data-ttu-id="68175-125">Prioritet </span><span class="sxs-lookup"><span data-stu-id="68175-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="68175-126">Kontostruktur – drift</span><span class="sxs-lookup"><span data-stu-id="68175-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="68175-127">1</span><span class="sxs-lookup"><span data-stu-id="68175-127">1</span></span>        |

<span data-ttu-id="68175-128"><em>En tom værdi i feltet \**Sammenlign kontonummer</em>* betyder, at alle tilsvarende konti i den definerede kontostruktur vil indgå i sammenholdningsreglen.</span><span class="sxs-lookup"><span data-stu-id="68175-128"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="68175-129">Bogføringsdefinition – genererede poster</span><span class="sxs-lookup"><span data-stu-id="68175-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="68175-130">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="68175-130">Account structure</span></span> | <span data-ttu-id="68175-131">Genereret kontonummer</span><span class="sxs-lookup"><span data-stu-id="68175-131">Generated account number</span></span>                    | <span data-ttu-id="68175-132">Genereret debet/kredit</span><span class="sxs-lookup"><span data-stu-id="68175-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="68175-133">Saldo</span><span class="sxs-lookup"><span data-stu-id="68175-133">Balance</span></span>           | <span data-ttu-id="68175-134">300143 - -(Behæftelseskonto)</span><span class="sxs-lookup"><span data-stu-id="68175-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="68175-135">Samme</span><span class="sxs-lookup"><span data-stu-id="68175-135">Same</span></span>                   |
| <span data-ttu-id="68175-136">Saldo</span><span class="sxs-lookup"><span data-stu-id="68175-136">Balance</span></span>           | <span data-ttu-id="68175-137">300144 - -(Reservér til behæftelseskonto)</span><span class="sxs-lookup"><span data-stu-id="68175-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="68175-138">Balancere</span><span class="sxs-lookup"><span data-stu-id="68175-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="68175-139">Posteringer med konti, dimensionsværdier og beløb</span><span class="sxs-lookup"><span data-stu-id="68175-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="68175-140">Konti og dimensionsværdier hentes enten fra de regnskabsfordelinger, som du angiver for en indkøbsordrelinje, eller de kommer fra de konti og dimensioner, som genereres automatisk på grundlag af standardindstillingerne for leverandører, varer, kategorier og dimensionsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="68175-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="68175-141">Konto + dimensioner</span><span class="sxs-lookup"><span data-stu-id="68175-141">Account + dimensions</span></span>           | <span data-ttu-id="68175-142">Debet</span><span class="sxs-lookup"><span data-stu-id="68175-142">Debit</span></span>  | <span data-ttu-id="68175-143">Kredit</span><span class="sxs-lookup"><span data-stu-id="68175-143">Credit</span></span> | <span data-ttu-id="68175-144">Kommentar</span><span class="sxs-lookup"><span data-stu-id="68175-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="68175-145">606400-OU\_1-OU\_3566-Uddannelse</span><span class="sxs-lookup"><span data-stu-id="68175-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="68175-146">250,00</span><span class="sxs-lookup"><span data-stu-id="68175-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="68175-147">Finansposter genereret fra bogføringsdefinitionen</span><span class="sxs-lookup"><span data-stu-id="68175-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="68175-148">Genererede finansposter oprettes til registrering af behæftelserne.</span><span class="sxs-lookup"><span data-stu-id="68175-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="68175-149">Konto + dimensioner</span><span class="sxs-lookup"><span data-stu-id="68175-149">Account + dimensions</span></span>           | <span data-ttu-id="68175-150">Debet</span><span class="sxs-lookup"><span data-stu-id="68175-150">Debit</span></span>  | <span data-ttu-id="68175-151">Kredit</span><span class="sxs-lookup"><span data-stu-id="68175-151">Credit</span></span> | <span data-ttu-id="68175-152">Kommentar</span><span class="sxs-lookup"><span data-stu-id="68175-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="68175-153">300143-OU\_1-OU\_3566-Uddannelse</span><span class="sxs-lookup"><span data-stu-id="68175-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="68175-154">250,00</span><span class="sxs-lookup"><span data-stu-id="68175-154">250.00</span></span> |        |         |
| <span data-ttu-id="68175-155">300144-OU\_1-OU\_3566-Uddannelse</span><span class="sxs-lookup"><span data-stu-id="68175-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="68175-156">250,00</span><span class="sxs-lookup"><span data-stu-id="68175-156">250.00</span></span> |         |

<span data-ttu-id="68175-157">I dette eksempel matcher enhver konto, der er del af Kontostruktur – drift kriterierne for bogføringsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="68175-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="68175-158">Når 606500-OU\_1-OU\_3566-Uddannelse evalueres, oprettes der derfor genererede poster for de konti, der er defineret for bogføringsdefinitionen i ruden **Genererede poster**.</span><span class="sxs-lookup"><span data-stu-id="68175-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="68175-159">Eksempel: Budgetdisponeringer</span><span class="sxs-lookup"><span data-stu-id="68175-159">Example: Budget appropriations</span></span>
<span data-ttu-id="68175-160">Når du aktiverer budgetdisponering ved at vælge **Aktivér budgetdisponering** på siden **Finansparametre**, skal bogføringsdefinitionerne bruges til registrering af budgetregisterposter i finans.</span><span class="sxs-lookup"><span data-stu-id="68175-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="68175-161">Når der findes en aktiv budgetstyringskonfiguration, som er aktiveret, kan der bruges bogføringsdefinitioner og posteringsbogføringsdefinitioner som et led i registreringen af poster vedrørende disponering, revision, overførsel, projekt, anlægsaktiv samt udbuds- og efterspørgselsprognoser i finans.</span><span class="sxs-lookup"><span data-stu-id="68175-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="68175-162">Hvis du vil konfigurere en bogføringsdefinition for budgetregisterposter med budgettypen **Oprindeligt budget**, hvor der er aktiveret disponeringer, kan du vælge modulet **Budget** på siden **Bogføringsdefinitioner**.</span><span class="sxs-lookup"><span data-stu-id="68175-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="68175-163">I området **Budget** på siden **Definitioner af posteringsbogføring** kan du derefter bruge budgetkoderne til at knytte bogføringsdefinitionen til budgetregisterposter med budgettypen **Oprindeligt budget**.</span><span class="sxs-lookup"><span data-stu-id="68175-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="68175-164">Når budgetdisponeringer og bogføringsdefinitioner er aktiveret, registreres budgetregisterposter for budgetstyring og i finans.</span><span class="sxs-lookup"><span data-stu-id="68175-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="68175-165">Bogføringsdefinition – søgekriterier</span><span class="sxs-lookup"><span data-stu-id="68175-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="68175-166">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="68175-166">Account structure</span></span>       | <span data-ttu-id="68175-167">Sammenlign kontonummer</span><span class="sxs-lookup"><span data-stu-id="68175-167">Match account number</span></span> | <span data-ttu-id="68175-168">Prioritet </span><span class="sxs-lookup"><span data-stu-id="68175-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="68175-169">Kontostruktur – drift</span><span class="sxs-lookup"><span data-stu-id="68175-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="68175-170">1</span><span class="sxs-lookup"><span data-stu-id="68175-170">1</span></span>        |

<span data-ttu-id="68175-171"><em>En tom værdi i feltet \**Sammenlign kontonummer</em>* betyder, at alle tilsvarende konti i den definerede kontostruktur vil indgå i sammenholdningsreglen.</span><span class="sxs-lookup"><span data-stu-id="68175-171"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="68175-172">Bogføringsdefinition – genererede poster</span><span class="sxs-lookup"><span data-stu-id="68175-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="68175-173">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="68175-173">Account structure</span></span> | <span data-ttu-id="68175-174">Genereret kontonummer</span><span class="sxs-lookup"><span data-stu-id="68175-174">Generated account number</span></span>              | <span data-ttu-id="68175-175">Genereret debet/kredit</span><span class="sxs-lookup"><span data-stu-id="68175-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="68175-176">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="68175-176">Account structure</span></span> | <span data-ttu-id="68175-177">300145 - (Forventet omsætningskonto)</span><span class="sxs-lookup"><span data-stu-id="68175-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="68175-178">Samme</span><span class="sxs-lookup"><span data-stu-id="68175-178">Same</span></span>                   |
| <span data-ttu-id="68175-179">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="68175-179">Account structure</span></span> | <span data-ttu-id="68175-180">300146 - (Disponeringskonto)</span><span class="sxs-lookup"><span data-stu-id="68175-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="68175-181">Balancere</span><span class="sxs-lookup"><span data-stu-id="68175-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="68175-182">Posteringer med konti, dimensionsværdier og beløb</span><span class="sxs-lookup"><span data-stu-id="68175-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="68175-183">Du kan angive konti, dimensionsværdier og beløb for budgetkontoposten på siden **Budgetregisterpost**.</span><span class="sxs-lookup"><span data-stu-id="68175-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="68175-184">Konto + dimensioner</span><span class="sxs-lookup"><span data-stu-id="68175-184">Account + dimensions</span></span>           | <span data-ttu-id="68175-185">Debet</span><span class="sxs-lookup"><span data-stu-id="68175-185">Debit</span></span> | <span data-ttu-id="68175-186">Kredit</span><span class="sxs-lookup"><span data-stu-id="68175-186">Credit</span></span> | <span data-ttu-id="68175-187">Kommentar</span><span class="sxs-lookup"><span data-stu-id="68175-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="68175-188">606400-OU\_1-OU\_3566-Uddannelse</span><span class="sxs-lookup"><span data-stu-id="68175-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="68175-189">250,00</span><span class="sxs-lookup"><span data-stu-id="68175-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="68175-190">Finansposter genereret fra bogføringsdefinitionen</span><span class="sxs-lookup"><span data-stu-id="68175-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="68175-191">Genererede finansposter oprettes til registrering af de oprindelige budget i hver dimension.</span><span class="sxs-lookup"><span data-stu-id="68175-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="68175-192">Konto + dimensioner</span><span class="sxs-lookup"><span data-stu-id="68175-192">Account + dimensions</span></span>           | <span data-ttu-id="68175-193">Debet</span><span class="sxs-lookup"><span data-stu-id="68175-193">Debit</span></span>  | <span data-ttu-id="68175-194">Kredit</span><span class="sxs-lookup"><span data-stu-id="68175-194">Credit</span></span> | <span data-ttu-id="68175-195">Kommentar</span><span class="sxs-lookup"><span data-stu-id="68175-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="68175-196">300145-OU\_1-OU\_3566-Uddannelse</span><span class="sxs-lookup"><span data-stu-id="68175-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="68175-197">250,00</span><span class="sxs-lookup"><span data-stu-id="68175-197">250.00</span></span> |         |
| <span data-ttu-id="68175-198">300146-OU\_1-OU\_3566-Uddannelse</span><span class="sxs-lookup"><span data-stu-id="68175-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="68175-199">250,00</span><span class="sxs-lookup"><span data-stu-id="68175-199">250.00</span></span> |        |         |

<span data-ttu-id="68175-200">I dette eksempel matcher enhver konto, der er del af Kontostruktur – drift kriterierne for bogføringsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="68175-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="68175-201">Derfor oprettes de genererede finansposter, når 606400-OU\_1-OU\_3566-Uddannelse evalueres.</span><span class="sxs-lookup"><span data-stu-id="68175-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>






