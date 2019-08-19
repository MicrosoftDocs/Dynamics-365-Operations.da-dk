---
title: Oprette et organisationsrapporthierarki
description: Du kan bruge denne procedure til at oprette et rapporthierarki til organisationsrapportering.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5684c710b8e167a4a39f106eb3c0fd77e3011dbd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841339"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="fcffe-103">Oprette et organisationsrapporthierarki</span><span class="sxs-lookup"><span data-stu-id="fcffe-103">Create an organization report hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fcffe-104">Du kan bruge denne procedure til at oprette et rapporthierarki til organisationsrapportering.</span><span class="sxs-lookup"><span data-stu-id="fcffe-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="fcffe-105">Formålet med denne registrering er at føre dig gennem dimensionshierarkiet, så du kan fortsætte, indtil rapporteringsstrukturen for hele organisationen er oprettet.</span><span class="sxs-lookup"><span data-stu-id="fcffe-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="fcffe-106">Denne registrering bruger USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="fcffe-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="fcffe-107">Gå til Omkostningsregnskab > Dimensioner > Dimensionshierarkier.</span><span class="sxs-lookup"><span data-stu-id="fcffe-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="fcffe-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fcffe-108">Click New.</span></span>
3. <span data-ttu-id="fcffe-109">Vælg 'Klassifikationshierarki for dimension' i feltet HierarchyTypeComboBox.</span><span class="sxs-lookup"><span data-stu-id="fcffe-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="fcffe-110">Vælg Klassifikationshierarki for dimension.</span><span class="sxs-lookup"><span data-stu-id="fcffe-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="fcffe-111">Klassifikationshierarki for dimension-typen bruges til at definere regler og til rapporteringsformål.</span><span class="sxs-lookup"><span data-stu-id="fcffe-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="fcffe-112">Den understøtter alle dimensioner, f.eks. omkostningsobjekter, omkostningselementer og statistiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="fcffe-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="fcffe-113">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="fcffe-113">Click Create.</span></span>
5. <span data-ttu-id="fcffe-114">Skriv 'Organisation USP2' i feltet Dimensionshierarki.</span><span class="sxs-lookup"><span data-stu-id="fcffe-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="fcffe-115">Indtast eller vælg en værdi i feltet Dimension.</span><span class="sxs-lookup"><span data-stu-id="fcffe-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="fcffe-116">Vælg Bærere.</span><span class="sxs-lookup"><span data-stu-id="fcffe-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="fcffe-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-117">Click Save.</span></span>
8. <span data-ttu-id="fcffe-118">Klik på Vis hierarki.</span><span class="sxs-lookup"><span data-stu-id="fcffe-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="fcffe-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fcffe-119">Click New.</span></span>
10. <span data-ttu-id="fcffe-120">Skriv 'Administrerende direktør' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="fcffe-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="fcffe-121">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-121">Click Save.</span></span>
12. <span data-ttu-id="fcffe-122">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fcffe-122">Click New.</span></span>
13. <span data-ttu-id="fcffe-123">Skriv 'Administrerende direktør' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="fcffe-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="fcffe-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-124">Click Save.</span></span>
15. <span data-ttu-id="fcffe-125">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fcffe-125">Click New.</span></span>
16. <span data-ttu-id="fcffe-126">Skriv 'Region Øst' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="fcffe-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="fcffe-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-127">Click Save.</span></span>
18. <span data-ttu-id="fcffe-128">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fcffe-128">Click New.</span></span>
19. <span data-ttu-id="fcffe-129">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fcffe-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="fcffe-130">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="fcffe-131">Vælg det dimensionsmedlem, der svarer til noden.</span><span class="sxs-lookup"><span data-stu-id="fcffe-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="fcffe-132">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-132">Click Save.</span></span>
22. <span data-ttu-id="fcffe-133">Vælg 'Organisation USP2\Administrerende direktør\Bærere for administrerende direktør' i træet.</span><span class="sxs-lookup"><span data-stu-id="fcffe-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="fcffe-134">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fcffe-134">Click New.</span></span>
24. <span data-ttu-id="fcffe-135">Skriv 'Region Vest' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="fcffe-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="fcffe-136">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-136">Click Save.</span></span>
26. <span data-ttu-id="fcffe-137">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fcffe-137">Click New.</span></span>
27. <span data-ttu-id="fcffe-138">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fcffe-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="fcffe-139">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="fcffe-140">Vælg det dimensionsmedlem, der svarer til noden.</span><span class="sxs-lookup"><span data-stu-id="fcffe-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="fcffe-141">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-141">Click Save.</span></span>
30. <span data-ttu-id="fcffe-142">Vælg 'Organisation USP2\Administrerende direktør' i træet.</span><span class="sxs-lookup"><span data-stu-id="fcffe-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="fcffe-143">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fcffe-143">Click New.</span></span>
32. <span data-ttu-id="fcffe-144">Skriv 'Bærere for administrerende direktør' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="fcffe-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="fcffe-145">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-145">Click Save.</span></span>
34. <span data-ttu-id="fcffe-146">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fcffe-146">Click New.</span></span>
35. <span data-ttu-id="fcffe-147">Skriv 'Marketingkampa' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="fcffe-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="fcffe-148">Skriv 'Marketingkampagne' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="fcffe-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="fcffe-149">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-149">Click Save.</span></span>
38. <span data-ttu-id="fcffe-150">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fcffe-150">Click New.</span></span>
39. <span data-ttu-id="fcffe-151">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fcffe-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="fcffe-152">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="fcffe-153">Vælg det dimensionsmedlem, der svarer til noden.</span><span class="sxs-lookup"><span data-stu-id="fcffe-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="fcffe-154">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-154">Click Save.</span></span>
42. <span data-ttu-id="fcffe-155">Vælg 'Organisation USP2\Administrerende direktør\Bærere for administrerende direktør' i træet.</span><span class="sxs-lookup"><span data-stu-id="fcffe-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="fcffe-156">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fcffe-156">Click New.</span></span>
44. <span data-ttu-id="fcffe-157">Skriv 'Messer' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="fcffe-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="fcffe-158">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-158">Click Save.</span></span>
46. <span data-ttu-id="fcffe-159">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fcffe-159">Click New.</span></span>
47. <span data-ttu-id="fcffe-160">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fcffe-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="fcffe-161">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="fcffe-162">Vælg det dimensionsmedlem, der svarer til noden.</span><span class="sxs-lookup"><span data-stu-id="fcffe-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="fcffe-163">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-163">Click Save.</span></span>
50. <span data-ttu-id="fcffe-164">Vælg 'Organisation USP2\Administrerende direktør' i træet.</span><span class="sxs-lookup"><span data-stu-id="fcffe-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="fcffe-165">Skriv 'Bærere for administrerende direktør' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="fcffe-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="fcffe-166">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-166">Click Save.</span></span>
53. <span data-ttu-id="fcffe-167">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fcffe-167">Click New.</span></span>
54. <span data-ttu-id="fcffe-168">Skriv 'Call centre' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="fcffe-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="fcffe-169">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-169">Click Save.</span></span>
56. <span data-ttu-id="fcffe-170">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fcffe-170">Click New.</span></span>
57. <span data-ttu-id="fcffe-171">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fcffe-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="fcffe-172">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="fcffe-173">Vælg det dimensionsmedlem, der svarer til noden.</span><span class="sxs-lookup"><span data-stu-id="fcffe-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="fcffe-174">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fcffe-174">Click Save.</span></span>

