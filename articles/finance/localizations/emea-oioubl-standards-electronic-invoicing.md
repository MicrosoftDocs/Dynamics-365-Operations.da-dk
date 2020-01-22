---
title: Understøttede standarder til elektronisk fakturering i Europa
description: I dette emne beskrives det dækningsniveau, der findes for elektronisk fakturering for Europa.
author: mrolecki
manager: AnnBe
ms.date: 07/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 10274
ms.search.region: Austria, Denmark, Italy, Norway, Spain, France, Belgium, Netherlands
ms.search.industry: ''
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2fb188498705dcbad841645ced43e6a1715cbbd0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915160"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a><span data-ttu-id="eaaac-103">Understøttede standarder til elektronisk fakturering i Europa</span><span class="sxs-lookup"><span data-stu-id="eaaac-103">Supported standards for electronic invoicing in Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eaaac-104">I dette emne beskrives det dækningsniveau, der findes for elektronisk fakturering for Europa.</span><span class="sxs-lookup"><span data-stu-id="eaaac-104">This topic explains the level of coverage that exists for electronic invoicing for Europe.</span></span> 

<span data-ttu-id="eaaac-105">Implementering og indførelse overalt i EU af elektronisk fakturering er reguleret [Rådets direktiv 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), hvilket har indflydelse på alle EU-medlemsstater.</span><span class="sxs-lookup"><span data-stu-id="eaaac-105">Implementation and adoption of European Union-wide electronic invoicing is regulated [Council Directive 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), which affects all EU member states.</span></span> <span data-ttu-id="eaaac-106">Virksomheder, der gerne vil have fordel af elektronisk fakturering, skal sende salgsordrefakturaer, fritekstfakturaer, projektfakturaer, kreditnotaer for salgsordre og kreditnotaer for projektfakturaer som .XML-filer til offentlige myndigheder eller andre handelspartnere, der bemyndiger anvendelse af elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="eaaac-106">Companies that want to benefit from electronic invoicing must submit sales order invoices, free text invoices, project invoices, sales order credit notes, and project invoice credit notes as .xml files to the government or other trading parties that mandate use of electronic invoicing.</span></span> <span data-ttu-id="eaaac-107">Disse .XML-filer skal opfylde bestemte standarder.</span><span class="sxs-lookup"><span data-stu-id="eaaac-107">These .xml files must comply with certain standards.</span></span> <span data-ttu-id="eaaac-108">Landespecifikke krav og deres gennemførelse kan variere på tværs af EU-medlemsstaterne, men ofte bruger de Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) i forskellige versioner med tilpasninger samt [PEPPOL](https://www.peppol.eu)-specifikationer og adgangspunkter til validering og transport.</span><span class="sxs-lookup"><span data-stu-id="eaaac-108">The country-specific requirements and their implementation may differ across EU member states but commonly they are using Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in different versions with customizations as well as [PEPPOL](https://www.peppol.eu) specifications and access points for validation and transportation.</span></span> <span data-ttu-id="eaaac-109">Den primære fordel ved UBL er, at forretningsdokumenter kan standardiseres til forskellige formål.</span><span class="sxs-lookup"><span data-stu-id="eaaac-109">The primary advantage of UBL is that business documents can be standardized for different purposes.</span></span> <span data-ttu-id="eaaac-110">Da UBL er en fleksibel, international standard, der understøtter mange forretningsmæssige krav, kan disse forretningsdokumenter udveksles på tværs af nationale grænser.</span><span class="sxs-lookup"><span data-stu-id="eaaac-110">Because UBL is a flexible, international standard that supports many business requirements, these business documents can be exchanged across national borders.</span></span>

## <a name="what-electronic-invoice-formats-are-currently-available-in-dynamics-365-finance"></a><span data-ttu-id="eaaac-111">Hvilke elektroniske fakturaformater er i øjeblikket tilgængelige i Dynamics 365 Finance?</span><span class="sxs-lookup"><span data-stu-id="eaaac-111">What electronic invoice formats are currently available in Dynamics 365 Finance?</span></span>

<span data-ttu-id="eaaac-112">Der findes følgende landespecifikke formater for elektroniske fakturaer:</span><span class="sxs-lookup"><span data-stu-id="eaaac-112">The following country-specific formats of electronic invoices are available:</span></span>

-   <span data-ttu-id="eaaac-113">OIOUBL-v.2.02 for Danmark</span><span class="sxs-lookup"><span data-stu-id="eaaac-113">OIOUBL v.2.02 for Denmark</span></span>
-   <span data-ttu-id="eaaac-114">EHF v.3.0 for Norge</span><span class="sxs-lookup"><span data-stu-id="eaaac-114">EHF v.3.0 for Norway</span></span>
-   <span data-ttu-id="eaaac-115">PEPPOL BIS v.2 for Østrig, Frankrig og Belgien</span><span class="sxs-lookup"><span data-stu-id="eaaac-115">PEPPOL BIS v.2 for Austria, France, and Belgium</span></span>
-   <span data-ttu-id="eaaac-116">UBL-OHNL 1.9 for Nederlandene</span><span class="sxs-lookup"><span data-stu-id="eaaac-116">UBL-OHNL 1.9 for the Netherlands</span></span>
-   <span data-ttu-id="eaaac-117">FacturaE v.3.2.1 for Spanien</span><span class="sxs-lookup"><span data-stu-id="eaaac-117">FacturaE v.3.2.1 for Spain</span></span>
-   <span data-ttu-id="eaaac-118">FatturaPA v.1.2 for Italien</span><span class="sxs-lookup"><span data-stu-id="eaaac-118">FatturaPA v.1.2 for Italy</span></span>
-   <span data-ttu-id="eaaac-119">xRechnung v.1.2 for Tyskland</span><span class="sxs-lookup"><span data-stu-id="eaaac-119">xRechnung v.1.2 for Germany</span></span>
-   <span data-ttu-id="eaaac-120">Åbn PEPPOL BIS Billing v.3.0 for Den Europæiske Union</span><span class="sxs-lookup"><span data-stu-id="eaaac-120">Open PEPPOL BIS Billing v.3.0 for European Union</span></span>

<span data-ttu-id="eaaac-121">Elektronisk fakturering er baseret på [Elektronisk indberetning (ER)](../../dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="eaaac-121">Electronic invoicing is based on [Electronic reporting (ER)](../../dev-itpro/analytics/general-electronic-reporting.md).</span></span> <span data-ttu-id="eaaac-122">Der er blevet oprettet en **Debitorfakturamodel**-datamodel og adskillige lande-/regionspecifikke ER-formatkonfigurationer for Østrig (AT), Danmark (DK), Italien (IT), Norge (NO), Spanien (ES), Frankrig (FR), Belgien (BE), Nederlandene (NL) og Tyskland (DE) samt Den Europæiske Union (EU).</span><span class="sxs-lookup"><span data-stu-id="eaaac-122">A **Customer invoice model** data model and several country/region-specific ER format configurations have been created for Austria (AT), Denmark (DK), Italy (IT), Norway (NO), Spain (ES), France (FR), Belgium (BE), the Netherlands (NL), Germany (DE), and the European Union (EU).</span></span>

-   <span data-ttu-id="eaaac-123">OIOUBL salgsfaktura - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="eaaac-123">OIOUBL Sales invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="eaaac-124">OIOUBL salgskreditnota - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="eaaac-124">OIOUBL Sales credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="eaaac-125">OIOUBL projektfaktura - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="eaaac-125">OIOUBL Project invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="eaaac-126">OIOUBL projektkreditnota - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="eaaac-126">OIOUBL Project credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="eaaac-127">UBL-salgsfaktura FR</span><span class="sxs-lookup"><span data-stu-id="eaaac-127">UBL Sales Invoice FR</span></span>
-   <span data-ttu-id="eaaac-128">UBL-salgskreditnota FR</span><span class="sxs-lookup"><span data-stu-id="eaaac-128">UBL Sales Credit Note FR</span></span>
-   <span data-ttu-id="eaaac-129">UBL-projektfaktura FR</span><span class="sxs-lookup"><span data-stu-id="eaaac-129">UBL Project Invoice FR</span></span>
-   <span data-ttu-id="eaaac-130">UBL-projektkreditnota FR</span><span class="sxs-lookup"><span data-stu-id="eaaac-130">UBL Project Credit Note FR</span></span>
-   <span data-ttu-id="eaaac-131">UBL-salgsfaktura BE</span><span class="sxs-lookup"><span data-stu-id="eaaac-131">UBL Sales Invoice BE</span></span>
-   <span data-ttu-id="eaaac-132">UBL-salgskreditnota BE</span><span class="sxs-lookup"><span data-stu-id="eaaac-132">UBL Sales Credit Note BE</span></span>
-   <span data-ttu-id="eaaac-133">UBL-projektfaktura BE</span><span class="sxs-lookup"><span data-stu-id="eaaac-133">UBL Project Invoice BE</span></span>
-   <span data-ttu-id="eaaac-134">UBL-projektkreditnota BE</span><span class="sxs-lookup"><span data-stu-id="eaaac-134">UBL Project Credit Note BE</span></span>
-   <span data-ttu-id="eaaac-135">UBL-salgsfaktura NL</span><span class="sxs-lookup"><span data-stu-id="eaaac-135">UBL Sales Invoice NL</span></span>
-   <span data-ttu-id="eaaac-136">UBL-salgskreditnota NL</span><span class="sxs-lookup"><span data-stu-id="eaaac-136">UBL Sales Credit Note NL</span></span>
-   <span data-ttu-id="eaaac-137">UBL-projektfaktura NL</span><span class="sxs-lookup"><span data-stu-id="eaaac-137">UBL Project Invoice NL</span></span>
-   <span data-ttu-id="eaaac-138">UBL-projektkreditnota NL</span><span class="sxs-lookup"><span data-stu-id="eaaac-138">UBL Project Credit Note NL</span></span> 
-   <span data-ttu-id="eaaac-139">Salgsfaktura (ES)</span><span class="sxs-lookup"><span data-stu-id="eaaac-139">Sales invoice (ES)</span></span>
-   <span data-ttu-id="eaaac-140">Salgsfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="eaaac-140">Sales invoice (IT)</span></span>
-   <span data-ttu-id="eaaac-141">Projektfaktura (ES)</span><span class="sxs-lookup"><span data-stu-id="eaaac-141">Project invoice (ES)</span></span>
-   <span data-ttu-id="eaaac-142">Projektfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="eaaac-142">Project invoice (IT)</span></span>
-   <span data-ttu-id="eaaac-143">Salgsfaktura DE</span><span class="sxs-lookup"><span data-stu-id="eaaac-143">Sales Invoice DE</span></span>
-   <span data-ttu-id="eaaac-144">Projektfaktura DE</span><span class="sxs-lookup"><span data-stu-id="eaaac-144">Project Invoice DE</span></span>
-   <span data-ttu-id="eaaac-145">Peppol Salgsfaktura - for EU</span><span class="sxs-lookup"><span data-stu-id="eaaac-145">Peppol Sales Invoice - for EU</span></span>
-   <span data-ttu-id="eaaac-146">Peppol Salgskreditnota - for EU</span><span class="sxs-lookup"><span data-stu-id="eaaac-146">Peppol Sales Credit Note - for EU</span></span>
-   <span data-ttu-id="eaaac-147">Peppol Projektfaktura - for EU</span><span class="sxs-lookup"><span data-stu-id="eaaac-147">Peppol Project Invoice - for EU</span></span>
-   <span data-ttu-id="eaaac-148">Peppol Projektkreditnota - for EU</span><span class="sxs-lookup"><span data-stu-id="eaaac-148">Peppol Project Credit Note - for EU</span></span>

<span data-ttu-id="eaaac-149">De elektroniske fakturaer og kreditnotaer, som du genererer, omfatter nødvendige oplysninger som et europæisk varenummer (EAN) og oplysninger om kontakt, dimensionskontonummer og adresse til kunden.</span><span class="sxs-lookup"><span data-stu-id="eaaac-149">The electronic invoices and credit notes that you generate include required information, such as a European Article Numbering (EAN) number, contact person, dimension account number, and address information for the customer.</span></span> <span data-ttu-id="eaaac-150">Der anvendes valideringsregler, når der genereres fakturaer, så du kan kontrollere, at de korrekte oplysninger er angivet.</span><span class="sxs-lookup"><span data-stu-id="eaaac-150">Validation rules are applied when invoices are generated so you can verify that the correct information has been entered.</span></span> <span data-ttu-id="eaaac-151">Sættet af nødvendige oplysninger kan variere fra land til land.</span><span class="sxs-lookup"><span data-stu-id="eaaac-151">The set of required information may differ from country to country.</span></span> <span data-ttu-id="eaaac-152">Da både kravene og de understøttede lande og formater kan blive ændret, bør du altid gå til det delte aktivbibliotek i Microsoft Dynamics Lifecycle Services (LCS) og få vist den seneste liste over tilgængelige filer, som har aktivtypen **GER-konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="eaaac-152">Because the requirements, as well as supported countries and formats, is subject to change, you should always go to the Shared asset library on Microsoft Dynamics Lifecycle services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span>

## <a name="additional-information"></a><span data-ttu-id="eaaac-153">Yderligere oplysninger</span><span class="sxs-lookup"><span data-stu-id="eaaac-153">Additional information</span></span>
<span data-ttu-id="eaaac-154">Du kan få flere oplysninger om opsætning af elektroniske fakturaer ved at afspille følgende [opgaveguider](../../fin-and-ops/get-started/help-overview.md#task-guides) i ruden Hjælp:</span><span class="sxs-lookup"><span data-stu-id="eaaac-154">For more details about how to set up electronic invoices, you can play the following [Task guides](../../fin-and-ops/get-started/help-overview.md#task-guides) in the Help pane:</span></span>

 - <span data-ttu-id="eaaac-155">Konfigurere elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="eaaac-155">Set up OIOUBL electronic invoicing</span></span>
 - <span data-ttu-id="eaaac-156">Importere OIOUBL elektroniske faktureringskonfigurationer</span><span class="sxs-lookup"><span data-stu-id="eaaac-156">Import OIOUBL electronic invoicing configurations</span></span>
 - <span data-ttu-id="eaaac-157">Konfigurere debitorkonti til elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="eaaac-157">Set up customer accounts for OIOUBL electronic invoicing</span></span>

> [!NOTE] 
> <span data-ttu-id="eaaac-158">Selvom disse opgaveguider er oprettet specifikt til det danske e-fakturaformat *OIOUBL*, gælder de også for andre understøttede lande, med mindre afvigelser.</span><span class="sxs-lookup"><span data-stu-id="eaaac-158">Although these Task guides were created for Danish-specific e-invoice format *OIOUBL*, they are applicable for other supported countries with minor deviations.</span></span>
