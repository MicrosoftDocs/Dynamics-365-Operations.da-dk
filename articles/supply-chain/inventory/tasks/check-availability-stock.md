--- 
title: "Kontrollere tilgængelighed af lagerbeholdning"
description: "Denne fremgangsmåde viser, hvordan du kontrollerer disponible og fysisk disponibel lagerbeholdning for et bestemt varenummer."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: 
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6db29d422e7dfd7b2481b4fcbc404278e37511d1
ms.openlocfilehash: 26a8f51eda1f4249862a23fa0103b7a144d974a1
ms.contentlocale: da-dk
ms.lasthandoff: 10/08/2018

---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="55a42-103">Kontrollere tilgængelighed af lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="55a42-103">Check the availability of stock</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55a42-104">Denne fremgangsmåde viser, hvordan du kontrollerer disponible og fysisk disponibel lagerbeholdning for et bestemt varenummer.</span><span class="sxs-lookup"><span data-stu-id="55a42-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="55a42-105">Den viser også, hvordan du får leveringsoplysninger relateret til en vare.</span><span class="sxs-lookup"><span data-stu-id="55a42-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="55a42-106">Fysisk disponibel lagerbeholdning er den disponible lagerbeholdning, der er tilgængelig – den er købt, modtaget og registreret.</span><span class="sxs-lookup"><span data-stu-id="55a42-106">Physical on-hand inventory is the on-hand inventory that’s available – that is, it’s purchased, received and registered.</span></span> <span data-ttu-id="55a42-107">Den disponible lagerbeholdning indeholder den tilgængelige disponible lagerbeholdning, men også det lager, der er bestilt og forventes, men endnu ikke modtaget eller registreret.</span><span class="sxs-lookup"><span data-stu-id="55a42-107">On-hand inventory includes the available on-hand inventory, but also the inventory that’s been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="55a42-108">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="55a42-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="55a42-109">Hvis du bruger USMF, kan du bruge eksempelværdier, der vises.</span><span class="sxs-lookup"><span data-stu-id="55a42-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="55a42-110">Disse opgaver udføres normalt af en lagerarbejder.</span><span class="sxs-lookup"><span data-stu-id="55a42-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="55a42-111">Kontrollér disponibel lagerbeholdning for en vare</span><span class="sxs-lookup"><span data-stu-id="55a42-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="55a42-112">Gå til Lagerstyring > Forespørgsler og rapporter > Disponibel lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="55a42-112">Go to Inventory management > Inquiries and reports > On-hand inventory.</span></span>
2. <span data-ttu-id="55a42-113">Vælg varenummerrækken.</span><span class="sxs-lookup"><span data-stu-id="55a42-113">Select the Item number row.</span></span>
    * <span data-ttu-id="55a42-114">Hvis du vil forespørge om den disponible lagerbeholdning efter varenummer, skal du markere den række, hvor tabellen er angivet til den disponible lagerbeholdning og felt er angivet til varenummer.</span><span class="sxs-lookup"><span data-stu-id="55a42-114">To query the on-hand inventory by item number, select the row where the Table is set to On-hand inventory and Field is set to Item number.</span></span>  
3. <span data-ttu-id="55a42-115">Vælg den vare, du vil forespørge på, i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="55a42-115">In the Criteria field, select the item you want to query.</span></span>
    * <span data-ttu-id="55a42-116">Hvis du bruger demodatafirmaet USMF, kan du vælge 'M9201'.</span><span class="sxs-lookup"><span data-stu-id="55a42-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="55a42-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="55a42-117">Click OK.</span></span>
5. <span data-ttu-id="55a42-118">Klik på Dimensioner.</span><span class="sxs-lookup"><span data-stu-id="55a42-118">Click Dimensions.</span></span>
    * <span data-ttu-id="55a42-119">Med fanen Dimensioner kan du vælge, hvor mange oplysninger du vil se om den disponible lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="55a42-119">The Dimensions tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="55a42-120">Hvis du har brug for data vedrørende reservation, skal du få vist alle lagerdimensioner for de varer, der bruger avancerede lagerstedsprocesser (WHS).</span><span class="sxs-lookup"><span data-stu-id="55a42-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>  
