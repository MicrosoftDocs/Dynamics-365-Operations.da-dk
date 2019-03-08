---
title: Oprette et indkøbskatalog
description: Denne vejledning viser, hvordan du opretter et indkøbskatalog.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f2a010e21f16b3908a6ee5f18d8f144c5130be7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "314687"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="6ae3d-103">Oprette et indkøbskatalog</span><span class="sxs-lookup"><span data-stu-id="6ae3d-103">Create a procurement catalog</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ae3d-104">Denne vejledning viser, hvordan du opretter et indkøbskatalog.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-104">This guide shows you how to create a procurement catalog.</span></span> <span data-ttu-id="6ae3d-105">Denne opgave vil normalt udføres af en professionel indkøber.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="6ae3d-106">Du lærer også, hvordan medarbejdere kan bruge kataloget, når de opretter en indkøbsrekvisition.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="6ae3d-107">Før du kan oprette et katalog, skal der være et indkøbskategorihierarki i systemet.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="6ae3d-108">Hierarkiet arves af det nye katalog sammen med alle de produkter, der er i hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="6ae3d-109">Du kan bruge denne vejledning i demodatafirmaet USMF, hvor indkøbskategorihierarkiet er tilgængeligt, såvel som de eksempler, der bruges i trinnene i proceduren.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="6ae3d-110">Kontroller, at der findes et indkøbskategorihierarki</span><span class="sxs-lookup"><span data-stu-id="6ae3d-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="6ae3d-111">Gå til Indkøb og forsyning > Indkøbskategorier.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-111">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="6ae3d-112">Et indkøbskategorihierarki er tilgængeligt i USMF-demodatafirmaet, og produkter er føjet til kategorien Kontormaskiner/computere.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the Office machines/Computers category.</span></span> <span data-ttu-id="6ae3d-113">Hvis du kører denne procedure som en opgaveguide, skal du låse opgaveguiden op, hvis du vil søge i kategorien.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="6ae3d-114">Hvis et hierarki ikke var tilgængeligt, skal du oprette det ved at klikke på Ny.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-114">If a hierarchy was not available, you’d create it by clicking New.</span></span> <span data-ttu-id="6ae3d-115">Det kan du kun gøre én gang.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-115">This can only be done once.</span></span>  
2. <span data-ttu-id="6ae3d-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="6ae3d-117">Oprette et katalog</span><span class="sxs-lookup"><span data-stu-id="6ae3d-117">Create a catalog</span></span>
1. <span data-ttu-id="6ae3d-118">Gå til Indkøb og forsyning > Kataloger > Indkøbskataloger.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-118">Go to Procurement and sourcing > Catalogs > Procurement catalogs.</span></span>
2. <span data-ttu-id="6ae3d-119">Klik på Nyt indkøbskatalog for at åbne dialogboksen, hvor du kan slippe den.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-119">Click New procurement catalog to open the drop dialog.</span></span>
3. <span data-ttu-id="6ae3d-120">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-120">In the Name field, type a value.</span></span>
4. <span data-ttu-id="6ae3d-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-121">Click OK.</span></span>
5. <span data-ttu-id="6ae3d-122">Udvid 'FIRMAS INDKØBSKATEGORIER' i træet.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-122">In the tree, expand 'CORP PROCUREMENT CATEGORIES'.</span></span>
6. <span data-ttu-id="6ae3d-123">Udvid 'KONTORMASKINER' i træet.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-123">In the tree, expand 'OFFICE MACHINES'.</span></span>
7. <span data-ttu-id="6ae3d-124">Vælg 'Computere' i træet.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-124">In the tree, select 'Computers'.</span></span>
    * <span data-ttu-id="6ae3d-125">Produkterne fra indkøbskategorien vises på listen.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="6ae3d-126">Hvis du vil føje et produkt til kategorien, skal du gøre det på siden Indkøbskategorihierarki eller på siden Vareoplysninger.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-126">If you want to add a product to the category you need to do this on the Procurement category hierarchy page or on the Item details page.</span></span>  
    * <span data-ttu-id="6ae3d-127">Standardopdateringstypen bestemmer, om nye produkter, der er føjet til indkøbskategorihierarkiet, er synlige i kataloget med det samme.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-127">The Default update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="6ae3d-128">Hvis opdateringstypen er indstillet til Dynamisk, kan ændringer ses øjeblikkeligt.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-128">If the update type is set to Dynamic, changes are visible immediately.</span></span> <span data-ttu-id="6ae3d-129">Hvis opdateringstypen er Statisk, er nye produkter kun synlige for brugere af kataloget, når kataloget er blevet udgivet igen.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-129">If the update type is Static, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="6ae3d-130">Publiceringshandling er tilgængelig i handlingsruden øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-130">The Publish action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="6ae3d-131">Hvis produkter fjernes fra indkøbskategorihierarkiet, er ændringen straks synlig, uanset hvilken værdi der er i feltet Standardopdateringstype.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the Default update type field.</span></span>  
