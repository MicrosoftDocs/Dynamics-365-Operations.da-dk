---
title: "Årsagskoder for lageroptælling"
description: "Dette emne beskriver, hvordan du konfigurerer og anvender årsagskoder til optællingsopgaver."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 2f4332432ad73861cd9b6b6452685d3175ace56b
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="0351c-103">Årsagskoder for lageroptælling</span><span class="sxs-lookup"><span data-stu-id="0351c-103">Reason codes for inventory counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0351c-104">Med årsagskoder kan du analysere resultaterne af en optællingsproces og eventuelle uoverensstemmelser, der opstår under denne proces.</span><span class="sxs-lookup"><span data-stu-id="0351c-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="0351c-105">Du kan angive årsagen til optællingen, f.eks. en ødelagt palle eller en regulering af lageret, der er baseret på lagerprøver.</span><span class="sxs-lookup"><span data-stu-id="0351c-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="0351c-106">Anbefaling</span><span class="sxs-lookup"><span data-stu-id="0351c-106">Recommendation</span></span>

<span data-ttu-id="0351c-107">Før du konfigurerer systemet, anbefales det, at du definerer en strategi for at arbejde med årsagskoder.</span><span class="sxs-lookup"><span data-stu-id="0351c-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="0351c-108">Prøv f.eks. at besvare følgende spørgsmål:</span><span class="sxs-lookup"><span data-stu-id="0351c-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="0351c-109">Skal årsagskoder være obligatoriske på lagersteder?</span><span class="sxs-lookup"><span data-stu-id="0351c-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="0351c-110">Årsagskoder skal være obligatoriske eller valgfrie for bestemte varer?</span><span class="sxs-lookup"><span data-stu-id="0351c-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="0351c-111">Hvor mange årsagskoder skal du bruge?</span><span class="sxs-lookup"><span data-stu-id="0351c-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="0351c-112">Hvordan skal brugere af stregkodescannere bruge årsagskoder?</span><span class="sxs-lookup"><span data-stu-id="0351c-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="0351c-113">Skal årsagskoderne være forvalgte, obligatoriske eller ikke kunne redigeres?</span><span class="sxs-lookup"><span data-stu-id="0351c-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="0351c-114">Kræver lagermedarbejdere andre funktionsmåder for årsagskoder på mobile scannere?</span><span class="sxs-lookup"><span data-stu-id="0351c-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="0351c-115">Hvis svaret er Ja, kan du oprette flere menupunkter og tildele dem til forskellige personer.</span><span class="sxs-lookup"><span data-stu-id="0351c-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="0351c-116">Hvor anvendes årsagskoder</span><span class="sxs-lookup"><span data-stu-id="0351c-116">Where reason codes apply</span></span>

<span data-ttu-id="0351c-117">Du kan oprette flere årsagskodepolitikker, og hver årsagskodepolitik kan have to politikker for årsagskoder for optælling.</span><span class="sxs-lookup"><span data-stu-id="0351c-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="0351c-118">Politikker for optællingsårsagskoder kan bruges på lagerstedsniveau eller vareniveau.</span><span class="sxs-lookup"><span data-stu-id="0351c-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="0351c-119">Konfigurere politikker for årsagskoder</span><span class="sxs-lookup"><span data-stu-id="0351c-119">Set up reason code policies</span></span>

