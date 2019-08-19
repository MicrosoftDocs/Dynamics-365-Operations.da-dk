---
title: Bruge sikkerhedslagerkladde for at opdatere minimumdisponering
description: Denne fremgangsmåde viser, hvordan du kan beregne minimumdækningsforslaget baseret på historiske transaktioner og derefter opdatere varedisponeringen med forslagene.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3b2916d6d2f24579fd9795c0e0bc548b6c2b747
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835767"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="3f2db-103">Bruge sikkerhedslagerkladde for at opdatere minimumdisponering</span><span class="sxs-lookup"><span data-stu-id="3f2db-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f2db-104">Denne fremgangsmåde viser, hvordan du kan beregne minimumdækningsforslaget baseret på historiske transaktioner og derefter opdatere varedisponeringen med forslagene.</span><span class="sxs-lookup"><span data-stu-id="3f2db-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="3f2db-105">Dette kan du gøre ved hjælp af sikkerhedslagerkladden.</span><span class="sxs-lookup"><span data-stu-id="3f2db-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="3f2db-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="3f2db-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="3f2db-107">Denne opgave er beregnet til produktionsplanlæggeren og skal hjælpe med at vedligeholde minimumdækning.</span><span class="sxs-lookup"><span data-stu-id="3f2db-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="3f2db-108">Opret et nyt sikkerhedslagerkladdenavn</span><span class="sxs-lookup"><span data-stu-id="3f2db-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="3f2db-109">Gå til Sikkerhedslagerkladdenavne.</span><span class="sxs-lookup"><span data-stu-id="3f2db-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="3f2db-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3f2db-110">Click New.</span></span>
3. <span data-ttu-id="3f2db-111">Skriv 'Materiale' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3f2db-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="3f2db-112">Skriv 'Materiale' i feltet 'Beskrivelse'.</span><span class="sxs-lookup"><span data-stu-id="3f2db-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="3f2db-113">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3f2db-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="3f2db-114">Opret en sikkerhedslagerkladde</span><span class="sxs-lookup"><span data-stu-id="3f2db-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="3f2db-115">Gå til Beregning af sikkerhedslager.</span><span class="sxs-lookup"><span data-stu-id="3f2db-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="3f2db-116">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3f2db-116">Click New.</span></span>
3. <span data-ttu-id="3f2db-117">Indtast eller vælg en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3f2db-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="3f2db-118">Vælg den sikkerhedslagerkladde, du har oprettet, for eksempel Materiale.</span><span class="sxs-lookup"><span data-stu-id="3f2db-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="3f2db-119">Klik på Opret linjer.</span><span class="sxs-lookup"><span data-stu-id="3f2db-119">Click Create lines.</span></span>
5. <span data-ttu-id="3f2db-120">Indtast en dato i feltet Fra dato.</span><span class="sxs-lookup"><span data-stu-id="3f2db-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="3f2db-121">Sæt bilagsdato til '02-01-2015'.</span><span class="sxs-lookup"><span data-stu-id="3f2db-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="3f2db-122">Indtast en dato i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="3f2db-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="3f2db-123">Sæt bilagsdato til '30-12-2015'.</span><span class="sxs-lookup"><span data-stu-id="3f2db-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="3f2db-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3f2db-124">Click OK.</span></span>
    * <span data-ttu-id="3f2db-125">Derved oprettes der linjer for de dimensioner, der har lagerposteringer.</span><span class="sxs-lookup"><span data-stu-id="3f2db-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="3f2db-126">Beregn forslag</span><span class="sxs-lookup"><span data-stu-id="3f2db-126">Calculate proposal</span></span>
1. <span data-ttu-id="3f2db-127">Klik på Beregn forslag.</span><span class="sxs-lookup"><span data-stu-id="3f2db-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="3f2db-128">Vælg indstillingen Brug gns.afgang under gennemløbstiden.</span><span class="sxs-lookup"><span data-stu-id="3f2db-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="3f2db-129">Angiv multiplikationsfaktoren til '10'.</span><span class="sxs-lookup"><span data-stu-id="3f2db-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="3f2db-130">Miltipliceringsfaktoren bruges til at justere forslaget.</span><span class="sxs-lookup"><span data-stu-id="3f2db-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="3f2db-131">Fordi demodata kun har få transaktioner, skal du angive faktoren for at få et realistisk forslag.</span><span class="sxs-lookup"><span data-stu-id="3f2db-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="3f2db-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3f2db-132">Click OK.</span></span>
    * <span data-ttu-id="3f2db-133">Rul ned for at finde M0002 og M0003.</span><span class="sxs-lookup"><span data-stu-id="3f2db-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="3f2db-134">Få vist kolonnen Beregnet minimumantal.</span><span class="sxs-lookup"><span data-stu-id="3f2db-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="3f2db-135">Opdater minimummængde</span><span class="sxs-lookup"><span data-stu-id="3f2db-135">Update minimum quantity</span></span>
1. <span data-ttu-id="3f2db-136">Indtast et tal i feltet Ny minimummængde.</span><span class="sxs-lookup"><span data-stu-id="3f2db-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="3f2db-137">Opdater den nye minimummængde, så den svarer til værdien i den beregnede minimummængde.</span><span class="sxs-lookup"><span data-stu-id="3f2db-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="3f2db-138">Hvis det beregnede minimum er nul, kan du angive den ønskede fremtidige værdi.</span><span class="sxs-lookup"><span data-stu-id="3f2db-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="3f2db-139">Du kan f.eks. angive den beregnede minimummængde i dette felt for M0002, der har lagersted 12.</span><span class="sxs-lookup"><span data-stu-id="3f2db-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="3f2db-140">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3f2db-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3f2db-141">Du kan f.eks. vælge M0002, der har lagersted 12.</span><span class="sxs-lookup"><span data-stu-id="3f2db-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="3f2db-142">Indtast et tal i feltet Ny minimummængde.</span><span class="sxs-lookup"><span data-stu-id="3f2db-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="3f2db-143">Opdater den nye minimummængde, så den svarer til værdien i den beregnede minimummængde.</span><span class="sxs-lookup"><span data-stu-id="3f2db-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="3f2db-144">Hvis det beregnede minimum er nul, kan du angive den ønskede fremtidige værdi.</span><span class="sxs-lookup"><span data-stu-id="3f2db-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="3f2db-145">Bogfør det nye minimumantal, og valider resultatet</span><span class="sxs-lookup"><span data-stu-id="3f2db-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="3f2db-146">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="3f2db-146">Click Post.</span></span>
2. <span data-ttu-id="3f2db-147">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3f2db-147">Click OK.</span></span>
3. <span data-ttu-id="3f2db-148">Klik for at følge linket i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="3f2db-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="3f2db-149">Klik for at følge linket i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="3f2db-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="3f2db-150">Klik på Plan i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3f2db-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="3f2db-151">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="3f2db-151">Click Item coverage.</span></span>
    * <span data-ttu-id="3f2db-152">Bemærk, at minimumantallet er blevet opdateret med det nye minimumsantal fra sikkerhedslagerkladden.</span><span class="sxs-lookup"><span data-stu-id="3f2db-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  

