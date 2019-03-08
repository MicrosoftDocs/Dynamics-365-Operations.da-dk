---
title: Registrere materialeforbrug ved hjælp af en mobilenhed
description: I dette emne beskrives en arbejdsgang, der gør det muligt at registrere forbrug af råmaterialer i produktionen ved hjælp af en håndholdt enhed.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5b9c73cf9b23eb8ad9ed872b76b92b395609e9a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "336123"
---
# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="600cc-103">Registrere materialeforbrug ved hjælp af en mobilenhed</span><span class="sxs-lookup"><span data-stu-id="600cc-103">Register material consumption using a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="600cc-104">I dette emne beskrives en arbejdsgang, der gør det muligt at registrere forbrug af råmaterialer i produktionen ved hjælp af en håndholdt enhed.</span><span class="sxs-lookup"><span data-stu-id="600cc-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="600cc-105">Introduktion</span><span class="sxs-lookup"><span data-stu-id="600cc-105">Introduction</span></span>
------------

<span data-ttu-id="600cc-106">Denne arbejdsproces er relevant, hvis der er strenge krav til sporbarhed af materialer.</span><span class="sxs-lookup"><span data-stu-id="600cc-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="600cc-107">I så fald skal den nøjagtige tid og det nøjagtige antal rapporteres for forbruget for at opretholde materialernes sporbarhed.</span><span class="sxs-lookup"><span data-stu-id="600cc-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="600cc-108">Denne proces kan ses som modsætning til forlæns- eller baglænstrækoperationer, hvor der er en forskydning mellem tidspunktet for registreringen og tidspunktet, hvornår det faktiske forbrug finder sted.</span><span class="sxs-lookup"><span data-stu-id="600cc-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="600cc-109">Det forklarer, hvorfor en strategi for automatisk forbrug ikke kan bruges til visse materialer med krav til sporbarhed.</span><span class="sxs-lookup"><span data-stu-id="600cc-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="600cc-110">Lad os se på et enkelt scenario, der forklarer, hvordan du konfigurerer en arbejdsgang for at aktivere registrering af forbrug af råmaterialer i produktionen ved hjælp af en håndholdt enhed.</span><span class="sxs-lookup"><span data-stu-id="600cc-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> <span data-ttu-id="600cc-111">[![Konfigurere en arbejdsgang for at aktivere registrering af forbrug af råmaterialer ved hjælp af en håndholdt enhed](./media/scenario3.png)](./media/scenario3.png)</span><span class="sxs-lookup"><span data-stu-id="600cc-111">[![set up a workflow to enable registration of raw material consumption by using a handheld device](./media/scenario3.png)](./media/scenario3.png)</span></span>

### <a name="scenario-details"></a><span data-ttu-id="600cc-112">Scenariedetaljer</span><span class="sxs-lookup"><span data-stu-id="600cc-112">Scenario details</span></span>

