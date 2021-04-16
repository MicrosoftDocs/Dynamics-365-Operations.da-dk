---
title: Oprette et indkøbskatalog
description: Dette emner beskriver, hvordan du opretter et indkøbskatalog.
author: kamaybac
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59117df519b7aa525713d3acd70195cc42614b9a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812392"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="96fb4-103">Oprette et indkøbskatalog</span><span class="sxs-lookup"><span data-stu-id="96fb4-103">Create a procurement catalog</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="96fb4-104">Dette emner beskriver, hvordan du opretter et indkøbskatalog.</span><span class="sxs-lookup"><span data-stu-id="96fb4-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="96fb4-105">Denne opgave vil normalt udføres af en professionel indkøber.</span><span class="sxs-lookup"><span data-stu-id="96fb4-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="96fb4-106">Du lærer også, hvordan medarbejdere kan bruge kataloget, når de opretter en indkøbsrekvisition.</span><span class="sxs-lookup"><span data-stu-id="96fb4-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="96fb4-107">Før du kan oprette et katalog, skal der være et indkøbskategorihierarki i systemet.</span><span class="sxs-lookup"><span data-stu-id="96fb4-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="96fb4-108">Hierarkiet arves af det nye katalog sammen med alle de produkter, der er i hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="96fb4-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="96fb4-109">Du kan bruge denne vejledning i demodatafirmaet USMF, hvor indkøbskategorihierarkiet er tilgængeligt, såvel som de eksempler, der bruges i trinnene i proceduren.</span><span class="sxs-lookup"><span data-stu-id="96fb4-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="96fb4-110">Kontroller, at der findes et indkøbskategorihierarki</span><span class="sxs-lookup"><span data-stu-id="96fb4-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="96fb4-111">Gå til **Navigationsrude > Moduler > Indkøb og forsyning > Kreditorer > Indkøbskategorier**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="96fb4-112">Et indkøbskategorihierarki er tilgængeligt i USMF-demodatafirmaet, og produkter er føjet til kategorien **Kontormaskiner/computere**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="96fb4-113">Hvis du kører denne procedure som en opgaveguide, skal du låse opgaveguiden op, hvis du vil søge i kategorien.</span><span class="sxs-lookup"><span data-stu-id="96fb4-113">If you're running this procedure as a task guide, you'll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="96fb4-114">Hvis et hierarki ikke var tilgængeligt, skal du oprette det ved at klikke på **Nyt**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-114">If a hierarchy was not available, you'd create it by clicking **New**.</span></span> <span data-ttu-id="96fb4-115">Det kan du kun gøre én gang.</span><span class="sxs-lookup"><span data-stu-id="96fb4-115">This can only be done once.</span></span>  
2. <span data-ttu-id="96fb4-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="96fb4-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="96fb4-117">Oprette et katalog</span><span class="sxs-lookup"><span data-stu-id="96fb4-117">Create a catalog</span></span>
1. <span data-ttu-id="96fb4-118">Gå til **Navigationsrude > Moduler > Indkøb og forsyning > Kataloger > Indkøbskataloger**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="96fb4-119">Vælg **Nyt indkøbskatalog** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="96fb4-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="96fb4-120">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="96fb4-121">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-121">Select **OK**.</span></span>
5. <span data-ttu-id="96fb4-122">Udvid **FIRMAS INDKØBSKATEGORIER** i træet.</span><span class="sxs-lookup"><span data-stu-id="96fb4-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="96fb4-123">Udvid **KONTORMASKINER** i træet.</span><span class="sxs-lookup"><span data-stu-id="96fb4-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="96fb4-124">Vælg **Computere** i træet.</span><span class="sxs-lookup"><span data-stu-id="96fb4-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="96fb4-125">Produkterne fra indkøbskategorien vises på listen.</span><span class="sxs-lookup"><span data-stu-id="96fb4-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="96fb4-126">Hvis du vil føje et produkt til kategorien, skal du gøre det på siden **Indkøbskategorihierarki** eller på siden **Vareoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="96fb4-127">Opdateringstypen **Standard** bestemmer, om nye produkter, der er føjet til indkøbskategorihierarkiet, er synlige i kataloget med det samme.</span><span class="sxs-lookup"><span data-stu-id="96fb4-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="96fb4-128">Hvis opdateringstypen er indstillet til **Dynamisk**, kan ændringer ses øjeblikkeligt.</span><span class="sxs-lookup"><span data-stu-id="96fb4-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="96fb4-129">Hvis opdateringstypen er **Statisk**, er nye produkter kun synlige for brugere af kataloget, når kataloget er blevet udgivet igen.</span><span class="sxs-lookup"><span data-stu-id="96fb4-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="96fb4-130">Handlingen **Publicer** er tilgængelig i handlingsruden øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="96fb4-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="96fb4-131">Hvis produkter fjernes fra indkøbskategorihierarkiet, er ændringen straks synlig, uanset hvilken værdi der er i feltet **Standard** for opdateringstype.</span><span class="sxs-lookup"><span data-stu-id="96fb4-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="96fb4-132">I handlingsruden skal du vælge **Kategorinavigation** og sikre, at **Aktivér** er valgt.</span><span class="sxs-lookup"><span data-stu-id="96fb4-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="96fb4-133">Vælg **Aktivér katalog**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="96fb4-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="96fb4-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="96fb4-135">Gør kataloget synligt</span><span class="sxs-lookup"><span data-stu-id="96fb4-135">Make the catalog visible</span></span>
1. <span data-ttu-id="96fb4-136">Gå til **Navigationsrude > Moduler > Indkøb og forsyning > Opsætning > Politikker > Indkøbspolitikker**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="96fb4-137">Vælg **Indkøbspolitikken USMF**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="96fb4-138">Du skal vælge indkøbspolitik, så den juridiske enhed, som arbejderen har knyttet til din brugerprofil, kan bestille produkter.</span><span class="sxs-lookup"><span data-stu-id="96fb4-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="96fb4-139">I USMF-demodataene er administratorbrugeren knyttet til den arbejder, der hedder **Julia Funderburk**, og hun bestiller som standard produkter i USMF.</span><span class="sxs-lookup"><span data-stu-id="96fb4-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="96fb4-140">Vælg det katalog, du netop har oprettet.</span><span class="sxs-lookup"><span data-stu-id="96fb4-140">Select the catalog that you've just created.</span></span>
4. <span data-ttu-id="96fb4-141">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="96fb4-142">Brug kataloget</span><span class="sxs-lookup"><span data-stu-id="96fb4-142">Use the catalog</span></span>
1. <span data-ttu-id="96fb4-143">Gå til **Navigationsrude > Moduler > Indkøb og forsyning > Indkøbsrekvisitioner > Alle indkøbsrekvisitioner**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="96fb4-144">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-144">Select **New**.</span></span>
3. <span data-ttu-id="96fb4-145">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="96fb4-146">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-146">Select **OK**.</span></span>
5. <span data-ttu-id="96fb4-147">Vælg **Tilføj produkter**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-147">Select **Add products**.</span></span>
6. <span data-ttu-id="96fb4-148">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="96fb4-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="96fb4-149">Du kan bruge kategorihierarkiet til venstre eller filteret øverst på listen til at filtrere produkterne.</span><span class="sxs-lookup"><span data-stu-id="96fb4-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="96fb4-150">Vælg **Tilføj til linjer**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="96fb4-151">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="96fb4-151">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]