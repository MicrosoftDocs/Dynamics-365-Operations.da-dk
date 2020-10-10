---
title: Lokalisere fejl i produktkvitteringer og fakturering
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med produktkvitteringer og fakturering.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d86fa3df1de13cc0e0fb94449207a326069da25b
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834334"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="11507-103">Lokalisere fejl i produktkvitteringer og fakturering</span><span class="sxs-lookup"><span data-stu-id="11507-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="11507-104">Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med produktkvitteringer og fakturering.</span><span class="sxs-lookup"><span data-stu-id="11507-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="11507-105">Jeg kan ikke bogføre mere end én faktura på en indkøbsordrelinje, der har kategoribaserede varer.</span><span class="sxs-lookup"><span data-stu-id="11507-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="11507-106">Et antal skal angives, hvis du vil bogføre fakturaer.</span><span class="sxs-lookup"><span data-stu-id="11507-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="11507-107">Hvis hele antallet på en linje kun er faktureret for et delvist beløb, kan du derfor ikke fakturere restbeløbet på en anden faktura.</span><span class="sxs-lookup"><span data-stu-id="11507-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="11507-108">Jeg får vist fejlmeddelelsen "Objektreferencen er ikke angivet" under bekræftelse af indkøbsordren, eller der er opstået "Destinationen for en aktivering udløste en undtagelse" under bogføring af kreditorfakturaen.</span><span class="sxs-lookup"><span data-stu-id="11507-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="11507-109">Dette problem kan opstå på grund af inkonsistens i indkøbsordrefordeling.</span><span class="sxs-lookup"><span data-stu-id="11507-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="11507-110">Hvis du vil løse dette problem og nulstille indkøbsordren til en *Kladde*-tilstand, skal du gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Nulstil indkøbsordrefordeling**.</span><span class="sxs-lookup"><span data-stu-id="11507-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="11507-111">Du kan finde flere oplysninger i følgende blogindlæg: [Løse fejl i indkøbsordrefordeling i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="11507-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="11507-112">Jeg kan ikke konsolidere flere produktkvitteringer i en enkelt indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="11507-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="11507-113">Du kan ikke konsolidere flere produktkvitteringer i en enkelt indkøbsordre, hvis de forskellige produktkvitteringslinjer har forskellige regnskabsdatoer.</span><span class="sxs-lookup"><span data-stu-id="11507-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="11507-114">I tidligere versioner af Microsoft Dynamics 365 Supply Chain Management var konsolidering tilladt i denne situation.</span><span class="sxs-lookup"><span data-stu-id="11507-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="11507-115">Det er dog fejlrisiko ved denne praksis.</span><span class="sxs-lookup"><span data-stu-id="11507-115">However, the practice is prone to error.</span></span> <span data-ttu-id="11507-116">Regnskabsdatoen på de indkøbsordrelinjer, der oprettes, bør ikke være forskellige fra regnskabsdatoen på de produktkvitteringslinjer, som disse indkøbsordrelinjer er oprettet ud fra.</span><span class="sxs-lookup"><span data-stu-id="11507-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="11507-117">(Regnskabsdatoen på indkøbsordrelinjerne svarer til regnskabsdatoen på indkøbsordrehovedet). Det er derfor ikke længere tilladt at konsolidere flere produktkvitteringer i en enkelt indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="11507-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="11507-118">Regnskabsdatoen bruges f.eks. ved budgetreservationer og behæftelser.</span><span class="sxs-lookup"><span data-stu-id="11507-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="11507-119">Derfor skal den beholdes under overgangen fra produktkvittering til indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="11507-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="11507-120">Når produktkvitteringer annulleres, kan transaktionerne bogføres på en suspenderet finanskonto.</span><span class="sxs-lookup"><span data-stu-id="11507-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="11507-121">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="11507-121">Issue description</span></span>

<span data-ttu-id="11507-122">Hvis en produktkvittering annulleres, tillader systemet, at der bogføres transaktioner på suspenderede finanskonti, selvom hovedkontiene er suspenderet.</span><span class="sxs-lookup"><span data-stu-id="11507-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="11507-123">Genskabe problemet</span><span class="sxs-lookup"><span data-stu-id="11507-123">Reproduce the issue</span></span>

<span data-ttu-id="11507-124">Følgende procedurer viser en måde at genskabe problemet på.</span><span class="sxs-lookup"><span data-stu-id="11507-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="11507-125">På siden **Kreditorparametre** skal du under fanen **Generelt** kontrollere, at indstillingen **Bogfør produktkvittering i finans** er angivet til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="11507-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="11507-126">Opret en indkøbsordre, og tilføj en ordrelinje, der har et antal på *1.000* for et produkt.</span><span class="sxs-lookup"><span data-stu-id="11507-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="11507-127">Bekræft indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="11507-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="11507-128">Bogfør produktkvitteringen, og kontrollér bilagene.</span><span class="sxs-lookup"><span data-stu-id="11507-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="11507-129">Suspender de relevante hovedkonti, *200140* og *140200*.</span><span class="sxs-lookup"><span data-stu-id="11507-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="11507-130">Annuller den bogførte produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="11507-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="11507-131">Bemærk, at transaktioner kan bogføres på de suspenderede finanskonti.</span><span class="sxs-lookup"><span data-stu-id="11507-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="11507-132">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="11507-132">Issue resolution</span></span>

