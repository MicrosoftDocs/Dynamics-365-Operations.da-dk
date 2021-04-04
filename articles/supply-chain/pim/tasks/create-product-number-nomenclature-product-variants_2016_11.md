---
title: Oprette et produktnummernomenklatur for konfigurerede produktvarianter
description: Denne procedure viser, hvordan du konfigurerer en nomenklatur for produktnumre for konfigurerede produktvarianter, og hvordan den kan knyttes til en produktmaster, der kan konfigureres.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07922a20d5c99640f32bb28ddddaffe846440667
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258869"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="73656-103">Oprette et produktnummernomenklatur for konfigurerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="73656-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="73656-104">Denne procedure viser, hvordan du konfigurerer en nomenklatur for produktnumre for konfigurerede produktvarianter, og hvordan den kan knyttes til en produktmaster, der kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="73656-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="73656-105">Denne fremgangsmåde viser også, hvordan du kan opbygge en konfigurationsnomenklatur en produktkonfigurations modelkomponent.</span><span class="sxs-lookup"><span data-stu-id="73656-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="73656-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="73656-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="73656-107">Den nye nomenklatur for produktnumre er knyttet til produktmasteren D0004.</span><span class="sxs-lookup"><span data-stu-id="73656-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="73656-108">Denne opgave udføres normalt af en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="73656-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="73656-109">Opret en nomenklatur for produktnummer</span><span class="sxs-lookup"><span data-stu-id="73656-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="73656-110">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="73656-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="73656-111">Klik på Produktnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="73656-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="73656-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="73656-112">Click New.</span></span>
4. <span data-ttu-id="73656-113">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="73656-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="73656-114">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="73656-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="73656-115">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="73656-115">Click Add.</span></span>
7. <span data-ttu-id="73656-116">Klik på Produktmasternummer.</span><span class="sxs-lookup"><span data-stu-id="73656-116">Click Product master number.</span></span>
8. <span data-ttu-id="73656-117">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="73656-117">Click Add.</span></span>
9. <span data-ttu-id="73656-118">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="73656-118">Click Text constant.</span></span>
10. <span data-ttu-id="73656-119">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73656-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="73656-120">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="73656-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="73656-121">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="73656-121">Click Add.</span></span>
13. <span data-ttu-id="73656-122">Klik på Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="73656-122">Click Configuration.</span></span>
14. <span data-ttu-id="73656-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="73656-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="73656-124">Tildel nomenklaturen for produktnummer til en produktmaster</span><span class="sxs-lookup"><span data-stu-id="73656-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="73656-125">Klik på Produktmastere.</span><span class="sxs-lookup"><span data-stu-id="73656-125">Click Product masters.</span></span>
2. <span data-ttu-id="73656-126">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="73656-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="73656-127">Filtrer f.eks. efter feltet Produktnummer med værdien "D".</span><span class="sxs-lookup"><span data-stu-id="73656-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="73656-128">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73656-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="73656-129">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="73656-129">Click Edit.</span></span>
5. <span data-ttu-id="73656-130">Vælg Ja i feltet Brug nomenklatur.</span><span class="sxs-lookup"><span data-stu-id="73656-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="73656-131">Indtast eller vælg en værdi i feltet Nomenklatur for produktvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="73656-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="73656-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="73656-132">Close the page.</span></span>
8. <span data-ttu-id="73656-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="73656-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="73656-134">Opret nomenklatur for en komponent i en produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="73656-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="73656-135">Klik på Produktkonfigurationsmodeller.</span><span class="sxs-lookup"><span data-stu-id="73656-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="73656-136">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="73656-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="73656-137">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73656-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="73656-138">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="73656-138">Click Edit.</span></span>
5. <span data-ttu-id="73656-139">Vælg Ja i feltet Brug konfigurationsnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="73656-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="73656-140">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="73656-140">Click Add.</span></span>
7. <span data-ttu-id="73656-141">Klik på Attributværdi.</span><span class="sxs-lookup"><span data-stu-id="73656-141">Click Attribute value.</span></span>
8. <span data-ttu-id="73656-142">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73656-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="73656-143">Indtast eller vælg en værdi i feltet Attribut.</span><span class="sxs-lookup"><span data-stu-id="73656-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="73656-144">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="73656-144">Click Add.</span></span>
11. <span data-ttu-id="73656-145">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="73656-145">Click Text constant.</span></span>
12. <span data-ttu-id="73656-146">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73656-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="73656-147">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="73656-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="73656-148">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="73656-148">Click Add.</span></span>
15. <span data-ttu-id="73656-149">Klik på Attributværdi.</span><span class="sxs-lookup"><span data-stu-id="73656-149">Click Attribute value.</span></span>
16. <span data-ttu-id="73656-150">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73656-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="73656-151">Indtast eller vælg en værdi i feltet Attribut.</span><span class="sxs-lookup"><span data-stu-id="73656-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="73656-152">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="73656-152">Click Add.</span></span>
19. <span data-ttu-id="73656-153">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="73656-153">Click Text constant.</span></span>
20. <span data-ttu-id="73656-154">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73656-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="73656-155">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="73656-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="73656-156">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="73656-156">Click Add.</span></span>
23. <span data-ttu-id="73656-157">Klik på Attributværdi.</span><span class="sxs-lookup"><span data-stu-id="73656-157">Click Attribute value.</span></span>
24. <span data-ttu-id="73656-158">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73656-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="73656-159">Indtast eller vælg en værdi i feltet Attribut.</span><span class="sxs-lookup"><span data-stu-id="73656-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="73656-160">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="73656-160">Click Add.</span></span>
27. <span data-ttu-id="73656-161">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="73656-161">Click Text constant.</span></span>
28. <span data-ttu-id="73656-162">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73656-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="73656-163">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="73656-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="73656-164">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="73656-164">Click Add.</span></span>
31. <span data-ttu-id="73656-165">Klik på Attributværdi.</span><span class="sxs-lookup"><span data-stu-id="73656-165">Click Attribute value.</span></span>
32. <span data-ttu-id="73656-166">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73656-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="73656-167">Indtast eller vælg en værdi i feltet Attribut.</span><span class="sxs-lookup"><span data-stu-id="73656-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="73656-168">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="73656-168">Click Add.</span></span>
35. <span data-ttu-id="73656-169">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="73656-169">Click Text constant.</span></span>
36. <span data-ttu-id="73656-170">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73656-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="73656-171">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="73656-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="73656-172">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="73656-172">Click Add.</span></span>
39. <span data-ttu-id="73656-173">Klik på Nummerserieværdi.</span><span class="sxs-lookup"><span data-stu-id="73656-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="73656-174">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73656-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="73656-175">Skriv eller vælg en værdi i feltet Nummerserie.</span><span class="sxs-lookup"><span data-stu-id="73656-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="73656-176">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="73656-176">Close the page.</span></span>
43. <span data-ttu-id="73656-177">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="73656-177">Close the page.</span></span>
44. <span data-ttu-id="73656-178">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="73656-178">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]