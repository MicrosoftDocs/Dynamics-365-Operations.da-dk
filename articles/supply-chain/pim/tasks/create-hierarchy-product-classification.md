---
title: Oprette et hierarki eller en produktklassifikation
description: Denne fremgangsmåde viser, hvordan du opretter et nyt kategorihierarki og tildeler en varekodehierarkitype.
author: ShylaThompson
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0ff1a2ba20059d3fcb0347220e6e81130e03ac0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203727"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="a0db7-103">Oprette et hierarki eller en produktklassifikation</span><span class="sxs-lookup"><span data-stu-id="a0db7-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0db7-104">Denne fremgangsmåde viser, hvordan du opretter et nyt kategorihierarki og tildeler en varekodehierarkitype.</span><span class="sxs-lookup"><span data-stu-id="a0db7-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="a0db7-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="a0db7-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a0db7-106">Denne fremgangsmåde er beregnet til kategorilederen.</span><span class="sxs-lookup"><span data-stu-id="a0db7-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="a0db7-107">Opret det nye kategorihierarki</span><span class="sxs-lookup"><span data-stu-id="a0db7-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="a0db7-108">Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Konfiguration > Kategorier og attributter > Kategorihierarkier**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="a0db7-109">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-109">Click **New**.</span></span>
3. <span data-ttu-id="a0db7-110">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="a0db7-111">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="a0db7-112">Klik på **Opret**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="a0db7-113">Opbyg hierarkiet</span><span class="sxs-lookup"><span data-stu-id="a0db7-113">Build the hierarchy</span></span>
1. <span data-ttu-id="a0db7-114">Klik på kategorinoden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-114">Click **New** category node.</span></span>
2. <span data-ttu-id="a0db7-115">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="a0db7-116">Skriv en værdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="a0db7-117">Indtast en værdi i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="a0db7-118">Klik på kategorinoden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-118">Click **New** category node.</span></span>
6. <span data-ttu-id="a0db7-119">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="a0db7-120">Skriv en værdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="a0db7-121">Indtast en værdi i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="a0db7-122">Klik på kategorinoden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-122">Click **New** category node.</span></span>
10. <span data-ttu-id="a0db7-123">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="a0db7-124">Skriv en værdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="a0db7-125">Indtast en værdi i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="a0db7-126">Klik på kategorinoden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-126">Click **New** category node.</span></span>
14. <span data-ttu-id="a0db7-127">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="a0db7-128">Skriv en værdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="a0db7-129">Indtast en værdi i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="a0db7-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a0db7-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="a0db7-131">Klassificer hierarkiet</span><span class="sxs-lookup"><span data-stu-id="a0db7-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="a0db7-132">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="a0db7-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="a0db7-133">Klik på **Kategorihierarki** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="a0db7-134">Klik på **Tilknyt hierarkitype**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="a0db7-135">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-135">Click **New**.</span></span>
5. <span data-ttu-id="a0db7-136">Vælg en indstilling i feltet **Kategori for hierarkitype**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="a0db7-137">Vælg **kategorihierarkitype for varekode til klassificering af produktet**.</span><span class="sxs-lookup"><span data-stu-id="a0db7-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="a0db7-138">Klik på rullelisten i feltet **Kategorihierarki** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a0db7-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a0db7-139">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="a0db7-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="a0db7-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a0db7-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a0db7-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a0db7-141">Close the page.</span></span>

