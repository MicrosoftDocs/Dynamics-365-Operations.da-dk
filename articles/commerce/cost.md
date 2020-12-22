---
title: Omkostningskonfiguration for fordelt ordrestyring (DOM)
description: Dette emne beskriver omkostningskonfiguration til fordelt ordrestyring (DOM) i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7644cb9800a418fd123b32a0257b787277fcb19f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458656"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="09ac6-103">Omkostningskonfiguration for fordelt ordrestyring (DOM)</span><span class="sxs-lookup"><span data-stu-id="09ac6-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09ac6-104">Organisationer betragter flere omkostningskomponenter for at bestemme den optimale lokation, som ordren skal opfyldes fra.</span><span class="sxs-lookup"><span data-stu-id="09ac6-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="09ac6-105">Nogle af disse omkostningskomponenter er forsendelsesomkostninger, håndteringsomkostninger og emballageomkostninger.</span><span class="sxs-lookup"><span data-stu-id="09ac6-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="09ac6-106">Der beregnes en kombination af disse omkostninger for at bestemme opfyldelseslokationen.</span><span class="sxs-lookup"><span data-stu-id="09ac6-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="09ac6-107">Når den første gentagelse af den fordelte ordrestyring (DOM) i Dynamics 365 Commerce har optimeret tildelingen af ordrer på opfyldelseslokationer, er den kun indregnet i afstanden.</span><span class="sxs-lookup"><span data-stu-id="09ac6-107">When the first iteration of distributed order management (DOM) in Dynamics 365 Commerce optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="09ac6-108">Selvom afstanden kan korreleres med en omkostning, er det ikke det samme som omkostning.</span><span class="sxs-lookup"><span data-stu-id="09ac6-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="09ac6-109">En forsendelsesmetode om natten koster f.eks. mere end tre dages forsendelse eller syv dages forsendelse over den samme afstand.</span><span class="sxs-lookup"><span data-stu-id="09ac6-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="09ac6-110">Med funktionen til omkostningskonfiguration kan detailforretninger definere og konfigurere yderligere omkostningskomponenter, der skal beregnes og medtages for at bestemme den optimale lokation, som ordrelinjer skal opfyldes fra.</span><span class="sxs-lookup"><span data-stu-id="09ac6-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="09ac6-111">Når omkostningskomponenter er konfigureret, bruger DOM-problemløseren kun disse omkostningsdefinitioner til at bestemme den optimale lokation for ordreopfyldelse.</span><span class="sxs-lookup"><span data-stu-id="09ac6-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="09ac6-112">Den betragter ikke afstandskomponenten som en omkostning.</span><span class="sxs-lookup"><span data-stu-id="09ac6-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="09ac6-113">Men, hvis ingen omkostningskomponenter er konfigureret, bruger DOM-problemløseren ikke afstandskomponenten som en omkostning til at bestemme den optimale lokation for ordreopfyldelse.</span><span class="sxs-lookup"><span data-stu-id="09ac6-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="09ac6-114">Konfigurere omkostningskomponenter</span><span class="sxs-lookup"><span data-stu-id="09ac6-114">Set up cost components</span></span>

<span data-ttu-id="09ac6-115">Der kan defineres to overordnede typer af omkostningskomponenter i systemet: **Forsendelse** og **Anden**.</span><span class="sxs-lookup"><span data-stu-id="09ac6-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="09ac6-116">Begge typer af omkostningskomponent understøtter flere beregningsbasis, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="09ac6-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="09ac6-117">Type af omkostningskomponent</span><span class="sxs-lookup"><span data-stu-id="09ac6-117">Cost component type</span></span></th>
<th><span data-ttu-id="09ac6-118">Beregningsbasis</span><span class="sxs-lookup"><span data-stu-id="09ac6-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ac6-119">Forsendelse</span><span class="sxs-lookup"><span data-stu-id="09ac6-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="09ac6-120">Simpel</span><span class="sxs-lookup"><span data-stu-id="09ac6-120">Simple</span></span></li>
<li><span data-ttu-id="09ac6-121">Lagdelt</span><span class="sxs-lookup"><span data-stu-id="09ac6-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="09ac6-122">Anden</span><span class="sxs-lookup"><span data-stu-id="09ac6-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="09ac6-123">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="09ac6-123">Sales order</span></span></li>
<li><span data-ttu-id="09ac6-124">Salgslinje</span><span class="sxs-lookup"><span data-stu-id="09ac6-124">Sales line</span></span></li>
<li><span data-ttu-id="09ac6-125">Lokation</span><span class="sxs-lookup"><span data-stu-id="09ac6-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="09ac6-126">Komponenttype af forsendelsesomkostning</span><span class="sxs-lookup"><span data-stu-id="09ac6-126">Shipping cost component type</span></span>

