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
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9a06a67f851e4a73df90f999683d5ea27f38e66
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543927"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="cd022-103">Oprette et organisationsrapporthierarki</span><span class="sxs-lookup"><span data-stu-id="cd022-103">Create an organization report hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd022-104">Du kan bruge denne procedure til at oprette et rapporthierarki til organisationsrapportering.</span><span class="sxs-lookup"><span data-stu-id="cd022-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="cd022-105">Formålet med denne registrering er at føre dig gennem dimensionshierarkiet, så du kan fortsætte, indtil rapporteringsstrukturen for hele organisationen er oprettet.</span><span class="sxs-lookup"><span data-stu-id="cd022-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="cd022-106">Denne registrering bruger USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="cd022-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="cd022-107">Gå til Omkostningsregnskab > Dimensioner > Dimensionshierarkier.</span><span class="sxs-lookup"><span data-stu-id="cd022-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="cd022-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cd022-108">Click New.</span></span>
3. <span data-ttu-id="cd022-109">Vælg 'Klassifikationshierarki for dimension' i feltet HierarchyTypeComboBox.</span><span class="sxs-lookup"><span data-stu-id="cd022-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="cd022-110">Vælg Klassifikationshierarki for dimension.</span><span class="sxs-lookup"><span data-stu-id="cd022-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="cd022-111">Klassifikationshierarki for dimension-typen bruges til at definere regler og til rapporteringsformål.</span><span class="sxs-lookup"><span data-stu-id="cd022-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="cd022-112">Den understøtter alle dimensioner, f.eks. omkostningsobjekter, omkostningselementer og statistiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="cd022-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="cd022-113">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="cd022-113">Click Create.</span></span>
5. <span data-ttu-id="cd022-114">Skriv 'Organisation USP2' i feltet Dimensionshierarki.</span><span class="sxs-lookup"><span data-stu-id="cd022-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="cd022-115">Indtast eller vælg en værdi i feltet Dimension.</span><span class="sxs-lookup"><span data-stu-id="cd022-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="cd022-116">Vælg Bærere.</span><span class="sxs-lookup"><span data-stu-id="cd022-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="cd022-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cd022-117">Click Save.</span></span>
8. <span data-ttu-id="cd022-118">Klik på Vis hierarki.</span><span class="sxs-lookup"><span data-stu-id="cd022-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="cd022-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cd022-119">Click New.</span></span>
10. <span data-ttu-id="cd022-120">Skriv 'Administrerende direktør' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="cd022-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="cd022-121">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cd022-121">Click Save.</span></span>
12. <span data-ttu-id="cd022-122">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cd022-122">Click New.</span></span>
13. <span data-ttu-id="cd022-123">Skriv 'Administrerende direktør' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="cd022-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="cd022-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cd022-124">Click Save.</span></span>
15. <span data-ttu-id="cd022-125">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cd022-125">Click New.</span></span>
16. <span data-ttu-id="cd022-126">Skriv 'Region Øst' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="cd022-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="cd022-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cd022-127">Click Save.</span></span>
18. <span data-ttu-id="cd022-128">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cd022-128">Click New.</span></span>
19. <span data-ttu-id="cd022-129">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cd022-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="cd022-130">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="cd022-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="cd022-131">Vælg det dimensionsmedlem, der svarer til noden.</span><span class="sxs-lookup"><span data-stu-id="cd022-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="cd022-132">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cd022-132">Click Save.</span></span>
22. <span data-ttu-id="cd022-133">Vælg 'Organisation USP2\Administrerende direktør\Bærere for administrerende direktør' i træet.</span><span class="sxs-lookup"><span data-stu-id="cd022-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="cd022-134">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cd022-134">Click New.</span></span>
24. <span data-ttu-id="cd022-135">Skriv 'Region Vest' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="cd022-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="cd022-136">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cd022-136">Click Save.</span></span>
26. <span data-ttu-id="cd022-137">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cd022-137">Click New.</span></span>
27. <span data-ttu-id="cd022-138">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cd022-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="cd022-139">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="cd022-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="cd022-140">Vælg det dimensionsmedlem, der svarer til noden.</span><span class="sxs-lookup"><span data-stu-id="cd022-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="cd022-141">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cd022-141">Click Save.</span></span>
30. <span data-ttu-id="cd022-142">Vælg 'Organisation USP2\Administrerende direktør' i træet.</span><span class="sxs-lookup"><span data-stu-id="cd022-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="cd022-143">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cd022-143">Click New.</span></span>
32. <span data-ttu-id="cd022-144">Skriv 'Bærere for administrerende direktør' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="cd022-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="cd022-145">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cd022-145">Click Save.</span></span>
34. <span data-ttu-id="cd022-146">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cd022-146">Click New.</span></span>
35. <span data-ttu-id="cd022-147">Skriv 'Marketingkampa' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="cd022-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="cd022-148">Skriv 'Marketingkampagne' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="cd022-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="cd022-149">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cd022-149">Click Save.</span></span>
38. <span data-ttu-id="cd022-150">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cd022-150">Click New.</span></span>
39. <span data-ttu-id="cd022-151">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cd022-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="cd022-152">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="cd022-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="cd022-153">Vælg det dimensionsmedlem, der svarer til noden.</span><span class="sxs-lookup"><span data-stu-id="cd022-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="cd022-154">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cd022-154">Click Save.</span></span>
42. <span data-ttu-id="cd022-155">Vælg 'Organisation USP2\Administrerende direktør\Bærere for administrerende direktør' i træet.</span><span class="sxs-lookup"><span data-stu-id="cd022-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="cd022-156">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cd022-156">Click New.</span></span>
44. <span data-ttu-id="cd022-157">Skriv 'Messer' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="cd022-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="cd022-158">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cd022-158">Click Save.</span></span>
46. <span data-ttu-id="cd022-159">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cd022-159">Click New.</span></span>
47. <span data-ttu-id="cd022-160">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cd022-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="cd022-161">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="cd022-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="cd022-162">Vælg det dimensionsmedlem, der svarer til noden.</span><span class="sxs-lookup"><span data-stu-id="cd022-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="cd022-163">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cd022-163">Click Save.</span></span>
50. <span data-ttu-id="cd022-164">Vælg 'Organisation USP2\Administrerende direktør' i træet.</span><span class="sxs-lookup"><span data-stu-id="cd022-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="cd022-165">Skriv 'Bærere for administrerende direktør' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="cd022-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="cd022-166">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cd022-166">Click Save.</span></span>
53. <span data-ttu-id="cd022-167">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cd022-167">Click New.</span></span>
54. <span data-ttu-id="cd022-168">Skriv 'Call centre' i feltet Nodenavn.</span><span class="sxs-lookup"><span data-stu-id="cd022-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="cd022-169">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cd022-169">Click Save.</span></span>
56. <span data-ttu-id="cd022-170">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cd022-170">Click New.</span></span>
57. <span data-ttu-id="cd022-171">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cd022-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="cd022-172">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="cd022-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="cd022-173">Vælg det dimensionsmedlem, der svarer til noden.</span><span class="sxs-lookup"><span data-stu-id="cd022-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="cd022-174">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cd022-174">Click Save.</span></span>

