---
title: "Demoskærmlayout til data i Retail Modern POS og Cloud POS"
description: "Dette emne indeholder oplysninger om de skærmlayout, der følger med demodatasæt til POS-oplevelserne i Microsoft Dynamics 365 for Retail."
author: zlinster
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: zlinster
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 41930e89a7cae5cdb84e728da47de3bc5de312ca
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---

# <a name="demo-data-screen-layouts-in-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="af18d-103">Demoskærmlayout til data i Retail Modern POS og Cloud POS</span><span class="sxs-lookup"><span data-stu-id="af18d-103">Demo data screen layouts in Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="af18d-104">Dette emne indeholder oplysninger om de skærmlayout, der følger med demodatasæt til POS-oplevelserne i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="af18d-104">This topic provides information about the screen layouts that are included with the demo data set for the point of sale (POS) experiences in Microsoft Dynamics 365 for Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="af18d-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="af18d-105">Overview</span></span>

<span data-ttu-id="af18d-106">De eksempelskærmlayouts, der følger med Retail-demodata, leverer indhold, der er optimeret til forskellige detailsegmenter, butiksmedarbejderroller og enheder.</span><span class="sxs-lookup"><span data-stu-id="af18d-106">The sample screen layouts that are included with Retail demo data provide content that is optimized for various retail segments, store worker roles, and devices.</span></span> <span data-ttu-id="af18d-107">Et enkelt layout kan indeholde flere layoutstørrelser og kombinationer af knapmatricer for at sikre dækning, når butiksmedarbejderne flytter mellem enheder og stationer.</span><span class="sxs-lookup"><span data-stu-id="af18d-107">A single layout can contain several layout sizes and combinations of button grids, to help ensure coverage as store workers move between devices and stations.</span></span> <span data-ttu-id="af18d-108">I dette emne beskrives forskellene mellem disse layouts, de operationer, de indeholder, og den samlede oplevelse, de leverer.</span><span class="sxs-lookup"><span data-stu-id="af18d-108">This topic highlights the differences between these layouts, the operations that they provide, and the overall experiences that they deliver.</span></span>

