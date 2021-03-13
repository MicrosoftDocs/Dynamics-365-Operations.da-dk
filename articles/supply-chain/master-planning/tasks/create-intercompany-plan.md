---
title: Oprette en intern plan
description: Denne fremgangsmåde viser, hvordan du opretter en intern plan.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c368e461860a41d0110f5aed79c2aac49c437d68
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011396"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="5e6b7-103">Oprette en intern plan</span><span class="sxs-lookup"><span data-stu-id="5e6b7-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5e6b7-104">Denne fremgangsmåde viser, hvordan du opretter en intern plan.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="5e6b7-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="5e6b7-106">Konfigurer en intern planlægningsgruppe</span><span class="sxs-lookup"><span data-stu-id="5e6b7-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="5e6b7-107">Gå i **navigationsruden** til **Moduler > Varedisponering > Konfiguration > Interne planlægningsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="5e6b7-108">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5e6b7-109">For eksempel kan du filtrere på feltet Navn med værdien '10'.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="5e6b7-110">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="5e6b7-111">Klik på **Slet**.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-111">Click **Delete**.</span></span> <span data-ttu-id="5e6b7-112">Dette trin skal udføres for at afkorte kørslen af den interne varedisponering.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="5e6b7-113">Intern planlægning kører varedisponering i alle virksomheder i en planlægningsgruppe med start fra den laveste planlægningsrækkefølge.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="5e6b7-114">Klik på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-114">Click **Yes**.</span></span>
6. <span data-ttu-id="5e6b7-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="5e6b7-116">Oprette en intern plan</span><span class="sxs-lookup"><span data-stu-id="5e6b7-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="5e6b7-117">Gå i **navigationsruden** til **Moduler > Varedisponering > Arbejdsområder > Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="5e6b7-118">Klik på **Intern varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="5e6b7-119">Klik på rullelisten i feltet **Intern planlægningsgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5e6b7-120">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="5e6b7-121">Vælg intern planlægningsgruppe 10.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="5e6b7-122">Skriv '2' i feltet **Antal gentagelser af intern planlægning**.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="5e6b7-123">Den interne planlægningsgruppe 10 har to medlemmer.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="5e6b7-124">Hvis du vil overføre forsinkelserne fra kildefirmaet (USMF) til kundefirmaet (DEMF), skal du køre internt i begge firmaer to gange.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="5e6b7-125">Den første gentagelse fordeler behovet ud og identificerer forsinkelser i kildefirmaet (USMF).</span><span class="sxs-lookup"><span data-stu-id="5e6b7-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="5e6b7-126">Den anden gentagelse overfører forsinkelserne fra USMF til DEMF.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="5e6b7-127">Vælg 'Genopbygning' i feltet **Første gentagelse**.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="5e6b7-128">Vælg 'Genopbygning' i feltet **Efterfølgende gentagelser**.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="5e6b7-129">Indtast et antal i feltet **Antal tråde**.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="5e6b7-130">Dette repræsenterer antallet af parallelle tråde, der bruges til planlægning.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="5e6b7-131">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="5e6b7-132">Se resultatet af planen</span><span class="sxs-lookup"><span data-stu-id="5e6b7-132">View the result of the plan</span></span>
1. <span data-ttu-id="5e6b7-133">Klik på rullelisten i feltet **Plan** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="5e6b7-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="5e6b7-135">Klik på linket for StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="5e6b7-136">Du skal være i firmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="5e6b7-137">Klik på **Ordreforslag**.</span><span class="sxs-lookup"><span data-stu-id="5e6b7-137">Click **Planned orders**.</span></span>

