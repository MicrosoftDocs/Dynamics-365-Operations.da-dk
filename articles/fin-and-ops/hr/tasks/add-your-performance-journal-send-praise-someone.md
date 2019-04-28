---
title: Tilføje til performancekladde og sende ros til en person
description: Performancekladden indeholder oplysninger, der vedrører, hvordan du har opfyldt dine mål, eller hvordan du har performet i en periode.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EssWorkspace, HcmPerfJournal, HcmPerfJournalAddLink, HcmPerfPraise, HcmWorkerLookUpByPerson, HcmPerfJournalAdd
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f2f8e0e858a27bec09eee6f7f02dc952fe8e408
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/19/2019
ms.locfileid: "856456"
---
# <a name="add-to-your-performance-journal-and-send-praise-to-someone"></a><span data-ttu-id="8f1b1-103">Tilføje til performancekladde og sende ros til en person</span><span class="sxs-lookup"><span data-stu-id="8f1b1-103">Add to your performance journal and send praise to someone</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8f1b1-104">Performancekladden indeholder oplysninger, der vedrører, hvordan du har opfyldt dine mål, eller hvordan du har performet i en periode.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-104">The performance journal holds information that relates to how you met your goals or how you performed during a period.</span></span> <span data-ttu-id="8f1b1-105">Du kan også rose handlinger udført af en kollega fra kladden.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-105">You can also praise the actions of a co-worker from the journal.</span></span> <span data-ttu-id="8f1b1-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8f1b1-107">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="8f1b1-108">Gå til Alle arbejdsområder > Medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-108">Go to All workspaces > Employee self service.</span></span>
2. <span data-ttu-id="8f1b1-109">Klik på Performancekladde.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-109">Click Performance journal.</span></span>
3. <span data-ttu-id="8f1b1-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-110">Click New.</span></span>
4. <span data-ttu-id="8f1b1-111">Skriv en værdi i feltet Titel.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-111">In the Title field, type a value.</span></span>
5. <span data-ttu-id="8f1b1-112">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="8f1b1-113">Datoen for performancekladden er den dato, kladden blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-113">The performance journal date is the date that the journal was created.</span></span>  
    * <span data-ttu-id="8f1b1-114">Kilden repræsenterer, hvor performancekladden kom fra.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-114">The source represents where the performance journal came from.</span></span> <span data-ttu-id="8f1b1-115">Når du opretter en, kommer den fra Min kladde.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-115">When you create one, it comes from My journal.</span></span> <span data-ttu-id="8f1b1-116">Hvis projektlederen opretter en, kommer det fra Lederkladde.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-116">If your manager creates one, it comes from the Manager journal.</span></span>  
    * <span data-ttu-id="8f1b1-117">Du kan dele denne kladde med din leder eller kun gøre den synlig for dig.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-117">You can share this journal with your manager or make it only visible to you.</span></span>  
6. <span data-ttu-id="8f1b1-118">Angiv en dato i feltet Startdato.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-118">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="8f1b1-119">Indtast en dato i feltet Kompileret dato.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-119">In the Date completed field, enter a date.</span></span>
8. <span data-ttu-id="8f1b1-120">Vælg Ja i feltet Udviklingsplan.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-120">Select Yes in the Development plan field.</span></span>
9. <span data-ttu-id="8f1b1-121">Skriv en værdi i feltet Nøgleord.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-121">In the Keywords field, type a value.</span></span>
10. <span data-ttu-id="8f1b1-122">Klik på Tilføj eksternt link.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-122">Click Add external link.</span></span>
11. <span data-ttu-id="8f1b1-123">Skriv 'Envision' i feltet 'Beskrivelse'.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-123">In the Description field, type 'Envision'.</span></span>
12. <span data-ttu-id="8f1b1-124">Indtast 'https://www.microsoft.com/en/envision/default' i feltet Internetadresse.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-124">In the Internet address field, type 'https://www.microsoft.com/en/envision/default'.</span></span>
13. <span data-ttu-id="8f1b1-125">Klik på titelteksten under knappen Gem kaldet "Performancejournal" for at vende tilbage til gitteret.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-125">Click on the caption below the Save button called "Performance journal" to return to the grid.</span></span>
    * <span data-ttu-id="8f1b1-126">Du kan føje den eller de valgte kladder til et mål, så det vises, når du åbner målet.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-126">You can add the selected journal or journals to a goal so that it appears when you open the goal.</span></span> <span data-ttu-id="8f1b1-127">Der tilføjes et link på hurtigfanen Links. Hvis du føjer en kladde til et mål og derefter føjer målet til en evaluering, vises kladden automatisk i evalueringen.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-127">A link will be added in the Links fast tab.    If you add a journal to a goal and then add the goal to a review, the journal will appear on the review automatically.</span></span>  
    * <span data-ttu-id="8f1b1-128">Du kan føje den eller de valgte kladder til en evaluering så det vises, når du åbner evalueringen.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-128">You can add the selected journal or journals to a review so that it appears when you open the review.</span></span>    <span data-ttu-id="8f1b1-129">I oversigtspanelet Links tilføjes der et link.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-129">A link will be added in the Links fast tab.</span></span>  
14. <span data-ttu-id="8f1b1-130">Klik på Tilføj hurtigt.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-130">Click Quick add.</span></span>
15. <span data-ttu-id="8f1b1-131">Skriv en værdi i feltet Titel.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-131">In the Title field, type a value.</span></span>
16. <span data-ttu-id="8f1b1-132">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-132">In the Description field, type a value.</span></span>
17. <span data-ttu-id="8f1b1-133">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-133">Click Save.</span></span>
18. <span data-ttu-id="8f1b1-134">Klik på Send ros.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-134">Click Send praise.</span></span>
19. <span data-ttu-id="8f1b1-135">Vælg en person på listen over medarbejdere i firmaet.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-135">Select a person from the list of employees in the company.</span></span>
20. <span data-ttu-id="8f1b1-136">Skriv 'Tak for hjælpen på konferencen!' i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-136">In the Description field, enter 'Thanks for all the help at the conference!'.</span></span>
21. <span data-ttu-id="8f1b1-137">Klik på Send.</span><span class="sxs-lookup"><span data-stu-id="8f1b1-137">Click Send.</span></span>

