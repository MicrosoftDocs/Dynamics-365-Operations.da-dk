---
title: Momsberegning (prøveversion)
description: Dette emne forklarer det overordnede område og funktionerne for til momsberegning.
author: wangchen
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b26472e195d9bdbba340a118c106de1a4dc79b34
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021926"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="1ffb3-103">Momsberegning (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="1ffb3-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="1ffb3-104">Momsberegning er en særdeles skalerbar flerdimensional tjeneste, som gør det muligt for det globale momsprogram at automatisere og forenkle fastlæggelse og beregning af moms.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="1ffb3-105">Momsprogrammet kan konfigureres fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="1ffb3-106">De elementer, der kan konfigureres, omfatter, men er ikke begrænset til, den momspligtige datamodel, momskode, matrix for anvendelse af moms og momsberegningsformlen.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="1ffb3-107">Momsprogrammet kører på Microsoft Azure-kerneserviceplatformen og tilbyder moderne teknologi og eksponentiel skalerbarhed.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="1ffb3-108">Beregning af moms kan integreres med Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1ffb3-109">Senere vil det også blive integreret i , Dynamics 365 Project Operations, Dynamics 365 Commerce og andre programmer fra første part og tredjepart.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="1ffb3-110">Momsberegning er et mikroservicebaseret momsprogram, der tilbyder eksponentiel skalerbarhed.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="1ffb3-111">Du kan få hjælp til at udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="1ffb3-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="1ffb3-112">Konfigurer momsberegning via Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="1ffb3-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="1ffb3-113">RCS er en udvidet version af ER-designeren (Elektronisk rapportering) og er tilgængelig som en enkeltstående tjeneste.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="1ffb3-114">Konfigurer momsmatrixen til automatisk at bestemme momskoder og -satser.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="1ffb3-115">Konfigurer momsmatrixen til automatisk at bestemme momsregistreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="1ffb3-116">Konfigurer momsberegningsdesigneren for at definere formler og betingelser.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="1ffb3-117">Del momsfastsættelses- og -beregningsløsningen på tværs af juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="1ffb3-118">Hvis du vil bruge tjenesten til momsberegning, skal du installere tilføjelsesprogrammet Momsberegningstjeneste fra dit projekt i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1ffb3-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="1ffb3-119">Fuldfør derefter opsætningen i RCS, og aktivér tjenesten til momsberegning i Finance og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="1ffb3-120">Du kan finde flere oplysninger i [Start her med momstjeneste](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="1ffb3-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="1ffb3-121">Tilgængelighed</span><span class="sxs-lookup"><span data-stu-id="1ffb3-121">Availability</span></span>

<span data-ttu-id="1ffb3-122">Momsberegning er kun tilgængelig i sandkassemiljøer og for udvalgte kunder via et offentligt forhåndsversionsprogram.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="1ffb3-123">Senere vil den blive generelt tilgængelig for alle kunder og i produktionsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="1ffb3-124">Der leveres fortsat nye funktioner, så du skal derfor sørge for ofte at læse den sidste nye dokumentation for at få mere at vide om dækning og området af understøttede funktioner.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="1ffb3-125">Momsberegning implementeres i følgende Azure-geografiske områder.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="1ffb3-126">Den vil også blive implementeret i flere Azure-geografiske områder baseret på kundernes behov:</span><span class="sxs-lookup"><span data-stu-id="1ffb3-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="1ffb3-127">United States</span><span class="sxs-lookup"><span data-stu-id="1ffb3-127">United States</span></span>
- <span data-ttu-id="1ffb3-128">Europa</span><span class="sxs-lookup"><span data-stu-id="1ffb3-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="1ffb3-129">Momsberegning understøtter ikke implementering i det lokale miljø af Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="1ffb3-130">Den understøtter heller ikke tidligere versioner, f.eks. Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="1ffb3-131">Fremhævning af funktioner</span><span class="sxs-lookup"><span data-stu-id="1ffb3-131">Feature highlights</span></span>

- <span data-ttu-id="1ffb3-132">En konfigurerbar momsmatrix til automatisk at bestemme og beregne moms</span><span class="sxs-lookup"><span data-stu-id="1ffb3-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="1ffb3-133">Understøttelse af flere momsregistreringsnumre</span><span class="sxs-lookup"><span data-stu-id="1ffb3-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="1ffb3-134">Understøttelse af flytteordre til fastlæggelse og beregning af moms</span><span class="sxs-lookup"><span data-stu-id="1ffb3-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="1ffb3-135">Understøttelse af flytteordre til fastlæggelse af flere momsregistreringsnumre</span><span class="sxs-lookup"><span data-stu-id="1ffb3-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="1ffb3-136">Understøttede transaktioner</span><span class="sxs-lookup"><span data-stu-id="1ffb3-136">Supported transactions</span></span>

<span data-ttu-id="1ffb3-137">Momsberegning kan aktiveres via juridisk enhed og transaktion.</span><span class="sxs-lookup"><span data-stu-id="1ffb3-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="1ffb3-138">Følgende transaktioner understøttes:</span><span class="sxs-lookup"><span data-stu-id="1ffb3-138">The following transactions are supported:</span></span>