<span data-ttu-id="09ac6-127">Dette afsnit forklarer, hvordan du kan oprette hver enkelt kombination af omkostningskomponenttypen **Forsendelse** og beregningsbasis for forsendelsesomkostninger.</span><span class="sxs-lookup"><span data-stu-id="09ac6-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="09ac6-128">Det forklarer også, hvordan DOM-problemløseren bruger de enkelte kombinationer.</span><span class="sxs-lookup"><span data-stu-id="09ac6-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="09ac6-129">Omkostningskomponenttype = forsendelses- og beregningsbasis = simpel</span><span class="sxs-lookup"><span data-stu-id="09ac6-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="09ac6-130">Hvis der bruges en kombination af omkostningskomponenttypen **Forsendelse** og **Simpel** beregningsbasis, baseres forsendelsesomkostningerne for en leveringsmåde enten på en flad omkostning eller afstand.</span><span class="sxs-lookup"><span data-stu-id="09ac6-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="09ac6-131">Du skal konfigurere følgende felter for denne kombination:</span><span class="sxs-lookup"><span data-stu-id="09ac6-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="09ac6-132">**Omkostningsfaktor** – Angiv et entydigt id for omkostningsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="09ac6-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="09ac6-133">**Beskrivelse** – Indtast navnet og beskrivelse for omkostningsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="09ac6-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="09ac6-134">**Startdato** og **Slutdato** – Du kan bruge disse felter til at begrænse omkostningsfaktoren til et bestemt datointerval.</span><span class="sxs-lookup"><span data-stu-id="09ac6-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="09ac6-135">Hvis du ikke udfylder disse felter, gælder for omkostningsfaktoren for en uendelig periode.</span><span class="sxs-lookup"><span data-stu-id="09ac6-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="09ac6-136">**Aktiv** – Angiv, om omkostningsfaktoren er aktiv.</span><span class="sxs-lookup"><span data-stu-id="09ac6-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="09ac6-137">DOM benytter kun aktive omkostningsfaktorer, der er tilknyttet opfyldningsprofilen.</span><span class="sxs-lookup"><span data-stu-id="09ac6-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="09ac6-138">**Regnskab** – Angiv den juridiske enhed, som omkostningsfaktoren er konfigureret til.</span><span class="sxs-lookup"><span data-stu-id="09ac6-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="09ac6-139">Alle linjer i beregningskriterierne skal være for den samme juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="09ac6-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="09ac6-140">**Leveringsmåder** – Angiv de leveringsmåder, som omkostningen er konfigureret for.</span><span class="sxs-lookup"><span data-stu-id="09ac6-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="09ac6-141">**Beregningstype** – Angiv, hvordan omkostningen skal beregnes for en bestemt leveringsmåde.</span><span class="sxs-lookup"><span data-stu-id="09ac6-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="09ac6-142">Der understøttes to beregningstyper:</span><span class="sxs-lookup"><span data-stu-id="09ac6-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="09ac6-143">**Fast** – En fast omkostning bruges til leveringsmåden.</span><span class="sxs-lookup"><span data-stu-id="09ac6-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="09ac6-144">Hvis du vælger denne beregningstype, definerer feltet **Omkostning** de faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="09ac6-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="09ac6-145">**Pr. afstandsenhed** – Omkostningen for leveringsmåden beregnes som den kostværdi, der er angivet i feltet **Omkostning**, gange afstanden mellem leveringsadressen og lokationerne.</span><span class="sxs-lookup"><span data-stu-id="09ac6-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="09ac6-146">**Omkostning** – Angiv den kostværdi, der skal bruges sammen med feltet **Beregningstype** til at beregne omkostningen for en leveringsmåde.</span><span class="sxs-lookup"><span data-stu-id="09ac6-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="09ac6-147">Omkostningskomponenttype = forsendelses- og beregningsbasis = lagdelt</span><span class="sxs-lookup"><span data-stu-id="09ac6-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="09ac6-148">Hvis der bruges en kombination af omkostningskomponenttypen **Forsendelse** og **Lagdelt** beregningsbasis, baseres forsendelsesomkostningerne for en leveringsmåde enten på en flad omkostning eller afstand.</span><span class="sxs-lookup"><span data-stu-id="09ac6-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="09ac6-149">Men i denne kombination baseres afstanden på et lagdelt interval af afstande.</span><span class="sxs-lookup"><span data-stu-id="09ac6-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="09ac6-150">Du skal konfigurere følgende felter for denne kombination:</span><span class="sxs-lookup"><span data-stu-id="09ac6-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="09ac6-151">**Omkostningsfaktor** – Angiv et entydigt id for omkostningsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="09ac6-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="09ac6-152">**Beskrivelse** – Indtast navnet og beskrivelse for omkostningsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="09ac6-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="09ac6-153">**Standardomkostning** – Angiv den omkostning, der skal bruges til en leveringsmåde, hvis afstanden mellem leveringsadressen og lokationen ikke falder i nogen af de lagdelte afstande for leveringsmåden.</span><span class="sxs-lookup"><span data-stu-id="09ac6-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="09ac6-154">**Startdato** og **Slutdato** – Du kan bruge disse felter til at begrænse omkostningsfaktoren til et bestemt datointerval.</span><span class="sxs-lookup"><span data-stu-id="09ac6-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="09ac6-155">Hvis du ikke udfylder disse felter, gælder for omkostningsfaktoren for en uendelig periode.</span><span class="sxs-lookup"><span data-stu-id="09ac6-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="09ac6-156">**Aktiv** – Angiv, om omkostningsfaktoren er aktiv.</span><span class="sxs-lookup"><span data-stu-id="09ac6-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="09ac6-157">DOM benytter kun aktive omkostningsfaktorer, der er tilknyttet opfyldningsprofilen.</span><span class="sxs-lookup"><span data-stu-id="09ac6-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="09ac6-158">**Regnskab** – Angiv den juridiske enhed, som omkostningsfaktoren er konfigureret til.</span><span class="sxs-lookup"><span data-stu-id="09ac6-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="09ac6-159">Alle linjer i beregningskriterierne skal være for den samme juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="09ac6-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="09ac6-160">**Leveringsmåder** – Angiv de leveringsmåder, som omkostningen er konfigureret for.</span><span class="sxs-lookup"><span data-stu-id="09ac6-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="09ac6-161">**Afstandstype** – Angiv, om den lagdelte afstandsdefinition er en afstand i luftlinje eller en vejafstand.</span><span class="sxs-lookup"><span data-stu-id="09ac6-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="09ac6-162">**Afstandsenheder** – Angiv den enhed, som den lagdelte afstand måles i.</span><span class="sxs-lookup"><span data-stu-id="09ac6-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="09ac6-163">**Afstand fra** – Angiv startintervallet for den lagdelte afstand.</span><span class="sxs-lookup"><span data-stu-id="09ac6-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="09ac6-164">**Afstand til** – Angiv slutintervallet for den lagdelte afstand.</span><span class="sxs-lookup"><span data-stu-id="09ac6-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="09ac6-165">**Beregningstype** – Angiv, hvordan omkostningen skal beregnes for en bestemt leveringsmåde og lagdelt afstand.</span><span class="sxs-lookup"><span data-stu-id="09ac6-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="09ac6-166">Der understøttes to beregningstyper:</span><span class="sxs-lookup"><span data-stu-id="09ac6-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="09ac6-167">**Fast** – En fast omkostning bruges til leveringsmåden.</span><span class="sxs-lookup"><span data-stu-id="09ac6-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="09ac6-168">Hvis du vælger denne beregningstype, definerer feltet **Omkostning** de faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="09ac6-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="09ac6-169">**Pr. afstandsenhed** – Omkostningen for leveringsmåden og den lagdelte afstand beregnes som den kostværdi, der er angivet i feltet **Omkostning**, gange afstanden mellem leveringsadressen og lokationerne.</span><span class="sxs-lookup"><span data-stu-id="09ac6-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="09ac6-170">**Omkostning** – Angiv den kostværdi, der skal bruges sammen med feltet **Beregningstype** til at beregne omkostningen for en leveringsmåde.</span><span class="sxs-lookup"><span data-stu-id="09ac6-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="09ac6-171">Når du definerer lagdelte afstande, validerer systemet, at der ikke er nogen manglende eller overlappende afstande.</span><span class="sxs-lookup"><span data-stu-id="09ac6-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="09ac6-172">Den afstandstype, der bruges til leveringsmåden, skal være den samme på tværs af alle de lagdelte afstande.</span><span class="sxs-lookup"><span data-stu-id="09ac6-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="09ac6-173">Anden type af omkostningskomponent</span><span class="sxs-lookup"><span data-stu-id="09ac6-173">Other cost component type</span></span>

