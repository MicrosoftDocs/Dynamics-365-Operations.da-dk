---
title: "Indkøb og forsyning i den offentlige sektor"
description: "Denne oversigt introducerer dig til den offentlige sektors funktion Indkøb og forsyning. Dette omfatter indkøbsordrekoder, certificering kreditortyper, funktion til klassificering af købsaftaler og indkøbsordrelinjebeløb."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AgreementClassification, BudgetParameters, ProcCategoryHierarchyManagement, PurchTableListPage, smmActivities, VendCertificationType, VendTableListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 19681
ms.assetid: c99b2aeb-4ac2-4abe-b8b9-786b664c103d
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 66251ed112dae9db73485df806be0aca5957e78e
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="procurement-and-sourcing-in-the-public-sector"></a><span data-ttu-id="df22d-104">Indkøb og forsyning i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="df22d-104">Procurement and sourcing in the public sector</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="df22d-105">Denne oversigt introducerer dig til den offentlige sektors funktion Indkøb og forsyning.</span><span class="sxs-lookup"><span data-stu-id="df22d-105">This overview introduces you to the public sector Procurement and sourcing functionality.</span></span> <span data-ttu-id="df22d-106">Dette omfatter indkøbsordrekoder, certificering kreditortyper, funktion til klassificering af købsaftaler og indkøbsordrelinjebeløb.</span><span class="sxs-lookup"><span data-stu-id="df22d-106">This includes purchase order codes, vendor certification types, purchase agreement classification functionality, and purchase order line amounts.</span></span>

<span data-ttu-id="df22d-107">I denne artikel beskrives de indkøbs- og forsyningsfunktioner, der er tilgængelige for den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="df22d-107">This article describes the Procurement and sourcing functionality that is available for the public sector.</span></span> 

## <a name="what-are-the-prerequisites-for-setting-up-procurement-and-sourcing-in-the-public-sector"></a><span data-ttu-id="df22d-108">Hvad er forudsætningerne for opsætning af indkøb og forsyning i den offentlige sektor?</span><span class="sxs-lookup"><span data-stu-id="df22d-108">What are the prerequisites for setting up Procurement and sourcing in the public sector?</span></span>
<span data-ttu-id="df22d-109">Før du begynder at justere indstillingerne og angive dine data, skal du:</span><span class="sxs-lookup"><span data-stu-id="df22d-109">Before you begin to adjust the settings and input your data, you should:</span></span>

-   <span data-ttu-id="df22d-110">Konfigurer leverandører</span><span class="sxs-lookup"><span data-stu-id="df22d-110">Set up vendors</span></span>
-   <span data-ttu-id="df22d-111">Definere nummereringssystemet for kreditorer, indkøbsordrer og så videre</span><span class="sxs-lookup"><span data-stu-id="df22d-111">Set up the numbering system for vendors, purchase orders, and so on</span></span>
-   <span data-ttu-id="df22d-112">Angiv certificeringstyper for kreditor.</span><span class="sxs-lookup"><span data-stu-id="df22d-112">Specify vendor certification types</span></span>

<span data-ttu-id="df22d-113">Du skal muligvis konfigurere følgende indkøbs- og forsyningsfunktioner for offentlige organisationer:</span><span class="sxs-lookup"><span data-stu-id="df22d-113">You may need to set up the following Procurement and sourcing features for public sector organizations:</span></span>

-    <span data-ttu-id="df22d-114">[Indkøbsordrekoder i den offentlige sektor](purchase-order-codes-public-sector.md) Opret koder og særlige meddelelser til bekræftelse af indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="df22d-114">[Public sector purchase order codes](purchase-order-codes-public-sector.md) Create codes and special messages for confirming purchase orders.</span></span> <span data-ttu-id="df22d-115">En bekræftende indkøbsordre omgår den typiske indkøbsproces.</span><span class="sxs-lookup"><span data-stu-id="df22d-115">A confirming purchase order circumvents the typical purchasing process.</span></span>

> [!NOTE]
> <span data-ttu-id="df22d-116">Dette gælder også for Kreditor.</span><span class="sxs-lookup"><span data-stu-id="df22d-116">This also applies to Accounts payable.</span></span>

-   [<span data-ttu-id="df22d-117">Regnskab i den offentlige sektor i Frankrig</span><span class="sxs-lookup"><span data-stu-id="df22d-117">Public sector accounting in France</span></span>](../localizations/emea-fra-public-sector-accounting.md) 

