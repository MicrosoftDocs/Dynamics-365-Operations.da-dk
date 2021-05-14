---
title: Kvalitetstilknytninger
description: I dette emne beskriver, hvordan du kan bruge kvalitettilknytninger i Microsoft Dynamics 365 Supply Chain Management til automatisk at generere kvalitetsordrer, der er relateret til dine salgs-, indkøbs- og produktionsprocesser.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f46f09dc9b67cfb04d0320a071c2c739266af58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956591"
---
# <a name="quality-associations"></a><span data-ttu-id="5d452-103">Kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="5d452-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d452-104">I dette emne beskriver, hvordan du kan bruge kvalitettilknytninger i Microsoft Dynamics 365 Supply Chain Management til automatisk at generere kvalitetsordrer, der er relateret til dine salgs-, indkøbs- og produktionsprocesser.</span><span class="sxs-lookup"><span data-stu-id="5d452-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="5d452-105">En kvalitetstilknytning angiver alle følgende oplysninger for en kvalitetsordre, der oprettes:</span><span class="sxs-lookup"><span data-stu-id="5d452-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="5d452-106">Posteringshændelsen</span><span class="sxs-lookup"><span data-stu-id="5d452-106">The transaction event</span></span>
- <span data-ttu-id="5d452-107">Det sæt test, der skal udføres på varerne</span><span class="sxs-lookup"><span data-stu-id="5d452-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="5d452-108">Det acceptable kvalitetsniveau (AQL)</span><span class="sxs-lookup"><span data-stu-id="5d452-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="5d452-109">Prøveplanen</span><span class="sxs-lookup"><span data-stu-id="5d452-109">The sampling plan</span></span>

<span data-ttu-id="5d452-110">Du skal definere en kvalitetstilknytning for hver afvigelse i en forretningsproces, der kræver automatisk generering af kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="5d452-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="5d452-111">For eksempel kan der oprettes en kvalitetsordre i forretningsprocesserne for indkøbsordrer, karantæneordrer, salgsordrer og produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="5d452-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="5d452-112">Arbejde med kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="5d452-112">Working with quality associations</span></span>

