---
title: Konfigurere fragtmænd
description: I dette emne beskrives, hvordan du kan konfigurere en fragtmand og definere detaljer som tjeneste, forsendelsestilstand, transporttilbud, transportbegrænsninger og forsendelsessats.
author: ShylaThompson
manager: AnnBe
ms.date: 07/19/2019
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
ms.openlocfilehash: 7a43a99e10b915f1265be14f2442069dae3a22e5
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867021"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="0ed80-103">Konfigurere fragtmænd</span><span class="sxs-lookup"><span data-stu-id="0ed80-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0ed80-104">I dette emne beskrives, hvordan du kan konfigurere en fragtmand og definere detaljer som tjeneste, forsendelsestilstand, transporttilbud, transportbegrænsninger og forsendelsessats.</span><span class="sxs-lookup"><span data-stu-id="0ed80-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="0ed80-105">Derefter kan en transportkoordinator tildele en fragtmand til en indgående eller udgående last.</span><span class="sxs-lookup"><span data-stu-id="0ed80-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="0ed80-106">Opret en ny fragtmand</span><span class="sxs-lookup"><span data-stu-id="0ed80-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="0ed80-107">Gå til **Navigationsrude > Moduler > Transportstyring > Opsætning > Fragtmænd > Fragtmænd**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="0ed80-108">Vælg **Ny** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0ed80-108">Select **New** in the Action pane.</span></span>
3. <span data-ttu-id="0ed80-109">Skriv en værdi i feltet **Fragtmand**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="0ed80-110">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="0ed80-111">Vælg en indstilling på rullelisten i feltet **Måde**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="0ed80-112">Udfyld generelle oplysninger om fragtmanden</span><span class="sxs-lookup"><span data-stu-id="0ed80-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="0ed80-113">Slå udvidelsen af sektionen **Oversigt** til/fra.</span><span class="sxs-lookup"><span data-stu-id="0ed80-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="0ed80-114">Markér eller fjern markeringen i afkrydsningsfeltet **Aktivér fragtmand**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="0ed80-115">Vælg en indstilling på rullelisten i feltet **Kreditorkonto**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="0ed80-116">Vælg kreditorkontoen, som fragtmanden skal tildeles.</span><span class="sxs-lookup"><span data-stu-id="0ed80-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="0ed80-117">Vælg en indstilling i feltet **Transporttilbudstype**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="0ed80-118">Vælg **Manuelt** for at bruge siden Transporttilbud, eller vælg **EDI** for opdatere tilbuddet ved hjælp af EDI (Electronic Data Interchange).</span><span class="sxs-lookup"><span data-stu-id="0ed80-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="0ed80-119">Markér eller fjern markeringen i afkrydsningsfeltet **Aktivér fragtmandssatser**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="0ed80-120">Opret de nødvendige tjenester for fragtmanden</span><span class="sxs-lookup"><span data-stu-id="0ed80-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="0ed80-121">Slå udvidelsen af sektionen afsnittet **Tjenester** til/fra.</span><span class="sxs-lookup"><span data-stu-id="0ed80-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="0ed80-122">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-122">Select **New**.</span></span>
3. <span data-ttu-id="0ed80-123">Skriv en værdi i feltet **Fragttjeneste**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="0ed80-124">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="0ed80-125">Vælg en indstilling på rullelisten i feltet **Transportmetode**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="0ed80-126">Konfigurer adressen for fragtmanden (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="0ed80-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="0ed80-127">Slå udvidelsen af sektionen **Adresser** til/fra.</span><span class="sxs-lookup"><span data-stu-id="0ed80-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="0ed80-128">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-128">Select **New**.</span></span>
3. <span data-ttu-id="0ed80-129">Skriv en værdi i feltet **Navn eller beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="0ed80-130">Vælg en indstilling på rullelisten i feltet **Land/område**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="0ed80-131">Vælg en indstilling på rullelisten i feltet **Postnummer**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="0ed80-132">Skriv en værdi i feltet **Gade**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="0ed80-133">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="0ed80-134">Konfigurer vurderingsprofil for fragtmanden</span><span class="sxs-lookup"><span data-stu-id="0ed80-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="0ed80-135">Slå udvidelsen af sektionen **Vurderingsprofiler** til/fra.</span><span class="sxs-lookup"><span data-stu-id="0ed80-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="0ed80-136">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-136">Select **New**.</span></span>
3. <span data-ttu-id="0ed80-137">Skriv en værdi i feltet **Vurderingsprofil**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="0ed80-138">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="0ed80-139">Vælg en indstilling på rullelisten i feltet **Sted**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="0ed80-140">Vælg en indstilling på rullelisten i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="0ed80-141">Vælg en indstilling på rullelisten i feltet **Satsprogram**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="0ed80-142">Vælg det Satsprogram, der er i overensstemmelse med den kontrakt, du har lavet med fragtmanden.</span><span class="sxs-lookup"><span data-stu-id="0ed80-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="0ed80-143">Vælg en indstilling på rullelisten i feltet **Satsmaster**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="0ed80-144">Vælg en indstilling på rullelisten i feltet **Program til transittid**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="0ed80-145">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0ed80-145">Select **Save**.</span></span>

