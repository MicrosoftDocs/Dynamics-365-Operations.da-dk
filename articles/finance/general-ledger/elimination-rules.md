---
title: Elimineringsregler
description: Dette emne indeholder oplysninger om elimineringsregler og de forskellige indstillinger for rapportering om elimineringer.
author: aprilolson
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0427c05f0c960bd898de3ac308d743f7ccec08f3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823758"
---
# <a name="elimination-rules"></a><span data-ttu-id="fe8cb-103">Elimineringsregler</span><span class="sxs-lookup"><span data-stu-id="fe8cb-103">Elimination rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe8cb-104">Dette emne indeholder oplysninger om elimineringsregler og de forskellige indstillinger for rapportering om elimineringer.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-104">This topic provides information about elimination rules and the various options for reporting about eliminations.</span></span>

<span data-ttu-id="fe8cb-105">Der kræves elimineringsposteringer, når en juridisk enhed for et moderselskab har forretninger med en eller flere juridiske enheder for datterselskaber og bruger konsolideret regnskabsaflæggelse.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-105">Elimination transactions are required when a parent legal entity does business with one or more subsidiary legal entities and uses consolidated financial reporting.</span></span> <span data-ttu-id="fe8cb-106">Konsoliderede regnskaber må kun indeholde transaktioner, der opstår mellem den konsoliderede organisation og de andre enheder uden for de pågældende organisationer.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-106">Consolidated financial statements must include only transactions that occur between the consolidated organization and other entities outside that organizations.</span></span> <span data-ttu-id="fe8cb-107">Derfor skal transaktioner mellem de juridiske enheder, der er del af samme organisation, være fjernet, eller elimineret, fra Finans, så de ikke vises i regnskabsrapporter.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-107">Therefore, transactions between legal entities that are part of the same organization must be removed, or eliminated, from the general ledger, so they don't appear on financial reports.</span></span> <span data-ttu-id="fe8cb-108">Der er flere måder at rapportere om elimineringer på:</span><span class="sxs-lookup"><span data-stu-id="fe8cb-108">There are multiple ways to report about eliminations:</span></span>

-   <span data-ttu-id="fe8cb-109">En elimineringsregel kan oprettes og behandles i et konsoliderings- eller elimineringsregnskab.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-109">An elimination rule can be created and processed in a consolidation or elimination company.</span></span>
-   <span data-ttu-id="fe8cb-110">Regnskabsaflæggelse kan bruges til at vise elimineringskonti og -dimensioner for en bestemt række eller kolonne.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-110">Financial reporting can be used to show the eliminations accounts and dimensions on a specific row or column.</span></span>
-   <span data-ttu-id="fe8cb-111">En særskilt juridisk enhed kan bruges til at bogføre manuelle transaktionsposter for at spore elimineringer.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-111">A separate legal entity can be used to post manual transaction entries to track eliminations.</span></span>

<span data-ttu-id="fe8cb-112">I dette emne beskrives de elimineringsregler, der behandles i et konsolidering-s eller elimineringsregnskab.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-112">This topic focuses on elimination rules that are processed in a consolidation or elimination company.</span></span> <span data-ttu-id="fe8cb-113">Du kan oprette elimineringsregler for at oprette elimineringsposteringer i en juridisk enhed, der er angivet som juridisk destinationsenhed for elimineringer.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-113">You can set up elimination rules to create elimination transactions in a legal entity that is specified as the destination legal entity for eliminations.</span></span> <span data-ttu-id="fe8cb-114">Denne juridiske destinationsenhed er kendt som juridisk enhed til elimineringen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-114">This destination legal entity is known as the elimination legal entity.</span></span> <span data-ttu-id="fe8cb-115">Der kan oprettes elimineringskladder enten under konsolideringsprocessen eller ved hjælp af et elimineringskladdeforslag.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-115">Elimination journals can be generated either during the consolidation process or by using an elimination journal proposal.</span></span> <span data-ttu-id="fe8cb-116">Før du opretter elimineringsregler, skal du sætte dig ind i følgende begreber:</span><span class="sxs-lookup"><span data-stu-id="fe8cb-116">Before you set up elimination rules, you should become familiar with the following terms:</span></span>

