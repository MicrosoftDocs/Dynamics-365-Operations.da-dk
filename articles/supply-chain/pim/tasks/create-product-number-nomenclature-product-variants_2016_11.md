---
title: Oprette et produktnummernomenklatur for konfigurerede produktvarianter
description: Denne procedure viser, hvordan du konfigurerer en nomenklatur for produktnumre for konfigurerede produktvarianter, og hvordan den kan knyttes til en produktmaster, der kan konfigureres.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a837721db5281b0626f37b7a793349b91afa6f85
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147750"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="ccd23-103">Oprette et produktnummernomenklatur for konfigurerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="ccd23-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ccd23-104">Denne procedure viser, hvordan du konfigurerer en nomenklatur for produktnumre for konfigurerede produktvarianter, og hvordan den kan knyttes til en produktmaster, der kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="ccd23-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="ccd23-105">Denne fremgangsmåde viser også, hvordan du kan opbygge en konfigurationsnomenklatur en produktkonfigurations modelkomponent.</span><span class="sxs-lookup"><span data-stu-id="ccd23-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="ccd23-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="ccd23-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ccd23-107">Den nye nomenklatur for produktnumre er knyttet til produktmasteren D0004.</span><span class="sxs-lookup"><span data-stu-id="ccd23-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="ccd23-108">Denne opgave udføres normalt af en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="ccd23-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="ccd23-109">Opret en nomenklatur for produktnummer</span><span class="sxs-lookup"><span data-stu-id="ccd23-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="ccd23-110">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="ccd23-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ccd23-111">Klik på Produktnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="ccd23-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="ccd23-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="ccd23-112">Click New.</span></span>
4. <span data-ttu-id="ccd23-113">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ccd23-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ccd23-114">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ccd23-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="ccd23-115">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ccd23-115">Click Add.</span></span>
7. <span data-ttu-id="ccd23-116">Klik på Produktmasternummer.</span><span class="sxs-lookup"><span data-stu-id="ccd23-116">Click Product master number.</span></span>
8. <span data-ttu-id="ccd23-117">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ccd23-117">Click Add.</span></span>
9. <span data-ttu-id="ccd23-118">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="ccd23-118">Click Text constant.</span></span>
10. <span data-ttu-id="ccd23-119">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ccd23-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="ccd23-120">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="ccd23-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="ccd23-121">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ccd23-121">Click Add.</span></span>
13. <span data-ttu-id="ccd23-122">Klik på Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ccd23-122">Click Configuration.</span></span>
14. <span data-ttu-id="ccd23-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ccd23-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="ccd23-124">Tildel nomenklaturen for produktnummer til en produktmaster</span><span class="sxs-lookup"><span data-stu-id="ccd23-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="ccd23-125">Klik på Produktmastere.</span><span class="sxs-lookup"><span data-stu-id="ccd23-125">Click Product masters.</span></span>
2. <span data-ttu-id="ccd23-126">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="ccd23-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ccd23-127">Filtrer f.eks. efter feltet Produktnummer med værdien "D".</span><span class="sxs-lookup"><span data-stu-id="ccd23-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="ccd23-128">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ccd23-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ccd23-129">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="ccd23-129">Click Edit.</span></span>
5. <span data-ttu-id="ccd23-130">Vælg Ja i feltet Brug nomenklatur.</span><span class="sxs-lookup"><span data-stu-id="ccd23-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="ccd23-131">Indtast eller vælg en værdi i feltet Nomenklatur for produktvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="ccd23-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="ccd23-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ccd23-132">Close the page.</span></span>
8. <span data-ttu-id="ccd23-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ccd23-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="ccd23-134">Opret nomenklatur for en komponent i en produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="ccd23-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="ccd23-135">Klik på Produktkonfigurationsmodeller.</span><span class="sxs-lookup"><span data-stu-id="ccd23-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="ccd23-136">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ccd23-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ccd23-137">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ccd23-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ccd23-138">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="ccd23-138">Click Edit.</span></span>
5. <span data-ttu-id="ccd23-139">Vælg Ja i feltet Brug konfigurationsnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="ccd23-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="ccd23-140">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ccd23-140">Click Add.</span></span>
7. <span data-ttu-id="ccd23-141">Klik på Attributværdi.</span><span class="sxs-lookup"><span data-stu-id="ccd23-141">Click Attribute value.</span></span>
8. <span data-ttu-id="ccd23-142">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ccd23-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ccd23-143">Indtast eller vælg en værdi i feltet Attribut.</span><span class="sxs-lookup"><span data-stu-id="ccd23-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="ccd23-144">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ccd23-144">Click Add.</span></span>
11. <span data-ttu-id="ccd23-145">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="ccd23-145">Click Text constant.</span></span>
12. <span data-ttu-id="ccd23-146">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ccd23-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="ccd23-147">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="ccd23-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="ccd23-148">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ccd23-148">Click Add.</span></span>
15. <span data-ttu-id="ccd23-149">Klik på Attributværdi.</span><span class="sxs-lookup"><span data-stu-id="ccd23-149">Click Attribute value.</span></span>
16. <span data-ttu-id="ccd23-150">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ccd23-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="ccd23-151">Indtast eller vælg en værdi i feltet Attribut.</span><span class="sxs-lookup"><span data-stu-id="ccd23-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="ccd23-152">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ccd23-152">Click Add.</span></span>
19. <span data-ttu-id="ccd23-153">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="ccd23-153">Click Text constant.</span></span>
20. <span data-ttu-id="ccd23-154">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ccd23-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="ccd23-155">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="ccd23-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="ccd23-156">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ccd23-156">Click Add.</span></span>
23. <span data-ttu-id="ccd23-157">Klik på Attributværdi.</span><span class="sxs-lookup"><span data-stu-id="ccd23-157">Click Attribute value.</span></span>
24. <span data-ttu-id="ccd23-158">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ccd23-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="ccd23-159">Indtast eller vælg en værdi i feltet Attribut.</span><span class="sxs-lookup"><span data-stu-id="ccd23-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="ccd23-160">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ccd23-160">Click Add.</span></span>
27. <span data-ttu-id="ccd23-161">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="ccd23-161">Click Text constant.</span></span>
28. <span data-ttu-id="ccd23-162">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ccd23-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="ccd23-163">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="ccd23-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="ccd23-164">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ccd23-164">Click Add.</span></span>
31. <span data-ttu-id="ccd23-165">Klik på Attributværdi.</span><span class="sxs-lookup"><span data-stu-id="ccd23-165">Click Attribute value.</span></span>
32. <span data-ttu-id="ccd23-166">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ccd23-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="ccd23-167">Indtast eller vælg en værdi i feltet Attribut.</span><span class="sxs-lookup"><span data-stu-id="ccd23-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="ccd23-168">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ccd23-168">Click Add.</span></span>
35. <span data-ttu-id="ccd23-169">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="ccd23-169">Click Text constant.</span></span>
36. <span data-ttu-id="ccd23-170">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ccd23-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="ccd23-171">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="ccd23-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="ccd23-172">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ccd23-172">Click Add.</span></span>
39. <span data-ttu-id="ccd23-173">Klik på Nummerserieværdi.</span><span class="sxs-lookup"><span data-stu-id="ccd23-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="ccd23-174">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ccd23-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="ccd23-175">Skriv eller vælg en værdi i feltet Nummerserie.</span><span class="sxs-lookup"><span data-stu-id="ccd23-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="ccd23-176">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ccd23-176">Close the page.</span></span>
43. <span data-ttu-id="ccd23-177">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ccd23-177">Close the page.</span></span>
44. <span data-ttu-id="ccd23-178">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ccd23-178">Close the page.</span></span>

