---
title: Understøttede standarder til elektronisk fakturering i Europa
description: I dette emne beskrives det dækningsniveau, der findes for elektronisk fakturering for Europa.
author: mrolecki
manager: AnnBe
ms.date: 11/19/2020
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
ms.openlocfilehash: 3ed98c268af841b1625f547c79f271f3e3a81b74
ms.sourcegitcommit: 3d16522c00ba2d30aa43befbf1b7b3eaad377325
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/20/2020
ms.locfileid: "4592463"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a><span data-ttu-id="dcafc-103">Understøttede standarder til elektronisk fakturering i Europa</span><span class="sxs-lookup"><span data-stu-id="dcafc-103">Supported standards for electronic invoicing in Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dcafc-104">I dette emne beskrives det dækningsniveau, der findes for elektronisk fakturering for Europa.</span><span class="sxs-lookup"><span data-stu-id="dcafc-104">This topic explains the level of coverage that exists for electronic invoicing for Europe.</span></span> 

<span data-ttu-id="dcafc-105">Implementering og indførelse overalt i EU af elektronisk fakturering er reguleret [Rådets direktiv 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), hvilket har indflydelse på alle EU-medlemsstater.</span><span class="sxs-lookup"><span data-stu-id="dcafc-105">Implementation and adoption of European Union-wide electronic invoicing is regulated [Council Directive 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), which affects all EU member states.</span></span> <span data-ttu-id="dcafc-106">Virksomheder, der gerne vil have fordel af elektronisk fakturering, skal sende salgsordrefakturaer, fritekstfakturaer, projektfakturaer, kreditnotaer for salgsordre og kreditnotaer for projektfakturaer som .XML-filer til offentlige myndigheder eller andre handelspartnere, der bemyndiger anvendelse af elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="dcafc-106">Companies that want to benefit from electronic invoicing must submit sales order invoices, free text invoices, project invoices, sales order credit notes, and project invoice credit notes as .xml files to the government or other trading parties that mandate use of electronic invoicing.</span></span> <span data-ttu-id="dcafc-107">Disse .XML-filer skal opfylde bestemte standarder.</span><span class="sxs-lookup"><span data-stu-id="dcafc-107">These .xml files must comply with certain standards.</span></span> <span data-ttu-id="dcafc-108">Landespecifikke krav og deres gennemførelse kan variere på tværs af EU-medlemsstaterne, men ofte bruger de Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) i forskellige versioner med tilpasninger samt [PEPPOL](https://www.peppol.eu)-specifikationer og adgangspunkter til validering og transport.</span><span class="sxs-lookup"><span data-stu-id="dcafc-108">The country-specific requirements and their implementation may differ across EU member states but commonly they are using Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in different versions with customizations as well as [PEPPOL](https://www.peppol.eu) specifications and access points for validation and transportation.</span></span> <span data-ttu-id="dcafc-109">Den primære fordel ved UBL er, at forretningsdokumenter kan standardiseres til forskellige formål.</span><span class="sxs-lookup"><span data-stu-id="dcafc-109">The primary advantage of UBL is that business documents can be standardized for different purposes.</span></span> <span data-ttu-id="dcafc-110">Da UBL er en fleksibel, international standard, der understøtter mange forretningsmæssige krav, kan disse forretningsdokumenter udveksles på tværs af nationale grænser.</span><span class="sxs-lookup"><span data-stu-id="dcafc-110">Because UBL is a flexible, international standard that supports many business requirements, these business documents can be exchanged across national borders.</span></span>

## <a name="electronic-invoice-formats-currently-available-in-dynamics-365-finance"></a><span data-ttu-id="dcafc-111">Elektroniske fakturaformater, der i øjeblikket er tilgængelige i Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="dcafc-111">Electronic invoice formats currently available in Dynamics 365 Finance</span></span>

<span data-ttu-id="dcafc-112">Der findes følgende landespecifikke formater for elektroniske fakturaer:</span><span class="sxs-lookup"><span data-stu-id="dcafc-112">The following country-specific formats of electronic invoices are available:</span></span>

-   <span data-ttu-id="dcafc-113">OIOUBL-v.2.02 for Danmark</span><span class="sxs-lookup"><span data-stu-id="dcafc-113">OIOUBL v.2.02 for Denmark</span></span>
-   <span data-ttu-id="dcafc-114">EHF v.3.0 for Norge</span><span class="sxs-lookup"><span data-stu-id="dcafc-114">EHF v.3.0 for Norway</span></span>
-   <span data-ttu-id="dcafc-115">PEPPOL BIS v.2 for Østrig, Frankrig og Belgien</span><span class="sxs-lookup"><span data-stu-id="dcafc-115">PEPPOL BIS v.2 for Austria, France, and Belgium</span></span>
-   <span data-ttu-id="dcafc-116">UBL-OHNL 1.9 for Nederlandene</span><span class="sxs-lookup"><span data-stu-id="dcafc-116">UBL-OHNL 1.9 for the Netherlands</span></span>
-   <span data-ttu-id="dcafc-117">FacturaE v.3.2.1 for Spanien</span><span class="sxs-lookup"><span data-stu-id="dcafc-117">FacturaE v.3.2.1 for Spain</span></span>
-   <span data-ttu-id="dcafc-118">FatturaPA v.1.2 for Italien</span><span class="sxs-lookup"><span data-stu-id="dcafc-118">FatturaPA v.1.2 for Italy</span></span>
-   <span data-ttu-id="dcafc-119">xRechnung v.1.2 for Tyskland</span><span class="sxs-lookup"><span data-stu-id="dcafc-119">xRechnung v.1.2 for Germany</span></span>
-   <span data-ttu-id="dcafc-120">Åbn PEPPOL BIS Billing v.3.0 for Den Europæiske Union</span><span class="sxs-lookup"><span data-stu-id="dcafc-120">Open PEPPOL BIS Billing v.3.0 for European Union</span></span>
-   <span data-ttu-id="dcafc-121">Estisk specifikt format version 1.2</span><span class="sxs-lookup"><span data-stu-id="dcafc-121">Estonian specific format version 1.2</span></span>
-   <span data-ttu-id="dcafc-122">Finvoice 3.0 for Finland</span><span class="sxs-lookup"><span data-stu-id="dcafc-122">Finvoice 3.0 for Finland</span></span>

<span data-ttu-id="dcafc-123">Elektronisk fakturering er baseret på [Elektronisk indberetning (ER)](../../dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="dcafc-123">Electronic invoicing is based on [Electronic reporting (ER)](../../dev-itpro/analytics/general-electronic-reporting.md).</span></span> <span data-ttu-id="dcafc-124">Der er oprettet en **Fakturamodel**-datamodel, fakturamodeltilknytning og flere forskellige lande-/områdespecifikke formatkonfigurationer for følgende lande/områder:</span><span class="sxs-lookup"><span data-stu-id="dcafc-124">An **Invoice model** data model, invoice model mapping, and several country/region-specific ER format configurations have been created for the following countries/regions:</span></span> 

- <span data-ttu-id="dcafc-125">Østrig (AT)</span><span class="sxs-lookup"><span data-stu-id="dcafc-125">Austria (AT)</span></span>
- <span data-ttu-id="dcafc-126">Danmark (DK)</span><span class="sxs-lookup"><span data-stu-id="dcafc-126">Denmark (DK)</span></span>
- <span data-ttu-id="dcafc-127">Italien (IT)</span><span class="sxs-lookup"><span data-stu-id="dcafc-127">Italy (IT)</span></span>
- <span data-ttu-id="dcafc-128">Norge (NO)</span><span class="sxs-lookup"><span data-stu-id="dcafc-128">Norway (NO)</span></span>
- <span data-ttu-id="dcafc-129">Spanien (ES)</span><span class="sxs-lookup"><span data-stu-id="dcafc-129">Spain (ES)</span></span>
- <span data-ttu-id="dcafc-130">Frankrig (FR)</span><span class="sxs-lookup"><span data-stu-id="dcafc-130">France (FR)</span></span>
- <span data-ttu-id="dcafc-131">Belgien (BE)</span><span class="sxs-lookup"><span data-stu-id="dcafc-131">Belgium (BE)</span></span>
- <span data-ttu-id="dcafc-132">Nederlandene (NL)</span><span class="sxs-lookup"><span data-stu-id="dcafc-132">The Netherlands (NL)</span></span>
- <span data-ttu-id="dcafc-133">Tyskland (DE)</span><span class="sxs-lookup"><span data-stu-id="dcafc-133">Germany (DE)</span></span>
- <span data-ttu-id="dcafc-134">Estland (EE)</span><span class="sxs-lookup"><span data-stu-id="dcafc-134">Estonia (EE)</span></span>
- <span data-ttu-id="dcafc-135">Finland (FI)</span><span class="sxs-lookup"><span data-stu-id="dcafc-135">Finland (FI)</span></span>
- <span data-ttu-id="dcafc-136">Den Europæiske Union (EU)</span><span class="sxs-lookup"><span data-stu-id="dcafc-136">The European Union (EU)</span></span>

<span data-ttu-id="dcafc-137">**Fakturamodel**-datamodel, fakturamodel og lande-/områdespecifikke ER-formatkonfigurationer omfatter:</span><span class="sxs-lookup"><span data-stu-id="dcafc-137">The **Invoice model** data model, invoice model mapping, and country/region-specific ER format configurations include:</span></span>

-   <span data-ttu-id="dcafc-138">OIOUBL salgsfaktura - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="dcafc-138">OIOUBL Sales invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="dcafc-139">OIOUBL salgskreditnota - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="dcafc-139">OIOUBL Sales credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="dcafc-140">OIOUBL projektfaktura - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="dcafc-140">OIOUBL Project invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="dcafc-141">OIOUBL projektkreditnota - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="dcafc-141">OIOUBL Project credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="dcafc-142">UBL-salgsfaktura FR</span><span class="sxs-lookup"><span data-stu-id="dcafc-142">UBL Sales Invoice FR</span></span>
-   <span data-ttu-id="dcafc-143">UBL-salgskreditnota FR</span><span class="sxs-lookup"><span data-stu-id="dcafc-143">UBL Sales Credit Note FR</span></span>
-   <span data-ttu-id="dcafc-144">UBL-projektfaktura FR</span><span class="sxs-lookup"><span data-stu-id="dcafc-144">UBL Project Invoice FR</span></span>
-   <span data-ttu-id="dcafc-145">UBL-projektkreditnota FR</span><span class="sxs-lookup"><span data-stu-id="dcafc-145">UBL Project Credit Note FR</span></span>
-   <span data-ttu-id="dcafc-146">UBL-salgsfaktura BE</span><span class="sxs-lookup"><span data-stu-id="dcafc-146">UBL Sales Invoice BE</span></span>
-   <span data-ttu-id="dcafc-147">UBL-salgskreditnota BE</span><span class="sxs-lookup"><span data-stu-id="dcafc-147">UBL Sales Credit Note BE</span></span>
-   <span data-ttu-id="dcafc-148">UBL-projektfaktura BE</span><span class="sxs-lookup"><span data-stu-id="dcafc-148">UBL Project Invoice BE</span></span>
-   <span data-ttu-id="dcafc-149">UBL-projektkreditnota BE</span><span class="sxs-lookup"><span data-stu-id="dcafc-149">UBL Project Credit Note BE</span></span>
-   <span data-ttu-id="dcafc-150">UBL-salgsfaktura NL</span><span class="sxs-lookup"><span data-stu-id="dcafc-150">UBL Sales Invoice NL</span></span>
-   <span data-ttu-id="dcafc-151">UBL-salgskreditnota NL</span><span class="sxs-lookup"><span data-stu-id="dcafc-151">UBL Sales Credit Note NL</span></span>
-   <span data-ttu-id="dcafc-152">UBL-projektfaktura NL</span><span class="sxs-lookup"><span data-stu-id="dcafc-152">UBL Project Invoice NL</span></span>
-   <span data-ttu-id="dcafc-153">UBL-projektkreditnota NL</span><span class="sxs-lookup"><span data-stu-id="dcafc-153">UBL Project Credit Note NL</span></span> 
-   <span data-ttu-id="dcafc-154">Salgsfaktura (ES)</span><span class="sxs-lookup"><span data-stu-id="dcafc-154">Sales invoice (ES)</span></span>
-   <span data-ttu-id="dcafc-155">Salgsfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="dcafc-155">Sales invoice (IT)</span></span>
-   <span data-ttu-id="dcafc-156">Projektfaktura (ES)</span><span class="sxs-lookup"><span data-stu-id="dcafc-156">Project invoice (ES)</span></span>
-   <span data-ttu-id="dcafc-157">Projektfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="dcafc-157">Project invoice (IT)</span></span>
-   <span data-ttu-id="dcafc-158">Salgsfaktura DE</span><span class="sxs-lookup"><span data-stu-id="dcafc-158">Sales Invoice DE</span></span>
-   <span data-ttu-id="dcafc-159">Projektfaktura DE</span><span class="sxs-lookup"><span data-stu-id="dcafc-159">Project Invoice DE</span></span>
-   <span data-ttu-id="dcafc-160">Peppol Salgsfaktura - for EU</span><span class="sxs-lookup"><span data-stu-id="dcafc-160">Peppol Sales Invoice - for EU</span></span>
-   <span data-ttu-id="dcafc-161">Peppol Salgskreditnota - for EU</span><span class="sxs-lookup"><span data-stu-id="dcafc-161">Peppol Sales Credit Note - for EU</span></span>
-   <span data-ttu-id="dcafc-162">Peppol Projektfaktura - for EU</span><span class="sxs-lookup"><span data-stu-id="dcafc-162">Peppol Project Invoice - for EU</span></span>
-   <span data-ttu-id="dcafc-163">Peppol Projektkreditnota - for EU</span><span class="sxs-lookup"><span data-stu-id="dcafc-163">Peppol Project Credit Note - for EU</span></span>
-   <span data-ttu-id="dcafc-164">Salgsfaktura (EE)</span><span class="sxs-lookup"><span data-stu-id="dcafc-164">Sales invoice (EE)</span></span>
-   <span data-ttu-id="dcafc-165">Projektfaktura (EE)</span><span class="sxs-lookup"><span data-stu-id="dcafc-165">Project invoice (EE)</span></span>
-   <span data-ttu-id="dcafc-166">Salgsfaktura (FI)</span><span class="sxs-lookup"><span data-stu-id="dcafc-166">Sales invoice (FI)</span></span>
-   <span data-ttu-id="dcafc-167">Projektfaktura (FI)</span><span class="sxs-lookup"><span data-stu-id="dcafc-167">Project invoice (FI)</span></span>

<span data-ttu-id="dcafc-168">De elektroniske fakturaer og kreditnotaer, som du genererer, omfatter nødvendige oplysninger som et europæisk varenummer (EAN) og oplysninger om kontakt, dimensionskontonummer og adresse til kunden.</span><span class="sxs-lookup"><span data-stu-id="dcafc-168">The electronic invoices and credit notes that you generate include required information, such as a European Article Numbering (EAN) number, contact person, dimension account number, and address information for the customer.</span></span> <span data-ttu-id="dcafc-169">Der anvendes valideringsregler, når der genereres fakturaer, så du kan kontrollere, at de korrekte oplysninger er angivet.</span><span class="sxs-lookup"><span data-stu-id="dcafc-169">Validation rules are applied when invoices are generated so you can verify that the correct information has been entered.</span></span> <span data-ttu-id="dcafc-170">Sættet af nødvendige oplysninger kan variere fra land til land.</span><span class="sxs-lookup"><span data-stu-id="dcafc-170">The set of required information may differ from country to country.</span></span> <span data-ttu-id="dcafc-171">Da både kravene og de understøttede lande og formater kan blive ændret, bør du altid gå til det delte aktivbibliotek i Microsoft Dynamics Lifecycle Services (LCS) og få vist den seneste liste over tilgængelige filer, som har aktivtypen **GER-konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="dcafc-171">Because the requirements, as well as supported countries and formats, is subject to change, you should always go to the Shared asset library on Microsoft Dynamics Lifecycle Services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span>

## <a name="electronic-invoice-configuration"></a><span data-ttu-id="dcafc-172">Konfiguration af elektronisk faktura</span><span class="sxs-lookup"><span data-stu-id="dcafc-172">Electronic invoice configuration</span></span>
<span data-ttu-id="dcafc-173">Opsætningen og de særlige oplysninger om elektroniske fakturaer afhænger af det land/område, som den er implementeret for.</span><span class="sxs-lookup"><span data-stu-id="dcafc-173">The setup and specifics of electronic invoices depend on the country/region that it's implemented for.</span></span> <span data-ttu-id="dcafc-174">Du kan finde flere oplysninger om, hvordan du konfigurerer og bruger elektroniske debitorfakturaer, i de relaterede lande-/områdespecifikke emner:</span><span class="sxs-lookup"><span data-stu-id="dcafc-174">For more information about how to set up and use customer electronic invoices, see the related country-specific topics:</span></span>

- [<span data-ttu-id="dcafc-175">Italien</span><span class="sxs-lookup"><span data-stu-id="dcafc-175">Italy</span></span>](emea-ita-e-invoices.md)
- [<span data-ttu-id="dcafc-176">Norge</span><span class="sxs-lookup"><span data-stu-id="dcafc-176">Norway</span></span>](emea-nor-e-invoices.md)
- [<span data-ttu-id="dcafc-177">Tyskland</span><span class="sxs-lookup"><span data-stu-id="dcafc-177">Germany</span></span>](emea-deu-e-invoices.md)
- [<span data-ttu-id="dcafc-178">Finland</span><span class="sxs-lookup"><span data-stu-id="dcafc-178">Finland</span></span>](https://support.microsoft.com/help/4559937)
- [<span data-ttu-id="dcafc-179">Estland</span><span class="sxs-lookup"><span data-stu-id="dcafc-179">Estonia</span></span>](https://support.microsoft.com/help/4552679)
- [<span data-ttu-id="dcafc-180">PEPPOL</span><span class="sxs-lookup"><span data-stu-id="dcafc-180">PEPPOL</span></span>](https://support.microsoft.com/help/4490320)

## <a name="additional-resources"></a><span data-ttu-id="dcafc-181">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="dcafc-181">Additional resources</span></span>
<span data-ttu-id="dcafc-182">Du kan få flere oplysninger om opsætning af elektroniske fakturaer ved at afspille følgende [opgaveguider](../../fin-and-ops/get-started/help-overview.md#task-guides) i ruden Hjælp:</span><span class="sxs-lookup"><span data-stu-id="dcafc-182">For more details about how to set up electronic invoices, you can play the following [Task guides](../../fin-and-ops/get-started/help-overview.md#task-guides) in the Help pane:</span></span>

 - <span data-ttu-id="dcafc-183">Konfigurere elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="dcafc-183">Set up OIOUBL electronic invoicing</span></span>
 - <span data-ttu-id="dcafc-184">Importere OIOUBL elektroniske faktureringskonfigurationer</span><span class="sxs-lookup"><span data-stu-id="dcafc-184">Import OIOUBL electronic invoicing configurations</span></span>
 - <span data-ttu-id="dcafc-185">Konfigurere debitorkonti til elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="dcafc-185">Set up customer accounts for OIOUBL electronic invoicing</span></span>

> [!NOTE] 
> <span data-ttu-id="dcafc-186">Selvom disse opgaveguider er oprettet specifikt til det danske e-fakturaformat *OIOUBL*, gælder de også for andre understøttede lande/områder, med mindre afvigelser.</span><span class="sxs-lookup"><span data-stu-id="dcafc-186">Although these Task guides were created for Danish-specific e-invoice format *OIOUBL*, they are applicable for other supported countries/regions with minor deviations.</span></span>