-   <span data-ttu-id="fe8cb-117">**Juridisk kildeenhed** – Den juridiske enhed, hvor de beløb, der elimineres, blev bogført.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-117">**Source legal entity** – The legal entity where the amounts that are being eliminated were posted.</span></span>
-   <span data-ttu-id="fe8cb-118">**Juridisk destinationsenhed** – Den juridiske enhed, hvor elimineringsregler bogføres.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-118">**Destination legal entity** – The legal entity where elimination rules are posted.</span></span>
-   <span data-ttu-id="fe8cb-119">**Juridisk elimineringsenhed** – Den juridiske enhed, der er angivet som den juridiske destinationsenhed for elimineringer.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-119">**Elimination legal entity** – The legal entity that is specified as the destination legal entity for eliminations.</span></span>
-   <span data-ttu-id="fe8cb-120">**Konsolideret juridisk enhed** – Den juridiske enhed, der er oprettet til at rapportere økonomiske resultater for en gruppe juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-120">**Consolidated legal entity** – The legal entity that is created to report financial results for a group of legal entities.</span></span> <span data-ttu-id="fe8cb-121">De økonomiske data fra de juridiske enheder er konsolideret i denne juridiske enhed, og derefter oprettes der en økonomisk rapport ved hjælp af de kombinerede data.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-121">The financial data from the legal entities is consolidated into this legal entity, and then a financial report is created by using the combined data.</span></span>

