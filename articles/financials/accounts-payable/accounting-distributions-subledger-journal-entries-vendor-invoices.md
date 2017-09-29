---
title: Regnskabsfordelinger og kladdeposteringer for reskontro til kreditorfakturaer
description: "Regnskabsfordelinger bruges til at definere, hvordan et beløb skal redegøres for, f.eks. hvordan udgifter, skat eller afgifter redegøres for på en kreditorfaktura. Alle beløb, der skal tages i betragtning, når kreditorfakturaen journaliseres, har en eller flere regnskabsfordelinger."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f8169c32dc47c1635f6d3d00852d14d677678868
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---

# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a><span data-ttu-id="d633d-104">Regnskabsfordelinger og kladdeposteringer for reskontro til kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="d633d-104">Accounting distributions and subledger journal entries for vendor invoices</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d633d-105">Regnskabsfordelinger bruges til at definere, hvordan et beløb skal redegøres for, f.eks. hvordan udgifter, skat eller afgifter redegøres for på en kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="d633d-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="d633d-106">Alle beløb, der skal tages i betragtning, når kreditorfakturaen journaliseres, har en eller flere regnskabsfordelinger.</span><span class="sxs-lookup"><span data-stu-id="d633d-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="d633d-107">Regnskabsfordelinger</span><span class="sxs-lookup"><span data-stu-id="d633d-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="d633d-108">Du kan bruge følgende knapper på siden Kreditorfaktura til at få vist og eventuelt ændre regnskabsfordelingerne for hvert beløb på kreditorfakturaen.</span><span class="sxs-lookup"><span data-stu-id="d633d-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="d633d-109">**Distribuer beløb** – vis og ret de regnskabsmæssige fordelinger for en enkelt linje og evt. underordnede linjer, f.eks. skatter eller afgifter.</span><span class="sxs-lookup"><span data-stu-id="d633d-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="d633d-110">Du kan også få vist og redigere regnskabsfordelinger for den underordnede linje direkte fra siden Momstransaktioner eller siden Gebyrposter.</span><span class="sxs-lookup"><span data-stu-id="d633d-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="d633d-111">Ændre beløb i fakturahoveder, f.eks. afgifter eller valutaafrundingsbeløb.</span><span class="sxs-lookup"><span data-stu-id="d633d-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="d633d-112">Reducer linjebeløb i kreditorfakturaen.</span><span class="sxs-lookup"><span data-stu-id="d633d-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="d633d-113">**Få vist fordelinger** – Få vist regnskabsfordelingerne for alle linjer i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="d633d-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="d633d-114">Du kan ikke redigere de regnskabsmæssige fordelinger fra denne visning.</span><span class="sxs-lookup"><span data-stu-id="d633d-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="d633d-115">Få vist overskrifts- og linjebeløb.</span><span class="sxs-lookup"><span data-stu-id="d633d-115">View header and line amounts.</span></span>

