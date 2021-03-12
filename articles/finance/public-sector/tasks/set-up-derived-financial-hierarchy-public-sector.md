---
title: Konfigurere et afledt finansielt hierarki i den offentlige sektor
description: Dette emne indeholder oplysninger om brug af afledte finansielle hierarkier til at indsamle og analysere data for bogførte transaktioner for bestemte tal i hovedkonto, fuld kontonumre og økonomiske dimensionsværdier.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, LedgerDerivedFinHierarchyLegalEntities, LedgerDerivedFinHierarchies
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: da386d77fd467e3d400925d6f3d00015e8305ed7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4984670"
---
# <a name="set-up-a-derived-financial-hierarchy-in-the-public-sector"></a><span data-ttu-id="7afbd-103">Konfigurere et afledt finansielt hierarki i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="7afbd-103">Set up a derived financial hierarchy in the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7afbd-104">For at opfylde CGAC-krav (Government-wide Accounting Classification) skal organisationer i den offentlige sektor bruge afledte finansielle hierarkier for at indsamle og analysere bogførte posteringsdata for specifikke hovedkontonumre, fulde kontonumre og økonomiske dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="7afbd-104">To meet Common Government-wide Accounting Classification (CGAC) requirements, public sector organizations can use derived financial hierarchies to collect and analyze posted transaction data for specific main account numbers, full account numbers, and financial dimension values.</span></span> <span data-ttu-id="7afbd-105">Denne procedure er oprettet med PSUS-demodatafirmaet i den offentlige sektor partition.</span><span class="sxs-lookup"><span data-stu-id="7afbd-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>


## <a name="create-a-category-hierarchy"></a><span data-ttu-id="7afbd-106">Opret et kategorihierarki</span><span class="sxs-lookup"><span data-stu-id="7afbd-106">Create a category hierarchy</span></span>
1. <span data-ttu-id="7afbd-107">Gå til administration af produktoplysninger > Opsætning af > Kategorier og attributter > Kategorihierarkier.</span><span class="sxs-lookup"><span data-stu-id="7afbd-107">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="7afbd-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7afbd-108">Click New.</span></span>
3. <span data-ttu-id="7afbd-109">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="7afbd-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="7afbd-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="7afbd-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7afbd-111">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="7afbd-111">Click Create.</span></span>
6. <span data-ttu-id="7afbd-112">Klik på Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="7afbd-112">Click New category node.</span></span>
7. <span data-ttu-id="7afbd-113">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="7afbd-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="7afbd-114">Skriv en værdi i feltet Kode.</span><span class="sxs-lookup"><span data-stu-id="7afbd-114">In the Code field, type a value.</span></span>
9. <span data-ttu-id="7afbd-115">Klik på Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="7afbd-115">Click New category node.</span></span>
10. <span data-ttu-id="7afbd-116">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="7afbd-116">In the Name field, type a value.</span></span>
11. <span data-ttu-id="7afbd-117">Skriv en værdi i feltet Kode.</span><span class="sxs-lookup"><span data-stu-id="7afbd-117">In the Code field, type a value.</span></span>
    * <span data-ttu-id="7afbd-118">(Valgfrit) Tilføj yderligere underordnede noder, eller angiv yderligere indstillinger for de noder, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="7afbd-118">(Optional) Add additional child nodes, or set additional options for the nodes that you have created.</span></span>  
12. <span data-ttu-id="7afbd-119">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="7afbd-119">Click Save.</span></span>

## <a name="assign-the-derived-financial-hierarchy-category-type"></a><span data-ttu-id="7afbd-120">Tildele det afledte økonomiske hierarkis kategoritype</span><span class="sxs-lookup"><span data-stu-id="7afbd-120">Assign the Derived financial hierarchy category type</span></span>
1. <span data-ttu-id="7afbd-121">Gå til administration af produktoplysninger > Opsætning > Kategorier og attributter > Tilknytninger af kategorihierarkiroller.</span><span class="sxs-lookup"><span data-stu-id="7afbd-121">Go to Product information management > Setup > Categories and attributes > Category hierarchy role associations.</span></span>
2. <span data-ttu-id="7afbd-122">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7afbd-122">Click New.</span></span>
3. <span data-ttu-id="7afbd-123">Vælg "Afledt økonomisk hierarki" i feltet Kategori for hierarkitype.</span><span class="sxs-lookup"><span data-stu-id="7afbd-123">In the Category hierarchy type field, select 'Derived financial hierarchy'.</span></span>
4. <span data-ttu-id="7afbd-124">Klik på rullelisten i feltet Kategorihierarki for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="7afbd-124">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7afbd-125">Klik på kategorihierarkiet, der skal knyttes til typen af afledt økonomisk hierarki, på listen.</span><span class="sxs-lookup"><span data-stu-id="7afbd-125">In the list, click the Category hierarchy to associate with the Derived financial hierarchy type.</span></span>
6. <span data-ttu-id="7afbd-126">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="7afbd-126">Click Save.</span></span>

