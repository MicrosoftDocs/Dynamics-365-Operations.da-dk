---
title: Oprette en ny lageropbygning
description: Dette emne beskriver, hvordan du konfigurerer oplysninger om lokationer på et lagersted.
author: perlynne
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a329df85c339c90e4bdc620c8a63837ebc19a7c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833971"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="cb97b-103">Oprette en ny lageropbygning</span><span class="sxs-lookup"><span data-stu-id="cb97b-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb97b-104">Dette emne beskriver, hvordan du konfigurerer oplysninger om lokationer på et lagersted.</span><span class="sxs-lookup"><span data-stu-id="cb97b-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="cb97b-105">Dette gælder for kun for lagersteder, der er oprettet ved hjælp af "grundlæggende lagerfunktioner" i modulet Lagerstyring, ikke for lagersteder, der er oprettet i modulet Lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="cb97b-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="cb97b-106">Du kan bruge denne procedure på demofirmaet USMF eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="cb97b-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="cb97b-107">Angiv lokalitetens standardkapacitet</span><span class="sxs-lookup"><span data-stu-id="cb97b-107">Set the default location capacity</span></span>
1. <span data-ttu-id="cb97b-108">Gå i navigationsruden til **Moduler > Lagerstyring > Opsætning > Parametre til lager- og lokationsstyring**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="cb97b-109">Vælg fanen **Lokationer**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="cb97b-110">Angiv et tal i feltet **Standardbredde**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="cb97b-111">Angiv et tal i feltet **Standarddybde**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="cb97b-112">Angiv et tal i feltet **Standardhøjde**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="cb97b-113">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-113">Select **Save**.</span></span>
7. <span data-ttu-id="cb97b-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cb97b-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="cb97b-115">Definer formatet for navnet på lokaliteten</span><span class="sxs-lookup"><span data-stu-id="cb97b-115">Define the location name format</span></span>
1. <span data-ttu-id="cb97b-116">I navigationsruden skal du gå til **Moduler > Lagerstyring > Opsætning > Lageropdeling > Lagersteder**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="cb97b-117">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-117">Select **New**.</span></span>
3. <span data-ttu-id="cb97b-118">Skriv en værdi i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="cb97b-119">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="cb97b-120">Vælg den ønskede post i opslaget til feltet **Sted**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="cb97b-121">Slå udvidelsen af sektionen **Lokationsnavne** til/fra.</span><span class="sxs-lookup"><span data-stu-id="cb97b-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="cb97b-122">Indstillingerne i denne sektion definerer standardformatet for navne på lokaliteter.</span><span class="sxs-lookup"><span data-stu-id="cb97b-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="cb97b-123">I vores eksempel medtager vi gangnummer, reolnummer og hyldenummer.</span><span class="sxs-lookup"><span data-stu-id="cb97b-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="cb97b-124">Angiv indstillingen **Medtag gang** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="cb97b-125">Angiv indstillingen **Medtag reol** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="cb97b-126">Angiv en værdi for reolen i feltet **Format**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="cb97b-127">Angiv indstillingen **Medtag hylde** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="cb97b-128">Angiv en værdi for hylden i feltet **Format**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="cb97b-129">Definer lagerstedslokationer</span><span class="sxs-lookup"><span data-stu-id="cb97b-129">Define warehouse locations</span></span>
1. <span data-ttu-id="cb97b-130">Vælg **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="cb97b-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="cb97b-131">Vælg **Guiden Lokation**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="cb97b-132">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-132">Select **Next**.</span></span>
4. <span data-ttu-id="cb97b-133">Fjern markeringen af indstillingen **Forsendelsesområder**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="cb97b-134">Fjern markeringen af indstillingen **Bulkvarelokationer**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="cb97b-135">Vælg **Næste**, indtil du kan vælge **Udfør**.</span><span class="sxs-lookup"><span data-stu-id="cb97b-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="cb97b-136">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cb97b-136">Close the page.</span></span>
8. <span data-ttu-id="cb97b-137">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="cb97b-137">Refresh the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]