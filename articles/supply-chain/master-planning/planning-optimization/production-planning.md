---
title: Produktionsplanlægning
description: Dette emne beskriver produktionsplanlægning med en forklaring af, hvordan du redigerer planlagte produktionsordrer ved hjælp af Planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eda22aa6f1e8d665d8ef390f24b247a76d4c2956
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992389"
---
# <a name="production-planning"></a><span data-ttu-id="7075e-103">Produktionsplanlægning</span><span class="sxs-lookup"><span data-stu-id="7075e-103">Production planning</span></span>

<span data-ttu-id="7075e-104">Planlægningsoptimering understøtter flere produktionsscenarier.</span><span class="sxs-lookup"><span data-stu-id="7075e-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="7075e-105">Hvis du migrerer fra det eksisterende, indbyggede varedisponeringsprogram, er det vigtigt, at du er opmærksom på ændret adfærd.</span><span class="sxs-lookup"><span data-stu-id="7075e-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<!-- The following video gives a short introduction to some of the current capabilities. 
KFM: Link to video for production functionality, coming soon... -->

## <a name="planned-production-orders"></a><span data-ttu-id="7075e-106">Produktionsordreforslag</span><span class="sxs-lookup"><span data-stu-id="7075e-106">Planned production orders</span></span>

<span data-ttu-id="7075e-107">Når varedisponering opretter ordreforslag for at opfylde kravene, fastlægges ordretypen af værdien i feltet **Ordreforslagstype**.</span><span class="sxs-lookup"><span data-stu-id="7075e-107">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="7075e-108">Hvis feltet **Ordreforslagstype** er angivet til *Produktion*, oprettes der produktionsordreforslag.</span><span class="sxs-lookup"><span data-stu-id="7075e-108">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="7075e-109">Disse produktionsordreforslag omfatter oplysninger om den aktive stykliste (BOM) og rute-id'et fra den relaterede produktionsopsætning.</span><span class="sxs-lookup"><span data-stu-id="7075e-109">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="7075e-110">Krav fra styklister</span><span class="sxs-lookup"><span data-stu-id="7075e-110">Requirements from BOMs</span></span>

<span data-ttu-id="7075e-111">Styklisteoplysninger anvendes under varedisponering.</span><span class="sxs-lookup"><span data-stu-id="7075e-111">BOM information is honored during master planning.</span></span> <span data-ttu-id="7075e-112">Outputforslaget omfatter materialeforsyning for at dække relateret materialebehov til produktion.</span><span class="sxs-lookup"><span data-stu-id="7075e-112">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="7075e-113">Under varedisponering bruges den aktuelle, aktive stykliste til at bestemme, hvilke materialer der kræves til produktionen.</span><span class="sxs-lookup"><span data-stu-id="7075e-113">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="7075e-114">Dette trin udføres gennem alle niveauer i styklistestrukturen, der er relateret til den nødvendige produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="7075e-114">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="7075e-115">Materialebehovet opfyldes ved hjælp af tilgængeligt lager, eksisterende forsyning i ordren og godkendte ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="7075e-115">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="7075e-116">Hvis der skal bruges yderligere materialer på et hvilket som helst sted, oprettes der et ordreforslag, der skal dække behovet.</span><span class="sxs-lookup"><span data-stu-id="7075e-116">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="7075e-117">Planlægning under autorisation</span><span class="sxs-lookup"><span data-stu-id="7075e-117">Scheduling during firming</span></span>

<span data-ttu-id="7075e-118">Produktionsordreforslag omfatter det rute-id, der kræves ved produktionsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="7075e-118">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="7075e-119">Planlægning af support under kørslen af disponeringen for ordreforslag afventer dog.</span><span class="sxs-lookup"><span data-stu-id="7075e-119">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="7075e-120">Rute-id'et bruges til at planlægge produktionsordreforslag under autorisation.</span><span class="sxs-lookup"><span data-stu-id="7075e-120">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="7075e-121">Leveringstiden for produktionsordreforslag kan derfor være forskellig fra leveringstiden for relaterede planlagte, autoriserede produktionsordrer, der oprettes fra dem, som beskrevet her:</span><span class="sxs-lookup"><span data-stu-id="7075e-121">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="7075e-122">**Produktionsordreforslag** – Leveringstiden er baseret på den statiske leveringstid fra det frigivne produkt.</span><span class="sxs-lookup"><span data-stu-id="7075e-122">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="7075e-123">**Autoriseret produktionsordre** – Leveringstiden er baseret på planlægning, der bruger ruteoplysninger og relaterede ressourcebegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="7075e-123">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="7075e-124">Yderligere oplysninger om forventet tilgængelighed af funktioner finder du i [Analyse af tilpasning af Planlægningsoptimering](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7075e-124">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="7075e-125">Hvis du er afhængig af, at produktionsfunktionaliteten endnu ikke er tilgængelig for Planlægningsoptimering, kan du fortsætte med at bruge det indbyggede varedisponeringsprogram.</span><span class="sxs-lookup"><span data-stu-id="7075e-125">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="7075e-126">Der kræves ingen undtagelse.</span><span class="sxs-lookup"><span data-stu-id="7075e-126">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="7075e-127">Forsinkelser</span><span class="sxs-lookup"><span data-stu-id="7075e-127">Delays</span></span>