1. <span data-ttu-id="0351c-120">Vælg **Lagerstyring** \> **Opsætning** \> **Lager** \> **Politikker for optællingsårsagskode**, og opret en ny politik for årsagskoder.</span><span class="sxs-lookup"><span data-stu-id="0351c-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="0351c-121">I feltet **Type af optællingsårsagskode** skal du vælge enten **Obligatorisk** eller **Valgfrit** for at angive, om valget af en årsagskode skal være en valgfri eller obligatorisk handling i en af følgende optællingskladder:</span><span class="sxs-lookup"><span data-stu-id="0351c-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="0351c-122">Cyklusoptælling (mobilenhed)</span><span class="sxs-lookup"><span data-stu-id="0351c-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="0351c-123">Spotoptælling (mobilenhed)</span><span class="sxs-lookup"><span data-stu-id="0351c-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="0351c-124">Grænseoptælling (mobilenhed)</span><span class="sxs-lookup"><span data-stu-id="0351c-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="0351c-125">Regulering ind (mobilenhed)</span><span class="sxs-lookup"><span data-stu-id="0351c-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="0351c-126">Regulering ud (mobilenhed)</span><span class="sxs-lookup"><span data-stu-id="0351c-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="0351c-127">Optællingskladde (Rich Client)</span><span class="sxs-lookup"><span data-stu-id="0351c-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="0351c-128">Du kan også angive årsagskoder for individuelle lagersteder og produkter.</span><span class="sxs-lookup"><span data-stu-id="0351c-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="0351c-129">Opsætningen af årsagskoder for produkter kan se bort fra opsætningen for lagersteder.</span><span class="sxs-lookup"><span data-stu-id="0351c-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="0351c-130">Obligatoriske årsagskoder</span><span class="sxs-lookup"><span data-stu-id="0351c-130">Mandatory reason codes</span></span>

<span data-ttu-id="0351c-131">Hvis parameteren **Obligatorisk** er angivet i konfigurationen af årsagskoder for lagersteder eller varer, kan optællingskladden ikke fuldføres og lukkes, før en årsagskode er angivet.</span><span class="sxs-lookup"><span data-stu-id="0351c-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="0351c-132">Konfigurere årsagskoder for lagersteder</span><span class="sxs-lookup"><span data-stu-id="0351c-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="0351c-133">Vælg **Lagerstyring** \> **Opsætning** \> **Lageropdeling** \> **Lagersteder**.</span><span class="sxs-lookup"><span data-stu-id="0351c-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="0351c-134">På fanen **Lagersted** i feltet **Politik for optællingsårsagskode** skal du vælge en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0351c-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="0351c-135">**Tom** – Den parameter, der er defineret for varen, bruges til at afgøre, om optællingskladder er obligatoriske for produktet.</span><span class="sxs-lookup"><span data-stu-id="0351c-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="0351c-136">**Obligatoriske** – Der kræves altid en årsagskode på optællingskladder for lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="0351c-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="0351c-137">**Valgfri** – Der kræves ikke en årsagskode på optællingskladder for lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="0351c-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="0351c-138">Konfigurere årsagskoder for produkter</span><span class="sxs-lookup"><span data-stu-id="0351c-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="0351c-139">Vælg **Administration af produktoplysninger** \> **Produkter** \> **Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="0351c-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="0351c-140">På fanen **Produkt** skal du vælge **Politik for optællingsårsagskode** og derefter vælge en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0351c-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="0351c-141">**Tom** – Den parameter, der er defineret for lagerstedet, bruges til at afgøre, om optællingskladder er obligatoriske for produktet.</span><span class="sxs-lookup"><span data-stu-id="0351c-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="0351c-142">**Obligatoriske** – Der kræves altid en årsagskode kræves på optællingskladder for produktet.</span><span class="sxs-lookup"><span data-stu-id="0351c-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="0351c-143">Denne indstilling tilsidesætter enhver indstilling for årsagskoder på lagerstedsniveau.</span><span class="sxs-lookup"><span data-stu-id="0351c-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="0351c-144">**Valgfri** – Der kræves ikke en årsagskode på optællingskladder for produktet.</span><span class="sxs-lookup"><span data-stu-id="0351c-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="0351c-145">Denne indstilling tilsidesætter enhver indstilling for årsagskoder på lagerstedsniveau.</span><span class="sxs-lookup"><span data-stu-id="0351c-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="0351c-146">Bruge årsagskoder i optællingskladder</span><span class="sxs-lookup"><span data-stu-id="0351c-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="0351c-147">I en optællingskladde kan du tilføje årsagskoder for optælling af følgende typer:</span><span class="sxs-lookup"><span data-stu-id="0351c-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="0351c-148">Cyklusoptælling</span><span class="sxs-lookup"><span data-stu-id="0351c-148">Cycle Count</span></span>
- <span data-ttu-id="0351c-149">Spotoptælling</span><span class="sxs-lookup"><span data-stu-id="0351c-149">Spot Count</span></span>
- <span data-ttu-id="0351c-150">Grænseoptælling</span><span class="sxs-lookup"><span data-stu-id="0351c-150">Threshold Count</span></span>
- <span data-ttu-id="0351c-151">Regulering ind</span><span class="sxs-lookup"><span data-stu-id="0351c-151">Adjustment In</span></span>
- <span data-ttu-id="0351c-152">Regulering ud</span><span class="sxs-lookup"><span data-stu-id="0351c-152">Adjustment Out</span></span>

