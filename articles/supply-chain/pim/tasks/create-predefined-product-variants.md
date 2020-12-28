---
title: Oprette foruddefinerede produktvarianter
description: Denne procedure fører dig gennem oprettelsen af produktvarianter for en produktmaster ved hjælp af kombinationer af produktdimensioner.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6fa9c6d4862a49bbf0b5ecbb8c0c3d573e0f49e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424628"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="6eab2-103">Oprette foruddefinerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="6eab2-103">Create predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6eab2-104">Denne procedure fører dig gennem oprettelsen af produktvarianter for en produktmaster ved hjælp af kombinationer af produktdimensioner.</span><span class="sxs-lookup"><span data-stu-id="6eab2-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="6eab2-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="6eab2-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="6eab2-106">Oprette en produktmaster</span><span class="sxs-lookup"><span data-stu-id="6eab2-106">Create a product master</span></span>
1. <span data-ttu-id="6eab2-107">Gå til Administration af produktoplysninger > Produkter > Produktmastere.</span><span class="sxs-lookup"><span data-stu-id="6eab2-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="6eab2-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6eab2-108">Click New.</span></span>
3. <span data-ttu-id="6eab2-109">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="6eab2-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="6eab2-110">Manuel indtastning af et produktnummer kræves kun, hvis der ingen nummerserie er indstillet for produktnummerfeltet.</span><span class="sxs-lookup"><span data-stu-id="6eab2-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="6eab2-111">Med andre ord kan du springe dette trin over, hvis nummerserien er indstillet for feltet.</span><span class="sxs-lookup"><span data-stu-id="6eab2-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="6eab2-112">Angiv en værdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="6eab2-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="6eab2-113">Indtast eller vælg en værdi i feltet Produktdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="6eab2-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="6eab2-114">Vælg produktdimensionsgruppen SizeCol (størrelse og farve).</span><span class="sxs-lookup"><span data-stu-id="6eab2-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="6eab2-115">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6eab2-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="6eab2-116">Tilføje produktdimensioner</span><span class="sxs-lookup"><span data-stu-id="6eab2-116">Add product dimensions</span></span>
1. <span data-ttu-id="6eab2-117">Klik på Produktdimensioner.</span><span class="sxs-lookup"><span data-stu-id="6eab2-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="6eab2-118">Dette eksempel viser, hvordan du manuelt angiver produktdimensioner.</span><span class="sxs-lookup"><span data-stu-id="6eab2-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="6eab2-119">Du kan også vælge en størrelses-, farve- eller typografigruppe, der indeholder de produktdimensionsværdier, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="6eab2-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="6eab2-120">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6eab2-120">Click New.</span></span>
3. <span data-ttu-id="6eab2-121">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6eab2-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6eab2-122">Indtast eller vælg en værdi i feltet Størrelse.</span><span class="sxs-lookup"><span data-stu-id="6eab2-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="6eab2-123">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6eab2-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="6eab2-124">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6eab2-124">Click New.</span></span>
7. <span data-ttu-id="6eab2-125">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6eab2-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="6eab2-126">Indtast eller vælg en værdi i feltet Størrelse.</span><span class="sxs-lookup"><span data-stu-id="6eab2-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="6eab2-127">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6eab2-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="6eab2-128">Klik på fanen Farver.</span><span class="sxs-lookup"><span data-stu-id="6eab2-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="6eab2-129">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6eab2-129">Click New.</span></span>
12. <span data-ttu-id="6eab2-130">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6eab2-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="6eab2-131">Indtast eller vælg en værdi i feltet Farve.</span><span class="sxs-lookup"><span data-stu-id="6eab2-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="6eab2-132">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6eab2-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="6eab2-133">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6eab2-133">Click New.</span></span>
16. <span data-ttu-id="6eab2-134">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6eab2-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="6eab2-135">Indtast eller vælg en værdi i feltet Farve.</span><span class="sxs-lookup"><span data-stu-id="6eab2-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="6eab2-136">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6eab2-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="6eab2-137">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="6eab2-137">Click Save.</span></span>
20. <span data-ttu-id="6eab2-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6eab2-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="6eab2-139">Generere produktvarianter</span><span class="sxs-lookup"><span data-stu-id="6eab2-139">Generate product variants</span></span>
1. <span data-ttu-id="6eab2-140">Klik på Produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="6eab2-140">Click Product variants.</span></span>
2. <span data-ttu-id="6eab2-141">Klik på Forslag til varianter.</span><span class="sxs-lookup"><span data-stu-id="6eab2-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="6eab2-142">Klik på Vælg alle.</span><span class="sxs-lookup"><span data-stu-id="6eab2-142">Click Select all.</span></span>
    * <span data-ttu-id="6eab2-143">I dette eksempel vælges alle mulige varianter.</span><span class="sxs-lookup"><span data-stu-id="6eab2-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="6eab2-144">Hvis kun en delmængde af de mulige produktdimensionskombinationer skal bruges til at oprette varianter, kan du vælge de enkelte poster.</span><span class="sxs-lookup"><span data-stu-id="6eab2-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="6eab2-145">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="6eab2-145">Click Create.</span></span>
    * <span data-ttu-id="6eab2-146">Du kan generere beskrivelser for alle de varianter, der er baseret på en kombination af dimensionsværdier for produktet.</span><span class="sxs-lookup"><span data-stu-id="6eab2-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="6eab2-147">Beskrivelserne er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="6eab2-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="6eab2-148">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="6eab2-148">Click Save.</span></span>

