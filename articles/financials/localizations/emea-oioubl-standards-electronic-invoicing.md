---
title: "Understøttede standarder til elektronisk fakturering i Europa"
description: "I dette emne beskrives det dækningsniveau, der findes for elektronisk fakturering i Microsoft Dynamics 365 for Finance and Operations i det europæiske område."
author: mrolecki
manager: AnnBe
ms.date: 07/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10274
ms.search.region: Austria, Denmark, Italy, Norway, Spain, France, Belgium, Netherlands
ms.search.industry: 
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 821e6df1a39b12b502f19e23e361fd407a83ed6c
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="supported-standards-for-electronic-invoicing-in-europe"></a><span data-ttu-id="8ae0b-103">Understøttede standarder til elektronisk fakturering i Europa</span><span class="sxs-lookup"><span data-stu-id="8ae0b-103">Supported standards for electronic invoicing in Europe</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="8ae0b-104">I dette emne beskrives det dækningsniveau, der findes for elektronisk fakturering for Europa.</span><span class="sxs-lookup"><span data-stu-id="8ae0b-104">This topic explains the level of coverage that exists for electronic invoicing for Europe.</span></span> 

<span data-ttu-id="8ae0b-105">Implementering og indførelse overalt i EU af elektronisk fakturering er reguleret [Rådets direktiv 2010/45/EU](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), hvilket har indflydelse på alle EU-medlemsstater.</span><span class="sxs-lookup"><span data-stu-id="8ae0b-105">Implementation and adoption of European Union-wide electronic invoicing is regulated [Council Directive 2010/45/EU](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), which affects all EU member states.</span></span> <span data-ttu-id="8ae0b-106">Virksomheder, der gerne vil have fordel af elektronisk fakturering, skal sende salgsordrefakturaer, fritekstfakturaer, projektfakturaer, kreditnotaer for salgsordre og kreditnotaer for projektfakturaer som .XML-filer til offentlige myndigheder eller andre handelspartnere, der bemyndiger anvendelse af elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="8ae0b-106">Companies that want to benefit from electronic invoicing must submit sales order invoices, free text invoices, project invoices, sales order credit notes, and project invoice credit notes as .xml files to the government or other trading parties that mandate use of electronic invoicing.</span></span> <span data-ttu-id="8ae0b-107">Disse .XML-filer skal opfylde bestemte standarder.</span><span class="sxs-lookup"><span data-stu-id="8ae0b-107">These .xml files must comply with certain standards.</span></span> <span data-ttu-id="8ae0b-108">Landespecifikke krav og deres gennemførelse kan variere på tværs af EU-medlemsstaterne, men ofte bruger de Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) i forskellige versioner med tilpasninger samt [PEPPOL](http://www.peppol.eu)-specifikationer og adgangspunkter til validering og transport.</span><span class="sxs-lookup"><span data-stu-id="8ae0b-108">The country-specific requirements and their implementation may differ across EU member states but commonly they are using Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in different versions with customizations as well as [PEPPOL](http://www.peppol.eu) specifications and access points for validation and transportation.</span></span> <span data-ttu-id="8ae0b-109">Den primære fordel ved UBL er, at forretningsdokumenter kan standardiseres til forskellige formål.</span><span class="sxs-lookup"><span data-stu-id="8ae0b-109">The primary advantage of UBL is that business documents can be standardized for different purposes.</span></span> <span data-ttu-id="8ae0b-110">Da UBL er en fleksibel, international standard, der understøtter mange forretningsmæssige krav, kan disse forretningsdokumenter udveksles på tværs af nationale grænser.</span><span class="sxs-lookup"><span data-stu-id="8ae0b-110">Because UBL is a flexible, international standard that supports many business requirements, these business documents can be exchanged across national borders.</span></span>

## <a name="what-electronic-invoice-formats-are-currently-available-in-finance-and-operations"></a><span data-ttu-id="8ae0b-111">Hvilke formater for elektroniske fakturaer er i øjeblikket tilgængelige i Finance and Operations?</span><span class="sxs-lookup"><span data-stu-id="8ae0b-111">What electronic invoice formats are currently available in Finance and Operations?</span></span>

<span data-ttu-id="8ae0b-112">Der findes følgende landespecifikke formater for elektroniske fakturaer:</span><span class="sxs-lookup"><span data-stu-id="8ae0b-112">The following country-specific formats of electronic invoices are available:</span></span>

-   <span data-ttu-id="8ae0b-113">OIOUBL-v.2.02 for Danmark</span><span class="sxs-lookup"><span data-stu-id="8ae0b-113">OIOUBL v.2.02 for Denmark</span></span>
-   <span data-ttu-id="8ae0b-114">EHF v.2.0.8 for Norge</span><span class="sxs-lookup"><span data-stu-id="8ae0b-114">EHF v.2.0.8 for Norway</span></span>
-   <span data-ttu-id="8ae0b-115">PEPPOL BIS v.2 for Østrig, Frankrig og Belgien</span><span class="sxs-lookup"><span data-stu-id="8ae0b-115">PEPPOL BIS v.2 for Austria, France, and Belgium</span></span>
-   <span data-ttu-id="8ae0b-116">UBL-OHNL 1.9 for Nederlandene</span><span class="sxs-lookup"><span data-stu-id="8ae0b-116">UBL-OHNL 1.9 for the Netherlands</span></span>
-   <span data-ttu-id="8ae0b-117">FacturaE v.3.2.1 for Spanien</span><span class="sxs-lookup"><span data-stu-id="8ae0b-117">FacturaE v.3.2.1 for Spain</span></span>
-   <span data-ttu-id="8ae0b-118">FatturaPA v.1.2 for Italien</span><span class="sxs-lookup"><span data-stu-id="8ae0b-118">FatturaPA v.1.2 for Italy</span></span>

<span data-ttu-id="8ae0b-119">Elektronisk fakturering er baseret på [elektronisk indberetning](../../dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="8ae0b-119">Electronic invoicing is based on [electronic reporting](../../dev-itpro/analytics/general-electronic-reporting.md).</span></span> <span data-ttu-id="8ae0b-120">Der er en **Debitorfakturamodel**-datamodel, og der er oprettet en række landespecifikke konfigurationer for elektroniske indberetningsformater for Østrig (AT), Danmark (DK), Italien (IT), Norge (NO), Spanien (ES), Frankrig (FR), Belgien (BE) Nederlandene (NL).</span><span class="sxs-lookup"><span data-stu-id="8ae0b-120">There is a **Customer invoice model** data model and a number of country-specific electronic reporting format configurations created for Austria (AT), Denmark (DK), Italy (IT), Norway (NO), Spain (ES), France (FR), Belgium (BE), and the Netherlands (NL).</span></span>

-   <span data-ttu-id="8ae0b-121">OIOUBL salgsfaktura - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="8ae0b-121">OIOUBL Sales invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="8ae0b-122">OIOUBL salgskreditnota - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="8ae0b-122">OIOUBL Sales credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="8ae0b-123">OIOUBL projektfaktura - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="8ae0b-123">OIOUBL Project invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="8ae0b-124">OIOUBL projektkreditnota - for AT, DK og NO</span><span class="sxs-lookup"><span data-stu-id="8ae0b-124">OIOUBL Project credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="8ae0b-125">UBL-salgsfaktura FR</span><span class="sxs-lookup"><span data-stu-id="8ae0b-125">UBL Sales Invoice FR</span></span>
-   <span data-ttu-id="8ae0b-126">UBL-salgskreditnota FR</span><span class="sxs-lookup"><span data-stu-id="8ae0b-126">UBL Sales Credit Note FR</span></span>
-   <span data-ttu-id="8ae0b-127">UBL-projektfaktura FR</span><span class="sxs-lookup"><span data-stu-id="8ae0b-127">UBL Project Invoice FR</span></span>
-   <span data-ttu-id="8ae0b-128">UBL-projektkreditnota FR</span><span class="sxs-lookup"><span data-stu-id="8ae0b-128">UBL Project Credit Note FR</span></span>
-   <span data-ttu-id="8ae0b-129">UBL-salgsfaktura BE</span><span class="sxs-lookup"><span data-stu-id="8ae0b-129">UBL Sales Invoice BE</span></span>
-   <span data-ttu-id="8ae0b-130">UBL-salgskreditnota BE</span><span class="sxs-lookup"><span data-stu-id="8ae0b-130">UBL Sales Credit Note BE</span></span>
-   <span data-ttu-id="8ae0b-131">UBL-projektfaktura BE</span><span class="sxs-lookup"><span data-stu-id="8ae0b-131">UBL Project Invoice BE</span></span>
-   <span data-ttu-id="8ae0b-132">UBL-projektkreditnota BE</span><span class="sxs-lookup"><span data-stu-id="8ae0b-132">UBL Project Credit Note BE</span></span>
-   <span data-ttu-id="8ae0b-133">UBL-salgsfaktura NL</span><span class="sxs-lookup"><span data-stu-id="8ae0b-133">UBL Sales Invoice NL</span></span>
-   <span data-ttu-id="8ae0b-134">UBL-salgskreditnota NL</span><span class="sxs-lookup"><span data-stu-id="8ae0b-134">UBL Sales Credit Note NL</span></span>
-   <span data-ttu-id="8ae0b-135">UBL-projektfaktura NL</span><span class="sxs-lookup"><span data-stu-id="8ae0b-135">UBL Project Invoice NL</span></span>
-   <span data-ttu-id="8ae0b-136">UBL-projektkreditnota NL</span><span class="sxs-lookup"><span data-stu-id="8ae0b-136">UBL Project Credit Note NL</span></span> 
-   <span data-ttu-id="8ae0b-137">Salgsfaktura (ES)</span><span class="sxs-lookup"><span data-stu-id="8ae0b-137">Sales invoice (ES)</span></span>
-   <span data-ttu-id="8ae0b-138">Salgsfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="8ae0b-138">Sales invoice (IT)</span></span>
-   <span data-ttu-id="8ae0b-139">Projektfaktura (ES)</span><span class="sxs-lookup"><span data-stu-id="8ae0b-139">Project invoice (ES)</span></span>
-   <span data-ttu-id="8ae0b-140">Projektfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="8ae0b-140">Project invoice (IT)</span></span>

<span data-ttu-id="8ae0b-141">De elektroniske fakturaer og kreditnotaer, som du genererer, omfatter nødvendige oplysninger som et europæisk varenummer (EAN) og oplysninger om kontakt, dimensionskontonummer og adresse til kunden.</span><span class="sxs-lookup"><span data-stu-id="8ae0b-141">The electronic invoices and credit notes that you generate include required information, such as a European Article Numbering (EAN) number, contact person, dimension account number, and address information for the customer.</span></span> <span data-ttu-id="8ae0b-142">Der anvendes valideringsregler, når der genereres fakturaer, så du kan kontrollere, at de korrekte oplysninger er angivet.</span><span class="sxs-lookup"><span data-stu-id="8ae0b-142">Validation rules are applied when invoices are generated so you can verify that the correct information has been entered.</span></span> <span data-ttu-id="8ae0b-143">Sættet af nødvendige oplysninger kan variere fra land til land.</span><span class="sxs-lookup"><span data-stu-id="8ae0b-143">The set of required information may differ from country to country.</span></span> <span data-ttu-id="8ae0b-144">Da både kravene og de understøttede lande og formater kan blive ændret, bør du altid gå til det delte aktivbibliotek i Microsoft Dynamics Lifecycle services (LCS) og få vist den seneste liste over tilgængelige filer, som har aktivtypen **GER-konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8ae0b-144">Because the requirements, as well as supported countries and formats, is subject to change, you should always go to the Shared asset library on Microsoft Dynamics Lifecycle services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span>

## <a name="additional-information"></a><span data-ttu-id="8ae0b-145">Yderligere oplysninger</span><span class="sxs-lookup"><span data-stu-id="8ae0b-145">Additional information</span></span>
<span data-ttu-id="8ae0b-146">Du kan få flere oplysninger om opsætning af elektroniske fakturaer ved at afspille følgende [opgaveguider](../../fin-and-ops/get-started/help-overview.md#task-guides) i ruden Hjælp:</span><span class="sxs-lookup"><span data-stu-id="8ae0b-146">For more details about how to set up electronic invoices, you can play the following [Task guides](../../fin-and-ops/get-started/help-overview.md#task-guides) in the Help pane:</span></span>

 - <span data-ttu-id="8ae0b-147">Konfigurere elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="8ae0b-147">Set up OIOUBL electronic invoicing</span></span>
 - <span data-ttu-id="8ae0b-148">Importere OIOUBL elektroniske faktureringskonfigurationer</span><span class="sxs-lookup"><span data-stu-id="8ae0b-148">Import OIOUBL electronic invoicing configurations</span></span>
 - <span data-ttu-id="8ae0b-149">Konfigurere debitorkonti til elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="8ae0b-149">Set up customer accounts for OIOUBL electronic invoicing</span></span>

> [!NOTE] 
> <span data-ttu-id="8ae0b-150">Selvom disse opgaveguider er oprettet specifikt til det danske e-fakturaformat *OIOUBL*, gælder de også for andre understøttede lande, med mindre afvigelser.</span><span class="sxs-lookup"><span data-stu-id="8ae0b-150">Although these Task guides were created for Danish-specific e-invoice format *OIOUBL*, they are applicable for other supported countries with minor deviations.</span></span>

