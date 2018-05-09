--- 
title: "Konfigurere politikker for indkøbskategorihierarkier"
description: "Brug denne fremgangsmåde til at oprette regler for bestilling af produkter i en kategori."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f98f5b578c1d01463d196b6018e9f47a9d924be7
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="0de50-103">Konfigurere politikker for indkøbskategorihierarkier</span><span class="sxs-lookup"><span data-stu-id="0de50-103">Set up policies for procurement category hierarchies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0de50-104">Brug denne fremgangsmåde til at oprette regler for bestilling af produkter i en kategori.</span><span class="sxs-lookup"><span data-stu-id="0de50-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="0de50-105">Reglerne er defineret for en bestemt indkøbspolitik.</span><span class="sxs-lookup"><span data-stu-id="0de50-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="0de50-106">Kategoriadgangspolitikreglen styrer, hvilke indkøbskategorier medarbejdere har adgang til, når de opretter en indkøbsrekvisition.</span><span class="sxs-lookup"><span data-stu-id="0de50-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="0de50-107">Når der oprettes en indkøbsrekvisition, afgøres den indkøbspolitik og den regel for kategoriadgang, der skal anvendes, af den juridiske enhed og den driftsenhed, som medarbejderen tilhører.</span><span class="sxs-lookup"><span data-stu-id="0de50-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="0de50-108">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="0de50-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="0de50-109">Denne opgave vil typisk blive udført af en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="0de50-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="0de50-110">Find politikken for indkøb</span><span class="sxs-lookup"><span data-stu-id="0de50-110">Find the procurement policy</span></span>
1. <span data-ttu-id="0de50-111">Gå til Indkøb og forsyning > Konfiguration > Politikker > Indkøbspolitikker.</span><span class="sxs-lookup"><span data-stu-id="0de50-111">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="0de50-112">Klik på linket i indkøbspolitikkens USMF-politik.</span><span class="sxs-lookup"><span data-stu-id="0de50-112">Click the link on the Procurement Policy USMF policy.</span></span>
    * <span data-ttu-id="0de50-113">Det er den politik, som du vil føje en regel til.</span><span class="sxs-lookup"><span data-stu-id="0de50-113">This is the policy that you’ll add a rule to.</span></span> <span data-ttu-id="0de50-114">Det skal være en aktiv politik.</span><span class="sxs-lookup"><span data-stu-id="0de50-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="0de50-115">Oprette en regel for adgang til kategori</span><span class="sxs-lookup"><span data-stu-id="0de50-115">Create a category access rule</span></span>
1. <span data-ttu-id="0de50-116">Vælg reglen for adgang til kategori.</span><span class="sxs-lookup"><span data-stu-id="0de50-116">Select the Category access policy rule.</span></span>
    * <span data-ttu-id="0de50-117">Hvis knappen Opret politikregel er nedtonet, skyldes det, at der allerede findes en aktiv politikregel for kategoriadgang.</span><span class="sxs-lookup"><span data-stu-id="0de50-117">If the Create policy rule button is dimmed, it’s because there’s already an active policy rule for Category access.</span></span> <span data-ttu-id="0de50-118">Kontrollér felterne Ikrafttrædelsesdato og Udløbsdato for at finde ud af, hvad reglen er, markér den derefter, og klik på Træk regel tilbage.</span><span class="sxs-lookup"><span data-stu-id="0de50-118">Check the Effective and Expiration date fields to determine which it is, then select it, and click Retire policy rule.</span></span> <span data-ttu-id="0de50-119">Hvis knappen Opret politikregel er tilgængelig, skal du ikke gøre noget.</span><span class="sxs-lookup"><span data-stu-id="0de50-119">If the Create policy rule button is available, you don’t need to do anything.</span></span>  
