---
title: Oprette et hierarki eller en produktklassifikation
description: Denne fremgangsmåde viser, hvordan du opretter et nyt kategorihierarki og tildeler en varekodehierarkitype.
author: ShylaThompson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: faf43eb15283ffd7e36ad38728f166884dddcd85
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844819"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="cb9e8-103">Oprette et hierarki eller en produktklassifikation</span><span class="sxs-lookup"><span data-stu-id="cb9e8-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb9e8-104">Denne fremgangsmåde viser, hvordan du opretter et nyt kategorihierarki og tildeler en varekodehierarkitype.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="cb9e8-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="cb9e8-106">Denne fremgangsmåde er beregnet til kategorilederen.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="cb9e8-107">Opret det nye kategorihierarki</span><span class="sxs-lookup"><span data-stu-id="cb9e8-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="cb9e8-108">Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Konfiguration > Kategorier og attributter > Kategorihierarkier**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="cb9e8-109">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-109">Click **New**.</span></span>
3. <span data-ttu-id="cb9e8-110">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="cb9e8-111">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="cb9e8-112">Klik på **Opret**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="cb9e8-113">Opbyg hierarkiet</span><span class="sxs-lookup"><span data-stu-id="cb9e8-113">Build the hierarchy</span></span>
1. <span data-ttu-id="cb9e8-114">Klik på kategorinoden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-114">Click **New** category node.</span></span>
2. <span data-ttu-id="cb9e8-115">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="cb9e8-116">Skriv en værdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="cb9e8-117">Indtast en værdi i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="cb9e8-118">Klik på kategorinoden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-118">Click **New** category node.</span></span>
6. <span data-ttu-id="cb9e8-119">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="cb9e8-120">Skriv en værdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="cb9e8-121">Indtast en værdi i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="cb9e8-122">Klik på kategorinoden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-122">Click **New** category node.</span></span>
10. <span data-ttu-id="cb9e8-123">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="cb9e8-124">Skriv en værdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="cb9e8-125">Indtast en værdi i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="cb9e8-126">Klik på kategorinoden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-126">Click **New** category node.</span></span>
14. <span data-ttu-id="cb9e8-127">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="cb9e8-128">Skriv en værdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="cb9e8-129">Indtast en værdi i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="cb9e8-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="cb9e8-131">Klassificer hierarkiet</span><span class="sxs-lookup"><span data-stu-id="cb9e8-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="cb9e8-132">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="cb9e8-133">Klik på **Kategorihierarki** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="cb9e8-134">Klik på **Tilknyt hierarkitype**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="cb9e8-135">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-135">Click **New**.</span></span>
5. <span data-ttu-id="cb9e8-136">Vælg en indstilling i feltet **Kategori for hierarkitype**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="cb9e8-137">Vælg **kategorihierarkitype for varekode til klassificering af produktet**.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="cb9e8-138">Klik på rullelisten i feltet **Kategorihierarki** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cb9e8-139">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="cb9e8-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cb9e8-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cb9e8-141">Close the page.</span></span>

