---
title: Oversigt over kvalitetsstyring
description: I dette emne beskrives det, hvordan du kan bruge kvalitetsstyring i Dynamics 365 Supply Chain Management til at forbedre produktkvaliteten i forsyningskæden.
author: perlynne
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba38f9c43fed81768155a27dda88a4bfb4a7828e
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653550"
---
# <a name="quality-management-overview"></a><span data-ttu-id="3ecc3-103">Oversigt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="3ecc3-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ecc3-104">I dette emne beskrives det, hvordan du kan bruge kvalitetsstyring i Dynamics 365 Supply Chain Management til at forbedre produktkvaliteten i forsyningskæden.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="3ecc3-105">Kvalitetsstyring kan hjælpe dig med at administrere behandlingstid, når du håndterer ikke-standardiserede produkter, uanset deres oprindelsessted.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="3ecc3-106">Fordi diagnosticeringstyper er knyttet til rapportering af korrektion, kan Supply Chain Management planlægge opgaver for at løse problemer og forhindre dem i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="3ecc3-107">Ud over funktionalitet til administration af uoverensstemmelse omfatter kvalitetsstyring funktionalitet til sporing af problemer efter problemtype (også interne problemer) og til identificering af løsninger som kortsigtede eller langsigtede.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="3ecc3-108">Statistik over nøgletal (KPI'er) giver indsigt i historikken for tidligere problemer med uoverensstemmelse, og de løsninger, der blev anvendt til at rette dem.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="3ecc3-109">Du kan bruge historikdata til at gennemgå effektiviteten af tidligere kvalitetsmål og fastlægge passende foranstaltninger, der skal bruges i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="3ecc3-110">Når du opretter en kvalitetstilknytning, kan Supply Chain Management oprette kvalitetsordrer for forskellige forretningsprocesser, hændelser og betingelser.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="3ecc3-111">Kvalitetstilknytningen kan dække en bestemt vare, en bestemt gruppe varer eller alle varer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="3ecc3-112">Eksempler på brug af kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="3ecc3-112">Examples of the use of quality management</span></span>
<span data-ttu-id="3ecc3-113">Kvalitetsstyring er fleksibel og kan gennemføres på forskellige måder for at opfylde kravene på bestemte niveauer i forsyningskædeoperationer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="3ecc3-114">Eksemplerne nedenfor viser mulige anvendelser af disse funktioner:</span><span class="sxs-lookup"><span data-stu-id="3ecc3-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="3ecc3-115">Automatisk starte en proces for kvalitetskontrol baseret på foruddefinerede kriterier (ved lagerregistreringen af en indkøbsordre fra en bestemt leverandør).</span><span class="sxs-lookup"><span data-stu-id="3ecc3-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="3ecc3-116">Spærre lageret under kontrol for at forhindre, at ikke-godkendt lagerbeholdning bliver brugt (fuld spærring af indkøbsordreantal).</span><span class="sxs-lookup"><span data-stu-id="3ecc3-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="3ecc3-117">Bruge vareprøve som en del af en kvalitetstilknytning til at definere beløbet af det aktuelle fysiske lager, der skal undersøges.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="3ecc3-118">Vareprøver kan baseres på faste antal eller en procentdel.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="3ecc3-119">Opret kvalitetsordrer for delleverancer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="3ecc3-120">For at oprette en kvalitetsordre, der er baseret på det antal, der fysisk er modtaget med en ordre, skal du markere afkrydsningsfeltet **Pr. opdateret antal** i formularen **Vareprøve**.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="3ecc3-121">Oprette testtyper, der omfatter minimum, maksimum og måltestværdier og udføre kvalitative kontra kvantitative test, der har foruddefinerede valideringsresultater.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="3ecc3-122">Angive et acceptabelt kvalitetsniveau (AQL) for at styre tolerancer for kvalitetsmål.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="3ecc3-123">Angive de ressourcer, som en inspektionshandling kræver, f.eks. et testområde og testinstrumenter.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="3ecc3-124">Arbejde med kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="3ecc3-124">Working with quality associations</span></span>
<span data-ttu-id="3ecc3-125">Den forretningsproces, der bruger en kvalitetstilknytning, kan knyttes til forskellige kildedokumenter, f.eks. indkøbsordrer, salgsordrer eller produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="3ecc3-126">De enkelte kvalitetstilknytningsposter definerer de test, det acceptable kvalitetsniveau (AQL) og den vareprøveplan, der gælder for de kvalitetsordrer, der oprettes.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="3ecc3-127">Du skal definere en kvalitetstilknytningspost for hver ændring i en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="3ecc3-128">Du kan f.eks. angive en kvalitetstilknytning, der genererer en kvalitetsordre, når en produktkvittering for en indkøbsordre opdateres.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="3ecc3-129">Afhængigt af opsætningen af udførelsesplanen kan selve den udløsende proces blive blokeret, mens der er en åben kvalitetsordre, eller de næste processer, som f.eks. fakturering, kan blive blokeret.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="3ecc3-130">**Bemærk!** Der kan være åbne kvalitetsordrer, men lagerantal blokeres automatisk fra at blive udstedet.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="3ecc3-131">Afhængigt af indstillingen **Fuld spærring** på siden **Stikprøver af varer** er antallet enten kvantiteten i kvalitetsordren eller kvantiteten i kildedokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="3ecc3-132">For en given forretningsproces identificerer kvalitetstilknytningsposten hændelsen og de betingelser, som der oprettes en kvalitetsordre for.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="3ecc3-133">Betingelserne kan være specifikke for et sted eller en juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="3ecc3-134">En kvalitetsordre, der involverer destruktive prøvninger, kan kun oprettes, når der findes en disponible lagerbeholdning for hændelsen.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="3ecc3-135">I følgende eksempel vises, hvordan en kvalitetstilknytningspost defineres for variationerne i de enkelte forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="3ecc3-136">Eksemplerne vises også i følgende tabel som en oversigt over de hændelser og betingelser, der er defineret af en kvalitetstilknytningspost.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="3ecc3-137">Referencetype</span><span class="sxs-lookup"><span data-stu-id="3ecc3-137">Reference type</span></span></th>
<th><span data-ttu-id="3ecc3-138">Hændelsestype</span><span class="sxs-lookup"><span data-stu-id="3ecc3-138">Event type</span></span></th>
<th><span data-ttu-id="3ecc3-139">Udførelse</span><span class="sxs-lookup"><span data-stu-id="3ecc3-139">Execution</span></span></th>
<th><span data-ttu-id="3ecc3-140">Hændelsesspærring</span><span class="sxs-lookup"><span data-stu-id="3ecc3-140">Event blocking</span></span></th>
<th><span data-ttu-id="3ecc3-141">Dokumentreference</span><span class="sxs-lookup"><span data-stu-id="3ecc3-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-142">Lager</span><span class="sxs-lookup"><span data-stu-id="3ecc3-142">Inventory</span></span></td>
<td><span data-ttu-id="3ecc3-143">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="3ecc3-143">Not applicable</span></span></td>
<td><span data-ttu-id="3ecc3-144">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="3ecc3-144">Not applicable</span></span></td>
<td><span data-ttu-id="3ecc3-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-145">None</span></span></td>
<td><span data-ttu-id="3ecc3-146">Alle</span><span class="sxs-lookup"><span data-stu-id="3ecc3-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="3ecc3-147">Salg</span><span class="sxs-lookup"><span data-stu-id="3ecc3-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="3ecc3-148">Plukproces er planlagt</span><span class="sxs-lookup"><span data-stu-id="3ecc3-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="3ecc3-149">Før</span><span class="sxs-lookup"><span data-stu-id="3ecc3-149">Before</span></span></td>
<td><span data-ttu-id="3ecc3-150">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="3ecc3-151">Bestemt id, gruppe eller kun alle</span><span class="sxs-lookup"><span data-stu-id="3ecc3-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-152">Plukproces</span><span class="sxs-lookup"><span data-stu-id="3ecc3-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-153">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="3ecc3-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-154">Faktura</span><span class="sxs-lookup"><span data-stu-id="3ecc3-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3ecc3-155">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="3ecc3-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="3ecc3-156">Før</span><span class="sxs-lookup"><span data-stu-id="3ecc3-156">Before</span></span></td>
<td><span data-ttu-id="3ecc3-157">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-158">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="3ecc3-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-159">Faktura</span><span class="sxs-lookup"><span data-stu-id="3ecc3-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="3ecc3-160">Indkøb</span><span class="sxs-lookup"><span data-stu-id="3ecc3-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="3ecc3-161">Tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="3ecc3-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="3ecc3-162">Før</span><span class="sxs-lookup"><span data-stu-id="3ecc3-162">Before</span></span></td>
<td><span data-ttu-id="3ecc3-163">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-164">Tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="3ecc3-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-165">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="3ecc3-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-166">Faktura</span><span class="sxs-lookup"><span data-stu-id="3ecc3-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3ecc3-167">Efter</span><span class="sxs-lookup"><span data-stu-id="3ecc3-167">After</span></span></td>
<td><span data-ttu-id="3ecc3-168">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-169">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="3ecc3-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-170">Faktura</span><span class="sxs-lookup"><span data-stu-id="3ecc3-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3ecc3-171">Registrering</span><span class="sxs-lookup"><span data-stu-id="3ecc3-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="3ecc3-172">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="3ecc3-172">Not applicable</span></span></td>
<td><span data-ttu-id="3ecc3-173">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-174">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="3ecc3-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-175">Faktura</span><span class="sxs-lookup"><span data-stu-id="3ecc3-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="3ecc3-176">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="3ecc3-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="3ecc3-177">Før</span><span class="sxs-lookup"><span data-stu-id="3ecc3-177">Before</span></span></td>
<td><span data-ttu-id="3ecc3-178">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-179">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="3ecc3-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-180">Faktura</span><span class="sxs-lookup"><span data-stu-id="3ecc3-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3ecc3-181">Efter</span><span class="sxs-lookup"><span data-stu-id="3ecc3-181">After</span></span></td>
<td><span data-ttu-id="3ecc3-182">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-183">Faktura</span><span class="sxs-lookup"><span data-stu-id="3ecc3-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="3ecc3-184">Produktion</span><span class="sxs-lookup"><span data-stu-id="3ecc3-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="3ecc3-185">Registrering</span><span class="sxs-lookup"><span data-stu-id="3ecc3-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="3ecc3-186">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="3ecc3-186">Not applicable</span></span></td>
<td><span data-ttu-id="3ecc3-187">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="3ecc3-188">Alle</span><span class="sxs-lookup"><span data-stu-id="3ecc3-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-189">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="3ecc3-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-190">Afslut</span><span class="sxs-lookup"><span data-stu-id="3ecc3-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="3ecc3-191">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="3ecc3-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="3ecc3-192">Før</span><span class="sxs-lookup"><span data-stu-id="3ecc3-192">Before</span></span></td>
<td><span data-ttu-id="3ecc3-193">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-194">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="3ecc3-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-195">Afslut</span><span class="sxs-lookup"><span data-stu-id="3ecc3-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3ecc3-196">Efter</span><span class="sxs-lookup"><span data-stu-id="3ecc3-196">After</span></span></td>
<td><span data-ttu-id="3ecc3-197">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-198">Afslut</span><span class="sxs-lookup"><span data-stu-id="3ecc3-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="3ecc3-199">Karantæne</span><span class="sxs-lookup"><span data-stu-id="3ecc3-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="3ecc3-200">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="3ecc3-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="3ecc3-201">Før</span><span class="sxs-lookup"><span data-stu-id="3ecc3-201">Before</span></span></td>
<td><span data-ttu-id="3ecc3-202">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="3ecc3-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-203">Afslut</span><span class="sxs-lookup"><span data-stu-id="3ecc3-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-204">Efter</span><span class="sxs-lookup"><span data-stu-id="3ecc3-204">After</span></span></td>
<td><span data-ttu-id="3ecc3-205">Afslut</span><span class="sxs-lookup"><span data-stu-id="3ecc3-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-206">Afslut</span><span class="sxs-lookup"><span data-stu-id="3ecc3-206">End</span></span></td>
<td><span data-ttu-id="3ecc3-207">Før</span><span class="sxs-lookup"><span data-stu-id="3ecc3-207">Before</span></span></td>
<td><span data-ttu-id="3ecc3-208">Afslut</span><span class="sxs-lookup"><span data-stu-id="3ecc3-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3ecc3-209">Ruteoperation</span><span class="sxs-lookup"><span data-stu-id="3ecc3-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="3ecc3-210">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="3ecc3-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="3ecc3-211">Før</span><span class="sxs-lookup"><span data-stu-id="3ecc3-211">Before</span></span></td>
<td><span data-ttu-id="3ecc3-212">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="3ecc3-213">Bestemt id, gruppe eller alle, og ressourcespecifik, gruppe eller alle</span><span class="sxs-lookup"><span data-stu-id="3ecc3-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-214">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="3ecc3-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-215">Efter</span><span class="sxs-lookup"><span data-stu-id="3ecc3-215">After</span></span></td>
<td><span data-ttu-id="3ecc3-216">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3ecc3-217">Produktion af samprodukter</span><span class="sxs-lookup"><span data-stu-id="3ecc3-217">Co-product production</span></span></td>
<td><span data-ttu-id="3ecc3-218">Registrering</span><span class="sxs-lookup"><span data-stu-id="3ecc3-218">Registration</span></span></td>
<td><span data-ttu-id="3ecc3-219">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="3ecc3-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3ecc3-220">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="3ecc3-221">Alle</span><span class="sxs-lookup"><span data-stu-id="3ecc3-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3ecc3-222">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="3ecc3-222">Report as finished</span></span></td>
<td><span data-ttu-id="3ecc3-223">Før</span><span class="sxs-lookup"><span data-stu-id="3ecc3-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-224">Efter</span><span class="sxs-lookup"><span data-stu-id="3ecc3-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3ecc3-225">Tabellen nedenfor indeholder flere oplysninger om, hvordan kvalitetsordrer kan oprettes for bestemte typer processer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="3ecc3-226">Procestype</span><span class="sxs-lookup"><span data-stu-id="3ecc3-226">Type of process</span></span></th>
<th><span data-ttu-id="3ecc3-227">Når kvalitetsordrer kan genereres automatisk</span><span class="sxs-lookup"><span data-stu-id="3ecc3-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="3ecc3-228">Når kvalitetsordrer kan genereres, hvis destruktiv prøvning er påkrævet</span><span class="sxs-lookup"><span data-stu-id="3ecc3-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="3ecc3-229">Betingelsesoplysninger</span><span class="sxs-lookup"><span data-stu-id="3ecc3-229">Condition information</span></span></th>
<th><span data-ttu-id="3ecc3-230">Manuel oprettelse af oplysninger</span><span class="sxs-lookup"><span data-stu-id="3ecc3-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-231">Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="3ecc3-231">Purchase order</span></span></td>
<td><span data-ttu-id="3ecc3-232">Før eller efter en tilgangsliste eller produktkvittering for det materiale, der er modtaget, bogføres</span><span class="sxs-lookup"><span data-stu-id="3ecc3-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="3ecc3-233">Efter produktkvitteringen for det materiale, der er modtaget, bogføres, da materialet skal være tilgængelig til destruktiv prøvning</span><span class="sxs-lookup"><span data-stu-id="3ecc3-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="3ecc3-234">Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller kreditor eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="3ecc3-235">En manuelt oprettet kvalitetsordre, der refererer til en indkøbsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-236">Karantæneordre</span><span class="sxs-lookup"><span data-stu-id="3ecc3-236">Quarantine order</span></span></td>
<td><span data-ttu-id="3ecc3-237">Før eller efter karantæneordren rapporteres som færdigmeldt eller afsluttet</span><span class="sxs-lookup"><span data-stu-id="3ecc3-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="3ecc3-238">Kvalitetsordrer, der kræver destruktive prøvninger kan ikke oprettes.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="3ecc3-239">Det antages, at funktionerne i karantæneordren håndterer bortskaffelsen af det materiale, der destrueres.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="3ecc3-240">Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller kreditor eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="3ecc3-241">En manuelt oprettet kvalitetsordre, der refererer til en karantæneordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-242">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="3ecc3-242">Sales order</span></span></td>
<td><span data-ttu-id="3ecc3-243">Før en planlagt plukproces eller opdatering af følgesedlen for de varer, der skal leveres</span><span class="sxs-lookup"><span data-stu-id="3ecc3-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="3ecc3-244">På alle trin</span><span class="sxs-lookup"><span data-stu-id="3ecc3-244">At any step</span></span></td>
<td><span data-ttu-id="3ecc3-245">Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller debitor eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="3ecc3-246">En manuelt oprettet kvalitetsordre, der refererer til en salgsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-247">Produktionsordre</span><span class="sxs-lookup"><span data-stu-id="3ecc3-247">Production order</span></span></td>
<td><span data-ttu-id="3ecc3-248">Før eller efter det færdigmeldte antal for produktionsordren er rapporteret</span><span class="sxs-lookup"><span data-stu-id="3ecc3-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="3ecc3-249">Efter det færdigmeldte antal for produktionsordren er rapporteret</span><span class="sxs-lookup"><span data-stu-id="3ecc3-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="3ecc3-250">Behovet for en kvalitetsordre kan afhænge af en bestemt lokation eller vare eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="3ecc3-251">En manuelt oprettet kvalitetsordre, der refererer til en produktionsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-252">Produktionsordre, der har en ruteoperation</span><span class="sxs-lookup"><span data-stu-id="3ecc3-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="3ecc3-253">Før eller efter rapporten er færdigmeldt for en operation</span><span class="sxs-lookup"><span data-stu-id="3ecc3-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="3ecc3-254">Efter færdigrapportering af produktionen for den sidste operation</span><span class="sxs-lookup"><span data-stu-id="3ecc3-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="3ecc3-255">Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller operationsressource eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="3ecc3-256">En manuelt oprettet kvalitetsordre, der refererer til en ruteoperation, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-257">Lager</span><span class="sxs-lookup"><span data-stu-id="3ecc3-257">Inventory</span></span></td>
<td><span data-ttu-id="3ecc3-258">En kvalitetsordre kan ikke genereres automatisk for en transaktion i en lagerkladde eller flytteordretransaktioner.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="3ecc3-259">En kvalitetsordre skal oprettes manuelt for en vares lagerantal.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="3ecc3-260">Fysisk disponibel lagerbeholdning er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="3ecc3-261">Eksempler på automatisk generering af kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="3ecc3-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="3ecc3-262">Køb</span><span class="sxs-lookup"><span data-stu-id="3ecc3-262">Purchasing</span></span>