<span data-ttu-id="5d452-113">Den forretningsproces, der bruger en kvalitetstilknytning, kan knyttes til forskellige kildedokumenter, f.eks. indkøbsordrer, salgsordrer eller produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="5d452-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="5d452-114">De enkelte kvalitetstilknytningsposter definerer de test, det acceptable kvalitetsniveau (AQL) og den vareprøveplan, der gælder for de kvalitetsordrer, der oprettes.</span><span class="sxs-lookup"><span data-stu-id="5d452-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="5d452-115">Du skal definere en kvalitetstilknytningspost for hver ændring i en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="5d452-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="5d452-116">Du kan f.eks. angive en kvalitetstilknytning, der genererer en kvalitetsordre, når en produktkvittering for en indkøbsordre opdateres.</span><span class="sxs-lookup"><span data-stu-id="5d452-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="5d452-117">Afhængigt af opsætningen af udførelsesplanen kan selve udløserprocessen blokeres, mens der er en åben kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="5d452-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="5d452-118">Efterfølgende processer, f.eks. fakturering af indkøbsordrer, kan også blokeres.</span><span class="sxs-lookup"><span data-stu-id="5d452-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="5d452-119">Der kan være åbne kvalitetsordrer, men lagerantal blokeres automatisk fra at blive udstedt.</span><span class="sxs-lookup"><span data-stu-id="5d452-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="5d452-120">Afhængigt af indstillingen for feltet **Fuld blokering** på siden **Varestikprøver** er antallet enten kvantiteten i kvalitetsordren eller kvantiteten i kildedokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="5d452-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="5d452-121">Du kan finde flere oplysninger under [Varestikprøver for kvalitetsstyring](quality-item-sampling.md).</span><span class="sxs-lookup"><span data-stu-id="5d452-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="5d452-122">For en given virksomhedsproces identificerer kvalitetstilknytningsposten den hændelse og de betingelser, som en kvalitetsordre genereres for.</span><span class="sxs-lookup"><span data-stu-id="5d452-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="5d452-123">Betingelserne kan være specifikke for et sted eller en juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="5d452-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="5d452-124">En kvalitetsordre, der involverer destruktive prøvninger, kan kun oprettes, når der findes en disponible lagerbeholdning for hændelsen.</span><span class="sxs-lookup"><span data-stu-id="5d452-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="5d452-125">Du kan arbejde med kvalitetstilknytninger ved at gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Kvalitetstilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="5d452-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="5d452-126">Følgende eksempler viser, hvordan en kvalitetstilknytningspost defineres for variationerne i de enkelte virksomhedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="5d452-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="5d452-127">Eksemplerne vises også i følgende tabel som en oversigt over de hændelser og betingelser, der er defineret af en kvalitetstilknytningspost.</span><span class="sxs-lookup"><span data-stu-id="5d452-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5d452-128">Referencetype</span><span class="sxs-lookup"><span data-stu-id="5d452-128">Reference type</span></span></th>
<th><span data-ttu-id="5d452-129">Hændelsestype</span><span class="sxs-lookup"><span data-stu-id="5d452-129">Event type</span></span></th>
<th><span data-ttu-id="5d452-130">Udførelse</span><span class="sxs-lookup"><span data-stu-id="5d452-130">Execution</span></span></th>
<th><span data-ttu-id="5d452-131">Hændelsesspærring</span><span class="sxs-lookup"><span data-stu-id="5d452-131">Event blocking</span></span></th>
<th><span data-ttu-id="5d452-132">Dokumentreference</span><span class="sxs-lookup"><span data-stu-id="5d452-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5d452-133">Lager</span><span class="sxs-lookup"><span data-stu-id="5d452-133">Inventory</span></span></td>
<td><span data-ttu-id="5d452-134">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5d452-134">Not applicable</span></span></td>
<td><span data-ttu-id="5d452-135">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5d452-135">Not applicable</span></span></td>
<td><span data-ttu-id="5d452-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="5d452-136">None</span></span></td>
<td><span data-ttu-id="5d452-137">Alle</span><span class="sxs-lookup"><span data-stu-id="5d452-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="5d452-138">Salg</span><span class="sxs-lookup"><span data-stu-id="5d452-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="5d452-139">Plukproces er planlagt</span><span class="sxs-lookup"><span data-stu-id="5d452-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="5d452-140">Før</span><span class="sxs-lookup"><span data-stu-id="5d452-140">Before</span></span></td>
<td><span data-ttu-id="5d452-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="5d452-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="5d452-142">Bestemt id, gruppe eller kun alle</span><span class="sxs-lookup"><span data-stu-id="5d452-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-143">Plukproces</span><span class="sxs-lookup"><span data-stu-id="5d452-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-144">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="5d452-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-145">Faktura</span><span class="sxs-lookup"><span data-stu-id="5d452-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5d452-146">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="5d452-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="5d452-147">Før</span><span class="sxs-lookup"><span data-stu-id="5d452-147">Before</span></span></td>
<td><span data-ttu-id="5d452-148">Ingen</span><span class="sxs-lookup"><span data-stu-id="5d452-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-149">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="5d452-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-150">Faktura</span><span class="sxs-lookup"><span data-stu-id="5d452-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="5d452-151">Indkøb</span><span class="sxs-lookup"><span data-stu-id="5d452-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="5d452-152">Tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="5d452-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="5d452-153">Før</span><span class="sxs-lookup"><span data-stu-id="5d452-153">Before</span></span></td>
<td><span data-ttu-id="5d452-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="5d452-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-155">Tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="5d452-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-156">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="5d452-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-157">Faktura</span><span class="sxs-lookup"><span data-stu-id="5d452-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5d452-158">Efter</span><span class="sxs-lookup"><span data-stu-id="5d452-158">After</span></span></td>
<td><span data-ttu-id="5d452-159">Ingen</span><span class="sxs-lookup"><span data-stu-id="5d452-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-160">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="5d452-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-161">Faktura</span><span class="sxs-lookup"><span data-stu-id="5d452-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5d452-162">Registrering</span><span class="sxs-lookup"><span data-stu-id="5d452-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="5d452-163">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5d452-163">Not applicable</span></span></td>
<td><span data-ttu-id="5d452-164">Ingen</span><span class="sxs-lookup"><span data-stu-id="5d452-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-165">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="5d452-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-166">Faktura</span><span class="sxs-lookup"><span data-stu-id="5d452-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5d452-167">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="5d452-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="5d452-168">Før</span><span class="sxs-lookup"><span data-stu-id="5d452-168">Before</span></span></td>
<td><span data-ttu-id="5d452-169">Ingen</span><span class="sxs-lookup"><span data-stu-id="5d452-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-170">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="5d452-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-171">Faktura</span><span class="sxs-lookup"><span data-stu-id="5d452-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5d452-172">Efter</span><span class="sxs-lookup"><span data-stu-id="5d452-172">After</span></span></td>
<td><span data-ttu-id="5d452-173">Ingen</span><span class="sxs-lookup"><span data-stu-id="5d452-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-174">Faktura</span><span class="sxs-lookup"><span data-stu-id="5d452-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="5d452-175">Produktion</span><span class="sxs-lookup"><span data-stu-id="5d452-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="5d452-176">Registrering</span><span class="sxs-lookup"><span data-stu-id="5d452-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="5d452-177">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5d452-177">Not applicable</span></span></td>
<td><span data-ttu-id="5d452-178">Ingen</span><span class="sxs-lookup"><span data-stu-id="5d452-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="5d452-179">Alle</span><span class="sxs-lookup"><span data-stu-id="5d452-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-180">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="5d452-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-181">Afslut</span><span class="sxs-lookup"><span data-stu-id="5d452-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5d452-182">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="5d452-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="5d452-183">Før</span><span class="sxs-lookup"><span data-stu-id="5d452-183">Before</span></span></td>
<td><span data-ttu-id="5d452-184">Ingen</span><span class="sxs-lookup"><span data-stu-id="5d452-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-185">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="5d452-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-186">Afslut</span><span class="sxs-lookup"><span data-stu-id="5d452-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5d452-187">Efter</span><span class="sxs-lookup"><span data-stu-id="5d452-187">After</span></span></td>
<td><span data-ttu-id="5d452-188">Ingen</span><span class="sxs-lookup"><span data-stu-id="5d452-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-189">Afslut</span><span class="sxs-lookup"><span data-stu-id="5d452-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="5d452-190">Karantæne</span><span class="sxs-lookup"><span data-stu-id="5d452-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="5d452-191">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="5d452-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="5d452-192">Før</span><span class="sxs-lookup"><span data-stu-id="5d452-192">Before</span></span></td>
<td><span data-ttu-id="5d452-193">Færdigmeld</span><span class="sxs-lookup"><span data-stu-id="5d452-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-194">Afslut</span><span class="sxs-lookup"><span data-stu-id="5d452-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-195">Efter</span><span class="sxs-lookup"><span data-stu-id="5d452-195">After</span></span></td>
<td><span data-ttu-id="5d452-196">Afslut</span><span class="sxs-lookup"><span data-stu-id="5d452-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-197">Afslut</span><span class="sxs-lookup"><span data-stu-id="5d452-197">End</span></span></td>
<td><span data-ttu-id="5d452-198">Før</span><span class="sxs-lookup"><span data-stu-id="5d452-198">Before</span></span></td>
<td><span data-ttu-id="5d452-199">Afslut</span><span class="sxs-lookup"><span data-stu-id="5d452-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5d452-200">Ruteoperation</span><span class="sxs-lookup"><span data-stu-id="5d452-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="5d452-201">Færdigmelding</span><span class="sxs-lookup"><span data-stu-id="5d452-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="5d452-202">Før</span><span class="sxs-lookup"><span data-stu-id="5d452-202">Before</span></span></td>
<td><span data-ttu-id="5d452-203">None</span><span class="sxs-lookup"><span data-stu-id="5d452-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="5d452-204">Specifik Id, Gruppe eller Alle, og specifik Ressource, Gruppe eller Alle</span><span class="sxs-lookup"><span data-stu-id="5d452-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-205">Færdigmelding</span><span class="sxs-lookup"><span data-stu-id="5d452-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-206">Efter</span><span class="sxs-lookup"><span data-stu-id="5d452-206">After</span></span></td>
<td><span data-ttu-id="5d452-207">None</span><span class="sxs-lookup"><span data-stu-id="5d452-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5d452-208">Produktion af samprodukter</span><span class="sxs-lookup"><span data-stu-id="5d452-208">Co-product production</span></span></td>
<td><span data-ttu-id="5d452-209">Registrering</span><span class="sxs-lookup"><span data-stu-id="5d452-209">Registration</span></span></td>
<td><span data-ttu-id="5d452-210">Ikke anvendelig</span><span class="sxs-lookup"><span data-stu-id="5d452-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5d452-211">None</span><span class="sxs-lookup"><span data-stu-id="5d452-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="5d452-212">Alt</span><span class="sxs-lookup"><span data-stu-id="5d452-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5d452-213">Færdigmelding</span><span class="sxs-lookup"><span data-stu-id="5d452-213">Report as finished</span></span></td>
<td><span data-ttu-id="5d452-214">Før</span><span class="sxs-lookup"><span data-stu-id="5d452-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-215">Efter</span><span class="sxs-lookup"><span data-stu-id="5d452-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5d452-216">Funktionen *Kvalitetsstyring for lagerstedsprocesser* føjer funktioner til behandlingen af kvalitetsordrer for produktion, hvor feltet **Hændelsestype** er angivet til *Færdigmelding* og feltet **Udførelse** er angivet til *Efter*, og til køb, hvor feltet **Hændelsestype** er angivet til *Registrering*.</span><span class="sxs-lookup"><span data-stu-id="5d452-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="5d452-217">Du kan finde flere oplysninger i [Kvalitetsstyring for lagerstedsprocesser](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="5d452-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="5d452-218">Tabellen nedenfor indeholder flere oplysninger om, hvordan kvalitetsordrer kan oprettes for bestemte typer processer.</span><span class="sxs-lookup"><span data-stu-id="5d452-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="5d452-219">Procestype</span><span class="sxs-lookup"><span data-stu-id="5d452-219">Type of process</span></span></th>
<th><span data-ttu-id="5d452-220">Når kvalitetsordrer kan genereres automatisk</span><span class="sxs-lookup"><span data-stu-id="5d452-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="5d452-221">Når kvalitetsordrer kan genereres, hvis destruktiv prøvning er påkrævet</span><span class="sxs-lookup"><span data-stu-id="5d452-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="5d452-222">Betingelsesoplysninger</span><span class="sxs-lookup"><span data-stu-id="5d452-222">Condition information</span></span></th>
<th><span data-ttu-id="5d452-223">Manuel oprettelse af oplysninger</span><span class="sxs-lookup"><span data-stu-id="5d452-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5d452-224">Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="5d452-224">Purchase order</span></span></td>
<td><span data-ttu-id="5d452-225">Før eller efter en tilgangsliste eller produktkvittering for det materiale, der er modtaget, bogføres</span><span class="sxs-lookup"><span data-stu-id="5d452-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="5d452-226">Efter produktkvitteringen for det materiale, der er modtaget, bogføres, da materialet skal være tilgængelig til destruktiv prøvning</span><span class="sxs-lookup"><span data-stu-id="5d452-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="5d452-227">Behovet for en kvalitetsordre kan afhænge af en specifik lokation, vare eller leverandør eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="5d452-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5d452-228">En manuelt oprettet kvalitetsordre, der refererer til en indkøbsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="5d452-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-229">Karantæneordre</span><span class="sxs-lookup"><span data-stu-id="5d452-229">Quarantine order</span></span></td>
<td><span data-ttu-id="5d452-230">Før eller efter karantæneordren rapporteres som færdigmeldt eller afsluttet</span><span class="sxs-lookup"><span data-stu-id="5d452-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="5d452-231">Kvalitetsordrer, der kræver destruktive test, kan ikke genereres.</span><span class="sxs-lookup"><span data-stu-id="5d452-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="5d452-232">Det antages, at funktionen til karantæneordrer håndterer bortskaffelsen af det materiale, der skal destrueres.</span><span class="sxs-lookup"><span data-stu-id="5d452-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="5d452-233">Behovet for en kvalitetsordre kan afhænge af en specifik lokation, vare eller leverandør eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="5d452-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5d452-234">En manuelt oprettet kvalitetsordre, der refererer til en karantæneordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="5d452-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-235">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="5d452-235">Sales order</span></span></td>
<td><span data-ttu-id="5d452-236">Før en planlagt plukproces eller opdatering af følgesedlen for de varer, der skal leveres</span><span class="sxs-lookup"><span data-stu-id="5d452-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="5d452-237">På alle trin</span><span class="sxs-lookup"><span data-stu-id="5d452-237">At any step</span></span></td>
<td><span data-ttu-id="5d452-238">Behovet for en kvalitetsordre kan afhænge af en specifik lokation, vare eller kunde eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="5d452-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5d452-239">En manuelt oprettet kvalitetsordre, der refererer til en salgsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="5d452-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-240">Produktionsordre</span><span class="sxs-lookup"><span data-stu-id="5d452-240">Production order</span></span></td>
<td><span data-ttu-id="5d452-241">Før eller efter det færdigmeldte antal for produktionsordren er rapporteret</span><span class="sxs-lookup"><span data-stu-id="5d452-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="5d452-242">Efter det færdigmeldte antal for produktionsordren er rapporteret</span><span class="sxs-lookup"><span data-stu-id="5d452-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="5d452-243">Behovet for en kvalitetsordre kan afhænge af en specifik lokation eller vare eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="5d452-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5d452-244">En manuelt oprettet kvalitetsordre, der refererer til en produktionsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="5d452-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-245">Produktionsordre, der har en ruteoperation</span><span class="sxs-lookup"><span data-stu-id="5d452-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="5d452-246">Før eller efter rapporten er færdigmeldt for en operation</span><span class="sxs-lookup"><span data-stu-id="5d452-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="5d452-247">Efter færdigrapportering af produktionen for den sidste operation</span><span class="sxs-lookup"><span data-stu-id="5d452-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="5d452-248">Behovet for en kvalitetsordre kan afhænge af en specifik lokation, vare eller operationsressource eller en kombination af disse forhold.</span><span class="sxs-lookup"><span data-stu-id="5d452-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5d452-249">En manuelt oprettet kvalitetsordre, der refererer til en ruteoperation, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</span><span class="sxs-lookup"><span data-stu-id="5d452-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5d452-250">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="5d452-250">Inventory</span></span></td>
<td><span data-ttu-id="5d452-251">En kvalitetsordre kan ikke genereres automatisk for en transaktion i en lagerkladde eller for flytteordretransaktioner.</span><span class="sxs-lookup"><span data-stu-id="5d452-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="5d452-252">En kvalitetsordre skal oprettes manuelt for en vares lagerantal.</span><span class="sxs-lookup"><span data-stu-id="5d452-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="5d452-253">Fysisk disponibel lagerbeholdning er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="5d452-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="5d452-254">Eksempler på automatisk oprettelse af kvalitetsordrer</span><span class="sxs-lookup"><span data-stu-id="5d452-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="5d452-255">Køb</span><span class="sxs-lookup"><span data-stu-id="5d452-255">Purchasing</span></span>

