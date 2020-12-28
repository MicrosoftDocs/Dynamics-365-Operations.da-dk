---
title: Oversigt over kvalitetsstyring
description: I dette emne beskrives det, hvordan du kan bruge kvalitetsstyring i Dynamics 365 Supply Chain Management til at forbedre produktkvaliteten i forsyningskæden.
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1d7828e6bb9a3684c1d76e2cfac96174a8dfbf4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424700"
---
# <a name="quality-management-overview"></a><span data-ttu-id="028e6-103">Oversigt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="028e6-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="028e6-104">I dette emne beskrives det, hvordan du kan bruge kvalitetsstyring i Dynamics 365 Supply Chain Management til at forbedre produktkvaliteten i forsyningskæden.</span><span class="sxs-lookup"><span data-stu-id="028e6-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="028e6-105">Kvalitetsstyring kan hjælpe dig med at administrere behandlingstid, når du håndterer ikke-standardiserede produkter, uanset deres oprindelsessted.</span><span class="sxs-lookup"><span data-stu-id="028e6-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="028e6-106">Fordi diagnosticeringstyper er knyttet til rapportering af korrektion, kan Supply Chain Management planlægge opgaver for at løse problemer og forhindre dem i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="028e6-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="028e6-107">Ud over funktionalitet til administration af uoverensstemmelse omfatter kvalitetsstyring funktionalitet til sporing af problemer efter problemtype (også interne problemer) og til identificering af løsninger som kortsigtede eller langsigtede.</span><span class="sxs-lookup"><span data-stu-id="028e6-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="028e6-108">Statistik over nøgletal (KPI'er) giver indsigt i historikken for tidligere problemer med uoverensstemmelse, og de løsninger, der blev anvendt til at rette dem.</span><span class="sxs-lookup"><span data-stu-id="028e6-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="028e6-109">Du kan bruge historikdata til at gennemgå effektiviteten af tidligere kvalitetsmål og fastlægge passende foranstaltninger, der skal bruges i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="028e6-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="028e6-110">Når du opretter en kvalitetstilknytning, kan Supply Chain Management oprette kvalitetsordrer for forskellige forretningsprocesser, hændelser og betingelser.</span><span class="sxs-lookup"><span data-stu-id="028e6-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="028e6-111">Kvalitetstilknytningen kan dække en bestemt vare, en bestemt gruppe varer eller alle varer.</span><span class="sxs-lookup"><span data-stu-id="028e6-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="028e6-112">Eksempler på brug af kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="028e6-112">Examples of the use of quality management</span></span>
<span data-ttu-id="028e6-113">Kvalitetsstyring er fleksibel og kan gennemføres på forskellige måder for at opfylde kravene på bestemte niveauer i forsyningskædeoperationer.</span><span class="sxs-lookup"><span data-stu-id="028e6-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="028e6-114">Eksemplerne nedenfor viser mulige anvendelser af disse funktioner:</span><span class="sxs-lookup"><span data-stu-id="028e6-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="028e6-115">Automatisk starte en proces for kvalitetskontrol baseret på foruddefinerede kriterier (ved lagerregistreringen af en indkøbsordre fra en bestemt leverandør).</span><span class="sxs-lookup"><span data-stu-id="028e6-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="028e6-116">Spærre lageret under kontrol for at forhindre, at ikke-godkendt lagerbeholdning bliver brugt (fuld spærring af indkøbsordreantal).</span><span class="sxs-lookup"><span data-stu-id="028e6-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="028e6-117">Bruge vareprøve som en del af en kvalitetstilknytning til at definere beløbet af det aktuelle fysiske lager, der skal undersøges.</span><span class="sxs-lookup"><span data-stu-id="028e6-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="028e6-118">Vareprøver kan baseres på faste antal, en procentdel eller et fuldt id.</span><span class="sxs-lookup"><span data-stu-id="028e6-118">Sampling can be based on fixed quantities, a percentage, or full license plate.</span></span>

> [!NOTE]
> <span data-ttu-id="028e6-119">Funktionen _Kvalitetsstyring for lagerstedsprocesser_ udvider funktionerne for kvalitetsstyring.</span><span class="sxs-lookup"><span data-stu-id="028e6-119">The _Quality management for warehouse processes_ feature extends the capabilities of quality management.</span></span> <span data-ttu-id="028e6-120">Hvis du bruger denne funktion, skal du se [Kvalitetsstyring for lagerstedsprocesser](quality-management-for-warehouses-processes.md) for at få vist eksempler på, hvordan kvalitetsstyring fungerer, når den er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="028e6-120">If you are using this feature, then see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md) for examples of how quality management works when it's enabled.</span></span>