<span data-ttu-id="0351c-153">Årsagskoder føjes til kladdelinjerne i optællingskladder af typen **Optællingskladde**.</span><span class="sxs-lookup"><span data-stu-id="0351c-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="0351c-154">Vælg **Lagerstyring** \> **Kladdeposteringer** \> **Vareoptælling** \> **Optælling**.</span><span class="sxs-lookup"><span data-stu-id="0351c-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="0351c-155">I linjedetaljerne i optællingskladden, i feltet **Optællingsårsagskode** skal du vælge en indstilling.</span><span class="sxs-lookup"><span data-stu-id="0351c-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="0351c-156">Få vist optællingshistorikken, sådan som den er registreret af årsagskoder</span><span class="sxs-lookup"><span data-stu-id="0351c-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="0351c-157">Vælg **Lagerstyring** \> **Forespørgsler og rapporter** \> **Optællingshistorik**, få derefter vist den optællingshistorik i feltet **Optællingsårsagskode**, som er registreret gennem en årsagskode.</span><span class="sxs-lookup"><span data-stu-id="0351c-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="0351c-158">Bruge en årsagskode til en regulering af antal</span><span class="sxs-lookup"><span data-stu-id="0351c-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="0351c-159">På siden **Disponibel lagerbeholdning** skal du vælge **Juster antal**.</span><span class="sxs-lookup"><span data-stu-id="0351c-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="0351c-160">Du kan åbne siden **Disponibel lagerbeholdning** på flere måder.</span><span class="sxs-lookup"><span data-stu-id="0351c-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="0351c-161">Vælg f.eks. **Lagerstyring** \> **Forespørgsler og rapporter** \> **Disponibel lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="0351c-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="0351c-162">Vælg **Juster antal**, og vælg derefter en årsagskode i feltet **Optællingsårsagskode**.</span><span class="sxs-lookup"><span data-stu-id="0351c-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="0351c-163">Konfigurere årsagskoder for mobilenheds menupunkter</span><span class="sxs-lookup"><span data-stu-id="0351c-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="0351c-164">Du kan konfigurere årsagskoder for enhver type optælling i et menupunkt på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="0351c-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="0351c-165">Konfigurationen af menupunktet på mobilenheden indeholder følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="0351c-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="0351c-166">Om årsagskoden vises for mobilenhedens arbejder under optælling.</span><span class="sxs-lookup"><span data-stu-id="0351c-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="0351c-167">Den standardårsagskode, der vises i en mobilenheds menupunkt.</span><span class="sxs-lookup"><span data-stu-id="0351c-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="0351c-168">Om brugeren kan redigere årsagskoden.</span><span class="sxs-lookup"><span data-stu-id="0351c-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="0351c-169">Konfigurere årsagskoder på en mobilenhed</span><span class="sxs-lookup"><span data-stu-id="0351c-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="0351c-170">Vælg **Lokationsstyring** \> **Opsætning** \> **Mobilenhed** \> **Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="0351c-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="0351c-171">På fanen **Cyklusoptælling** skal du vælge **Cyklusoptælling**.</span><span class="sxs-lookup"><span data-stu-id="0351c-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="0351c-172">I feltet **Standardkode for optællingsårsag** skal du angive den standardårsagskode, der skal registreres, når optællingen udføres ved hjælp af mobilenhedens menupunkt.</span><span class="sxs-lookup"><span data-stu-id="0351c-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="0351c-173">I feltet **Vis optællingsårsagskode** skal du vælge **Linje** for at vise årsagskoden efter registrering af hver afvigelse.</span><span class="sxs-lookup"><span data-stu-id="0351c-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="0351c-174">Alternativt skal du vælge **Skjul**, hvis årsagskoden ikke skal vises.</span><span class="sxs-lookup"><span data-stu-id="0351c-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="0351c-175">Angiv indstillingen **Rediger optællingsårsagskode** til enten **Ja** eller **Nej**.</span><span class="sxs-lookup"><span data-stu-id="0351c-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="0351c-176">Hvis du angiver denne indstilling til **Ja**, kan arbejderen redigere årsagskoden, når den vises på mobileenheden under optælling.</span><span class="sxs-lookup"><span data-stu-id="0351c-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="0351c-177">Knappen **Cyklusoptælling** kan aktiveres i menupunktet på enhver mobilenhed, hvor optælling kan udføres.</span><span class="sxs-lookup"><span data-stu-id="0351c-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="0351c-178">Eksemplet omfatter menupunkter for spotoptællinger, brugerstyret arbejde og systemstyret arbejde.</span><span class="sxs-lookup"><span data-stu-id="0351c-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="0351c-179">Godkendelse af cyklusoptælling</span><span class="sxs-lookup"><span data-stu-id="0351c-179">Cycle count approvals</span></span>

