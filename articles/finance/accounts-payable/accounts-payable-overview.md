---
title: Oversigt over konfiguration af Kreditor
description: I denne artikel beskrives de sider, som du kan bruge til at konfigurere grundlæggende og valgfri funktioner for Kreditor. Der beskrives også de installationstrin, du skal fuldføre, før du begynder at konfigurere Kreditor.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1ca94bf4a6eb9f65d7302c2071fd108be752764
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177051"
---
# <a name="configure-accounts-payable-overview"></a><span data-ttu-id="351ff-104">Oversigt over konfiguration af Kreditor</span><span class="sxs-lookup"><span data-stu-id="351ff-104">Configure Accounts payable overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="351ff-105">I denne artikel beskrives de sider, som du kan bruge til at konfigurere grundlæggende og valgfri funktioner for Kreditor.</span><span class="sxs-lookup"><span data-stu-id="351ff-105">This article describes the pages that you use to set up basic and optional functionality for Accounts payable.</span></span> <span data-ttu-id="351ff-106">Der beskrives også de installationstrin, du skal fuldføre, før du begynder at konfigurere Kreditor.</span><span class="sxs-lookup"><span data-stu-id="351ff-106">It also describes setup steps that you must complete before you start to set up Accounts payable.</span></span>

<a name="prerequisites-for-accounts-payable-setup"></a><span data-ttu-id="351ff-107">Forudsætninger for konfiguration af kreditorer</span><span class="sxs-lookup"><span data-stu-id="351ff-107">Prerequisites for Accounts payable setup</span></span>
----------------------------------------

<span data-ttu-id="351ff-108">Inden du kan konfigurere kreditorer, skal du fuldføre følgende konfiguration:</span><span class="sxs-lookup"><span data-stu-id="351ff-108">Before you can set up Accounts payable, you must complete the following setup:</span></span>

-   <span data-ttu-id="351ff-109">I Finans:</span><span class="sxs-lookup"><span data-stu-id="351ff-109">In General ledger:</span></span>
    -   <span data-ttu-id="351ff-110">Hvis du vil bruge betalingskladder, skal du konfigurere betalingskladderne.</span><span class="sxs-lookup"><span data-stu-id="351ff-110">If you plan to use payment journals, set up payment journals.</span></span>
    -   <span data-ttu-id="351ff-111">Hvis du planlægger at køre valutakursreguleringer, skal du oprette valutakoder på siden Valutaer, konfigurere valutakurstyper på siden Valutakurstyper og konfigurere valutakurser på siden Valutakurser.</span><span class="sxs-lookup"><span data-stu-id="351ff-111">If you plan to run exchange rate adjustments, set up currency codes on the Currencies page, set up exchange rate types on the Exchange rate types page, and set up currency exchange rates on the Currency exchange rates page.</span></span>
-   <span data-ttu-id="351ff-112">I Kontant- og bankstyring skal du konfigurere bankkonti, der skal bruges med betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="351ff-112">In Cash and bank management, set up bank accounts to use with methods of payment.</span></span>

## <a name="setup-pages-for-accounts-payable"></a><span data-ttu-id="351ff-113">Opsætning af sider for kreditor</span><span class="sxs-lookup"><span data-stu-id="351ff-113">Setup pages for Accounts payable</span></span>

