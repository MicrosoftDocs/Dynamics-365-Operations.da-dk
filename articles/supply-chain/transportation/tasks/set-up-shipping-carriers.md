---
title: Konfigurere fragtmænd
description: Denne procedure beskriver, hvordan du kan konfigurere en fragtmand og definere detaljer som tjeneste, forsendelsestilstand, transporttilbud, transportbegrænsninger og forsendelsessats.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "314480"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="d3c4c-103">Konfigurere fragtmænd</span><span class="sxs-lookup"><span data-stu-id="d3c4c-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3c4c-104">Denne procedure beskriver, hvordan du kan konfigurere en fragtmand og definere detaljer som tjeneste, forsendelsestilstand, transporttilbud, transportbegrænsninger og forsendelsessats.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="d3c4c-105">Derefter kan en transportkoordinator tildele en fragtmand til en indgående eller udgående last.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="d3c4c-106">Opret en ny fragtmand</span><span class="sxs-lookup"><span data-stu-id="d3c4c-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="d3c4c-107">Gå til Transportstyring > Opsætning > Fragtmænd > Fragtmænd.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="d3c4c-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-108">Click New.</span></span>
3. <span data-ttu-id="d3c4c-109">Skriv en værdi i feltet Fragtmand.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="d3c4c-110">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d3c4c-111">Klik på rullelisten i feltet Tilstand for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d3c4c-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="d3c4c-113">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="d3c4c-114">Udfyld generelle oplysninger om fragtmanden</span><span class="sxs-lookup"><span data-stu-id="d3c4c-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="d3c4c-115">Slå udvidelsen af sektionen Oversigt til/fra.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="d3c4c-116">Markér eller fjern markeringen i afkrydsningsfeltet Aktivér fragtmand.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="d3c4c-117">Klik på rullelisten i feltet Kreditor for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d3c4c-118">Vælg kreditorkontoen, som fragtmanden skal tildeles.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="d3c4c-119">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d3c4c-120">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d3c4c-121">Vælg en indstilling i feltet Transporttilbud.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="d3c4c-122">Vælg Manuelt for at bruge siden Transporttilbud, eller vælg EDI for opdatere tilbuddet ved hjælp af EDI (Electronic Data Interchange).</span><span class="sxs-lookup"><span data-stu-id="d3c4c-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="d3c4c-123">Markér eller fjern markeringen i afkrydsningsfeltet Aktivér fragtmandssatser.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="d3c4c-124">Opret de nødvendige tjenester for fragtmanden</span><span class="sxs-lookup"><span data-stu-id="d3c4c-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="d3c4c-125">Slå udvidelsen af sektionen afsnittet Tjenester til/fra.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="d3c4c-126">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-126">Click New.</span></span>
3. <span data-ttu-id="d3c4c-127">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d3c4c-128">Skriv en værdi i feltet Fragttjeneste.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="d3c4c-129">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="d3c4c-130">Klik på rullelisten i feltet Transportmetode for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d3c4c-131">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d3c4c-132">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="d3c4c-133">Konfigurer adressen for fragtmanden (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="d3c4c-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="d3c4c-134">Slå udvidelsen af sektionen Adresser til/fra.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="d3c4c-135">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-135">Click New.</span></span>
3. <span data-ttu-id="d3c4c-136">Skriv en værdi i feltet Navn eller beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="d3c4c-137">Klik på rullelisten i feltet Land/område for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d3c4c-138">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d3c4c-139">Klik på rullelisten i feltet Postnummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d3c4c-140">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d3c4c-141">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d3c4c-142">Skriv en værdi i feltet Gade.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="d3c4c-143">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="d3c4c-144">Konfigurer vurderingsprofil for fragtmanden</span><span class="sxs-lookup"><span data-stu-id="d3c4c-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="d3c4c-145">Slå udvidelsen af sektionen Vurderingsprofiler til/fra.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="d3c4c-146">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-146">Click New.</span></span>
3. <span data-ttu-id="d3c4c-147">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d3c4c-148">Skriv en værdi i feltet Vurderingsprofil.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="d3c4c-149">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="d3c4c-150">Klik på rullelisten i feltet Sted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d3c4c-151">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d3c4c-152">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d3c4c-153">Klik på rullelisten i feltet Lagersted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="d3c4c-154">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="d3c4c-155">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="d3c4c-156">Klik på rullelisten i feltet Satsprogram for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d3c4c-157">Vælg det Satsprogram, der er i overensstemmelse med den kontrakt, du har lavet med fragtmanden.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="d3c4c-158">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="d3c4c-159">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="d3c4c-160">Klik på rullelisten i feltet Satsmaster for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="d3c4c-161">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="d3c4c-162">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="d3c4c-163">Klik på rullelisten i feltet Program til transittid for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="d3c4c-164">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="d3c4c-165">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d3c4c-165">Click Save.</span></span>