<span data-ttu-id="5d452-256">Hvis du i forbindelse med indkøb angiver feltet **Hændelsestype** til *Produktkvittering* og feltet **Udførelse** til *Efter* på siden **Kvalitetstilknytninger**, får du følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="5d452-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="5d452-257">Hvis indstillingen **Pr. opdateret antal** er angivet til *Ja*, genereres der en kvalitetsordre for hver kvittering i forhold til indkøbsordren baseret på det modtagne antal og indstillinger i stikprøven af vare.</span><span class="sxs-lookup"><span data-stu-id="5d452-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="5d452-258">Hver gang der modtages et antal på indkøbsordren, oprettes der nye kvalitetsordrer ud fra det nye antal, der er modtaget.</span><span class="sxs-lookup"><span data-stu-id="5d452-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="5d452-259">Hvis indstillingen **Pr. opdateret antal** er angivet til *Nej*, genereres der en kvalitetsordre for den første kvittering i forhold til indkøbsordren baseret på det modtagne antal.</span><span class="sxs-lookup"><span data-stu-id="5d452-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="5d452-260">Derudover oprettes en eller flere kvalitetsordrer ud fra det resterende antal afhængigt af sporingsdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="5d452-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="5d452-261">Kvalitetsordrer genereres ikke for efterfølgende kvitteringer i forhold til indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="5d452-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="5d452-262">Produktion</span><span class="sxs-lookup"><span data-stu-id="5d452-262">Production</span></span>

