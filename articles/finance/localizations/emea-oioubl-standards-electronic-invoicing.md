---
title: Understøttede standarder til elektronisk fakturering i Europa
description: I dette emne beskrives det dækningsniveau, der findes for elektronisk fakturering for Europa.
author: mrolecki
manager: AnnBe
ms.date: 09/03/2020
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
ms.openlocfilehash: c86cc90e5f441641bc14d20898e65325d7c7d716
ms.sourcegitcommit: 1ca48d95fbff2555307cc1e5e5e23feea79a8bc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/03/2020
ms.locfileid: "3763680"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a><span data-ttu-id="e5ad6-103">Understøttede standarder til elektronisk fakturering i Europa</span><span class="sxs-lookup"><span data-stu-id="e5ad6-103">Supported standards for electronic invoicing in Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5ad6-104">I dette emne beskrives det dækningsniveau, der findes for elektronisk fakturering for Europa.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-104">This topic explains the level of coverage that exists for electronic invoicing for Europe.</span></span> 

<span data-ttu-id="e5ad6-105">Implementering og indførelse overalt i EU af elektronisk fakturering er reguleret [Rådets direktiv 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), hvilket har indflydelse på alle EU-medlemsstater.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-105">Implementation and adoption of European Union-wide electronic invoicing is regulated [Council Directive 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), which affects all EU member states.</span></span> <span data-ttu-id="e5ad6-106">Virksomheder, der gerne vil have fordel af elektronisk fakturering, skal sende salgsordrefakturaer, fritekstfakturaer, projektfakturaer, kreditnotaer for salgsordre og kreditnotaer for projektfakturaer som .XML-filer til offentlige myndigheder eller andre handelspartnere, der bemyndiger anvendelse af elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-106">Companies that want to benefit from electronic invoicing must submit sales order invoices, free text invoices, project invoices, sales order credit notes, and project invoice credit notes as .xml files to the government or other trading parties that mandate use of electronic invoicing.</span></span> <span data-ttu-id="e5ad6-107">Disse .XML-filer skal opfylde bestemte standarder.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-107">These .xml files must comply with certain standards.</span></span> <span data-ttu-id="e5ad6-108">Landespecifikke krav og deres gennemførelse kan variere på tværs af EU-medlemsstaterne, men ofte bruger de Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) i forskellige versioner med tilpasninger samt [PEPPOL](https://www.peppol.eu)-specifikationer og adgangspunkter til validering og transport.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-108">The country-specific requirements and their implementation may differ across EU member states but commonly they are using Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in different versions with customizations as well as [PEPPOL](https://www.peppol.eu) specifications and access points for validation and transportation.</span></span> <span data-ttu-id="e5ad6-109">Den primære fordel ved UBL er, at forretningsdokumenter kan standardiseres til forskellige formål.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-109">The primary advantage of UBL is that business documents can be standardized for different purposes.</span></span> <span data-ttu-id="e5ad6-110">Da UBL er en fleksibel, international standard, der understøtter mange forretningsmæssige krav, kan disse forretningsdokumenter udveksles på tværs af nationale grænser.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-110">Because UBL is a flexible, international standard that supports many business requirements, these business documents can be exchanged across national borders.</span></span>

## <a name="electronic-invoice-formats-currently-available-in-dynamics-365-finance"></a><span data-ttu-id="e5ad6-111">Elektroniske fakturaformater, der i øjeblikket er tilgængelige i Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="e5ad6-111">Electronic invoice formats currently available in Dynamics 365 Finance</span></span>

<span data-ttu-id="e5ad6-112">Der findes følgende landespecifikke formater for elektroniske fakturaer:</span><span class="sxs-lookup"><span data-stu-id="e5ad6-112">The following country-specific formats of electronic invoices are available:</span></span>

-   <span data-ttu-id="e5ad6-113">OIOUBL-v.2.02 for Danmark</span><span class="sxs-lookup"><span data-stu-id="e5ad6-113">OIOUBL v.2.02 for Denmark</span></span>
-   <span data-ttu-id="e5ad6-114">EHF v.3.0 for Norge</span><span class="sxs-lookup"><span data-stu-id="e5ad6-114">EHF v.3.0 for Norway</span></span>
-   <span data-ttu-id="e5ad6-115">PEPPOL BIS v.2 for Østrig, Frankrig og Belgien</span><span class="sxs-lookup"><span data-stu-id="e5ad6-115">PEPPOL BIS v.2 for Austria, France, and Belgium</span></span>
-   <span data-ttu-id="e5ad6-116">UBL-OHNL 1.9 for Nederlandene</span><span class="sxs-lookup"><span data-stu-id="e5ad6-116">UBL-OHNL 1.9 for the Netherlands</span></span>
-   <span data-ttu-id="e5ad6-117">FacturaE v.3.2.1 for Spanien</span><span class="sxs-lookup"><span data-stu-id="e5ad6-117">FacturaE v.3.2.1 for Spain</span></span>
-   <span data-ttu-id="e5ad6-118">FatturaPA v.1.2 for Italien</span><span class="sxs-lookup"><span data-stu-id="e5ad6-118">FatturaPA v.1.2 for Italy</span></span>
-   <span data-ttu-id="e5ad6-119">xRechnung v.1.2 for Tyskland</span><span class="sxs-lookup"><span data-stu-id="e5ad6-119">xRechnung v.1.2 for Germany</span></span>
-   <span data-ttu-id="e5ad6-120">Åbn PEPPOL BIS Billing v.3.0 for Den Europæiske Union</span><span class="sxs-lookup"><span data-stu-id="e5ad6-120">Open PEPPOL BIS Billing v.3.0 for European Union</span></span>
-   <span data-ttu-id="e5ad6-121">Estisk specifikt format version 1.2</span><span class="sxs-lookup"><span data-stu-id="e5ad6-121">Estonian specific format version 1.2</span></span>
-   <span data-ttu-id="e5ad6-122">Finvoice 3.0 for Finland</span><span class="sxs-lookup"><span data-stu-id="e5ad6-122">Finvoice 3.0 for Finland</span></span>

<span data-ttu-id="e5ad6-123">Elektronisk fakturering er baseret på [Elektronisk indberetning (ER)](../../dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="e5ad6-123">Electronic invoicing is based on [Electronic reporting (ER)](../../dev-itpro/analytics/general-electronic-reporting.md).</span></span> <span data-ttu-id="e5ad6-124">Der er blevet oprettet en **Fakturamodel** som datamodel, tilknytning af fakturamodel og flere lande-/områdespecifikke ER-formatkonfigurationer for Østrig (AT), Danmark (DK), Italien (IT), Norge (NO), Spanien (ES), Frankrig (FR), Belgien (BE), Nederlandene (NL), Tyskland (DE), Estland (EE), Finland (FI) samt Den Europæiske Union (EU).</span><span class="sxs-lookup"><span data-stu-id="e5ad6-124">An **Invoice model** data model, invoice model mapping, and several country/region-specific ER format configurations have been created for Austria (AT), Denmark (DK), Italy (IT), Norway (NO), Spain (ES), France (FR), Belgium (BE), the Netherlands (NL), Germany (DE), Estonia (EE), Finland (FI), and the European Union (EU).</span></span>

-   <span data-ttu-id="e5ad6-125">OIOUBL salgsfaktura - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="e5ad6-125">OIOUBL Sales invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="e5ad6-126">OIOUBL salgskreditnota - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="e5ad6-126">OIOUBL Sales credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="e5ad6-127">OIOUBL projektfaktura - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="e5ad6-127">OIOUBL Project invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="e5ad6-128">OIOUBL projektkreditnota - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="e5ad6-128">OIOUBL Project credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="e5ad6-129">UBL-salgsfaktura FR</span><span class="sxs-lookup"><span data-stu-id="e5ad6-129">UBL Sales Invoice FR</span></span>
-   <span data-ttu-id="e5ad6-130">UBL-salgskreditnota FR</span><span class="sxs-lookup"><span data-stu-id="e5ad6-130">UBL Sales Credit Note FR</span></span>
-   <span data-ttu-id="e5ad6-131">UBL-projektfaktura FR</span><span class="sxs-lookup"><span data-stu-id="e5ad6-131">UBL Project Invoice FR</span></span>
-   <span data-ttu-id="e5ad6-132">UBL-projektkreditnota FR</span><span class="sxs-lookup"><span data-stu-id="e5ad6-132">UBL Project Credit Note FR</span></span>
-   <span data-ttu-id="e5ad6-133">UBL-salgsfaktura BE</span><span class="sxs-lookup"><span data-stu-id="e5ad6-133">UBL Sales Invoice BE</span></span>
-   <span data-ttu-id="e5ad6-134">UBL-salgskreditnota BE</span><span class="sxs-lookup"><span data-stu-id="e5ad6-134">UBL Sales Credit Note BE</span></span>
-   <span data-ttu-id="e5ad6-135">UBL-projektfaktura BE</span><span class="sxs-lookup"><span data-stu-id="e5ad6-135">UBL Project Invoice BE</span></span>
-   <span data-ttu-id="e5ad6-136">UBL-projektkreditnota BE</span><span class="sxs-lookup"><span data-stu-id="e5ad6-136">UBL Project Credit Note BE</span></span>
-   <span data-ttu-id="e5ad6-137">UBL-salgsfaktura NL</span><span class="sxs-lookup"><span data-stu-id="e5ad6-137">UBL Sales Invoice NL</span></span>
-   <span data-ttu-id="e5ad6-138">UBL-salgskreditnota NL</span><span class="sxs-lookup"><span data-stu-id="e5ad6-138">UBL Sales Credit Note NL</span></span>
-   <span data-ttu-id="e5ad6-139">UBL-projektfaktura NL</span><span class="sxs-lookup"><span data-stu-id="e5ad6-139">UBL Project Invoice NL</span></span>
-   <span data-ttu-id="e5ad6-140">UBL-projektkreditnota NL</span><span class="sxs-lookup"><span data-stu-id="e5ad6-140">UBL Project Credit Note NL</span></span> 
-   <span data-ttu-id="e5ad6-141">Salgsfaktura (ES)</span><span class="sxs-lookup"><span data-stu-id="e5ad6-141">Sales invoice (ES)</span></span>
-   <span data-ttu-id="e5ad6-142">Salgsfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="e5ad6-142">Sales invoice (IT)</span></span>
-   <span data-ttu-id="e5ad6-143">Projektfaktura (ES)</span><span class="sxs-lookup"><span data-stu-id="e5ad6-143">Project invoice (ES)</span></span>
-   <span data-ttu-id="e5ad6-144">Projektfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="e5ad6-144">Project invoice (IT)</span></span>
-   <span data-ttu-id="e5ad6-145">Salgsfaktura DE</span><span class="sxs-lookup"><span data-stu-id="e5ad6-145">Sales Invoice DE</span></span>
-   <span data-ttu-id="e5ad6-146">Projektfaktura DE</span><span class="sxs-lookup"><span data-stu-id="e5ad6-146">Project Invoice DE</span></span>
-   <span data-ttu-id="e5ad6-147">Peppol Salgsfaktura - for EU</span><span class="sxs-lookup"><span data-stu-id="e5ad6-147">Peppol Sales Invoice - for EU</span></span>
-   <span data-ttu-id="e5ad6-148">Peppol Salgskreditnota - for EU</span><span class="sxs-lookup"><span data-stu-id="e5ad6-148">Peppol Sales Credit Note - for EU</span></span>
-   <span data-ttu-id="e5ad6-149">Peppol Projektfaktura - for EU</span><span class="sxs-lookup"><span data-stu-id="e5ad6-149">Peppol Project Invoice - for EU</span></span>
-   <span data-ttu-id="e5ad6-150">Peppol Projektkreditnota - for EU</span><span class="sxs-lookup"><span data-stu-id="e5ad6-150">Peppol Project Credit Note - for EU</span></span>
-   <span data-ttu-id="e5ad6-151">Salgsfaktura (EE)</span><span class="sxs-lookup"><span data-stu-id="e5ad6-151">Sales invoice (EE)</span></span>
-   <span data-ttu-id="e5ad6-152">Projektfaktura (EE)</span><span class="sxs-lookup"><span data-stu-id="e5ad6-152">Project invoice (EE)</span></span>
-   <span data-ttu-id="e5ad6-153">Salgsfaktura (FI)</span><span class="sxs-lookup"><span data-stu-id="e5ad6-153">Sales invoice (FI)</span></span>
-   <span data-ttu-id="e5ad6-154">Projektfaktura (FI)</span><span class="sxs-lookup"><span data-stu-id="e5ad6-154">Project invoice (FI)</span></span>

<span data-ttu-id="e5ad6-155">De elektroniske fakturaer og kreditnotaer, som du genererer, omfatter nødvendige oplysninger som et europæisk varenummer (EAN) og oplysninger om kontakt, dimensionskontonummer og adresse til kunden.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-155">The electronic invoices and credit notes that you generate include required information, such as a European Article Numbering (EAN) number, contact person, dimension account number, and address information for the customer.</span></span> <span data-ttu-id="e5ad6-156">Der anvendes valideringsregler, når der genereres fakturaer, så du kan kontrollere, at de korrekte oplysninger er angivet.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-156">Validation rules are applied when invoices are generated so you can verify that the correct information has been entered.</span></span> <span data-ttu-id="e5ad6-157">Sættet af nødvendige oplysninger kan variere fra land til land.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-157">The set of required information may differ from country to country.</span></span> <span data-ttu-id="e5ad6-158">Da både kravene og de understøttede lande og formater kan blive ændret, bør du altid gå til det delte aktivbibliotek i Microsoft Dynamics Lifecycle Services (LCS) og få vist den seneste liste over tilgængelige filer, som har aktivtypen **GER-konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-158">Because the requirements, as well as supported countries and formats, is subject to change, you should always go to the Shared asset library on Microsoft Dynamics Lifecycle services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5ad6-159">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e5ad6-159">Additional resources</span></span>
<span data-ttu-id="e5ad6-160">Du kan få flere oplysninger om opsætning af elektroniske fakturaer ved at afspille følgende [opgaveguider](../../fin-and-ops/get-started/help-overview.md#task-guides) i ruden Hjælp:</span><span class="sxs-lookup"><span data-stu-id="e5ad6-160">For more details about how to set up electronic invoices, you can play the following [Task guides](../../fin-and-ops/get-started/help-overview.md#task-guides) in the Help pane:</span></span>

 - <span data-ttu-id="e5ad6-161">Konfigurere elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="e5ad6-161">Set up OIOUBL electronic invoicing</span></span>
 - <span data-ttu-id="e5ad6-162">Importere OIOUBL elektroniske faktureringskonfigurationer</span><span class="sxs-lookup"><span data-stu-id="e5ad6-162">Import OIOUBL electronic invoicing configurations</span></span>
 - <span data-ttu-id="e5ad6-163">Konfigurere debitorkonti til elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="e5ad6-163">Set up customer accounts for OIOUBL electronic invoicing</span></span>

> [!NOTE] 
> <span data-ttu-id="e5ad6-164">Selvom disse opgaveguider er oprettet specifikt til det danske e-fakturaformat *OIOUBL*, gælder de også for andre understøttede lande/områder, med mindre afvigelser.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-164">Although these Task guides were created for Danish-specific e-invoice format *OIOUBL*, they are applicable for other supported countries with minor deviations.</span></span>