![Layouts til demodata på tværs af enheder](../retail/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a><span data-ttu-id="af18d-110">Anatomi af et skærmlayout-id</span><span class="sxs-lookup"><span data-stu-id="af18d-110">Anatomy of a screen layout ID</span></span>

<span data-ttu-id="af18d-111">For at finde skærmlayouts i Retail, skal du gå til **Retail** > **Konfiguration af kanal** > **POS-opsætning** > **POS** > **Skærmlayout**.</span><span class="sxs-lookup"><span data-stu-id="af18d-111">To find screen layouts in Retail, go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>

![Side til skærmlayouts i Retail](../retail/media/demo-screen-layouts-fig-2-1.png)

<span data-ttu-id="af18d-113">Skærmlayout-id'er må være på op til 10 tegn.</span><span class="sxs-lookup"><span data-stu-id="af18d-113">Screen layout IDs can have a maximum of 10 characters.</span></span> <span data-ttu-id="af18d-114">Id'et er en streng, der består af tre dele af oplysninger i følgende rækkefølge:</span><span class="sxs-lookup"><span data-stu-id="af18d-114">The ID is a string that consists of three pieces of information, in this order:</span></span>

1. <span data-ttu-id="af18d-115">Regnskab</span><span class="sxs-lookup"><span data-stu-id="af18d-115">Company</span></span>
2. <span data-ttu-id="af18d-116">Layoutversion</span><span class="sxs-lookup"><span data-stu-id="af18d-116">Layout version</span></span>
3. <span data-ttu-id="af18d-117">Karakter</span><span class="sxs-lookup"><span data-stu-id="af18d-117">Persona</span></span>

### <a name="company"></a><span data-ttu-id="af18d-118">Regnskab</span><span class="sxs-lookup"><span data-stu-id="af18d-118">Company</span></span>

| <span data-ttu-id="af18d-119">Bogstav</span><span class="sxs-lookup"><span data-stu-id="af18d-119">Letter</span></span> | <span data-ttu-id="af18d-120">Regnskab</span><span class="sxs-lookup"><span data-stu-id="af18d-120">Company</span></span>         |
|--------|-----------------|
| <span data-ttu-id="af18d-121">T</span><span class="sxs-lookup"><span data-stu-id="af18d-121">A</span></span>      | <span data-ttu-id="af18d-122">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="af18d-122">Adventure Works</span></span> |
| <span data-ttu-id="af18d-123">F</span><span class="sxs-lookup"><span data-stu-id="af18d-123">F</span></span>      | <span data-ttu-id="af18d-124">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="af18d-124">Fabrikam</span></span>        |
| <span data-ttu-id="af18d-125">A</span><span class="sxs-lookup"><span data-stu-id="af18d-125">C</span></span>      | <span data-ttu-id="af18d-126">Contoso</span><span class="sxs-lookup"><span data-stu-id="af18d-126">Contoso</span></span>         |

### <a name="layout-version"></a><span data-ttu-id="af18d-127">Layoutversion</span><span class="sxs-lookup"><span data-stu-id="af18d-127">Layout version</span></span>

| <span data-ttu-id="af18d-128">Versionsnummer</span><span class="sxs-lookup"><span data-stu-id="af18d-128">Version number</span></span> | <span data-ttu-id="af18d-129">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="af18d-129">Description</span></span>                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="af18d-130">3</span><span class="sxs-lookup"><span data-stu-id="af18d-130">3</span></span>              | <span data-ttu-id="af18d-131">Den grundlæggende version, der understøtter flere skærmstørrelser til forskellige enheder og størrelsesforhold</span><span class="sxs-lookup"><span data-stu-id="af18d-131">The base version that supports multiple screen sizes for various devices and aspect ratios</span></span> |
| <span data-ttu-id="af18d-132">3.1</span><span class="sxs-lookup"><span data-stu-id="af18d-132">3.1</span></span>            | <span data-ttu-id="af18d-133">Den grundlæggende version, der har yderligere understøttelse af panelet **Anbefalede produkter**</span><span class="sxs-lookup"><span data-stu-id="af18d-133">The base version that has additional support for the **Recommended products** panel</span></span>        |

### <a name="persona"></a><span data-ttu-id="af18d-134">Karakter</span><span class="sxs-lookup"><span data-stu-id="af18d-134">Persona</span></span>

| <span data-ttu-id="af18d-135">Forkortelse</span><span class="sxs-lookup"><span data-stu-id="af18d-135">Abbreviation</span></span> | <span data-ttu-id="af18d-136">Karakter</span><span class="sxs-lookup"><span data-stu-id="af18d-136">Persona</span></span>       | <span data-ttu-id="af18d-137">Indhold</span><span class="sxs-lookup"><span data-stu-id="af18d-137">Contents</span></span> |
|--------------|---------------|----------|
| <span data-ttu-id="af18d-138">CSH</span><span class="sxs-lookup"><span data-stu-id="af18d-138">CSH</span></span>          | <span data-ttu-id="af18d-139">Kasseassistent</span><span class="sxs-lookup"><span data-stu-id="af18d-139">Cashier</span></span>       | <span data-ttu-id="af18d-140">Kasserer-layouts omfatter alle transaktionsrelaterede handlinger, f.eks. kundeordrer, returneringer, rabatter, annulleringer og gavekort.</span><span class="sxs-lookup"><span data-stu-id="af18d-140">Cashier layouts include all transaction-related operations, such as customer orders, returns, discounts, voids, and gift cards.</span></span> <span data-ttu-id="af18d-141">Disse layout omfatter også de daglige opgaver til lagerstyring, f.eks. pristjek, lageropslag og lageroptællinger.</span><span class="sxs-lookup"><span data-stu-id="af18d-141">These layouts also include daily tasks for inventory management, such price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="af18d-142">Der er også grundlæggende styring af skift med startbeløb, afbrydelse af skift og tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="af18d-142">Basic shift management is also provided for start amounts, suspending shifts, and time clock.</span></span> |
| <span data-ttu-id="af18d-143">MGR</span><span class="sxs-lookup"><span data-stu-id="af18d-143">MGR</span></span>          | <span data-ttu-id="af18d-144">Butikschef</span><span class="sxs-lookup"><span data-stu-id="af18d-144">Store Manager</span></span> | <span data-ttu-id="af18d-145">Layouts til butikschef omfatter alle posteringsrelaterede operationer, der findes i kassererens layout, men omfatte også tilsidesættelser af moms.</span><span class="sxs-lookup"><span data-stu-id="af18d-145">Store Manager layouts include all transaction-related operations that are found in the Cashier layouts but also include tax overrides.</span></span> <span data-ttu-id="af18d-146">Disse layout omfatter også de daglige opgaver til lagerstyring, f.eks. pristjek, lageropslag og lageroptællinger.</span><span class="sxs-lookup"><span data-stu-id="af18d-146">These layouts also include daily tasks for inventory management, such as price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="af18d-147">Styring af skift er medtaget for at starte, afbryde og lukke skift.</span><span class="sxs-lookup"><span data-stu-id="af18d-147">Shift management is provided for starting, suspending, and closing shifts.</span></span> <span data-ttu-id="af18d-148">Desuden omfatter layouts kasseskuffeoperationer for posteringer, fjernelse, kasseoptællinger og aflevering i pengeskab og bank.</span><span class="sxs-lookup"><span data-stu-id="af18d-148">Additionally, the layouts include drawer operations for entries, removals, tender declarations, and safe and bank drops.</span></span> <span data-ttu-id="af18d-149">Endelig omfatter disse layouts adgangen til ydeevnerapporter og mulighed for at udskrive X- og / Z-rapporter.</span><span class="sxs-lookup"><span data-stu-id="af18d-149">Finally, these layouts include access to performance reports, and enable X and Z reports to be printed.</span></span> |
| <span data-ttu-id="af18d-150">STK</span><span class="sxs-lookup"><span data-stu-id="af18d-150">STK</span></span>          | <span data-ttu-id="af18d-151">Lagermedarbejder</span><span class="sxs-lookup"><span data-stu-id="af18d-151">Stock Clerk</span></span>   | <span data-ttu-id="af18d-152">Layouts til lagermedarbejder er optimeret til lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="af18d-152">Stock Clerk layouts are optimized for inventory management.</span></span> <span data-ttu-id="af18d-153">De omfatter adgangen til de daglige opgaver til pristjek, lageropslag, pluk og tilgang, statusoptællinger og adskillelse af sæt.</span><span class="sxs-lookup"><span data-stu-id="af18d-153">They include access to daily tasks for price checks, inventory lookups, picking and receiving, stock counts, and kit disassembly.</span></span> <span data-ttu-id="af18d-154">Disse layouts indeholder også grundlæggende operationer for skift, f.eks. tidsregistrering og afbrydelse af skift.</span><span class="sxs-lookup"><span data-stu-id="af18d-154">These layouts also provide basic shift operations for time clock and suspending shifts.</span></span> <span data-ttu-id="af18d-155">Selvom disse layouts primært er beregnet til back-office-opgaver, har lagermedarbejdere de samme operationer som kasserere med hensyn til transaktionsskærmbilleder.</span><span class="sxs-lookup"><span data-stu-id="af18d-155">Although these layouts are intended mainly for back-office tasks, stock clerks have the same operations as cashiers for transaction screens.</span></span> |

### <a name="example-layout"></a><span data-ttu-id="af18d-156">Eksempellayout</span><span class="sxs-lookup"><span data-stu-id="af18d-156">Example layout</span></span>

<span data-ttu-id="af18d-157">Her er et eksempel på et skærmlayout-id for Fabrikam-virksomheden, layout version 3 og karakteren butikschef:</span><span class="sxs-lookup"><span data-stu-id="af18d-157">Here is an example of a screen layout ID for the Fabrikam company, layout version 3, and the Store Manager persona:</span></span>

<span data-ttu-id="af18d-158">F3MGR</span><span class="sxs-lookup"><span data-stu-id="af18d-158">F3MGR</span></span>

<span data-ttu-id="af18d-159">I følgende illustration vises et eksempel på velkomstskærmbilledet for en butikschef hos Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="af18d-159">The following illustration shows an example of the Welcome screen for a Fabrikam store manager.</span></span>

![Velkomstskærmbillede for Fabrikam-butikschefen](../retail/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a><span data-ttu-id="af18d-161">Layoutstørrelser</span><span class="sxs-lookup"><span data-stu-id="af18d-161">Layout sizes</span></span>

### <a name="full-vs-compact-layouts"></a><span data-ttu-id="af18d-162">Fuldstændige vs. kompakte layouts</span><span class="sxs-lookup"><span data-stu-id="af18d-162">Full vs. compact layouts</span></span>

<span data-ttu-id="af18d-163">Et skærmlayout kan indeholde konfigurationer for både fuldstændige og kompakte enheder.</span><span class="sxs-lookup"><span data-stu-id="af18d-163">A screen layout can have configurations for both full devices and compact devices.</span></span> <span data-ttu-id="af18d-164">Derfor kan en bruger blive knyttet til et enkelt skærmlayout, der fungerer på tværs af forskellige størrelser og formfaktorer i butikken.</span><span class="sxs-lookup"><span data-stu-id="af18d-164">Therefore, a user can be assigned to a single screen layout that will work across various sizes and form factors in the store.</span></span>

- <span data-ttu-id="af18d-165">**Moderne POS – Fuld** – Fulde layouts er typisk bedst til større skærme som pc-skærme eller tablets.</span><span class="sxs-lookup"><span data-stu-id="af18d-165">**Modern POS - Full** – Typically, full layouts are best used for larger displays, such as desktop computer monitors or tablets.</span></span> <span data-ttu-id="af18d-166">Brugere kan vælge de elementer på brugergrænsefladen, som layoutet omfatter, angive størrelsen på og placeringen af disse elementer og konfigurere deres detaljerede egenskaber.</span><span class="sxs-lookup"><span data-stu-id="af18d-166">Users can select the UI elements that the layout includes, specify the size and placement of those elements, and configure their detailed properties.</span></span> <span data-ttu-id="af18d-167">Fulde layouts understøtter både stående og liggende konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="af18d-167">Full layouts support both portrait and landscape configurations.</span></span>
- <span data-ttu-id="af18d-168">**Moderne POS - Kompakt** – Kompakte layouts er typisk bedst til telefoner eller små tablets.</span><span class="sxs-lookup"><span data-stu-id="af18d-168">**Modern POS - Compact** – Typically, compact layouts are best used for phones or small tablets.</span></span> <span data-ttu-id="af18d-169">Designmulighederne er begrænsede på kompakte enheder.</span><span class="sxs-lookup"><span data-stu-id="af18d-169">Design possibilities are limited for compact devices.</span></span> <span data-ttu-id="af18d-170">Brugerne kan konfigurere kolonnerne og felterne til kvitteringsruden og ruden med totaler.</span><span class="sxs-lookup"><span data-stu-id="af18d-170">Users can configure the columns and fields for the receipt pane and the totals pane.</span></span>

### <a name="screen-resolutions-that-are-provided"></a><span data-ttu-id="af18d-171">Skærmopløsninger, der følger</span><span class="sxs-lookup"><span data-stu-id="af18d-171">Screen resolutions that are provided</span></span>

<span data-ttu-id="af18d-172">Følgende tabel viser de layoutstørrelser, som findes til typiske skærmopløsninger.</span><span class="sxs-lookup"><span data-stu-id="af18d-172">The following table shows the layout sizes that are provided for typical screen resolutions.</span></span>

| <span data-ttu-id="af18d-173">Layouttype</span><span class="sxs-lookup"><span data-stu-id="af18d-173">Layout type</span></span> | <span data-ttu-id="af18d-174">Løsning</span><span class="sxs-lookup"><span data-stu-id="af18d-174">Resolution</span></span> | <span data-ttu-id="af18d-175">Størrelsesforhold</span><span class="sxs-lookup"><span data-stu-id="af18d-175">Aspect ratio</span></span> | <span data-ttu-id="af18d-176">Måldisplay</span><span class="sxs-lookup"><span data-stu-id="af18d-176">Target display</span></span>          |
|-------------|------------|--------------|-------------------------|
| <span data-ttu-id="af18d-177">Komprimer\*</span><span class="sxs-lookup"><span data-stu-id="af18d-177">Compact\*</span></span>   | <span data-ttu-id="af18d-178">480 × 853</span><span class="sxs-lookup"><span data-stu-id="af18d-178">480 × 853</span></span>  | <span data-ttu-id="af18d-179">16:9</span><span class="sxs-lookup"><span data-stu-id="af18d-179">16:9</span></span>         | <span data-ttu-id="af18d-180">Telefoner</span><span class="sxs-lookup"><span data-stu-id="af18d-180">Phones</span></span>                  |
| <span data-ttu-id="af18d-181">Fuld</span><span class="sxs-lookup"><span data-stu-id="af18d-181">Full</span></span>        | <span data-ttu-id="af18d-182">1024 × 768</span><span class="sxs-lookup"><span data-stu-id="af18d-182">1024 × 768</span></span> | <span data-ttu-id="af18d-183">4:3</span><span class="sxs-lookup"><span data-stu-id="af18d-183">4:3</span></span>          | <span data-ttu-id="af18d-184">Tablets</span><span class="sxs-lookup"><span data-stu-id="af18d-184">Tablets</span></span>                 |
| <span data-ttu-id="af18d-185">Fuld\*</span><span class="sxs-lookup"><span data-stu-id="af18d-185">Full\*</span></span>      | <span data-ttu-id="af18d-186">1280 × 720</span><span class="sxs-lookup"><span data-stu-id="af18d-186">1280 × 720</span></span> | <span data-ttu-id="af18d-187">16:9</span><span class="sxs-lookup"><span data-stu-id="af18d-187">16:9</span></span>         | <span data-ttu-id="af18d-188">Tablets</span><span class="sxs-lookup"><span data-stu-id="af18d-188">Tablets</span></span>                 |
| <span data-ttu-id="af18d-189">Fuld</span><span class="sxs-lookup"><span data-stu-id="af18d-189">Full</span></span>        | <span data-ttu-id="af18d-190">1366 × 768</span><span class="sxs-lookup"><span data-stu-id="af18d-190">1366 × 768</span></span> | <span data-ttu-id="af18d-191">16:9</span><span class="sxs-lookup"><span data-stu-id="af18d-191">16:9</span></span>         | <span data-ttu-id="af18d-192">Tablets, større skærme</span><span class="sxs-lookup"><span data-stu-id="af18d-192">Tablets, larger screens</span></span> |
| <span data-ttu-id="af18d-193">Fuld</span><span class="sxs-lookup"><span data-stu-id="af18d-193">Full</span></span>        | <span data-ttu-id="af18d-194">1440 × 960</span><span class="sxs-lookup"><span data-stu-id="af18d-194">1440 × 960</span></span> | <span data-ttu-id="af18d-195">3:2</span><span class="sxs-lookup"><span data-stu-id="af18d-195">3:2</span></span>          | <span data-ttu-id="af18d-196">Tablets, større skærme</span><span class="sxs-lookup"><span data-stu-id="af18d-196">Tablets, larger screens</span></span> |

<span data-ttu-id="af18d-197">\* Disse yderligere layoutstørrelser er kun tilgængelige i Adventure Works- og Fabrikam-layouts.</span><span class="sxs-lookup"><span data-stu-id="af18d-197">\* These additional layout sizes are available only in Adventure Works and Fabrikam layouts.</span></span>


>[!TIP]
> <span data-ttu-id="af18d-198">POS vælger automatisk layoutstørrelser, baseret på den nærmeste størrelse, der er tilgængelig for skærmopløsningen i det aktuelle appvindue.</span><span class="sxs-lookup"><span data-stu-id="af18d-198">POS automatically selects layout sizes, based on the closest size that is available for the screen resolution of the current app window.</span></span> <span data-ttu-id="af18d-199">Hvis du vil finde det skærmlayout-id og den layoutopløsning, der aktuelt bruges i Retail Modern POS (MPOS) eller Retail Cloud POS (CPOS), skal du åbne siden **Indstillinger** siden, og se i afsnittet **Sessionsoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="af18d-199">To find the screen layout ID and layout resolution that are currently used, in Retail Modern POS (MPOS) or Retail Cloud POS (CPOS), open the **Settings** page, and look in the **Session information** section.</span></span> <span data-ttu-id="af18d-200">Du kan også se den faktiske vinduesopløsning for dit aktuelle program eller browserramme.</span><span class="sxs-lookup"><span data-stu-id="af18d-200">You can also see the actual window resolution for your current application or browser frame.</span></span> <span data-ttu-id="af18d-201">Når du har disse oplysninger, du kan finde kilden til indholdet i layoutet i Retail ved at gå til **Konfiguration af kanal** > **POS-opsætning** > **POS** > **Skærmlayout**.</span><span class="sxs-lookup"><span data-stu-id="af18d-201">After you have this information, you can find the source of the layout content in Retail by going to **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>


![Skærmlayouts og layoutopløsninger/-størrelser i Retail og POS](../retail/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a><span data-ttu-id="af18d-203">Firmaer og brands</span><span class="sxs-lookup"><span data-stu-id="af18d-203">Companies and brands</span></span>

<span data-ttu-id="af18d-204">Hvert fiktivt firma henvender sig til en andet detailsegment og omfatter produktkataloger, som er tilpasset til virksomhedens marked.</span><span class="sxs-lookup"><span data-stu-id="af18d-204">Each fictitious company is targeted to a different retail segment and includes product catalogs that are tuned for the company's market.</span></span> <span data-ttu-id="af18d-205">Hver virksomhed har et entydigt visuelt brand, der følger med dets produkter.</span><span class="sxs-lookup"><span data-stu-id="af18d-205">Each company has a unique visual brand that accompanies its products.</span></span> <span data-ttu-id="af18d-206">Brandingelementerne omfatter fremhævelsesfarve, mørkt eller lyst tema og ledsagende billeder, der giver realistiske oplevelser.</span><span class="sxs-lookup"><span data-stu-id="af18d-206">Branding elements include the accent color, dark or light theme, and accompanying photographs that provide realistic experiences.</span></span>

### <a name="company-segment-and-visual-characteristics"></a><span data-ttu-id="af18d-207">Firmasegment og visuelle egenskaber</span><span class="sxs-lookup"><span data-stu-id="af18d-207">Company segment and visual characteristics</span></span>

| <span data-ttu-id="af18d-208">Regnskab</span><span class="sxs-lookup"><span data-stu-id="af18d-208">Company</span></span>         | <span data-ttu-id="af18d-209">Adresse</span><span class="sxs-lookup"><span data-stu-id="af18d-209">Location</span></span> | <span data-ttu-id="af18d-210">Segment</span><span class="sxs-lookup"><span data-stu-id="af18d-210">Segment</span></span>        | <span data-ttu-id="af18d-211">Markering</span><span class="sxs-lookup"><span data-stu-id="af18d-211">Accent</span></span> | <span data-ttu-id="af18d-212">Tema</span><span class="sxs-lookup"><span data-stu-id="af18d-212">Theme</span></span> |
|-----------------|----------|----------------|--------|-------|
| <span data-ttu-id="af18d-213">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="af18d-213">Adventure Works</span></span> | <span data-ttu-id="af18d-214">Seattle</span><span class="sxs-lookup"><span data-stu-id="af18d-214">Seattle</span></span>  | <span data-ttu-id="af18d-215">Sportsudstyr</span><span class="sxs-lookup"><span data-stu-id="af18d-215">Sporting Goods</span></span> | <span data-ttu-id="af18d-216">Blå</span><span class="sxs-lookup"><span data-stu-id="af18d-216">Blue</span></span>   | <span data-ttu-id="af18d-217">Mørk</span><span class="sxs-lookup"><span data-stu-id="af18d-217">Dark</span></span>  |
| <span data-ttu-id="af18d-218">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="af18d-218">Fabrikam</span></span>        | <span data-ttu-id="af18d-219">Houston</span><span class="sxs-lookup"><span data-stu-id="af18d-219">Houston</span></span>  | <span data-ttu-id="af18d-220">Mode</span><span class="sxs-lookup"><span data-stu-id="af18d-220">Fashion</span></span>        | <span data-ttu-id="af18d-221">Grøn</span><span class="sxs-lookup"><span data-stu-id="af18d-221">Green</span></span>  | <span data-ttu-id="af18d-222">Lys</span><span class="sxs-lookup"><span data-stu-id="af18d-222">Light</span></span> |
| <span data-ttu-id="af18d-223">Contoso</span><span class="sxs-lookup"><span data-stu-id="af18d-223">Contoso</span></span>         | <span data-ttu-id="af18d-224">Boston</span><span class="sxs-lookup"><span data-stu-id="af18d-224">Boston</span></span>   | <span data-ttu-id="af18d-225">Elektronik</span><span class="sxs-lookup"><span data-stu-id="af18d-225">Electronics</span></span>    | <span data-ttu-id="af18d-226">Rød</span><span class="sxs-lookup"><span data-stu-id="af18d-226">Red</span></span>    | <span data-ttu-id="af18d-227">Mørk</span><span class="sxs-lookup"><span data-stu-id="af18d-227">Dark</span></span>  |


>[!NOTE]
> <span data-ttu-id="af18d-228">Adventure Works og Fabrikam er de to største brands.</span><span class="sxs-lookup"><span data-stu-id="af18d-228">Adventure Works and Fabrikam are the two flagship brands.</span></span> <span data-ttu-id="af18d-229">Contoso er tilgængelig, men ikke alle layouts medfølger.</span><span class="sxs-lookup"><span data-stu-id="af18d-229">Contoso is available, but not all layouts have been provided.</span></span>


<span data-ttu-id="af18d-230">Nedenstående illustrationer viser eksempler på velkomstsiden og transaktionssiden for de tre fiktive firmaer.</span><span class="sxs-lookup"><span data-stu-id="af18d-230">The following illustrations show examples of the welcome page and transaction page for the three fictitious companies.</span></span>

### <a name="adventure-works"></a><span data-ttu-id="af18d-231">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="af18d-231">Adventure Works</span></span>

![Velkomstside i demodata til Adventure Works](../retail/media/demo-screen-layouts-fig-4-1a.png)

![Transaktionsside i demodata til Adventure Works](../retail/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a><span data-ttu-id="af18d-234">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="af18d-234">Fabrikam</span></span>

![Velkomstside i demodata til Fabrikam](../retail/media/demo-screen-layouts-fig-4-2a.png)

![Transaktionsside i demodata til Fabrikam](../retail/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a><span data-ttu-id="af18d-237">Contoso</span><span class="sxs-lookup"><span data-stu-id="af18d-237">Contoso</span></span>

![Layout af demodata til Contoso](../retail/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a><span data-ttu-id="af18d-239">Matrix for brugerlogon</span><span class="sxs-lookup"><span data-stu-id="af18d-239">User sign in matrix</span></span>

<span data-ttu-id="af18d-240">Der er angivet brugere til de forskellige skærmlayouts.</span><span class="sxs-lookup"><span data-stu-id="af18d-240">Users have been provided for the various screen layouts.</span></span> <span data-ttu-id="af18d-241">Ved hjælp af tabellen nedenfor, skal du være i stand til at få adgang til alle skærmbillederne.</span><span class="sxs-lookup"><span data-stu-id="af18d-241">By using the following table, you should be able to access any of the screens.</span></span> <span data-ttu-id="af18d-242">Du skal blot logge på ved brug af et passende operatør-id.</span><span class="sxs-lookup"><span data-stu-id="af18d-242">Just sign in by using an appropriate operator ID.</span></span>

| <span data-ttu-id="af18d-243">Regnskab</span><span class="sxs-lookup"><span data-stu-id="af18d-243">Company</span></span>         | <span data-ttu-id="af18d-244">Skærmlayout-id</span><span class="sxs-lookup"><span data-stu-id="af18d-244">Screen layout ID</span></span> | <span data-ttu-id="af18d-245">Karakter</span><span class="sxs-lookup"><span data-stu-id="af18d-245">Persona</span></span>          | <span data-ttu-id="af18d-246">Operatør-id'er</span><span class="sxs-lookup"><span data-stu-id="af18d-246">Operator IDs</span></span>           |
|-----------------|------------------|---------------   |------------------------|
| <span data-ttu-id="af18d-247">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="af18d-247">Adventure Works</span></span> | <span data-ttu-id="af18d-248">A3MGR</span><span class="sxs-lookup"><span data-stu-id="af18d-248">A3MGR</span></span>            | <span data-ttu-id="af18d-249">Butikschef</span><span class="sxs-lookup"><span data-stu-id="af18d-249">Store Manager</span></span>    | <span data-ttu-id="af18d-250">000154, 000137, 000073</span><span class="sxs-lookup"><span data-stu-id="af18d-250">000154, 000137, 000073</span></span> |
| <span data-ttu-id="af18d-251">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="af18d-251">Adventure Works</span></span> | <span data-ttu-id="af18d-252">A3CSH</span><span class="sxs-lookup"><span data-stu-id="af18d-252">A3CSH</span></span>            | <span data-ttu-id="af18d-253">Kasseassistent</span><span class="sxs-lookup"><span data-stu-id="af18d-253">Cashier</span></span>          | <span data-ttu-id="af18d-254">000150, 000175, 000165</span><span class="sxs-lookup"><span data-stu-id="af18d-254">000150, 000175, 000165</span></span> |
| <span data-ttu-id="af18d-255">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="af18d-255">Adventure Works</span></span> | <span data-ttu-id="af18d-256">A3STK</span><span class="sxs-lookup"><span data-stu-id="af18d-256">A3STK</span></span>            | <span data-ttu-id="af18d-257">Lagermedarbejder</span><span class="sxs-lookup"><span data-stu-id="af18d-257">Stock Clerk</span></span>      | <span data-ttu-id="af18d-258">000155, 000181, 000152</span><span class="sxs-lookup"><span data-stu-id="af18d-258">000155, 000181, 000152</span></span> |
| <span data-ttu-id="af18d-259">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="af18d-259">Fabrikam</span></span>        | <span data-ttu-id="af18d-260">F3MGR</span><span class="sxs-lookup"><span data-stu-id="af18d-260">F3MGR</span></span>            | <span data-ttu-id="af18d-261">Butikschef</span><span class="sxs-lookup"><span data-stu-id="af18d-261">Store Manager</span></span>    | <span data-ttu-id="af18d-262">000160, 000168, 000163</span><span class="sxs-lookup"><span data-stu-id="af18d-262">000160, 000168, 000163</span></span> |
| <span data-ttu-id="af18d-263">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="af18d-263">Fabrikam</span></span>        | <span data-ttu-id="af18d-264">F3CSH</span><span class="sxs-lookup"><span data-stu-id="af18d-264">F3CSH</span></span>            | <span data-ttu-id="af18d-265">Kasseassistent</span><span class="sxs-lookup"><span data-stu-id="af18d-265">Cashier</span></span>          | <span data-ttu-id="af18d-266">000161, 000113, 000114</span><span class="sxs-lookup"><span data-stu-id="af18d-266">000161, 000113, 000114</span></span> |
| <span data-ttu-id="af18d-267">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="af18d-267">Fabrikam</span></span>        | <span data-ttu-id="af18d-268">F3STK</span><span class="sxs-lookup"><span data-stu-id="af18d-268">F3STK</span></span>            | <span data-ttu-id="af18d-269">Lagermedarbejder</span><span class="sxs-lookup"><span data-stu-id="af18d-269">Stock Clerk</span></span>      | <span data-ttu-id="af18d-270">000164, 000112, 000123</span><span class="sxs-lookup"><span data-stu-id="af18d-270">000164, 000112, 000123</span></span> |
| <span data-ttu-id="af18d-271">Contoso</span><span class="sxs-lookup"><span data-stu-id="af18d-271">Contoso</span></span>         | <span data-ttu-id="af18d-272">C3MGR</span><span class="sxs-lookup"><span data-stu-id="af18d-272">C3MGR</span></span>            | <span data-ttu-id="af18d-273">Butikschef</span><span class="sxs-lookup"><span data-stu-id="af18d-273">Store Manager</span></span>    | <span data-ttu-id="af18d-274">000100, 000111</span><span class="sxs-lookup"><span data-stu-id="af18d-274">000100, 000111</span></span>         |
| <span data-ttu-id="af18d-275">Contoso</span><span class="sxs-lookup"><span data-stu-id="af18d-275">Contoso</span></span>         | <span data-ttu-id="af18d-276">C3CSH</span><span class="sxs-lookup"><span data-stu-id="af18d-276">C3CSH</span></span>            | <span data-ttu-id="af18d-277">Kasseassistent</span><span class="sxs-lookup"><span data-stu-id="af18d-277">Cashier</span></span>          | <span data-ttu-id="af18d-278">000110, 000120</span><span class="sxs-lookup"><span data-stu-id="af18d-278">000110, 000120</span></span>         |
| <span data-ttu-id="af18d-279">Contoso</span><span class="sxs-lookup"><span data-stu-id="af18d-279">Contoso</span></span>         | <span data-ttu-id="af18d-280">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="af18d-280">Not applicable</span></span>   | <span data-ttu-id="af18d-281">Lagermedarbejder</span><span class="sxs-lookup"><span data-stu-id="af18d-281">Stock Clerk</span></span>      | <span data-ttu-id="af18d-282">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="af18d-282">Not applicable</span></span>         |


>[!TIP]
> <span data-ttu-id="af18d-283">For at få de bedste resultater skal du aktivere et register i den tilsvarende butikslokalitet og angive firmaet til firmaet for den karakter, som du vil bruge, når du logger på.</span><span class="sxs-lookup"><span data-stu-id="af18d-283">For best results, activate a register in the corresponding store location, and set the company to the company of the persona that you plan to use when you sign in.</span></span> <span data-ttu-id="af18d-284">På denne måde kan du hjælpe med til at garantere, at den visuelle profil og brandingbillederne justeres på tværs af oplevelsen.</span><span class="sxs-lookup"><span data-stu-id="af18d-284">In this way, you help guarantee that the visual profile and branding images are aligned across the experience.</span></span> <span data-ttu-id="af18d-285">Hvis du f.eks. er interesseret i at se et layout til Fabrikam for en kasserer, skal du aktivere et register i butikken i Houston.</span><span class="sxs-lookup"><span data-stu-id="af18d-285">For example, if you're interested in seeing a Fabrikam layout for a cashier, you should activate a register in the Houston store.</span></span>


<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail > Channel setup > POS setup > POS > Images**. -->

<!-- ![Images in Dynamics 365 for Retail](../retail/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../retail/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->