## <a name="associate-the-derived-financial-hierarchy-with-a-legal-entity"></a><span data-ttu-id="7afbd-127">Tilknytte det afledte økonomiske hierarki med en juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="7afbd-127">Associate the derived financial hierarchy with a legal entity</span></span>
1. <span data-ttu-id="7afbd-128">Gå til Finans > Diagram over konti > Dimensioner > Tilknyt økonomiske hierarkier.</span><span class="sxs-lookup"><span data-stu-id="7afbd-128">Go to General ledger > Chart of accounts > Dimensions > Associate financial hierarchies.</span></span>
2. <span data-ttu-id="7afbd-129">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7afbd-129">Click New.</span></span>
3. <span data-ttu-id="7afbd-130">Klik på rullelisten i feltet Juridisk enhed for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="7afbd-130">In the Legal entity field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="7afbd-131">Vælg den juridiske enhed, som skal tilknyttes det afledte økonomiske hierarki, på listen.</span><span class="sxs-lookup"><span data-stu-id="7afbd-131">In the list, select the legal entity to associate with the derived financial hierarchy.</span></span>
5. <span data-ttu-id="7afbd-132">Klik på rullelisten i feltet Afledt økonomisk hierarki for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="7afbd-132">In the Derived financial hierarchy field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="7afbd-133">Vælg det afledte økonomiske hierarki, som skal tilknyttes den juridiske enhed, på listen.</span><span class="sxs-lookup"><span data-stu-id="7afbd-133">In the list, select the derived financial hierarchy to associate with the legal entity.</span></span>
7. <span data-ttu-id="7afbd-134">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="7afbd-134">Click Save.</span></span>

## <a name="create-filter-rules-for-the-derived-financial-hierarchy"></a><span data-ttu-id="7afbd-135">Oprette filterregler for det afledte økonomiske hierarki</span><span class="sxs-lookup"><span data-stu-id="7afbd-135">Create filter rules for the derived financial hierarchy</span></span>
1. <span data-ttu-id="7afbd-136">Gå til Finans > Diagram over konti > Dimensioner > Afledte økonomiske hierarkier.</span><span class="sxs-lookup"><span data-stu-id="7afbd-136">Go to General ledger > Chart of accounts > Dimensions > Derived financial hierarchies.</span></span>
2. <span data-ttu-id="7afbd-137">Klik på rullelisten i feltet Afledt økonomisk hierarki for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="7afbd-137">In the Derived financial hierarchy field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7afbd-138">Klik på det hierarki, du vil oprette filterregler for, på listen.</span><span class="sxs-lookup"><span data-stu-id="7afbd-138">In the list, click the hierarchy to create filter rules for.</span></span>
4. <span data-ttu-id="7afbd-139">Vælg "Vælg en underordnet node i træet" i træet.</span><span class="sxs-lookup"><span data-stu-id="7afbd-139">In the tree, select 'In the tree, select a child node.'.</span></span>
5. <span data-ttu-id="7afbd-140">Klik på Rediger filter.</span><span class="sxs-lookup"><span data-stu-id="7afbd-140">Click Edit filter.</span></span>
    * <span data-ttu-id="7afbd-141">Klik på Tilføj nye kriterier for at begynde at tilføje regler til filteret.</span><span class="sxs-lookup"><span data-stu-id="7afbd-141">Click Add new criteria to begin adding rules to the filter.</span></span> <span data-ttu-id="7afbd-142">Når du har tilføjet alle kriterierne, skal du klikke på Aktivér filter.</span><span class="sxs-lookup"><span data-stu-id="7afbd-142">After you've added all of the criteria, click Activate filter.</span></span>  

