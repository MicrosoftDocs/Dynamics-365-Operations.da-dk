---
title: Føje en beregningspolitik for kanban-mængder til en kanban-regel
description: Denne fremgangsmåde drejer sig om oprettelse af en politik for beregning af kanban-mængde og føje den til en kanban-regel til optimering af kanban-størrelse og mængde.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules, KanbanQuantityCalculation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a32753701c9e06c46ed9b2a9c4b0329f62f15597
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255463"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="a6082-103">Føje en beregningspolitik for kanban-mængder til en kanban-regel</span><span class="sxs-lookup"><span data-stu-id="a6082-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6082-104">Denne fremgangsmåde drejer sig om oprettelse af en politik for beregning af kanban-mængde og føje den til en kanban-regel til optimering af kanban-størrelse og mængde.</span><span class="sxs-lookup"><span data-stu-id="a6082-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="a6082-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="a6082-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a6082-106">Denne procedure er beregnet til værdistrømlederen.</span><span class="sxs-lookup"><span data-stu-id="a6082-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="a6082-107">Denne procedure er en forudsætning for oprettelse af proceduren Beregn kanban-mængdeforslag.</span><span class="sxs-lookup"><span data-stu-id="a6082-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="a6082-108">Opret en politik til beregning af kanban-mængde</span><span class="sxs-lookup"><span data-stu-id="a6082-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="a6082-109">Gå til Produktionsstyring > Periodiske opgaver > Beregning af kanban-mængde > Politikker for beregning af kanban-mængder.</span><span class="sxs-lookup"><span data-stu-id="a6082-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="a6082-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a6082-110">Click New.</span></span>
3. <span data-ttu-id="a6082-111">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="a6082-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a6082-112">Skriv f.eks. Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="a6082-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="a6082-113">Klik på rullelisten i feltet Behovsplan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a6082-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a6082-114">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="a6082-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a6082-115">Vælg StaticPlan for at beregne behov.</span><span class="sxs-lookup"><span data-stu-id="a6082-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="a6082-116">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a6082-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="a6082-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a6082-117">Click Save.</span></span>
8. <span data-ttu-id="a6082-118">Indtast "1" i feltet Mindste kanban-mængde.</span><span class="sxs-lookup"><span data-stu-id="a6082-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="a6082-119">Dette er det ekstra antal kanbans, der er medtaget i beregningen af kanban-mængder.</span><span class="sxs-lookup"><span data-stu-id="a6082-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="a6082-120">Indstil Sikkerhedsfaktor til "1".</span><span class="sxs-lookup"><span data-stu-id="a6082-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="a6082-121">Dette er den faktor, der bruges til at beregne den ekstra mængde sikkerhedslager.</span><span class="sxs-lookup"><span data-stu-id="a6082-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="a6082-122">Angiv "30" i feltet Dage forud.</span><span class="sxs-lookup"><span data-stu-id="a6082-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="a6082-123">Dette er det antal dage før beregningsdatoen af kanban-mængde, der er medtager i behovsberegningen.</span><span class="sxs-lookup"><span data-stu-id="a6082-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="a6082-124">Angiv "30" i feltet Dage bagud.</span><span class="sxs-lookup"><span data-stu-id="a6082-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="a6082-125">Dette er antallet af dage regnet fra den kanban-mængdeberegningsdato, der er medtaget i efterspørgselsberegningen.</span><span class="sxs-lookup"><span data-stu-id="a6082-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="a6082-126">Formlen bruges til beregningen vises med de faktiske værdier.</span><span class="sxs-lookup"><span data-stu-id="a6082-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="a6082-127">For eksempel, Kanban-mængde = ((gennemsnitlig daglig efterspørgsel x 2.00) + sikkerhedslager)/produktmængde pr. håndteringsenhed + 1</span><span class="sxs-lookup"><span data-stu-id="a6082-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="a6082-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a6082-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="a6082-129">Føj politikken til beregning af kanban-mængde til en kanban-regel</span><span class="sxs-lookup"><span data-stu-id="a6082-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="a6082-130">Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="a6082-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="a6082-131">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="a6082-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a6082-132">Vælg kanban-regel 000020 for denne procedure.</span><span class="sxs-lookup"><span data-stu-id="a6082-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="a6082-133">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a6082-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a6082-134">Slå udvidelse af sektionen Politikker for beregning af kanban-mængder til/fra.</span><span class="sxs-lookup"><span data-stu-id="a6082-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="a6082-135">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="a6082-135">Click Add.</span></span>
    * <span data-ttu-id="a6082-136">Tilføj politik for beregning af den kanban-mængde, du lige har oprettet i forrige underopgave.</span><span class="sxs-lookup"><span data-stu-id="a6082-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="a6082-137">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a6082-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="a6082-138">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a6082-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a6082-139">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a6082-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a6082-140">Vælg politikken, Speaker2016, du lige har oprettet i forrige underopgave.</span><span class="sxs-lookup"><span data-stu-id="a6082-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]