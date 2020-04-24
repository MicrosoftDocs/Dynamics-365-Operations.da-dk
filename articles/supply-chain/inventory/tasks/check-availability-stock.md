---
title: Kontrollere tilgængelighed af lagerbeholdning
description: Denne fremgangsmåde viser, hvordan du kontrollerer disponible og fysisk disponibel lagerbeholdning for et bestemt varenummer.
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e76c123ffbeb33cbc3ba01b4b2758208ed0c445f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204211"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="57542-103">Kontrollere tilgængelighed af lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="57542-103">Check the availability of stock</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57542-104">Denne fremgangsmåde viser, hvordan du kontrollerer disponible og fysisk disponibel lagerbeholdning for et bestemt varenummer.</span><span class="sxs-lookup"><span data-stu-id="57542-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="57542-105">Den viser også, hvordan du får leveringsoplysninger relateret til en vare.</span><span class="sxs-lookup"><span data-stu-id="57542-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="57542-106">Fysisk disponibel lagerbeholdning er den disponible lagerbeholdning, der er tilgængelig – den er købt, modtaget og registreret.</span><span class="sxs-lookup"><span data-stu-id="57542-106">Physical on-hand inventory is the on-hand inventory that's available – that is, it's purchased, received and registered.</span></span> <span data-ttu-id="57542-107">Den disponible lagerbeholdning indeholder den tilgængelige disponible lagerbeholdning, men også det lager, der er bestilt og forventes, men endnu ikke modtaget eller registreret.</span><span class="sxs-lookup"><span data-stu-id="57542-107">On-hand inventory includes the available on-hand inventory, but also the inventory that's been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="57542-108">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="57542-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="57542-109">Hvis du bruger USMF, kan du bruge eksempelværdier, der vises.</span><span class="sxs-lookup"><span data-stu-id="57542-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="57542-110">Disse opgaver udføres normalt af en lagerarbejder.</span><span class="sxs-lookup"><span data-stu-id="57542-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="57542-111">Kontrollér disponibel lagerbeholdning for en vare</span><span class="sxs-lookup"><span data-stu-id="57542-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="57542-112">Gå til **Navigationsrude > Moduler > Lagerstyring > Forespørgsler og rapporter > Disponibel lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="57542-112">Go to **Navigation pane > Modules > Inventory management > Inquiries and reports > On-hand inventory**.</span></span>
2. <span data-ttu-id="57542-113">Vælg rækken **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="57542-113">Select the **Item number** row.</span></span> <span data-ttu-id="57542-114">Hvis du vil forespørge om den disponible lagerbeholdning efter varenummer, skal du markere den række, hvor tabellen er angivet til **Disponibel lagerbeholdning** og Felt er angivet til **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="57542-114">To query the on-hand inventory by item number, select the row where the Table is set to **On-hand inventory** and Field is set to **Item** number.</span></span>
3. <span data-ttu-id="57542-115">Vælg den vare, du vil forespørge på, i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="57542-115">In the **Criteria** field, select the item you want to query.</span></span> <span data-ttu-id="57542-116">Hvis du bruger demodatafirmaet USMF, kan du vælge 'M9201'.</span><span class="sxs-lookup"><span data-stu-id="57542-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="57542-117">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="57542-117">Click **OK**.</span></span>
5. <span data-ttu-id="57542-118">Klik på **Dimensioner** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="57542-118">On the **Action pane**, click **Dimensions**.</span></span> <span data-ttu-id="57542-119">Med fanen **Dimensioner** kan du vælge, hvor mange oplysninger du vil se om den disponible lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="57542-119">The **Dimensions** tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="57542-120">Hvis du har brug for data vedrørende reservation, skal du få vist alle lagerdimensioner for de varer, der bruger avancerede lagerstedsprocesser (WHS).</span><span class="sxs-lookup"><span data-stu-id="57542-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>
6. <span data-ttu-id="57542-121">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="57542-121">Click **OK**.</span></span>
7. <span data-ttu-id="57542-122">Klik på **Relaterede oplysninger** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="57542-122">On the **Action Pane**, click **Related information**.</span></span> <span data-ttu-id="57542-123">Hvis du ikke kan se denne indstilling, skal du muligvis klikke på ellipseknappen (...) for at få vist yderligere indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="57542-123">If you don't see this option, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>
8. <span data-ttu-id="57542-124">Klik på **Leveringsoversigt**.</span><span class="sxs-lookup"><span data-stu-id="57542-124">Click **Supply overview**.</span></span> <span data-ttu-id="57542-125">Fanen **Leveringsoversigt** indeholder leveringsoplysninger for en bestemt vare, som disponibelt antal, leveringstid og kreditoroplysninger.</span><span class="sxs-lookup"><span data-stu-id="57542-125">The **Supply overview** tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="57542-126">Udvid sektionen **Tilgængelige**.</span><span class="sxs-lookup"><span data-stu-id="57542-126">Expand the **On-hand** section.</span></span>
10. <span data-ttu-id="57542-127">Udvid sektionen **Kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="57542-127">Expand the **Vendors** section.</span></span>
11. <span data-ttu-id="57542-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="57542-128">Close the page.</span></span>
12. <span data-ttu-id="57542-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="57542-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="57542-130">Kontrollér fysisk disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="57542-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="57542-131">Gå til **Navigationsrude > Moduler > Lokationsstyring > Forespørgsler og rapporter > Fysisk disponibel lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="57542-131">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > Physical on-hand inventory**.</span></span>
2. <span data-ttu-id="57542-132">Indtast en værdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="57542-132">In the **Item number** field, type a value.</span></span> <span data-ttu-id="57542-133">Du kan bruge felterne Sted og Lagersted til at filtrere listen over varer.</span><span class="sxs-lookup"><span data-stu-id="57542-133">You can use the Site and Warehouse fields to filter the list of items.</span></span> 
3. <span data-ttu-id="57542-134">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="57542-134">Refresh the page.</span></span>
4. <span data-ttu-id="57542-135">Klik på **Vis dimensioner** i **Handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="57542-135">On the **Action pane**, click **Display Dimensions**.</span></span> <span data-ttu-id="57542-136">Med fanen Dimensionsvisning kan du vælge, hvor mange oplysninger du vil se om den disponible lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="57542-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>
5. <span data-ttu-id="57542-137">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="57542-137">Click **OK**.</span></span>
6. <span data-ttu-id="57542-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="57542-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="57542-139">Kontrollér disponibel lagerbeholdning efter lokation.</span><span class="sxs-lookup"><span data-stu-id="57542-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="57542-140">Gå til **Navigationsrude > Moduler > Lokationsstyring > Forespørgsler og rapporter > Disponibel efter lokation**.</span><span class="sxs-lookup"><span data-stu-id="57542-140">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > On hand by location**.</span></span>
2. <span data-ttu-id="57542-141">Skriv en værdi i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="57542-141">In the **Warehouse** field, type a value.</span></span> <span data-ttu-id="57542-142">Hvis du bruger demodatafirmaet USMF, kan du bruge "51".</span><span class="sxs-lookup"><span data-stu-id="57542-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="57542-143">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="57542-143">Refresh the page.</span></span>
4. <span data-ttu-id="57542-144">Klik på **Vis dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="57542-144">Click **Display Dimensions**.</span></span>
5. <span data-ttu-id="57542-145">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="57542-145">Click **OK**.</span></span>
6. <span data-ttu-id="57542-146">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="57542-146">Close the page.</span></span>

