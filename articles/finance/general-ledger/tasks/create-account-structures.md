---
title: Oprette kontostrukturer
description: Denne opgaveguide gennemgår oprettelse af en kontostruktur.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b75ee76a1fb874652415a2174441f629955d763a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441638"
---
# <a name="create-account-structures"></a><span data-ttu-id="876ac-103">Oprette kontostrukturer</span><span class="sxs-lookup"><span data-stu-id="876ac-103">Create account structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="876ac-104">Denne opgaveguide gennemgår oprettelse af en kontostruktur.</span><span class="sxs-lookup"><span data-stu-id="876ac-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="876ac-105">Der er brugt demodatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="876ac-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="876ac-106">Gå til **Navigationsrude > Moduler > Finans > Kontoplan > Strukturer > Konfigurer kontostrukturer**.</span><span class="sxs-lookup"><span data-stu-id="876ac-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="876ac-107">Klik på **Ny** i **handlingsruden** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="876ac-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="876ac-108">I feltet **Kontostruktur** skal du skrive et navn, som beskriver formålet med kontostrukturen.</span><span class="sxs-lookup"><span data-stu-id="876ac-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="876ac-109">I feltet **Beskrivelse** skal du indtaste et beskrivelse, som angiver formålet med kontostrukturen.</span><span class="sxs-lookup"><span data-stu-id="876ac-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="876ac-110">Klik på **Opret**.</span><span class="sxs-lookup"><span data-stu-id="876ac-110">Click **Create**.</span></span>
6. <span data-ttu-id="876ac-111">Klik på **Tilføj segment** i **Segmenter og tilladte værdier**.</span><span class="sxs-lookup"><span data-stu-id="876ac-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="876ac-112">På listen over dimensioner skal du vælge den dimension, der skal føjes til kontostrukturen.</span><span class="sxs-lookup"><span data-stu-id="876ac-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="876ac-113">Klik på **Tilføj segment** nederst på listen.</span><span class="sxs-lookup"><span data-stu-id="876ac-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="876ac-114">Gentag trin 6 til 9 efter behov.</span><span class="sxs-lookup"><span data-stu-id="876ac-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="876ac-115">Vælg segmentet i sektionen i **Oplysninger om tilladt værdi** for at redigere de tilladte værdier.</span><span class="sxs-lookup"><span data-stu-id="876ac-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="876ac-116">Klik f.eks. på feltet **Hovedkonto**.</span><span class="sxs-lookup"><span data-stu-id="876ac-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="876ac-117">Vælg en indstilling i feltet **Operatør**, f.eks. er mellem og inkluderer.</span><span class="sxs-lookup"><span data-stu-id="876ac-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="876ac-118">Skriv en værdi i feltet **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="876ac-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="876ac-119">For eksempel 600000.</span><span class="sxs-lookup"><span data-stu-id="876ac-119">For example, 600000.</span></span>  
13. <span data-ttu-id="876ac-120">Skriv en værdi i feltet **værdi**.</span><span class="sxs-lookup"><span data-stu-id="876ac-120">In the **through** field, type a value.</span></span> <span data-ttu-id="876ac-121">For eksempel 699999.</span><span class="sxs-lookup"><span data-stu-id="876ac-121">For example, 699999.</span></span>  
14. <span data-ttu-id="876ac-122">Klik på **Anvend** i sektionen **Oplysninger om tilladt værdi**.</span><span class="sxs-lookup"><span data-stu-id="876ac-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="876ac-123">Gentag trin 10 til 15 efter behov.</span><span class="sxs-lookup"><span data-stu-id="876ac-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="876ac-124">Klik på **Tilføj nye kriterier** i sektionen **Oplysninger om tilladt værdi**.</span><span class="sxs-lookup"><span data-stu-id="876ac-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="876ac-125">Vælg en indstilling i feltet Operatør, f.eks. er mellem og inkluderer.</span><span class="sxs-lookup"><span data-stu-id="876ac-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="876ac-126">Skriv en værdi i feltet **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="876ac-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="876ac-127">For eksempel 033.</span><span class="sxs-lookup"><span data-stu-id="876ac-127">For example, 033.</span></span>  
19. <span data-ttu-id="876ac-128">Skriv en værdi i feltet **værdi**.</span><span class="sxs-lookup"><span data-stu-id="876ac-128">In the **through** field, type a value.</span></span> <span data-ttu-id="876ac-129">For eksempel 034.</span><span class="sxs-lookup"><span data-stu-id="876ac-129">For example, 034.</span></span>  
20. <span data-ttu-id="876ac-130">Klik på **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="876ac-130">Click **Apply**.</span></span>
21. <span data-ttu-id="876ac-131">Vælg segmentet i gitteret for at redigere de tilladte værdier.</span><span class="sxs-lookup"><span data-stu-id="876ac-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="876ac-132">For eksempel Bærer.</span><span class="sxs-lookup"><span data-stu-id="876ac-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="876ac-133">Skriv en værdi i feltet **CostCenter**.</span><span class="sxs-lookup"><span data-stu-id="876ac-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="876ac-134">For eksempel 007..021.</span><span class="sxs-lookup"><span data-stu-id="876ac-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="876ac-135">Klik på **Tilføj** i **Segmenter og tilladte værdier**.</span><span class="sxs-lookup"><span data-stu-id="876ac-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="876ac-136">Skriv en værdi i feltet **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="876ac-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="876ac-137">For eksempel, 600000..699999</span><span class="sxs-lookup"><span data-stu-id="876ac-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="876ac-138">Vælg segmentet i gitteret for at redigere de tilladte værdier.</span><span class="sxs-lookup"><span data-stu-id="876ac-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="876ac-139">For eksempel Afdeling.</span><span class="sxs-lookup"><span data-stu-id="876ac-139">For example, Department.</span></span>  
26. <span data-ttu-id="876ac-140">Skriv en værdi i feltet Afdeling.</span><span class="sxs-lookup"><span data-stu-id="876ac-140">In the Department field, type a value.</span></span> <span data-ttu-id="876ac-141">For eksempel 032.</span><span class="sxs-lookup"><span data-stu-id="876ac-141">For example, 032.</span></span>  
27. <span data-ttu-id="876ac-142">Skriv en værdi i feltet CostCenter.</span><span class="sxs-lookup"><span data-stu-id="876ac-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="876ac-143">For eksempel 086.</span><span class="sxs-lookup"><span data-stu-id="876ac-143">For example, 086.</span></span>  
28. <span data-ttu-id="876ac-144">Klik på **Valider** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="876ac-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="876ac-145">Klik på **Aktivér** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="876ac-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="876ac-146">Klik på **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="876ac-146">Click **Activate**.</span></span>