-   <span data-ttu-id="028e6-121">Opret kvalitetsordrer for delleverancer.</span><span class="sxs-lookup"><span data-stu-id="028e6-121">Create quality orders for partial receipts.</span></span> <span data-ttu-id="028e6-122">For at oprette en kvalitetsordre, der er baseret på det antal, der fysisk er modtaget med en ordre, skal du markere afkrydsningsfeltet **Pr. opdateret antal** i formularen **Vareprøve**.</span><span class="sxs-lookup"><span data-stu-id="028e6-122">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="028e6-123">Oprette testtyper, der omfatter minimum, maksimum og måltestværdier og udføre kvalitative kontra kvantitative test, der har foruddefinerede valideringsresultater.</span><span class="sxs-lookup"><span data-stu-id="028e6-123">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="028e6-124">Angive et acceptabelt kvalitetsniveau (AQL) for at styre tolerancer for kvalitetsmål.</span><span class="sxs-lookup"><span data-stu-id="028e6-124">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="028e6-125">Angive de ressourcer, som en inspektionshandling kræver, f.eks. et testområde og testinstrumenter.</span><span class="sxs-lookup"><span data-stu-id="028e6-125">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="028e6-126">Arbejde med kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="028e6-126">Working with quality associations</span></span>
<span data-ttu-id="028e6-127">Den forretningsproces, der bruger en kvalitetstilknytning, kan knyttes til forskellige kildedokumenter, f.eks. indkøbsordrer, salgsordrer eller produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="028e6-127">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="028e6-128">De enkelte kvalitetstilknytningsposter definerer de test, det acceptable kvalitetsniveau (AQL) og den vareprøveplan, der gælder for de kvalitetsordrer, der oprettes.</span><span class="sxs-lookup"><span data-stu-id="028e6-128">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="028e6-129">Du skal definere en kvalitetstilknytningspost for hver ændring i en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="028e6-129">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="028e6-130">Du kan f.eks. angive en kvalitetstilknytning, der genererer en kvalitetsordre, når en produktkvittering for en indkøbsordre opdateres.</span><span class="sxs-lookup"><span data-stu-id="028e6-130">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="028e6-131">Afhængigt af opsætningen af udførelsesplanen kan selve den udløsende proces blive blokeret, mens der er en åben kvalitetsordre, eller de næste processer, som f.eks. fakturering, kan blive blokeret.</span><span class="sxs-lookup"><span data-stu-id="028e6-131">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="028e6-132">**Bemærk!** Der kan være åbne kvalitetsordrer, men lagerantal blokeres automatisk fra at blive udstedet.</span><span class="sxs-lookup"><span data-stu-id="028e6-132">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="028e6-133">Afhængigt af indstillingen **Fuld spærring** på siden **Stikprøver af varer** er antallet enten kvantiteten i kvalitetsordren eller kvantiteten i kildedokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="028e6-133">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="028e6-134">For en given forretningsproces identificerer kvalitetstilknytningsposten hændelsen og de betingelser, som der oprettes en kvalitetsordre for.</span><span class="sxs-lookup"><span data-stu-id="028e6-134">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="028e6-135">Betingelserne kan være specifikke for et sted eller en juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="028e6-135">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="028e6-136">En kvalitetsordre, der involverer destruktive prøvninger, kan kun oprettes, når der findes en disponible lagerbeholdning for hændelsen.</span><span class="sxs-lookup"><span data-stu-id="028e6-136">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="028e6-137">I følgende eksempel vises, hvordan en kvalitetstilknytningspost defineres for variationerne i de enkelte forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="028e6-137">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="028e6-138">Eksemplerne vises også i følgende tabel som en oversigt over de hændelser og betingelser, der er defineret af en kvalitetstilknytningspost.</span><span class="sxs-lookup"><span data-stu-id="028e6-138">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="028e6-139">Referencetype</span><span class="sxs-lookup"><span data-stu-id="028e6-139">Reference type</span></span></th>
<th><span data-ttu-id="028e6-140">Hændelsestype</span><span class="sxs-lookup"><span data-stu-id="028e6-140">Event type</span></span></th>
<th><span data-ttu-id="028e6-141">Udførelse</span><span class="sxs-lookup"><span data-stu-id="028e6-141">Execution</span></span></th>
<th><span data-ttu-id="028e6-142">Hændelsesspærring</span><span class="sxs-lookup"><span data-stu-id="028e6-142">Event blocking</span></span></th>
<th><span data-ttu-id="028e6-143">Dokumentreference</span><span class="sxs-lookup"><span data-stu-id="028e6-143">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="028e6-144">Lager</span><span class="sxs-lookup"><span data-stu-id="028e6-144">Inventory</span></span></td>
<td><span data-ttu-id="028e6-145">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="028e6-145">Not applicable</span></span></td>
<td><span data-ttu-id="028e6-146">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="028e6-146">Not applicable</span></span></td>
<td><span data-ttu-id="028e6-147">Ingen</span><span class="sxs-lookup"><span data-stu-id="028e6-147">None</span></span></td>
<td><span data-ttu-id="028e6-148">Alle</span><span class="sxs-lookup"><span data-stu-id="028e6-148">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="028e6-149">Salg</span><span class="sxs-lookup"><span data-stu-id="028e6-149">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="028e6-150">Plukproces er planlagt</span><span class="sxs-lookup"><span data-stu-id="028e6-150">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="028e6-151">Før</span><span class="sxs-lookup"><span data-stu-id="028e6-151">Before</span></span></td>
<td><span data-ttu-id="028e6-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="028e6-152">None</span></span></td>
<td rowspan="22"><span data-ttu-id="028e6-153">Bestemt id, gruppe eller kun alle</span><span class="sxs-lookup"><span data-stu-id="028e6-153">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-154">Plukproces</span><span class="sxs-lookup"><span data-stu-id="028e6-154">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-155">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="028e6-155">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-156">Faktura</span><span class="sxs-lookup"><span data-stu-id="028e6-156">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="028e6-157">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="028e6-157">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="028e6-158">Før</span><span class="sxs-lookup"><span data-stu-id="028e6-158">Before</span></span></td>
<td><span data-ttu-id="028e6-159">Ingen</span><span class="sxs-lookup"><span data-stu-id="028e6-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-160">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="028e6-160">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-161">Faktura</span><span class="sxs-lookup"><span data-stu-id="028e6-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="028e6-162">Indkøb</span><span class="sxs-lookup"><span data-stu-id="028e6-162">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="028e6-163">Tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="028e6-163">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="028e6-164">Før</span><span class="sxs-lookup"><span data-stu-id="028e6-164">Before</span></span></td>
<td><span data-ttu-id="028e6-165">Ingen</span><span class="sxs-lookup"><span data-stu-id="028e6-165">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-166">Tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="028e6-166">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-167">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="028e6-167">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-168">Faktura</span><span class="sxs-lookup"><span data-stu-id="028e6-168">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="028e6-169">Efter</span><span class="sxs-lookup"><span data-stu-id="028e6-169">After</span></span></td>
<td><span data-ttu-id="028e6-170">Ingen</span><span class="sxs-lookup"><span data-stu-id="028e6-170">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-171">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="028e6-171">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-172">Faktura</span><span class="sxs-lookup"><span data-stu-id="028e6-172">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="028e6-173">Registrering</span><span class="sxs-lookup"><span data-stu-id="028e6-173">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="028e6-174">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="028e6-174">Not applicable</span></span></td>
<td><span data-ttu-id="028e6-175">Ingen</span><span class="sxs-lookup"><span data-stu-id="028e6-175">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-176">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="028e6-176">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-177">Faktura</span><span class="sxs-lookup"><span data-stu-id="028e6-177">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="028e6-178">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="028e6-178">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="028e6-179">Før</span><span class="sxs-lookup"><span data-stu-id="028e6-179">Before</span></span></td>
<td><span data-ttu-id="028e6-180">Ingen</span><span class="sxs-lookup"><span data-stu-id="028e6-180">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-181">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="028e6-181">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-182">Faktura</span><span class="sxs-lookup"><span data-stu-id="028e6-182">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="028e6-183">Efter</span><span class="sxs-lookup"><span data-stu-id="028e6-183">After</span></span></td>
<td><span data-ttu-id="028e6-184">Ingen</span><span class="sxs-lookup"><span data-stu-id="028e6-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-185">Faktura</span><span class="sxs-lookup"><span data-stu-id="028e6-185">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="028e6-186">Produktion</span><span class="sxs-lookup"><span data-stu-id="028e6-186">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="028e6-187">Registrering</span><span class="sxs-lookup"><span data-stu-id="028e6-187">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="028e6-188">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="028e6-188">Not applicable</span></span></td>
<td><span data-ttu-id="028e6-189">Ingen</span><span class="sxs-lookup"><span data-stu-id="028e6-189">None</span></span></td>
<td rowspan="12"><span data-ttu-id="028e6-190">Alle</span><span class="sxs-lookup"><span data-stu-id="028e6-190">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-191">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="028e6-191">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-192">Afslut</span><span class="sxs-lookup"><span data-stu-id="028e6-192">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="028e6-193">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="028e6-193">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="028e6-194">Før</span><span class="sxs-lookup"><span data-stu-id="028e6-194">Before</span></span></td>
<td><span data-ttu-id="028e6-195">Ingen</span><span class="sxs-lookup"><span data-stu-id="028e6-195">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-196">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="028e6-196">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-197">Afslut</span><span class="sxs-lookup"><span data-stu-id="028e6-197">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="028e6-198">Efter</span><span class="sxs-lookup"><span data-stu-id="028e6-198">After</span></span></td>
<td><span data-ttu-id="028e6-199">Ingen</span><span class="sxs-lookup"><span data-stu-id="028e6-199">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-200">Afslut</span><span class="sxs-lookup"><span data-stu-id="028e6-200">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="028e6-201">Karantæne</span><span class="sxs-lookup"><span data-stu-id="028e6-201">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="028e6-202">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="028e6-202">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="028e6-203">Før</span><span class="sxs-lookup"><span data-stu-id="028e6-203">Before</span></span></td>
<td><span data-ttu-id="028e6-204">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="028e6-204">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-205">Afslut</span><span class="sxs-lookup"><span data-stu-id="028e6-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-206">Efter</span><span class="sxs-lookup"><span data-stu-id="028e6-206">After</span></span></td>
<td><span data-ttu-id="028e6-207">Afslut</span><span class="sxs-lookup"><span data-stu-id="028e6-207">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-208">Afslut</span><span class="sxs-lookup"><span data-stu-id="028e6-208">End</span></span></td>
<td><span data-ttu-id="028e6-209">Før</span><span class="sxs-lookup"><span data-stu-id="028e6-209">Before</span></span></td>
<td><span data-ttu-id="028e6-210">Afslut</span><span class="sxs-lookup"><span data-stu-id="028e6-210">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="028e6-211">Ruteoperation</span><span class="sxs-lookup"><span data-stu-id="028e6-211">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="028e6-212">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="028e6-212">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="028e6-213">Før</span><span class="sxs-lookup"><span data-stu-id="028e6-213">Before</span></span></td>
<td><span data-ttu-id="028e6-214">Ingen</span><span class="sxs-lookup"><span data-stu-id="028e6-214">None</span></span></td>
<td rowspan="3"><span data-ttu-id="028e6-215">Bestemt id, gruppe eller alle, og ressourcespecifik, gruppe eller alle</span><span class="sxs-lookup"><span data-stu-id="028e6-215">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-216">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="028e6-216">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-217">Efter</span><span class="sxs-lookup"><span data-stu-id="028e6-217">After</span></span></td>
<td><span data-ttu-id="028e6-218">Ingen</span><span class="sxs-lookup"><span data-stu-id="028e6-218">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="028e6-219">Produktion af samprodukter</span><span class="sxs-lookup"><span data-stu-id="028e6-219">Co-product production</span></span></td>
<td><span data-ttu-id="028e6-220">Registrering</span><span class="sxs-lookup"><span data-stu-id="028e6-220">Registration</span></span></td>
<td><span data-ttu-id="028e6-221">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="028e6-221">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="028e6-222">Ingen</span><span class="sxs-lookup"><span data-stu-id="028e6-222">None</span></span></td>
<td rowspan="3"><span data-ttu-id="028e6-223">Alle</span><span class="sxs-lookup"><span data-stu-id="028e6-223">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="028e6-224">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="028e6-224">Report as finished</span></span></td>
<td><span data-ttu-id="028e6-225">Før</span><span class="sxs-lookup"><span data-stu-id="028e6-225">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-226">Efter</span><span class="sxs-lookup"><span data-stu-id="028e6-226">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="028e6-227">Tabellen nedenfor indeholder flere oplysninger om, hvordan kvalitetsordrer kan oprettes for bestemte typer processer.</span><span class="sxs-lookup"><span data-stu-id="028e6-227">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="028e6-228">Procestype</span><span class="sxs-lookup"><span data-stu-id="028e6-228">Type of process</span></span></th>
<th><span data-ttu-id="028e6-229">Når kvalitetsordrer kan genereres automatisk</span><span class="sxs-lookup"><span data-stu-id="028e6-229">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="028e6-230">Når kvalitetsordrer kan genereres, hvis destruktiv prøvning er påkrævet</span><span class="sxs-lookup"><span data-stu-id="028e6-230">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="028e6-231">Betingelsesoplysninger</span><span class="sxs-lookup"><span data-stu-id="028e6-231">Condition information</span></span></th>
<th><span data-ttu-id="028e6-232">Manuel oprettelse af oplysninger</span><span class="sxs-lookup"><span data-stu-id="028e6-232">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="028e6-233">Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="028e6-233">Purchase order</span></span></td>
<td><span data-ttu-id="028e6-234">Før eller efter en tilgangsliste eller produktkvittering for det materiale, der er modtaget, bogføres</span><span class="sxs-lookup"><span data-stu-id="028e6-234">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="028e6-235">Efter produktkvitteringen for det materiale, der er modtaget, bogføres, da materialet skal være tilgængelig til destruktiv prøvning</span><span class="sxs-lookup"><span data-stu-id="028e6-235">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="028e6-236">Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller kreditor eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="028e6-236">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="028e6-237">En manuelt oprettet kvalitetsordre, der refererer til en indkøbsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="028e6-237">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-238">Karantæneordre</span><span class="sxs-lookup"><span data-stu-id="028e6-238">Quarantine order</span></span></td>
<td><span data-ttu-id="028e6-239">Før eller efter karantæneordren rapporteres som færdigmeldt eller afsluttet</span><span class="sxs-lookup"><span data-stu-id="028e6-239">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="028e6-240">Kvalitetsordrer, der kræver destruktive prøvninger kan ikke oprettes.</span><span class="sxs-lookup"><span data-stu-id="028e6-240">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="028e6-241">Det antages, at funktionerne i karantæneordren håndterer bortskaffelsen af det materiale, der destrueres.</span><span class="sxs-lookup"><span data-stu-id="028e6-241">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="028e6-242">Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller kreditor eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="028e6-242">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="028e6-243">En manuelt oprettet kvalitetsordre, der refererer til en karantæneordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="028e6-243">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-244">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="028e6-244">Sales order</span></span></td>
<td><span data-ttu-id="028e6-245">Før en planlagt plukproces eller opdatering af følgesedlen for de varer, der skal leveres</span><span class="sxs-lookup"><span data-stu-id="028e6-245">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="028e6-246">På alle trin</span><span class="sxs-lookup"><span data-stu-id="028e6-246">At any step</span></span></td>
<td><span data-ttu-id="028e6-247">Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller debitor eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="028e6-247">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="028e6-248">En manuelt oprettet kvalitetsordre, der refererer til en salgsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="028e6-248">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-249">Produktionsordre</span><span class="sxs-lookup"><span data-stu-id="028e6-249">Production order</span></span></td>
<td><span data-ttu-id="028e6-250">Før eller efter det færdigmeldte antal for produktionsordren er rapporteret</span><span class="sxs-lookup"><span data-stu-id="028e6-250">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="028e6-251">Efter det færdigmeldte antal for produktionsordren er rapporteret</span><span class="sxs-lookup"><span data-stu-id="028e6-251">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="028e6-252">Behovet for en kvalitetsordre kan afhænge af en bestemt lokation eller vare eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="028e6-252">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="028e6-253">En manuelt oprettet kvalitetsordre, der refererer til en produktionsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="028e6-253">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-254">Produktionsordre, der har en ruteoperation</span><span class="sxs-lookup"><span data-stu-id="028e6-254">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="028e6-255">Før eller efter rapporten er færdigmeldt for en operation</span><span class="sxs-lookup"><span data-stu-id="028e6-255">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="028e6-256">Efter færdigrapportering af produktionen for den sidste operation</span><span class="sxs-lookup"><span data-stu-id="028e6-256">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="028e6-257">Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller operationsressource eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="028e6-257">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="028e6-258">En manuelt oprettet kvalitetsordre, der refererer til en ruteoperation, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="028e6-258">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="028e6-259">Lager</span><span class="sxs-lookup"><span data-stu-id="028e6-259">Inventory</span></span></td>
<td><span data-ttu-id="028e6-260">En kvalitetsordre kan ikke genereres automatisk for en transaktion i en lagerkladde eller flytteordretransaktioner.</span><span class="sxs-lookup"><span data-stu-id="028e6-260">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="028e6-261">En kvalitetsordre skal oprettes manuelt for en vares lagerantal.</span><span class="sxs-lookup"><span data-stu-id="028e6-261">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="028e6-262">Fysisk disponibel lagerbeholdning er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="028e6-262">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="028e6-263">Eksempler på automatisk generering af kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="028e6-263">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="028e6-264">Køb</span><span class="sxs-lookup"><span data-stu-id="028e6-264">Purchasing</span></span>

