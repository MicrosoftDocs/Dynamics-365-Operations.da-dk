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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 004f3f24ec410d9f0e7d1e7264ec2730b9467410
ms.contentlocale: da-dk
ms.lasthandoff: 06/29/2017


---

# <a name="posting-definition-examples"></a><span data-ttu-id="b4829-103">Eksempler på bogføringsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="b4829-103">Posting definition examples</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b4829-104">Denne artikel indeholder eksempler på, hvordan bogføringsdefinitioner bruges for behæftelser i indkøbsordrer og budgetdisponeringer.</span><span class="sxs-lookup"><span data-stu-id="b4829-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="b4829-105">Inden du læser dette emne, skal du være fortrolig med bogføringsdefinitioner og posteringsbogføringsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="b4829-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="b4829-106">Du kan finde flere oplysninger i [Bogføringsdefinitioner](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="b4829-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="b4829-107">Følgende eksempler kan konfigureres på siden **Bogføringsdefinitioner**.</span><span class="sxs-lookup"><span data-stu-id="b4829-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="b4829-108">Hvert eksempel indeholder følgende områder:</span><span class="sxs-lookup"><span data-stu-id="b4829-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="b4829-109">Bogføringsdefinition – søgekriterier</span><span class="sxs-lookup"><span data-stu-id="b4829-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="b4829-110">Bogføringsdefinition – genererede poster</span><span class="sxs-lookup"><span data-stu-id="b4829-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="b4829-111">Posteringer med konti, dimensionsværdier og beløb</span><span class="sxs-lookup"><span data-stu-id="b4829-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="b4829-112">Finansposter genereret fra bogføringsdefinitionen</span><span class="sxs-lookup"><span data-stu-id="b4829-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="b4829-113">Når der er en match mellem kontiene og dimensionsværdierne i ruden **Sammenlign kriterier** for bogføringsdefinitionen og dimensionsværdierne i posteringen, genereres der finansposter med udgangspunkt i ruden **Genererede poster** for bogføringsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b4829-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="b4829-114">Knyt en bogføringsdefinition til en bestemt posteringstype ved brug af siden **Definitioner af posteringsbogføring**.</span><span class="sxs-lookup"><span data-stu-id="b4829-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="b4829-115">Efter at du har knyttet en bogføringsdefinition til en posteringstype og valgt **Brug bogføringsdefinitioner** på siden **Finansparametre**, skal alle posteringer med den valgte posteringstype bruge bogføringsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="b4829-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="b4829-116">Eksempel: Behæftelser for indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="b4829-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="b4829-117">Når du aktiverer behandling af behæftelser ved at vælge **Aktivér behæftelse** på siden **Finansparametre**, skal der bruges bogføringsposteringer til registrering af behæftelser i finans for alle konti, der skal hensættes.</span><span class="sxs-lookup"><span data-stu-id="b4829-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="b4829-118">I de fleste tilfælde hensættes alle udgiftskonti på balancen.</span><span class="sxs-lookup"><span data-stu-id="b4829-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="b4829-119">Bogføringsdefinitioner for behæftelser konfigureres for modulet **Køb** på siden **Bogføringsdefinitioner**.</span><span class="sxs-lookup"><span data-stu-id="b4829-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="b4829-120">I området **Køb** på siden **Definitioner af posteringsbogføring** kan du derefter vælge den posteringstype for **Indkøbsordre**, der skal bruges for at knytte bogføringsdefinitionen til indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="b4829-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="b4829-121">Alle bilagsposteringer for indkøbsordrebehæftelser skal være afstemt (dvs. debet skal være lig med kredit) inden for hver enkelt dimension på et bilag.</span><span class="sxs-lookup"><span data-stu-id="b4829-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="b4829-122">Bogføringsdefinition – søgekriterier</span><span class="sxs-lookup"><span data-stu-id="b4829-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="b4829-123">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="b4829-123">Account structure</span></span>       | <span data-ttu-id="b4829-124">Sammenlign kontonummer</span><span class="sxs-lookup"><span data-stu-id="b4829-124">Match account number</span></span> | <span data-ttu-id="b4829-125">Prioritet</span><span class="sxs-lookup"><span data-stu-id="b4829-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="b4829-126">Kontostruktur – drift</span><span class="sxs-lookup"><span data-stu-id="b4829-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="b4829-127">1</span><span class="sxs-lookup"><span data-stu-id="b4829-127">1</span></span>        |