<span data-ttu-id="600cc-113">I en fortløbende produktionsproces (5) bruges det batchstyrede råmateriale RM-100.</span><span class="sxs-lookup"><span data-stu-id="600cc-113">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="600cc-114">Materialet er disponibelt på lokationen Bulk-001 (1) i id'et PL-1 med to batches, B1 og B2, begge med et antal på 100 kg.</span><span class="sxs-lookup"><span data-stu-id="600cc-114">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="600cc-115">Lagerstedsarbejde (2) frigives og behandles for RM-100, og materialet plukkes fra Bulk-001 til produktionsindlagringslokationen PIL-01 (3), der er defineret som ikke-id-styret.</span><span class="sxs-lookup"><span data-stu-id="600cc-115">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="600cc-116">Maskinoperatøren afvejer materiale fra produktionsindlagringslokationen (3) og registrerer vægten og batchnummeret som forbrugt (4).</span><span class="sxs-lookup"><span data-stu-id="600cc-116">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="600cc-117">Fra produktionsindlagringslokationen føjes en del af materialet manuelt til produktionsprocessen i fastlagte tidsintervaller.</span><span class="sxs-lookup"><span data-stu-id="600cc-117">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="600cc-118">Når maskinoperatøren tilføjer materiale, vejes det på en vægt, og batchnummeret registreres.</span><span class="sxs-lookup"><span data-stu-id="600cc-118">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-theworkflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="600cc-119">Konfigurere arbejdsgangen for at registrere forbrug ved hjælp af en håndholdt enhed</span><span class="sxs-lookup"><span data-stu-id="600cc-119">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="600cc-120">Opret et færdigvareprodukt, FG-100, med en stykliste, der har det batchstyrede råmateriale RM-100.</span><span class="sxs-lookup"><span data-stu-id="600cc-120">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="600cc-121">Tilføj to batches, B1 og B2, af RM-100 i et antal på 100 til lokation: Bulk-001 på id: PL 1.</span><span class="sxs-lookup"><span data-stu-id="600cc-121">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="600cc-122">Den varetrækprincippet på styklistelinjen for RM-100 er indstillet til **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="600cc-122">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="600cc-123">Indstil produktionsindlagringslokationen til PIL-01.</span><span class="sxs-lookup"><span data-stu-id="600cc-123">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="600cc-124">Du kan gøre det ved at vælge denne lokation som standardproduktionsindlagringslokationen for lagersted til 51.</span><span class="sxs-lookup"><span data-stu-id="600cc-124">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="600cc-125">Oprette et nyt menupunkt på en mobilenhed:</span><span class="sxs-lookup"><span data-stu-id="600cc-125">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="600cc-126">**Menupunktnavn** - Registrer materialeforbrug.</span><span class="sxs-lookup"><span data-stu-id="600cc-126">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="600cc-127">**Titel** - Registrer materialeforbrug.</span><span class="sxs-lookup"><span data-stu-id="600cc-127">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="600cc-128">**Tilstand** - Indirekte.</span><span class="sxs-lookup"><span data-stu-id="600cc-128">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="600cc-129">**Aktivitetskode** – Registrer materialeforbrug.</span><span class="sxs-lookup"><span data-stu-id="600cc-129">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="600cc-130">Føj menupunktet til menuen for **Produktionsmobilenheden**.</span><span class="sxs-lookup"><span data-stu-id="600cc-130">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="600cc-131">Opret en produktionsordre for et færdige projekt.</span><span class="sxs-lookup"><span data-stu-id="600cc-131">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="600cc-132">**Varenummer**- FG-100</span><span class="sxs-lookup"><span data-stu-id="600cc-132">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="600cc-133">**Lokation** - 5</span><span class="sxs-lookup"><span data-stu-id="600cc-133">**Site** - 5</span></span> 
-    <span data-ttu-id="600cc-134">**Lagersted** - 51</span><span class="sxs-lookup"><span data-stu-id="600cc-134">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="600cc-135">**Antal** - 150</span><span class="sxs-lookup"><span data-stu-id="600cc-135">**Quantity** - 150</span></span>