<span data-ttu-id="028e6-265">Hvis du i forbindelse med indkøb angiver feltet **Hændelsestype** til **Produktkvittering** og feltet **Udførelse** til **Efter** på siden **Kvalitetstilknytninger**, får du følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="028e6-265">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="028e6-266">Hvis indstillingen **Pr. opdateret antal** er angivet til **Ja**, genereres der en kvalitetsordre for hver kvittering i forhold til indkøbsordren baseret på det modtagne antal og indstillinger i stikprøven af vare.</span><span class="sxs-lookup"><span data-stu-id="028e6-266">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="028e6-267">Hver gang der modtages et antal på indkøbsordren, oprettes der nye kvalitetsordrer ud fra det nye antal, der er modtaget.</span><span class="sxs-lookup"><span data-stu-id="028e6-267">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="028e6-268">Hvis indstillingen **Pr. opdateret antal** er angivet til **Nej**, genereres der en kvalitetsordre for den første kvittering i forhold til indkøbsordren baseret på det modtagne antal.</span><span class="sxs-lookup"><span data-stu-id="028e6-268">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="028e6-269">Derudover oprettes en eller flere kvalitetsordrer ud fra det resterende antal afhængigt af sporingsdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="028e6-269">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="028e6-270">Kvalitetsordrer genereres ikke for efterfølgende kvitteringer i forhold til indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="028e6-270">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="028e6-271">Produktion</span><span class="sxs-lookup"><span data-stu-id="028e6-271">Production</span></span>

