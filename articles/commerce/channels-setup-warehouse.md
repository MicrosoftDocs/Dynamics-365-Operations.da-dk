---
title: Konfigurer et lagersted
description: Dette emne beskriver, hvordan du kan konfigurere et lagersted til brug med en ny kanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9ba12876a8c8f841733d8ec49c33e900211c4ab4
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057850"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="616de-103">Konfigurere lagersted</span><span class="sxs-lookup"><span data-stu-id="616de-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="616de-104">Dette emne beskriver, hvordan du kan konfigurere et lagersted til brug med en ny kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="616de-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="616de-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="616de-105">Overview</span></span>

<span data-ttu-id="616de-106">Hver enkelt Commerce-kanal kræver, at den er tilknyttet et konfigureret lagersted.</span><span class="sxs-lookup"><span data-stu-id="616de-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="616de-107">Følgende procedurer indeholder den minimumkonfiguration, der kræves for at konfigurere et lagersted til en Commerce-kanal.</span><span class="sxs-lookup"><span data-stu-id="616de-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="616de-108">Du kan få yderligere oplysninger om opsætning af lagersteder i [Oversigt over lokationsstyring](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview).</span><span class="sxs-lookup"><span data-stu-id="616de-108">For more information regarding warehouse setup, please see the [Warehouse management overview](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="616de-109">Konfigurer et sted til et lagersted</span><span class="sxs-lookup"><span data-stu-id="616de-109">Configure a warehouse site</span></span>

<span data-ttu-id="616de-110">Før du konfigurerer et lagersted, skal du konfigurere et sted til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="616de-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="616de-111">Gør følgende for at konfigurere et sted til et lagersted.</span><span class="sxs-lookup"><span data-stu-id="616de-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="616de-112">Gå til **Moduler \> Detail og handel \> Konfiguration af kanal \> Steder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="616de-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="616de-113">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="616de-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="616de-114">Angiv en værdi i feltet **Sted**.</span><span class="sxs-lookup"><span data-stu-id="616de-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="616de-115">Angiv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="616de-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="616de-116">Angiv den relevante **Tidszone** i sektionen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="616de-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="616de-117">Angiv en adresse i feltet **Adresser**.</span><span class="sxs-lookup"><span data-stu-id="616de-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="616de-118">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="616de-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="616de-119">Følgende billede viser et eksempel på et sted til et lagersted.</span><span class="sxs-lookup"><span data-stu-id="616de-119">The following image shows an example warehouse site.</span></span>

![Eksempel på et sted til et lagersted](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="616de-121">Konfigurer et lagersted</span><span class="sxs-lookup"><span data-stu-id="616de-121">Set up a warehouse</span></span>

<span data-ttu-id="616de-122">Gør følgende for at konfigurere et lagersted.</span><span class="sxs-lookup"><span data-stu-id="616de-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="616de-123">Gå til **Moduler \> Detail og handel \> Konfiguration af kanal \> Lagersteder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="616de-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="616de-124">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="616de-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="616de-125">Indtast en værdi i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="616de-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="616de-126">Hvis dette er en 1:1-tilknytning til en butik, skal du overveje at bruge butiksnavnet eller navnet på et regionalt distributionscenter.</span><span class="sxs-lookup"><span data-stu-id="616de-126">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="616de-127">Angiv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="616de-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="616de-128">Vælg det sted til lagerstedet, du tidligere har oprettet, på rullelisten **Sted**.</span><span class="sxs-lookup"><span data-stu-id="616de-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="616de-129">Vælg **Standard** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="616de-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="616de-130">Hvis du vil angive et **Karantænelagersted**, skal du først følge disse trin for at oprette et ekstra lagersted, hvor **Type** er indstillet til **Karantæne**.</span><span class="sxs-lookup"><span data-stu-id="616de-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="616de-131">Hvis du vil angive et **Transitlagersted**, skal du først følge disse trin for at oprette et ekstra lagersted, hvor **Type** er indstillet til **Transit**.</span><span class="sxs-lookup"><span data-stu-id="616de-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="616de-132">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="616de-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="616de-133">Konfigurer lagergange</span><span class="sxs-lookup"><span data-stu-id="616de-133">Set up inventory aisles</span></span>

<span data-ttu-id="616de-134">Følg disse trin for at konfigurere lagergange.</span><span class="sxs-lookup"><span data-stu-id="616de-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="616de-135">Gå til **Moduler \> Retail og Commerce \> Konfiguration af kanal \> Konfiguration af lokation \> Lagergange** i navigationsruden..</span><span class="sxs-lookup"><span data-stu-id="616de-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="616de-136">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="616de-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="616de-137">Vælg det lagersted, du tidligere har oprettet, på rullelisten **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="616de-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="616de-138">Angiv et navn i feltet **Gang** (f.eks. "Def").</span><span class="sxs-lookup"><span data-stu-id="616de-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="616de-139">Angiv et navn i feltet **Navn** (f.eks. "Standardgang").</span><span class="sxs-lookup"><span data-stu-id="616de-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="616de-140">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="616de-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="616de-141">Konfigurer lokationer til lagerstedets lager</span><span class="sxs-lookup"><span data-stu-id="616de-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="616de-142">Gør følgende, hvis du vil oprette lokationer til lagerstedets lager for standard, beskadiget og returneret lager.</span><span class="sxs-lookup"><span data-stu-id="616de-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="616de-143">Gå til **Moduler \> Detail og handel \> Konfiguration af kanal \> Lagersteder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="616de-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="616de-144">Vælg det lagersted, som du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="616de-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="616de-145">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="616de-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="616de-146">Vælg **Lagersted** i handlingsruden, og vælg derefter **Lagerlokation**.</span><span class="sxs-lookup"><span data-stu-id="616de-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="616de-147">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="616de-147">On the action pane, select **New**.</span></span> <span data-ttu-id="616de-148">Rullelisten **Lagersted** bør som standard vise dit nye lagersted.</span><span class="sxs-lookup"><span data-stu-id="616de-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="616de-149">Angiv navnet på den gang, du har angivet tidligere, i fetlet **Gang**.</span><span class="sxs-lookup"><span data-stu-id="616de-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="616de-150">Angiv **Manuel opdatering** til **Ja**</span><span class="sxs-lookup"><span data-stu-id="616de-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="616de-151">Angiv navnet på lagerstedet i feltet **Sted**.</span><span class="sxs-lookup"><span data-stu-id="616de-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="616de-152">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="616de-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="616de-153">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="616de-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="616de-154">Rullelisten **Lagersted** bør som standard vise dit nye lagersted.</span><span class="sxs-lookup"><span data-stu-id="616de-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="616de-155">Angiv navnet på den gang, du har angivet tidligere, i fetlet **Gang**.</span><span class="sxs-lookup"><span data-stu-id="616de-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="616de-156">Angiv **Manuel opdatering** til **Ja**</span><span class="sxs-lookup"><span data-stu-id="616de-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="616de-157">Angiv "Beskadiget" i feltet **Sted**.</span><span class="sxs-lookup"><span data-stu-id="616de-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="616de-158">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="616de-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="616de-159">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="616de-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="616de-160">Rullelisten **Lagersted** bør som standard vise dit nye lagersted.</span><span class="sxs-lookup"><span data-stu-id="616de-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="616de-161">Angiv navnet på den gang, du har angivet tidligere, i fetlet **Gang**.</span><span class="sxs-lookup"><span data-stu-id="616de-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="616de-162">Angiv **Manuel opdatering** til **Ja**</span><span class="sxs-lookup"><span data-stu-id="616de-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="616de-163">Angiv "Returneringer" i feltet **Sted**.</span><span class="sxs-lookup"><span data-stu-id="616de-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="616de-164">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="616de-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="616de-165">Følgende billede viser opsætningen af en lagerlokation til et lagersted i San Francisco.</span><span class="sxs-lookup"><span data-stu-id="616de-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Eksempel på opsætning af lagerlokation](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="616de-167">Akslut konfigurationen af lagerstedet</span><span class="sxs-lookup"><span data-stu-id="616de-167">Complete warehouse setup</span></span>

<span data-ttu-id="616de-168">Gør følgende for at fuldføre konfigurationen af lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="616de-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="616de-169">Gå til **Moduler \> Detail og handel \> Konfiguration af kanal \> Lagersteder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="616de-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="616de-170">Vælg det lagersted, som du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="616de-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="616de-171">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="616de-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="616de-172">Under **Lager- og lokationsstyring**:</span><span class="sxs-lookup"><span data-stu-id="616de-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="616de-173">Angiv **Standardplacering for modtagelse** til den standardlokalitet, der blev oprettet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="616de-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="616de-174">Vælg **Standardafgangslokation** til den standardlokalitet, der blev oprettet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="616de-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="616de-175">Angiv en adresse på lagerstedet i sektionen **Adresser**.</span><span class="sxs-lookup"><span data-stu-id="616de-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="616de-176">Under sektionen **Detail**:</span><span class="sxs-lookup"><span data-stu-id="616de-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="616de-177">Angiv placeringen for returnering, der tidligere blev oprettet, i feltet **Placering af standardreturnering**.</span><span class="sxs-lookup"><span data-stu-id="616de-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="616de-178">Angiv **Butik** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="616de-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="616de-179">Angiv **Vægt** til **1,00**.</span><span class="sxs-lookup"><span data-stu-id="616de-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="616de-180">Angiv standardplaceringen, der tidligere blev oprettet, i feltet **Lagerdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="616de-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="616de-181">Angiv **Fysisk negativt lager** til **Ja** under afsnittet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="616de-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="616de-182">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="616de-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="616de-183">Følgende billede viser oplysninger om et konfigureret lagersted.</span><span class="sxs-lookup"><span data-stu-id="616de-183">The following image shows details for a configured warehouse.</span></span>

![Eksempel på konfigureret lagersted](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="616de-185">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="616de-185">Additional resources</span></span>

[<span data-ttu-id="616de-186">Oversigt over lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="616de-186">Warehouse management overview</span></span>](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview)

[<span data-ttu-id="616de-187">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="616de-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="616de-188">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="616de-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="616de-189">Konfigurer en detailkanal</span><span class="sxs-lookup"><span data-stu-id="616de-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="616de-190">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="616de-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="616de-191">Konfigurere en callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="616de-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