<span data-ttu-id="600cc-136">Produktionsordren er **Estimeret** og **Frigivet** og lagerstedsarbejde er oprettet.</span><span class="sxs-lookup"><span data-stu-id="600cc-136">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="600cc-137">Afslut arbejdet ved hjælp af arbejdsgangen for råmaterialepluk for den håndholdte enhed.</span><span class="sxs-lookup"><span data-stu-id="600cc-137">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="600cc-138">Derved føres materialet fra bulkvarelokationen til produktionsindlagringslokation PIL-01.</span><span class="sxs-lookup"><span data-stu-id="600cc-138">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="600cc-139">Når arbejdet er fuldført, har materialet status **Plukket på produktionsindlagringslokationen**.</span><span class="sxs-lookup"><span data-stu-id="600cc-139">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="600cc-140">Status efter at arbejdet er blevet behandlet kan være enten **Plukket** eller **Reserveret fysisk**.</span><span class="sxs-lookup"><span data-stu-id="600cc-140">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="600cc-141">Dette konfigureres med parameteren **Afgangsstatus efter læg på lager i lagerstedsformularen**.</span><span class="sxs-lookup"><span data-stu-id="600cc-141">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="600cc-142">Igangsæt produktionsordren fra klienten eller fra den håndholdte enhed ved hjælp af menupunktet **Produktionsstart**.</span><span class="sxs-lookup"><span data-stu-id="600cc-142">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="600cc-143">Når produktionsordren er startet, kan du registrere materialeforbruget med arbejdsgangen for den håndholdte enhed.</span><span class="sxs-lookup"><span data-stu-id="600cc-143">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="600cc-144">Lad os starte med at registrere forbruget på 25 kg af batch B1.</span><span class="sxs-lookup"><span data-stu-id="600cc-144">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="600cc-145">Vælg menupunktet **Registrer materiale** **forbrug** i menuen for den håndholdte enhed, og angiv følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="600cc-145">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="600cc-146">Produktionsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="600cc-146">The production order number.</span></span> 
-    <span data-ttu-id="600cc-147">Det sted, hvor materialet skal forbruges, i dette tilfælde PIL-01.</span><span class="sxs-lookup"><span data-stu-id="600cc-147">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="600cc-148">Varenummer RM-100.</span><span class="sxs-lookup"><span data-stu-id="600cc-148">Item number RM-100.</span></span> 
-    <span data-ttu-id="600cc-149">Batchnummer B1.</span><span class="sxs-lookup"><span data-stu-id="600cc-149">Batch number B1.</span></span> 
-    <span data-ttu-id="600cc-150">Et antal på 25.</span><span class="sxs-lookup"><span data-stu-id="600cc-150">A quantity of 25.</span></span>

7.  <span data-ttu-id="600cc-151">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="600cc-151">Select **OK**.</span></span>

<span data-ttu-id="600cc-152">Bemærk, at meddelelsen "Journallinje er oprettet" vises på skærmen.</span><span class="sxs-lookup"><span data-stu-id="600cc-152">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="600cc-153">I produktionsordren er der en åben kladde af typen **Produktionsplukliste** for varenummer RM-100 og batchnummer B1.</span><span class="sxs-lookup"><span data-stu-id="600cc-153">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="600cc-154">Du kan nu vælge at fortsætte registreringen, for eksempel på batchnummer B2, og hver gang du vælger **OK**, føjes der en ny kladdelinje til den åbne kladde.</span><span class="sxs-lookup"><span data-stu-id="600cc-154">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="600cc-155">Når du har gennemført registreringen, kan du vælge **Udført** for at bogføre kladden og afslutte arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="600cc-155">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="600cc-156">Yderligere kommentarer</span><span class="sxs-lookup"><span data-stu-id="600cc-156">Additional comments</span></span> 

-   <span data-ttu-id="600cc-157">Hvis en bruger annullerer arbejdsgangen, når der oprettes en kladdelinje, er kladden i en ikke-bogført tilstand, men hvis brugeren på et senere tidspunkt bruger arbejdsgangen til den samme produktionsordre, føjes linjerne til den åbne kladde i stedet for en ny kladde.</span><span class="sxs-lookup"><span data-stu-id="600cc-157">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="600cc-158">Den nye arbejdsgang understøtter også registrering af serienumre.</span><span class="sxs-lookup"><span data-stu-id="600cc-158">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="600cc-159">Det er kun muligt at registrere et varenummer, der er defineret i styklisten eller formlen for den valgte produktionsordre eller batchordre.</span><span class="sxs-lookup"><span data-stu-id="600cc-159">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="600cc-160">Materiale kan overforbruges.</span><span class="sxs-lookup"><span data-stu-id="600cc-160">Material can be overconsumed.</span></span> <span data-ttu-id="600cc-161">Hvis der f.eks. er forkalkuleret et materialeforbrug på 100 kg, kan det være et overforbrug på f.eks. 105 kg.</span><span class="sxs-lookup"><span data-stu-id="600cc-161">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>


