---
title: Oversigt over kvalitetsstyring
description: "I denne artikel beskrives det, hvordan du kan bruge kvalitetsstyring i Microsoft Dynamics 365 for Finance and Operations til at forbedre produktkvaliteten i forsyningskæden."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 28ef47e2dc1f9c7e1c0b262c58332dcfea1f7495
ms.contentlocale: da-dk
ms.lasthandoff: 09/12/2017

---

# <a name="quality-management-overview"></a><span data-ttu-id="e7c0e-103">Oversigt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="e7c0e-103">Quality management overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e7c0e-104">I denne artikel beskrives det, hvordan du kan bruge kvalitetsstyring i Microsoft Dynamics 365 for Finance and Operations til at forbedre produktkvaliteten i forsyningskæden.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-104">This article describes how you can use quality management in Microsoft Dynamics 365 for Finance and Operations to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="e7c0e-105">Kvalitetsstyring kan hjælpe dig med at administrere behandlingstid, når du håndterer ikke-standardiserede produkter, uanset deres oprindelsessted.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="e7c0e-106">Fordi diagnosticeringstyper er knyttet til rapportering af korrektion, kan Microsoft Dynamics 365 for Finance and Operations planlægge opgaver for at løse problemer og forhindre dem i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-106">Because diagnostic types are linked to correction reporting, Microsoft Dynamics 365 for Finance and Operations can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="e7c0e-107">Ud over funktionalitet til administration af uoverensstemmelse omfatter kvalitetsstyring funktionalitet til sporing af problemer efter problemtype (også interne problemer) og til identificering af løsninger som kortsigtede eller langsigtede.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="e7c0e-108">Statistik over nøgletal (KPI'er) giver indsigt i historikken for tidligere problemer med uoverensstemmelse, og de løsninger, der blev anvendt til at rette dem.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="e7c0e-109">Du kan bruge historikdata til at gennemgå effektiviteten af tidligere kvalitetsmål og fastlægge passende foranstaltninger, der skal bruges i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="e7c0e-110">Når du opretter en kvalitetstilknytning, kan Finance and Operations oprette kvalitetsordrer til forskellige forretningsprocesser, hændelser og betingelser.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-110">When you set up a quality association, Finance and Operations can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="e7c0e-111">Kvalitetstilknytningen kan dække en bestemt vare, en bestemt gruppe varer eller alle varer.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="e7c0e-112">Eksempler på brug af kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="e7c0e-112">Examples of the use of quality management</span></span>
<span data-ttu-id="e7c0e-113">Kvalitetsstyring er fleksibel og kan gennemføres på forskellige måder for at opfylde kravene på bestemte niveauer i forsyningskædeoperationer.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="e7c0e-114">Eksemplerne nedenfor viser mulige anvendelser af disse funktioner:</span><span class="sxs-lookup"><span data-stu-id="e7c0e-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="e7c0e-115">Automatisk starte en proces for kvalitetskontrol baseret på foruddefinerede kriterier (ved lagerregistreringen af en indkøbsordre fra en bestemt leverandør).</span><span class="sxs-lookup"><span data-stu-id="e7c0e-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="e7c0e-116">Spærre lageret under kontrol for at forhindre, at ikke-godkendt lagerbeholdning bliver brugt (fuld spærring af indkøbsordreantal).</span><span class="sxs-lookup"><span data-stu-id="e7c0e-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="e7c0e-117">Bruge vareprøve som en del af en kvalitetstilknytning til at definere beløbet af det aktuelle fysiske lager, der skal undersøges.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="e7c0e-118">Vareprøver kan baseres på faste antal eller en procentdel.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="e7c0e-119">Opret kvalitetsordrer for delleverancer.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="e7c0e-120">For at oprette en kvalitetsordre, der er baseret på det antal, der fysisk er modtaget med en ordre, skal du markere afkrydsningsfeltet **Pr. opdateret antal** i formularen **Vareprøve**.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="e7c0e-121">Oprette testtyper, der omfatter minimum, maksimum og måltestværdier og udføre kvalitative kontra kvantitative test, der har foruddefinerede valideringsresultater.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="e7c0e-122">Angive et acceptabelt kvalitetsniveau (AQL) for at styre tolerancer for kvalitetsmål.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="e7c0e-123">Angive de ressourcer, som en inspektionshandling kræver, f.eks. et testområde og testinstrumenter.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="e7c0e-124">Arbejde med kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="e7c0e-124">Working with quality associations</span></span>
<span data-ttu-id="e7c0e-125">Den forretningsproces, der bruger en kvalitetstilknytning, kan knyttes til forskellige kildedokumenter, f.eks. indkøbsordrer, salgsordrer eller produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="e7c0e-126">De enkelte kvalitetstilknytningsposter definerer de test, det acceptable kvalitetsniveau (AQL) og den vareprøveplan, der gælder for de kvalitetsordrer, der oprettes.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="e7c0e-127">Du skal definere en kvalitetstilknytningspost for hver ændring i en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="e7c0e-128">Du kan f.eks. angive en kvalitetstilknytning, der genererer en kvalitetsordre, når en produktkvittering for en indkøbsordre opdateres.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="e7c0e-129">Afhængigt af opsætningen af udførelsesplanen kan selve den udløsende proces blive blokeret, mens der er en åben kvalitetsordre, eller de næste processer, som f.eks. fakturering, kan blive blokeret.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="e7c0e-130">**Bemærk!** Der kan være åbne kvalitetsordrer, men lagerantal blokeres automatisk fra at blive udstedet.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="e7c0e-131">Afhængigt af indstillingen **Fuld spærring** på siden **Stikprøver af varer** er antallet enten kvantiteten i kvalitetsordren eller kvantiteten i kildedokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="e7c0e-132">For en given forretningsproces identificerer kvalitetstilknytningsposten hændelsen og de betingelser, som der oprettes en kvalitetsordre for.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="e7c0e-133">Betingelserne kan være specifikke for et sted eller en juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="e7c0e-134">En kvalitetsordre, der involverer destruktive prøvninger, kan kun oprettes, når der findes en disponible lagerbeholdning for hændelsen.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="e7c0e-135">I følgende eksempel vises, hvordan en kvalitetstilknytningspost defineres for variationerne i de enkelte forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="e7c0e-136">Eksemplerne vises også i følgende tabel som en oversigt over de hændelser og betingelser, der er defineret af en kvalitetstilknytningspost.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="e7c0e-137">Referencetype</span><span class="sxs-lookup"><span data-stu-id="e7c0e-137">Reference type</span></span></th>
<th><span data-ttu-id="e7c0e-138">Hændelsestype</span><span class="sxs-lookup"><span data-stu-id="e7c0e-138">Event type</span></span></th>
<th><span data-ttu-id="e7c0e-139">Udførelse</span><span class="sxs-lookup"><span data-stu-id="e7c0e-139">Execution</span></span></th>
<th><span data-ttu-id="e7c0e-140">Hændelsesspærring</span><span class="sxs-lookup"><span data-stu-id="e7c0e-140">Event blocking</span></span></th>
<th><span data-ttu-id="e7c0e-141">Dokumentreference</span><span class="sxs-lookup"><span data-stu-id="e7c0e-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-142">Lager</span><span class="sxs-lookup"><span data-stu-id="e7c0e-142">Inventory</span></span></td>
<td><span data-ttu-id="e7c0e-143">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="e7c0e-143">Not applicable</span></span></td>
<td><span data-ttu-id="e7c0e-144">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="e7c0e-144">Not applicable</span></span></td>
<td><span data-ttu-id="e7c0e-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-145">None</span></span></td>
<td><span data-ttu-id="e7c0e-146">Alle</span><span class="sxs-lookup"><span data-stu-id="e7c0e-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="e7c0e-147">Salg</span><span class="sxs-lookup"><span data-stu-id="e7c0e-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="e7c0e-148">Plukproces er planlagt</span><span class="sxs-lookup"><span data-stu-id="e7c0e-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="e7c0e-149">Før</span><span class="sxs-lookup"><span data-stu-id="e7c0e-149">Before</span></span></td>
<td><span data-ttu-id="e7c0e-150">Ingen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="e7c0e-151">Bestemt id, gruppe eller kun alle</span><span class="sxs-lookup"><span data-stu-id="e7c0e-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-152">Plukproces</span><span class="sxs-lookup"><span data-stu-id="e7c0e-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-153">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="e7c0e-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-154">Faktura</span><span class="sxs-lookup"><span data-stu-id="e7c0e-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e7c0e-155">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="e7c0e-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="e7c0e-156">Før</span><span class="sxs-lookup"><span data-stu-id="e7c0e-156">Before</span></span></td>
<td><span data-ttu-id="e7c0e-157">Ingen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-158">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="e7c0e-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-159">Faktura</span><span class="sxs-lookup"><span data-stu-id="e7c0e-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="e7c0e-160">Indkøb</span><span class="sxs-lookup"><span data-stu-id="e7c0e-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="e7c0e-161">Tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="e7c0e-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="e7c0e-162">Før</span><span class="sxs-lookup"><span data-stu-id="e7c0e-162">Before</span></span></td>
<td><span data-ttu-id="e7c0e-163">Ingen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-164">Tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="e7c0e-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-165">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="e7c0e-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-166">Faktura</span><span class="sxs-lookup"><span data-stu-id="e7c0e-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e7c0e-167">Efter</span><span class="sxs-lookup"><span data-stu-id="e7c0e-167">After</span></span></td>
<td><span data-ttu-id="e7c0e-168">Ingen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-169">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="e7c0e-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-170">Faktura</span><span class="sxs-lookup"><span data-stu-id="e7c0e-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e7c0e-171">Registrering</span><span class="sxs-lookup"><span data-stu-id="e7c0e-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="e7c0e-172">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="e7c0e-172">Not applicable</span></span></td>
<td><span data-ttu-id="e7c0e-173">Ingen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-174">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="e7c0e-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-175">Faktura</span><span class="sxs-lookup"><span data-stu-id="e7c0e-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="e7c0e-176">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="e7c0e-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="e7c0e-177">Før</span><span class="sxs-lookup"><span data-stu-id="e7c0e-177">Before</span></span></td>
<td><span data-ttu-id="e7c0e-178">Ingen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-179">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="e7c0e-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-180">Faktura</span><span class="sxs-lookup"><span data-stu-id="e7c0e-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e7c0e-181">Efter</span><span class="sxs-lookup"><span data-stu-id="e7c0e-181">After</span></span></td>
<td><span data-ttu-id="e7c0e-182">Ingen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-183">Faktura</span><span class="sxs-lookup"><span data-stu-id="e7c0e-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="e7c0e-184">Produktion</span><span class="sxs-lookup"><span data-stu-id="e7c0e-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="e7c0e-185">Registrering</span><span class="sxs-lookup"><span data-stu-id="e7c0e-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="e7c0e-186">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="e7c0e-186">Not applicable</span></span></td>
<td><span data-ttu-id="e7c0e-187">Ingen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="e7c0e-188">Alle</span><span class="sxs-lookup"><span data-stu-id="e7c0e-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-189">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="e7c0e-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-190">Afslut</span><span class="sxs-lookup"><span data-stu-id="e7c0e-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="e7c0e-191">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="e7c0e-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="e7c0e-192">Før</span><span class="sxs-lookup"><span data-stu-id="e7c0e-192">Before</span></span></td>
<td><span data-ttu-id="e7c0e-193">Ingen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-194">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="e7c0e-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-195">Afslut</span><span class="sxs-lookup"><span data-stu-id="e7c0e-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e7c0e-196">Efter</span><span class="sxs-lookup"><span data-stu-id="e7c0e-196">After</span></span></td>
<td><span data-ttu-id="e7c0e-197">Ingen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-198">Afslut</span><span class="sxs-lookup"><span data-stu-id="e7c0e-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="e7c0e-199">Karantæne</span><span class="sxs-lookup"><span data-stu-id="e7c0e-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="e7c0e-200">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="e7c0e-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="e7c0e-201">Før</span><span class="sxs-lookup"><span data-stu-id="e7c0e-201">Before</span></span></td>
<td><span data-ttu-id="e7c0e-202">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="e7c0e-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-203">Afslut</span><span class="sxs-lookup"><span data-stu-id="e7c0e-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-204">Efter</span><span class="sxs-lookup"><span data-stu-id="e7c0e-204">After</span></span></td>
<td><span data-ttu-id="e7c0e-205">Afslut</span><span class="sxs-lookup"><span data-stu-id="e7c0e-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-206">Afslut</span><span class="sxs-lookup"><span data-stu-id="e7c0e-206">End</span></span></td>
<td><span data-ttu-id="e7c0e-207">Før</span><span class="sxs-lookup"><span data-stu-id="e7c0e-207">Before</span></span></td>
<td><span data-ttu-id="e7c0e-208">Afslut</span><span class="sxs-lookup"><span data-stu-id="e7c0e-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e7c0e-209">Ruteoperation</span><span class="sxs-lookup"><span data-stu-id="e7c0e-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="e7c0e-210">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="e7c0e-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="e7c0e-211">Før</span><span class="sxs-lookup"><span data-stu-id="e7c0e-211">Before</span></span></td>
<td><span data-ttu-id="e7c0e-212">Ingen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="e7c0e-213">Bestemt id, gruppe eller alle, og ressourcespecifik, gruppe eller alle</span><span class="sxs-lookup"><span data-stu-id="e7c0e-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-214">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="e7c0e-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-215">Efter</span><span class="sxs-lookup"><span data-stu-id="e7c0e-215">After</span></span></td>
<td><span data-ttu-id="e7c0e-216">Ingen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e7c0e-217">Produktion af samprodukter</span><span class="sxs-lookup"><span data-stu-id="e7c0e-217">Co-product production</span></span></td>
<td><span data-ttu-id="e7c0e-218">Registrering</span><span class="sxs-lookup"><span data-stu-id="e7c0e-218">Registration</span></span></td>
<td><span data-ttu-id="e7c0e-219">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="e7c0e-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e7c0e-220">Ingen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="e7c0e-221">Alle</span><span class="sxs-lookup"><span data-stu-id="e7c0e-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e7c0e-222">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="e7c0e-222">Report as finished</span></span></td>
<td><span data-ttu-id="e7c0e-223">Før</span><span class="sxs-lookup"><span data-stu-id="e7c0e-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-224">Efter</span><span class="sxs-lookup"><span data-stu-id="e7c0e-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7c0e-225">Tabellen nedenfor indeholder flere oplysninger om, hvordan kvalitetsordrer kan oprettes for bestemte typer processer.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="e7c0e-226">Procestype</span><span class="sxs-lookup"><span data-stu-id="e7c0e-226">Type of process</span></span></th>
<th><span data-ttu-id="e7c0e-227">Når kvalitetsordrer kan genereres automatisk</span><span class="sxs-lookup"><span data-stu-id="e7c0e-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="e7c0e-228">Når kvalitetsordrer kan genereres, hvis destruktiv prøvning er påkrævet</span><span class="sxs-lookup"><span data-stu-id="e7c0e-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="e7c0e-229">Betingelsesoplysninger</span><span class="sxs-lookup"><span data-stu-id="e7c0e-229">Condition information</span></span></th>
<th><span data-ttu-id="e7c0e-230">Manuel oprettelse af oplysninger</span><span class="sxs-lookup"><span data-stu-id="e7c0e-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-231">Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="e7c0e-231">Purchase order</span></span></td>
<td><span data-ttu-id="e7c0e-232">Før eller efter en tilgangsliste eller produktkvittering for det materiale, der er modtaget, bogføres</span><span class="sxs-lookup"><span data-stu-id="e7c0e-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="e7c0e-233">Efter produktkvitteringen for det materiale, der er modtaget, bogføres, da materialet skal være tilgængelig til destruktiv prøvning</span><span class="sxs-lookup"><span data-stu-id="e7c0e-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="e7c0e-234">Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller kreditor eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="e7c0e-235">En manuelt oprettet kvalitetsordre, der refererer til en indkøbsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-236">Karantæneordre</span><span class="sxs-lookup"><span data-stu-id="e7c0e-236">Quarantine order</span></span></td>
<td><span data-ttu-id="e7c0e-237">Før eller efter karantæneordren rapporteres som færdigmeldt eller afsluttet</span><span class="sxs-lookup"><span data-stu-id="e7c0e-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="e7c0e-238">Kvalitetsordrer, der kræver destruktive prøvninger kan ikke oprettes.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-238">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="e7c0e-239">Det antages, at funktionerne i karantæneordren håndterer bortskaffelsen af det materiale, der destrueres.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-239">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="e7c0e-240">Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller kreditor eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="e7c0e-241">En manuelt oprettet kvalitetsordre, der refererer til en karantæneordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-242">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="e7c0e-242">Sales order</span></span></td>
<td><span data-ttu-id="e7c0e-243">Før en planlagt plukproces eller opdatering af følgesedlen for de varer, der skal leveres</span><span class="sxs-lookup"><span data-stu-id="e7c0e-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="e7c0e-244">På alle trin</span><span class="sxs-lookup"><span data-stu-id="e7c0e-244">At any step</span></span></td>
<td><span data-ttu-id="e7c0e-245">Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller debitor eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="e7c0e-246">En manuelt oprettet kvalitetsordre, der refererer til en salgsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-247">Produktionsordre</span><span class="sxs-lookup"><span data-stu-id="e7c0e-247">Production order</span></span></td>
<td><span data-ttu-id="e7c0e-248">Før eller efter det færdigmeldte antal for produktionsordren er rapporteret</span><span class="sxs-lookup"><span data-stu-id="e7c0e-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="e7c0e-249">Efter det færdigmeldte antal for produktionsordren er rapporteret</span><span class="sxs-lookup"><span data-stu-id="e7c0e-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="e7c0e-250">Behovet for en kvalitetsordre kan afhænge af en bestemt lokation eller vare eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="e7c0e-251">En manuelt oprettet kvalitetsordre, der refererer til en produktionsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-252">Produktionsordre, der har en ruteoperation</span><span class="sxs-lookup"><span data-stu-id="e7c0e-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="e7c0e-253">Før eller efter rapporten er færdigmeldt for en operation</span><span class="sxs-lookup"><span data-stu-id="e7c0e-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="e7c0e-254">Efter færdigrapportering af produktionen for den sidste operation</span><span class="sxs-lookup"><span data-stu-id="e7c0e-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="e7c0e-255">Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller operationsressource eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="e7c0e-256">En manuelt oprettet kvalitetsordre, der refererer til en ruteoperation, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7c0e-257">Lager</span><span class="sxs-lookup"><span data-stu-id="e7c0e-257">Inventory</span></span></td>
<td><span data-ttu-id="e7c0e-258">En kvalitetsordre kan ikke genereres automatisk for en transaktion i en lagerkladde eller flytteordretransaktioner.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="e7c0e-259">En kvalitetsordre skal oprettes manuelt for en vares lagerantal.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-259">A quality order must be created manually for an item's inventory quantity.</span></span> <span data-ttu-id="e7c0e-260">Fysisk disponibel lagerbeholdning er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="e7c0e-261">Kvalitetsstyringssider</span><span class="sxs-lookup"><span data-stu-id="e7c0e-261">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7c0e-262">Side</span><span class="sxs-lookup"><span data-stu-id="e7c0e-262">Page</span></span></th>
<th><span data-ttu-id="e7c0e-263">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e7c0e-263">Description</span></span></th>
<th><span data-ttu-id="e7c0e-264">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e7c0e-264">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e7c0e-265">Kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="e7c0e-265">Quality associations</span></span></td>
<td><span data-ttu-id="e7c0e-266">Se de tidligere afsnit i denne artikel.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-266">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="e7c0e-267">En kvalitetstilknytning angiver alle følgende oplysninger for en kvalitetsordre, der oprettes:</span><span class="sxs-lookup"><span data-stu-id="e7c0e-267">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="e7c0e-268">Posteringshændelsen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-268">The transaction event</span></span></li>
<li><span data-ttu-id="e7c0e-269">Det sæt test, der skal udføres på varerne</span><span class="sxs-lookup"><span data-stu-id="e7c0e-269">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="e7c0e-270">Det acceptable kvalitetsniveau (AQL)</span><span class="sxs-lookup"><span data-stu-id="e7c0e-270">The AQL</span></span></li>
<li><span data-ttu-id="e7c0e-271">Prøveplanen</span><span class="sxs-lookup"><span data-stu-id="e7c0e-271">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="e7c0e-272">Du skal definere en kvalitetstilknytning for hver afvigelse i en forretningsproces, der kræver automatisk generering af kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-272">You must define a quality associationfor each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="e7c0e-273">For eksempel kan der oprettes en kvalitetsordre i forretningsprocesserne for indkøbsordrer, karantæneordrer, salgsordrer og produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-273">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7c0e-274">Test</span><span class="sxs-lookup"><span data-stu-id="e7c0e-274">Tests</span></span></td>
<td><span data-ttu-id="e7c0e-275">Du kan bruge denne side til at definere og få vist de individuelle test, der bestemmer, om produkterne opfylder kvalitetsspecifikationerne.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-275">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="e7c0e-276">Du kan tildele en eller flere individuelle test til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-276">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="e7c0e-277">Når du gør det, skal du også angive testspecifikke oplysninger, f.eks. de acceptable måleværdier.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-277">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="e7c0e-278">Måleværdier bruges til kvantitative test, og testvariabler bruges til kvalitative test.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-278">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="e7c0e-279">En kvantitativ test har testtypen <strong>Heltal</strong> eller <strong>Del</strong> og har også en angivet måleenhed.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-279">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="e7c0e-280">Kvalitetsspecifikationer og testresultater er udtrykt som tal.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-280">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="e7c0e-281">En kvalitativ test har testtypen <strong>Indstilling</strong>.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-281">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="e7c0e-282">Kvalitative test forudsætter flere oplysninger om den testvariabel, der måles, og de faste indstillinger.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-282">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="e7c0e-283">Kvalitetsspecifikationer og testresultater er udtrykt i overensstemmelse med et udfald.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-283">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="e7c0e-284">Et produktionsfirma udfører to test af købt materiale: en kvantitativ test for materialets kvalitet og en kvalitetstest for skader på emballagen.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-284">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="e7c0e-285">Firmaet definerer flere oplysninger om den kvalitative test for at identificere testvariablen (beskadiget emballage) og udfaldet.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-285">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="e7c0e-286">Firmaet bruger siden <strong>Testgrupper</strong> til at tildele de to test til en testgruppe og til at angive de testspecifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-286">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="e7c0e-287">Testgruppen tildeles til en kvalitetsordre, så firmaet kan rapportere testresultaterne for de to test.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-287">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7c0e-288">Testgrupper</span><span class="sxs-lookup"><span data-stu-id="e7c0e-288">Test groups</span></span></td>
<td><span data-ttu-id="e7c0e-289">Brug denne side til at konfigurere, redigere og få vist testgrupper og individuelle test, der er tildelt til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-289">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="e7c0e-290">I den øverste rude vises testgrupper, og i den nederste gruppe vises de test, der er knyttet til en valgt testgruppe.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-290">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="e7c0e-291">Du kan tildele flere politikker til en testgruppe, f.eks. en prøveplan, et acceptabelt kvalitetsniveau (AQL) og kravet om destruktiv test.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-291">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="e7c0e-292">Når du knytter en individuel test til en testgruppe, definerer du flere oplysninger, f.eks. rækkefølge, dokumenter og gyldighedsdatoer.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-292">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="e7c0e-293">For kvantitative test skal de oplysninger, du angiver, også omfatte acceptable målingsværdier.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-293">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="e7c0e-294">For kvalitative test skal oplysningerne også omfatte testvariablen og standardudfaldet.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-294">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="e7c0e-295">Den testgruppe, der tildeles til en kvalitetsordre, definerer det testsæt, der skal som standard skal udføres på den angivne vare.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-295">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="e7c0e-296">Du kan dog tilføje, slette eller ændre test i kvalitetsordren.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-296">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="e7c0e-297">Testresultaterne rapporteres for hver test i en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-297">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="e7c0e-298">En produktionsvirksomhed definerer en testgruppe for hver afvigelse fra firmaets retningslinjer for kvalitet.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-298">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="e7c0e-299">De forskellige testgrupper reflekterer forskelle i prøveplaner, hvilke testsæt der skal udføres sammen, det acceptable kvalitetsniveau og andre faktorer.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-299">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="e7c0e-300">For kvantitative test er der også forskelle i de acceptable måleværdier.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-300">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="e7c0e-301">Virksomheden sikrer sig, at retningslinjerne for kvalitet følges, ved at tildele en testgruppe til hver enkelt regel for automatisk oprettelse af kvalitetsordrer på siden <strong>Kvalitetstilknytning</strong> og tildeler også en testgruppe til kvalitetsordrer, der oprettes manuelt.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-301">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7c0e-302">Varekvalitetsgrupper</span><span class="sxs-lookup"><span data-stu-id="e7c0e-302">Item quality groups</span></span></td>
<td><span data-ttu-id="e7c0e-303">Du kan bruge denne side til at konfigurere, redigere og få vist de varer, der er tildelt en kvalitetsgruppe, eller de kvalitetsgrupper, der er tildelt en vare.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-303">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="e7c0e-304">En kvalitetsgruppe repræsenterer almindelige testkrav til varer.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-304">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="e7c0e-305">Når du har defineret testkravene på siden <strong>Testgrupper</strong>, kan du definere reglerne for automatisk generering af kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-305">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="e7c0e-306">For at forenkle processen skal du undlade at definere regler for de enkelte varer.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-306">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="e7c0e-307">I stedet skal du angive regler for en kvalitetsgruppe ved hjælp af siden <strong>Kvalitetstilknytninger</strong>.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-307">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="e7c0e-308">Du kan også bruge siden <strong>Varekvalitetsgrupper</strong> for en valgt kvalitetsgruppe for at tildele relevante varer til den pågældende gruppe.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-308">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="e7c0e-309">Du kan også bruge siden <strong>Varekvalitetsgrupper</strong> for en valgt kvalitetsgruppe for en valgt vare for at tildele relevante kvalitetsgrupper til den pågældende vare.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-309">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="e7c0e-310">En produktionsvirksomhed indkøber forskellige råvarer, der har samme testkrav til indgående inspektion.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-310">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="e7c0e-311">Virksomheden definerer en kvalitetsgruppe og tildeler derefter kvalitetsgruppen de varenumre, der er knyttet gruppen.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-311">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="e7c0e-312">Senere indkøber virksomheden en ny type råvarer med de samme testkrav.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-312">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="e7c0e-313">I stedet for at konfigurere nye testkrav til de nye råvarer føjer virksomheden varenummeret på de nye råvarer til den eksisterende kvalitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-313">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="e7c0e-314">Den samme produktionsvirksomhed producerer desuden varer med de samme produktionstestkrav og leverer varer med de samme krav til test før forsendelse.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-314">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="e7c0e-315">Virksomheden definerer yderligere to kvalitetsgrupper og tildeler derefter hver gruppe de relevante varenumre.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-315">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7c0e-316">Testvariabler</span><span class="sxs-lookup"><span data-stu-id="e7c0e-316">Test variables</span></span></td>
<td><span data-ttu-id="e7c0e-317">Brug denne side til at angive og få vist variabler, der er tilknyttet en kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-317">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="e7c0e-318">Du kan angive faste udfald, der repræsenterer mulighederne for hver variabel.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-318">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="e7c0e-319">Du kan definere test på siden <strong>Test</strong>.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-319">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="e7c0e-320">Ved kvalitative test skal du angive testtypen <strong>Indstilling</strong>.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-320">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="e7c0e-321">Brug siden <strong>Testgrupper</strong> til at tildele en testvariabel til en individuel test.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-321">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="e7c0e-322">En produktionsvirksomhed, der fremstiller småkager, anvender en inspektionstest for det færdige produkt.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-322">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="e7c0e-323">Denne inspektionstest har adskillige variabler.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-323">This inspection test has several variables.</span></span> <span data-ttu-id="e7c0e-324">En af variablerne er smag, og de mulige udfald for denne variabel er god og dårlig.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-324">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="e7c0e-325">Farve er en anden variabel, og de mulige udfald er mørk, for lys og korrekt.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-325">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7c0e-326">Udfald af testvariabel</span><span class="sxs-lookup"><span data-stu-id="e7c0e-326">Test variable outcomes</span></span></td>
<td><span data-ttu-id="e7c0e-327">Brug denne side til at konfigurere, redigere og få vist de mulige testresultater for en testvariabel, der er knyttet til en kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-327">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="e7c0e-328">For hvert udfald angiver du status <strong>Bestået</strong> eller <strong>Mislykket</strong>.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-328">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="e7c0e-329">Du skal definere en variabel og dens udfald for hver kvalitative test, der er defineret på siden <strong>Test</strong>.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-329">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="e7c0e-330">(For kvalitative test er testtypen indstillet til <strong>Indstilling</strong> på siden <strong>Test</strong>). Brug siden <strong>Testgrupper</strong> til at tildele en testvariabel og standardudfaldet til en individuel kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-330">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="e7c0e-331">En produktionsvirksomhed, der fremstiller småkager, anvender en inspektionstest for det færdige produkt.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-331">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="e7c0e-332">Denne inspektionstest har adskillige variabler.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-332">This inspection test has of several variables.</span></span> <span data-ttu-id="e7c0e-333">En af variablerne er smag, og de mulige udfald for denne variabel er god og dårlig.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-333">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="e7c0e-334">Farve er en anden variabel, og de mulige udfald er mørk, for lys og korrekt.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-334">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="e7c0e-335">Hvert udfald får tildelt status <strong>Bestået</strong> eller <strong>Mislykket</strong>.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-335">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="e7c0e-336">Under inspektionstesten til hver variabel, rapporterer den person, der foretager inspektionen, testresultatet ved at vælge et af udfaldene.</span><span class="sxs-lookup"><span data-stu-id="e7c0e-336">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="e7c0e-337">Se også</span><span class="sxs-lookup"><span data-stu-id="e7c0e-337">See also</span></span>
--------

[<span data-ttu-id="e7c0e-338">Processer for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="e7c0e-338">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="e7c0e-339">Aktivering af uoverensstemmelsesstyring</span><span class="sxs-lookup"><span data-stu-id="e7c0e-339">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)