8. <span data-ttu-id="6ae3d-132">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-132">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="6ae3d-133">klik på Skjul.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-133">Click Hide.</span></span>
10. <span data-ttu-id="6ae3d-134">Klik på Katalognavigation i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-134">On the Action Pane, click Category navigation.</span></span>
11. <span data-ttu-id="6ae3d-135">Klik på Deaktiver.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-135">Click Disable.</span></span>
12. <span data-ttu-id="6ae3d-136">Klik på Katalognavigation i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-136">On the Action Pane, click Category navigation.</span></span>
13. <span data-ttu-id="6ae3d-137">Klik på Enable.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-137">Click Enable.</span></span>
14. <span data-ttu-id="6ae3d-138">Klik på Aktivér katalog.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-138">Click Activate catalog.</span></span>
15. <span data-ttu-id="6ae3d-139">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-139">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="6ae3d-140">Gør kataloget synligt</span><span class="sxs-lookup"><span data-stu-id="6ae3d-140">Make the catalog visible</span></span>
1. <span data-ttu-id="6ae3d-141">Gå til Indkøb og forsyning > Konfiguration > Politikker > Indkøbspolitikker.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-141">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="6ae3d-142">Vælg indkøbspolitikken USMF.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-142">Select Procurement Policy USMF.</span></span>
    * <span data-ttu-id="6ae3d-143">Du skal vælge indkøbspolitik, så den juridiske enhed, som arbejderen har knyttet til din brugerprofil, kan bestille produkter.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-143">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="6ae3d-144">I USMF-demodataene er administratorbrugeren knyttet til den arbejder, der hedder Julia Funderburk, og hun bestiller som standard produkter i USMF.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-144">In the USMF demo data, the Admin user is connected to the worker called Julia Funderburk, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="6ae3d-145">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-145">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6ae3d-146">Vælg det katalog, du netop har oprettet.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-146">Select the catalog that you’ve just created.</span></span>
5. <span data-ttu-id="6ae3d-147">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-147">Click OK.</span></span>
6. <span data-ttu-id="6ae3d-148">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-148">Close the page.</span></span>
7. <span data-ttu-id="6ae3d-149">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-149">Close the page.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="6ae3d-150">Brug kataloget</span><span class="sxs-lookup"><span data-stu-id="6ae3d-150">Use the catalog</span></span>
1. <span data-ttu-id="6ae3d-151">Gå til Indkøb og Forsyning > Indkøbsrekvisitioner > Alle indkøbsrekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-151">Go to Procurement and sourcing > Purchase requisitions > All purchase requisitions.</span></span>
2. <span data-ttu-id="6ae3d-152">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-152">Click New.</span></span>
3. <span data-ttu-id="6ae3d-153">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-153">In the Name field, type a value.</span></span>
4. <span data-ttu-id="6ae3d-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-154">Click OK.</span></span>
5. <span data-ttu-id="6ae3d-155">Klik på Tilføj produkter.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-155">Click Add products.</span></span>
6. <span data-ttu-id="6ae3d-156">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6ae3d-157">Du kan bruge kategorihierarkiet til venstre eller filteret øverst på listen til at filtrere produkterne.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-157">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="6ae3d-158">Klik på Føj til linjer</span><span class="sxs-lookup"><span data-stu-id="6ae3d-158">Click Add to lines.</span></span>
8. <span data-ttu-id="6ae3d-159">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-159">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="6ae3d-160">Klik på Føj til linjer</span><span class="sxs-lookup"><span data-stu-id="6ae3d-160">Click Add to lines.</span></span>
10. <span data-ttu-id="6ae3d-161">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6ae3d-161">Click OK.</span></span>