<span data-ttu-id="351ff-114">Du kan bruge følgende sider til at konfigurere de grundlæggende funktioner i Kreditor for hver juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="351ff-114">Use the following pages to set up the basic functionality of Accounts payable for each legal entity.</span></span> <span data-ttu-id="351ff-115">De viste sider vises i den rækkefølge, som det anbefales at konfigurere dem i.</span><span class="sxs-lookup"><span data-stu-id="351ff-115">The pages are listed in the recommended order of setup.</span></span> <span data-ttu-id="351ff-116">Du kan gøre konfigureringsprocessen nemmere ved at oprette skabeloner fra de første poster, du opretter.</span><span class="sxs-lookup"><span data-stu-id="351ff-116">To make the setup process easier, you can create templates from the first records that you create.</span></span> <span data-ttu-id="351ff-117">I en skabelon bliver der typisk indtastet værdier i mange felter for at afspejle de egenskaber, som organisationen ønsker at anvende for en bestemt type kreditor.</span><span class="sxs-lookup"><span data-stu-id="351ff-117">In a template, values are typically entered in many fields to reflect the features that the organization wants to implement for a particular type of vendor.</span></span>
1.  <span data-ttu-id="351ff-118">På siden Betalingsbetingelser skal du definere de betalingsbetingelser, du knytter til salgsordrer, indkøbsordrer, debitorer og kreditorer, og som bestemmer forfaldsdatoer for fakturaer.</span><span class="sxs-lookup"><span data-stu-id="351ff-118">On the Terms of payment page, define the terms of payment that you assign to sales orders, purchase orders, customers, and vendors, and that determine invoice due dates.</span></span> <span data-ttu-id="351ff-119">Du kan finde flere oplysninger under [Definere kreditorbetalingsgebyrer](tasks/define-vendor-payment-fees.md).</span><span class="sxs-lookup"><span data-stu-id="351ff-119">For more information, see [Define vendor payment fees](tasks/define-vendor-payment-fees.md).</span></span>
2.  <span data-ttu-id="351ff-120">På siden Betalingsmåder – kreditorer skal du oprette og vedligeholde oplysninger om, hvordan organisationen betaler sine kreditorer.</span><span class="sxs-lookup"><span data-stu-id="351ff-120">On the Methods of payment - vendors page, create and maintain information about how the organization pays its vendors.</span></span>
3.  <span data-ttu-id="351ff-121">På siden Kreditorgruppe skal du oprette og vedligeholde grupper af kreditorer, der deler vigtige parametre for bogføring, udligning og betaling, rapportering og budgettering.</span><span class="sxs-lookup"><span data-stu-id="351ff-121">On the Vendor groups page, create and maintain groups of vendors that share important parameters for posting, settlement and payment, reporting, and forecasting.</span></span>
4.  <span data-ttu-id="351ff-122">På siden Kreditorposteringsprofiler skal du definere, hvordan kreditorposter bogføres i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="351ff-122">On the Vendor posting profiles page, define how vendor transactions are posted to the general ledger.</span></span>
5.  <span data-ttu-id="351ff-123">På siden Kreditorparametre kan du konfigurere de standardindstillinger, der anvendes, hvis en mere specifik indstilling ikke er angivet, parametre for forskellige typer funktioner og forskellige nummerserier for kreditorer.</span><span class="sxs-lookup"><span data-stu-id="351ff-123">On the Accounts payable parameters page, set up default settings that are applied if a more specific setting isn't specified, parameters for various kinds of functionality, and the various number sequences for Accounts payable.</span></span>
6.  <span data-ttu-id="351ff-124">På siden Formularopsætning kan du definere de forskellige dokumenter, der er relateret til kreditorer, og som organisationen bruger til at holde styr på tilgange fra kreditorer og til at angive årsager til betalingsflowet til kreditorer.</span><span class="sxs-lookup"><span data-stu-id="351ff-124">On the Form setup page, define the format of various documents that are related to vendors, and that the organization uses to keep track of receipts from vendors and enter reasons for the flow of payments to vendors.</span></span>
7.  <span data-ttu-id="351ff-125">På siden Kreditorer kan du oprette og vedligeholde kreditorkonti og også de skattemyndigheder, som din organisation indberetter moms til.</span><span class="sxs-lookup"><span data-stu-id="351ff-125">On the Vendors page, create and maintain vendor accounts, and also the tax authorities that your organization reports sales taxes to.</span></span>

