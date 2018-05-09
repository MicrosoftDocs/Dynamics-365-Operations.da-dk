--- 
title: "Definere dækningsregler for varer"
description: Det demodatafirma, der bruges til at oprette denne procedure, er USMF.
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3205fe6a10ce714073334c7ccd25acb755e0aebf
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="519e5-103">Definere dækningsregler for varer</span><span class="sxs-lookup"><span data-stu-id="519e5-103">Define coverage rules for items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="519e5-104">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="519e5-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="519e5-105">Denne procedure viser, hvordan du opretter disponeringsregler og tilsidesætter disponeringsindstillinger for et bestemt element.</span><span class="sxs-lookup"><span data-stu-id="519e5-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="519e5-106">Det viser også, hvordan du angiver standardindstillinger for lager.</span><span class="sxs-lookup"><span data-stu-id="519e5-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="519e5-107">Oprette en disponeringsgruppe</span><span class="sxs-lookup"><span data-stu-id="519e5-107">Create a coverage group</span></span>
1. <span data-ttu-id="519e5-108">Gå til Disponeringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="519e5-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="519e5-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="519e5-109">Click New.</span></span>
3. <span data-ttu-id="519e5-110">Skriv en værdi i feltet Dækningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="519e5-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="519e5-111">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="519e5-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="519e5-112">Skriv en værdi i feltet Kalender.</span><span class="sxs-lookup"><span data-stu-id="519e5-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="519e5-113">Vælg den kalender, som varedisponering bruger til at oprette genopfyldningsforslag for varer i denne gruppe.</span><span class="sxs-lookup"><span data-stu-id="519e5-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="519e5-114">Vælg en indstilling i feltet Disponeringskode.</span><span class="sxs-lookup"><span data-stu-id="519e5-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="519e5-115">Vælg Krav til denne procedure.</span><span class="sxs-lookup"><span data-stu-id="519e5-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="519e5-116">Angiv "90" i feltet Disponeringstidshorisont (dage).</span><span class="sxs-lookup"><span data-stu-id="519e5-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="519e5-117">For elementer i denne gruppe vil varedisponering oprette genopfyldningsforslag for op til 90 dage ud i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="519e5-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="519e5-118">Angiv "1" i feltet Negative dage.</span><span class="sxs-lookup"><span data-stu-id="519e5-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="519e5-119">Angiv "1" i feltet Positive dage.</span><span class="sxs-lookup"><span data-stu-id="519e5-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="519e5-120">Vis eller skjul sektionen Andet.</span><span class="sxs-lookup"><span data-stu-id="519e5-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="519e5-121">Angiv "1" i feltet Modtagelsesmargen lagt til behovsdato</span><span class="sxs-lookup"><span data-stu-id="519e5-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="519e5-122">Hvis modtagelsesmargenen f.eks. angives til 1 dag, og en indkøbsordrelinje planlægges til tilgang d. 15. maj, beregner varedisponering den justerede modtagelsesdato som d. 16. maj.</span><span class="sxs-lookup"><span data-stu-id="519e5-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="519e5-123">Angiv "1" i feltet Afgangsmargen trukket fra behovsdato.</span><span class="sxs-lookup"><span data-stu-id="519e5-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="519e5-124">Hvis sikkerhedsmargenen f.eks. angives til 1 dag, og en salgsordrelinje planlægges til levering d. 15. maj, beregner varedisponering den justerede leveringsdato som d. 14. maj.</span><span class="sxs-lookup"><span data-stu-id="519e5-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="519e5-125">Angiv "1" i feltet Bestillingsmargen tilføjet til varens leveringstid.</span><span class="sxs-lookup"><span data-stu-id="519e5-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="519e5-126">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="519e5-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="519e5-127">Opret et nyt produkt</span><span class="sxs-lookup"><span data-stu-id="519e5-127">Create a new product</span></span>
1. <span data-ttu-id="519e5-128">Gå til Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="519e5-128">Go to Released products.</span></span>
2. <span data-ttu-id="519e5-129">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="519e5-129">Click New.</span></span>
3. <span data-ttu-id="519e5-130">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="519e5-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="519e5-131">Angiv en værdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="519e5-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="519e5-132">Klik på rullelisten i feltet Varemodelgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="519e5-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="519e5-133">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="519e5-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="519e5-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="519e5-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="519e5-135">Klik på rullelisten i feltet Varegruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="519e5-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="519e5-136">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="519e5-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="519e5-137">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="519e5-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="519e5-138">Klik på rullelisten i feltet Lagringsdimensionsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="519e5-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="519e5-139">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="519e5-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="519e5-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="519e5-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="519e5-141">Klik på rullelisten i feltet Sporingsdimensionsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="519e5-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="519e5-142">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="519e5-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="519e5-143">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="519e5-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="519e5-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="519e5-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="519e5-145">Konfigurer standardindstillinger for ordre</span><span class="sxs-lookup"><span data-stu-id="519e5-145">Setup default order settings</span></span>
1. <span data-ttu-id="519e5-146">Klik på Plan i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="519e5-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="519e5-147">Klik på Standardindstillinger for ordre.</span><span class="sxs-lookup"><span data-stu-id="519e5-147">Click Default order settings.</span></span>
3. <span data-ttu-id="519e5-148">Angiv det sted, der bruges som standard, når indkøbsordrer oprettes, i feltet Købssted.</span><span class="sxs-lookup"><span data-stu-id="519e5-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="519e5-149">I feltet Sted for lager skal du angive det sted, hvor elementet opbevares.</span><span class="sxs-lookup"><span data-stu-id="519e5-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="519e5-150">Vis eller skjul sektionen Lager.</span><span class="sxs-lookup"><span data-stu-id="519e5-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="519e5-151">Angiv Multiplum til "10".</span><span class="sxs-lookup"><span data-stu-id="519e5-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="519e5-152">Angiv Min.</span><span class="sxs-lookup"><span data-stu-id="519e5-152">Set Min.</span></span> <span data-ttu-id="519e5-153">ordreantal til "10".</span><span class="sxs-lookup"><span data-stu-id="519e5-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="519e5-154">Angiv Maks.</span><span class="sxs-lookup"><span data-stu-id="519e5-154">Set Max.</span></span> <span data-ttu-id="519e5-155">ordreantal til "100".</span><span class="sxs-lookup"><span data-stu-id="519e5-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="519e5-156">Angiv Standardordreantal til "10".</span><span class="sxs-lookup"><span data-stu-id="519e5-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="519e5-157">Angiv et tal i feltet Leveringstid for indkøb.</span><span class="sxs-lookup"><span data-stu-id="519e5-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="519e5-158">Markér eller fjern markeringen i afkrydsningsfeltet Arbejdsdage.</span><span class="sxs-lookup"><span data-stu-id="519e5-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="519e5-159">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="519e5-159">Click Save.</span></span>
13. <span data-ttu-id="519e5-160">I feltet Standardordretype skal du vælge "Indkøbsordre".</span><span class="sxs-lookup"><span data-stu-id="519e5-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="519e5-161">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="519e5-161">Click Save.</span></span>
15. <span data-ttu-id="519e5-162">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="519e5-162">Close the page.</span></span>
    * <span data-ttu-id="519e5-163">Luk siden Standardindstillinger for ordre.</span><span class="sxs-lookup"><span data-stu-id="519e5-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="519e5-164">Føj en vare til en disponeringsgruppe</span><span class="sxs-lookup"><span data-stu-id="519e5-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="519e5-165">Vis eller skjul sektionen Plan.</span><span class="sxs-lookup"><span data-stu-id="519e5-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="519e5-166">Klik på rullelisten i feltet Dækningsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="519e5-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="519e5-167">Find den disponeringsgruppe, du har oprettet, på listen.</span><span class="sxs-lookup"><span data-stu-id="519e5-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="519e5-168">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="519e5-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="519e5-169">Opret varedisponeringsregler</span><span class="sxs-lookup"><span data-stu-id="519e5-169">Create item coverage rules</span></span>
