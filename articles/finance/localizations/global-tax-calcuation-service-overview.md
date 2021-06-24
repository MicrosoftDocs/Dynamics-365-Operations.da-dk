---
title: Momsberegning (prøveversion)
description: Dette emne forklarer det overordnede område og funktionerne for til momsberegning.
author: wangchen
ms.date: 06/03/2021
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
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184095"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="2a7ec-103">Momsberegning (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="2a7ec-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="2a7ec-104">Momsberegning er en særdeles skalerbar flerdimensional tjeneste, som gør det muligt for det globale momsprogram at automatisere og forenkle fastlæggelse og beregning af moms.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="2a7ec-105">Momsprogrammet kan konfigureres fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="2a7ec-106">De elementer, der kan konfigureres, omfatter, men er ikke begrænset til, den momspligtige datamodel, momskode, matrix for anvendelse af moms og momsberegningsformlen.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="2a7ec-107">Momsprogrammet kører på Microsoft Azure-kerneserviceplatformen og tilbyder moderne teknologi og eksponentiel skalerbarhed.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="2a7ec-108">Beregning af moms kan integreres med Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="2a7ec-109">Senere vil det også blive integreret i , Dynamics 365 Project Operations, Dynamics 365 Commerce og andre programmer fra første part og tredjepart.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a7ec-110">Når du aktiverer tjenesten Momsberegning, kan der udføres visse handlinger på relaterede data i et andet datacenter end det datacenter, der vedligeholder dine tjenestedata.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-110">When you enable the Tax Calculation service, some operations on related data might be performed in a data center other than the data center that maintains your service data.</span></span> <span data-ttu-id="2a7ec-111">Gennemse [Vilkår og betingelser](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md), før du aktiverer tjenesten Momsberegning.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-111">Review the [Terms and Conditions](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) before you enable the Tax Calculation service.</span></span> <span data-ttu-id="2a7ec-112">Det er vigtigt for os at beskytte dine personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-112">Your privacy is important to us.</span></span> <span data-ttu-id="2a7ec-113">Du kan få mere at vide ved at læse vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=521839).</span><span class="sxs-lookup"><span data-stu-id="2a7ec-113">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