<span data-ttu-id="d633d-116">Hvis kreditorfakturaen henviser til en indkøbsordre, kan du opdele og redigere regnskabfordelingerne for linjer, der indeholder en vare, der ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="d633d-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="d633d-117">Hvis kreditorfakturalinjen ikke henviser til en indkøbsordrelinje, kan du også slette en regnskabsfordeling.</span><span class="sxs-lookup"><span data-stu-id="d633d-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="d633d-118">Du kan ikke opdele eller slette linjer for afgifter, skatter og linjerabatter.</span><span class="sxs-lookup"><span data-stu-id="d633d-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="d633d-119">Du kan ændre finanskontoen, men du kan ikke ændre beløb eller procenter.</span><span class="sxs-lookup"><span data-stu-id="d633d-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="d633d-120">Hvis den overordnede linje indeholder en vare, der ikke føres på lager, og regnskabsfordelingerne er opdelt, opdeles den underordnede linje automatisk, så den svarer til de økonomiske dimensioner for den overordnede linje.</span><span class="sxs-lookup"><span data-stu-id="d633d-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="d633d-121">De regnskabsmæssige fordelinger for den underordnede linje kan ikke opdeles yderligere eller blive slettet, men afhængigt af opsætningen af den underordnede linje kan du muligvis ændre finanskontoen for regnskabsfordelingerne af den underordnede linje.</span><span class="sxs-lookup"><span data-stu-id="d633d-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="d633d-122">Fordeling af beløb</span><span class="sxs-lookup"><span data-stu-id="d633d-122">Distributing amounts</span></span>
<span data-ttu-id="d633d-123">Når du indtaster en kreditorfaktura, fordeles hvert beløb på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="d633d-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d633d-124">Type kreditorfakturalinje</span><span class="sxs-lookup"><span data-stu-id="d633d-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="d633d-125">Prioritering, der bestemmer, hvor den primære konto vises fra</span><span class="sxs-lookup"><span data-stu-id="d633d-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="d633d-126">Prioritering, der bestemmer, hvilke standard for økonomisk dimensionsværdi der vises.</span><span class="sxs-lookup"><span data-stu-id="d633d-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d633d-127">Lagerført produkt</span><span class="sxs-lookup"><span data-stu-id="d633d-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="d633d-128">Regnskabsfordeling for indkøbsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-129">Feltet Hovedkonto, når Udgifter til indkøb for produkt er markeret på siden Bogføring.</span><span class="sxs-lookup"><span data-stu-id="d633d-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="d633d-130">Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-131">Brug de finansielle standarddimensionsværdier på kreditorfakturaen.</span><span class="sxs-lookup"><span data-stu-id="d633d-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d633d-132">En indkøbskategori eller et produkt, der ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="d633d-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="d633d-133">Regnskabsfordelingen for købsordrelinjen, hvis kreditorfakturalinjen henviser til en købsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="d633d-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-134">Feltet Hovedkonto, når Udgifter til indkøb for udgift er markeret på siden Bogføring.</span><span class="sxs-lookup"><span data-stu-id="d633d-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="d633d-135">Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-136">Hvis hovedkontoen er en fordelingskonto, skal du bruge standardværdien fra definitionen af fordelingskontoen.</span><span class="sxs-lookup"><span data-stu-id="d633d-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="d633d-137">Brug de finansielle standarddimensionsværdier på kreditorfakturaen.</span><span class="sxs-lookup"><span data-stu-id="d633d-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="d633d-138">Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="d633d-139">Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</span><span class="sxs-lookup"><span data-stu-id="d633d-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d633d-140">Anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="d633d-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="d633d-141">Regnskabsfordelingen for købsordrelinjen, hvis kreditorfakturalinjen henviser til en købsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="d633d-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-142">Hvis Anskaffelse er valgt i feltet Posteringstype i formen Kreditorfaktura, feltet Hovedkonto, når Anskaffelse er markeret på profilsiden Bogføre anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="d633d-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="d633d-143">Hvis Anskaffelsesregulering er valgt i feltet Posteringstype, feltet Hovedkonto, når Anskaffelsesregulering er markeret på profilsiden Bogføre anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="d633d-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="d633d-144">Brug regnskabsfordelingen til købsordrelinjen, hvis fakturalinjen henviser til en købsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="d633d-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-145">Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="d633d-146">Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</span><span class="sxs-lookup"><span data-stu-id="d633d-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d633d-147">Projekt, der er defineret på kreditorfakturalinjen</span><span class="sxs-lookup"><span data-stu-id="d633d-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="d633d-148">Regnskabsfordelingen til købsordrelinjen, hvis fakturalinjen henviser til en købsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="d633d-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-149">Hvis Balance er valgt i feltet Bogfør omkostninger - Vare på siden Projektgrupper, feltet Hovedkonto, når Omkostning er valgt på konfigurationssiden Finanskontering.</span><span class="sxs-lookup"><span data-stu-id="d633d-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="d633d-150">Hvis Drift er valgt i feltet Bogfør omkostninger - Vare på siden Projektgrupper, feltet Hovedkonto, når Omkostning - vare er valgt på konfigurationssiden Finanskontering.</span><span class="sxs-lookup"><span data-stu-id="d633d-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="d633d-151">Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d633d-152">Linjerabat</span><span class="sxs-lookup"><span data-stu-id="d633d-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="d633d-153">Regnskabsfordelingen til købsordrelinjen, hvis fakturalinjen henviser til en købsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="d633d-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-154">Feltet Hovedkonto når, Rabat er valgt på siden Bogføring.</span><span class="sxs-lookup"><span data-stu-id="d633d-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="d633d-155">Hvis der ikke er defineret en primær konto til en rabat på posteringsprofilen, regnskabsfordelingen for den samlede pris på købsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="d633d-156">Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-157">Bruge økonomiske dimensioner fra regnskabfordelingerne for den udvidede pris på kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="d633d-158">Brug de finansielle dimensionsværdier for kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="d633d-159">Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</span><span class="sxs-lookup"><span data-stu-id="d633d-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d633d-160">Indkøbstillæg, der angives under fanen Pris og rabat på indkøbsordrelinjen</span><span class="sxs-lookup"><span data-stu-id="d633d-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="d633d-161">Regnskabsfordelingen til købsordrelinjen, hvis fakturalinjen henviser til en købsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="d633d-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-162">Regnskabsfordelinger af den udvidede pris på indkøbsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="d633d-163">Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-164">Bruge økonomiske dimensioner fra regnskabfordelingerne for den udvidede pris på kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d633d-165">Linjetillæg</span><span class="sxs-lookup"><span data-stu-id="d633d-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="d633d-166">Regnskabsfordelingen til købsordrelinjen, hvis fakturalinjen henviser til en købsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="d633d-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-167">Hvis Finanskonto er valgt i feltet Debettype i formen Gebyrkode, feltet Debetkonto på siden Gebyrkode.</span><span class="sxs-lookup"><span data-stu-id="d633d-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="d633d-168">Hvis Vare er valgt i feltet Debettype i formularen Gebyrkode, regnskabsfordelingen for den udvidede pris på indkøbsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-169">Hvis Debitor/Kreditor er valgt i feltet Debettype i formen Gebyrkode, feltet Kreditkonto på siden Gebyrkode.</span><span class="sxs-lookup"><span data-stu-id="d633d-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="d633d-170">Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-171">Bruge økonomiske dimensioner fra regnskabfordelingerne for den udvidede pris på kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="d633d-172">Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="d633d-173">Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</span><span class="sxs-lookup"><span data-stu-id="d633d-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d633d-174">Moms med følgende betingelse:</span><span class="sxs-lookup"><span data-stu-id="d633d-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="d633d-175">Indstillingen Anvend amerikanske momsregler er valgt på siden Finansparametre.</span><span class="sxs-lookup"><span data-stu-id="d633d-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="d633d-176">Regnskabsfordelingen til købsordrelinjen, hvis fakturalinjen henviser til en købsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="d633d-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-177">Regnskabsfordelingen af den udvidede pris eller gebyret.</span><span class="sxs-lookup"><span data-stu-id="d633d-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="d633d-178">Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-179">Bruge økonomiske dimensioner fra regnskabfordelingerne for den udvidede pris på kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="d633d-180">Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d633d-181">Moms med følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="d633d-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d633d-182">Indstillingen Anvend amerikanske momsregler er ikke valgt på siden Finansparametre.</span><span class="sxs-lookup"><span data-stu-id="d633d-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="d633d-183">Feltet Importmoms for momsgruppen er ikke valgt på siden Momsgrupper.</span><span class="sxs-lookup"><span data-stu-id="d633d-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="d633d-184">Hvis momsbeløbet kan refunderes, feltet Konto for indgående moms på siden Finanskonteringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="d633d-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="d633d-185">Hvis skattebeløbet ikke er refunderbart, den udvidede pris eller regnskabsfordelingen for gebyret.</span><span class="sxs-lookup"><span data-stu-id="d633d-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="d633d-186">Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-187">Brug de økonomiske dimensioner fra den udvidede pris eller regnskabsfordelingerne for gebyret på kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="d633d-188">Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="d633d-189">Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</span><span class="sxs-lookup"><span data-stu-id="d633d-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d633d-190">Moms med følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="d633d-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d633d-191">Indstillingen Anvend amerikanske momsregler er ikke valgt på siden Finansparametre.</span><span class="sxs-lookup"><span data-stu-id="d633d-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="d633d-192">Feltet Importmoms for momsgruppen er valgt på siden Momsgrupper.</span><span class="sxs-lookup"><span data-stu-id="d633d-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="d633d-193">Hvis momsbeløbet kan refunderes, feltet Konto for indgående moms på siden Finanskonteringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="d633d-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="d633d-194">Hvis momsbeløbet kan ikke refunderes, feltet Udgift for importmoms på siden Finanskonteringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="d633d-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="d633d-195">Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-196">Brug de økonomiske dimensioner fra den udvidede pris eller regnskabsfordelingerne for gebyret på kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="d633d-197">Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="d633d-198">Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</span><span class="sxs-lookup"><span data-stu-id="d633d-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d633d-199">Gebyr i overskrift</span><span class="sxs-lookup"><span data-stu-id="d633d-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="d633d-200">Hvis Finanskonto er valgt i feltet Debettype i formen Gebyrkode, feltet Debetkonto på siden Gebyrkode.</span><span class="sxs-lookup"><span data-stu-id="d633d-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="d633d-201">Hvis Debitor/Kreditor er valgt i feltet Debettype i formen Gebyrkode, feltet Kreditkonto på siden Gebyrkode.</span><span class="sxs-lookup"><span data-stu-id="d633d-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="d633d-202">Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-203">Hvis hovedkontoen er en fordelingskonto, skal du bruge standardværdien fra definitionen af fordelingskontoen.</span><span class="sxs-lookup"><span data-stu-id="d633d-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="d633d-204">Brug standardskabelonværdierne for den økonomiske dimension fra kreditorfakturahovedet.</span><span class="sxs-lookup"><span data-stu-id="d633d-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="d633d-205">Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="d633d-206">Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</span><span class="sxs-lookup"><span data-stu-id="d633d-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d633d-207">Ordrehovedrabat</span><span class="sxs-lookup"><span data-stu-id="d633d-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="d633d-208">Feltet Hovedkonto for bogføringstype Kreditor, fakturarabat på siden Konti til automatisk posteringer.</span><span class="sxs-lookup"><span data-stu-id="d633d-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="d633d-209">Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="d633d-210">Bruge økonomiske dimensioner fra regnskabfordelingerne for den udvidede pris på kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="d633d-211">Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d633d-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="d633d-212">Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</span><span class="sxs-lookup"><span data-stu-id="d633d-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

 
<a name="distributing-taxes"></a><span data-ttu-id="d633d-213">Fordeling af skatter</span><span class="sxs-lookup"><span data-stu-id="d633d-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="d633d-214">Regnskabsfordelinger for skat kan ikke oprettes, før der er beregnet skat.</span><span class="sxs-lookup"><span data-stu-id="d633d-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="d633d-215">Hvis du vil beregne moms, skal du fuldføre en af følgende opgaver på siden Kreditorfaktura:</span><span class="sxs-lookup"><span data-stu-id="d633d-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="d633d-216">Få vist fakturatotalen.</span><span class="sxs-lookup"><span data-stu-id="d633d-216">View the invoice total.</span></span>
-   <span data-ttu-id="d633d-217">Få vist momsen.</span><span class="sxs-lookup"><span data-stu-id="d633d-217">View the sales tax.</span></span>
-   <span data-ttu-id="d633d-218">Få vist reskontrokladden.</span><span class="sxs-lookup"><span data-stu-id="d633d-218">View the subledger journal.</span></span>
-   <span data-ttu-id="d633d-219">Få vist regnskabsfordelinger for den færdige kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="d633d-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="d633d-220">Sæt kreditorfakturaen på hold.</span><span class="sxs-lookup"><span data-stu-id="d633d-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="d633d-221">Bogfør kreditorfakturaen.</span><span class="sxs-lookup"><span data-stu-id="d633d-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="d633d-222">Reskontrokladder for kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="d633d-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="d633d-223">Før du bogfører en kreditorfaktura, kan du få vist den komplette regnskabspost for fakturaen, hvilket omfatter debit og kredit, for at kontrollere, at fakturaen bogføres på de rigtige konti.</span><span class="sxs-lookup"><span data-stu-id="d633d-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="d633d-224">Denne visning af hele regnskabsenheden kaldes en reskontrokladde.</span><span class="sxs-lookup"><span data-stu-id="d633d-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="d633d-225">Hvis kladdeposteringen for reskontroer er forkert, når du gennemser den før journalisering af kreditorfakturaen, kan du ikke ændre kladdeposteringen for reskontro.</span><span class="sxs-lookup"><span data-stu-id="d633d-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="d633d-226">I stedet skal du redigere de regnskabsmæssige fordelinger eller posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="d633d-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="d633d-227">De regnskabsmæssige fordelinger bruges til at definere én side af regnskabsenheden, debiteringen eller krediteringen.</span><span class="sxs-lookup"><span data-stu-id="d633d-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="d633d-228">Den modsvarende kontopost for reskontrokladde oprettes ved hjælp af posteringsprofiler, f.eks fra kreditorkontoen eller skat.</span><span class="sxs-lookup"><span data-stu-id="d633d-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>






