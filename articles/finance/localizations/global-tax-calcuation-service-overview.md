---
title: Momsberegningstjeneste (forhåndsversion)
description: Dette emne forklarer det overordnede område og funktionerne for tjenesten til momsberegning.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818218"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="60acd-103">Momsberegningstjeneste (forhåndsversion)</span><span class="sxs-lookup"><span data-stu-id="60acd-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="60acd-104">Tjenesten til momsberegning er en særdeles skalerbar flerdimensional tjeneste, som gør det muligt for det globale momsprogram at automatisere og forenkle fastlæggelse og beregning af moms.</span><span class="sxs-lookup"><span data-stu-id="60acd-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="60acd-105">Momsprogrammet kan konfigureres fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="60acd-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="60acd-106">De elementer, der kan konfigureres, omfatter, men er ikke begrænset til, den momspligtige datamodel, momskode, matrix for anvendelse af moms og momsberegningsformlen.</span><span class="sxs-lookup"><span data-stu-id="60acd-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="60acd-107">Momsprogrammet kører på Microsoft Azure-kerneserviceplatformen og tilbyder moderne teknologi og eksponentiel skalerbarhed.</span><span class="sxs-lookup"><span data-stu-id="60acd-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="60acd-108">Tjenesten til beregning af moms kan integreres med Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="60acd-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="60acd-109">Senere vil det også blive integreret i , Dynamics 365 Project Operations, Dynamics 365 Commerce og andre programmer fra første part og tredjepart.</span><span class="sxs-lookup"><span data-stu-id="60acd-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="60acd-110">Tjenesten til momsberegning er et Microsoft-baseret momsprogram, der tilbyder eksponentiel skalerbarhed.</span><span class="sxs-lookup"><span data-stu-id="60acd-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="60acd-111">Du kan få hjælp til at udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="60acd-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="60acd-112">Konfigurer momsberegningstjenesten via Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="60acd-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="60acd-113">RCS er en udvidet version af ER-designeren (Elektronisk rapportering) og er tilgængelig som en enkeltstående tjeneste.</span><span class="sxs-lookup"><span data-stu-id="60acd-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="60acd-114">Konfigurer momsmatrixen til automatisk at bestemme momskoder og -satser.</span><span class="sxs-lookup"><span data-stu-id="60acd-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="60acd-115">Konfigurer momsmatrixen til automatisk at bestemme momsregistreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="60acd-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="60acd-116">Konfigurer momsberegningsdesigneren for at definere formler og betingelser.</span><span class="sxs-lookup"><span data-stu-id="60acd-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="60acd-117">Del momsfastsættelses- og -beregningsløsningen på tværs af juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="60acd-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="60acd-118">Hvis du vil bruge tjenesten til momsberegning, skal du installere tilføjelsesprogrammet Momsberegningstjeneste fra dit projekt i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="60acd-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="60acd-119">Fuldfør derefter opsætningen i RCS, og aktivér tjenesten til momsberegning i Finance og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="60acd-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="60acd-120">Du kan finde flere oplysninger i [Start her med momstjeneste](https://go.microsoft.com/fwlink/?linkid=2138482).</span><span class="sxs-lookup"><span data-stu-id="60acd-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="60acd-121">Tilgængelighed</span><span class="sxs-lookup"><span data-stu-id="60acd-121">Availability</span></span>

<span data-ttu-id="60acd-122">Tjenesten til momsberegning er kun tilgængelig i sandkassemiljøer og for udvalgte kunder via et offentligt forhåndsversionsprogram.</span><span class="sxs-lookup"><span data-stu-id="60acd-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="60acd-123">Senere vil den blive generelt tilgængelig for alle kunder og i produktionsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="60acd-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="60acd-124">Der vil fortsat blive leveret nye funktioner i tjenesten til momsberegning.</span><span class="sxs-lookup"><span data-stu-id="60acd-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="60acd-125">Du skal derfor sørge for ofte at læse den sidste nye dokumentation for at få mere at vide om dækning og området af understøttede funktioner.</span><span class="sxs-lookup"><span data-stu-id="60acd-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="60acd-126">Tjenesten til momsberegning implementeres i følgende Azure-geografiske områder.</span><span class="sxs-lookup"><span data-stu-id="60acd-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="60acd-127">Den vil også blive implementeret i flere Azure-geografiske områder baseret på kundernes behov:</span><span class="sxs-lookup"><span data-stu-id="60acd-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="60acd-128">United States</span><span class="sxs-lookup"><span data-stu-id="60acd-128">United States</span></span>
- <span data-ttu-id="60acd-129">Europa</span><span class="sxs-lookup"><span data-stu-id="60acd-129">Europe</span></span>
- <span data-ttu-id="60acd-130">Frankrig</span><span class="sxs-lookup"><span data-stu-id="60acd-130">France</span></span>
- <span data-ttu-id="60acd-131">Storbritannien</span><span class="sxs-lookup"><span data-stu-id="60acd-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="60acd-132">Tjenesten til momsberegning understøtter ikke implementering i det lokale miljø af Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="60acd-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="60acd-133">Den understøtter heller ikke tidligere versioner, f.eks. Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="60acd-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="60acd-134">Fremhævning af funktioner</span><span class="sxs-lookup"><span data-stu-id="60acd-134">Feature highlights</span></span>

- <span data-ttu-id="60acd-135">En konfigurerbar momsmatrix til automatisk at bestemme og beregne moms</span><span class="sxs-lookup"><span data-stu-id="60acd-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="60acd-136">Understøttelse af flere momsregistreringsnumre</span><span class="sxs-lookup"><span data-stu-id="60acd-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="60acd-137">Understøttelse af flytteordre til fastlæggelse og beregning af moms</span><span class="sxs-lookup"><span data-stu-id="60acd-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="60acd-138">Understøttelse af flytteordre til fastlæggelse af flere momsregistreringsnumre</span><span class="sxs-lookup"><span data-stu-id="60acd-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="60acd-139">Understøttede transaktioner</span><span class="sxs-lookup"><span data-stu-id="60acd-139">Supported transactions</span></span>

<span data-ttu-id="60acd-140">Tjenesten til momsberegning kan aktiveres via juridisk enhed og transaktion.</span><span class="sxs-lookup"><span data-stu-id="60acd-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="60acd-141">Følgende transaktioner understøttes:</span><span class="sxs-lookup"><span data-stu-id="60acd-141">The following transactions are supported:</span></span>

- <span data-ttu-id="60acd-142">Salgsproces</span><span class="sxs-lookup"><span data-stu-id="60acd-142">Sales process</span></span>

    - <span data-ttu-id="60acd-143">Salgstilbud</span><span class="sxs-lookup"><span data-stu-id="60acd-143">Sales quotation</span></span>
    - <span data-ttu-id="60acd-144">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="60acd-144">Sales order</span></span>
    - <span data-ttu-id="60acd-145">Bekræftelse</span><span class="sxs-lookup"><span data-stu-id="60acd-145">Confirmation</span></span>
    - <span data-ttu-id="60acd-146">Plukliste</span><span class="sxs-lookup"><span data-stu-id="60acd-146">Picking list</span></span>
    - <span data-ttu-id="60acd-147">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="60acd-147">Packing slip</span></span>
    - <span data-ttu-id="60acd-148">Salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="60acd-148">Sales invoice</span></span>
    - <span data-ttu-id="60acd-149">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="60acd-149">Credit note</span></span>
    - <span data-ttu-id="60acd-150">Returordre</span><span class="sxs-lookup"><span data-stu-id="60acd-150">Return order</span></span>
    - <span data-ttu-id="60acd-151">Overskrift til diverse gebyrer</span><span class="sxs-lookup"><span data-stu-id="60acd-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="60acd-152">Linje til diverse gebyrer</span><span class="sxs-lookup"><span data-stu-id="60acd-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="60acd-153">Indkøbsproces</span><span class="sxs-lookup"><span data-stu-id="60acd-153">Purchase process</span></span>

    - <span data-ttu-id="60acd-154">Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="60acd-154">Purchase order</span></span>
    - <span data-ttu-id="60acd-155">Bekræftelse</span><span class="sxs-lookup"><span data-stu-id="60acd-155">Confirmation</span></span>
    - <span data-ttu-id="60acd-156">Tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="60acd-156">Receipts list</span></span>
    - <span data-ttu-id="60acd-157">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="60acd-157">Product receipt</span></span>
    - <span data-ttu-id="60acd-158">Indkøbsfaktura</span><span class="sxs-lookup"><span data-stu-id="60acd-158">Purchase invoice</span></span>
    - <span data-ttu-id="60acd-159">Overskrift til diverse gebyrer</span><span class="sxs-lookup"><span data-stu-id="60acd-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="60acd-160">Linje til diverse gebyrer</span><span class="sxs-lookup"><span data-stu-id="60acd-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="60acd-161">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="60acd-161">Credit note</span></span>
    - <span data-ttu-id="60acd-162">Returordre</span><span class="sxs-lookup"><span data-stu-id="60acd-162">Return order</span></span>
    - <span data-ttu-id="60acd-163">Indkøbsrekvisition</span><span class="sxs-lookup"><span data-stu-id="60acd-163">Purchase requisition</span></span>
    - <span data-ttu-id="60acd-164">Diverse gebyrer til indkøbsrekvisitionslinje</span><span class="sxs-lookup"><span data-stu-id="60acd-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="60acd-165">Tilbudsanmodning</span><span class="sxs-lookup"><span data-stu-id="60acd-165">Request for quotation</span></span>
    - <span data-ttu-id="60acd-166">Diverse gebyrer i overskrift til tilbudsanmodning</span><span class="sxs-lookup"><span data-stu-id="60acd-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="60acd-167">Diverse gebyrer i linje til tilbudsanmodning</span><span class="sxs-lookup"><span data-stu-id="60acd-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="60acd-168">Lagerproces</span><span class="sxs-lookup"><span data-stu-id="60acd-168">Inventory process</span></span>

    - <span data-ttu-id="60acd-169">Flytteordre – send</span><span class="sxs-lookup"><span data-stu-id="60acd-169">Transfer order – ship</span></span>
    - <span data-ttu-id="60acd-170">Flytteordre – modtag</span><span class="sxs-lookup"><span data-stu-id="60acd-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="60acd-171">Tilknyttede ressourcer</span><span class="sxs-lookup"><span data-stu-id="60acd-171">Related resources</span></span>

[<span data-ttu-id="60acd-172">Start her med momstjeneste</span><span class="sxs-lookup"><span data-stu-id="60acd-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="60acd-173">Flere momsregistreringsnumre</span><span class="sxs-lookup"><span data-stu-id="60acd-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="60acd-174">Understøttelse af momsfunktion til flytteordre</span><span class="sxs-lookup"><span data-stu-id="60acd-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="60acd-175">Sådan bygger du udvidelse i momstjeneste</span><span class="sxs-lookup"><span data-stu-id="60acd-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
