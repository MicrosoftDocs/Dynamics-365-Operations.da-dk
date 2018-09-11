--- 
title: "Konfigurere en arbejdsskabelon for indkøbsordrer"
description: "Denne procedure fokuserer på konfiguration af en simpel arbejdsskabelon, der skal bruges, når varer, du har modtaget, lægges på lager."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 4c388a8ed6a852a92caa3a1eff2d0e8017694bcd
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="e1053-103">Konfigurere en arbejdsskabelon for indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="e1053-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e1053-104">Denne procedure fokuserer på konfiguration af en simpel arbejdsskabelon, der skal bruges, når varer, du har modtaget, lægges på lager.</span><span class="sxs-lookup"><span data-stu-id="e1053-104">This procedure focuses on the set up of a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="e1053-105">Arbejdsskabeloner bestemmer det sæt instruktioner, der vises for lagermedarbejderen på en mobilenhed, når varer flyttes fra modtagelsesområdet.</span><span class="sxs-lookup"><span data-stu-id="e1053-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="e1053-106">Du kan bruge denne procedure med de nævnte data i demodatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="e1053-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="e1053-107">Før du starter denne vejledning, skal du oprette et arbejdspulje-id.</span><span class="sxs-lookup"><span data-stu-id="e1053-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="e1053-108">I dette eksempel bruges arbejdspulje-id'et Indgående.</span><span class="sxs-lookup"><span data-stu-id="e1053-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="e1053-109">Denne procedure er beregnet til lagerchefen.</span><span class="sxs-lookup"><span data-stu-id="e1053-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="e1053-110">Gå til Lagerstedsstyring > Opsætning > Arbejde > Arbejdsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="e1053-110">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="e1053-111">I feltet Arbejdsordretype skal du vælge "Indkøbsordrer".</span><span class="sxs-lookup"><span data-stu-id="e1053-111">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="e1053-112">Oprette et arbejdsskabelonhoved</span><span class="sxs-lookup"><span data-stu-id="e1053-112">Create a work template header</span></span>
1. <span data-ttu-id="e1053-113">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e1053-113">Click New.</span></span>
2. <span data-ttu-id="e1053-114">Indtast et tal i feltet Sekvensnummer.</span><span class="sxs-lookup"><span data-stu-id="e1053-114">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="e1053-115">Dette er den rækkefølge, som arbejdsskabelonerne skal evalueres i.</span><span class="sxs-lookup"><span data-stu-id="e1053-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="e1053-116">Du kan om nødvendigt ændre rækkefølgen.</span><span class="sxs-lookup"><span data-stu-id="e1053-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="e1053-117">Indtast en værdi i feltet Arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="e1053-117">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="e1053-118">Dette er det entydige id for denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="e1053-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="e1053-119">Skriv en værdi i feltet Beskrivelse af arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="e1053-119">In the Work template description field, type a value.</span></span>
    * <span data-ttu-id="e1053-120">Indstillingen Gyldig markeres ikke, før du har fuldført alle de oplysninger, der er nødvendige for skabelonen, og derefter har klikket på Gem.</span><span class="sxs-lookup"><span data-stu-id="e1053-120">The Valid option will not be checked until you’ve completed all the information that's needed by the template and have then clicked Save.</span></span>  
    * <span data-ttu-id="e1053-121">En arbejdsordre af typen Indkøbsordre kan ikke behandles automatisk, så lad indstillingen Udfør automatisk behandling være indstillet til Nej.</span><span class="sxs-lookup"><span data-stu-id="e1053-121">A work order of type Purchase order cannot be automatically processed, so leave the  Automatically process option set to No.</span></span>  