<span data-ttu-id="3ecc3-263">Hvis du i forbindelse med indkøb angiver feltet **Hændelsestype** til **Produktkvittering** og feltet **Udførelse** til **Efter** på siden **Kvalitetstilknytninger**, får du følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="3ecc3-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="3ecc3-264">Hvis indstillingen **Pr. opdateret antal** er angivet til **Ja**, genereres der en kvalitetsordre for hver kvittering i forhold til indkøbsordren baseret på det modtagne antal og indstillinger i stikprøven af vare.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="3ecc3-265">Hver gang der modtages et antal på indkøbsordren, oprettes der nye kvalitetsordrer ud fra det nye antal, der er modtaget.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="3ecc3-266">Hvis indstillingen **Pr. opdateret antal** er angivet til **Nej**, genereres der en kvalitetsordre for den første kvittering i forhold til indkøbsordren baseret på det modtagne antal.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="3ecc3-267">Derudover oprettes en eller flere kvalitetsordrer ud fra det resterende antal afhængigt af sporingsdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="3ecc3-268">Kvalitetsordrer genereres ikke for efterfølgende kvitteringer i forhold til indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="3ecc3-269">Kvalitetsspecifikation</span><span class="sxs-lookup"><span data-stu-id="3ecc3-269">Quality specification</span></span></th>
<th><span data-ttu-id="3ecc3-270">Pr. opdateret antal</span><span class="sxs-lookup"><span data-stu-id="3ecc3-270">Per updated quantity</span></span></th>
<th><span data-ttu-id="3ecc3-271">Pr. sporingsdimension</span><span class="sxs-lookup"><span data-stu-id="3ecc3-271">Per tracking dimension</span></span></th>
<th><span data-ttu-id="3ecc3-272">Resultat</span><span class="sxs-lookup"><span data-stu-id="3ecc3-272">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-273">Procent: 10 %</span><span class="sxs-lookup"><span data-stu-id="3ecc3-273">Percentage: 10%</span></span></td>
<td><span data-ttu-id="3ecc3-274">Ja</span><span class="sxs-lookup"><span data-stu-id="3ecc3-274">Yes</span></span></td>
<td>
<p><span data-ttu-id="3ecc3-275">Batchnummer: Nej</span><span class="sxs-lookup"><span data-stu-id="3ecc3-275">Batch number: No</span></span></p>
<p><span data-ttu-id="3ecc3-276">Serienummer: Nej</span><span class="sxs-lookup"><span data-stu-id="3ecc3-276">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="3ecc3-277">Ordreantal: 100</span><span class="sxs-lookup"><span data-stu-id="3ecc3-277">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="3ecc3-278">Færdigmelding for 30</span><span class="sxs-lookup"><span data-stu-id="3ecc3-278">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="3ecc3-279">Kvalitetsordrenr. 1 for 3 (10 % af 30)</span><span class="sxs-lookup"><span data-stu-id="3ecc3-279">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3ecc3-280">Færdigmelding for 70</span><span class="sxs-lookup"><span data-stu-id="3ecc3-280">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="3ecc3-281">Kvalitetsordrenr. 2 for 7 (10 % af det resterende ordreantal, hvilket er lig med 70 i dette tilfælde)</span><span class="sxs-lookup"><span data-stu-id="3ecc3-281">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-282">Fast antal: 1</span><span class="sxs-lookup"><span data-stu-id="3ecc3-282">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="3ecc3-283">Nr.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-283">No</span></span></td>
<td>
<p><span data-ttu-id="3ecc3-284">Batchnummer: Nej</span><span class="sxs-lookup"><span data-stu-id="3ecc3-284">Batch number: No</span></span></p>
<p><span data-ttu-id="3ecc3-285">Serienummer: Nej</span><span class="sxs-lookup"><span data-stu-id="3ecc3-285">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="3ecc3-286">Ordreantal: 100</span><span class="sxs-lookup"><span data-stu-id="3ecc3-286">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="3ecc3-287">Færdigmelding for 30</span><span class="sxs-lookup"><span data-stu-id="3ecc3-287">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="3ecc3-288">Kvalitetsordrenr. 1 oprettes for 1 (for det første færdigmeldte antal, der har en fast værdi af 1).</span><span class="sxs-lookup"><span data-stu-id="3ecc3-288">Quality order #1 is created for 1 (for the first reported-as-finished quantity, which has a fixed value of 1).</span></span></li>
<li><span data-ttu-id="3ecc3-289">Der oprettes ikke flere kvalitetsordrer i forhold til det resterende antal.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-289">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3ecc3-290">Færdigmelding for 10</span><span class="sxs-lookup"><span data-stu-id="3ecc3-290">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="3ecc3-291">Der oprettes ingen kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-291">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3ecc3-292">Færdigmelding for 60</span><span class="sxs-lookup"><span data-stu-id="3ecc3-292">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="3ecc3-293">Der oprettes ingen kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-293">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-294">Fast antal: 1</span><span class="sxs-lookup"><span data-stu-id="3ecc3-294">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="3ecc3-295">Ja</span><span class="sxs-lookup"><span data-stu-id="3ecc3-295">Yes</span></span></td>
<td>
<p><span data-ttu-id="3ecc3-296">Batchnummer: Ja</span><span class="sxs-lookup"><span data-stu-id="3ecc3-296">Batch number: Yes</span></span></p>
<p><span data-ttu-id="3ecc3-297">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="3ecc3-297">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="3ecc3-298">Ordreantal: 10</span><span class="sxs-lookup"><span data-stu-id="3ecc3-298">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="3ecc3-299">Færdigmelding for 3</span><span class="sxs-lookup"><span data-stu-id="3ecc3-299">Report as finished for 3</span></span>
<ul>
<li><span data-ttu-id="3ecc3-300">Kvalitetsordrenr. 1 for 1 af batchnr. b1, serienr. s1</span><span class="sxs-lookup"><span data-stu-id="3ecc3-300">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="3ecc3-301">Kvalitetsordrenr. 2 for 1 af batchnr. b2, serienr. s2</span><span class="sxs-lookup"><span data-stu-id="3ecc3-301">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="3ecc3-302">Kvalitetsordrenr. 3 for 1 af batchnr. b3, serienr. s3</span><span class="sxs-lookup"><span data-stu-id="3ecc3-302">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3ecc3-303">Færdigmelding for 2</span><span class="sxs-lookup"><span data-stu-id="3ecc3-303">Report as finished for 2</span></span>
<ul>
<li><span data-ttu-id="3ecc3-304">Kvalitetsordrenr. 4 for 1 af batchnr. b4, serienr. s4</span><span class="sxs-lookup"><span data-stu-id="3ecc3-304">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="3ecc3-305">Kvalitetsordrenr. 5 for 1 af batchnr. b5, serienr. s5</span><span class="sxs-lookup"><span data-stu-id="3ecc3-305">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="3ecc3-306"><strong>Bemærk:</strong> Batchen kan genbruges.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-306"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-307">Fast antal: 2</span><span class="sxs-lookup"><span data-stu-id="3ecc3-307">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="3ecc3-308">Nr.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-308">No</span></span></td>
<td>
<p><span data-ttu-id="3ecc3-309">Batchnummer: Ja</span><span class="sxs-lookup"><span data-stu-id="3ecc3-309">Batch number: Yes</span></span></p>
<p><span data-ttu-id="3ecc3-310">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="3ecc3-310">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="3ecc3-311">Ordreantal: 10</span><span class="sxs-lookup"><span data-stu-id="3ecc3-311">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="3ecc3-312">Færdigmelding for 4</span><span class="sxs-lookup"><span data-stu-id="3ecc3-312">Report as finished for 4</span></span>
<ul>
<li><span data-ttu-id="3ecc3-313">Kvalitetsordrenr. 1 for 1 af batchnr. b1, serienr. s1.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-313">Quality order #1 for 1 of batch #b1, serial #s1.</span></span></li>
<li><span data-ttu-id="3ecc3-314">Kvalitetsordrenr. 2 for 1 af batchnr. b2, serienr. s2.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-314">Quality order #2 for 1 of batch #b2, serial #s2.</span></span></li>
<li><span data-ttu-id="3ecc3-315">Kvalitetsordrenr. 3 for 1 af batchnr. b3, serienr. s3.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-315">Quality order #3 for 1 of batch #b3, serial #s3.</span></span></li>
<li><span data-ttu-id="3ecc3-316">Kvalitetsordrenr. 4 for 1 af batchnr. b4, serienr. s4.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-316">Quality order #4 for 1 of batch #b4, serial #s4.</span></span></li>
<li><span data-ttu-id="3ecc3-317">Der oprettes ikke flere kvalitetsordrer i forhold til det resterende antal.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-317">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3ecc3-318">Færdigmelding for 6</span><span class="sxs-lookup"><span data-stu-id="3ecc3-318">Report as finished for 6</span></span>
<ul>
<li><span data-ttu-id="3ecc3-319">Der oprettes ingen kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-319">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="production"></a><span data-ttu-id="3ecc3-320">Produktion</span><span class="sxs-lookup"><span data-stu-id="3ecc3-320">Production</span></span>