## <a name="optional-setup-pages-for-accounts-payable"></a><span data-ttu-id="351ff-126">Valgfri opsætningssider for Kreditor</span><span class="sxs-lookup"><span data-stu-id="351ff-126">Optional setup pages for Accounts payable</span></span>
<span data-ttu-id="351ff-127">Ud over de grundlæggende funktioner har kreditor andre funktioner, du kan konfigurere.</span><span class="sxs-lookup"><span data-stu-id="351ff-127">In addition to the basic functionality, Accounts payable has other functionality that you can set up.</span></span>

<span data-ttu-id="351ff-128">De ekstra opsætningssider er organiseret efter funktioner.</span><span class="sxs-lookup"><span data-stu-id="351ff-128">The additional setup pages are organized by functionality.</span></span>

<span data-ttu-id="351ff-129">**Politikker**</span><span class="sxs-lookup"><span data-stu-id="351ff-129">**Policies**</span></span>
-   <span data-ttu-id="351ff-130">På siden Politik for kreditorfaktura kan du angive politikker for kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="351ff-130">On the Vendor invoice policy page, set up vendor invoice policies.</span></span>

<span data-ttu-id="351ff-131">**Fakturasammenholdelse**</span><span class="sxs-lookup"><span data-stu-id="351ff-131">**Invoice matching**</span></span>

-   <span data-ttu-id="351ff-132">På siden Tolerancer for fakturatotaler kan du angive tolerancer for sammenholdelse af fakturatotaler.</span><span class="sxs-lookup"><span data-stu-id="351ff-132">On the Invoice totals tolerances page, set up tolerances for invoice totals.</span></span>
-   <span data-ttu-id="351ff-133">På siden Sammenholdelsespolitik kan du angive politikker for tovejs- og trevejssammenholdelse.</span><span class="sxs-lookup"><span data-stu-id="351ff-133">On the Matching policy page, set up two-way and three-way matching policies.</span></span>
-   <span data-ttu-id="351ff-134">På siden Pristolerancer kan du angive tolerancer for salgspriser.</span><span class="sxs-lookup"><span data-stu-id="351ff-134">On the Price tolerances page, set up tolerances for unit prices.</span></span>
-   <span data-ttu-id="351ff-135">På siden Pristolerancegrupper for vare kan du angive tolerancegrupper for varepriser.</span><span class="sxs-lookup"><span data-stu-id="351ff-135">On the Item price tolerance groups page, set up tolerance groups for item prices.</span></span>
-   <span data-ttu-id="351ff-136">På siden Pristolerancegrupper for kreditor kan du angive tolerancegrupper for leverandørpriser.</span><span class="sxs-lookup"><span data-stu-id="351ff-136">On the Vendor price tolerance groups page, set up  tolerance groups for vendor prices.</span></span>
-   <span data-ttu-id="351ff-137">På siden Gebyrtolerancer kan du angive tolerancer for gebyrer.</span><span class="sxs-lookup"><span data-stu-id="351ff-137">On the Charges tolerances page, set up tolerances for charges.</span></span>

<span data-ttu-id="351ff-138">**Arbejdsgang**</span><span class="sxs-lookup"><span data-stu-id="351ff-138">**Workflow**</span></span>

-   <span data-ttu-id="351ff-139">På siden Kreditorarbejdsgange kan du angive arbejdsgangekonfigurationer for kladdegodkendelser og indkøbsrekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="351ff-139">On the Accounts payable workflows page, set up workflow configurations for journal approvals and purchase requisitions.</span></span>

<span data-ttu-id="351ff-140">**Årsager**</span><span class="sxs-lookup"><span data-stu-id="351ff-140">**Reasons**</span></span>

-   <span data-ttu-id="351ff-141">På siden Kreditorårsager kan du angive årsagskoder.</span><span class="sxs-lookup"><span data-stu-id="351ff-141">On the Vendor reasons page, set up reason codes.</span></span>

<span data-ttu-id="351ff-142">**Tillæg**</span><span class="sxs-lookup"><span data-stu-id="351ff-142">**Charges**</span></span>

