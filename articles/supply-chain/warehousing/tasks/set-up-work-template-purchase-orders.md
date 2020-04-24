---
title: Konfigurere en arbejdsskabelon for indkøbsordrer
description: I dette emne beskrives, hvordan du konfigurerer en simpel arbejdsskabelon, der skal bruges, når varer, du har modtaget, lægges på lager.
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a3e91fe67ed97b37bfb89f5f487e2bc59c3f7bb8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216752"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="7f3c2-103">Konfigurere en arbejdsskabelon for indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="7f3c2-103">Set up a work template for purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f3c2-104">I dette emne beskrives, hvordan du konfigurerer en simpel arbejdsskabelon, der skal bruges, når varer, du har modtaget, lægges på lager.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="7f3c2-105">Arbejdsskabeloner bestemmer det sæt instruktioner, der vises for lagermedarbejderen på en mobilenhed, når varer flyttes fra modtagelsesområdet.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="7f3c2-106">Du kan bruge denne procedure med de nævnte data i demodatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="7f3c2-107">Før du starter denne vejledning, skal du oprette et arbejdspulje-id.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="7f3c2-108">I dette eksempel bruges arbejdspulje-id'et Indgående.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="7f3c2-109">Denne procedure er beregnet til lagerchefen.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="7f3c2-110">I navigationsruden skal du gå til **Moduler > Lokationsstyring > Opsætning > Arbejde > Arbejdsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="7f3c2-111">I feltet **Arbejdsordretype** skal du vælge **Indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="7f3c2-112">Oprette et arbejdsskabelonhoved</span><span class="sxs-lookup"><span data-stu-id="7f3c2-112">Create a work template header</span></span>
1. <span data-ttu-id="7f3c2-113">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-113">Select **New**.</span></span>
2. <span data-ttu-id="7f3c2-114">Indtast et tal i feltet **Serienummer**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="7f3c2-115">Dette er den rækkefølge, som arbejdsskabelonerne skal evalueres i.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="7f3c2-116">Du kan om nødvendigt ændre rækkefølgen.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="7f3c2-117">Indtast en værdi i feltet **Arbejdsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="7f3c2-118">Dette er det entydige id for denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="7f3c2-119">Skriv en værdi i feltet **Beskrivelse af arbejdsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="7f3c2-120">Indstillingen **Gyldig** markeres ikke, før du har fuldført alle de oplysninger, der er nødvendige for skabelonen, og derefter har valgt **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-120">The **Valid** option will not be checked until you've completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="7f3c2-121">En arbejdsordre af typen **Indkøbsordre** kan ikke behandles automatisk, så lad indstillingen **Udfør automatisk behandling** være indstillet til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="7f3c2-122">Indtast en værdi i feltet **Arbejdspulje-id**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="7f3c2-123">Med arbejdspulje-id'er kan du organisere arbejde i grupper.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="7f3c2-124">Den værdi, du angiver her, bliver standardværdien for arbejde, der oprettes ved hjælp af denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-124">The value that you set here will be the default value for any work that's created using this template.</span></span>  
6. <span data-ttu-id="7f3c2-125">Skriv `1` i feltet **Arbejdsprioritet**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="7f3c2-126">Dette angiver vigtigheden af arbejdet, og den værdi, du angiver her, bliver brugt som standard for alt arbejde, der oprettes ved hjælp af denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="7f3c2-127">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-127">Select **Save**.</span></span> <span data-ttu-id="7f3c2-128">Du skal gemme arbejdsskabelonhovedet, før knappen **Rediger forespørgsel** bliver tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="7f3c2-129">Konfigurer forespørgslen til arbejdsskabelonen</span><span class="sxs-lookup"><span data-stu-id="7f3c2-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="7f3c2-130">Vælg **Rediger forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-130">Select **Edit query**.</span></span> <span data-ttu-id="7f3c2-131">Vi skal angive en begrænsning, så skabelonen kun kan bruges på et bestemt lagersted.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-131">We'll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="7f3c2-132">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-132">Select **Add**.</span></span>
3. <span data-ttu-id="7f3c2-133">I feltet **Felt** for den nye række skal du skrive `warehouse`.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="7f3c2-134">Skriv en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="7f3c2-135">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-135">Select **OK**.</span></span>
6. <span data-ttu-id="7f3c2-136">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="7f3c2-137">Angiv arbejdsskabelondetaljer</span><span class="sxs-lookup"><span data-stu-id="7f3c2-137">Set work template details</span></span>
1. <span data-ttu-id="7f3c2-138">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-138">Select **New**.</span></span>
2. <span data-ttu-id="7f3c2-139">Vælg **Pluk** i feltet **Arbejdstype**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="7f3c2-140">Skriv `purchase` i feltet **Arbejdsklasse-id**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="7f3c2-141">Den arbejdsklassen, som du angiver her, bliver standard på alle arbejdslinjer af typen Pluk, som oprettes ved hjælp af denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="7f3c2-142">Arbejdsklassen kan ikke tilsidesættes i arbejdsordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="7f3c2-143">Arbejdsklasser bruges til at dirigere og/eller begrænse typen af arbejdsordrelinjer, som en lagermedarbejder kan behandle på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="7f3c2-144">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-144">Select **New**.</span></span>
5. <span data-ttu-id="7f3c2-145">Vælg **Læg på lager** i feltet **Arbejdstype**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="7f3c2-146">Skriv en værdi i feltet **Arbejdsklasse-id**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="7f3c2-147">Pluk og læg-instruktionerne er et sæt.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="7f3c2-148">Hvert pluk/lægsæt skal have samme arbejdsklasse.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="7f3c2-149">Brug samme arbejdsklasse, som du angav for plukinstruktionen.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="7f3c2-150">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-150">Select **Save**.</span></span> <span data-ttu-id="7f3c2-151">Bemærk, at afkrydsningsfeltet **Gyldig** nu er markeret.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-151">Note that the **Valid** checkbox is now checked.</span></span>  