2. <span data-ttu-id="0de50-120">Klik på Opret politikregel.</span><span class="sxs-lookup"><span data-stu-id="0de50-120">Click Create policy rule.</span></span>
3. <span data-ttu-id="0de50-121">Angiv en dato og et klokkeslæt i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="0de50-121">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="0de50-122">Tiden må ikke overlappe med en anden regel, der allerede er aktiv.</span><span class="sxs-lookup"><span data-stu-id="0de50-122">The time must not overlap with another rule that’s already active.</span></span>  
    * <span data-ttu-id="0de50-123">Vælg en kategori, som reglen skal gælde for.</span><span class="sxs-lookup"><span data-stu-id="0de50-123">Select a category that the rule will apply to.</span></span> <span data-ttu-id="0de50-124">Notér, hvilken kategori det er – du skal bruge den senere.</span><span class="sxs-lookup"><span data-stu-id="0de50-124">Make a note of which category this is – you’ll need it later.</span></span> <span data-ttu-id="0de50-125">Når du vælger en kategori, tilføjes den eller de tilhørende overordnede kategorier også på listen Valgte kategorier.</span><span class="sxs-lookup"><span data-stu-id="0de50-125">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span>  
    * <span data-ttu-id="0de50-126">Hvis reglen skal anvendes på alle underkategorier af den valgte kategori, skal du markere afkrydsningsfeltet Medtag underkategorier.</span><span class="sxs-lookup"><span data-stu-id="0de50-126">If you want the rule to apply to all subcategories of the selected category, select the Include subcategories check box.</span></span>  
4. <span data-ttu-id="0de50-127">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="0de50-127">Click Add.</span></span>
    * <span data-ttu-id="0de50-128">Hvis du angiver indstillingen Medtag overordnet regel til Ja, tildeles den politikregel, du definerer for en overordnet kategori, også til dens underordnede kategorier, hvis der ikke er defineret en politikregel for de underordnede kategorier.</span><span class="sxs-lookup"><span data-stu-id="0de50-128">If you set the Include parent rule option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>  
5. <span data-ttu-id="0de50-129">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0de50-129">Click OK.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="0de50-130">Oprette en politikregel for kategori.</span><span class="sxs-lookup"><span data-stu-id="0de50-130">Create a category policy rule</span></span>
1. <span data-ttu-id="0de50-131">Vælg reglen for kategori</span><span class="sxs-lookup"><span data-stu-id="0de50-131">Select the Category policy rule</span></span>
    * <span data-ttu-id="0de50-132">Hvis knappen Opret politikregel er nedtonet, skal du vælge den aktive politikregel og derefter klikke på Træk regel tilbage.</span><span class="sxs-lookup"><span data-stu-id="0de50-132">If the Create policy rule button is dimmed, select the active policy rule, and then click Retire policy rule.</span></span>  
2. <span data-ttu-id="0de50-133">Klik på Opret politikregel.</span><span class="sxs-lookup"><span data-stu-id="0de50-133">Click Create policy rule.</span></span>
3. <span data-ttu-id="0de50-134">Angiv en dato og et klokkeslæt i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="0de50-134">In the Effective date field, enter a date and time.</span></span>
4. <span data-ttu-id="0de50-135">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="0de50-135">Click Add.</span></span>
5. <span data-ttu-id="0de50-136">Vælg den samme kategori, du har brugt til reglen for kategoriadgang.</span><span class="sxs-lookup"><span data-stu-id="0de50-136">Select the same category that you used for the Category access rule.</span></span>
6. <span data-ttu-id="0de50-137">Vælg en indstilling i feltet Kreditorvalg.</span><span class="sxs-lookup"><span data-stu-id="0de50-137">In the Vendor selection field, select an option.</span></span>
    * <span data-ttu-id="0de50-138">Vælg en regel, der skal styre, hvilken slags kreditorer der kan vælges til kategorien, når der oprettes indkøbsrekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="0de50-138">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="0de50-139">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="0de50-139">Click Close.</span></span>
    * <span data-ttu-id="0de50-140">De politikregler, du har defineret, har været for indkøbsrekvisitionen af typen Forbrug.</span><span class="sxs-lookup"><span data-stu-id="0de50-140">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="0de50-141">Hvis du vil definere politikker for indkøbsrekvisitioner af typen Opfyldning, skal du oprette en regel for politikregeltypen kaldet "Regel for adgang til genopfyldningskategori".</span><span class="sxs-lookup"><span data-stu-id="0de50-141">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called “Replenishment category access policy rule”.</span></span>  