<span data-ttu-id="3ecc3-321">Hvis du i forbindelse med produktion angiver feltet **Hændelsestype** til **Færdigmelding** og feltet **Udførelse** til **Efter** på siden **Kvalitetstilknytninger**, får du følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="3ecc3-321">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="3ecc3-322">Hvis indstillingen **Pr. opdateret antal** er angivet til **Ja**, genereres der en kvalitetsordre baseret på hvert færdige antal og indstillinger i stikprøven af vare.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-322">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="3ecc3-323">Hver gang et antal færdigmeldes på indkøbsordren, oprettes der nye kvalitetsordrer ud fra det nye antal, der er færdigmeldt.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-323">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="3ecc3-324">Denne genereringslogik stemmer overens med indkøb.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-324">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="3ecc3-325">Hvis indstillingen **Pr. opdateret antal** er angivet til **Nej**, genereres der en kvalitetsordre, første gang et antal færdigmeldes, baseret på det færdige antal.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-325">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="3ecc3-326">Derudover oprettes en eller flere kvalitetsordrer ud fra det resterende antal afhængigt af sporingsdimensionerne for stikprøven af varen.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-326">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="3ecc3-327">Kvalitetsordrer genereres ikke for efterfølgende færdige antal.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-327">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="3ecc3-328">Kvalitetsspecifikation</span><span class="sxs-lookup"><span data-stu-id="3ecc3-328">Quality specification</span></span></th>
<th><span data-ttu-id="3ecc3-329">Pr. opdateret antal</span><span class="sxs-lookup"><span data-stu-id="3ecc3-329">Per updated quantity</span></span></th>
<th><span data-ttu-id="3ecc3-330">Pr. sporingsdimension</span><span class="sxs-lookup"><span data-stu-id="3ecc3-330">Per tracking dimension</span></span></th>
<th><span data-ttu-id="3ecc3-331">Resultat</span><span class="sxs-lookup"><span data-stu-id="3ecc3-331">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-332">Procent: 10 %</span><span class="sxs-lookup"><span data-stu-id="3ecc3-332">Percentage: 10%</span></span></td>
<td><span data-ttu-id="3ecc3-333">Ja</span><span class="sxs-lookup"><span data-stu-id="3ecc3-333">Yes</span></span></td>
<td>
<p><span data-ttu-id="3ecc3-334">Batchnummer: Nej</span><span class="sxs-lookup"><span data-stu-id="3ecc3-334">Batch number: No</span></span></p>
<p><span data-ttu-id="3ecc3-335">Serienummer: Nej</span><span class="sxs-lookup"><span data-stu-id="3ecc3-335">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="3ecc3-336">Ordreantal: 100</span><span class="sxs-lookup"><span data-stu-id="3ecc3-336">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="3ecc3-337">Færdigmelding for 30</span><span class="sxs-lookup"><span data-stu-id="3ecc3-337">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="3ecc3-338">Kvalitetsordrenr. 1 for 3 (10 % af 30)</span><span class="sxs-lookup"><span data-stu-id="3ecc3-338">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3ecc3-339">Færdigmelding for 70</span><span class="sxs-lookup"><span data-stu-id="3ecc3-339">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="3ecc3-340">Kvalitetsordrenr. 2 for 7 (10 % af det resterende ordreantal, hvilket er lig med 70 i dette tilfælde)</span><span class="sxs-lookup"><span data-stu-id="3ecc3-340">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-341">Fast antal: 1</span><span class="sxs-lookup"><span data-stu-id="3ecc3-341">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="3ecc3-342">Nr.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-342">No</span></span></td>
<td>
<p><span data-ttu-id="3ecc3-343">Batchnummer: Nej</span><span class="sxs-lookup"><span data-stu-id="3ecc3-343">Batch number: No</span></span></p>
<p><span data-ttu-id="3ecc3-344">Serienummer: Nej</span><span class="sxs-lookup"><span data-stu-id="3ecc3-344">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="3ecc3-345">Ordreantal: 100</span><span class="sxs-lookup"><span data-stu-id="3ecc3-345">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="3ecc3-346">Færdigmelding for 30</span><span class="sxs-lookup"><span data-stu-id="3ecc3-346">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="3ecc3-347">Kvalitetsordrenr. 1 for 1 (for det første færdigmeldte antal, der har en fast værdi af 1)</span><span class="sxs-lookup"><span data-stu-id="3ecc3-347">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="3ecc3-348">Kvalitetsordrenr. 2 for 1 (for det resterende antal, der stadig har en fast værdi af 1)</span><span class="sxs-lookup"><span data-stu-id="3ecc3-348">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3ecc3-349">Færdigmelding for 10</span><span class="sxs-lookup"><span data-stu-id="3ecc3-349">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="3ecc3-350">Der oprettes ingen kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-350">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3ecc3-351">Færdigmelding for 60</span><span class="sxs-lookup"><span data-stu-id="3ecc3-351">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="3ecc3-352">Der oprettes ingen kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-352">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-353">Fast antal: 1</span><span class="sxs-lookup"><span data-stu-id="3ecc3-353">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="3ecc3-354">Ja</span><span class="sxs-lookup"><span data-stu-id="3ecc3-354">Yes</span></span></td>
<td>
<p><span data-ttu-id="3ecc3-355">Batchnummer: Ja</span><span class="sxs-lookup"><span data-stu-id="3ecc3-355">Batch number: Yes</span></span></p>
<p><span data-ttu-id="3ecc3-356">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="3ecc3-356">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="3ecc3-357">Ordreantal: 10</span><span class="sxs-lookup"><span data-stu-id="3ecc3-357">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="3ecc3-358">Færdigmeld for 3: 1 for nr. b1, nr. s1. 1 for nr. b2, nr. s2 og 1 for nr. b3, nr. s3</span><span class="sxs-lookup"><span data-stu-id="3ecc3-358">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="3ecc3-359">Kvalitetsordrenr. 1 for 1 af batchnr. b1, serienr. s1</span><span class="sxs-lookup"><span data-stu-id="3ecc3-359">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="3ecc3-360">Kvalitetsordrenr. 2 for 1 af batchnr. b2, serienr. s2</span><span class="sxs-lookup"><span data-stu-id="3ecc3-360">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="3ecc3-361">Kvalitetsordrenr. 3 for 1 af batchnr. b3, serienr. s3</span><span class="sxs-lookup"><span data-stu-id="3ecc3-361">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3ecc3-362">Færdigmeld for 2: 1 for nr. b4, nr. s4. og 1 for nr. b5, nr. s5</span><span class="sxs-lookup"><span data-stu-id="3ecc3-362">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="3ecc3-363">Kvalitetsordrenr. 4 for 1 af batchnr. b4, serienr. s4</span><span class="sxs-lookup"><span data-stu-id="3ecc3-363">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="3ecc3-364">Kvalitetsordrenr. 5 for 1 af batchnr. b5, serienr. s5</span><span class="sxs-lookup"><span data-stu-id="3ecc3-364">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="3ecc3-365"><strong>Bemærk:</strong> Batchen kan genbruges.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-365"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="3ecc3-366">Fast antal: 2</span><span class="sxs-lookup"><span data-stu-id="3ecc3-366">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="3ecc3-367">Nr.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-367">No</span></span></td>
<td>
<p><span data-ttu-id="3ecc3-368">Batchnummer: Ja</span><span class="sxs-lookup"><span data-stu-id="3ecc3-368">Batch number: Yes</span></span></p>
<p><span data-ttu-id="3ecc3-369">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="3ecc3-369">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="3ecc3-370">Ordreantal: 10</span><span class="sxs-lookup"><span data-stu-id="3ecc3-370">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="3ecc3-371">Færdigmeld for 4: 1 for nr. b1, nr. s1. 1 for nr. b2, nr. s2, 1 for nr. b3, nr. s3 og 1 for nr. b4, nr. s4</span><span class="sxs-lookup"><span data-stu-id="3ecc3-371">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="3ecc3-372">Kvalitetsordrenr. 1 for 1 af batchnr. b1, serienr. s1</span><span class="sxs-lookup"><span data-stu-id="3ecc3-372">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="3ecc3-373">Kvalitetsordrenr. 2 for 1 af batchnr. b2, serienr. s2</span><span class="sxs-lookup"><span data-stu-id="3ecc3-373">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="3ecc3-374">Kvalitetsordrenr. 3 for 1 af batchnr. b3, serienr. s3</span><span class="sxs-lookup"><span data-stu-id="3ecc3-374">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="3ecc3-375">Kvalitetsordrenr. 4 for 1 af batchnr. b4, serienr. s4</span><span class="sxs-lookup"><span data-stu-id="3ecc3-375">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="3ecc3-376">Kvalitetsordre nr. 5 for 2, uden en reference til et batch og et serienummer</span><span class="sxs-lookup"><span data-stu-id="3ecc3-376">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3ecc3-377">Færdigmeld for 6: 1 for nr. b5, nr. s5. 1 for nr. b6, nr. s6. 1 for nr. b7, nr. s7. 1 for nr. b8, nr. s8. 1 for nr. b9, nr. s9 og 1 for nr. b10, nr. s10</span><span class="sxs-lookup"><span data-stu-id="3ecc3-377">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="3ecc3-378">Der oprettes ingen kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-378">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="3ecc3-379">Kvalitetsstyringssider</span><span class="sxs-lookup"><span data-stu-id="3ecc3-379">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ecc3-380">Side</span><span class="sxs-lookup"><span data-stu-id="3ecc3-380">Page</span></span></th>
<th><span data-ttu-id="3ecc3-381">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="3ecc3-381">Description</span></span></th>
<th><span data-ttu-id="3ecc3-382">Eksempel</span><span class="sxs-lookup"><span data-stu-id="3ecc3-382">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ecc3-383">Kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="3ecc3-383">Quality associations</span></span></td>
<td><span data-ttu-id="3ecc3-384">Se de tidligere afsnit i denne artikel.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-384">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="3ecc3-385">En kvalitetstilknytning angiver alle følgende oplysninger for en kvalitetsordre, der oprettes:</span><span class="sxs-lookup"><span data-stu-id="3ecc3-385">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="3ecc3-386">Posteringshændelsen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-386">The transaction event</span></span></li>
<li><span data-ttu-id="3ecc3-387">Det sæt test, der skal udføres på varerne</span><span class="sxs-lookup"><span data-stu-id="3ecc3-387">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="3ecc3-388">Det acceptable kvalitetsniveau (AQL)</span><span class="sxs-lookup"><span data-stu-id="3ecc3-388">The AQL</span></span></li>
<li><span data-ttu-id="3ecc3-389">Prøveplanen</span><span class="sxs-lookup"><span data-stu-id="3ecc3-389">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="3ecc3-390">Du skal definere en kvalitetstilknytning for hver afvigelse i en forretningsproces, der kræver automatisk generering af kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-390">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="3ecc3-391">For eksempel kan der oprettes en kvalitetsordre i forretningsprocesserne for indkøbsordrer, karantæneordrer, salgsordrer og produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-391">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ecc3-392">Test</span><span class="sxs-lookup"><span data-stu-id="3ecc3-392">Tests</span></span></td>
<td><span data-ttu-id="3ecc3-393">Du kan bruge denne side til at definere og få vist de individuelle test, der bestemmer, om produkterne opfylder kvalitetsspecifikationerne.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-393">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="3ecc3-394">Du kan tildele en eller flere individuelle test til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-394">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="3ecc3-395">Når du gør det, skal du også angive testspecifikke oplysninger, f.eks. de acceptable måleværdier.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-395">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="3ecc3-396">Måleværdier bruges til kvantitative test, og testvariabler bruges til kvalitative test.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-396">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="3ecc3-397">En kvantitativ test har testtypen <strong>Heltal</strong> eller <strong>Del</strong> og har også en angivet måleenhed.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-397">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="3ecc3-398">Kvalitetsspecifikationer og testresultater er udtrykt som tal.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-398">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="3ecc3-399">En kvalitativ test har testtypen <strong>Indstilling</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-399">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="3ecc3-400">Kvalitative test forudsætter flere oplysninger om den testvariabel, der måles, og de faste indstillinger.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-400">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="3ecc3-401">Kvalitetsspecifikationer og testresultater er udtrykt i overensstemmelse med et udfald.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-401">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="3ecc3-402">Et produktionsfirma udfører to test af købt materiale: en kvantitativ test for materialets kvalitet og en kvalitetstest for skader på emballagen.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-402">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="3ecc3-403">Firmaet definerer flere oplysninger om den kvalitative test for at identificere testvariablen (beskadiget emballage) og udfaldet.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-403">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="3ecc3-404">Firmaet bruger siden <strong>Testgrupper</strong> til at tildele de to test til en testgruppe og til at angive de testspecifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-404">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="3ecc3-405">Testgruppen tildeles til en kvalitetsordre, så firmaet kan rapportere testresultaterne for de to test.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-405">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ecc3-406">Testgrupper</span><span class="sxs-lookup"><span data-stu-id="3ecc3-406">Test groups</span></span></td>
<td><span data-ttu-id="3ecc3-407">Brug denne side til at konfigurere, redigere og få vist testgrupper og individuelle test, der er tildelt til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-407">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="3ecc3-408">I den øverste rude vises testgrupper, og i den nederste gruppe vises de test, der er knyttet til en valgt testgruppe.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-408">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="3ecc3-409">Du kan tildele flere politikker til en testgruppe, f.eks. en prøveplan, et acceptabelt kvalitetsniveau (AQL) og kravet om destruktiv test.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-409">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="3ecc3-410">Når du knytter en individuel test til en testgruppe, definerer du flere oplysninger, f.eks. rækkefølge, dokumenter og gyldighedsdatoer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-410">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="3ecc3-411">For kvantitative test skal de oplysninger, du angiver, også omfatte acceptable målingsværdier.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-411">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="3ecc3-412">For kvalitative test skal oplysningerne også omfatte testvariablen og standardudfaldet.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-412">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="3ecc3-413">Den testgruppe, der tildeles til en kvalitetsordre, definerer det testsæt, der skal som standard skal udføres på den angivne vare.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-413">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="3ecc3-414">Du kan dog tilføje, slette eller ændre test i kvalitetsordren.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-414">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="3ecc3-415">Testresultaterne rapporteres for hver test i en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-415">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="3ecc3-416">En produktionsvirksomhed definerer en testgruppe for hver afvigelse fra firmaets retningslinjer for kvalitet.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-416">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="3ecc3-417">De forskellige testgrupper reflekterer forskelle i prøveplaner, hvilke testsæt der skal udføres sammen, det acceptable kvalitetsniveau og andre faktorer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-417">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="3ecc3-418">For kvantitative test er der også forskelle i de acceptable måleværdier.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-418">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="3ecc3-419">Virksomheden sikrer sig, at retningslinjerne for kvalitet følges, ved at tildele en testgruppe til hver enkelt regel for automatisk oprettelse af kvalitetsordrer på siden <strong>Kvalitetstilknytning</strong> og tildeler også en testgruppe til kvalitetsordrer, der oprettes manuelt.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-419">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ecc3-420">Varekvalitetsgrupper</span><span class="sxs-lookup"><span data-stu-id="3ecc3-420">Item quality groups</span></span></td>
<td><span data-ttu-id="3ecc3-421">Du kan bruge denne side til at konfigurere, redigere og få vist de varer, der er tildelt en kvalitetsgruppe, eller de kvalitetsgrupper, der er tildelt en vare.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-421">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="3ecc3-422">En kvalitetsgruppe repræsenterer almindelige testkrav til varer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-422">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="3ecc3-423">Når du har defineret testkravene på siden <strong>Testgrupper</strong>, kan du definere reglerne for automatisk generering af kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-423">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="3ecc3-424">For at forenkle processen skal du undlade at definere regler for de enkelte varer.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-424">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="3ecc3-425">I stedet skal du angive regler for en kvalitetsgruppe ved hjælp af siden <strong>Kvalitetstilknytninger</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-425">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="3ecc3-426">Du kan også bruge siden <strong>Varekvalitetsgrupper</strong> for en valgt kvalitetsgruppe for at tildele relevante varer til den pågældende gruppe.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-426">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="3ecc3-427">Du kan også bruge siden <strong>Varekvalitetsgrupper</strong> for en valgt kvalitetsgruppe for en valgt vare for at tildele relevante kvalitetsgrupper til den pågældende vare.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-427">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="3ecc3-428">En produktionsvirksomhed indkøber forskellige råvarer, der har samme testkrav til indgående inspektion.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-428">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="3ecc3-429">Virksomheden definerer en kvalitetsgruppe og tildeler derefter kvalitetsgruppen de varenumre, der er knyttet gruppen.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-429">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="3ecc3-430">Senere indkøber virksomheden en ny type råvarer med de samme testkrav.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-430">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="3ecc3-431">I stedet for at konfigurere nye testkrav til de nye råvarer føjer virksomheden varenummeret på de nye råvarer til den eksisterende kvalitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-431">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="3ecc3-432">Den samme produktionsvirksomhed producerer desuden varer med de samme produktionstestkrav og leverer varer med de samme krav til test før forsendelse.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-432">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="3ecc3-433">Virksomheden definerer yderligere to kvalitetsgrupper og tildeler derefter hver gruppe de relevante varenumre.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-433">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ecc3-434">Testvariabler</span><span class="sxs-lookup"><span data-stu-id="3ecc3-434">Test variables</span></span></td>
<td><span data-ttu-id="3ecc3-435">Brug denne side til at angive og få vist variabler, der er tilknyttet en kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-435">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="3ecc3-436">Du kan angive faste udfald, der repræsenterer mulighederne for hver variabel.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-436">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="3ecc3-437">Du kan definere test på siden <strong>Test</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-437">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="3ecc3-438">Ved kvalitative test skal du angive testtypen <strong>Indstilling</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-438">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="3ecc3-439">Brug siden <strong>Testgrupper</strong> til at tildele en testvariabel til en individuel test.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-439">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="3ecc3-440">En produktionsvirksomhed, der fremstiller småkager, anvender en inspektionstest for det færdige produkt.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-440">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="3ecc3-441">Denne inspektionstest har adskillige variabler.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-441">This inspection test has several variables.</span></span> <span data-ttu-id="3ecc3-442">En af variablerne er smag, og de mulige udfald for denne variabel er god og dårlig.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-442">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="3ecc3-443">Farve er en anden variabel, og de mulige udfald er mørk, for lys og korrekt.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-443">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ecc3-444">Udfald af testvariabel</span><span class="sxs-lookup"><span data-stu-id="3ecc3-444">Test variable outcomes</span></span></td>
<td><span data-ttu-id="3ecc3-445">Brug denne side til at konfigurere, redigere og få vist de mulige testresultater for en testvariabel, der er knyttet til en kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-445">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="3ecc3-446">For hvert udfald angiver du status <strong>Bestået</strong> eller <strong>Mislykket</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-446">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="3ecc3-447">Du skal definere en variabel og dens udfald for hver kvalitative test, der er defineret på siden <strong>Test</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-447">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="3ecc3-448">(For kvalitative test er testtypen indstillet til <strong>Indstilling</strong> på siden <strong>Test</strong>). Brug siden <strong>Testgrupper</strong> til at tildele en testvariabel og standardudfaldet til en individuel kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-448">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="3ecc3-449">En produktionsvirksomhed, der fremstiller småkager, anvender en inspektionstest for det færdige produkt.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-449">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="3ecc3-450">Denne inspektionstest har adskillige variabler.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-450">This inspection test has of several variables.</span></span> <span data-ttu-id="3ecc3-451">En af variablerne er smag, og de mulige udfald for denne variabel er god og dårlig.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-451">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="3ecc3-452">Farve er en anden variabel, og de mulige udfald er mørk, for lys og korrekt.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-452">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="3ecc3-453">Hvert udfald får tildelt status <strong>Bestået</strong> eller <strong>Mislykket</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-453">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="3ecc3-454">Under inspektionstesten til hver variabel, rapporterer den person, der foretager inspektionen, testresultatet ved at vælge et af udfaldene.</span><span class="sxs-lookup"><span data-stu-id="3ecc3-454">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="3ecc3-455">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3ecc3-455">Additional resources</span></span>
--------

[<span data-ttu-id="3ecc3-456">Processer for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="3ecc3-456">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="3ecc3-457">Aktivering af uoverensstemmelsesstyring</span><span class="sxs-lookup"><span data-stu-id="3ecc3-457">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)
