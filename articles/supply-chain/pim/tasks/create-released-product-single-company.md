---
title: Oprette et frigivet produkt for et enkelt firma
description: Denne fremgangsmåde beskriver, hvordan du opretter et enkelt frigivet produkt inden for rammerne af en enkelt juridisk enhed.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dfe93a3084bb8c7f2b181b35d393b8afdabb9f4b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258821"
---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="73ac9-103">Oprette et frigivet produkt for et enkelt firma</span><span class="sxs-lookup"><span data-stu-id="73ac9-103">Create a released product for a single company</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="73ac9-104">Denne fremgangsmåde beskriver, hvordan du opretter et enkelt frigivet produkt inden for rammerne af en enkelt juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="73ac9-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="73ac9-105">Når et frigivet produkt er oprettet, er det umiddelbart kun tilgængelig i denne enhed.</span><span class="sxs-lookup"><span data-stu-id="73ac9-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="73ac9-106">Du kan gennemgå denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="73ac9-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="73ac9-107">Denne opgave udføres normalt af en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="73ac9-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="73ac9-108">Opret et frigivet produkt</span><span class="sxs-lookup"><span data-stu-id="73ac9-108">Create a released product</span></span>
1. <span data-ttu-id="73ac9-109">Gå til Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="73ac9-109">Go to Released products.</span></span>
2. <span data-ttu-id="73ac9-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="73ac9-110">Click New.</span></span>
3. <span data-ttu-id="73ac9-111">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="73ac9-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="73ac9-112">Hvis der ikke automatisk er angivet et produktnummer i feltet Produktnummer, skal du skrive et entydigt produktnummer.</span><span class="sxs-lookup"><span data-stu-id="73ac9-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="73ac9-113">Dette trin er kun påkrævet, hvis der ikke er oprettet nogen nummerserie for produktnumre.</span><span class="sxs-lookup"><span data-stu-id="73ac9-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="73ac9-114">Angiv en værdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="73ac9-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="73ac9-115">Produktets navn angives som standard til søgenavnet.</span><span class="sxs-lookup"><span data-stu-id="73ac9-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="73ac9-116">Hvis det er nødvendigt, kan du vælge for at ændre søgenavnet.</span><span class="sxs-lookup"><span data-stu-id="73ac9-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="73ac9-117">Klik på rullelisten i feltet Varemodelgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="73ac9-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="73ac9-118">Varemodelgrupper indeholder indstillinger, der bestemmer, hvordan varerne kontrolleres og håndteres i forbindelse med varetilgang og vareafgang.</span><span class="sxs-lookup"><span data-stu-id="73ac9-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="73ac9-119">Indstillingerne bestemmer også beregningen af vareforbrug.</span><span class="sxs-lookup"><span data-stu-id="73ac9-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="73ac9-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="73ac9-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="73ac9-122">Klik på rullelisten i feltet Varegruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="73ac9-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="73ac9-123">Varegrupper bruges til at styre lagerbeholdningen, fordi lagervarerne kan deles op i grupper med fælles karakteristiske træk.</span><span class="sxs-lookup"><span data-stu-id="73ac9-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="73ac9-124">Hvis du f.eks. vil styre, hvordan oplysninger bogføres på hovedkonti, kan du oprette en række forskellige varegrupper, der er tilknyttet bestemte hovedkonti.</span><span class="sxs-lookup"><span data-stu-id="73ac9-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="73ac9-125">På denne måde kan du spore lagerværdien af varer på forskellige stadier.</span><span class="sxs-lookup"><span data-stu-id="73ac9-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="73ac9-126">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="73ac9-127">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="73ac9-128">Klik på rullelisten i feltet Lagringsdimensionsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="73ac9-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="73ac9-129">Lagringsdimensionerne gør det lettere at styre, hvordan varer opbevares og plukkes på lageret.</span><span class="sxs-lookup"><span data-stu-id="73ac9-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="73ac9-130">For eksempel kan en lagringsdimension være Sted og Lagersted.</span><span class="sxs-lookup"><span data-stu-id="73ac9-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="73ac9-131">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="73ac9-132">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="73ac9-133">Klik på rullelisten i feltet Sporingsdimensionsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="73ac9-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="73ac9-134">Sporingsdimensionsgruppen bestemmer, hvilke sporingsdimensioner du kan føje til et produkt.</span><span class="sxs-lookup"><span data-stu-id="73ac9-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="73ac9-135">For eksempel bruges batchnummeret og serienummeret til at spore lagervarer.</span><span class="sxs-lookup"><span data-stu-id="73ac9-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="73ac9-136">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="73ac9-137">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="73ac9-138">Klik på rullelisten i feltet Lagerenhed for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="73ac9-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="73ac9-139">Lagerenheden bestemmer, hvordan produktet skal kvantificeres, når det opbevares på lager.</span><span class="sxs-lookup"><span data-stu-id="73ac9-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="73ac9-140">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="73ac9-141">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="73ac9-142">Klik på rullelisten i feltet Købsenhed for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="73ac9-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="73ac9-143">Købsenheden bestemmer, hvordan produktet kvantificeres, når det er købt hos en kreditor.</span><span class="sxs-lookup"><span data-stu-id="73ac9-143">The purchase unit determines how the product is quantified when it's purchased from a vendor.</span></span>  
21. <span data-ttu-id="73ac9-144">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="73ac9-145">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="73ac9-146">Klik på rullelisten i feltet Salgsenhed for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="73ac9-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="73ac9-147">Salgsenheden bestemmer, hvordan produktet kvantificeres, når det sælges til en debitor.</span><span class="sxs-lookup"><span data-stu-id="73ac9-147">The sales unit determines how the product is quantified when it's sold to a customer.</span></span>  
24. <span data-ttu-id="73ac9-148">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="73ac9-149">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="73ac9-150">Klik på rullelisten i feltet Styklisteenhed for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="73ac9-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="73ac9-151">Styklisteenheden bestemmer, hvordan produktet kvantificeres, når det inkluderes på en stykliste.</span><span class="sxs-lookup"><span data-stu-id="73ac9-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="73ac9-152">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="73ac9-153">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="73ac9-154">Klik på rullelisten i feltet Varemomsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="73ac9-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="73ac9-155">Varemomsgruppen i gruppen Salgsskat bestemmer, hvordan momsen beregnes for hver vare.</span><span class="sxs-lookup"><span data-stu-id="73ac9-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="73ac9-156">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="73ac9-157">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="73ac9-158">Klik på rullelisten i feltet Varemomsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="73ac9-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="73ac9-159">Varemomsgruppen i gruppen Indkøbsskat bestemmer, hvordan købsmomsen beregnes for hver vare.</span><span class="sxs-lookup"><span data-stu-id="73ac9-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="73ac9-160">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="73ac9-161">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="73ac9-162">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="73ac9-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="73ac9-163">Tilføj produktegenskaber</span><span class="sxs-lookup"><span data-stu-id="73ac9-163">Add product characteristics</span></span>
1. <span data-ttu-id="73ac9-164">Vis eller skjul sektionen Administrer lager.</span><span class="sxs-lookup"><span data-stu-id="73ac9-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="73ac9-165">Angiv et tal i feltet Nettovægt.</span><span class="sxs-lookup"><span data-stu-id="73ac9-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="73ac9-166">Angiv et tal i feltet Taravægt.</span><span class="sxs-lookup"><span data-stu-id="73ac9-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="73ac9-167">Angiv et tal i feltet Bruttodybde.</span><span class="sxs-lookup"><span data-stu-id="73ac9-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="73ac9-168">Angiv et tal i feltet Bruttobredde.</span><span class="sxs-lookup"><span data-stu-id="73ac9-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="73ac9-169">Angiv et tal i feltet Bruttohøjde.</span><span class="sxs-lookup"><span data-stu-id="73ac9-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="73ac9-170">Angiv et tal i feltet Volumen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="73ac9-171">Tilføj økonomiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="73ac9-171">Add financial dimensions</span></span>
1. <span data-ttu-id="73ac9-172">Udvid eller skjul sektionen Økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="73ac9-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="73ac9-173">Klik på rullelisten i feltet BusinessUnit for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="73ac9-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="73ac9-174">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="73ac9-175">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="73ac9-176">Klik på rullelisten i feltet CostCenter for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="73ac9-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="73ac9-177">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="73ac9-178">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="73ac9-179">Klik på rullelisten i feltet Afdeling for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="73ac9-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="73ac9-180">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="73ac9-181">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="73ac9-182">Klik på rullelisten i feltet Varegruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="73ac9-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="73ac9-183">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="73ac9-184">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="73ac9-184">In the list, click the link in the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]