<span data-ttu-id="df22d-118">For franske organisationer kan yderligere trin være nødvendige for den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="df22d-118">For French organizations, additional steps may be required for the public sector.</span></span>

<span data-ttu-id="df22d-119">I de følgende afsnit beskrives de indkøbs- og forsyningsfunktioner, der er tilgængelige for den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="df22d-119">The following sections describe the Procurement and sourcing features that are available for the public sector.</span></span>

## <a name="what-are-vendor-certification-types"></a><span data-ttu-id="df22d-120">Hvad er kreditorcertificeringstyper?</span><span class="sxs-lookup"><span data-stu-id="df22d-120">What are vendor certification types?</span></span>
<span data-ttu-id="df22d-121">Du kan oprette og tildele enhver type certificering, som kreditorer kan have, til kreditororganisationer.</span><span class="sxs-lookup"><span data-stu-id="df22d-121">You can create and assign to vendor organizations any types of certification that the vendors hold.</span></span> <span data-ttu-id="df22d-122">Dette omfatter ikke kun professionelle legitimationsoplysninger som en professionel teknikers licens eller Microsoft SQL Server-certificering, men også om de har ansvarsforsikring, minoritetsstatus eller overholder forskellige miljømæssige eller forbrugermæssige sikkerhedsstandarder.</span><span class="sxs-lookup"><span data-stu-id="df22d-122">This includes not only professional credentials, such as a professional engineer’s license or Microsoft SQL Server Certification, but also whether they have liability insurance, minority status, or are in compliance with various environmental or consumer safety standards.</span></span> 

<span data-ttu-id="df22d-123">Du kan bruge siden **Certificeringstype** i modulet Kreditor til at angive certificeringstypen og -beskrivelsen.</span><span class="sxs-lookup"><span data-stu-id="df22d-123">You use the **Certification type** page in Accounts payable to enter the certification type and the description.</span></span>

## <a name="what-do-i-need-to-know-about-purchase-or-sales-agreement-classifications"></a><span data-ttu-id="df22d-124">Værd at vide om købs- eller salgsaftaleklassifikationer</span><span class="sxs-lookup"><span data-stu-id="df22d-124">What do I need to know about purchase or sales agreement classifications?</span></span>
<span data-ttu-id="df22d-125">Når brugere opretter en ny købsaftale eller salgsaftale, skal de altid vælge typen købsaftale eller salgsaftale.</span><span class="sxs-lookup"><span data-stu-id="df22d-125">When users create a new purchase agreement or sales agreement, they must always select the type of purchase agreement or sales agreement.</span></span> <span data-ttu-id="df22d-126">Yderligere kontroller til den offentlige sektor er tilgængelige på siden **Aftaleklassifikationer**.</span><span class="sxs-lookup"><span data-stu-id="df22d-126">Additional public sector controls are available on the **Agreement classifications** pages.</span></span> 

<span data-ttu-id="df22d-127">For at oprette og angive aftaleklassifikationer skal du bruge siden **Købsaftaleklassifikation** i Indkøb og forsyning eller siden **Salgsaftaleklassifikation** i Salg og marketing.</span><span class="sxs-lookup"><span data-stu-id="df22d-127">To create and specify agreement classifications, you use the **Purchase agreement classification** page in Procurement and sourcing or the **Sales agreement classification** page in Sales and marketing.</span></span> 

<span data-ttu-id="df22d-128">Tag følgende oplysninger i betragtning, når du angiver oplysninger om købs- eller salgsaftaleklassifikationer.</span><span class="sxs-lookup"><span data-stu-id="df22d-128">Take the following information into account when specifying details for purchase or sales agreement classifications.</span></span>

### <a name="how-do-i-enter-information-about-subcontractors-on-purchase-agreements"></a><span data-ttu-id="df22d-129">Hvordan angiver jeg oplysninger om underleverandører i købsaftaler?</span><span class="sxs-lookup"><span data-stu-id="df22d-129">How do I enter information about subcontractors on purchase agreements?</span></span>

<span data-ttu-id="df22d-130">Vælg indstillingen **Underleverandører**.</span><span class="sxs-lookup"><span data-stu-id="df22d-130">Select the **Subcontractors** option.</span></span>

### <a name="how-do-i-enter-information-about-insurance-policies-and-bonds-on-purchase-agreements"></a><span data-ttu-id="df22d-131">Hvordan indtaster jeg oplysninger om forsikringspolicerne og obligationer i købsaftaler?</span><span class="sxs-lookup"><span data-stu-id="df22d-131">How do I enter information about insurance policies and bonds on purchase agreements?</span></span>