<span data-ttu-id="028e6-272">Hvis du i forbindelse med produktion angiver feltet **Hændelsestype** til **Færdigmelding** og feltet **Udførelse** til **Efter** på siden **Kvalitetstilknytninger**, får du følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="028e6-272">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="028e6-273">Hvis indstillingen **Pr. opdateret antal** er angivet til **Ja**, genereres der en kvalitetsordre baseret på hvert færdige antal og indstillinger i stikprøven af vare.</span><span class="sxs-lookup"><span data-stu-id="028e6-273">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="028e6-274">Hver gang et antal færdigmeldes på indkøbsordren, oprettes der nye kvalitetsordrer ud fra det nye antal, der er færdigmeldt.</span><span class="sxs-lookup"><span data-stu-id="028e6-274">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="028e6-275">Denne genereringslogik stemmer overens med indkøb.</span><span class="sxs-lookup"><span data-stu-id="028e6-275">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="028e6-276">Hvis indstillingen **Pr. opdateret antal** er angivet til **Nej**, genereres der en kvalitetsordre, første gang et antal færdigmeldes, baseret på det færdige antal.</span><span class="sxs-lookup"><span data-stu-id="028e6-276">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="028e6-277">Derudover oprettes en eller flere kvalitetsordrer ud fra det resterende antal afhængigt af sporingsdimensionerne for stikprøven af varen.</span><span class="sxs-lookup"><span data-stu-id="028e6-277">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="028e6-278">Kvalitetsordrer genereres ikke for efterfølgende færdige antal.</span><span class="sxs-lookup"><span data-stu-id="028e6-278">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="028e6-279">Kvalitetsspecifikation</span><span class="sxs-lookup"><span data-stu-id="028e6-279">Quality specification</span></span></th>
<th><span data-ttu-id="028e6-280">Pr. opdateret antal</span><span class="sxs-lookup"><span data-stu-id="028e6-280">Per updated quantity</span></span></th>
<th><span data-ttu-id="028e6-281">Pr. sporingsdimension</span><span class="sxs-lookup"><span data-stu-id="028e6-281">Per tracking dimension</span></span></th>
<th><span data-ttu-id="028e6-282">Resultat</span><span class="sxs-lookup"><span data-stu-id="028e6-282">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="028e6-283">Procent: 10 %</span><span class="sxs-lookup"><span data-stu-id="028e6-283">Percentage: 10%</span></span></td>
<td><span data-ttu-id="028e6-284">Ja</span><span class="sxs-lookup"><span data-stu-id="028e6-284">Yes</span></span></td>
<td>
<p><span data-ttu-id="028e6-285">Batchnummer: Nej</span><span class="sxs-lookup"><span data-stu-id="028e6-285">Batch number: No</span></span></p>
<p><span data-ttu-id="028e6-286">Serienummer: Nej</span><span class="sxs-lookup"><span data-stu-id="028e6-286">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="028e6-287">Ordreantal: 100</span><span class="sxs-lookup"><span data-stu-id="028e6-287">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="028e6-288">Færdigmelding for 30</span><span class="sxs-lookup"><span data-stu-id="028e6-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="028e6-289">Kvalitetsordrenr. 1 for 3 (10 % af 30)</span><span class="sxs-lookup"><span data-stu-id="028e6-289">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="028e6-290">Færdigmelding for 70</span><span class="sxs-lookup"><span data-stu-id="028e6-290">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="028e6-291">Kvalitetsordrenr. 2 for 7 (10 % af det resterende ordreantal, hvilket er lig med 70 i dette tilfælde)</span><span class="sxs-lookup"><span data-stu-id="028e6-291">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="028e6-292">Fast antal: 1</span><span class="sxs-lookup"><span data-stu-id="028e6-292">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="028e6-293">Nr.</span><span class="sxs-lookup"><span data-stu-id="028e6-293">No</span></span></td>
<td>
<p><span data-ttu-id="028e6-294">Batchnummer: Nej</span><span class="sxs-lookup"><span data-stu-id="028e6-294">Batch number: No</span></span></p>
<p><span data-ttu-id="028e6-295">Serienummer: Nej</span><span class="sxs-lookup"><span data-stu-id="028e6-295">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="028e6-296">Ordreantal: 100</span><span class="sxs-lookup"><span data-stu-id="028e6-296">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="028e6-297">Færdigmelding for 30</span><span class="sxs-lookup"><span data-stu-id="028e6-297">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="028e6-298">Kvalitetsordrenr. 1 for 1 (for det første færdigmeldte antal, der har en fast værdi af 1)</span><span class="sxs-lookup"><span data-stu-id="028e6-298">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="028e6-299">Kvalitetsordrenr. 2 for 1 (for det resterende antal, der stadig har en fast værdi af 1)</span><span class="sxs-lookup"><span data-stu-id="028e6-299">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="028e6-300">Færdigmelding for 10</span><span class="sxs-lookup"><span data-stu-id="028e6-300">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="028e6-301">Der oprettes ingen kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="028e6-301">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="028e6-302">Færdigmelding for 60</span><span class="sxs-lookup"><span data-stu-id="028e6-302">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="028e6-303">Der oprettes ingen kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="028e6-303">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="028e6-304">Fast antal: 1</span><span class="sxs-lookup"><span data-stu-id="028e6-304">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="028e6-305">Ja</span><span class="sxs-lookup"><span data-stu-id="028e6-305">Yes</span></span></td>
<td>
<p><span data-ttu-id="028e6-306">Batchnummer: Ja</span><span class="sxs-lookup"><span data-stu-id="028e6-306">Batch number: Yes</span></span></p>
<p><span data-ttu-id="028e6-307">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="028e6-307">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="028e6-308">Ordreantal: 10</span><span class="sxs-lookup"><span data-stu-id="028e6-308">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="028e6-309">Færdigmeld for 3: 1 for nr. b1, nr. s1. 1 for nr. b2, nr. s2 og 1 for nr. b3, nr. s3</span><span class="sxs-lookup"><span data-stu-id="028e6-309">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="028e6-310">Kvalitetsordrenr. 1 for 1 af batchnr. b1, serienr. s1</span><span class="sxs-lookup"><span data-stu-id="028e6-310">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="028e6-311">Kvalitetsordrenr. 2 for 1 af batchnr. b2, serienr. s2</span><span class="sxs-lookup"><span data-stu-id="028e6-311">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="028e6-312">Kvalitetsordrenr. 3 for 1 af batchnr. b3, serienr. s3</span><span class="sxs-lookup"><span data-stu-id="028e6-312">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="028e6-313">Færdigmeld for 2: 1 for nr. b4, nr. s4. og 1 for nr. b5, nr. s5</span><span class="sxs-lookup"><span data-stu-id="028e6-313">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="028e6-314">Kvalitetsordrenr. 4 for 1 af batchnr. b4, serienr. s4</span><span class="sxs-lookup"><span data-stu-id="028e6-314">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="028e6-315">Kvalitetsordrenr. 5 for 1 af batchnr. b5, serienr. s5</span><span class="sxs-lookup"><span data-stu-id="028e6-315">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="028e6-316"><strong>Bemærk:</strong> Batchen kan genbruges.</span><span class="sxs-lookup"><span data-stu-id="028e6-316"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="028e6-317">Fast antal: 2</span><span class="sxs-lookup"><span data-stu-id="028e6-317">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="028e6-318">Nr.</span><span class="sxs-lookup"><span data-stu-id="028e6-318">No</span></span></td>
<td>
<p><span data-ttu-id="028e6-319">Batchnummer: Ja</span><span class="sxs-lookup"><span data-stu-id="028e6-319">Batch number: Yes</span></span></p>
<p><span data-ttu-id="028e6-320">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="028e6-320">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="028e6-321">Ordreantal: 10</span><span class="sxs-lookup"><span data-stu-id="028e6-321">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="028e6-322">Færdigmeld for 4: 1 for nr. b1, nr. s1. 1 for nr. b2, nr. s2, 1 for nr. b3, nr. s3 og 1 for nr. b4, nr. s4</span><span class="sxs-lookup"><span data-stu-id="028e6-322">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="028e6-323">Kvalitetsordrenr. 1 for 1 af batchnr. b1, serienr. s1</span><span class="sxs-lookup"><span data-stu-id="028e6-323">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="028e6-324">Kvalitetsordrenr. 2 for 1 af batchnr. b2, serienr. s2</span><span class="sxs-lookup"><span data-stu-id="028e6-324">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="028e6-325">Kvalitetsordrenr. 3 for 1 af batchnr. b3, serienr. s3</span><span class="sxs-lookup"><span data-stu-id="028e6-325">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="028e6-326">Kvalitetsordrenr. 4 for 1 af batchnr. b4, serienr. s4</span><span class="sxs-lookup"><span data-stu-id="028e6-326">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="028e6-327">Kvalitetsordre nr. 5 for 2, uden en reference til et batch og et serienummer</span><span class="sxs-lookup"><span data-stu-id="028e6-327">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="028e6-328">Færdigmeld for 6: 1 for nr. b5, nr. s5. 1 for nr. b6, nr. s6. 1 for nr. b7, nr. s7. 1 for nr. b8, nr. s8. 1 for nr. b9, nr. s9 og 1 for nr. b10, nr. s10</span><span class="sxs-lookup"><span data-stu-id="028e6-328">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="028e6-329">Der oprettes ingen kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="028e6-329">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="028e6-330">Funktionen *Kvalitetsstyring for lagerstedsprocesser* føjer egenskaber til behandling af kvalitetsordrer til produktion med **Hændelsestype** angivet til *Færdigmeld* og **Udførelse** angivet til *Efter* og for køb med **Hændelsestype** angivet til *Færdigmelding*.</span><span class="sxs-lookup"><span data-stu-id="028e6-330">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production with **Event type** set to *Report as finished* and **Execution** set to *After*, and for purchases with **Event type** set to *Registration*.</span></span> <span data-ttu-id="028e6-331">Der er flere oplysninger under [Kvalitetsstyring for lagerstedsprocesser](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="028e6-331">For details, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

## <a name="quality-management-pages"></a><span data-ttu-id="028e6-332">Kvalitetsstyringssider</span><span class="sxs-lookup"><span data-stu-id="028e6-332">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="028e6-333">Side</span><span class="sxs-lookup"><span data-stu-id="028e6-333">Page</span></span></th>
<th><span data-ttu-id="028e6-334">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="028e6-334">Description</span></span></th>
<th><span data-ttu-id="028e6-335">Eksempel</span><span class="sxs-lookup"><span data-stu-id="028e6-335">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="028e6-336">Kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="028e6-336">Quality associations</span></span></td>
<td><span data-ttu-id="028e6-337">Se de tidligere afsnit i denne artikel.</span><span class="sxs-lookup"><span data-stu-id="028e6-337">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="028e6-338">En kvalitetstilknytning angiver alle følgende oplysninger for en kvalitetsordre, der oprettes:</span><span class="sxs-lookup"><span data-stu-id="028e6-338">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="028e6-339">Posteringshændelsen</span><span class="sxs-lookup"><span data-stu-id="028e6-339">The transaction event</span></span></li>
<li><span data-ttu-id="028e6-340">Det sæt test, der skal udføres på varerne</span><span class="sxs-lookup"><span data-stu-id="028e6-340">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="028e6-341">Det acceptable kvalitetsniveau (AQL)</span><span class="sxs-lookup"><span data-stu-id="028e6-341">The AQL</span></span></li>
<li><span data-ttu-id="028e6-342">Prøveplanen</span><span class="sxs-lookup"><span data-stu-id="028e6-342">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="028e6-343">Du skal definere en kvalitetstilknytning for hver afvigelse i en forretningsproces, der kræver automatisk generering af kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="028e6-343">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="028e6-344">For eksempel kan der oprettes en kvalitetsordre i forretningsprocesserne for indkøbsordrer, karantæneordrer, salgsordrer og produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="028e6-344">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="028e6-345">Test</span><span class="sxs-lookup"><span data-stu-id="028e6-345">Tests</span></span></td>
<td><span data-ttu-id="028e6-346">Du kan bruge denne side til at definere og få vist de individuelle test, der bestemmer, om produkterne opfylder kvalitetsspecifikationerne.</span><span class="sxs-lookup"><span data-stu-id="028e6-346">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="028e6-347">Du kan tildele en eller flere individuelle test til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="028e6-347">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="028e6-348">Når du gør det, skal du også angive testspecifikke oplysninger, f.eks. de acceptable måleværdier.</span><span class="sxs-lookup"><span data-stu-id="028e6-348">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="028e6-349">Måleværdier bruges til kvantitative test, og testvariabler bruges til kvalitative test.</span><span class="sxs-lookup"><span data-stu-id="028e6-349">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="028e6-350">En kvantitativ test har testtypen <strong>Heltal</strong> eller <strong>Del</strong> og har også en angivet måleenhed.</span><span class="sxs-lookup"><span data-stu-id="028e6-350">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="028e6-351">Kvalitetsspecifikationer og testresultater er udtrykt som tal.</span><span class="sxs-lookup"><span data-stu-id="028e6-351">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="028e6-352">En kvalitativ test har testtypen <strong>Indstilling</strong>.</span><span class="sxs-lookup"><span data-stu-id="028e6-352">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="028e6-353">Kvalitative test forudsætter flere oplysninger om den testvariabel, der måles, og de faste indstillinger.</span><span class="sxs-lookup"><span data-stu-id="028e6-353">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="028e6-354">Kvalitetsspecifikationer og testresultater er udtrykt i overensstemmelse med et udfald.</span><span class="sxs-lookup"><span data-stu-id="028e6-354">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="028e6-355">Et produktionsfirma udfører to test af købt materiale: en kvantitativ test for materialets kvalitet og en kvalitetstest for skader på emballagen.</span><span class="sxs-lookup"><span data-stu-id="028e6-355">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="028e6-356">Firmaet definerer flere oplysninger om den kvalitative test for at identificere testvariablen (beskadiget emballage) og udfaldet.</span><span class="sxs-lookup"><span data-stu-id="028e6-356">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="028e6-357">Firmaet bruger siden <strong>Testgrupper</strong> til at tildele de to test til en testgruppe og til at angive de testspecifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="028e6-357">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="028e6-358">Testgruppen tildeles til en kvalitetsordre, så firmaet kan rapportere testresultaterne for de to test.</span><span class="sxs-lookup"><span data-stu-id="028e6-358">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="028e6-359">Testgrupper</span><span class="sxs-lookup"><span data-stu-id="028e6-359">Test groups</span></span></td>
<td><span data-ttu-id="028e6-360">Brug denne side til at konfigurere, redigere og få vist testgrupper og individuelle test, der er tildelt til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="028e6-360">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="028e6-361">I den øverste rude vises testgrupper, og i den nederste gruppe vises de test, der er knyttet til en valgt testgruppe.</span><span class="sxs-lookup"><span data-stu-id="028e6-361">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="028e6-362">Du kan tildele flere politikker til en testgruppe, f.eks. en prøveplan, et acceptabelt kvalitetsniveau (AQL) og kravet om destruktiv test.</span><span class="sxs-lookup"><span data-stu-id="028e6-362">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="028e6-363">Når du knytter en individuel test til en testgruppe, definerer du flere oplysninger, f.eks. rækkefølge, dokumenter og gyldighedsdatoer.</span><span class="sxs-lookup"><span data-stu-id="028e6-363">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="028e6-364">For kvantitative test skal de oplysninger, du angiver, også omfatte acceptable målingsværdier.</span><span class="sxs-lookup"><span data-stu-id="028e6-364">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="028e6-365">For kvalitative test skal oplysningerne også omfatte testvariablen og standardudfaldet.</span><span class="sxs-lookup"><span data-stu-id="028e6-365">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="028e6-366">Den testgruppe, der tildeles til en kvalitetsordre, definerer det testsæt, der skal som standard skal udføres på den angivne vare.</span><span class="sxs-lookup"><span data-stu-id="028e6-366">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="028e6-367">Du kan dog tilføje, slette eller ændre test i kvalitetsordren.</span><span class="sxs-lookup"><span data-stu-id="028e6-367">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="028e6-368">Testresultaterne rapporteres for hver test i en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="028e6-368">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="028e6-369">En produktionsvirksomhed definerer en testgruppe for hver afvigelse fra firmaets retningslinjer for kvalitet.</span><span class="sxs-lookup"><span data-stu-id="028e6-369">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="028e6-370">De forskellige testgrupper reflekterer forskelle i prøveplaner, hvilke testsæt der skal udføres sammen, det acceptable kvalitetsniveau og andre faktorer.</span><span class="sxs-lookup"><span data-stu-id="028e6-370">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="028e6-371">For kvantitative test er der også forskelle i de acceptable måleværdier.</span><span class="sxs-lookup"><span data-stu-id="028e6-371">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="028e6-372">Virksomheden sikrer sig, at retningslinjerne for kvalitet følges, ved at tildele en testgruppe til hver enkelt regel for automatisk oprettelse af kvalitetsordrer på siden <strong>Kvalitetstilknytning</strong> og tildeler også en testgruppe til kvalitetsordrer, der oprettes manuelt.</span><span class="sxs-lookup"><span data-stu-id="028e6-372">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="028e6-373">Varekvalitetsgrupper</span><span class="sxs-lookup"><span data-stu-id="028e6-373">Item quality groups</span></span></td>
<td><span data-ttu-id="028e6-374">Du kan bruge denne side til at konfigurere, redigere og få vist de varer, der er tildelt en kvalitetsgruppe, eller de kvalitetsgrupper, der er tildelt en vare.</span><span class="sxs-lookup"><span data-stu-id="028e6-374">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="028e6-375">En kvalitetsgruppe repræsenterer almindelige testkrav til varer.</span><span class="sxs-lookup"><span data-stu-id="028e6-375">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="028e6-376">Når du har defineret testkravene på siden <strong>Testgrupper</strong>, kan du definere reglerne for automatisk generering af kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="028e6-376">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="028e6-377">For at forenkle processen skal du undlade at definere regler for de enkelte varer.</span><span class="sxs-lookup"><span data-stu-id="028e6-377">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="028e6-378">I stedet skal du angive regler for en kvalitetsgruppe ved hjælp af siden <strong>Kvalitetstilknytninger</strong>.</span><span class="sxs-lookup"><span data-stu-id="028e6-378">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="028e6-379">Du kan også bruge siden <strong>Varekvalitetsgrupper</strong> for en valgt kvalitetsgruppe for at tildele relevante varer til den pågældende gruppe.</span><span class="sxs-lookup"><span data-stu-id="028e6-379">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="028e6-380">Du kan også bruge siden <strong>Varekvalitetsgrupper</strong> for en valgt kvalitetsgruppe for en valgt vare for at tildele relevante kvalitetsgrupper til den pågældende vare.</span><span class="sxs-lookup"><span data-stu-id="028e6-380">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="028e6-381">En produktionsvirksomhed indkøber forskellige råvarer, der har samme testkrav til indgående inspektion.</span><span class="sxs-lookup"><span data-stu-id="028e6-381">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="028e6-382">Virksomheden definerer en kvalitetsgruppe og tildeler derefter kvalitetsgruppen de varenumre, der er knyttet gruppen.</span><span class="sxs-lookup"><span data-stu-id="028e6-382">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="028e6-383">Senere indkøber virksomheden en ny type råvarer med de samme testkrav.</span><span class="sxs-lookup"><span data-stu-id="028e6-383">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="028e6-384">I stedet for at konfigurere nye testkrav til de nye råvarer føjer virksomheden varenummeret på de nye råvarer til den eksisterende kvalitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="028e6-384">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="028e6-385">Den samme produktionsvirksomhed producerer desuden varer med de samme produktionstestkrav og leverer varer med de samme krav til test før forsendelse.</span><span class="sxs-lookup"><span data-stu-id="028e6-385">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="028e6-386">Virksomheden definerer yderligere to kvalitetsgrupper og tildeler derefter hver gruppe de relevante varenumre.</span><span class="sxs-lookup"><span data-stu-id="028e6-386">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="028e6-387">Testvariabler</span><span class="sxs-lookup"><span data-stu-id="028e6-387">Test variables</span></span></td>
<td><span data-ttu-id="028e6-388">Brug denne side til at angive og få vist variabler, der er tilknyttet en kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="028e6-388">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="028e6-389">Du kan angive faste udfald, der repræsenterer mulighederne for hver variabel.</span><span class="sxs-lookup"><span data-stu-id="028e6-389">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="028e6-390">Du kan definere test på siden <strong>Test</strong>.</span><span class="sxs-lookup"><span data-stu-id="028e6-390">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="028e6-391">Ved kvalitative test skal du angive testtypen <strong>Indstilling</strong>.</span><span class="sxs-lookup"><span data-stu-id="028e6-391">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="028e6-392">Brug siden <strong>Testgrupper</strong> til at tildele en testvariabel til en individuel test.</span><span class="sxs-lookup"><span data-stu-id="028e6-392">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="028e6-393">En produktionsvirksomhed, der fremstiller småkager, anvender en inspektionstest for det færdige produkt.</span><span class="sxs-lookup"><span data-stu-id="028e6-393">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="028e6-394">Denne inspektionstest har adskillige variabler.</span><span class="sxs-lookup"><span data-stu-id="028e6-394">This inspection test has several variables.</span></span> <span data-ttu-id="028e6-395">En af variablerne er smag, og de mulige udfald for denne variabel er god og dårlig.</span><span class="sxs-lookup"><span data-stu-id="028e6-395">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="028e6-396">Farve er en anden variabel, og de mulige udfald er mørk, for lys og korrekt.</span><span class="sxs-lookup"><span data-stu-id="028e6-396">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="028e6-397">Udfald af testvariabel</span><span class="sxs-lookup"><span data-stu-id="028e6-397">Test variable outcomes</span></span></td>
<td><span data-ttu-id="028e6-398">Brug denne side til at konfigurere, redigere og få vist de mulige testresultater for en testvariabel, der er knyttet til en kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="028e6-398">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="028e6-399">For hvert udfald angiver du status <strong>Bestået</strong> eller <strong>Mislykket</strong>.</span><span class="sxs-lookup"><span data-stu-id="028e6-399">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="028e6-400">Du skal definere en variabel og dens udfald for hver kvalitative test, der er defineret på siden <strong>Test</strong>.</span><span class="sxs-lookup"><span data-stu-id="028e6-400">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="028e6-401">(For kvalitative test er testtypen indstillet til <strong>Indstilling</strong> på siden <strong>Test</strong>). Brug siden <strong>Testgrupper</strong> til at tildele en testvariabel og standardudfaldet til en individuel kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="028e6-401">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="028e6-402">En produktionsvirksomhed, der fremstiller småkager, anvender en inspektionstest for det færdige produkt.</span><span class="sxs-lookup"><span data-stu-id="028e6-402">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="028e6-403">Denne inspektionstest har adskillige variabler.</span><span class="sxs-lookup"><span data-stu-id="028e6-403">This inspection test has of several variables.</span></span> <span data-ttu-id="028e6-404">En af variablerne er smag, og de mulige udfald for denne variabel er god og dårlig.</span><span class="sxs-lookup"><span data-stu-id="028e6-404">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="028e6-405">Farve er en anden variabel, og de mulige udfald er mørk, for lys og korrekt.</span><span class="sxs-lookup"><span data-stu-id="028e6-405">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="028e6-406">Hvert udfald får tildelt status <strong>Bestået</strong> eller <strong>Mislykket</strong>.</span><span class="sxs-lookup"><span data-stu-id="028e6-406">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="028e6-407">Under inspektionstesten til hver variabel, rapporterer den person, der foretager inspektionen, testresultatet ved at vælge et af udfaldene.</span><span class="sxs-lookup"><span data-stu-id="028e6-407">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="028e6-408">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="028e6-408">Additional resources</span></span>
--------

[<span data-ttu-id="028e6-409">Processer for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="028e6-409">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="028e6-410">Håndtering af uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="028e6-410">Nonconformance management</span></span>](enable-nonconformance-management.md)

[<span data-ttu-id="028e6-411">Kvalitetsstyring for lagerstedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="028e6-411">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)
