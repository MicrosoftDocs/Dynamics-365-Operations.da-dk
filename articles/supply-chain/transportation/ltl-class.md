---
title: Mindre end truckload-klasser (LTL)
description: Dette emne forklarer, hvad mindre end truckload-klasser (LTL) er, og beskriver, hvordan de konfigureres i Microsoft Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941804"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="5dd0a-103">Mindre end truckload-klasser (LTL)</span><span class="sxs-lookup"><span data-stu-id="5dd0a-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5dd0a-104">En klasse, der er mindre end truckload (LTL), er en forsendelsesklasse, der bruges til at klassificere varer, der kan afsendes.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="5dd0a-105">Generelt har alle typer produkter eller varer en NMFC-kode (National Motor Freight Classification), der svarer til nummeret på en bestemt fragtklasse for LTL-forsendelser.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="5dd0a-106">LTL-fragtklasser repræsenterer varekategorier, hvorimod NMFC-koder er relateret til specifikke varer i hver af de 18 fragtklasser.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="5dd0a-107">Med denne funktion kan du bruge systemet til at udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="5dd0a-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="5dd0a-108">Definer de LTL-fragtklasser, der bruges i din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="5dd0a-109">Tildel hver LTL-klasse til en NMFC-kode på siden **NMFC-koder**.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="5dd0a-110">Du kan finde flere oplysninger i [NMFC-koder (National Motor Freight Classification)](nmfc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5dd0a-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="5dd0a-111">Tildel en NMFC-kode (og dermed den tilknyttede LTL-kode) til hvert produkt på siden **Produkter**.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="5dd0a-112">Vurder nøje, den LTL-klasse for det enkelte produkt, som en NMFC-kode er tildelt.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="5dd0a-113">Fastlæg emballagekravene for hver LTL-klasse ved at kontrollere de internationale LTL-standarder.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="5dd0a-114">På denne måde sikrer du, at dine produkter bliver beskyttet korrekt og fragtet på sikker vis.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="5dd0a-115">Etabler nøjagtige forsendelsesestimater baseret på LTL-fragtklassen for hvert produkt.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="5dd0a-116">Dette emne beskriver, hvordan du opretter LTL-klasser i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="5dd0a-117">Oprette en LTL-klasse</span><span class="sxs-lookup"><span data-stu-id="5dd0a-117">Create an LTL class</span></span>

<span data-ttu-id="5dd0a-118">Benyt følgende fremgangsmåde for at oprette en LTL-klasse.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="5dd0a-119">Udfør ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="5dd0a-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="5dd0a-120">Gå til **Lagerstedsstyring \> Opsætning \> Lagerbeholdning \> LTL-klasser**.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="5dd0a-121">Gå til **Transportstyring \> Opsætning \> Transportstandarder \> LTL-klasser**.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="5dd0a-122">Vælg **Ny** i handlingsruden for at oprette en LTL-klasse.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="5dd0a-123">Angiv derefter følgende felter:</span><span class="sxs-lookup"><span data-stu-id="5dd0a-123">Then set the following fields:</span></span>

    - <span data-ttu-id="5dd0a-124">**LTL-klasse** – Angiv virksomhedens interne LTL-klasseidentifikation (id) for varetypen.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="5dd0a-125">De fleste virksomheder følger de internationale standarder.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-125">Most companies use the international standard.</span></span> <span data-ttu-id="5dd0a-126">I dette tilfælde vil værdien i dette felt svare til værdien i feltet **Klasse**.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="5dd0a-127">Hvis virksomheden anvender sin egen standard, skal du dog angive en kode, der overholder standarden.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="5dd0a-128">**Navn** – Angiv et beskrivende navn, der kan hjælpe dig og andre brugere med at vælge den rette LTL-klasse for hver NMFC-kode.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="5dd0a-129">**Klasse** – Angiv den internationale LTL-standardklasses id for varetypen.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="5dd0a-130">Den kode, du angiver her, skal overholde den officielle standard.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="5dd0a-131">Eksempel: Konfigurere LTL-klasser</span><span class="sxs-lookup"><span data-stu-id="5dd0a-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="5dd0a-132">I følgende eksempel vises det, hvordan du kan konfigurere to forskellige LTL-klasser, som du kan bruge til forskellige typer produkter.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="5dd0a-133">Gå til **Lagerstedsstyring \> Opsætning \> Lagerbeholdning \> LTL-klasser**.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="5dd0a-134">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5dd0a-135">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="5dd0a-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="5dd0a-136">**LTL-klasse:** *92,5*</span><span class="sxs-lookup"><span data-stu-id="5dd0a-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="5dd0a-137">**Navn:** *Computere, skærme, køleskabe*</span><span class="sxs-lookup"><span data-stu-id="5dd0a-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="5dd0a-138">**Klasse:** *92,5*</span><span class="sxs-lookup"><span data-stu-id="5dd0a-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="5dd0a-139">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5dd0a-140">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5dd0a-141">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="5dd0a-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="5dd0a-142">**LTL-klasse:** *125*</span><span class="sxs-lookup"><span data-stu-id="5dd0a-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="5dd0a-143">**Navn:** *Små husholdningsapparater*</span><span class="sxs-lookup"><span data-stu-id="5dd0a-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="5dd0a-144">**Klasse:** *125*</span><span class="sxs-lookup"><span data-stu-id="5dd0a-144">**Class:** *125*</span></span>

1. <span data-ttu-id="5dd0a-145">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5dd0a-146">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5dd0a-146">Additional resources</span></span>

- [<span data-ttu-id="5dd0a-147">NMFC-koder (National Motor Freight Classification)</span><span class="sxs-lookup"><span data-stu-id="5dd0a-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="5dd0a-148">Oprette en fragtseddel</span><span class="sxs-lookup"><span data-stu-id="5dd0a-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
