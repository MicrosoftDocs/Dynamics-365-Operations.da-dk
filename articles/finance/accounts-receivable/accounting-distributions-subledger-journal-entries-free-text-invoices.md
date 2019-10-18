---
title: Regnskabsfordelinger og kladdeposteringer for reskontro til fritekstfakturaer
description: Regnskabsfordelinger bruges til at definere, hvordan et beløb skal redegøres for, f.eks. hvordan indtægt, skat eller afgifter redegøres for på en fritekstfaktura. Alle beløb, der skal tages redegøres for, når fritekstfakturaen journaliseres, har en eller flere regnskabsfordelinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 515d0a9c35507fad04b776e1f0b6225ac5a162d3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189240"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a><span data-ttu-id="4e4d2-104">Regnskabsfordelinger og kladdeposteringer for reskontro til fritekstfakturaer</span><span class="sxs-lookup"><span data-stu-id="4e4d2-104">Accounting distributions and subledger journal entries for free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e4d2-105">Regnskabsfordelinger bruges til at definere, hvordan et beløb skal redegøres for, f.eks. hvordan indtægt, skat eller afgifter redegøres for på en fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="4e4d2-106">Alle beløb, der skal tages redegøres for, når fritekstfakturaen journaliseres, har en eller flere regnskabsfordelinger.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="4e4d2-107">Regnskabsfordelinger</span><span class="sxs-lookup"><span data-stu-id="4e4d2-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="4e4d2-108">Du kan bruge følgende knapper på siden Fritekstfaktura til at få vist og eventuelt ændre regnskabsfordelingerne for hvert beløb på fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="4e4d2-109">**Distribuer beløb** – Vis og ret de regnskabsmæssige fordelinger for en enkelt linje og evt. underordnede linjer, f.eks. skatter eller afgifter.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="4e4d2-110">Du kan også få vist og redigere regnskabsfordelinger for den underordnede linje direkte fra siden Momstransaktioner eller siden Gebyrposter.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="4e4d2-111">Ret overskriftsbeløb i fritekstfakturaer, f.eks. afgifter eller valutaafrundingsbeløb.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="4e4d2-112">Ret linjebeløb i fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="4e4d2-113">**Få vist fordelinger** – Få vist regnskabsfordelingerne for alle linjer i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="4e4d2-114">Du kan ikke redigere de regnskabsmæssige fordelinger fra denne visning.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="4e4d2-115">Få vist overskrifts- og linjebeløb.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="4e4d2-116">Fordeling af beløb</span><span class="sxs-lookup"><span data-stu-id="4e4d2-116">Distributing amounts</span></span>
<span data-ttu-id="4e4d2-117">Når du indtaster en fritekstfaktura, fordeles hvert beløb på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4e4d2-118">Type pengebeløb</span><span class="sxs-lookup"><span data-stu-id="4e4d2-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="4e4d2-119">Hvor hovedkontoen vises fra</span><span class="sxs-lookup"><span data-stu-id="4e4d2-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="4e4d2-120">Prioritering, der bestemmer, hvilke standard for økonomisk dimensionsværdi der vises.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4e4d2-121">Linje i fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="4e4d2-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="4e4d2-122">Finanskontoen på fritekstfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="4e4d2-123">Hvis hovedkontoen er en fordelingskonto, skal du bruge standardværdien fra definitionen af fordelingskontoen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="4e4d2-124">Hvis hovedkontoen ikke er en fordelingskonto, skal du bruge standardskabelonen for økonomisk dimension på linjen i fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4e4d2-125">Brug standardværdierne for økonomisk dimension på linjen i fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4e4d2-126">Brug de økonomiske standarddimensionsværdier fra finanskontoen på siden Kontoplan.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e4d2-127">Linje i fritekstfaktura til en kombination af et anlægsaktivnummer og en værdimodel</span><span class="sxs-lookup"><span data-stu-id="4e4d2-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4e4d2-128"><strong>Bemærk! </strong></span><span class="sxs-lookup"><span data-stu-id="4e4d2-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4e4d2-129">Hovedkontoen på linjen i fritekstfakturaen vil være anlægsaktivets kassationskonto.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="4e4d2-130">Finanskontoen på fritekstfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="4e4d2-131">Brug standardværdierne for økonomisk dimension på linjen i fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4e4d2-132">Brug de økonomiske standarddimensionsværdier fra finanskontoen på siden Kontoplan.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e4d2-133">Rabatbeløb i fritekstfakturaen</span><span class="sxs-lookup"><span data-stu-id="4e4d2-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="4e4d2-134">Feltet Hovedkonto til debitorrabatter på siden Kasserabatter.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="4e4d2-135">Hvis hovedkontoen er en fordelingskonto, skal du bruge standardværdien fra definitionen af fordelingskontoen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="4e4d2-136">Hvis hovedkontoen ikke er en fordelingskonto, skal du bruge standardskabelonen for økonomisk dimension på linjen i fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4e4d2-137">Brug standardværdierne for økonomisk dimension på linjen i fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4e4d2-138">Brug de økonomiske standarddimensionsværdier fra finanskontoen på siden Kontoplan.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e4d2-139">Momsbeløb i fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="4e4d2-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="4e4d2-140">Feltet Moms, der skal betales på siden Finanskonteringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="4e4d2-141">Brug de økonomiske dimensioner, der er defineret i linjebeløbet i fritekstfakturaen eller fordelingerne for gebyrlinjebeløbet.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="4e4d2-142">Brug standardværdierne for økonomisk dimension på linjen i fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4e4d2-143">Brug de økonomiske standarddimensionsværdier fra finanskontoen på siden Kontoplan.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e4d2-144">Gebyrlinjebeløb i fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="4e4d2-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="4e4d2-145">Feltet Kreditkonto på siden Gebyrkode.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="4e4d2-146">Hvis hovedkontoen er en fordelingskonto, skal du bruge standardværdien fra definitionen af fordelingskontoen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="4e4d2-147">Hvis hovedkontoen ikke er en fordelingskonto, skal du bruge standardskabelonen for økonomisk dimension på linjen i fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4e4d2-148">Brug standardværdierne for økonomisk dimension på linjen i fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4e4d2-149">Brug de økonomiske standarddimensionsværdier fra finanskontoen på siden Kontoplan.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="4e4d2-150">Fordeling af skatter</span><span class="sxs-lookup"><span data-stu-id="4e4d2-150">Distributing taxes</span></span>
<span data-ttu-id="4e4d2-151">Regnskabsfordelinger for skat kan ikke oprettes, før der er beregnet skat.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="4e4d2-152">Hvis du vil beregne moms, skal du fuldføre en af følgende opgaver i formularen Fritekstfaktura:</span><span class="sxs-lookup"><span data-stu-id="4e4d2-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="4e4d2-153">Få vist momsen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-153">View the sales tax.</span></span>
-   <span data-ttu-id="4e4d2-154">Få vist fakturatotalen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-154">View the invoice total.</span></span>
-   <span data-ttu-id="4e4d2-155">Få vist pengestrømmen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-155">View the cash flow.</span></span>
-   <span data-ttu-id="4e4d2-156">Få vist regnskabsmæssige fordelinger for hele fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="4e4d2-157">Få vist reskontrokladden.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="4e4d2-158">Reskontrokladder til fritekstfakturaer</span><span class="sxs-lookup"><span data-stu-id="4e4d2-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="4e4d2-159">Før du bogfører en fritekstfaktura, kan du få vist den komplette regnskabsenhed for fakturaen, hvilket omfatter debiteringer og krediteringer til kontrol af, at fakturaen bogføres på de rigtige konti.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="4e4d2-160">Denne visning af hele regnskabsenheden kaldes en reskontrokladde.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="4e4d2-161">Hvis kladdeposteringen for reskontro er forkert, når du gennemser den før journalisering af fritekstfakturaen, kan du ikke ændre kladdeposteringen for reskontroen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="4e4d2-162">I stedet skal du redigere de regnskabsmæssige fordelinger eller posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="4e4d2-163">De regnskabsmæssige fordelinger bruges til at definere én side af regnskabsenheden, debiteringen eller krediteringen.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="4e4d2-164">Den modsvarende kontopost for reskontrokladde oprettes ud fra posteringsprofiler, f.eks fra debitorkontoen eller afgiften.</span><span class="sxs-lookup"><span data-stu-id="4e4d2-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>