-   <span data-ttu-id="351ff-143">På siden Gebyrkode kan du angive koder for de gebyrer, der bruges i indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="351ff-143">On the Charges code page, set up codes for the charges that are used in purchase orders.</span></span>
-   <span data-ttu-id="351ff-144">På siden Kreditorgebyrgruppe kan du oprette og vedligeholde gebyrgrupper for kreditorer.</span><span class="sxs-lookup"><span data-stu-id="351ff-144">On the Vendor charges group page, create and maintain charges groups for vendors.</span></span>
-   <span data-ttu-id="351ff-145">På siden Varegebyrgrupper kan du oprette og vedligeholde gebyrgrupper for varer.</span><span class="sxs-lookup"><span data-stu-id="351ff-145">On the Item charge groups page, create and maintain charges groups for items.</span></span>
-   <span data-ttu-id="351ff-146">På siden Automatiske gebyrer kan du definere de gebyrer, der automatisk knyttes til ordrer.</span><span class="sxs-lookup"><span data-stu-id="351ff-146">On the Auto charges page, define the charges that are automatically assigned to orders.</span></span>

<span data-ttu-id="351ff-147">**Supplerende varer**</span><span class="sxs-lookup"><span data-stu-id="351ff-147">**Supplementary items**</span></span>

-   <span data-ttu-id="351ff-148">På siden Supplerende varegrupper – Kreditor kan du oprette og vedligeholde supplerende varegrupper for kreditorer.</span><span class="sxs-lookup"><span data-stu-id="351ff-148">On the Supplementary item groups - Vendor page, create and maintain supplementary item groups for vendors.</span></span>
-   <span data-ttu-id="351ff-149">På siden Supplerende varegrupper – Lager kan du oprette og vedligeholde supplerende varegrupper for varer.</span><span class="sxs-lookup"><span data-stu-id="351ff-149">On the Supplementary item groups - Inventory page, create and maintain supplementary item groups for items.</span></span>

<span data-ttu-id="351ff-150">**Fordeling**</span><span class="sxs-lookup"><span data-stu-id="351ff-150">**Distribution**</span></span>

-   <span data-ttu-id="351ff-151">På siden Leveringsbetingelser kan du oprette og vedligeholde betingelserne for en vares overførsel fra sælger til køber.</span><span class="sxs-lookup"><span data-stu-id="351ff-151">On the Terms of delivery page, create and maintain the conditions for an item's transfer from seller to buyer.</span></span>
-   <span data-ttu-id="351ff-152">På siden Leveringsmåder kan du oprette og vedligeholde de transportmåder, der bruges, når en ordre leveres fra sælger til køber.</span><span class="sxs-lookup"><span data-stu-id="351ff-152">On the Modes of delivery page, create and maintain the methods of transport that are used when an order is delivered from the seller to the buyer.</span></span>
-   <span data-ttu-id="351ff-153">På siden Destinationskoder kan du oprette og vedligeholde identifikatorer og beskrivelser for leveringsdestinationer.</span><span class="sxs-lookup"><span data-stu-id="351ff-153">On the Destination codes page, create and maintain identifiers and descriptions for delivery destinations.</span></span>

<span data-ttu-id="351ff-154">**Formularer**</span><span class="sxs-lookup"><span data-stu-id="351ff-154">**Forms**</span></span>

-   <span data-ttu-id="351ff-155">På siden Formularnoter kan du oprette den standardtekst, der vises på diverse sider.</span><span class="sxs-lookup"><span data-stu-id="351ff-155">On the Form notes page, create the standard text that appears on various pages.</span></span>
-   <span data-ttu-id="351ff-156">På siden Formsorteringsparametre kan du konfigurere sorteringsrækkefølgen for rekvisitioner, tilgangslister, følgesedler og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="351ff-156">On the Form sorting parameters page, set up the sorting order for requisitions, receipt lists, packing slips, and invoices.</span></span>
-   <span data-ttu-id="351ff-157">På siden Opsætning af udskriftsstyring kan du angive udskrifts- og administrationsoplysninger for originaler og kopier af siderne.</span><span class="sxs-lookup"><span data-stu-id="351ff-157">On the Print management setup page, set up print management information for originals and copies of pages.</span></span>

