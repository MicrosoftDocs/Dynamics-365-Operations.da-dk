---
title: Nummerserier
description: "Talserier bruges til generering af læselige, entydige identifikatorer for masterdataposter og transaktionsposter, der kræver identifikatorer."
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: NumberSequenceTableListPage, NumberSequenceConfiguration
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a290f6f453d8440d6e68a13915339d3da31d959a
ms.openlocfilehash: 353113d7c7341eab567224a0d3508f6fdb7bdcec
ms.contentlocale: da-dk
ms.lasthandoff: 04/03/2018

---

# <a name="number-sequences"></a><span data-ttu-id="cb03b-103">Nummerserier</span><span class="sxs-lookup"><span data-stu-id="cb03b-103">Number sequences</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cb03b-104">Talserier bruges til generering af læselige, entydige identifikatorer for masterdataposter og transaktionsposter, der kræver identifikatorer.</span><span class="sxs-lookup"><span data-stu-id="cb03b-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="cb03b-105">En masterdatapost eller transaktionspost, der kræver et id, kaldes en *reference*.</span><span class="sxs-lookup"><span data-stu-id="cb03b-105">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span>

<span data-ttu-id="cb03b-106">Før du kan oprette nye poster for en reference, skal du konfigurere en nummerserie og knytte den til referencen.</span><span class="sxs-lookup"><span data-stu-id="cb03b-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="cb03b-107">Det anbefales, at du bruger de sider, der findes i **Virksomhedsadministration**, til at konfigurere nummerserier.</span><span class="sxs-lookup"><span data-stu-id="cb03b-107">We recommend that you use the pages in **Organization administration** to set up number sequences.</span></span> <span data-ttu-id="cb03b-108">Hvis der kræves modulspecifikke indstillinger, kan du bruge parametersiden i et modul til at angive nummerserier for referencen i det pågældende modul.</span><span class="sxs-lookup"><span data-stu-id="cb03b-108">If module-specific settings are required, you can use the parameters page in a module to specify number sequences for the references in that module.</span></span> <span data-ttu-id="cb03b-109">I **Debitor** og **Kreditor** kan du f.eks. konfigurere nummerseriegrupper, hvis du vil tildele specifikke nummerserier til specifikke debitorer eller kreditorer.</span><span class="sxs-lookup"><span data-stu-id="cb03b-109">For example, in **Accounts receivable** and **Accounts payable**, you can set up number sequence groups to allocate specific number sequences to specific customers or vendors.</span></span> 

<span data-ttu-id="cb03b-110">Når du konfigurerer en nummerserie, skal du angive et område, som definerer, hvilken organisation der bruger nummerserien.</span><span class="sxs-lookup"><span data-stu-id="cb03b-110">When you set up a number sequence, you must specify a scope, which defines which organization uses the number sequence.</span></span> <span data-ttu-id="cb03b-111">Området kan være **Delt**, **Firma**, **Juridisk enhed** eller **Driftsenhed**.</span><span class="sxs-lookup"><span data-stu-id="cb03b-111">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="cb03b-112">Områderne **Juridisk enhed** og **Firma** kan også kombineres med **Regnskabskalenderperiode**, så der oprettes endnu mere specifikke nummerserier.</span><span class="sxs-lookup"><span data-stu-id="cb03b-112">**Legal entity** and **Company** scopes can be combined with **Fiscal calendar period** to create even more specific number sequences.</span></span> 

<span data-ttu-id="cb03b-113">Nummerserieformater består af segmenter.</span><span class="sxs-lookup"><span data-stu-id="cb03b-113">Number sequence formats consist of segments.</span></span> <span data-ttu-id="cb03b-114">Nummerserier med et andet område end **Delt** kan indeholde segmenter, der svarer til området.</span><span class="sxs-lookup"><span data-stu-id="cb03b-114">Number sequences with a scope other than **Shared** can contain segments that correspond to the scope.</span></span> <span data-ttu-id="cb03b-115">En nummerserie med området **Juridisk enhed** kan f.eks. indeholde et segment for en juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="cb03b-115">For example, a number sequence with a scope of **Legal entity** can contain a legal entity segment.</span></span> <span data-ttu-id="cb03b-116">Hvis du medtager et områdesegment i nummerserieformatet, kan du identificere området for en specifik post ved at se på postens nummer.</span><span class="sxs-lookup"><span data-stu-id="cb03b-116">By including a scope segment in the number sequence format, you can identify the scope of a particular record by looking at its number.</span></span> 