<span data-ttu-id="0351c-180">Før antallet godkendes, kan brugeren ændre den årsagskode, der er tilknyttet optællingen.</span><span class="sxs-lookup"><span data-stu-id="0351c-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="0351c-181">Når optællingen er godkendt, angives årsagskoden i optællingskladdens linjer.</span><span class="sxs-lookup"><span data-stu-id="0351c-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="0351c-182">Rediger godkendelse af cyklusoptælling</span><span class="sxs-lookup"><span data-stu-id="0351c-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="0351c-183">Vælg **Lokationsstyring** \> **Cyklusoptælling** \> **Ventende gennemsyn af cyklusoptællingsarbejde**.</span><span class="sxs-lookup"><span data-stu-id="0351c-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="0351c-184">Vælg **Cyklusoptælling**, og vælg derefter en ny årsagskode i feltet **Årsagskode**.</span><span class="sxs-lookup"><span data-stu-id="0351c-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="0351c-185">Redigere mobilenhedens menupunkt for Regulering ind og Regulering ud</span><span class="sxs-lookup"><span data-stu-id="0351c-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="0351c-186">Vælg **Lokationsstyring** \> **Opsætning** \> **Mobilenhed** \> **Menupunkter i mobilenhed**, og vælg derefter **Regulering ind og ud**.</span><span class="sxs-lookup"><span data-stu-id="0351c-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="0351c-187">Angiv indstillingen **Brug eksisterende arbejde** til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="0351c-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="0351c-188">I feltet **Arbejdsoprettelsesproces** skal du vælge **Regulering ind**.</span><span class="sxs-lookup"><span data-stu-id="0351c-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="0351c-189">Følgende felter føjes til mobilenhedens menupunkt, når **Regulering ind** eller **Regulering ud** er valgt under oprettelsen af arbejdsoprettelsesprocessen:</span><span class="sxs-lookup"><span data-stu-id="0351c-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="0351c-190">Standardkode for optællingsårsag</span><span class="sxs-lookup"><span data-stu-id="0351c-190">Default counting reason code</span></span>
- <span data-ttu-id="0351c-191">Vis optællingsårsagskode</span><span class="sxs-lookup"><span data-stu-id="0351c-191">Display counting reason code</span></span>
- <span data-ttu-id="0351c-192">Rediger optællingsårsagskode</span><span class="sxs-lookup"><span data-stu-id="0351c-192">Edit counting reason code</span></span>