- <span data-ttu-id="1ffb3-139">Salgsproces</span><span class="sxs-lookup"><span data-stu-id="1ffb3-139">Sales process</span></span>

    - <span data-ttu-id="1ffb3-140">Salgstilbud</span><span class="sxs-lookup"><span data-stu-id="1ffb3-140">Sales quotation</span></span>
    - <span data-ttu-id="1ffb3-141">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="1ffb3-141">Sales order</span></span>
    - <span data-ttu-id="1ffb3-142">Bekræftelse</span><span class="sxs-lookup"><span data-stu-id="1ffb3-142">Confirmation</span></span>
    - <span data-ttu-id="1ffb3-143">Plukliste</span><span class="sxs-lookup"><span data-stu-id="1ffb3-143">Picking list</span></span>
    - <span data-ttu-id="1ffb3-144">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="1ffb3-144">Packing slip</span></span>
    - <span data-ttu-id="1ffb3-145">Salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="1ffb3-145">Sales invoice</span></span>
    - <span data-ttu-id="1ffb3-146">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="1ffb3-146">Credit note</span></span>
    - <span data-ttu-id="1ffb3-147">Returordre</span><span class="sxs-lookup"><span data-stu-id="1ffb3-147">Return order</span></span>
    - <span data-ttu-id="1ffb3-148">Overskrift til diverse gebyrer</span><span class="sxs-lookup"><span data-stu-id="1ffb3-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="1ffb3-149">Linje til diverse gebyrer</span><span class="sxs-lookup"><span data-stu-id="1ffb3-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="1ffb3-150">Indkøbsproces</span><span class="sxs-lookup"><span data-stu-id="1ffb3-150">Purchase process</span></span>

    - <span data-ttu-id="1ffb3-151">Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="1ffb3-151">Purchase order</span></span>
    - <span data-ttu-id="1ffb3-152">Bekræftelse</span><span class="sxs-lookup"><span data-stu-id="1ffb3-152">Confirmation</span></span>
    - <span data-ttu-id="1ffb3-153">Tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="1ffb3-153">Receipts list</span></span>
    - <span data-ttu-id="1ffb3-154">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="1ffb3-154">Product receipt</span></span>
    - <span data-ttu-id="1ffb3-155">Indkøbsfaktura</span><span class="sxs-lookup"><span data-stu-id="1ffb3-155">Purchase invoice</span></span>
    - <span data-ttu-id="1ffb3-156">Overskrift til diverse gebyrer</span><span class="sxs-lookup"><span data-stu-id="1ffb3-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="1ffb3-157">Linje til diverse gebyrer</span><span class="sxs-lookup"><span data-stu-id="1ffb3-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="1ffb3-158">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="1ffb3-158">Credit note</span></span>
    - <span data-ttu-id="1ffb3-159">Returordre</span><span class="sxs-lookup"><span data-stu-id="1ffb3-159">Return order</span></span>
    - <span data-ttu-id="1ffb3-160">Indkøbsrekvisition</span><span class="sxs-lookup"><span data-stu-id="1ffb3-160">Purchase requisition</span></span>
    - <span data-ttu-id="1ffb3-161">Diverse gebyrer til indkøbsrekvisitionslinje</span><span class="sxs-lookup"><span data-stu-id="1ffb3-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="1ffb3-162">Tilbudsanmodning</span><span class="sxs-lookup"><span data-stu-id="1ffb3-162">Request for quotation</span></span>
    - <span data-ttu-id="1ffb3-163">Diverse gebyrer i overskrift til tilbudsanmodning</span><span class="sxs-lookup"><span data-stu-id="1ffb3-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="1ffb3-164">Diverse gebyrer i linje til tilbudsanmodning</span><span class="sxs-lookup"><span data-stu-id="1ffb3-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="1ffb3-165">Lagerproces</span><span class="sxs-lookup"><span data-stu-id="1ffb3-165">Inventory process</span></span>

    - <span data-ttu-id="1ffb3-166">Flytteordre – send</span><span class="sxs-lookup"><span data-stu-id="1ffb3-166">Transfer order – ship</span></span>
    - <span data-ttu-id="1ffb3-167">Flytteordre – modtag</span><span class="sxs-lookup"><span data-stu-id="1ffb3-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="1ffb3-168">Tilknyttede ressourcer</span><span class="sxs-lookup"><span data-stu-id="1ffb3-168">Related resources</span></span>

[<span data-ttu-id="1ffb3-169">Start her med momstjeneste</span><span class="sxs-lookup"><span data-stu-id="1ffb3-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="1ffb3-170">Flere momsregistreringsnumre</span><span class="sxs-lookup"><span data-stu-id="1ffb3-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="1ffb3-171">Understøttelse af momsfunktion til flytteordre</span><span class="sxs-lookup"><span data-stu-id="1ffb3-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="1ffb3-172">Sådan bygger du udvidelse i momstjeneste</span><span class="sxs-lookup"><span data-stu-id="1ffb3-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)