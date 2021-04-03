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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 772c7584549b30a34e371a7911131edc01214ed8
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477628"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="6ced9-103">Konfigurere lagersted</span><span class="sxs-lookup"><span data-stu-id="6ced9-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6ced9-104">Dette emne beskriver, hvordan du kan konfigurere et lagersted til brug med en ny kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6ced9-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6ced9-105">Hver enkelt Commerce-kanal kræver, at den er tilknyttet et konfigureret lagersted.</span><span class="sxs-lookup"><span data-stu-id="6ced9-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="6ced9-106">Følgende procedurer indeholder den minimumkonfiguration, der kræves for at konfigurere et lagersted til en Commerce-kanal.</span><span class="sxs-lookup"><span data-stu-id="6ced9-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="6ced9-107">Du kan få yderligere oplysninger om opsætning af lagersteder i [Oversigt over lokationsstyring](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6ced9-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="6ced9-108">Konfigurer et sted til et lagersted</span><span class="sxs-lookup"><span data-stu-id="6ced9-108">Configure a warehouse site</span></span>

<span data-ttu-id="6ced9-109">Før du konfigurerer et lagersted, skal du konfigurere et sted til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="6ced9-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="6ced9-110">Gør følgende for at konfigurere et sted til et lagersted.</span><span class="sxs-lookup"><span data-stu-id="6ced9-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="6ced9-111">Gå til **Moduler \> Detail og handel \> Konfiguration af kanal \> Steder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="6ced9-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="6ced9-112">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6ced9-113">Angiv en værdi i feltet **Sted**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="6ced9-114">Angiv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="6ced9-115">Angiv den relevante **Tidszone** i sektionen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="6ced9-116">Angiv en adresse i feltet **Adresser**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="6ced9-117">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6ced9-118">Følgende billede viser et eksempel på et sted til et lagersted.</span><span class="sxs-lookup"><span data-stu-id="6ced9-118">The following image shows an example warehouse site.</span></span>

![Eksempel på et sted til et lagersted](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="6ced9-120">Konfigurer et lagersted</span><span class="sxs-lookup"><span data-stu-id="6ced9-120">Set up a warehouse</span></span>

<span data-ttu-id="6ced9-121">Gør følgende for at konfigurere et lagersted.</span><span class="sxs-lookup"><span data-stu-id="6ced9-121">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="6ced9-122">Gå til **Moduler \> Detail og handel \> Konfiguration af kanal \> Lagersteder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="6ced9-122">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="6ced9-123">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-123">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6ced9-124">Indtast en værdi i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-124">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="6ced9-125">Hvis dette er en 1:1-tilknytning til en butik, skal du overveje at bruge butiksnavnet eller navnet på et regionalt distributionscenter.</span><span class="sxs-lookup"><span data-stu-id="6ced9-125">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="6ced9-126">Angiv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-126">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="6ced9-127">Vælg det sted til lagerstedet, du tidligere har oprettet, på rullelisten **Sted**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-127">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="6ced9-128">Vælg **Standard** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-128">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="6ced9-129">Hvis du vil angive et **Karantænelagersted**, skal du først følge disse trin for at oprette et ekstra lagersted, hvor **Type** er indstillet til **Karantæne**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-129">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="6ced9-130">Hvis du vil angive et **Transitlagersted**, skal du først følge disse trin for at oprette et ekstra lagersted, hvor **Type** er indstillet til **Transit**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-130">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="6ced9-131">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-131">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="6ced9-132">Konfigurer lagergange</span><span class="sxs-lookup"><span data-stu-id="6ced9-132">Set up inventory aisles</span></span>

<span data-ttu-id="6ced9-133">Følg disse trin for at konfigurere lagergange.</span><span class="sxs-lookup"><span data-stu-id="6ced9-133">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="6ced9-134">Gå til **Moduler \> Retail og Commerce \> Konfiguration af kanal \> Konfiguration af lokation \> Lagergange** i navigationsruden..</span><span class="sxs-lookup"><span data-stu-id="6ced9-134">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="6ced9-135">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-135">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6ced9-136">Vælg det lagersted, du tidligere har oprettet, på rullelisten **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-136">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="6ced9-137">Angiv et navn i feltet **Gang** (f.eks. "Def").</span><span class="sxs-lookup"><span data-stu-id="6ced9-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="6ced9-138">Angiv et navn i feltet **Navn** (f.eks. "Standardgang").</span><span class="sxs-lookup"><span data-stu-id="6ced9-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="6ced9-139">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="6ced9-140">Konfigurer lokationer til lagerstedets lager</span><span class="sxs-lookup"><span data-stu-id="6ced9-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="6ced9-141">Gør følgende, hvis du vil oprette lokationer til lagerstedets lager for standard, beskadiget og returneret lager.</span><span class="sxs-lookup"><span data-stu-id="6ced9-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="6ced9-142">Gå til **Moduler \> Detail og handel \> Konfiguration af kanal \> Lagersteder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="6ced9-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="6ced9-143">Vælg det lagersted, som du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="6ced9-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="6ced9-144">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6ced9-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="6ced9-145">Vælg **Lagersted** i handlingsruden, og vælg derefter **Lagerlokation**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="6ced9-146">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-146">On the action pane, select **New**.</span></span> <span data-ttu-id="6ced9-147">Rullelisten **Lagersted** bør som standard vise dit nye lagersted.</span><span class="sxs-lookup"><span data-stu-id="6ced9-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="6ced9-148">Angiv navnet på den gang, du har angivet tidligere, i fetlet **Gang**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="6ced9-149">Angiv **Manuel opdatering** til **Ja**</span><span class="sxs-lookup"><span data-stu-id="6ced9-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="6ced9-150">Angiv navnet på lagerstedet i feltet **Sted**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="6ced9-151">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="6ced9-152">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="6ced9-153">Rullelisten **Lagersted** bør som standard vise dit nye lagersted.</span><span class="sxs-lookup"><span data-stu-id="6ced9-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="6ced9-154">Angiv navnet på den gang, du har angivet tidligere, i fetlet **Gang**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="6ced9-155">Angiv **Manuel opdatering** til **Ja**</span><span class="sxs-lookup"><span data-stu-id="6ced9-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="6ced9-156">Angiv "Beskadiget" i feltet **Sted**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="6ced9-157">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="6ced9-158">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="6ced9-159">Rullelisten **Lagersted** bør som standard vise dit nye lagersted.</span><span class="sxs-lookup"><span data-stu-id="6ced9-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="6ced9-160">Angiv navnet på den gang, du har angivet tidligere, i fetlet **Gang**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="6ced9-161">Angiv **Manuel opdatering** til **Ja**</span><span class="sxs-lookup"><span data-stu-id="6ced9-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="6ced9-162">Angiv "Returneringer" i feltet **Sted**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="6ced9-163">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="6ced9-164">Følgende billede viser opsætningen af en lagerlokation til et lagersted i San Francisco.</span><span class="sxs-lookup"><span data-stu-id="6ced9-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Eksempel på opsætning af lagerlokation](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="6ced9-166">Akslut konfigurationen af lagerstedet</span><span class="sxs-lookup"><span data-stu-id="6ced9-166">Complete warehouse setup</span></span>

<span data-ttu-id="6ced9-167">Gør følgende for at fuldføre konfigurationen af lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="6ced9-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="6ced9-168">Gå til **Moduler \> Detail og handel \> Konfiguration af kanal \> Lagersteder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="6ced9-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="6ced9-169">Vælg det lagersted, som du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="6ced9-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="6ced9-170">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6ced9-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="6ced9-171">Under **Lager- og lokationsstyring**:</span><span class="sxs-lookup"><span data-stu-id="6ced9-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="6ced9-172">Angiv **Standardplacering for modtagelse** til den standardlokalitet, der blev oprettet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="6ced9-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="6ced9-173">Vælg **Standardafgangslokation** til den standardlokalitet, der blev oprettet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="6ced9-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="6ced9-174">Angiv en adresse på lagerstedet i sektionen **Adresser**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="6ced9-175">Under sektionen **Detail**:</span><span class="sxs-lookup"><span data-stu-id="6ced9-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="6ced9-176">Angiv placeringen for returnering, der tidligere blev oprettet, i feltet **Placering af standardreturnering**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="6ced9-177">Angiv **Butik** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="6ced9-178">Angiv **Vægt** til **1,00**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="6ced9-179">Angiv standardplaceringen, der tidligere blev oprettet, i feltet **Lagerdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="6ced9-180">Angiv **Fysisk negativt lager** til **Ja** under afsnittet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="6ced9-181">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6ced9-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6ced9-182">Følgende billede viser oplysninger om et konfigureret lagersted.</span><span class="sxs-lookup"><span data-stu-id="6ced9-182">The following image shows details for a configured warehouse.</span></span>

![Eksempel på konfigureret lagersted](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="6ced9-184">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6ced9-184">Additional resources</span></span>

[<span data-ttu-id="6ced9-185">Oversigt over lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="6ced9-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="6ced9-186">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="6ced9-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="6ced9-187">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="6ced9-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="6ced9-188">Konfigurer en detailkanal</span><span class="sxs-lookup"><span data-stu-id="6ced9-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="6ced9-189">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="6ced9-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="6ced9-190">Konfigurere en callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="6ced9-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
