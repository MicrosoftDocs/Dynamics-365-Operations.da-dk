---
title: Oprette et organisationsrapporthierarki
description: Du kan bruge denne procedure til at oprette et rapporthierarki til organisationsrapportering.
author: ShylaThompson
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727a77b5a3a64bd4b679103e24d8c4c384a113e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815734"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="30512-103">Oprette et organisationsrapporthierarki</span><span class="sxs-lookup"><span data-stu-id="30512-103">Create an organization report hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="30512-104">Du kan bruge denne procedure til at oprette et rapporthierarki til organisationsrapportering.</span><span class="sxs-lookup"><span data-stu-id="30512-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="30512-105">Formålet med denne registrering er at føre dig gennem dimensionshierarkiet, så du kan fortsætte, indtil rapporteringsstrukturen for hele organisationen er oprettet.</span><span class="sxs-lookup"><span data-stu-id="30512-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="30512-106">Denne registrering bruger USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="30512-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="30512-107">Gå til Omkostningsregnskab > Dimensioner > Dimensionshierarkier.</span><span class="sxs-lookup"><span data-stu-id="30512-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="30512-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="30512-108">Click New.</span></span>
3. <span data-ttu-id="30512-109">Vælg 'Klassifikationshierarki for dimension' i feltet HierarchyTypeComboBox.</span><span class="sxs-lookup"><span data-stu-id="30512-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="30512-110">Vælg Klassifikationshierarki for dimension.</span><span class="sxs-lookup"><span data-stu-id="30512-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="30512-111">Klassifikationshierarki for dimension-typen bruges til at definere regler og til rapporteringsformål.</span><span class="sxs-lookup"><span data-stu-id="30512-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="30512-112">Den understøtter alle dimensioner, f.eks. omkostningsobjekter, omkostningselementer og statistiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="30512-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="30512-113">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="30512-113">Click Create.</span></span>
5. <span data-ttu-id="30512-114">Skriv 'Organisation USP2' i feltet Dimensionshierarki.</span><span class="sxs-lookup"><span data-stu-id="30512-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="30512-115">Indtast eller vælg en værdi i feltet Dimension.</span><span class="sxs-lookup"><span data-stu-id="30512-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="30512-116">Vælg Bærere.</span><span class="sxs-lookup"><span data-stu-id="30512-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="30512-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30512-117">Click Save.</span></span>
8. <span data-ttu-id="30512-118">Klik på Vis hierarki.</span><span class="sxs-lookup"><span data-stu-id="30512-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="30512-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="30512-119">Click New.</span></span>
10. <span data-ttu-id="30512-120">Skriv 'Administrerende direktør' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="30512-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="30512-121">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30512-121">Click Save.</span></span>
12. <span data-ttu-id="30512-122">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="30512-122">Click New.</span></span>
13. <span data-ttu-id="30512-123">Skriv 'Administrerende direktør' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="30512-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="30512-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30512-124">Click Save.</span></span>
15. <span data-ttu-id="30512-125">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="30512-125">Click New.</span></span>
16. <span data-ttu-id="30512-126">Skriv 'Region Øst' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="30512-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="30512-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30512-127">Click Save.</span></span>
18. <span data-ttu-id="30512-128">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="30512-128">Click New.</span></span>
19. <span data-ttu-id="30512-129">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="30512-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="30512-130">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="30512-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="30512-131">Vælg det dimensionsmedlem, der svarer til noden.</span><span class="sxs-lookup"><span data-stu-id="30512-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="30512-132">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30512-132">Click Save.</span></span>
22. <span data-ttu-id="30512-133">Vælg 'Organisation USP2\Administrerende direktør\Bærere for administrerende direktør' i træet.</span><span class="sxs-lookup"><span data-stu-id="30512-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="30512-134">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="30512-134">Click New.</span></span>
24. <span data-ttu-id="30512-135">Skriv 'Region Vest' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="30512-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="30512-136">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30512-136">Click Save.</span></span>
26. <span data-ttu-id="30512-137">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="30512-137">Click New.</span></span>
27. <span data-ttu-id="30512-138">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="30512-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="30512-139">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="30512-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="30512-140">Vælg det dimensionsmedlem, der svarer til noden.</span><span class="sxs-lookup"><span data-stu-id="30512-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="30512-141">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30512-141">Click Save.</span></span>
30. <span data-ttu-id="30512-142">Vælg 'Organisation USP2\Administrerende direktør' i træet.</span><span class="sxs-lookup"><span data-stu-id="30512-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="30512-143">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="30512-143">Click New.</span></span>
32. <span data-ttu-id="30512-144">Skriv 'Bærere for administrerende direktør' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="30512-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="30512-145">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30512-145">Click Save.</span></span>
34. <span data-ttu-id="30512-146">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="30512-146">Click New.</span></span>
35. <span data-ttu-id="30512-147">Skriv 'Marketingkampa' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="30512-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="30512-148">Skriv 'Marketingkampagne' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="30512-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="30512-149">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30512-149">Click Save.</span></span>
38. <span data-ttu-id="30512-150">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="30512-150">Click New.</span></span>
39. <span data-ttu-id="30512-151">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="30512-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="30512-152">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="30512-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="30512-153">Vælg det dimensionsmedlem, der svarer til noden.</span><span class="sxs-lookup"><span data-stu-id="30512-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="30512-154">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30512-154">Click Save.</span></span>
42. <span data-ttu-id="30512-155">Vælg 'Organisation USP2\Administrerende direktør\Bærere for administrerende direktør' i træet.</span><span class="sxs-lookup"><span data-stu-id="30512-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="30512-156">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="30512-156">Click New.</span></span>
44. <span data-ttu-id="30512-157">Skriv 'Messer' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="30512-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="30512-158">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30512-158">Click Save.</span></span>
46. <span data-ttu-id="30512-159">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="30512-159">Click New.</span></span>
47. <span data-ttu-id="30512-160">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="30512-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="30512-161">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="30512-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="30512-162">Vælg det dimensionsmedlem, der svarer til noden.</span><span class="sxs-lookup"><span data-stu-id="30512-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="30512-163">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30512-163">Click Save.</span></span>
50. <span data-ttu-id="30512-164">Vælg 'Organisation USP2\Administrerende direktør' i træet.</span><span class="sxs-lookup"><span data-stu-id="30512-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="30512-165">Skriv 'Bærere for administrerende direktør' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="30512-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="30512-166">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30512-166">Click Save.</span></span>
53. <span data-ttu-id="30512-167">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="30512-167">Click New.</span></span>
54. <span data-ttu-id="30512-168">Skriv 'Call centre' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="30512-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="30512-169">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30512-169">Click Save.</span></span>
56. <span data-ttu-id="30512-170">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="30512-170">Click New.</span></span>
57. <span data-ttu-id="30512-171">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="30512-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="30512-172">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="30512-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="30512-173">Vælg det dimensionsmedlem, der svarer til noden.</span><span class="sxs-lookup"><span data-stu-id="30512-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="30512-174">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="30512-174">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]