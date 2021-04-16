---
title: Kontrollere tilgængelighed af lagerbeholdning
description: Denne fremgangsmåde viser, hvordan du kontrollerer disponible og fysisk disponibel lagerbeholdning for et bestemt varenummer.
author: ShylaThompson
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1b68a40ba433f7db6eb910961cd429629387bbe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834091"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="0ea04-103">Kontrollere tilgængelighed af lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="0ea04-103">Check the availability of stock</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0ea04-104">Denne fremgangsmåde viser, hvordan du kontrollerer disponible og fysisk disponibel lagerbeholdning for et bestemt varenummer.</span><span class="sxs-lookup"><span data-stu-id="0ea04-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="0ea04-105">Den viser også, hvordan du får leveringsoplysninger relateret til en vare.</span><span class="sxs-lookup"><span data-stu-id="0ea04-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="0ea04-106">Fysisk disponibel lagerbeholdning er den disponible lagerbeholdning, der er tilgængelig – den er købt, modtaget og registreret.</span><span class="sxs-lookup"><span data-stu-id="0ea04-106">Physical on-hand inventory is the on-hand inventory that's available – that is, it's purchased, received and registered.</span></span> <span data-ttu-id="0ea04-107">Den disponible lagerbeholdning indeholder den tilgængelige disponible lagerbeholdning, men også det lager, der er bestilt og forventes, men endnu ikke modtaget eller registreret.</span><span class="sxs-lookup"><span data-stu-id="0ea04-107">On-hand inventory includes the available on-hand inventory, but also the inventory that's been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="0ea04-108">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="0ea04-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="0ea04-109">Hvis du bruger USMF, kan du bruge eksempelværdier, der vises.</span><span class="sxs-lookup"><span data-stu-id="0ea04-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="0ea04-110">Disse opgaver udføres normalt af en lagerarbejder.</span><span class="sxs-lookup"><span data-stu-id="0ea04-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="0ea04-111">Kontrollér disponibel lagerbeholdning for en vare</span><span class="sxs-lookup"><span data-stu-id="0ea04-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="0ea04-112">Gå til **Navigationsrude > Moduler > Lagerstyring > Forespørgsler og rapporter > Disponibel lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-112">Go to **Navigation pane > Modules > Inventory management > Inquiries and reports > On-hand inventory**.</span></span>
2. <span data-ttu-id="0ea04-113">Vælg rækken **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-113">Select the **Item number** row.</span></span> <span data-ttu-id="0ea04-114">Hvis du vil forespørge om den disponible lagerbeholdning efter varenummer, skal du markere den række, hvor tabellen er angivet til **Disponibel lagerbeholdning** og Felt er angivet til **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-114">To query the on-hand inventory by item number, select the row where the Table is set to **On-hand inventory** and Field is set to **Item** number.</span></span>
3. <span data-ttu-id="0ea04-115">Vælg den vare, du vil forespørge på, i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-115">In the **Criteria** field, select the item you want to query.</span></span> <span data-ttu-id="0ea04-116">Hvis du bruger demodatafirmaet USMF, kan du vælge 'M9201'.</span><span class="sxs-lookup"><span data-stu-id="0ea04-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="0ea04-117">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-117">Click **OK**.</span></span>
5. <span data-ttu-id="0ea04-118">Klik på **Dimensioner** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-118">On the **Action Pane**, click **Dimensions**.</span></span> <span data-ttu-id="0ea04-119">Med fanen **Dimensioner** kan du vælge, hvor mange oplysninger du vil se om den disponible lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="0ea04-119">The **Dimensions** tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="0ea04-120">Hvis du har brug for data vedrørende reservation, skal du få vist alle lagerdimensioner for de varer, der bruger avancerede lagerstedsprocesser (WMS).</span><span class="sxs-lookup"><span data-stu-id="0ea04-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WMS) processes.</span></span>
6. <span data-ttu-id="0ea04-121">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-121">Click **OK**.</span></span>
7. <span data-ttu-id="0ea04-122">Klik på **Relaterede oplysninger** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-122">On the **Action Pane**, click **Related information**.</span></span> <span data-ttu-id="0ea04-123">Hvis du ikke kan se denne indstilling, skal du muligvis klikke på ellipseknappen (...) for at få vist yderligere indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0ea04-123">If you don't see this option, you may need to click on the Ellipsis button (…) to see additional Action Pane options.</span></span>
8. <span data-ttu-id="0ea04-124">Klik på **Leveringsoversigt**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-124">Click **Supply overview**.</span></span> <span data-ttu-id="0ea04-125">Fanen **Leveringsoversigt** indeholder leveringsoplysninger for en bestemt vare, som disponibelt antal, leveringstid og kreditoroplysninger.</span><span class="sxs-lookup"><span data-stu-id="0ea04-125">The **Supply overview** tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="0ea04-126">Udvid sektionen **Tilgængelige**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-126">Expand the **On-hand** section.</span></span>
10. <span data-ttu-id="0ea04-127">Udvid sektionen **Kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-127">Expand the **Vendors** section.</span></span>
11. <span data-ttu-id="0ea04-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0ea04-128">Close the page.</span></span>
12. <span data-ttu-id="0ea04-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0ea04-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="0ea04-130">Kontrollér fysisk disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="0ea04-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="0ea04-131">Gå til **Navigationsrude > Moduler > Lokationsstyring > Forespørgsler og rapporter > Fysisk disponibel lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-131">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > Physical on-hand inventory**.</span></span>
2. <span data-ttu-id="0ea04-132">Indtast en værdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-132">In the **Item number** field, type a value.</span></span> <span data-ttu-id="0ea04-133">Du kan bruge felterne Sted og Lagersted til at filtrere listen over varer.</span><span class="sxs-lookup"><span data-stu-id="0ea04-133">You can use the Site and Warehouse fields to filter the list of items.</span></span> 
3. <span data-ttu-id="0ea04-134">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="0ea04-134">Refresh the page.</span></span>
4. <span data-ttu-id="0ea04-135">Klik på **Vis dimensioner** i **Handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-135">On the **Action Pane**, click **Display Dimensions**.</span></span> <span data-ttu-id="0ea04-136">Med fanen Dimensionsvisning kan du vælge, hvor mange oplysninger du vil se om den disponible lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="0ea04-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>
5. <span data-ttu-id="0ea04-137">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-137">Click **OK**.</span></span>
6. <span data-ttu-id="0ea04-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0ea04-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="0ea04-139">Kontrollér disponibel lagerbeholdning efter lokation.</span><span class="sxs-lookup"><span data-stu-id="0ea04-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="0ea04-140">Gå til **Navigationsrude > Moduler > Lokationsstyring > Forespørgsler og rapporter > Disponibel efter lokation**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-140">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > On hand by location**.</span></span>
2. <span data-ttu-id="0ea04-141">Skriv en værdi i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-141">In the **Warehouse** field, type a value.</span></span> <span data-ttu-id="0ea04-142">Hvis du bruger demodatafirmaet USMF, kan du bruge "51".</span><span class="sxs-lookup"><span data-stu-id="0ea04-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="0ea04-143">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="0ea04-143">Refresh the page.</span></span>
4. <span data-ttu-id="0ea04-144">Klik på **Vis dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-144">Click **Display Dimensions**.</span></span>
5. <span data-ttu-id="0ea04-145">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ea04-145">Click **OK**.</span></span>
6. <span data-ttu-id="0ea04-146">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0ea04-146">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]