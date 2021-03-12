---
title: Foretage fejlfinding af pluk og pakning
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du plukker og pakker i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2cce1038ed393fc8a7bb489a37fc0921b0ac755e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993923"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="a16ba-103">Foretage fejlfinding af pluk og pakning</span><span class="sxs-lookup"><span data-stu-id="a16ba-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a16ba-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du plukker og pakker i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a16ba-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="a16ba-105">Jeg får vist følgende fejlmeddelelse: "Dimensionslokation kan ikke være tom, hvis der er angivet dimensionsserienummer".</span><span class="sxs-lookup"><span data-stu-id="a16ba-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a16ba-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="a16ba-106">Issue description</span></span>

<span data-ttu-id="a16ba-107">Du får vist denne fejlmeddelelse, hvis du opretter en flytteordre for en serievare ved hjælp af et lagersted, der er aktiveret til avanceret lokationsstyring (WMS), og du derefter forsøger at bekræfte forsendelsen, efter at arbejdet er fuldført.</span><span class="sxs-lookup"><span data-stu-id="a16ba-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a16ba-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="a16ba-108">Issue resolution</span></span>

<span data-ttu-id="a16ba-109">Feltet **Standardtilgangslokation** er tomt for et transitlagersted i "fra"-lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="a16ba-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="a16ba-110">Du kan løse dette problem ved at angive en standardtilgangslokation på transitlagerstedet.</span><span class="sxs-lookup"><span data-stu-id="a16ba-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="a16ba-111">Kontrollér, at denne lokation er id-styret.</span><span class="sxs-lookup"><span data-stu-id="a16ba-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="a16ba-112">Jeg får vist følgende fejlmeddelelse: "Ugyldigt id".</span><span class="sxs-lookup"><span data-stu-id="a16ba-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a16ba-113">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="a16ba-113">Issue description</span></span>

<span data-ttu-id="a16ba-114">Du får vist denne fejlmeddelelse i lagerstedsappen, når du scanner et nummerplade-id.</span><span class="sxs-lookup"><span data-stu-id="a16ba-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a16ba-115">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="a16ba-115">Issue resolution</span></span>

<span data-ttu-id="a16ba-116">Kontrollér, at nummerpladens id findes i id-tabellen, og at varerne og antallet på id'et er tilgængelige (med andre ord blokeres de ikke).</span><span class="sxs-lookup"><span data-stu-id="a16ba-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="a16ba-117">Jeg får vist følgende fejlmeddelelse: "Feltets lastvægt (=-%1) kan kun indeholde positive tal.</span><span class="sxs-lookup"><span data-stu-id="a16ba-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="a16ba-118">Opdateringen er annulleret".</span><span class="sxs-lookup"><span data-stu-id="a16ba-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a16ba-119">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="a16ba-119">Issue description</span></span>

<span data-ttu-id="a16ba-120">Du får vist denne fejlmeddelelse, hvis der er åbent arbejde, når du behandler arbejde fra pakkelokationer til midlertidige lokationer, eller fra midlertidige lokationer til dock-lokationer.</span><span class="sxs-lookup"><span data-stu-id="a16ba-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a16ba-121">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="a16ba-121">Issue resolution</span></span>

<span data-ttu-id="a16ba-122">Du kan løse dette problem ved at gå til **Systemadministration \> Periodiske opgaver \> Database \> Konsistenskontrol** og køre processen til **Konsistenskontrol af lagersteds lastvægt**.</span><span class="sxs-lookup"><span data-stu-id="a16ba-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="a16ba-123">Jeg får vist følgende fejlmeddelelse: "Antallet er ikke gyldigt for enheden %1".</span><span class="sxs-lookup"><span data-stu-id="a16ba-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a16ba-124">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="a16ba-124">Issue description</span></span>

<span data-ttu-id="a16ba-125">Du får vist denne fejlmeddelelse, når du forsøger at udføre et *opdelt pluk* på tværs af flere batches.</span><span class="sxs-lookup"><span data-stu-id="a16ba-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a16ba-126">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="a16ba-126">Issue resolution</span></span>

<span data-ttu-id="a16ba-127">Lagermedarbejderen skal bruge *Kort pluk* som proces i lagerstedsappen.</span><span class="sxs-lookup"><span data-stu-id="a16ba-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="a16ba-128">Hvis du forsøger at plukke flere batcher fra samme lokation, kan du også bruge indstillingen **Fuld** i lagerstedsappen.</span><span class="sxs-lookup"><span data-stu-id="a16ba-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="a16ba-129">Jeg kan ikke flytte lager til en lokation, der er id-kontrolleret.</span><span class="sxs-lookup"><span data-stu-id="a16ba-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a16ba-130">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="a16ba-130">Issue description</span></span>