<span data-ttu-id="cb03b-117">Udover segmenter, der svarer til områder, kan nummerserieformater indeholde segmenter af typen **Konstant** og **Alfanumerisk**.</span><span class="sxs-lookup"><span data-stu-id="cb03b-117">In addition to segments that correspond to scopes, number sequence formats can contain **Constant** and **Alphanumeric segments**.</span></span> <span data-ttu-id="cb03b-118">Et **Konstant** segment indeholder et sæt af bogstaver, tal eller tegn, der ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="cb03b-118">A **Constant** segment contains a set of letters, numbers, or symbols that does not change.</span></span> <span data-ttu-id="cb03b-119">Et **Alfanumerisk** segment indeholder et sæt af bogstaver eller tal, hvis værdi øges, hver gang der bruges et tal.</span><span class="sxs-lookup"><span data-stu-id="cb03b-119">An **Alphanumeric** segment contains a set of letters or numbers that increment every time that a number is used.</span></span> <span data-ttu-id="cb03b-120">Brug et taltegn (\#) for at angive stigende tal, og tegnet & for stigende bogstaver.</span><span class="sxs-lookup"><span data-stu-id="cb03b-120">Use a number sign (\#) to represent incrementing numbers and an ampersand (&) to represent incrementing letters.</span></span> <span data-ttu-id="cb03b-121">Formatet \#\#\#\#\#\_2017 giver f.eks. serien 00001\_2017, 00002\_2017 osv.</span><span class="sxs-lookup"><span data-stu-id="cb03b-121">For example, the format \#\#\#\#\#\_2017 creates the sequence 00001\_2017, 00002\_2017, and so on.</span></span>

<a name="number-sequence-examples"></a><span data-ttu-id="cb03b-122">Eksempler på nummerserier</span><span class="sxs-lookup"><span data-stu-id="cb03b-122">Number sequence examples</span></span>
------------------------

<span data-ttu-id="cb03b-123">I følgende eksempler vises det, hvordan segmenter bruges til oprettelse af nummerserieformater.</span><span class="sxs-lookup"><span data-stu-id="cb03b-123">The following examples show how to use segments to create number sequence formats.</span></span> <span data-ttu-id="cb03b-124">Eksemplerne viser nærmere bestemt virkningerne af at bruge områdesegmenter.</span><span class="sxs-lookup"><span data-stu-id="cb03b-124">In particular, the examples demonstrate the effects of using scope segments.</span></span>

### <a name="expense-report-numbers"></a><span data-ttu-id="cb03b-125">Udgiftsrapportnumre</span><span class="sxs-lookup"><span data-stu-id="cb03b-125">Expense report numbers</span></span>

<span data-ttu-id="cb03b-126">I det følgende eksempel konfigureres der udgiftsrapportnumre for den juridiske enhed med navnet **CS**.</span><span class="sxs-lookup"><span data-stu-id="cb03b-126">In the following example, expense report numbers are set up for the legal entity that is titled **CS**.</span></span> 

- <span data-ttu-id="cb03b-127">**Område:** Rejser og udgifter</span><span class="sxs-lookup"><span data-stu-id="cb03b-127">**Area:** Travel and expense</span></span> 
- <span data-ttu-id="cb03b-128">**Reference:** Udgiftsrapportnummer</span><span class="sxs-lookup"><span data-stu-id="cb03b-128">**Reference:** Expense report number</span></span> 
- <span data-ttu-id="cb03b-129">**Omfang:** Juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="cb03b-129">**Scope:** Legal entity</span></span> 
- <span data-ttu-id="cb03b-130">**Juridisk enhed:** CS</span><span class="sxs-lookup"><span data-stu-id="cb03b-130">**Legal entity:** CS</span></span>

| <span data-ttu-id="cb03b-131">Segmenter</span><span class="sxs-lookup"><span data-stu-id="cb03b-131">Segments</span></span>  | <span data-ttu-id="cb03b-132">Segmenttype</span><span class="sxs-lookup"><span data-stu-id="cb03b-132">Segment type</span></span> | <span data-ttu-id="cb03b-133">Værdi</span><span class="sxs-lookup"><span data-stu-id="cb03b-133">Value</span></span>     |
|-----------|--------------|-----------|
| <span data-ttu-id="cb03b-134">Segment 1</span><span class="sxs-lookup"><span data-stu-id="cb03b-134">Segment 1</span></span> | <span data-ttu-id="cb03b-135">Juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="cb03b-135">Legal entity</span></span> | <span data-ttu-id="cb03b-136">CS</span><span class="sxs-lookup"><span data-stu-id="cb03b-136">CS</span></span>        |
| <span data-ttu-id="cb03b-137">Segment 2</span><span class="sxs-lookup"><span data-stu-id="cb03b-137">Segment 2</span></span> | <span data-ttu-id="cb03b-138">Konstant</span><span class="sxs-lookup"><span data-stu-id="cb03b-138">Constant</span></span>     | <span data-ttu-id="cb03b-139">-UDGIFT-</span><span class="sxs-lookup"><span data-stu-id="cb03b-139">-EXPENSE-</span></span> |
| <span data-ttu-id="cb03b-140">Segment 3</span><span class="sxs-lookup"><span data-stu-id="cb03b-140">Segment 3</span></span> | <span data-ttu-id="cb03b-141">Alfanumerisk</span><span class="sxs-lookup"><span data-stu-id="cb03b-141">Alphanumeric</span></span> | \#\#\#\#  |

<span data-ttu-id="cb03b-142">**Eksempel på formateret nummer**: CS-UDGIFT-0039</span><span class="sxs-lookup"><span data-stu-id="cb03b-142">**Example of formatted number**: CS-EXPENSE-0039</span></span> 

<span data-ttu-id="cb03b-143">Du kan konfigurere et lignende nummerserieformat til andre juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="cb03b-143">You can set up a similar number sequence format for other legal entities.</span></span> <span data-ttu-id="cb03b-144">Hvis du f.eks. kun ændrer værdien af segmentet juridisk enhed for den juridiske enhed **RW**, vil det formaterede nummer være RW-UDGIFT-0039.</span><span class="sxs-lookup"><span data-stu-id="cb03b-144">For example, for a legal entity that is named **RW**, if you change only the value of the legal entity segment, the formatted number is RW-EXPENSE-0039.</span></span> <span data-ttu-id="cb03b-145">Du kan også ændre hele nummerserieformatet for andre juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="cb03b-145">You can also change the whole number sequence format for other legal entities.</span></span> <span data-ttu-id="cb03b-146">Du kan f.eks. udelade området juridisk enhed, så der oprettes et formateret nummer som f.eks. Udg-0001.</span><span class="sxs-lookup"><span data-stu-id="cb03b-146">For example, you can omit the legal entity scope segment to create a formatted number such as Exp-0001.</span></span>

### <a name="sales-order-numbers"></a><span data-ttu-id="cb03b-147">Salgsordrenumre</span><span class="sxs-lookup"><span data-stu-id="cb03b-147">Sales order numbers</span></span>

<span data-ttu-id="cb03b-148">I følgende eksempel konfigureres der salgsordrenumre for firma-id'et **CEU**.</span><span class="sxs-lookup"><span data-stu-id="cb03b-148">In the following example, sales order numbers are set up for the company ID **CEU**.</span></span> 

- <span data-ttu-id="cb03b-149">**Område:** Salg</span><span class="sxs-lookup"><span data-stu-id="cb03b-149">**Area:** Sales</span></span> 
- <span data-ttu-id="cb03b-150">**Reference:** Salgsordre</span><span class="sxs-lookup"><span data-stu-id="cb03b-150">**Reference:** Sales order</span></span> 
- <span data-ttu-id="cb03b-151">**Omfang:** Firma</span><span class="sxs-lookup"><span data-stu-id="cb03b-151">**Scope:** Company</span></span> 
- <span data-ttu-id="cb03b-152">**Firma:** CEU</span><span class="sxs-lookup"><span data-stu-id="cb03b-152">**Company:** CEU</span></span>

| <span data-ttu-id="cb03b-153">Segmenter</span><span class="sxs-lookup"><span data-stu-id="cb03b-153">Segments</span></span>  | <span data-ttu-id="cb03b-154">Segmenttype</span><span class="sxs-lookup"><span data-stu-id="cb03b-154">Segment type</span></span> | <span data-ttu-id="cb03b-155">Værdi</span><span class="sxs-lookup"><span data-stu-id="cb03b-155">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="cb03b-156">Segment 1</span><span class="sxs-lookup"><span data-stu-id="cb03b-156">Segment 1</span></span> | <span data-ttu-id="cb03b-157">Konstant</span><span class="sxs-lookup"><span data-stu-id="cb03b-157">Constant</span></span>     | <span data-ttu-id="cb03b-158">SO-</span><span class="sxs-lookup"><span data-stu-id="cb03b-158">SO-</span></span>      |
| <span data-ttu-id="cb03b-159">Segment 2</span><span class="sxs-lookup"><span data-stu-id="cb03b-159">Segment 2</span></span> | <span data-ttu-id="cb03b-160">Alfanumerisk</span><span class="sxs-lookup"><span data-stu-id="cb03b-160">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="cb03b-161">**Eksempel på formateret nummer**: SO-0029</span><span class="sxs-lookup"><span data-stu-id="cb03b-161">**Example of formatted number**: SO-0029</span></span> 

<span data-ttu-id="cb03b-162">Selvom der ikke er angivet et områdesegment, genstartes nummereringen for hvert firma-id.</span><span class="sxs-lookup"><span data-stu-id="cb03b-162">Even though a scope segment is not included in the format, numbering restarts for each company ID.</span></span> <span data-ttu-id="cb03b-163">Hvis du bruger samme format for alle firma-id'er, bruges de samme numre i hvert firma.</span><span class="sxs-lookup"><span data-stu-id="cb03b-163">If you use the same format for all company IDs, the same numbers are used in each company.</span></span> <span data-ttu-id="cb03b-164">Salgsordrenummeret SO-0029 kan f.eks. bruges i hvert firma.</span><span class="sxs-lookup"><span data-stu-id="cb03b-164">For example, sales order number SO-0029 is used in each company.</span></span> <span data-ttu-id="cb03b-165">Du kan også ændre hele nummerserieformatet for andre firma-id'er.</span><span class="sxs-lookup"><span data-stu-id="cb03b-165">You can also change the whole number sequence format for other company IDs.</span></span>

### <a name="purchase-requisition-numbers"></a><span data-ttu-id="cb03b-166">Indkøbsrekvisitionsnumre</span><span class="sxs-lookup"><span data-stu-id="cb03b-166">Purchase requisition numbers</span></span>

<span data-ttu-id="cb03b-167">I det følgende eksempel gælder indkøbsrekvisitionsnumre for hele organisationen.</span><span class="sxs-lookup"><span data-stu-id="cb03b-167">In the following example, purchase requisition numbers are organization-wide.</span></span> 

- <span data-ttu-id="cb03b-168">**Område:** Indkøb</span><span class="sxs-lookup"><span data-stu-id="cb03b-168">**Area:** Purchase</span></span> 
- <span data-ttu-id="cb03b-169">**Reference:** Indkøbsrekvisition</span><span class="sxs-lookup"><span data-stu-id="cb03b-169">**Reference:** Purchase requisition</span></span> 
- <span data-ttu-id="cb03b-170">**Omfang:** Delt</span><span class="sxs-lookup"><span data-stu-id="cb03b-170">**Scope:** Shared</span></span>

| <span data-ttu-id="cb03b-171">Segmenter</span><span class="sxs-lookup"><span data-stu-id="cb03b-171">Segments</span></span>  | <span data-ttu-id="cb03b-172">Segmenttype</span><span class="sxs-lookup"><span data-stu-id="cb03b-172">Segment type</span></span> | <span data-ttu-id="cb03b-173">Værdi</span><span class="sxs-lookup"><span data-stu-id="cb03b-173">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="cb03b-174">Segment 1</span><span class="sxs-lookup"><span data-stu-id="cb03b-174">Segment 1</span></span> | <span data-ttu-id="cb03b-175">Konstant</span><span class="sxs-lookup"><span data-stu-id="cb03b-175">Constant</span></span>     | <span data-ttu-id="cb03b-176">Rek</span><span class="sxs-lookup"><span data-stu-id="cb03b-176">Req</span></span>      |
| <span data-ttu-id="cb03b-177">Segment 2</span><span class="sxs-lookup"><span data-stu-id="cb03b-177">Segment 2</span></span> | <span data-ttu-id="cb03b-178">Alfanumerisk</span><span class="sxs-lookup"><span data-stu-id="cb03b-178">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="cb03b-179">**Eksempel på formateret nummer**: Req0052</span><span class="sxs-lookup"><span data-stu-id="cb03b-179">**Example of formatted number**: Req0052</span></span> 

<span data-ttu-id="cb03b-180">Da omfanget er **Delt**, bruges nummerserieformatet i hele organisationen.</span><span class="sxs-lookup"><span data-stu-id="cb03b-180">Because the scope is **Shared**, the number sequence format is used across the organization.</span></span> <span data-ttu-id="cb03b-181">Du kan ikke konfigurere forskellige nummerserieformater for forskellige dele af organisationen.</span><span class="sxs-lookup"><span data-stu-id="cb03b-181">You cannot set up different number sequence formats for different parts of the organization.</span></span> 

<a name="performance-considerations-for-number-sequences"></a><span data-ttu-id="cb03b-182">Overvejelser vedrørende ydeevne for nummerserier</span><span class="sxs-lookup"><span data-stu-id="cb03b-182">Performance considerations for number sequences</span></span>
-----------------------------------------------

<span data-ttu-id="cb03b-183">Overvej følgende oplysninger, som vedrører, hvordan konfigurationen af nummerserier kan påvirke systemets ydeevne, før du konfigurerer nummerserier.</span><span class="sxs-lookup"><span data-stu-id="cb03b-183">Consider the following information about how the configuration of number sequences can affect system performance before you set up number sequences.</span></span>

### <a name="continuous-and-non-continuous-number-sequences"></a><span data-ttu-id="cb03b-184">Fortløbende og ikke-fortløbende nummerserier</span><span class="sxs-lookup"><span data-stu-id="cb03b-184">Continuous and non-continuous number sequences</span></span>

<span data-ttu-id="cb03b-185">Nummerserier kan være fortløbende eller ikke-fortløbende.</span><span class="sxs-lookup"><span data-stu-id="cb03b-185">Number sequences can be continuous or non-continuous.</span></span> <span data-ttu-id="cb03b-186">En fortløbende nummerserie springer ingen numre over, men numrene vil muligvis ikke blive brugt i rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="cb03b-186">A continuous number sequence does not skip any numbers, but numbers may not be used sequentially.</span></span> <span data-ttu-id="cb03b-187">Numre fra en ikke-fortløbende nummerserie bruges i rækkefølge, men nummerserien kan springe numre over.</span><span class="sxs-lookup"><span data-stu-id="cb03b-187">Numbers from a non-continuous number sequence are used sequentially, but the number sequence may skip numbers.</span></span> <span data-ttu-id="cb03b-188">Hvis f.eks. en bruger annullerer en postering, genereres der et nummer, men det bruges ikke.</span><span class="sxs-lookup"><span data-stu-id="cb03b-188">For example, if a user cancels a transaction, a number is generated, but not used.</span></span> <span data-ttu-id="cb03b-189">I en fortløbende nummerserie, vil dette nummer blive brugt igen senere.</span><span class="sxs-lookup"><span data-stu-id="cb03b-189">In a continuous number sequence, that number is recycled later.</span></span> <span data-ttu-id="cb03b-190">I en ikke-fortløbende nummerserie bruges nummeret ikke.</span><span class="sxs-lookup"><span data-stu-id="cb03b-190">In a non-continuous number sequence, the number is not used.</span></span> 

<span data-ttu-id="cb03b-191">Fortløbende nummerserier er typisk påkrævet for eksterne dokumenter, som f.eks. indkøbsordrer, salgsordrer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="cb03b-191">Continuous number sequences are typically required for external documents, such as purchase orders, sales orders, and invoices.</span></span> <span data-ttu-id="cb03b-192">Dog kan forløbende nummerserier have alvorlig indvirkning på systemets svartider, fordi systemet skal anmode om et nummer fra databasen, hver gang der oprettes et nyt dokument eller en ny post.</span><span class="sxs-lookup"><span data-stu-id="cb03b-192">However, continuous number sequences can adversely affect system response times because the system must request a number from the database every time that a new document or record is created.</span></span> 

<span data-ttu-id="cb03b-193">Hvis du bruger en ikke-fortløbende nummerserie, kan du aktivere **Forudallokering** i oversigtspanelet **Ydeevne** på siden **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="cb03b-193">If you use a non-continuous number sequence, you can enable **Preallocation** on the **Performance** FastTab of the **Number sequences** page.</span></span> <span data-ttu-id="cb03b-194">Når du angiver et antal numre, der skal forudallokeres, vælger systemet disse numre og gemmer dem i hukommelsen.</span><span class="sxs-lookup"><span data-stu-id="cb03b-194">When you specify a quantity of numbers to preallocate, the system selects those numbers and stores them in memory.</span></span> <span data-ttu-id="cb03b-195">Der anmodes kun om nye numre fra databasen, når den forudallokerede mængde numre er brugt op.</span><span class="sxs-lookup"><span data-stu-id="cb03b-195">New numbers are requested from the database only after the preallocated quantity has been used.</span></span> 

<span data-ttu-id="cb03b-196">Hvis ikke der er lovmæssige krav, der foreskriver brug af fortløbende nummerserier, anbefales det, at du bruger ikke-forløbende nummerserier for at opnå bedre ydeevne.</span><span class="sxs-lookup"><span data-stu-id="cb03b-196">Unless there is a regulatory requirement that you use continuous number sequences, we recommend that you use non-continuous number sequences for better performance.</span></span>

### <a name="automatic-cleanup-of-number-sequences"></a><span data-ttu-id="cb03b-197">Automatisk oprydning af nummerserier</span><span class="sxs-lookup"><span data-stu-id="cb03b-197">Automatic cleanup of number sequences</span></span>

<span data-ttu-id="cb03b-198">Hvis der opstår strømafbrydelse, programfejl eller anden uventet defekt, kan systemet ikke automatisk genbruge numre til fortløbende nummerserier.</span><span class="sxs-lookup"><span data-stu-id="cb03b-198">In case of a power failure, an application error, or other unexpected failure, the system cannot recycle numbers automatically for continuous number sequences.</span></span> <span data-ttu-id="cb03b-199">Du kan køre oprydningsprocessen manuelt eller automatisk for at finde de tabte numre.</span><span class="sxs-lookup"><span data-stu-id="cb03b-199">You can run the cleanup process manually or automatically to recover the lost numbers.</span></span> 

<span data-ttu-id="cb03b-200">Husk at tage serverbelastningen i betragtning, når du planlægger oprydningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="cb03b-200">Carefully consider server usage when you plan the cleanup process.</span></span> <span data-ttu-id="cb03b-201">Det anbefales, at du udfører oprydningen som et batchjob uden for spidsbelastningstidspunkter.</span><span class="sxs-lookup"><span data-stu-id="cb03b-201">We recommend that you perform the cleanup as a batch job during non-peak hours.</span></span>






