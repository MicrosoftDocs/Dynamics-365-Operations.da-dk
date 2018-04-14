---
title: "Forudsætninger for standardomkostninger"
description: "I dette emne beskrives de grundlæggende trin til brug af standardomkostninger."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f7f1cef3198462eab15c1c7d2de4c5d4a5576919
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="prerequisites-for-standard-costs"></a><span data-ttu-id="caf78-103">Forudsætninger for standardomkostninger</span><span class="sxs-lookup"><span data-stu-id="caf78-103">Prerequisites for standard costs</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="caf78-104">I dette emne beskrives de grundlæggende trin til brug af standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="caf78-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="caf78-105">Efterfølgende trin afhænger af virksomhedens aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="caf78-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="caf78-106">Trinene er f.eks. forskellige i et ikke-produktionsmiljø, et produktionsmiljø, der ikke bruger ruter, eller et produktionsmiljø, der bruges ruter.</span><span class="sxs-lookup"><span data-stu-id="caf78-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="caf78-107">Benyt følgende fremgangsmåde for at konfigurere standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="caf78-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="caf78-108">**1. Opret en varemodelgruppe for standardomkostninger.**</span><span class="sxs-lookup"><span data-stu-id="caf78-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="caf78-109">Brug siden **Varemodelgrupper** til at oprette en ny gruppe for standardomkostninger, og tildel en lagermodel med **Standardomkostning**.</span><span class="sxs-lookup"><span data-stu-id="caf78-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="caf78-110">Identifikationen for varemodelgruppen skal give mening, f.eks. **Std.omk**.</span><span class="sxs-lookup"><span data-stu-id="caf78-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="caf78-111">Markér afkrydsningsfelterne for at angive, at økonomisk negativ lagerbeholdning skal være tilladt for gruppen, at der skal bogføres fysisk og økonomisk lager.</span><span class="sxs-lookup"><span data-stu-id="caf78-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="caf78-112">Varer tildeles denne standardkostgruppe.</span><span class="sxs-lookup"><span data-stu-id="caf78-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="caf78-113">**2. Definer finanskonti, der vedrører standardomkostningsafvigelser.**</span><span class="sxs-lookup"><span data-stu-id="caf78-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="caf78-114">Brug siden **Kontoplan** til at definere finanskonti, der er knyttet til standardomkostningsafvigelser.</span><span class="sxs-lookup"><span data-stu-id="caf78-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="caf78-115">Disse finanskonti skal defineres, før de kan tildeles på siden **Bogføring**.</span><span class="sxs-lookup"><span data-stu-id="caf78-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="caf78-116">Finanskontiene kan afspejle varegrupper og omkostningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="caf78-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="caf78-117">**3. Tildel finanskonti til varebogføringer, der er knyttet til standardomkostningsafvigelser.**</span><span class="sxs-lookup"><span data-stu-id="caf78-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="caf78-118">Brug siden **Bogføring** til at tildele de finanskonti, der er knyttet til standardomkostningsafvigelser.</span><span class="sxs-lookup"><span data-stu-id="caf78-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="caf78-119">Du kan angive en finanskonto for afvigelser for de enkelte varer (eller varegrupper) og for de enkelte omkostningsgrupper (eller omkostningsgruppetyper), eller du kan angive, at finanskontoen gælder for alle varer og alle omkostningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="caf78-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="caf78-120">Disse indstillinger svarer til omkostningsrelationer for tabeller, grupper og alle.</span><span class="sxs-lookup"><span data-stu-id="caf78-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="caf78-121">Før du definerer reglerne for varekontering, skal du bruge siden **Transaktionskombinationer** til at aktivere omkostningsrelationer (for tabeller, grupper og alle).</span><span class="sxs-lookup"><span data-stu-id="caf78-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="caf78-122">**4. Definer lagerparametre, der er knyttet til standardomkostninger.**</span><span class="sxs-lookup"><span data-stu-id="caf78-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="caf78-123">Brug fanen **Stykliste** på siden **Lagerparametre** til at definere to parametre for omkostningsstyring, der er knyttet til standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="caf78-123">Use the **Bills of materials** tab on the **Inventory parameters** page to define two cost control parameters that are related to standard costs.</span></span> 

    -  <span data-ttu-id="caf78-124">I feltet **Kostprisopdeling** skal du vælge **Ingen** eller **Underfinanskonto**.</span><span class="sxs-lookup"><span data-stu-id="caf78-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="caf78-125">Hvis du vælger **Underfinanskonto**, er kostprisopdelingen en *aktiv* kostprisopdeling.</span><span class="sxs-lookup"><span data-stu-id="caf78-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="caf78-126">En aktiv kostprisopdeling er vigtig for beregning, bevarelse og visning af segmentering af omkostningsgrupper på tværs af en produktstruktur med flere niveauer for standardomkostningsvarer.</span><span class="sxs-lookup"><span data-stu-id="caf78-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="caf78-127">Når kostprisopdelingen er aktiv, kan du rapportere og analysere lager, IGVA (igangværende arbejde) og vareforbrug for de enkelte omkostningsgrupper på et enkelt niveau, flere niveauer eller i det samlede format.</span><span class="sxs-lookup"><span data-stu-id="caf78-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="caf78-128">Når kostprisopdelingen er aktiv, og du aktiverer omkostninger for en produceret vare, lagres segmenteringen af omkostningsgruppen i varens kostprispost.</span><span class="sxs-lookup"><span data-stu-id="caf78-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="caf78-129">Hvis du vælger **Ingen**, vedligeholdes kostgruppesegmenteringen ikke for varer med standardkostpriser.</span><span class="sxs-lookup"><span data-stu-id="caf78-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="caf78-130">Med andre ord beregnes og vedligeholdes en produceret vares standardkostpris som et enkelt beløb uden segmentering af omkostningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="caf78-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="caf78-131">Kostbidraget for producerede komponenter samles i dette enkeltbeløb.</span><span class="sxs-lookup"><span data-stu-id="caf78-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="caf78-132">I feltet **Afvigelser fra standard** skal du vælge **Opsummeret** eller **Pr. kostgruppe**.</span><span class="sxs-lookup"><span data-stu-id="caf78-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="caf78-133">Hvis du vælger **Pr. kostgruppe**, kan du identificere afvigelser i indkøbsprisen og produktionsafvigelser pr. omkostningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="caf78-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="caf78-134">Du kan også identificere de fire typer produktionsafvigelser: afvigelse i partistørrelse, antal, pris og erstatning.</span><span class="sxs-lookup"><span data-stu-id="caf78-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="caf78-135">Hvis du vælger **Opsummeret**, kan du ikke identificere afgivelser for de enkelte omkostningsgrupper, og du kan ikke identificere de fire typer produktionsafvigelser.</span><span class="sxs-lookup"><span data-stu-id="caf78-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="caf78-136">Du kan kun se en opsummeret produktionsafvigelse.</span><span class="sxs-lookup"><span data-stu-id="caf78-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="caf78-137">Reglerne for afvigelser fra standarden fungerer uafhængigt af reglerne for kostprisopdeling.</span><span class="sxs-lookup"><span data-stu-id="caf78-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="caf78-138">Du kan med andre ord vælge en regel for kostprisopdeling som **Ingen** og vælge afvigelser for de enkelte omkostningsgrupper, så du stadig kan registrere produktionsafvigelser for de enkelte omkostningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="caf78-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="caf78-139">**5. Opret efterkalkulationsversioner for standardomkostninger.**</span><span class="sxs-lookup"><span data-stu-id="caf78-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="caf78-140">Brug siden **Opsætning af efterkalkulationsversion** til at oprette en eller flere omkostningsversioner for standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="caf78-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="caf78-141">De enkelte omkostningsversioner skal oprettes med omkostningstypen **Standardomkostninger** og skal tillade, at der må være omkostningsoplysninger i indholdet.</span><span class="sxs-lookup"><span data-stu-id="caf78-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="caf78-142">**6. Konfigurer en eksisterende kunde til at bruge standardomkostninger.**</span><span class="sxs-lookup"><span data-stu-id="caf78-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="caf78-143">Kunder, der vil ændre deres eksisterende varer til en lagermodel med standardomkostninger, skal bruge siden **Standardomkostningskonverteringer**.</span><span class="sxs-lookup"><span data-stu-id="caf78-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="caf78-144">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="caf78-144">Related topics</span></span>
--------

[<span data-ttu-id="caf78-145">Oversigt over standardomkostningskonvertering</span><span class="sxs-lookup"><span data-stu-id="caf78-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)