<span data-ttu-id="11507-133">Transaktioner kan bogføres på de suspenderede finanskonti, når produktkvitteringer annulleres, da denne funktionsmåde giver mulighed for korrekte bogføringer.</span><span class="sxs-lookup"><span data-stu-id="11507-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="11507-134">Bilagsnummeret på produktkvitteringen forbruges, selvom der ikke genereres et økonomisk bilag under produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="11507-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="11507-135">Hvis indstillingen **Periodiser passiver ved produktmodtagelse** er angivet til *Nej* for varemodelgruppen, vil der ikke blive bogført til Finans.</span><span class="sxs-lookup"><span data-stu-id="11507-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="11507-136">Der vil dog blive registreret en fysisk hændelse med det formål at foretage regnskabsføring i en reskontro, og den pågældende hændelse kræver et bilagsnummer.</span><span class="sxs-lookup"><span data-stu-id="11507-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="11507-137">Dette bilagsnummer er det bilagsnummer, der refereres til i lagertransaktionerne.</span><span class="sxs-lookup"><span data-stu-id="11507-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="11507-138">Det anbefales, at du angiver indstillingen **Periodiser passiver ved produktmodtagelse** til *Ja* som beskrevet i følgende blogindlæg: [Bogføre diverse gebyrer på tidspunktet for produktmodtagelse](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="11507-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes*, as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="11507-139">Indstillingen Vil du bogføre på omkostningskontoen i finans? er ikke aktiveret.</span><span class="sxs-lookup"><span data-stu-id="11507-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="11507-140">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="11507-140">Issue description</span></span>

<span data-ttu-id="11507-141">Dette problem opstår, når en indkøbsordre faktureres, hvis indstillingen **Vil du bogføre på omkostningskontoen i finans?** er angivet til *Ja* under fanen **Faktura** på siden **Kreditorparametre**.</span><span class="sxs-lookup"><span data-stu-id="11507-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="11507-142">Genskabe problemet</span><span class="sxs-lookup"><span data-stu-id="11507-142">Reproduce the issue</span></span>

<span data-ttu-id="11507-143">Følgende procedurer viser en måde at genskabe problemet på.</span><span class="sxs-lookup"><span data-stu-id="11507-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="11507-144">Gå til **Kreditor \> Opsætning \> Kreditorparametre**.</span><span class="sxs-lookup"><span data-stu-id="11507-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="11507-145">Under fanen **Faktura** skal du angive **Vil du bogføre på omkostningskontoen i finans?** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="11507-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="11507-146">Gå til **Lagerstyring \> Konfiguration \> Bogføring \> Bogføring**.</span><span class="sxs-lookup"><span data-stu-id="11507-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="11507-147">Under fanen **Indkøbsordre** skal du sikre dig, at du har slettet alle linjerne i købsudgiften for produktet.</span><span class="sxs-lookup"><span data-stu-id="11507-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="11507-148">Gå til **Kreditor \> Indkøbsordrer \> Alle indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="11507-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="11507-149">Oprette en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="11507-149">Create a purchase order.</span></span> <span data-ttu-id="11507-150">Vælg **1001 ACME kontorartikler** i feltet *Kreditorkonto*.</span><span class="sxs-lookup"><span data-stu-id="11507-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="11507-151">Tilføj en indkøbsordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="11507-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="11507-152">**Varenummer:** *D0011 laserprojektor*</span><span class="sxs-lookup"><span data-stu-id="11507-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="11507-153">**Lokation:** *1*</span><span class="sxs-lookup"><span data-stu-id="11507-153">**Site:** *1*</span></span>
    - <span data-ttu-id="11507-154">**Lagersted:** *11*</span><span class="sxs-lookup"><span data-stu-id="11507-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="11507-155">**Antal:** *4*</span><span class="sxs-lookup"><span data-stu-id="11507-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="11507-156">Vælg **Bekræft** i gruppen **Handling** under fanen **Indkøb** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="11507-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="11507-157">Gå til handlingsruden, og vælg **Produktkvittering** i gruppen **Generér** under fanen **Modtag**.</span><span class="sxs-lookup"><span data-stu-id="11507-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="11507-158">Angiv et vilkårligt nummer i feltet **Produktkvittering** i dialogboksen **Konterer produktkvittering**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="11507-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="11507-159">Vælg **Faktura** i gruppen **Generér** under fanen **Faktura** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="11507-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="11507-160">Angiv et vilkårligt nummer som fakturanummer i feltet **Nummer**.</span><span class="sxs-lookup"><span data-stu-id="11507-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="11507-161">Opdater status for sammenholdelse, og bogfør.</span><span class="sxs-lookup"><span data-stu-id="11507-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="11507-162">Bemærk, at du nu får vist følgende fejl, når du opretter en faktura ud fra en indkøbsordre: "Kontonummer for konteringstypen Indkøbsudgifter for produkt findes ikke".</span><span class="sxs-lookup"><span data-stu-id="11507-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="11507-163">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="11507-163">Issue resolution</span></span>

<span data-ttu-id="11507-164">Dette afhænger af parameterindstillingerne for fakturaer og fakturagrupper.</span><span class="sxs-lookup"><span data-stu-id="11507-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="11507-165">Du kan finde flere oplysninger i følgende blogindlæg: [Regnskabsføring for indkøbstillæg og lagervariation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span><span class="sxs-lookup"><span data-stu-id="11507-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>