<span data-ttu-id="351ff-158">**Betalinger**</span><span class="sxs-lookup"><span data-stu-id="351ff-158">**Payments**</span></span>

-   <span data-ttu-id="351ff-159">På siden Kasserabat kan du konfigurere og administrere betingelserne for at opnå kasserabatter.</span><span class="sxs-lookup"><span data-stu-id="351ff-159">On the Cash discounts page, set up and manage the terms for obtaining cash discounts.</span></span> <span data-ttu-id="351ff-160">Kasserabatkoderne knyttes til kreditorer og anvendes på indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="351ff-160">The cash discount codes are linked to vendors and are applied to purchase orders.</span></span>
-   <span data-ttu-id="351ff-161">På siden Betalingsplaner kan du oprette betalingsplaner, der bruges til administration af ratebetalinger til kreditorer.</span><span class="sxs-lookup"><span data-stu-id="351ff-161">On the Payment schedules page, set up the payment schedules that are used to manage installment payments to vendors.</span></span>
-   <span data-ttu-id="351ff-162">På siden Betalingsdage kan du definere de betalingsdage, der bruges til beregning af forfaldsdatoer, og angive betalingsdage for en bestemt ugedag eller dag i måneden.</span><span class="sxs-lookup"><span data-stu-id="351ff-162">On the Payment days page, define the payment days that are used to calculate due dates, and specify payment days for a specific day of the week or month.</span></span>
-   <span data-ttu-id="351ff-163">På siden Betalingsgebyr kan du oprette og vedligeholde gebyrer, der er knyttet til kreditorer.</span><span class="sxs-lookup"><span data-stu-id="351ff-163">On the Payment fee page, create and maintain the payment fees that are associated with vendors.</span></span>
-   <span data-ttu-id="351ff-164">På siden Betalingsinstruktion kan du oprette og vedligeholde betalingsinstruktioner.</span><span class="sxs-lookup"><span data-stu-id="351ff-164">On the Payment instruction page, create and maintain payment instructions.</span></span>

<span data-ttu-id="351ff-165">**Statistik**</span><span class="sxs-lookup"><span data-stu-id="351ff-165">**Statistics**</span></span>

-   <span data-ttu-id="351ff-166">På siden Definitioner af forældelsesperioder kan du konfigurere brugerdefinerede intervaller, der bruges til at analysere forfaldsfordelingen af kreditorkonti.</span><span class="sxs-lookup"><span data-stu-id="351ff-166">On the Aging period definitions page, set up user-defined intervals that are used to analyze the maturity distribution of vendor accounts.</span></span>
-   <span data-ttu-id="351ff-167">På siden Forretningsområde kan du oprette koder for de forretningsområder, der er knyttet til kreditorer.</span><span class="sxs-lookup"><span data-stu-id="351ff-167">On the Line of business page, create the line of business (LOB) codes that are assigned to vendors.</span></span>

<span data-ttu-id="351ff-168">**1099-skat**</span><span class="sxs-lookup"><span data-stu-id="351ff-168">**Tax 1099**</span></span>

-   <span data-ttu-id="351ff-169">På siden **1099-felter** kan du bekræfte og opdatere de minimumbeløb, der skal rapporteres til de interne skattemyndigheder (IRS), baseret på de seneste myndighedskrav.</span><span class="sxs-lookup"><span data-stu-id="351ff-169">On the **1099 fields** page, verify and update the minimum amounts that must be reported to the Internal Revenue Service (IRS), based on the latest IRS requirements.</span></span>