<span data-ttu-id="b4829-128">*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.</span><span class="sxs-lookup"><span data-stu-id="b4829-128">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="b4829-129">Bogføringsdefinition – genererede poster</span><span class="sxs-lookup"><span data-stu-id="b4829-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="b4829-130">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="b4829-130">Account structure</span></span> | <span data-ttu-id="b4829-131">Genereret kontonummer</span><span class="sxs-lookup"><span data-stu-id="b4829-131">Generated account number</span></span>                    | <span data-ttu-id="b4829-132">Genereret debet/kredit</span><span class="sxs-lookup"><span data-stu-id="b4829-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="b4829-133">Saldo</span><span class="sxs-lookup"><span data-stu-id="b4829-133">Balance</span></span>           | <span data-ttu-id="b4829-134">300143 - -(Behæftelseskonto)</span><span class="sxs-lookup"><span data-stu-id="b4829-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="b4829-135">Samme</span><span class="sxs-lookup"><span data-stu-id="b4829-135">Same</span></span>                   |
| <span data-ttu-id="b4829-136">Saldo</span><span class="sxs-lookup"><span data-stu-id="b4829-136">Balance</span></span>           | <span data-ttu-id="b4829-137">300144 - -(Reservér til behæftelseskonto)</span><span class="sxs-lookup"><span data-stu-id="b4829-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="b4829-138">Balancere</span><span class="sxs-lookup"><span data-stu-id="b4829-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="b4829-139">Posteringer med konti, dimensionsværdier og beløb</span><span class="sxs-lookup"><span data-stu-id="b4829-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="b4829-140">Konti og dimensionsværdier hentes enten fra de regnskabsfordelinger, som du angiver for en indkøbsordrelinje, eller de kommer fra de konti og dimensioner, som genereres automatisk på grundlag af standardindstillingerne for leverandører, varer, kategorier og dimensionsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="b4829-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="b4829-141">Konto + dimensioner</span><span class="sxs-lookup"><span data-stu-id="b4829-141">Account + dimensions</span></span>           | <span data-ttu-id="b4829-142">Debet</span><span class="sxs-lookup"><span data-stu-id="b4829-142">Debit</span></span>  | <span data-ttu-id="b4829-143">Kredit</span><span class="sxs-lookup"><span data-stu-id="b4829-143">Credit</span></span> | <span data-ttu-id="b4829-144">Kommentar</span><span class="sxs-lookup"><span data-stu-id="b4829-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="b4829-145">606400-OU\_1-OU\_3566-Uddannelse</span><span class="sxs-lookup"><span data-stu-id="b4829-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="b4829-146">250,00</span><span class="sxs-lookup"><span data-stu-id="b4829-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="b4829-147">Finansposter genereret fra bogføringsdefinitionen</span><span class="sxs-lookup"><span data-stu-id="b4829-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="b4829-148">Genererede finansposter oprettes til registrering af behæftelserne.</span><span class="sxs-lookup"><span data-stu-id="b4829-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="b4829-149">Konto + dimensioner</span><span class="sxs-lookup"><span data-stu-id="b4829-149">Account + dimensions</span></span>           | <span data-ttu-id="b4829-150">Debet</span><span class="sxs-lookup"><span data-stu-id="b4829-150">Debit</span></span>  | <span data-ttu-id="b4829-151">Kredit</span><span class="sxs-lookup"><span data-stu-id="b4829-151">Credit</span></span> | <span data-ttu-id="b4829-152">Kommentar</span><span class="sxs-lookup"><span data-stu-id="b4829-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="b4829-153">300143-OU\_1-OU\_3566-Uddannelse</span><span class="sxs-lookup"><span data-stu-id="b4829-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="b4829-154">250,00</span><span class="sxs-lookup"><span data-stu-id="b4829-154">250.00</span></span> |        |         |
| <span data-ttu-id="b4829-155">300144-OU\_1-OU\_3566-Uddannelse</span><span class="sxs-lookup"><span data-stu-id="b4829-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="b4829-156">250,00</span><span class="sxs-lookup"><span data-stu-id="b4829-156">250.00</span></span> |         |