1. <span data-ttu-id="519e5-170">Klik på Plan i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="519e5-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="519e5-171">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="519e5-171">Click Item coverage.</span></span>
3. <span data-ttu-id="519e5-172">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="519e5-172">Click New.</span></span>
4. <span data-ttu-id="519e5-173">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="519e5-173">Click the General tab.</span></span>
5. <span data-ttu-id="519e5-174">Markér feltet på overskriften Tilsidesæt indstillinger for disponeringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="519e5-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="519e5-175">Angiv "60" i feltet Disponeringstidshorisont (dage).</span><span class="sxs-lookup"><span data-stu-id="519e5-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="519e5-176">Selvom varerne i disponeringsgruppen Krav er planlagt 90 dage frem, bliver dette element planlagt 60 dage frem.</span><span class="sxs-lookup"><span data-stu-id="519e5-176">Although items in coverage group Requirement are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="519e5-177">Angiv "2" i feltet Negative dage.</span><span class="sxs-lookup"><span data-stu-id="519e5-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="519e5-178">Angiv "2" i feltet Positive dage.</span><span class="sxs-lookup"><span data-stu-id="519e5-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="519e5-179">Klik på fanen Leveringstid.</span><span class="sxs-lookup"><span data-stu-id="519e5-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="519e5-180">Markér feltet på overskriften overskriften Indkøb.</span><span class="sxs-lookup"><span data-stu-id="519e5-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="519e5-181">Angiv "5" i feltet Indkøbstid.</span><span class="sxs-lookup"><span data-stu-id="519e5-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="519e5-182">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="519e5-182">Click Save.</span></span>


