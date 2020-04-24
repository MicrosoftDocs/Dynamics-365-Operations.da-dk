---
title: Oversigt over forudsætninger for standardomkostninger
description: I dette emne beskrives de grundlæggende trin til brug af standardomkostninger.
author: AndersGirke
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f66f7061c608379689016e3c0b9c5ba4ad23dc9e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214501"
---
# <a name="prerequisites-for-standard-costs-overview"></a><span data-ttu-id="9bdf8-103">Oversigt over forudsætninger for standardomkostninger</span><span class="sxs-lookup"><span data-stu-id="9bdf8-103">Prerequisites for standard costs overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bdf8-104">I dette emne beskrives de grundlæggende trin til brug af standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="9bdf8-105">Efterfølgende trin afhænger af virksomhedens aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="9bdf8-106">Trinene er f.eks. forskellige i et ikke-produktionsmiljø, et produktionsmiljø, der ikke bruger ruter, eller et produktionsmiljø, der bruges ruter.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="9bdf8-107">Benyt følgende fremgangsmåde for at konfigurere standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="9bdf8-108">**1. Opret en varemodelgruppe for standardomkostninger.**</span><span class="sxs-lookup"><span data-stu-id="9bdf8-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="9bdf8-109">Brug siden **Varemodelgrupper** til at oprette en ny gruppe for standardomkostninger, og tildel en lagermodel med **Standardomkostning**.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="9bdf8-110">Identifikationen for varemodelgruppen skal give mening, f.eks. **Std.omk**.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="9bdf8-111">Markér afkrydsningsfelterne for at angive, at økonomisk negativ lagerbeholdning skal være tilladt for gruppen, at der skal bogføres fysisk og økonomisk lager.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="9bdf8-112">Varer tildeles denne standardkostgruppe.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="9bdf8-113">**2. Definer finanskonti, der vedrører standardomkostningsafvigelser.**</span><span class="sxs-lookup"><span data-stu-id="9bdf8-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="9bdf8-114">Brug siden **Kontoplan** til at definere finanskonti, der er knyttet til standardomkostningsafvigelser.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="9bdf8-115">Disse finanskonti skal defineres, før de kan tildeles på siden **Bogføring**.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="9bdf8-116">Finanskontiene kan afspejle varegrupper og omkostningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="9bdf8-117">**3. Tildel finanskonti til varebogføringer, der er knyttet til standardomkostningsafvigelser.**</span><span class="sxs-lookup"><span data-stu-id="9bdf8-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="9bdf8-118">Brug siden **Bogføring** til at tildele de finanskonti, der er knyttet til standardomkostningsafvigelser.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="9bdf8-119">Du kan angive en finanskonto for afvigelser for de enkelte varer (eller varegrupper) og for de enkelte omkostningsgrupper (eller omkostningsgruppetyper), eller du kan angive, at finanskontoen gælder for alle varer og alle omkostningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="9bdf8-120">Disse indstillinger svarer til omkostningsrelationer for tabeller, grupper og alle.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="9bdf8-121">Før du definerer reglerne for varekontering, skal du bruge siden **Transaktionskombinationer** til at aktivere omkostningsrelationer (for tabeller, grupper og alle).</span><span class="sxs-lookup"><span data-stu-id="9bdf8-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="9bdf8-122">**4. Definer lagerparametre, der er knyttet til standardomkostninger.**</span><span class="sxs-lookup"><span data-stu-id="9bdf8-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="9bdf8-123">Brug fanen **Lagerregnskab** på siden **Konfiguration af regnskabspolitik for lager > Parametre** til at definere to parametre for omkostningsstyring, der er knyttet til standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-123">Use the **Inventory accounting** tab on the **Inventory accounting policies setup > Parameters** page to define two cost control parameters that are related to standard costs.</span></span>

    -  <span data-ttu-id="9bdf8-124">I feltet **Kostprisopdeling** skal du vælge **Ingen** eller **Underfinanskonto**.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="9bdf8-125">Hvis du vælger **Underfinanskonto**, er kostprisopdelingen en *aktiv* kostprisopdeling.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="9bdf8-126">En aktiv kostprisopdeling er vigtig for beregning, bevarelse og visning af segmentering af omkostningsgrupper på tværs af en produktstruktur med flere niveauer for standardomkostningsvarer.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="9bdf8-127">Når kostprisopdelingen er aktiv, kan du rapportere og analysere lager, IGVA (igangværende arbejde) og vareforbrug for de enkelte omkostningsgrupper på et enkelt niveau, flere niveauer eller i det samlede format.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="9bdf8-128">Når kostprisopdelingen er aktiv, og du aktiverer omkostninger for en produceret vare, lagres segmenteringen af omkostningsgruppen i varens kostprispost.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="9bdf8-129">Hvis du vælger **Ingen**, vedligeholdes kostgruppesegmenteringen ikke for varer med standardkostpriser.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="9bdf8-130">Med andre ord beregnes og vedligeholdes en produceret vares standardkostpris som et enkelt beløb uden segmentering af omkostningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="9bdf8-131">Kostbidraget for producerede komponenter samles i dette enkeltbeløb.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="9bdf8-132">I feltet **Afvigelser fra standard** skal du vælge **Opsummeret** eller **Pr. kostgruppe**.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="9bdf8-133">Hvis du vælger **Pr. kostgruppe**, kan du identificere afvigelser i indkøbsprisen og produktionsafvigelser pr. omkostningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="9bdf8-134">Du kan også identificere de fire typer produktionsafvigelser: afvigelse i partistørrelse, antal, pris og erstatning.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="9bdf8-135">Hvis du vælger **Opsummeret**, kan du ikke identificere afgivelser for de enkelte omkostningsgrupper, og du kan ikke identificere de fire typer produktionsafvigelser.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="9bdf8-136">Du kan kun se en opsummeret produktionsafvigelse.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="9bdf8-137">Reglerne for afvigelser fra standarden fungerer uafhængigt af reglerne for kostprisopdeling.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="9bdf8-138">Du kan med andre ord vælge en regel for kostprisopdeling som **Ingen** og vælge afvigelser for de enkelte omkostningsgrupper, så du stadig kan registrere produktionsafvigelser for de enkelte omkostningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="9bdf8-139">**5. Opret efterkalkulationsversioner for standardomkostninger.**</span><span class="sxs-lookup"><span data-stu-id="9bdf8-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="9bdf8-140">Brug siden **Opsætning af efterkalkulationsversion** til at oprette en eller flere omkostningsversioner for standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="9bdf8-141">De enkelte omkostningsversioner skal oprettes med omkostningstypen **Standardomkostninger** og skal tillade, at der må være omkostningsoplysninger i indholdet.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="9bdf8-142">**6. Konfigurer en eksisterende kunde til at bruge standardomkostninger.**</span><span class="sxs-lookup"><span data-stu-id="9bdf8-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="9bdf8-143">Kunder, der vil ændre deres eksisterende varer til en lagermodel med standardomkostninger, skal bruge siden **Standardomkostningskonverteringer**.</span><span class="sxs-lookup"><span data-stu-id="9bdf8-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="9bdf8-144">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="9bdf8-144">Related topics</span></span>
--------

[<span data-ttu-id="9bdf8-145">Oversigt over standardomkostningskonvertering</span><span class="sxs-lookup"><span data-stu-id="9bdf8-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)

### <a name="blogs"></a><span data-ttu-id="9bdf8-146">Blogs</span><span class="sxs-lookup"><span data-stu-id="9bdf8-146">Blogs</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="9bdf8-147">Fællesskabsblogge</span><span class="sxs-lookup"><span data-stu-id="9bdf8-147">Community blogs</span></span>

- [<span data-ttu-id="9bdf8-148">Sådan opsættes standardomkostninger for direkte materialer i Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9bdf8-148">How to set up standard costs for direct materials in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [<span data-ttu-id="9bdf8-149">Direkte standardlønomkostninger i Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9bdf8-149">Standard direct labor costs in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)