<span data-ttu-id="b4829-157">I dette eksempel matcher enhver konto, der er del af Kontostruktur – drift kriterierne for bogføringsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b4829-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="b4829-158">Når 606500-OU\_1-OU\_3566-Uddannelse evalueres, oprettes der derfor genererede poster for de konti, der er defineret for bogføringsdefinitionen i ruden **Genererede poster**.</span><span class="sxs-lookup"><span data-stu-id="b4829-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="b4829-159">Eksempel: Budgetdisponeringer</span><span class="sxs-lookup"><span data-stu-id="b4829-159">Example: Budget appropriations</span></span>
<span data-ttu-id="b4829-160">Når du aktiverer budgetdisponering ved at vælge **Aktivér budgetdisponering** på siden **Finansparametre**, skal bogføringsdefinitionerne bruges til registrering af budgetregisterposter i finans.</span><span class="sxs-lookup"><span data-stu-id="b4829-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="b4829-161">Når der findes en aktiv budgetstyringskonfiguration, som er aktiveret, kan der bruges bogføringsdefinitioner og posteringsbogføringsdefinitioner som et led i registreringen af poster vedrørende disponering, revision, overførsel, projekt, anlægsaktiv samt udbuds- og efterspørgselsprognoser i finans.</span><span class="sxs-lookup"><span data-stu-id="b4829-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="b4829-162">Hvis du vil konfigurere en bogføringsdefinition for budgetregisterposter med budgettypen **Oprindeligt budget**, hvor der er aktiveret disponeringer, kan du vælge modulet **Budget** på siden **Bogføringsdefinitioner**.</span><span class="sxs-lookup"><span data-stu-id="b4829-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="b4829-163">I området **Budget** på siden **Definitioner af posteringsbogføring** kan du derefter bruge budgetkoderne til at knytte bogføringsdefinitionen til budgetregisterposter med budgettypen **Oprindeligt budget**.</span><span class="sxs-lookup"><span data-stu-id="b4829-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="b4829-164">Når budgetdisponeringer og bogføringsdefinitioner er aktiveret, registreres budgetregisterposter for budgetstyring og i finans.</span><span class="sxs-lookup"><span data-stu-id="b4829-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="b4829-165">Bogføringsdefinition – søgekriterier</span><span class="sxs-lookup"><span data-stu-id="b4829-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="b4829-166">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="b4829-166">Account structure</span></span>       | <span data-ttu-id="b4829-167">Sammenlign kontonummer</span><span class="sxs-lookup"><span data-stu-id="b4829-167">Match account number</span></span> | <span data-ttu-id="b4829-168">Prioritet</span><span class="sxs-lookup"><span data-stu-id="b4829-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="b4829-169">Kontostruktur – drift</span><span class="sxs-lookup"><span data-stu-id="b4829-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="b4829-170">1</span><span class="sxs-lookup"><span data-stu-id="b4829-170">1</span></span>        |