<span data-ttu-id="fe8cb-122">Følgende tabel viser de typer transaktioner, der måske skal elimineres.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-122">The following table shows the types of transactions that might have to be eliminated.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe8cb-123">Konteringstype</span><span class="sxs-lookup"><span data-stu-id="fe8cb-123">Transaction type</span></span></th>
<th><span data-ttu-id="fe8cb-124">Eksempel:</span><span class="sxs-lookup"><span data-stu-id="fe8cb-124">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe8cb-125">Salgsordrepost og fakturering (centraliseret behandling)</span><span class="sxs-lookup"><span data-stu-id="fe8cb-125">Sales order entry and invoicing (centralized processing)</span></span></td>
<td><span data-ttu-id="fe8cb-126">Du sælger et produkt til en kunde på vegne af en anden juridisk enhed i organisationen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-126">You sell a product to a customer on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe8cb-127">Salgsordrepost (intern handel/ekstern handel) og fakturering</span><span class="sxs-lookup"><span data-stu-id="fe8cb-127">Sales order entry (intercompany/intracompany) and invoicing</span></span></td>
<td><span data-ttu-id="fe8cb-128">Du sælger produkter mellem juridiske enheder i organisationen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-128">You sell products between legal entities in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe8cb-129">Indkøbsordrer (centraliseret behandling)</span><span class="sxs-lookup"><span data-stu-id="fe8cb-129">Purchase orders (centralized processing)</span></span></td>
<td><span data-ttu-id="fe8cb-130">Du køber lager, forsyninger, tjenester, anlægsaktiver og andre produkter fra en leverandør på vegne af en anden juridisk enhed i din organisation.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-130">You purchase inventory, supplies, services, fixed assets, and other products from a vendor on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe8cb-131">Lagerstyring (intern handel/ekstern handel)</span><span class="sxs-lookup"><span data-stu-id="fe8cb-131">Inventory management (intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="fe8cb-132">Du kan overføre lageret fra én juridisk enhed til anlægsaktiver i en anden juridisk enhed i organisationen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-132">You transfer one legal entity’s inventory to the fixed assets of another legal entity in your organization.</span></span></li>
<li><span data-ttu-id="fe8cb-133">Du overfører én juridisk enheds lager til lageret i en anden juridisk enhed i organisationen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-133">You transfer one legal entity’s inventory to the inventory of another legal entity in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe8cb-134">Lagersporing i transit</span><span class="sxs-lookup"><span data-stu-id="fe8cb-134">In-transit inventory tracking</span></span></td>
<td><span data-ttu-id="fe8cb-135">Du overfører varer mellem lagersteder i den samme juridiske enhed, men på tværs af forskellige geografiske områder.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-135">You transfer items between warehouses in the same legal entity, but across different geographical sites.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe8cb-136">Centraliseret fakturabehandling for kreditorer</span><span class="sxs-lookup"><span data-stu-id="fe8cb-136">Accounts payable centralized invoice processing</span></span></td>
<td><span data-ttu-id="fe8cb-137">Du registrerer en faktura på vegne af en anden juridisk enhed i organisationen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-137">You record an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe8cb-138">Centraliseret betalingsbehandling for kreditorer</span><span class="sxs-lookup"><span data-stu-id="fe8cb-138">Accounts payable centralized payment processing</span></span></td>
<td><span data-ttu-id="fe8cb-139">Du betaler en faktura på vegne af en anden juridisk enhed i organisationen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-139">You pay an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe8cb-140">Likviditetsstyring og aktier (centraliseret behandling)</span><span class="sxs-lookup"><span data-stu-id="fe8cb-140">Cash management and treasury (centralized processing)</span></span></td>
<td><ul>
<li><span data-ttu-id="fe8cb-141">Du behandler skattebetalinger, skatterefusioner, rentetillæg, lån, forskud, udbyttebetalinger og forudbetalte royalties eller provisioner.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-141">You process tax payments, tax refunds, interest charges, loans, advances, dividend payments, and prepaid royalties or commissions.</span></span></li>
<li><span data-ttu-id="fe8cb-142">Du betaler en udgift på vegne af en anden juridisk enhed i organisationen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-142">You pay an expense on behalf of another legal entity in your organization.</span></span> <span data-ttu-id="fe8cb-143">Fakturaen angives i bøgerne for den juridiske destinationsenhed, og du skal udligne mellem juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-143">The invoice is entered in the destination legal entity’s books, and you must cross-settle between legal entities.</span></span> <span data-ttu-id="fe8cb-144">En juridisk enhed betaler f.eks. udgiftsrapporten for en medarbejder i en anden juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-144">For example, one legal entity pays the expense report of an employee in another legal entity.</span></span> <span data-ttu-id="fe8cb-145">I dette tilfælde har medarbejderens udgiftsrapport udgifter, der er relateret til en anden juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-145">In this case, the employee’s expense report has expenses that are related to another legal entity.</span></span></li>
<li><span data-ttu-id="fe8cb-146">Du overføre penge fra én juridisk enhed til en anden i organisationen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-146">You transfer cash from one legal entity to another in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe8cb-147">Debitorer (centraliseret behandling)</span><span class="sxs-lookup"><span data-stu-id="fe8cb-147">Accounts receivable (centralized processing)</span></span></td>
<td><span data-ttu-id="fe8cb-148">Du modtager kontanter for en anden juridisk enheds debitorfaktura, og du indsætter checken på den pågældende juridiske enheds bankkonto.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-148">You receive cash for another legal entity’s customer invoice, and you deposit the check into that legal entity’s bank account.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe8cb-149">Løn (centraliseret behandling, intern handel/ekstern handel)</span><span class="sxs-lookup"><span data-stu-id="fe8cb-149">Payroll (centralized processing, intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="fe8cb-150">Du betaler løn for en anden juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-150">You pay another legal entity’s payroll.</span></span> <span data-ttu-id="fe8cb-151">En juridisk enhed betaler f.eks. egen løn for sine medarbejdere, men tilbagefører arbejde, som en medarbejder har udført for en anden juridisk enhed, under denne lønkørsel.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-151">For example, a legal entity pays its own payroll for its employees but charges back work that an employee did for another legal entity during that pay run.</span></span> <span data-ttu-id="fe8cb-152">Eller en medarbejder har arbejdet deltids for den juridiske enhed A og deltids for den juridiske enhed B, og frynsegoderne går på tværs af al løn.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-152">Or, an employee worked half-time for legal entity A and half-time for legal entity B, and the benefits are across all pay.</span></span> <span data-ttu-id="fe8cb-153">I disse tilfælde vil medarbejderens løn omfatte løn fra begge juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-153">In these cases, the employee’s pay includes pay from both legal entities.</span></span> <span data-ttu-id="fe8cb-154">Ikke blot er lønnen bogført, men afgifter, frynsegoder, fradrag og periodiseret løn bogføres også.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-154">Not only are the salaries posted, but taxes, benefits, deductions, and accruals for salaries are also posted.</span></span></li>
<li><span data-ttu-id="fe8cb-155">Du overfører arbejdskraft fra én afdeling eller division til en anden.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-155">You transfer labor from one department or division to another.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe8cb-156">Anlægsaktiver (intern handel/ekstern handel)</span><span class="sxs-lookup"><span data-stu-id="fe8cb-156">Fixed assets (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="fe8cb-157">Du overfører anlægsaktiver til en anden juridisk enheds anlægsaktiver eller lager.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-157">You transfer fixed assets to another legal entity’s fixed assets or inventory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe8cb-158">Tildelinger (intern handel/ekstern handel)</span><span class="sxs-lookup"><span data-stu-id="fe8cb-158">Allocations (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="fe8cb-159">Du kan behandle virksomhedstildelinger.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-159">You process corporate allocations.</span></span> <span data-ttu-id="fe8cb-160">Tildelinger er aktiviteter på en hvilken som helst konto, der er tildelt, uanset hvilket modul de stammer fra.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-160">Allocations are activities to any account that is allocated, regardless of the originating module.</span></span></td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="fe8cb-161">Eksempel:</span><span class="sxs-lookup"><span data-stu-id="fe8cb-161">Example</span></span>
<span data-ttu-id="fe8cb-162">Din juridiske enhed, juridisk enhed A, sælger dimser til en anden juridisk enhed i organisationen, juridisk enhed B. Følgende eksempel viser, hvordan transaktioner, der forekommer mellem de to juridiske enheder, muligvis skal elimineres:</span><span class="sxs-lookup"><span data-stu-id="fe8cb-162">Your legal entity, legal entity A, sells widgets to another legal entity in your organization, legal entity B. The following example shows how transactions that occur between the two legal entities might have to be eliminated:</span></span>

-   <span data-ttu-id="fe8cb-163">Juridisk enhed A en sælger en dims, der koster 10,00, til juridisk enhed B for 10,00.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-163">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00.</span></span>
-   <span data-ttu-id="fe8cb-164">Juridisk enhed A sælger en dims, der koster 10,00, til juridisk enhed B for 10,00 plus 2,00 i faktiske leveringsomkostninger.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-164">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00, plus 2.00 in actual shipping costs.</span></span>
-   <span data-ttu-id="fe8cb-165">Juridisk enhed A sælger en dims, der koster 10,00, til juridisk enhed B for 15,00 og opnår fortjeneste på salget.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-165">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes a margin on the sale.</span></span>
-   <span data-ttu-id="fe8cb-166">Juridisk enhed A sælger en dims, der koster 10,00, til juridisk enhed B for 15,00 og registrerer halvdelen af fortjenesten på salget.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-166">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes half the margin on the sale.</span></span> <span data-ttu-id="fe8cb-167">Juridisk enhed B får den anden halvdel af fortjenesten på salget.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-167">Legal entity B recognizes the other half of the margin on the sale.</span></span> <span data-ttu-id="fe8cb-168">Derfor deles indtægten.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-168">Therefore, the revenue is split.</span></span> <span data-ttu-id="fe8cb-169">En delt indtægt fungerer som incitament for at bestille fra en anden juridisk enhed i organisationen i stedet for fra en ekstern organisation.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-169">Split revenue provides an incentive to order from another legal entity in the organization instead of an external organization.</span></span>

<span data-ttu-id="fe8cb-170">Alle disse transaktioner skaber interne transaktioner, der bogføres på skyldig til- og skyldig fra-konti.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-170">All these transactions create intercompany transactions that are posted to due-to and due-from accounts.</span></span> <span data-ttu-id="fe8cb-171">Derudover kan disse transaktioner omfatte avance- eller tabsbeløb, når beløbet for det interne salg ikke er lig med kostprisen for solgte varer</span><span class="sxs-lookup"><span data-stu-id="fe8cb-171">In addition, these transactions might include markup and markdown amounts when the amount of the intercompany sale doesn't equal the cost of the goods that were sold.</span></span>

## <a name="set-up-elimination-rules"></a><span data-ttu-id="fe8cb-172">Konfigurere elimineringsregler</span><span class="sxs-lookup"><span data-stu-id="fe8cb-172">Set up elimination rules</span></span>
<span data-ttu-id="fe8cb-173">Når du opretter elimineringsregler, anbefales det, at du opretter en økonomisk dimension, specielt med henblik på eliminering.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-173">When setting up elimination rules, we recommend that you create a financial dimension specifically for elimination purposes.</span></span> <span data-ttu-id="fe8cb-174">De fleste kunder navngiver den Samhandelspartner eller lignende.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-174">Most customers name it Trading Partner or something similar.</span></span> <span data-ttu-id="fe8cb-175">Hvis du beslutter ikke at bruge en økonomisk dimension, skal du have hovedkonti, der er specifikke for kun interne transaktioner.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-175">If you decide not to use a financial dimension, then be sure to have main accounts that are specific for intercompany transactions only.</span></span> 

<span data-ttu-id="fe8cb-176">Opsætningen for elimineringer findes i området Opsætning i modulet Konsolideringer.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-176">The setup for eliminations is found in the Setup area of the Consolidations module.</span></span> <span data-ttu-id="fe8cb-177">Når du angiver en beskrivelse af reglen, skal du vælge det regnskab, som elimineringskladden skal bogføres til.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-177">After you enter a description for the rule, you must pick the company that the elimination journal will post to.</span></span> <span data-ttu-id="fe8cb-178">Det skal være et regnskab, hvor **Brug til økonomisk eliminering** er valgt i opsætningen af den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-178">This should be a company that has **Use for financial elimination process** selected in the Legal entity setup.</span></span> 

<span data-ttu-id="fe8cb-179">Du kan angive en dato, hvor elimineringsreglen træder i kraft, og også hvor den udløber, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-179">You can set a date on which the elimination rule becomes effective and when it is expired, if needed.</span></span> <span data-ttu-id="fe8cb-180">Du skal indstille **Aktiv** til **Ja**, hvis den skal være tilgængelig i elimineringsforslagsprocessen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-180">You must set **Active** to **Yes** if you want it to be available in the elimination proposal process.</span></span> <span data-ttu-id="fe8cb-181">Vælg et kladdenavn, der har en **Eliminering**-type.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-181">Select a journal name that has a type of **Elimination**.</span></span>

<span data-ttu-id="fe8cb-182">Når du har defineret de grundlæggende elementer, du kan definere de faktiske behandlingsregler ved at klikke på **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-182">After you have defined the basics, you can define the actual processing rules by clicking **Lines**.</span></span> <span data-ttu-id="fe8cb-183">Der er to elimineringsmuligheder, eliminering af nettoændringsbeløbet eller definition af et fast beløb.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-183">There are two options for eliminations, eliminating the net change amount or defining a fixed amount.</span></span> 

<span data-ttu-id="fe8cb-184">Vælg kildekontoen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-184">Select your source account.</span></span> <span data-ttu-id="fe8cb-185">Du kan bruge en stjerne (\*) som jokertegn.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-185">You can use an asterisk (\*) as a wild card.</span></span> <span data-ttu-id="fe8cb-186">For eksemplet vil 1\* vælge alle konti, der starter med 1, som en datakilde til tildelingen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-186">For example, 1\* would select all accounts that start with a 1 as a source of data for the allocation.</span></span> 

<span data-ttu-id="fe8cb-187">Når du har valgt dine kildekonti, bestemmer **Specifikation af regnskab** den konto fra destinationsregnskabet, der bruges.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-187">After you have selected your source accounts, the **Account specification** determines the account from the destination company that is used.</span></span> <span data-ttu-id="fe8cb-188">Vælg **Kilde**, hvis du vil bruge den samme hovedkonto, der er defineret i **Kilde**-kontoen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-188">Select **Source** if you want to use the same main account defined in the **Source** account.</span></span> <span data-ttu-id="fe8cb-189">Hvis du vælger **Brugerdefineret**, skal du angive en destinationskonto.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-189">If you select **User defined**, then you must specify a destination account.</span></span> 

<span data-ttu-id="fe8cb-190">Dimensionsspecifikationen fungerer på samme måde.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-190">The dimension specification acts in the same way.</span></span> <span data-ttu-id="fe8cb-191">Hvis du vælger **Kilde**, bruges de samme dimensioner i modtagervirksomheden som i kilderegnskabet.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-191">If you select **Source**, it will use the same dimensions in the destination company as the source company.</span></span> <span data-ttu-id="fe8cb-192">Hvis du vælger **Brugerdefineret**, skal du angive dimensionerne i modtagervirksomheden ved at klikke på menupunktet **Destinationsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-192">If you select **User defined**, you will need to specify the dimensions in the destination company by clicking the **Destination dimensions** menu item.</span></span> 

<span data-ttu-id="fe8cb-193">Vælg de kildedimensioner og de økonomiske dimensioner og værdier, der bruges som kilde til elimineringen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-193">Select source dimensions and the financial dimensions and values that are used as a source of the elimination.</span></span>

## <a name="process-elimination-transactions"></a><span data-ttu-id="fe8cb-194">Anvend elimineringsposter</span><span class="sxs-lookup"><span data-stu-id="fe8cb-194">Process elimination transactions</span></span>
<span data-ttu-id="fe8cb-195">Der er to måder at behandle elimineringsposteringer på: under onlinekonsolideringsprocessen eller ved at oprette en elimineringskladde og køre elimineringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-195">There are two ways to process elimination transactions, during the consolidate online process or by creating an elimination journal and running the elimination proposal process.</span></span> <span data-ttu-id="fe8cb-196">I dette afsnit fokuseres på oprettelsen af kladden og kørsel af elimineringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-196">This section focuses on creating the journal and running the elimination process.</span></span> 

<span data-ttu-id="fe8cb-197">Vælg **Elimineringskladde** i modulet Konsolideringer i en virksomhed, der er defineret som et elimineringsregnskab.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-197">In a company defined as an elimination company, select **Elimination journal** in the Consolidations module.</span></span> <span data-ttu-id="fe8cb-198">Når du har valgt navnet på kladden, skal du klikke på **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-198">After you have selected the journal name, click **Lines**.</span></span> <span data-ttu-id="fe8cb-199">Du kan køre forslaget ved at vælge menuen **Forslag** og derefter vælge **Elimineringsforslag**.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-199">You can run the proposal by selecting the **Proposals** menu and then selecting **Elimination proposal**.</span></span>

<span data-ttu-id="fe8cb-200">Vælg det regnskab, der er kilden til de konsoliderede data, og vælg derefter den regel, du vil behandle.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-200">Select the company that is the source of the consolidated data, and then choose the rule that you want to process.</span></span> <span data-ttu-id="fe8cb-201">Angiv en startdato for at starte søgningen efter elimineringsbeløb og en slutdato, hvor søgningen efter elimineringsbeløb skal afsluttes.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-201">Enter a start date to begin the search for elimination amounts, and an end date to end the search date for elimination amounts.</span></span> <span data-ttu-id="fe8cb-202">Feltet **Finansposteringsdato** er den dato, der bruges til bogføring af kladden i finans.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-202">The **GL posting date** field is the date used for posting the journal to the general ledger.</span></span> <span data-ttu-id="fe8cb-203">Når du klikker på **OK**, kan du gennemse beløbene og bogføre kladden.</span><span class="sxs-lookup"><span data-stu-id="fe8cb-203">After you click **OK**, you can review the amounts and post the journal.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]