<span data-ttu-id="df22d-132">Vælg indstillingen **Certificeringer**.</span><span class="sxs-lookup"><span data-stu-id="df22d-132">Select the **Certifications** option.</span></span> <span data-ttu-id="df22d-133">Oplysningerne kan bruges til at oprette en rapport, du kan bruge til at overvåge kreditorens overholdelse af bestemte krav.</span><span class="sxs-lookup"><span data-stu-id="df22d-133">The information can be used to generate a report that you can use to monitor vendor compliance with certification requirements.</span></span> <span data-ttu-id="df22d-134">(For at generere rapporten skal du gå til siden **Certificeringsoverholdelse ved købsaftale**).</span><span class="sxs-lookup"><span data-stu-id="df22d-134">(To generate the report, go to the **Purchase agreement certification compliance** page.)</span></span>

### <a name="how-do-i-enter-information-about-milestones-and-tasks-on-purchase-agreements"></a><span data-ttu-id="df22d-135">Hvordan angiver jeg oplysninger om milepæle og opgaver i købsaftaler?</span><span class="sxs-lookup"><span data-stu-id="df22d-135">How do I enter information about milestones and tasks on purchase agreements?</span></span>

<span data-ttu-id="df22d-136">Vælg indstillingen **Aktiviteter**.</span><span class="sxs-lookup"><span data-stu-id="df22d-136">Select the **Activities** option.</span></span>

### <a name="how-do-i-require-direct-invoicing-and-prevent-the-use-of-release-orders-with-purchase-agreements"></a><span data-ttu-id="df22d-137">Hvordan kræver jeg direkte fakturering og forhindrer brug af aftræksordrer i købsaftaler?</span><span class="sxs-lookup"><span data-stu-id="df22d-137">How do I require direct invoicing and prevent the use of release orders with purchase agreements?</span></span>

<span data-ttu-id="df22d-138">Vælg indstillingen **Kræv direkte fakturering**.</span><span class="sxs-lookup"><span data-stu-id="df22d-138">Select the **Require direct invoicing** option.</span></span> 

## <a name="can-i-view-purchase-order-line-amounts"></a><span data-ttu-id="df22d-139">Kan jeg få vist linjebeløb for indkøbsordre?</span><span class="sxs-lookup"><span data-stu-id="df22d-139">Can I view purchase order line amounts?</span></span>
<span data-ttu-id="df22d-140">Ja.</span><span class="sxs-lookup"><span data-stu-id="df22d-140">Yes.</span></span> <span data-ttu-id="df22d-141">Du kan få vist linjeantal for en indkøbsordre, herunder det aktuelle ordreantal og eventuelle antal, der er modtaget eller faktureret.</span><span class="sxs-lookup"><span data-stu-id="df22d-141">Line amounts for a purchase order can be viewed, including the current ordered amount and any amounts that have been received or invoiced.</span></span> <span data-ttu-id="df22d-142">Du kan også få vist antal, der endnu ikke er faktureret, eller antal for fakturaer, der afventer.</span><span class="sxs-lookup"><span data-stu-id="df22d-142">They can also view any amounts that remain to be invoiced or amounts for pending invoices.</span></span>

### <a name="tip"></a><span data-ttu-id="df22d-143">Tip!</span><span class="sxs-lookup"><span data-stu-id="df22d-143">Tip</span></span>

<span data-ttu-id="df22d-144">Lad os sige, at du får vist en indkøbsordrelinje med indkøb, der er bogført på to finanskonti.</span><span class="sxs-lookup"><span data-stu-id="df22d-144">Let’s say you view a purchase order line with purchases posted to two ledger accounts.</span></span> <span data-ttu-id="df22d-145">Den ene finanskonto er beregnet til kontormøbler, der er bestilt hos en leverandør.</span><span class="sxs-lookup"><span data-stu-id="df22d-145">One ledger account is for office furniture ordered from a vendor.</span></span> <span data-ttu-id="df22d-146">Den anden finanskonto er beregnet til kontorartikler.</span><span class="sxs-lookup"><span data-stu-id="df22d-146">The second ledger account is for office supplies.</span></span> <span data-ttu-id="df22d-147">Ordreantallet er lig med summen af fakturerede antal, antallet på ventende fakturaer og antal, der ikke er faktureret endnu.</span><span class="sxs-lookup"><span data-stu-id="df22d-147">The ordered amount is equal to the sum of the invoiced amounts, pending invoice amounts, and invoice remaining amounts.</span></span> <span data-ttu-id="df22d-148">Det modtagne antal er den del af ordreantallet, der er modtaget fra kreditor.</span><span class="sxs-lookup"><span data-stu-id="df22d-148">The received amount is the portion of the ordered amount that has been received from the vendor.</span></span>