<span data-ttu-id="b4829-171">*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.</span><span class="sxs-lookup"><span data-stu-id="b4829-171">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="b4829-172">Bogføringsdefinition – genererede poster</span><span class="sxs-lookup"><span data-stu-id="b4829-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="b4829-173">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="b4829-173">Account structure</span></span> | <span data-ttu-id="b4829-174">Genereret kontonummer</span><span class="sxs-lookup"><span data-stu-id="b4829-174">Generated account number</span></span>              | <span data-ttu-id="b4829-175">Genereret debet/kredit</span><span class="sxs-lookup"><span data-stu-id="b4829-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="b4829-176">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="b4829-176">Account structure</span></span> | <span data-ttu-id="b4829-177">300145 - (Forventet omsætningskonto)</span><span class="sxs-lookup"><span data-stu-id="b4829-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="b4829-178">Samme</span><span class="sxs-lookup"><span data-stu-id="b4829-178">Same</span></span>                   |
| <span data-ttu-id="b4829-179">Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="b4829-179">Account structure</span></span> | <span data-ttu-id="b4829-180">300146 - (Disponeringskonto)</span><span class="sxs-lookup"><span data-stu-id="b4829-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="b4829-181">Balancere</span><span class="sxs-lookup"><span data-stu-id="b4829-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="b4829-182">Posteringer med konti, dimensionsværdier og beløb</span><span class="sxs-lookup"><span data-stu-id="b4829-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="b4829-183">Du kan angive konti, dimensionsværdier og beløb for budgetkontoposten på siden **Budgetregisterpost**.</span><span class="sxs-lookup"><span data-stu-id="b4829-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="b4829-184">Konto + dimensioner</span><span class="sxs-lookup"><span data-stu-id="b4829-184">Account + dimensions</span></span>           | <span data-ttu-id="b4829-185">Debet</span><span class="sxs-lookup"><span data-stu-id="b4829-185">Debit</span></span> | <span data-ttu-id="b4829-186">Kredit</span><span class="sxs-lookup"><span data-stu-id="b4829-186">Credit</span></span> | <span data-ttu-id="b4829-187">Kommentar</span><span class="sxs-lookup"><span data-stu-id="b4829-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="b4829-188">606400-OU\_1-OU\_3566-Uddannelse</span><span class="sxs-lookup"><span data-stu-id="b4829-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="b4829-189">250,00</span><span class="sxs-lookup"><span data-stu-id="b4829-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="b4829-190">Finansposter genereret fra bogføringsdefinitionen</span><span class="sxs-lookup"><span data-stu-id="b4829-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="b4829-191">Genererede finansposter oprettes til registrering af de oprindelige budget i hver dimension.</span><span class="sxs-lookup"><span data-stu-id="b4829-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="b4829-192">Konto + dimensioner</span><span class="sxs-lookup"><span data-stu-id="b4829-192">Account + dimensions</span></span>           | <span data-ttu-id="b4829-193">Debet</span><span class="sxs-lookup"><span data-stu-id="b4829-193">Debit</span></span>  | <span data-ttu-id="b4829-194">Kredit</span><span class="sxs-lookup"><span data-stu-id="b4829-194">Credit</span></span> | <span data-ttu-id="b4829-195">Kommentar</span><span class="sxs-lookup"><span data-stu-id="b4829-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="b4829-196">300145-OU\_1-OU\_3566-Uddannelse</span><span class="sxs-lookup"><span data-stu-id="b4829-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="b4829-197">250,00</span><span class="sxs-lookup"><span data-stu-id="b4829-197">250.00</span></span> |         |
| <span data-ttu-id="b4829-198">300146-OU\_1-OU\_3566-Uddannelse</span><span class="sxs-lookup"><span data-stu-id="b4829-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="b4829-199">250,00</span><span class="sxs-lookup"><span data-stu-id="b4829-199">250.00</span></span> |        |         |

<span data-ttu-id="b4829-200">I dette eksempel matcher enhver konto, der er del af Kontostruktur – drift kriterierne for bogføringsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b4829-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="b4829-201">Derfor oprettes de genererede finansposter, når 606400-OU\_1-OU\_3566-Uddannelse evalueres.</span><span class="sxs-lookup"><span data-stu-id="b4829-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>






