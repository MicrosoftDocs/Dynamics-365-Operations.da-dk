---
title: Oprette et lukket spørgsmål
description: Lukkede spørgsmål giver dig mulighed at angive muligheder, som svarpersonen kan vælge fra.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2eb53290d39fef0bf439a199dfd774138823ec2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417870"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="be3e6-103">Oprette et lukket spørgsmål</span><span class="sxs-lookup"><span data-stu-id="be3e6-103">Create a closed ended question</span></span>



<span data-ttu-id="be3e6-104">Lukkede spørgsmål giver dig mulighed at angive muligheder, som svarpersonen kan vælge fra.</span><span class="sxs-lookup"><span data-stu-id="be3e6-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="be3e6-105">Først skal du oprette en Svarsamling med svarene, derefter skal du oprette spørgsmålet, som bruger svarsamlingen.</span><span class="sxs-lookup"><span data-stu-id="be3e6-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="be3e6-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="be3e6-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="be3e6-107">Opret en svarsamling</span><span class="sxs-lookup"><span data-stu-id="be3e6-107">Create an answer group</span></span>
1. <span data-ttu-id="be3e6-108">Gå til Spørgeskema > Design > Svarsamlinger.</span><span class="sxs-lookup"><span data-stu-id="be3e6-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="be3e6-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="be3e6-109">Click New.</span></span>
3. <span data-ttu-id="be3e6-110">Indtast en værdi i feltet Svarsamling.</span><span class="sxs-lookup"><span data-stu-id="be3e6-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="be3e6-111">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="be3e6-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="be3e6-112">Du kan bruge funktionen Tilfældig til at placere svarene i en tilfældig rækkefølge, hver gang svarsamlingen bruges til et spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="be3e6-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="be3e6-113">Klik på Svar.</span><span class="sxs-lookup"><span data-stu-id="be3e6-113">Click Answer.</span></span>
6. <span data-ttu-id="be3e6-114">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="be3e6-114">Click New.</span></span>
    * <span data-ttu-id="be3e6-115">Sekvensnummeret styrer den rækkefølge, som svarene vises i, medmindre Tilfældig vælges til svarsamlingen.</span><span class="sxs-lookup"><span data-stu-id="be3e6-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="be3e6-116">Point kan overdrages til svar til brug i vurdering af spørgeskemaet.</span><span class="sxs-lookup"><span data-stu-id="be3e6-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="be3e6-117">Angiv et tal i feltet Point.</span><span class="sxs-lookup"><span data-stu-id="be3e6-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="be3e6-118">Det rigtige svar kan markeres for at angive, at det valgte svar er korrekt.</span><span class="sxs-lookup"><span data-stu-id="be3e6-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="be3e6-119">Dette kan bruges til vurdering af spørgeskemaet.</span><span class="sxs-lookup"><span data-stu-id="be3e6-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="be3e6-120">Skriv en værdi i feltet Svar.</span><span class="sxs-lookup"><span data-stu-id="be3e6-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="be3e6-121">Fortsæt med at oprette valgmuligheder for svar til svarsamlingen.</span><span class="sxs-lookup"><span data-stu-id="be3e6-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="be3e6-122">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="be3e6-122">Click New.</span></span>
10. <span data-ttu-id="be3e6-123">Angiv et tal i feltet Point.</span><span class="sxs-lookup"><span data-stu-id="be3e6-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="be3e6-124">Skriv en værdi i feltet Svar.</span><span class="sxs-lookup"><span data-stu-id="be3e6-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="be3e6-125">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="be3e6-125">Click New.</span></span>
13. <span data-ttu-id="be3e6-126">Angiv et tal i feltet Point.</span><span class="sxs-lookup"><span data-stu-id="be3e6-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="be3e6-127">Skriv en værdi i feltet Svar.</span><span class="sxs-lookup"><span data-stu-id="be3e6-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="be3e6-128">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="be3e6-128">Click New.</span></span>
16. <span data-ttu-id="be3e6-129">Angiv et tal i feltet Point.</span><span class="sxs-lookup"><span data-stu-id="be3e6-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="be3e6-130">Skriv en værdi i feltet Svar.</span><span class="sxs-lookup"><span data-stu-id="be3e6-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="be3e6-131">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="be3e6-131">Click New.</span></span>
19. <span data-ttu-id="be3e6-132">Angiv et tal i feltet Point.</span><span class="sxs-lookup"><span data-stu-id="be3e6-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="be3e6-133">Skriv en værdi i feltet Svar.</span><span class="sxs-lookup"><span data-stu-id="be3e6-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="be3e6-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="be3e6-134">Close the page.</span></span>
22. <span data-ttu-id="be3e6-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="be3e6-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="be3e6-136">Opret spørgsmålet</span><span class="sxs-lookup"><span data-stu-id="be3e6-136">Create the question</span></span>
1. <span data-ttu-id="be3e6-137">Gå til Spørgeskema > Design > Spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="be3e6-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="be3e6-138">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="be3e6-138">Click New.</span></span>
3. <span data-ttu-id="be3e6-139">Brug feltet Type til at gruppere relaterede spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="be3e6-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="be3e6-140">Du kan bruge inputtyper som afkrydsningsfelt, alternativknap eller kombinationsboks til lukkede spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="be3e6-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="be3e6-141">Vælg en indstilling i feltet Inputtype.</span><span class="sxs-lookup"><span data-stu-id="be3e6-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="be3e6-142">Indtast eller vælg en værdi i feltet Svarsamling.</span><span class="sxs-lookup"><span data-stu-id="be3e6-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="be3e6-143">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="be3e6-143">In the Text field, type a value.</span></span>

