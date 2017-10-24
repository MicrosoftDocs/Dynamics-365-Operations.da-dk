--- 
title: Oprette en intern plan
description: "Denne fremgangsmåde viser, hvordan du opretter en intern plan."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: da186f7ad74bb607fd6e7220d77c2f414789f29c
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="e314b-103">Oprette en intern plan</span><span class="sxs-lookup"><span data-stu-id="e314b-103">Create an intercompany plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e314b-104">Denne fremgangsmåde viser, hvordan du opretter en intern plan.</span><span class="sxs-lookup"><span data-stu-id="e314b-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="e314b-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="e314b-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="e314b-106">Konfigurer en intern planlægningsgruppe</span><span class="sxs-lookup"><span data-stu-id="e314b-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="e314b-107">Gå til Interne planlægningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="e314b-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="e314b-108">Overordnet planlægning > Opsætning > Interne planlægningsgrupper</span><span class="sxs-lookup"><span data-stu-id="e314b-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="e314b-109">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="e314b-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e314b-110">For eksempel kan du filtrere på feltet Navn med værdien '10'.</span><span class="sxs-lookup"><span data-stu-id="e314b-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="e314b-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e314b-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e314b-112">Klik på Slet.</span><span class="sxs-lookup"><span data-stu-id="e314b-112">Click Delete.</span></span>
    * <span data-ttu-id="e314b-113">Dette trin skal udføres for at afkorte kørslen af den interne varedisponering.</span><span class="sxs-lookup"><span data-stu-id="e314b-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="e314b-114">Intern planlægning kører varedisponering i alle virksomheder i en planlægningsgruppe med start fra den laveste planlægningsrækkefølge.</span><span class="sxs-lookup"><span data-stu-id="e314b-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="e314b-115">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="e314b-115">Click Yes.</span></span>
6. <span data-ttu-id="e314b-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e314b-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="e314b-117">Oprette en intern plan</span><span class="sxs-lookup"><span data-stu-id="e314b-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="e314b-118">Klik på Intern varedisponering.</span><span class="sxs-lookup"><span data-stu-id="e314b-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="e314b-119">Det er i arbejdsområdet Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="e314b-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="e314b-120">Klik på rullelisten i feltet Intern planlægningsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="e314b-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e314b-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e314b-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e314b-122">Vælg intern planlægningsgruppe 10.</span><span class="sxs-lookup"><span data-stu-id="e314b-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="e314b-123">Skriv 2 i feltet Antal gentagelser af intern planlægning.</span><span class="sxs-lookup"><span data-stu-id="e314b-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="e314b-124">Den interne planlægningsgruppe 10 har to medlemmer.</span><span class="sxs-lookup"><span data-stu-id="e314b-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="e314b-125">Hvis du vil overføre forsinkelserne fra kildefirmaet (USMF) til kundefirmaet (DEMF), skal du køre internt i begge firmaer to gange.</span><span class="sxs-lookup"><span data-stu-id="e314b-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="e314b-126">Den første gentagelse fordeler behovet ud og identificerer forsinkelser i kildefirmaet (USMF).</span><span class="sxs-lookup"><span data-stu-id="e314b-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="e314b-127">Den anden gentagelse overfører forsinkelserne fra USMF til DEMF.</span><span class="sxs-lookup"><span data-stu-id="e314b-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="e314b-128">Vælg en indstilling i feltet Første gentagelse.</span><span class="sxs-lookup"><span data-stu-id="e314b-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="e314b-129">Vælg 'Genopbygning' i feltet Første gentagelse.</span><span class="sxs-lookup"><span data-stu-id="e314b-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="e314b-130">Vælg 'Genopbygning' i feltet Efterfølgende gentagelser.</span><span class="sxs-lookup"><span data-stu-id="e314b-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="e314b-131">Indtast et antal i feltet Antal tråde.</span><span class="sxs-lookup"><span data-stu-id="e314b-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="e314b-132">Dette repræsenterer antallet af parallelle tråde, der bruges til planlægning.</span><span class="sxs-lookup"><span data-stu-id="e314b-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="e314b-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e314b-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="e314b-134">Se resultatet af planen</span><span class="sxs-lookup"><span data-stu-id="e314b-134">View the result of the plan</span></span>
1. <span data-ttu-id="e314b-135">Klik på rullelisten i feltet Plan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="e314b-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="e314b-136">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e314b-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e314b-137">Klik på linket for StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="e314b-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="e314b-138">Du skal være i firmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="e314b-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="e314b-139">Klik på Ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="e314b-139">Click Planned orders.</span></span>


