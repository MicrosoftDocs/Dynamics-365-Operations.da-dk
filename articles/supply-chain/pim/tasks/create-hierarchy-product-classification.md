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
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 439df63a4f8f0cc1c030554d18f80e9934c88b00
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986185"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="7bf7a-103">Oprette et hierarki eller en produktklassifikation</span><span class="sxs-lookup"><span data-stu-id="7bf7a-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7bf7a-104">Denne fremgangsmåde viser, hvordan du opretter et nyt kategorihierarki og tildeler en varekodehierarkitype.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="7bf7a-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7bf7a-106">Denne fremgangsmåde er beregnet til kategorilederen.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="7bf7a-107">Opret det nye kategorihierarki</span><span class="sxs-lookup"><span data-stu-id="7bf7a-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="7bf7a-108">Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Konfiguration > Kategorier og attributter > Kategorihierarkier**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="7bf7a-109">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-109">Click **New**.</span></span>
3. <span data-ttu-id="7bf7a-110">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="7bf7a-111">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="7bf7a-112">Klik på **Opret**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="7bf7a-113">Opbyg hierarkiet</span><span class="sxs-lookup"><span data-stu-id="7bf7a-113">Build the hierarchy</span></span>
1. <span data-ttu-id="7bf7a-114">Klik på kategorinoden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-114">Click **New** category node.</span></span>
2. <span data-ttu-id="7bf7a-115">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="7bf7a-116">Skriv en værdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="7bf7a-117">Indtast en værdi i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="7bf7a-118">Klik på kategorinoden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-118">Click **New** category node.</span></span>
6. <span data-ttu-id="7bf7a-119">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="7bf7a-120">Skriv en værdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="7bf7a-121">Indtast en værdi i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="7bf7a-122">Klik på kategorinoden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-122">Click **New** category node.</span></span>
10. <span data-ttu-id="7bf7a-123">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="7bf7a-124">Skriv en værdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="7bf7a-125">Indtast en værdi i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="7bf7a-126">Klik på kategorinoden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-126">Click **New** category node.</span></span>
14. <span data-ttu-id="7bf7a-127">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="7bf7a-128">Skriv en værdi i feltet **Kode**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="7bf7a-129">Indtast en værdi i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="7bf7a-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="7bf7a-131">Klassificer hierarkiet</span><span class="sxs-lookup"><span data-stu-id="7bf7a-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="7bf7a-132">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="7bf7a-133">Klik på **Kategorihierarki** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="7bf7a-134">Klik på **Tilknyt hierarkitype**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="7bf7a-135">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-135">Click **New**.</span></span>
5. <span data-ttu-id="7bf7a-136">Vælg en indstilling i feltet **Kategori for hierarkitype**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="7bf7a-137">Vælg **kategorihierarkitype for varekode til klassificering af produktet**.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="7bf7a-138">Klik på rullelisten i feltet **Kategorihierarki** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="7bf7a-139">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="7bf7a-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7bf7a-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7bf7a-141">Close the page.</span></span>