<span data-ttu-id="a16ba-131">Du kan ikke reducere plukantal på en last.</span><span class="sxs-lookup"><span data-stu-id="a16ba-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a16ba-132">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="a16ba-132">Issue resolution</span></span>

<span data-ttu-id="a16ba-133">I tidligere versioner kan du ikke reducere plukantal på en last.</span><span class="sxs-lookup"><span data-stu-id="a16ba-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="a16ba-134">Du kan dog nu vælge at flytte et pluk til en id-kontrolleret lokation.</span><span class="sxs-lookup"><span data-stu-id="a16ba-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="a16ba-135">Du skal angive både en **Lokation**-værdi og en **ID**-værdi for lastlinjen på siden **Reducer plukket antal**.</span><span class="sxs-lookup"><span data-stu-id="a16ba-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="a16ba-136">Kan jeg udskrive en følgeseddel eller pakkeindhold efter lagersted?</span><span class="sxs-lookup"><span data-stu-id="a16ba-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="a16ba-137">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="a16ba-137">Issue description</span></span>

<span data-ttu-id="a16ba-138">Du vil udskrive en følgeseddel eller pakkeindhold efter lagersted eller sted på siden **Opdater skabelonlinje for arbejdsrevision**.</span><span class="sxs-lookup"><span data-stu-id="a16ba-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a16ba-139">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="a16ba-139">Issue resolution</span></span>

<span data-ttu-id="a16ba-140">Når du udskriver et dokument ved hjælp af indstillinger for udskriftsstyring, skal du begrænse omfanget (lokation/lagersted) via udskriftsstyring i stedet for at vælge **Rediger udskriftsindstillinger** på siden **Opdater skabelonlinje for arbejdsrevision**.</span><span class="sxs-lookup"><span data-stu-id="a16ba-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="a16ba-141">Jeg kan ikke annullere en følgeseddel, når den er bogført fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a16ba-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a16ba-142">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="a16ba-142">Issue description</span></span>

<span data-ttu-id="a16ba-143">Når pluk- og forsendelsesprocesser er aktiveret for WMS, kan du ikke annullere en følgeseddel, når den er bogført fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a16ba-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a16ba-144">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="a16ba-144">Issue resolution</span></span>

<span data-ttu-id="a16ba-145">Hvis du vil rette bogførte følgesedler for varer, der er aktiveret for WMS, skal bogføringen ske fra lasten, ikke fra ordren.</span><span class="sxs-lookup"><span data-stu-id="a16ba-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="a16ba-146">Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="a16ba-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="a16ba-147">Generelt kan en salgsordre, der er plukket og afsendt via lokationsstyringsprocesser, få opdateret følgeseddel fra lasen eller forsendelsen og selve salgsordredokumentet.</span><span class="sxs-lookup"><span data-stu-id="a16ba-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="a16ba-148">Men hvis du opdaterer følgeseddel på salgsordren fra salgsordredokumentet, kan tilbageførslen af følgesedlen stadig ikke udføres fra last- eller salgsordren.</span><span class="sxs-lookup"><span data-stu-id="a16ba-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="a16ba-149">Det anbefales derfor, at du bruger bogføring af følgesedlen fra lasten.</span><span class="sxs-lookup"><span data-stu-id="a16ba-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="a16ba-150">I dette tilfælde vil tilbageførsel, der foretages fra lasten, blive aktiveret.</span><span class="sxs-lookup"><span data-stu-id="a16ba-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="a16ba-151">Jeg får følgende fejlmeddelelse: "Der kan ikke findes nok arbejde for klyngen".</span><span class="sxs-lookup"><span data-stu-id="a16ba-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a16ba-152">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="a16ba-152">Issue description</span></span>

<span data-ttu-id="a16ba-153">Når du bruger *Systemstyret klyngepluk* som proces, hvis du konfigurerer en klyngeprofil, hvor der f.eks. kan plukkes 10 placeringer, fungerer processen som planlagt, når der er nok arbejde til at plukke til 10 placeringer.</span><span class="sxs-lookup"><span data-stu-id="a16ba-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="a16ba-154">Men hvis der kun er otte placeringer, der kan plukkes, får du vist denne fejlmeddelelse, fordi der ikke er nok arbejde til én klynge.</span><span class="sxs-lookup"><span data-stu-id="a16ba-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a16ba-155">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="a16ba-155">Issue resolution</span></span>

<span data-ttu-id="a16ba-156">Du kan løse dette problem ved at redigere klyngeprofilen og angive indstillingen **Aktivér placeringer** til *Nej*.</span><span class="sxs-lookup"><span data-stu-id="a16ba-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>