5. <span data-ttu-id="e1053-122">Indtast en værdi i feltet Arbejdspulje-id.</span><span class="sxs-lookup"><span data-stu-id="e1053-122">In the Work pool ID field, type a value.</span></span>
    * <span data-ttu-id="e1053-123">Med arbejdspulje-id'er kan du organisere arbejde i grupper.</span><span class="sxs-lookup"><span data-stu-id="e1053-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="e1053-124">Den værdi, du angiver her, bliver standardværdien for arbejde, der oprettes ved hjælp af denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="e1053-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="e1053-125">Skriv 1 i feltet Arbejdsprioritet.</span><span class="sxs-lookup"><span data-stu-id="e1053-125">In the Work priority field, enter '1'.</span></span>
    * <span data-ttu-id="e1053-126">Dette angiver vigtigheden af arbejdet, og den værdi, du angiver her, bliver brugt som standard for alt arbejde, der oprettes ved hjælp af denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="e1053-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="e1053-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e1053-127">Click Save.</span></span>
    * <span data-ttu-id="e1053-128">Du skal gemme arbejdsskabelonhovedet, før knappen Rediger forespørgsel bliver tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="e1053-128">You must save the work template header before the Edit Query button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="e1053-129">Konfigurer forespørgslen til arbejdsskabelonen</span><span class="sxs-lookup"><span data-stu-id="e1053-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="e1053-130">Klik på Rediger forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="e1053-130">Click Edit query.</span></span>
    * <span data-ttu-id="e1053-131">Vi skal angive en begrænsning, så skabelonen kun kan bruges på et bestemt lagersted.</span><span class="sxs-lookup"><span data-stu-id="e1053-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="e1053-132">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="e1053-132">Click Add.</span></span>
3. <span data-ttu-id="e1053-133">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e1053-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e1053-134">I feltet Felt skal du skrive "lagersted".</span><span class="sxs-lookup"><span data-stu-id="e1053-134">In the Field field, type 'warehouse'.</span></span>
5. <span data-ttu-id="e1053-135">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="e1053-135">In the Criteria field, type a value.</span></span>
6. <span data-ttu-id="e1053-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e1053-136">Click OK.</span></span>
7. <span data-ttu-id="e1053-137">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="e1053-137">Click Yes.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="e1053-138">Angiv arbejdsskabelondetaljer</span><span class="sxs-lookup"><span data-stu-id="e1053-138">Set work template details</span></span>
1. <span data-ttu-id="e1053-139">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e1053-139">Click New.</span></span>
2. <span data-ttu-id="e1053-140">Vælg "Pluk" i feltet Arbejdstype.</span><span class="sxs-lookup"><span data-stu-id="e1053-140">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="e1053-141">Skriv "køb" i feltet Arbejdsklasse-id.</span><span class="sxs-lookup"><span data-stu-id="e1053-141">In the Work class ID field, type 'purchase'.</span></span>
    * <span data-ttu-id="e1053-142">Den arbejdsklassen, som du angiver her, bliver standard på alle arbejdslinjer af typen Pluk, som oprettes ved hjælp af denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="e1053-142">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="e1053-143">Arbejdsklassen kan ikke tilsidesættes i arbejdsordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="e1053-143">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="e1053-144">Arbejdsklasser bruges til at dirigere og/eller begrænse typen af arbejdsordrelinjer, som en lagermedarbejder kan behandle på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="e1053-144">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="e1053-145">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e1053-145">Click New.</span></span>
5. <span data-ttu-id="e1053-146">Vælg 'Læg på lager' i feltet Arbejdstype.</span><span class="sxs-lookup"><span data-stu-id="e1053-146">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="e1053-147">Skriv en værdi i feltet Arbejdsklasse-id.</span><span class="sxs-lookup"><span data-stu-id="e1053-147">In the Work class ID field, type a value.</span></span>
    * <span data-ttu-id="e1053-148">Pluk og læg-instruktionerne er et sæt.</span><span class="sxs-lookup"><span data-stu-id="e1053-148">The pick and put instructions are a set.</span></span> <span data-ttu-id="e1053-149">Hvert pluk/lægsæt skal have samme arbejdsklasse.</span><span class="sxs-lookup"><span data-stu-id="e1053-149">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="e1053-150">Brug samme arbejdsklasse, som du angav for plukinstruktionen.</span><span class="sxs-lookup"><span data-stu-id="e1053-150">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="e1053-151">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e1053-151">Click Save.</span></span>
    * <span data-ttu-id="e1053-152">Bemærk, at afkrydsningsfeltet Gyldig nu er markeret.</span><span class="sxs-lookup"><span data-stu-id="e1053-152">Note that the Valid checkbox is now checked.</span></span>  