<span data-ttu-id="2a7ec-114">Momsberegning er et mikroservicebaseret momsprogram, der tilbyder eksponentiel skalerbarhed.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-114">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="2a7ec-115">Du kan få hjælp til at udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="2a7ec-115">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="2a7ec-116">Konfigurer momsberegning via Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="2a7ec-116">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="2a7ec-117">RCS er en udvidet version af ER-designeren (Elektronisk rapportering) og er tilgængelig som en enkeltstående tjeneste.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-117">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="2a7ec-118">Konfigurer momsmatrixen til automatisk at bestemme momskoder og -satser.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-118">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="2a7ec-119">Konfigurer momsmatrixen til automatisk at bestemme momsregistreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-119">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="2a7ec-120">Konfigurer momsberegningsdesigneren for at definere formler og betingelser.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-120">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="2a7ec-121">Del momsfastsættelses- og -beregningsløsningen på tværs af juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-121">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="2a7ec-122">Hvis du vil bruge tjenesten til momsberegning, skal du installere tilføjelsesprogrammet Momsberegningstjeneste fra dit projekt i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2a7ec-122">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="2a7ec-123">Fuldfør derefter opsætningen i RCS, og aktivér tjenesten til momsberegning i Finance og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-123">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="2a7ec-124">Du kan finde flere oplysninger i [Start her med momstjeneste](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="2a7ec-124">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="2a7ec-125">Tilgængelighed</span><span class="sxs-lookup"><span data-stu-id="2a7ec-125">Availability</span></span>

<span data-ttu-id="2a7ec-126">Momsberegning er kun tilgængelig i sandkassemiljøer og for udvalgte kunder via et offentligt forhåndsversionsprogram.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-126">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="2a7ec-127">Senere vil den blive generelt tilgængelig for alle kunder og i produktionsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-127">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="2a7ec-128">Der leveres fortsat nye funktioner, så du skal derfor sørge for ofte at læse den sidste nye dokumentation for at få mere at vide om dækning og området af understøttede funktioner.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-128">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="2a7ec-129">Momsberegning implementeres i følgende Azure-geografiske områder.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-129">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="2a7ec-130">Den vil også blive implementeret i flere Azure-geografiske områder baseret på kundernes behov:</span><span class="sxs-lookup"><span data-stu-id="2a7ec-130">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="2a7ec-131">United States</span><span class="sxs-lookup"><span data-stu-id="2a7ec-131">United States</span></span>
- <span data-ttu-id="2a7ec-132">Europa</span><span class="sxs-lookup"><span data-stu-id="2a7ec-132">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="2a7ec-133">Momsberegning understøtter ikke implementering i det lokale miljø af Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-133">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="2a7ec-134">Den understøtter heller ikke tidligere versioner, f.eks. Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-134">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="2a7ec-135">Fremhævning af funktioner</span><span class="sxs-lookup"><span data-stu-id="2a7ec-135">Feature highlights</span></span>

- <span data-ttu-id="2a7ec-136">En konfigurerbar momsmatrix til automatisk at bestemme og beregne moms</span><span class="sxs-lookup"><span data-stu-id="2a7ec-136">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="2a7ec-137">Understøttelse af flere momsregistreringsnumre</span><span class="sxs-lookup"><span data-stu-id="2a7ec-137">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="2a7ec-138">Understøttelse af flytteordre til fastlæggelse og beregning af moms</span><span class="sxs-lookup"><span data-stu-id="2a7ec-138">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="2a7ec-139">Understøttelse af flytteordre til fastlæggelse af flere momsregistreringsnumre</span><span class="sxs-lookup"><span data-stu-id="2a7ec-139">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="2a7ec-140">Understøttede transaktioner</span><span class="sxs-lookup"><span data-stu-id="2a7ec-140">Supported transactions</span></span>

<span data-ttu-id="2a7ec-141">Momsberegning kan aktiveres via juridisk enhed og transaktion.</span><span class="sxs-lookup"><span data-stu-id="2a7ec-141">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="2a7ec-142">Følgende transaktioner understøttes:</span><span class="sxs-lookup"><span data-stu-id="2a7ec-142">The following transactions are supported:</span></span>

- <span data-ttu-id="2a7ec-143">Salgsproces</span><span class="sxs-lookup"><span data-stu-id="2a7ec-143">Sales process</span></span>

    - <span data-ttu-id="2a7ec-144">Salgstilbud</span><span class="sxs-lookup"><span data-stu-id="2a7ec-144">Sales quotation</span></span>
    - <span data-ttu-id="2a7ec-145">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="2a7ec-145">Sales order</span></span>
    - <span data-ttu-id="2a7ec-146">Bekræftelse</span><span class="sxs-lookup"><span data-stu-id="2a7ec-146">Confirmation</span></span>
    - <span data-ttu-id="2a7ec-147">Plukliste</span><span class="sxs-lookup"><span data-stu-id="2a7ec-147">Picking list</span></span>
    - <span data-ttu-id="2a7ec-148">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="2a7ec-148">Packing slip</span></span>
    - <span data-ttu-id="2a7ec-149">Salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="2a7ec-149">Sales invoice</span></span>
    - <span data-ttu-id="2a7ec-150">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="2a7ec-150">Credit note</span></span>
    - <span data-ttu-id="2a7ec-151">Returordre</span><span class="sxs-lookup"><span data-stu-id="2a7ec-151">Return order</span></span>
    - <span data-ttu-id="2a7ec-152">Overskrift til diverse gebyrer</span><span class="sxs-lookup"><span data-stu-id="2a7ec-152">Header miscellaneous charge</span></span>
    - <span data-ttu-id="2a7ec-153">Linje til diverse gebyrer</span><span class="sxs-lookup"><span data-stu-id="2a7ec-153">Line miscellaneous charge</span></span>

- <span data-ttu-id="2a7ec-154">Indkøbsproces</span><span class="sxs-lookup"><span data-stu-id="2a7ec-154">Purchase process</span></span>

    - <span data-ttu-id="2a7ec-155">Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="2a7ec-155">Purchase order</span></span>
    - <span data-ttu-id="2a7ec-156">Bekræftelse</span><span class="sxs-lookup"><span data-stu-id="2a7ec-156">Confirmation</span></span>
    - <span data-ttu-id="2a7ec-157">Tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="2a7ec-157">Receipts list</span></span>
    - <span data-ttu-id="2a7ec-158">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="2a7ec-158">Product receipt</span></span>
    - <span data-ttu-id="2a7ec-159">Indkøbsfaktura</span><span class="sxs-lookup"><span data-stu-id="2a7ec-159">Purchase invoice</span></span>
    - <span data-ttu-id="2a7ec-160">Overskrift til diverse gebyrer</span><span class="sxs-lookup"><span data-stu-id="2a7ec-160">Header miscellaneous charge</span></span>
    - <span data-ttu-id="2a7ec-161">Linje til diverse gebyrer</span><span class="sxs-lookup"><span data-stu-id="2a7ec-161">Line miscellaneous charge</span></span>
    - <span data-ttu-id="2a7ec-162">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="2a7ec-162">Credit note</span></span>
    - <span data-ttu-id="2a7ec-163">Returordre</span><span class="sxs-lookup"><span data-stu-id="2a7ec-163">Return order</span></span>
    - <span data-ttu-id="2a7ec-164">Indkøbsrekvisition</span><span class="sxs-lookup"><span data-stu-id="2a7ec-164">Purchase requisition</span></span>
    - <span data-ttu-id="2a7ec-165">Diverse gebyrer til indkøbsrekvisitionslinje</span><span class="sxs-lookup"><span data-stu-id="2a7ec-165">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="2a7ec-166">Tilbudsanmodning</span><span class="sxs-lookup"><span data-stu-id="2a7ec-166">Request for quotation</span></span>
    - <span data-ttu-id="2a7ec-167">Diverse gebyrer i overskrift til tilbudsanmodning</span><span class="sxs-lookup"><span data-stu-id="2a7ec-167">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="2a7ec-168">Diverse gebyrer i linje til tilbudsanmodning</span><span class="sxs-lookup"><span data-stu-id="2a7ec-168">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="2a7ec-169">Lagerproces</span><span class="sxs-lookup"><span data-stu-id="2a7ec-169">Inventory process</span></span>

    - <span data-ttu-id="2a7ec-170">Flytteordre – send</span><span class="sxs-lookup"><span data-stu-id="2a7ec-170">Transfer order – ship</span></span>
    - <span data-ttu-id="2a7ec-171">Flytteordre – modtag</span><span class="sxs-lookup"><span data-stu-id="2a7ec-171">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="2a7ec-172">Tilknyttede ressourcer</span><span class="sxs-lookup"><span data-stu-id="2a7ec-172">Related resources</span></span>

[<span data-ttu-id="2a7ec-173">Start her med momstjeneste</span><span class="sxs-lookup"><span data-stu-id="2a7ec-173">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="2a7ec-174">Flere momsregistreringsnumre</span><span class="sxs-lookup"><span data-stu-id="2a7ec-174">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="2a7ec-175">Understøttelse af momsfunktion til flytteordre</span><span class="sxs-lookup"><span data-stu-id="2a7ec-175">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="2a7ec-176">Sådan bygger du udvidelse i momstjeneste</span><span class="sxs-lookup"><span data-stu-id="2a7ec-176">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)