<span data-ttu-id="09ac6-174">Dette afsnit forklarer, hvordan du kan oprette hver enkelt kombination af omkostningskomponenttypen **Anden** og en anden omkostningstype for ikke-forsendelsesomkostninger.</span><span class="sxs-lookup"><span data-stu-id="09ac6-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="09ac6-175">Det forklarer også, hvordan DOM-problemløseren bruger de enkelte kombinationer.</span><span class="sxs-lookup"><span data-stu-id="09ac6-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="09ac6-176">Omkostningskomponent type = anden og anden omkostningstype = salgsordre</span><span class="sxs-lookup"><span data-stu-id="09ac6-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="09ac6-177">En kombination af omkostningskomponenttypen **Anden** og den anden omkostningstype **Salgsordre** bruges til at definere ikke-forsendelsesomkostninger på salgsordreniveau.</span><span class="sxs-lookup"><span data-stu-id="09ac6-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="09ac6-178">Du skal konfigurere følgende felter for denne kombination:</span><span class="sxs-lookup"><span data-stu-id="09ac6-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="09ac6-179">**Omkostningsfaktor** – Angiv et entydigt id for omkostningsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="09ac6-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="09ac6-180">**Beskrivelse** – Indtast navnet og beskrivelse for omkostningsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="09ac6-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="09ac6-181">**Startdato** og **Slutdato** – Du kan bruge disse felter til at begrænse omkostningsfaktoren til et bestemt datointerval.</span><span class="sxs-lookup"><span data-stu-id="09ac6-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="09ac6-182">Hvis du ikke udfylder disse felter, gælder for omkostningsfaktoren for en uendelig periode.</span><span class="sxs-lookup"><span data-stu-id="09ac6-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="09ac6-183">**Aktiv** – Angiv, om omkostningsfaktoren er aktiv.</span><span class="sxs-lookup"><span data-stu-id="09ac6-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="09ac6-184">DOM benytter kun aktive omkostningsfaktorer, der er tilknyttet opfyldningsprofilen.</span><span class="sxs-lookup"><span data-stu-id="09ac6-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="09ac6-185">**Omkostninger** – Angiv kostværdien for en ikke-forsendelsesomkostning på salgsordreniveau.</span><span class="sxs-lookup"><span data-stu-id="09ac6-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="09ac6-186">Omkostningskomponent type = anden og anden omkostningstype = salgslinje</span><span class="sxs-lookup"><span data-stu-id="09ac6-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="09ac6-187">En kombination af omkostningskomponenttypen **Anden** og den anden omkostningstype **Salgslinje** bruges til at definere ikke-forsendelsesomkostninger på salgsordrelinjeniveau.</span><span class="sxs-lookup"><span data-stu-id="09ac6-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="09ac6-188">Du skal konfigurere følgende felter for denne kombination:</span><span class="sxs-lookup"><span data-stu-id="09ac6-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="09ac6-189">**Omkostningsfaktor** – Angiv et entydigt id for omkostningsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="09ac6-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="09ac6-190">**Beskrivelse** – Indtast navnet og beskrivelse for omkostningsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="09ac6-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="09ac6-191">**Startdato** og **Slutdato** – Du kan bruge disse felter til at begrænse omkostningsfaktoren til et bestemt datointerval.</span><span class="sxs-lookup"><span data-stu-id="09ac6-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="09ac6-192">Hvis du ikke udfylder disse felter, gælder for omkostningsfaktoren for en uendelig periode.</span><span class="sxs-lookup"><span data-stu-id="09ac6-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="09ac6-193">**Aktiv** – Angiv, om omkostningsfaktoren er aktiv.</span><span class="sxs-lookup"><span data-stu-id="09ac6-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="09ac6-194">DOM benytter kun aktive omkostningsfaktorer, der er tilknyttet opfyldningsprofilen.</span><span class="sxs-lookup"><span data-stu-id="09ac6-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="09ac6-195">**Omkostninger** – Angiv kostværdien for en ikke-forsendelsesomkostning på salgsordrelinjeniveau.</span><span class="sxs-lookup"><span data-stu-id="09ac6-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="09ac6-196">Omkostningskomponent type = anden og anden omkostningstype = lokation</span><span class="sxs-lookup"><span data-stu-id="09ac6-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="09ac6-197">En kombination af omkostningskomponenttypen **Anden** og den anden omkostningstype **Lokation** bruges til at definere ikke-forsendelsesomkostninger for en gruppe af lokationer eller en enkelt lokation.</span><span class="sxs-lookup"><span data-stu-id="09ac6-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="09ac6-198">Du skal konfigurere følgende felter for denne kombination:</span><span class="sxs-lookup"><span data-stu-id="09ac6-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="09ac6-199">**Omkostningsfaktor** – Angiv et entydigt id for omkostningsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="09ac6-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="09ac6-200">**Beskrivelse** – Indtast navnet og beskrivelse for omkostningsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="09ac6-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="09ac6-201">**Startdato** og **Slutdato** – Du kan bruge disse felter til at begrænse omkostningsfaktoren til et bestemt datointerval.</span><span class="sxs-lookup"><span data-stu-id="09ac6-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="09ac6-202">Hvis du ikke udfylder disse felter, gælder for omkostningsfaktoren for en uendelig periode.</span><span class="sxs-lookup"><span data-stu-id="09ac6-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="09ac6-203">**Aktiv** – Angiv, om omkostningsfaktoren er aktiv.</span><span class="sxs-lookup"><span data-stu-id="09ac6-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="09ac6-204">DOM benytter kun aktive omkostningsfaktorer, der er tilknyttet opfyldningsprofilen.</span><span class="sxs-lookup"><span data-stu-id="09ac6-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="09ac6-205">**Opfyldelsesgruppe** – Angiv den gruppe af lokationer, som ikke-forsendelsesomkostningen er defineret for.</span><span class="sxs-lookup"><span data-stu-id="09ac6-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="09ac6-206">**Opfyldelseslokation** – Angiv den lokation, som ikke-forsendelsesomkostningen er defineret for.</span><span class="sxs-lookup"><span data-stu-id="09ac6-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="09ac6-207">Du kan ikke angive en opfyldelsesgruppe og en opfyldelseslokation på den samme linje for lokationsbaserede beregningskriterier.</span><span class="sxs-lookup"><span data-stu-id="09ac6-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="09ac6-208">**Omkostninger** – Angiv kostværdien for en ikke-forsendelsesomkostning på opfyldelsesgruppeniveau eller opfyldelseslokationsniveau.</span><span class="sxs-lookup"><span data-stu-id="09ac6-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09ac6-209">Hvis DOM skal medtage disse omkostninger, når de køres, skal du føje omkostningsfaktoren til den relevante opfyldelsesprofil.</span><span class="sxs-lookup"><span data-stu-id="09ac6-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>