<span data-ttu-id="7075e-128">Hvis leveringstiden for påkrævet materiale er længere end perioden mellem dags dato og datoen for materialebehov, forsinkes ordreforslaget for det påkrævede materiale og den relaterede produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="7075e-128">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="7075e-129">For ordreforslag beregnes forsinkelsen (i dage) på grundlag af leveringstiden fra det frigivne produkt.</span><span class="sxs-lookup"><span data-stu-id="7075e-129">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="7075e-130">Oplysningerne om forsinkelsen udbredes derefter gennem alle niveauer af styklistestrukturen.</span><span class="sxs-lookup"><span data-stu-id="7075e-130">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="7075e-131">Du kan derfor følge indvirkningen af forsinkede råmaterialer hele vejen frem til debitorsalgsordren.</span><span class="sxs-lookup"><span data-stu-id="7075e-131">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="7075e-132">Ændre ordreforslag</span><span class="sxs-lookup"><span data-stu-id="7075e-132">Modifying planned orders</span></span>

<span data-ttu-id="7075e-133">Når du ændrer oplysningerne i et ordreforslag, modtager du følgende meddelelse: "Bemærk, at indvirkningen af manuelle ændringer på ordreforslag ikke afspejles i resten af planen, før næste varedisponeringskørsel."</span><span class="sxs-lookup"><span data-stu-id="7075e-133">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="7075e-134">Hvis du vil ændre oplysningerne i et ordreforslag og se, hvordan det påvirker de relaterede materialebehov, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="7075e-134">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="7075e-135">Opdater ordreforslaget.</span><span class="sxs-lookup"><span data-stu-id="7075e-135">Update the planned order.</span></span>
2. <span data-ttu-id="7075e-136">Godkend ordreforslaget.</span><span class="sxs-lookup"><span data-stu-id="7075e-136">Approve the planned order.</span></span>
3. <span data-ttu-id="7075e-137">Kør varedisponering.</span><span class="sxs-lookup"><span data-stu-id="7075e-137">Run master planning.</span></span>

<span data-ttu-id="7075e-138">Når du kører varedisponering, skal du ikke bruge filtre, hvis produktionsordreforslag medtages.</span><span class="sxs-lookup"><span data-stu-id="7075e-138">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="7075e-139">Du kan finde flere oplysninger i afsnittet [Filtre](#filters) nedenfor i dette emne.</span><span class="sxs-lookup"><span data-stu-id="7075e-139">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="7075e-140">Hvis leveringsdatoen for ordreforslaget ændres til en senere dato, kan behovet udlignes i forhold til et nyt ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="7075e-140">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="7075e-141">Denne funktionsmåde forekommer, når den nye leveringsdato medfører forsinkelse for den udlignede efterspørgsel, men forsinkelsen kan undgås ifølge indstillingerne for leveringstiden.</span><span class="sxs-lookup"><span data-stu-id="7075e-141">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="7075e-142">Siden Udfoldning</span><span class="sxs-lookup"><span data-stu-id="7075e-142">Explosion page</span></span>

<span data-ttu-id="7075e-143">Du kan bruge siden **Udfoldning** til at analysere den efterspørgsel, der kræves i forbindelse med en bestemt produktionsordre eller et bestemt produktionsordreforslag, den relaterede disponering og udligningsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="7075e-143">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="7075e-144">Oplysninger på siden **Udfoldning** opdateres under varedisponering.</span><span class="sxs-lookup"><span data-stu-id="7075e-144">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="7075e-145">Du kan ikke opdatere oplysningerne direkte fra siden **Udfoldning**.</span><span class="sxs-lookup"><span data-stu-id="7075e-145">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="7075e-146">Filtre</span><span class="sxs-lookup"><span data-stu-id="7075e-146">Filters</span></span>

<span data-ttu-id="7075e-147">I forbindelse med planlægningsscenarier, der omfatter produktion, anbefales det, at du undgår filtrerede varedisponeringskørsler.</span><span class="sxs-lookup"><span data-stu-id="7075e-147">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="7075e-148">Hvis du vil sikre, at Planlægningsoptimering har de oplysninger, der er nødvendige for at beregne det korrekte resultat, skal du medtage alle produkter, der har relation til produkter, i hele styklistestrukturen i ordreforslaget.</span><span class="sxs-lookup"><span data-stu-id="7075e-148">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="7075e-149">Selvom afhængige underordnede varer registreres og medtages i varedisponeringskørsler, når det indbyggede varedisponeringsprogram bruges, udfører Planlægningsoptimering ikke denne handling.</span><span class="sxs-lookup"><span data-stu-id="7075e-149">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="7075e-150">Hvis f.eks. en enkelt rulle fra styklistestrukturen i produkt A også bruges til at producere produkt B, skal alle produkter i styklistestrukturen for produkter A og B medtages i filteret.</span><span class="sxs-lookup"><span data-stu-id="7075e-150">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="7075e-151">Da det kan være meget kompliceret at sikre, at alle produkter indgår i filteret, anbefales det, at du undgår filtrerede varedisponeringskørsler, når der er produktionsordrer involveret.</span><span class="sxs-lookup"><span data-stu-id="7075e-151">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>