6. <span data-ttu-id="55a42-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="55a42-121">Click OK.</span></span>
7. <span data-ttu-id="55a42-122">Klik på Relaterede oplysninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="55a42-122">On the Action Pane, click Related information.</span></span>
    * <span data-ttu-id="55a42-123">Hvis du ikke kan se dette, skal du muligvis klikke på ellipseknappen (...) for at få vist yderligere indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="55a42-123">If you don’t see this, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>  
8. <span data-ttu-id="55a42-124">Klik på Leveringsoversigt.</span><span class="sxs-lookup"><span data-stu-id="55a42-124">Click Supply overview.</span></span>
    * <span data-ttu-id="55a42-125">Fanen Leveringsoversigt indeholder leveringsoplysninger for en bestemt vare, som disponibelt antal, leveringstid og kreditoroplysninger.</span><span class="sxs-lookup"><span data-stu-id="55a42-125">The Supply overview tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="55a42-126">Udvid sektionen Tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="55a42-126">Expand the On-hand section.</span></span>
10. <span data-ttu-id="55a42-127">Vis sektionen Kreditorer.</span><span class="sxs-lookup"><span data-stu-id="55a42-127">Expand the Vendors section.</span></span>
11. <span data-ttu-id="55a42-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="55a42-128">Close the page.</span></span>
12. <span data-ttu-id="55a42-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="55a42-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="55a42-130">Kontrollér fysisk disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="55a42-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="55a42-131">Gå til Lagerstedsstyring > Forespørgsler og rapporter > Fysisk disponibel lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="55a42-131">Go to Warehouse management > Inquiries and reports > Physical on-hand inventory.</span></span>
2. <span data-ttu-id="55a42-132">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="55a42-132">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="55a42-133">Du kan bruge felterne Sted og Lagersted til at filtrere listen over varer.</span><span class="sxs-lookup"><span data-stu-id="55a42-133">You can use the Site and Warehouse fields to filter the list of items.</span></span>  
3. <span data-ttu-id="55a42-134">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="55a42-134">Refresh the page.</span></span>
4. <span data-ttu-id="55a42-135">Klik på Visningsdimensioner.</span><span class="sxs-lookup"><span data-stu-id="55a42-135">Click Display Dimensions.</span></span>
    * <span data-ttu-id="55a42-136">Med fanen Dimensionsvisning kan du vælge, hvor mange oplysninger du vil se om den disponible lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="55a42-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>  
5. <span data-ttu-id="55a42-137">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="55a42-137">Click OK.</span></span>
6. <span data-ttu-id="55a42-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="55a42-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="55a42-139">Kontrollér disponibel lagerbeholdning efter lokation.</span><span class="sxs-lookup"><span data-stu-id="55a42-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="55a42-140">Gå til Lagerstedsstyring > Forespørgsler og rapporter > Disponibel efter lokation.</span><span class="sxs-lookup"><span data-stu-id="55a42-140">Go to Warehouse management > Inquiries and reports > On hand by location.</span></span>
2. <span data-ttu-id="55a42-141">Skriv en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="55a42-141">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="55a42-142">Hvis du bruger demodatafirmaet USMF, kan du bruge "51".</span><span class="sxs-lookup"><span data-stu-id="55a42-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="55a42-143">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="55a42-143">Refresh the page.</span></span>
4. <span data-ttu-id="55a42-144">Klik på Visningsdimensioner.</span><span class="sxs-lookup"><span data-stu-id="55a42-144">Click Display Dimensions.</span></span>
5. <span data-ttu-id="55a42-145">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="55a42-145">Click OK.</span></span>
6. <span data-ttu-id="55a42-146">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="55a42-146">Close the page.</span></span>


