---
title: Definere dækningsregler for varer
description: Det demodatafirma, der bruges til at oprette denne procedure, er USMF.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd44c458da03807ddc1dc9d652da29c1404dbe64
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209599"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="09f6a-103">Definere dækningsregler for varer</span><span class="sxs-lookup"><span data-stu-id="09f6a-103">Define coverage rules for items</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09f6a-104">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="09f6a-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="09f6a-105">Denne procedure viser, hvordan du opretter disponeringsregler og tilsidesætter disponeringsindstillinger for et bestemt element.</span><span class="sxs-lookup"><span data-stu-id="09f6a-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="09f6a-106">Det viser også, hvordan du angiver standardindstillinger for lager.</span><span class="sxs-lookup"><span data-stu-id="09f6a-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="09f6a-107">Oprette en disponeringsgruppe</span><span class="sxs-lookup"><span data-stu-id="09f6a-107">Create a coverage group</span></span>
1. <span data-ttu-id="09f6a-108">Gå til **Navigationsrude > Moduler > Varedisponering > Opsætning > Disponeringsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-108">Go to **Navigation pane > Modules > Master planning > Setup > Coverage groups**.</span></span>
2. <span data-ttu-id="09f6a-109">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-109">Click **New**.</span></span>
3. <span data-ttu-id="09f6a-110">Skriv en værdi i feltet **Disponeringsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-110">In the **Coverage group** field, type a value.</span></span>
4. <span data-ttu-id="09f6a-111">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="09f6a-112">Skriv en værdi i feltet **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-112">In the **Calendar** field, type a value.</span></span> <span data-ttu-id="09f6a-113">Vælg den kalender, som varedisponering bruger til at oprette genopfyldningsforslag for varer i denne gruppe.</span><span class="sxs-lookup"><span data-stu-id="09f6a-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="09f6a-114">Vælg en indstilling i feltet **Disponeringskode**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-114">In the **Coverage code** field, select an option.</span></span> <span data-ttu-id="09f6a-115">Vælg 'Krav' til denne procedure.</span><span class="sxs-lookup"><span data-stu-id="09f6a-115">Select 'Requirement' for this procedure.</span></span>  
7. <span data-ttu-id="09f6a-116">Angiv '90' i feltet **Disponeringstidshorisont (dage)**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-116">In the **Coverage time fence (days) field**, enter '90'.</span></span> <span data-ttu-id="09f6a-117">For elementer i denne gruppe vil varedisponering oprette genopfyldningsforslag for op til 90 dage ud i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="09f6a-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="09f6a-118">Angiv '1' i feltet **Negative dage**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-118">In the **Negative days** field, enter '1'.</span></span>
9. <span data-ttu-id="09f6a-119">Angiv '1' i feltet **Positive dage**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-119">In the **Positive days** field, enter '1'.</span></span>
10. <span data-ttu-id="09f6a-120">Vis eller skjul sektionen **Andet**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-120">Expand or collapse the **Other** section.</span></span>
11. <span data-ttu-id="09f6a-121">Angiv '1' i feltet **Modtagelsesmargen lagt til behovsdato** under sektionen **Sikkerhedsmargen i dage**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-121">Under the **Safety margins in days** section, in the **Receipt margin added to requirement date** field, enter '1'.</span></span> <span data-ttu-id="09f6a-122">Hvis modtagelsesmargenen f.eks. angives til 1 dag, og en indkøbsordrelinje planlægges til tilgang d. 15. maj, beregner varedisponering den justerede modtagelsesdato som d. 16. maj.</span><span class="sxs-lookup"><span data-stu-id="09f6a-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="09f6a-123">Angiv '1' i feltet **Afgangsmargen trukket fra behovsdato**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-123">In the **Issue margin deducted from requirement date** field, enter '1'.</span></span> <span data-ttu-id="09f6a-124">Hvis sikkerhedsmargenen f.eks. angives til 1 dag, og en salgsordrelinje planlægges til levering d. 15. maj, beregner varedisponering den justerede leveringsdato som d. 14. maj.</span><span class="sxs-lookup"><span data-stu-id="09f6a-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="09f6a-125">Angiv '1' i feltet **Bestillingsmargen tilføjet til varens leveringstid**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-125">In the **Reorder margin added to item lead time** field, enter '1'.</span></span>
14. <span data-ttu-id="09f6a-126">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-126">Click **Save**.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="09f6a-127">Oprette et nyt produkt</span><span class="sxs-lookup"><span data-stu-id="09f6a-127">Create a new product</span></span>
1. <span data-ttu-id="09f6a-128">Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-128">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="09f6a-129">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-129">Click **New**.</span></span>
3. <span data-ttu-id="09f6a-130">Skriv en værdi i feltet **Produktnummer**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-130">In the **Product number** field, type a value.</span></span>
4. <span data-ttu-id="09f6a-131">Skriv en værdi i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-131">In the **Product name** field, type a value.</span></span>
5. <span data-ttu-id="09f6a-132">Klik på rullelisten i feltet **Varemodelgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="09f6a-132">In the **Item model group** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="09f6a-133">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="09f6a-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="09f6a-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="09f6a-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="09f6a-135">Klik på rullelisten i feltet **Varegruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="09f6a-135">In the **Item group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="09f6a-136">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="09f6a-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="09f6a-137">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="09f6a-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="09f6a-138">Klik på rullelisten i feltet **Lagringsdimensionsgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="09f6a-138">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="09f6a-139">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="09f6a-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="09f6a-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="09f6a-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="09f6a-141">Klik på rullelisten i feltet **Sporingsdimensionsgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="09f6a-141">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="09f6a-142">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="09f6a-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="09f6a-143">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="09f6a-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="09f6a-144">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-144">Click **OK**.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="09f6a-145">Konfigurer standardindstillinger for ordre</span><span class="sxs-lookup"><span data-stu-id="09f6a-145">Setup default order settings</span></span>
1. <span data-ttu-id="09f6a-146">Klik på **Plan** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-146">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="09f6a-147">Klik på **Standardindstillinger for ordre** under **Ordreindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-147">Under **Order settings**, click **Default order settings**.</span></span>
3. <span data-ttu-id="09f6a-148">Angiv det sted, der bruges som standard, når indkøbsordrer oprettes, i feltet **Standardsted** under **Indkøbsordre**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-148">Under **Purchase order**, in the **Default site** field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="09f6a-149">I feltet **Standardlagersted** skal du angive det sted, hvor varen opbevares.</span><span class="sxs-lookup"><span data-stu-id="09f6a-149">In the **Default warehouse** field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="09f6a-150">Vis eller skjul sektionen **Lager**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-150">Expand or collapse the **Inventory** section.</span></span>
6. <span data-ttu-id="09f6a-151">Skriv '10' i feltet **Multiplum**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-151">In the **Multiple** field, type '10'.</span></span>
7. <span data-ttu-id="09f6a-152">Skriv '10' i feltet **Min. ordreantal**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-152">In the **Min. order quantity** field, type '10'.</span></span>
8. <span data-ttu-id="09f6a-153">Skriv '100' i feltet **Maks. ordreantal**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-153">In the **Max. order quantity** field, type '100'.</span></span>
9. <span data-ttu-id="09f6a-154">Skriv '10' i feltet **Standardordreantal**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-154">In the **Standard order quantity**, type '10'.</span></span>
10. <span data-ttu-id="09f6a-155">Angiv et tal i feltet **Leveringstid for indkøb**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-155">In the **Purchase lead time** field, enter a number.</span></span>
11. <span data-ttu-id="09f6a-156">Markér eller fjern markeringen i afkrydsningsfeltet **Arbejdsdage**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-156">Select or clear the **Working days** check box.</span></span>
12. <span data-ttu-id="09f6a-157">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-157">Click **Save**.</span></span>
13. <span data-ttu-id="09f6a-158">I feltet **Standardordretype** skal du vælge 'Indkøbsordre'.</span><span class="sxs-lookup"><span data-stu-id="09f6a-158">In the **Default order type** field select 'Purchase order'.</span></span>
14. <span data-ttu-id="09f6a-159">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-159">Click **Save**.</span></span>
15. <span data-ttu-id="09f6a-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="09f6a-160">Close the page.</span></span> <span data-ttu-id="09f6a-161">Luk siden Standardindstillinger for ordre.</span><span class="sxs-lookup"><span data-stu-id="09f6a-161">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="09f6a-162">Føj en vare til en disponeringsgruppe</span><span class="sxs-lookup"><span data-stu-id="09f6a-162">Add an item to a coverage group</span></span>
1. <span data-ttu-id="09f6a-163">Vis eller skjul sektionen **Plan**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-163">Expand or collapse the **Plan** section.</span></span>
2. <span data-ttu-id="09f6a-164">Klik på rullelisten i feltet **Disponeringsgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="09f6a-164">In the **Coverage group** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="09f6a-165">Find den **Disponeringsgruppe**, du har oprettet, på listen.</span><span class="sxs-lookup"><span data-stu-id="09f6a-165">In the list, find the **Coverage group** you have created.</span></span>
4. <span data-ttu-id="09f6a-166">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="09f6a-166">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="09f6a-167">Opret varedisponeringsregler</span><span class="sxs-lookup"><span data-stu-id="09f6a-167">Create item coverage rules</span></span>
1. <span data-ttu-id="09f6a-168">Klik på **Plan** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-168">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="09f6a-169">Klik på **Varedisponering** under **Disponering**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-169">Under **Coverage**, click **Item coverage**.</span></span>
3. <span data-ttu-id="09f6a-170">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-170">Click **New**.</span></span>
4. <span data-ttu-id="09f6a-171">Klik på fanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-171">Click the **General** tab.</span></span>
5. <span data-ttu-id="09f6a-172">Markér feltet på overskriften **Tilsidesæt indstillinger for disponeringsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-172">Check the box on the header of **Override coverage group** settings.</span></span>
6. <span data-ttu-id="09f6a-173">Angiv '60' i feltet **Disponeringstidshorisont (dage)**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-173">In the **Coverage time fence (days)** field, enter '60'.</span></span> <span data-ttu-id="09f6a-174">Selvom varerne i disponeringsgruppen Krav er planlagt 90 dage frem, bliver dette element planlagt 60 dage frem.</span><span class="sxs-lookup"><span data-stu-id="09f6a-174">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="09f6a-175">Angiv '2' i feltet **Negative dage**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-175">In the **Negative days** field, enter '2'.</span></span>
8. <span data-ttu-id="09f6a-176">Angiv '2' i feltet **Positive dage**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-176">In the **Positive days** field, enter '2'.</span></span>
9. <span data-ttu-id="09f6a-177">Klik på fanen **Leveringstid**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-177">Click the **Lead time** tab.</span></span>
10. <span data-ttu-id="09f6a-178">Markér feltet på overskriften **Indkøb**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-178">Check the box on the header of **Purchase**.</span></span>
11. <span data-ttu-id="09f6a-179">Angiv '5' i feltet **Indkøbstid**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-179">In the **Purchase time** field, enter '5'.</span></span>
12. <span data-ttu-id="09f6a-180">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="09f6a-180">Click **Save**.</span></span>

