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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f75d7e493255b9c09c10b121f388854861cb0fc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424625"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="7cf06-103">Oprette et produktnummernomenklatur for konfigurerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="7cf06-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7cf06-104">Denne procedure viser, hvordan du konfigurerer en nomenklatur for produktnumre for konfigurerede produktvarianter, og hvordan den kan knyttes til en produktmaster, der kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="7cf06-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="7cf06-105">Denne fremgangsmåde viser også, hvordan du kan opbygge en konfigurationsnomenklatur en produktkonfigurations modelkomponent.</span><span class="sxs-lookup"><span data-stu-id="7cf06-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="7cf06-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="7cf06-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7cf06-107">Den nye nomenklatur for produktnumre er knyttet til produktmasteren D0004.</span><span class="sxs-lookup"><span data-stu-id="7cf06-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="7cf06-108">Denne opgave udføres normalt af en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="7cf06-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="7cf06-109">Opret en nomenklatur for produktnummer</span><span class="sxs-lookup"><span data-stu-id="7cf06-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="7cf06-110">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="7cf06-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="7cf06-111">Klik på Produktnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="7cf06-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="7cf06-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7cf06-112">Click New.</span></span>
4. <span data-ttu-id="7cf06-113">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="7cf06-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="7cf06-114">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="7cf06-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="7cf06-115">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7cf06-115">Click Add.</span></span>
7. <span data-ttu-id="7cf06-116">Klik på Produktmasternummer.</span><span class="sxs-lookup"><span data-stu-id="7cf06-116">Click Product master number.</span></span>
8. <span data-ttu-id="7cf06-117">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7cf06-117">Click Add.</span></span>
9. <span data-ttu-id="7cf06-118">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="7cf06-118">Click Text constant.</span></span>
10. <span data-ttu-id="7cf06-119">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7cf06-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="7cf06-120">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="7cf06-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="7cf06-121">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7cf06-121">Click Add.</span></span>
13. <span data-ttu-id="7cf06-122">Klik på Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7cf06-122">Click Configuration.</span></span>
14. <span data-ttu-id="7cf06-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7cf06-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="7cf06-124">Tildel nomenklaturen for produktnummer til en produktmaster</span><span class="sxs-lookup"><span data-stu-id="7cf06-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="7cf06-125">Klik på Produktmastere.</span><span class="sxs-lookup"><span data-stu-id="7cf06-125">Click Product masters.</span></span>
2. <span data-ttu-id="7cf06-126">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="7cf06-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="7cf06-127">Filtrer f.eks. efter feltet Produktnummer med værdien "D".</span><span class="sxs-lookup"><span data-stu-id="7cf06-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="7cf06-128">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7cf06-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7cf06-129">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="7cf06-129">Click Edit.</span></span>
5. <span data-ttu-id="7cf06-130">Vælg Ja i feltet Brug nomenklatur.</span><span class="sxs-lookup"><span data-stu-id="7cf06-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="7cf06-131">Indtast eller vælg en værdi i feltet Nomenklatur for produktvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="7cf06-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="7cf06-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7cf06-132">Close the page.</span></span>
8. <span data-ttu-id="7cf06-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7cf06-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="7cf06-134">Opret nomenklatur for en komponent i en produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="7cf06-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="7cf06-135">Klik på Produktkonfigurationsmodeller.</span><span class="sxs-lookup"><span data-stu-id="7cf06-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="7cf06-136">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="7cf06-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7cf06-137">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7cf06-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7cf06-138">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="7cf06-138">Click Edit.</span></span>
5. <span data-ttu-id="7cf06-139">Vælg Ja i feltet Brug konfigurationsnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="7cf06-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="7cf06-140">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7cf06-140">Click Add.</span></span>
7. <span data-ttu-id="7cf06-141">Klik på Attributværdi.</span><span class="sxs-lookup"><span data-stu-id="7cf06-141">Click Attribute value.</span></span>
8. <span data-ttu-id="7cf06-142">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7cf06-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="7cf06-143">Indtast eller vælg en værdi i feltet Attribut.</span><span class="sxs-lookup"><span data-stu-id="7cf06-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="7cf06-144">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7cf06-144">Click Add.</span></span>
11. <span data-ttu-id="7cf06-145">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="7cf06-145">Click Text constant.</span></span>
12. <span data-ttu-id="7cf06-146">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7cf06-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="7cf06-147">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="7cf06-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="7cf06-148">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7cf06-148">Click Add.</span></span>
15. <span data-ttu-id="7cf06-149">Klik på Attributværdi.</span><span class="sxs-lookup"><span data-stu-id="7cf06-149">Click Attribute value.</span></span>
16. <span data-ttu-id="7cf06-150">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7cf06-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="7cf06-151">Indtast eller vælg en værdi i feltet Attribut.</span><span class="sxs-lookup"><span data-stu-id="7cf06-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="7cf06-152">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7cf06-152">Click Add.</span></span>
19. <span data-ttu-id="7cf06-153">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="7cf06-153">Click Text constant.</span></span>
20. <span data-ttu-id="7cf06-154">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7cf06-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="7cf06-155">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="7cf06-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="7cf06-156">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7cf06-156">Click Add.</span></span>
23. <span data-ttu-id="7cf06-157">Klik på Attributværdi.</span><span class="sxs-lookup"><span data-stu-id="7cf06-157">Click Attribute value.</span></span>
24. <span data-ttu-id="7cf06-158">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7cf06-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="7cf06-159">Indtast eller vælg en værdi i feltet Attribut.</span><span class="sxs-lookup"><span data-stu-id="7cf06-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="7cf06-160">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7cf06-160">Click Add.</span></span>
27. <span data-ttu-id="7cf06-161">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="7cf06-161">Click Text constant.</span></span>
28. <span data-ttu-id="7cf06-162">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7cf06-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="7cf06-163">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="7cf06-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="7cf06-164">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7cf06-164">Click Add.</span></span>
31. <span data-ttu-id="7cf06-165">Klik på Attributværdi.</span><span class="sxs-lookup"><span data-stu-id="7cf06-165">Click Attribute value.</span></span>
32. <span data-ttu-id="7cf06-166">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7cf06-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="7cf06-167">Indtast eller vælg en værdi i feltet Attribut.</span><span class="sxs-lookup"><span data-stu-id="7cf06-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="7cf06-168">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7cf06-168">Click Add.</span></span>
35. <span data-ttu-id="7cf06-169">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="7cf06-169">Click Text constant.</span></span>
36. <span data-ttu-id="7cf06-170">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7cf06-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="7cf06-171">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="7cf06-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="7cf06-172">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7cf06-172">Click Add.</span></span>
39. <span data-ttu-id="7cf06-173">Klik på Nummerserieværdi.</span><span class="sxs-lookup"><span data-stu-id="7cf06-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="7cf06-174">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7cf06-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="7cf06-175">Skriv eller vælg en værdi i feltet Nummerserie.</span><span class="sxs-lookup"><span data-stu-id="7cf06-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="7cf06-176">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7cf06-176">Close the page.</span></span>
43. <span data-ttu-id="7cf06-177">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7cf06-177">Close the page.</span></span>
44. <span data-ttu-id="7cf06-178">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7cf06-178">Close the page.</span></span>

