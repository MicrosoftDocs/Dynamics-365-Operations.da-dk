---
title: Bruge sikkerhedslagerkladde for at opdatere minimumdisponering
description: Denne fremgangsmåde viser, hvordan du kan beregne minimumdækningsforslaget baseret på historiske transaktioner og derefter opdatere varedisponeringen med forslagene.
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d69daf3d307ba72ff6017d91849e3d22bd0bd85
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210312"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="b33d4-103">Bruge sikkerhedslagerkladde for at opdatere minimumdisponering</span><span class="sxs-lookup"><span data-stu-id="b33d4-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b33d4-104">Denne fremgangsmåde viser, hvordan du kan beregne minimumdækningsforslaget baseret på historiske transaktioner og derefter opdatere varedisponeringen med forslagene.</span><span class="sxs-lookup"><span data-stu-id="b33d4-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="b33d4-105">Dette kan du gøre ved hjælp af sikkerhedslagerkladden.</span><span class="sxs-lookup"><span data-stu-id="b33d4-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="b33d4-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="b33d4-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="b33d4-107">Denne opgave er beregnet til produktionsplanlæggeren og skal hjælpe med at vedligeholde minimumdækning.</span><span class="sxs-lookup"><span data-stu-id="b33d4-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="b33d4-108">Opret et nyt sikkerhedslagerkladdenavn</span><span class="sxs-lookup"><span data-stu-id="b33d4-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="b33d4-109">Gå i **Navigationsrude** til **Varedisponering > Opsætning > Sikkerhedslagerkladdenavne**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="b33d4-110">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-110">Click **New**.</span></span>
3. <span data-ttu-id="b33d4-111">Skriv 'Materiale' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="b33d4-112">Skriv 'Materiale' i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="b33d4-113">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b33d4-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="b33d4-114">Opret en sikkerhedslagerkladde</span><span class="sxs-lookup"><span data-stu-id="b33d4-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="b33d4-115">Gå i **Navigationsrude** til **Varedisponering > Varedisponering > Kørsel > Beregning af sikkerhedslager**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="b33d4-116">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-116">Click **New**.</span></span>
3. <span data-ttu-id="b33d4-117">Indtast eller vælg en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="b33d4-118">Vælg den sikkerhedslagerkladde, du har oprettet, for eksempel Materiale.</span><span class="sxs-lookup"><span data-stu-id="b33d4-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="b33d4-119">Klik på **Opret linjer**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="b33d4-120">Indtast en dato i feltet **Fra dato**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="b33d4-121">Indtast en dato i feltet **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="b33d4-122">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-122">Click **OK**.</span></span> <span data-ttu-id="b33d4-123">Derved oprettes der linjer for de dimensioner, der har lagerposteringer.</span><span class="sxs-lookup"><span data-stu-id="b33d4-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="b33d4-124">Beregn forslag</span><span class="sxs-lookup"><span data-stu-id="b33d4-124">Calculate proposal</span></span>
1. <span data-ttu-id="b33d4-125">Klik på **Beregn forslag**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="b33d4-126">Vælg indstillingen **Brug gns.afgang under gennemløbstiden**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="b33d4-127">Indstil **Multiplikationsfaktor** til '10'.</span><span class="sxs-lookup"><span data-stu-id="b33d4-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="b33d4-128">Miltipliceringsfaktoren bruges til at justere forslaget.</span><span class="sxs-lookup"><span data-stu-id="b33d4-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="b33d4-129">Fordi demodata kun har få transaktioner, skal du angive faktoren for at få et realistisk forslag.</span><span class="sxs-lookup"><span data-stu-id="b33d4-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="b33d4-130">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-130">Click **OK**.</span></span> <span data-ttu-id="b33d4-131">Rul ned for at finde M0002 og M0003.</span><span class="sxs-lookup"><span data-stu-id="b33d4-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="b33d4-132">Vis kolonnen **Beregnet minimumantal**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="b33d4-133">Opdater minimummængde</span><span class="sxs-lookup"><span data-stu-id="b33d4-133">Update minimum quantity</span></span>
1. <span data-ttu-id="b33d4-134">Indtast et tal i feltet **Ny minimummængde**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="b33d4-135">Opdater den nye minimummængde, så den svarer til værdien i den beregnede minimummængde.</span><span class="sxs-lookup"><span data-stu-id="b33d4-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="b33d4-136">Hvis det beregnede minimum er nul, kan du angive den ønskede fremtidige værdi.</span><span class="sxs-lookup"><span data-stu-id="b33d4-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="b33d4-137">Du kan f.eks. angive den beregnede minimummængde i dette felt for M0002, der har lagersted 12.</span><span class="sxs-lookup"><span data-stu-id="b33d4-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="b33d4-138">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b33d4-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="b33d4-139">Du kan f.eks. vælge M0002, der har lagersted 12.</span><span class="sxs-lookup"><span data-stu-id="b33d4-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="b33d4-140">Indtast et tal i feltet **Ny minimummængde**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="b33d4-141">Opdater den nye minimummængde, så den svarer til værdien i den beregnede minimummængde.</span><span class="sxs-lookup"><span data-stu-id="b33d4-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="b33d4-142">Hvis det beregnede minimum er nul, kan du angive den ønskede fremtidige værdi.</span><span class="sxs-lookup"><span data-stu-id="b33d4-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="b33d4-143">Bogfør det nye minimumantal, og valider resultatet</span><span class="sxs-lookup"><span data-stu-id="b33d4-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="b33d4-144">Klik på **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-144">Click **Post**.</span></span>
2. <span data-ttu-id="b33d4-145">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-145">Click **OK**.</span></span>
3. <span data-ttu-id="b33d4-146">Klik for at følge linket i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="b33d4-147">Klik for at følge linket i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="b33d4-148">Klik på Plan i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="b33d4-149">Klik på **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="b33d4-149">Click **Item coverage**.</span></span> <span data-ttu-id="b33d4-150">Bemærk, at **Minimumantal** er blevet opdateret med det nye minimumsantal fra sikkerhedslagerkladden.</span><span class="sxs-lookup"><span data-stu-id="b33d4-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  

