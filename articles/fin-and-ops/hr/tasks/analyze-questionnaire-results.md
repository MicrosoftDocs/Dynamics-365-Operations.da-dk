---
title: Analysere spørgeskemaresultater
description: Spørgeskemastatistik kan bruges til at beregne gennemsnit, totaler og procentdele baseret på en række demografiske data.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d8f9c2fcf0be117f8fcde5113c0d42f11786679
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/19/2019
ms.locfileid: "858577"
---
# <a name="analyzing-questionnaire-results"></a><span data-ttu-id="f2cfd-103">Analysere spørgeskemaresultater</span><span class="sxs-lookup"><span data-stu-id="f2cfd-103">Analyzing questionnaire results</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2cfd-104">Spørgeskemastatistik kan bruges til at beregne gennemsnit, totaler og procentdele baseret på en række demografiske data.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="f2cfd-105">Du begynder denne procedure ved at gå til Spørgeskema > Vis og analysér resultater > Spørgeskemastatistik.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="f2cfd-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="f2cfd-107">Opret en Spørgeskemastatistikpost</span><span class="sxs-lookup"><span data-stu-id="f2cfd-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="f2cfd-108">Gå til Spørgeskemastatistik.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="f2cfd-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-109">Click New.</span></span>
3. <span data-ttu-id="f2cfd-110">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f2cfd-111">Skriv en værdi i feltet Statistik.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="f2cfd-112">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="f2cfd-113">Klik på rullelisten i feltet Spørgeskema for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f2cfd-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f2cfd-115">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-115">Click the General tab.</span></span>
    * <span data-ttu-id="f2cfd-116">Vælg, hvis du vil medtage anonyme resultater eller resultater fra arbejdere, kontaktpersoner og ansøgere.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="f2cfd-117">Markér eller fjern markeringen i afkrydsningsfeltet Arbejder.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="f2cfd-118">Hvis du have vist resultaterne efter anciennitet eller alder, kan du angive de intervaller, som du vil bruge til at gruppere resultaterne.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="f2cfd-119">Angiv 5 for aldersintervallet for at gruppere resultaterne, så de er baseret på aldersintervaller a fem år.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="f2cfd-120">Angiv et tal i feltet Alder.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="f2cfd-121">Vælg, hvis du vil køre beregningen mod hele spørgeskemaet for hver resultatgruppe, for hvert spørgsmål eller for hver spørgsmålsrække.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="f2cfd-122">Vælg, hvordan du vil gruppere resultaterne.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="f2cfd-123">Hvis du f.eks. beregner det gennemsnitlige antal point pr. spørgsmål, kan du se de spørgsmål grupperet efter Resultatgruppe.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="f2cfd-124">Markér de data, du vil basere beregningen på.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="f2cfd-125">Hvis du f.eks. vil se den gennemsnitlige procentdel modtaget på spørgeskemaet på tværs af dine arbejderne i forhold til det gennemsnitlige antal point, der er opnået på tværs af dine medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="f2cfd-126">Klik på fanen Område.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-126">Click the Range tab.</span></span>
    * <span data-ttu-id="f2cfd-127">Du kan bruge intervaller til at indsnævre resultatsættet til kun dem, der opfylder kriterierne for området.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="f2cfd-128">Klik på fanen Gruppering pr.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="f2cfd-129">Brug Grupperinger til at finde ud af, hvordan resultatet skal vises.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="f2cfd-130">Gruppér f.eks resultaterne først efter køn, derpå efter alder.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="f2cfd-131">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f2cfd-132">Flyt grupperinger ind på den markerede side, og placer dem i den ønskede rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="f2cfd-133">Udfør statistikberegningen.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="f2cfd-134">Klik på Udfør.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-134">Click Execute.</span></span>
    * <span data-ttu-id="f2cfd-135">Vælg, hvilken beregningsfunktion du vil udføre på resultaterne.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="f2cfd-136">Du kan f.eks. beregne de gennemsnitlige procentsatser på tværs af spørgeskemaet for de valgte grupperinger eller det samlede antal point på tværs af resultatgrupper for de valgte grupperinger.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="f2cfd-137">Markér eller fjern markeringen i afkrydsningsfeltet Slet tidligere søgninger.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="f2cfd-138">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="f2cfd-139">Få vist resultaterne af kørslen af spørgeskemastatistikken.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="f2cfd-140">Klik på Resultat.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-140">Click Result.</span></span>
2. <span data-ttu-id="f2cfd-141">Klik på Resultat.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-141">Click Result.</span></span>
3. <span data-ttu-id="f2cfd-142">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f2cfd-142">Close the page.</span></span>