<table style="width:100%;">

<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />

<tbody>
<tr class="odd">
<td><span data-ttu-id="df22d-149"><strong>Finanskonto</strong></span><span class="sxs-lookup"><span data-stu-id="df22d-149"><strong>Ledger account</strong></span></span></td>
<td><span data-ttu-id="df22d-150"><strong>Bestilt</strong></span><span class="sxs-lookup"><span data-stu-id="df22d-150"><strong>Ordered</strong></span></span></td>
<td><span data-ttu-id="df22d-151"><strong>Modtaget</strong></span><span class="sxs-lookup"><span data-stu-id="df22d-151"><strong>Received</strong></span></span></td>
<td><span data-ttu-id="df22d-152"><strong>Faktureret</strong></span><span class="sxs-lookup"><span data-stu-id="df22d-152"><strong>Invoiced</strong></span></span></td>
<td><span data-ttu-id="df22d-153"><strong>Ventende faktura</strong></span><span class="sxs-lookup"><span data-stu-id="df22d-153"><strong>Pending invoice</strong></span></span></td>
<td><span data-ttu-id="df22d-154"><strong>Fakturarest</strong></span><span class="sxs-lookup"><span data-stu-id="df22d-154"><strong>Invoice remaining</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df22d-155">60010 (kontormøbler)</span><span class="sxs-lookup"><span data-stu-id="df22d-155">60010 (office furniture)</span></span></td>
<td><p><span data-ttu-id="df22d-156">1.200,00</span><span class="sxs-lookup"><span data-stu-id="df22d-156">1,200.00</span></span></p></td>
<td><span data-ttu-id="df22d-157">250,00</span><span class="sxs-lookup"><span data-stu-id="df22d-157">250.00</span></span></td>
<td><span data-ttu-id="df22d-158">350,00</span><span class="sxs-lookup"><span data-stu-id="df22d-158">350.00</span></span></td>
<td><span data-ttu-id="df22d-159">200,00</span><span class="sxs-lookup"><span data-stu-id="df22d-159">200.00</span></span></td>
<td><p><span data-ttu-id="df22d-160">650,00</span><span class="sxs-lookup"><span data-stu-id="df22d-160">650.00</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df22d-161">60020 (kontorartikler)</span><span class="sxs-lookup"><span data-stu-id="df22d-161">60020 (office supplies)</span></span></td>
<td><p><span data-ttu-id="df22d-162">750,00</span><span class="sxs-lookup"><span data-stu-id="df22d-162">750.00</span></span></p></td>
<td><span data-ttu-id="df22d-163">150,00</span><span class="sxs-lookup"><span data-stu-id="df22d-163">150.00</span></span></td>
<td><span data-ttu-id="df22d-164">400,00</span><span class="sxs-lookup"><span data-stu-id="df22d-164">400.00</span></span></td>
<td></td>
<td><p><span data-ttu-id="df22d-165">350,00</span><span class="sxs-lookup"><span data-stu-id="df22d-165">350.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df22d-166">I alt</span><span class="sxs-lookup"><span data-stu-id="df22d-166">Totals</span></span></td>
<td><p><span data-ttu-id="df22d-167">1.950,00</span><span class="sxs-lookup"><span data-stu-id="df22d-167">1,950.00</span></span></p></td>
<td><span data-ttu-id="df22d-168">400,00</span><span class="sxs-lookup"><span data-stu-id="df22d-168">400.00</span></span></td>
<td><span data-ttu-id="df22d-169">750,00</span><span class="sxs-lookup"><span data-stu-id="df22d-169">750.00</span></span></td>
<td><span data-ttu-id="df22d-170">200,00</span><span class="sxs-lookup"><span data-stu-id="df22d-170">200.00</span></span></td>
<td><p><span data-ttu-id="df22d-171">1.000,00</span><span class="sxs-lookup"><span data-stu-id="df22d-171">1,000.00</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="df22d-172">Du kan finde yderligere oplysninger i [Kreditorbetalinger i den offentlige sektor](../../supply-chain/procurement/procurement-sourcing-overview.md) og [Indkøb og forsyning i den offentlige sektor](accounts-payable-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="df22d-172">For more information, see [Procurement and sourcing](../../supply-chain/procurement/procurement-sourcing-overview.md) and [Accounts payable in the public sector](accounts-payable-public-sector.md).</span></span>