<span data-ttu-id="5d452-263">Hvis du i forbindelse med produktion angiver feltet **Hændelsestype** til *Færdigmelding* og feltet **Udførelse** til *Efter* på siden **Kvalitetstilknytninger**, får du følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="5d452-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="5d452-264">Hvis indstillingen **Pr. opdateret antal** er angivet til *Ja*, genereres der en kvalitetsordre baseret på hvert færdige antal og indstillinger i stikprøven af vare.</span><span class="sxs-lookup"><span data-stu-id="5d452-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="5d452-265">Hver gang et antal færdigmeldes på indkøbsordren, genereres der nye kvalitetsordrer ud fra det nye antal færdigmeldte varer.</span><span class="sxs-lookup"><span data-stu-id="5d452-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="5d452-266">Denne genereringslogik stemmer overens med indkøb.</span><span class="sxs-lookup"><span data-stu-id="5d452-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="5d452-267">Hvis indstillingen **Pr. opdateret antal** er angivet til *Nej*, genereres der en kvalitetsordre, første gang et antal færdigmeldes, baseret på det færdige antal.</span><span class="sxs-lookup"><span data-stu-id="5d452-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="5d452-268">Derudover oprettes en eller flere kvalitetsordrer ud fra det resterende antal afhængigt af sporingsdimensionerne for stikprøven af varen.</span><span class="sxs-lookup"><span data-stu-id="5d452-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="5d452-269">Kvalitetsordrer genereres ikke for efterfølgende færdige antal.</span><span class="sxs-lookup"><span data-stu-id="5d452-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5d452-270">Kvalitetsspecifikation</span><span class="sxs-lookup"><span data-stu-id="5d452-270">Quality specification</span></span></th>
<th><span data-ttu-id="5d452-271">Pr. opdateret antal</span><span class="sxs-lookup"><span data-stu-id="5d452-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="5d452-272">Pr. sporingsdimension</span><span class="sxs-lookup"><span data-stu-id="5d452-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="5d452-273">Resultat</span><span class="sxs-lookup"><span data-stu-id="5d452-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5d452-274">Procent: 10 %</span><span class="sxs-lookup"><span data-stu-id="5d452-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="5d452-275">Ja</span><span class="sxs-lookup"><span data-stu-id="5d452-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="5d452-276">Batchnummer: Nej</span><span class="sxs-lookup"><span data-stu-id="5d452-276">Batch number: No</span></span></p>
<p><span data-ttu-id="5d452-277">Serienummer: Nej</span><span class="sxs-lookup"><span data-stu-id="5d452-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="5d452-278">Ordreantal: 100</span><span class="sxs-lookup"><span data-stu-id="5d452-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="5d452-279">Færdigmelding for 30</span><span class="sxs-lookup"><span data-stu-id="5d452-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="5d452-280">Kvalitetsordre 1 for 3 (10 % af 30)</span><span class="sxs-lookup"><span data-stu-id="5d452-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5d452-281">Færdigmelding for 70</span><span class="sxs-lookup"><span data-stu-id="5d452-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="5d452-282">Kvalitetsordre. 2 for 7 (10 % af det resterende ordreantal, hvilket er lig med 70 i dette tilfælde)</span><span class="sxs-lookup"><span data-stu-id="5d452-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="5d452-283">Fast antal: 1</span><span class="sxs-lookup"><span data-stu-id="5d452-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="5d452-284">Ingen</span><span class="sxs-lookup"><span data-stu-id="5d452-284">No</span></span></td>
<td>
<p><span data-ttu-id="5d452-285">Batchnummer: Nej</span><span class="sxs-lookup"><span data-stu-id="5d452-285">Batch number: No</span></span></p>
<p><span data-ttu-id="5d452-286">Serienummer: Nej</span><span class="sxs-lookup"><span data-stu-id="5d452-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="5d452-287">Ordreantal: 100</span><span class="sxs-lookup"><span data-stu-id="5d452-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="5d452-288">Færdigmelding for 30</span><span class="sxs-lookup"><span data-stu-id="5d452-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="5d452-289">Kvalitetsordre 1 for 1 (for det første færdigmeldte antal, der har en fast værdi af 1)</span><span class="sxs-lookup"><span data-stu-id="5d452-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="5d452-290">Kvalitetsordre 2 for 1 (for det resterende antal, der stadig har en fast værdi af 1)</span><span class="sxs-lookup"><span data-stu-id="5d452-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5d452-291">Færdigmelding for 10</span><span class="sxs-lookup"><span data-stu-id="5d452-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="5d452-292">Der oprettes ingen kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="5d452-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5d452-293">Færdigmelding for 60</span><span class="sxs-lookup"><span data-stu-id="5d452-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="5d452-294">Der oprettes ingen kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="5d452-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="5d452-295">Fast antal: 1</span><span class="sxs-lookup"><span data-stu-id="5d452-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="5d452-296">Ja</span><span class="sxs-lookup"><span data-stu-id="5d452-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="5d452-297">Batchnummer: Ja</span><span class="sxs-lookup"><span data-stu-id="5d452-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="5d452-298">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="5d452-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="5d452-299">Ordreantal: 10</span><span class="sxs-lookup"><span data-stu-id="5d452-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="5d452-300">Færdigmelding for 3: 1 for batchnummer b1, serienummer s1, 1 for batchnummer b2, serienummer s2 og 1 for batchnummer b3, serienummer s3</span><span class="sxs-lookup"><span data-stu-id="5d452-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="5d452-301">Kvalitetsordre 1 for 1 af batchnummer b1, serienummer s1</span><span class="sxs-lookup"><span data-stu-id="5d452-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="5d452-302">Kvalitetsordre 2 for 1 af batchnummer b2, serienummer s2</span><span class="sxs-lookup"><span data-stu-id="5d452-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="5d452-303">Kvalitetsordre 3 for 1 af batchnummer b3, serienummer s3</span><span class="sxs-lookup"><span data-stu-id="5d452-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5d452-304">Færdigmelding for 2: 1 for batchnummer b4, serienummer s4 og 1 for batchnummer b5, serienummer s5</span><span class="sxs-lookup"><span data-stu-id="5d452-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="5d452-305">Kvalitetsordre 4 for 1 af batchnummer b4, serienummer s4</span><span class="sxs-lookup"><span data-stu-id="5d452-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="5d452-306">Kvalitetsordre 5 for 1 af batchnummer b5, serienummer s5</span><span class="sxs-lookup"><span data-stu-id="5d452-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="5d452-307"><strong>Bemærk:</strong> Batchen kan genbruges.</span><span class="sxs-lookup"><span data-stu-id="5d452-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="5d452-308">Fast antal: 2</span><span class="sxs-lookup"><span data-stu-id="5d452-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="5d452-309">Ingen</span><span class="sxs-lookup"><span data-stu-id="5d452-309">No</span></span></td>
<td>
<p><span data-ttu-id="5d452-310">Batchnummer: Ja</span><span class="sxs-lookup"><span data-stu-id="5d452-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="5d452-311">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="5d452-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="5d452-312">Ordreantal: 10</span><span class="sxs-lookup"><span data-stu-id="5d452-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="5d452-313">Færdigmelding for 4: 1 for batchnummer b1, serienummer s1, 1 for batchnummer b2, serienummer s2, 1 for batchnummer b3, serienummer s3 og 1 for batchnummer b4, serienummer 4</span><span class="sxs-lookup"><span data-stu-id="5d452-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="5d452-314">Kvalitetsordre 1 for 1 af batchnummer b1, serienummer s1</span><span class="sxs-lookup"><span data-stu-id="5d452-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="5d452-315">Kvalitetsordre 2 for 1 af batchnummer b2, serienummer s2</span><span class="sxs-lookup"><span data-stu-id="5d452-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="5d452-316">Kvalitetsordre 3 for 1 af batchnummer b3, serienummer s3</span><span class="sxs-lookup"><span data-stu-id="5d452-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="5d452-317">Kvalitetsordre 4 for 1 af batchnummer b4, serienummer s4</span><span class="sxs-lookup"><span data-stu-id="5d452-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="5d452-318">Kvalitetsordre 5 for 2, uden en reference til et batchnummer eller et serienummer</span><span class="sxs-lookup"><span data-stu-id="5d452-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5d452-319">Færdigmelding for 6: 1 for batchnummer b5, serienummer s5, 1 for batchnummer b6, serienummer s6, 1 for batchnummer b7, serienummer s7, 1 for batchnummer b8, serienummer s8, 1 for batchnummer b9, serienummer s9 og 1 for batchnummer b10, serienummer s10</span><span class="sxs-lookup"><span data-stu-id="5d452-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="5d452-320">Der oprettes ingen kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="5d452-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="5d452-321">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5d452-321">Additional resources</span></span>

- [<span data-ttu-id="5d452-322">Processer for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="5d452-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="5d452-323">Aktivere styring af kvalitet og uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="5d452-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="5d452-324">Kvalitetsstyring for lagerstedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="5d452-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
