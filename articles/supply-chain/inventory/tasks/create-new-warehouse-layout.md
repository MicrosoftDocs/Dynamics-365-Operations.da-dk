---
title: Oprette en ny lageropbygning
description: Dette emne beskriver, hvordan du konfigurerer oplysninger om lokationer på et lagersted.
author: perlynne
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09666e95cc90913f1bf8555b9ff2c48aa55369ed
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214015"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="849d6-103">Oprette en ny lageropbygning</span><span class="sxs-lookup"><span data-stu-id="849d6-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="849d6-104">Dette emne beskriver, hvordan du konfigurerer oplysninger om lokationer på et lagersted.</span><span class="sxs-lookup"><span data-stu-id="849d6-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="849d6-105">Dette gælder for kun for lagersteder, der er oprettet ved hjælp af "grundlæggende lagerfunktioner" i modulet Lagerstyring, ikke for lagersteder, der er oprettet i modulet Lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="849d6-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="849d6-106">Du kan bruge denne procedure på demofirmaet USMF eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="849d6-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="849d6-107">Angiv lokalitetens standardkapacitet</span><span class="sxs-lookup"><span data-stu-id="849d6-107">Set the default location capacity</span></span>
1. <span data-ttu-id="849d6-108">Gå i navigationsruden til **Moduler > Lagerstyring > Opsætning > Parametre til lager- og lokationsstyring**.</span><span class="sxs-lookup"><span data-stu-id="849d6-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="849d6-109">Vælg fanen **Lokationer**.</span><span class="sxs-lookup"><span data-stu-id="849d6-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="849d6-110">Angiv et tal i feltet **Standardbredde**.</span><span class="sxs-lookup"><span data-stu-id="849d6-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="849d6-111">Angiv et tal i feltet **Standarddybde**.</span><span class="sxs-lookup"><span data-stu-id="849d6-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="849d6-112">Angiv et tal i feltet **Standardhøjde**.</span><span class="sxs-lookup"><span data-stu-id="849d6-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="849d6-113">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="849d6-113">Select **Save**.</span></span>
7. <span data-ttu-id="849d6-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="849d6-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="849d6-115">Definer formatet for navnet på lokaliteten</span><span class="sxs-lookup"><span data-stu-id="849d6-115">Define the location name format</span></span>
1. <span data-ttu-id="849d6-116">I navigationsruden skal du gå til **Moduler > Lagerstyring > Opsætning > Lageropdeling > Lagersteder**.</span><span class="sxs-lookup"><span data-stu-id="849d6-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="849d6-117">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="849d6-117">Select **New**.</span></span>
3. <span data-ttu-id="849d6-118">Skriv en værdi i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="849d6-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="849d6-119">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="849d6-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="849d6-120">Vælg den ønskede post i opslaget til feltet **Sted**.</span><span class="sxs-lookup"><span data-stu-id="849d6-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="849d6-121">Slå udvidelsen af sektionen **Lokationsnavne** til/fra.</span><span class="sxs-lookup"><span data-stu-id="849d6-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="849d6-122">Indstillingerne i denne sektion definerer standardformatet for navne på lokaliteter.</span><span class="sxs-lookup"><span data-stu-id="849d6-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="849d6-123">I vores eksempel medtager vi gangnummer, reolnummer og hyldenummer.</span><span class="sxs-lookup"><span data-stu-id="849d6-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="849d6-124">Angiv indstillingen **Medtag gang** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="849d6-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="849d6-125">Angiv indstillingen **Medtag reol** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="849d6-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="849d6-126">Angiv en værdi for reolen i feltet **Format**.</span><span class="sxs-lookup"><span data-stu-id="849d6-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="849d6-127">Angiv indstillingen **Medtag hylde** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="849d6-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="849d6-128">Angiv en værdi for hylden i feltet **Format**.</span><span class="sxs-lookup"><span data-stu-id="849d6-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="849d6-129">Definer lagerstedslokationer</span><span class="sxs-lookup"><span data-stu-id="849d6-129">Define warehouse locations</span></span>
1. <span data-ttu-id="849d6-130">Vælg **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="849d6-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="849d6-131">Vælg **Guiden Lokation**.</span><span class="sxs-lookup"><span data-stu-id="849d6-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="849d6-132">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="849d6-132">Select **Next**.</span></span>
4. <span data-ttu-id="849d6-133">Fjern markeringen af indstillingen **Forsendelsesområder**.</span><span class="sxs-lookup"><span data-stu-id="849d6-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="849d6-134">Fjern markeringen af indstillingen **Bulkvarelokationer**.</span><span class="sxs-lookup"><span data-stu-id="849d6-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="849d6-135">Vælg **Næste**, indtil du kan vælge **Udfør**.</span><span class="sxs-lookup"><span data-stu-id="849d6-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="849d6-136">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="849d6-136">Close the page.</span></span>
8. <span data-ttu-id="849d6-137">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="849d6-137">Refresh the page.</span></span>