## <a name="optional-setup-for-other-modules"></a><span data-ttu-id="351ff-170">**Valgfri konfiguration til andre moduler**</span><span class="sxs-lookup"><span data-stu-id="351ff-170">**Optional setup for other modules**</span></span>
<span data-ttu-id="351ff-171">**Virksomhedsadministration**</span><span class="sxs-lookup"><span data-stu-id="351ff-171">**Organization administration**</span></span>

-   <span data-ttu-id="351ff-172">På siden Nummerserier kan du konfigurere nummerseriegrupper med fakturanumre.</span><span class="sxs-lookup"><span data-stu-id="351ff-172">On the Number sequences page, set up number sequence groups for invoice numbers.</span></span>
-   <span data-ttu-id="351ff-173">På følgende sider kan du definere adresseoplysninger:</span><span class="sxs-lookup"><span data-stu-id="351ff-173">On the following pages, set up address information:</span></span>
    -   <span data-ttu-id="351ff-174">Adresseopsætning</span><span class="sxs-lookup"><span data-stu-id="351ff-174">Address setup</span></span>
    -   <span data-ttu-id="351ff-175">NAF-koder</span><span class="sxs-lookup"><span data-stu-id="351ff-175">NAF codes</span></span>
    -   <span data-ttu-id="351ff-176">Import af postnumre</span><span class="sxs-lookup"><span data-stu-id="351ff-176">Import ZIP/postal codes</span></span>

<span data-ttu-id="351ff-177">**Økonomi**</span><span class="sxs-lookup"><span data-stu-id="351ff-177">**General ledger**</span></span>

-   <span data-ttu-id="351ff-178">På siden Økonomiske dimensioner kan du konfigurere de økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="351ff-178">On the Financial dimensions page, set up financial dimensions.</span></span>
-   <span data-ttu-id="351ff-179">På følgende sider kan du konfigurere momsoplysninger:</span><span class="sxs-lookup"><span data-stu-id="351ff-179">On the following pages, set up tax information:</span></span>
    -   <span data-ttu-id="351ff-180">Momskoder</span><span class="sxs-lookup"><span data-stu-id="351ff-180">Sales tax codes</span></span>
    -   <span data-ttu-id="351ff-181">Momsgrupper</span><span class="sxs-lookup"><span data-stu-id="351ff-181">Sales tax groups</span></span>
    -   <span data-ttu-id="351ff-182">Varemomsgrupper</span><span class="sxs-lookup"><span data-stu-id="351ff-182">Item sales tax groups</span></span>
    -   <span data-ttu-id="351ff-183">Kontogruppe</span><span class="sxs-lookup"><span data-stu-id="351ff-183">Account group</span></span>
    -   <span data-ttu-id="351ff-184">Momsfritagelseskoder</span><span class="sxs-lookup"><span data-stu-id="351ff-184">Sales tax exempt codes</span></span>
    -   <span data-ttu-id="351ff-185">Momsjurisdiktionsområder</span><span class="sxs-lookup"><span data-stu-id="351ff-185">Sales tax jurisdictions</span></span>
    -   <span data-ttu-id="351ff-186">Momsmyndigheder</span><span class="sxs-lookup"><span data-stu-id="351ff-186">Sales tax authorities</span></span>
    -   <span data-ttu-id="351ff-187">Momsafregningsperioder</span><span class="sxs-lookup"><span data-stu-id="351ff-187">Sales tax settlement periods</span></span>

<span data-ttu-id="351ff-188">**Kontant- og bankstyring**</span><span class="sxs-lookup"><span data-stu-id="351ff-188">**Cash and bank management**</span></span>

-   <span data-ttu-id="351ff-189">På siden Betalingsformålskoder kan du konfigurere nationalbankens formålskoder.</span><span class="sxs-lookup"><span data-stu-id="351ff-189">On the Payment purpose codes page, set up the Central Bank purpose code.</span></span>





