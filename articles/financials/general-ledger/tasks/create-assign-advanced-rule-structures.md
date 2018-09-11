--- 
title: Oprette og tildele avancerede regelstrukturer
description: "Denne opgaveguide gennemgår oprettelse og tildeling af en avanceret regelstruktur til en kontostruktur."
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: a371e2bd08ee3f65658e015990d46a430267add2
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="112d5-103">Oprette og tildele avancerede regelstrukturer</span><span class="sxs-lookup"><span data-stu-id="112d5-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="112d5-104">Denne opgaveguide gennemgår oprettelse og tildeling af en avanceret regelstruktur til en kontostruktur.</span><span class="sxs-lookup"><span data-stu-id="112d5-104">This task guide steps through creating and assigning an advanced rule structure to an account structure.</span></span> <span data-ttu-id="112d5-105">Denne guide anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="112d5-105">This guide uses the USMF demo company.</span></span>


## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="112d5-106">Opret en avanceret regelstruktur</span><span class="sxs-lookup"><span data-stu-id="112d5-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="112d5-107">Gå til Finans > Kontoplan > Strukturer > Avancerede regelstrukturer.</span><span class="sxs-lookup"><span data-stu-id="112d5-107">Go to General ledger > Chart of accounts > Structures > Advanced rule structures.</span></span>
2. <span data-ttu-id="112d5-108">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="112d5-108">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="112d5-109">I feltet Avanceret regelstruktur skal du skrive et navn, som beskriver regelstrukturen.</span><span class="sxs-lookup"><span data-stu-id="112d5-109">In the Advanced rule structure field, type a name to descritbe the rule structure.</span></span>
4. <span data-ttu-id="112d5-110">I feltet Beskrivelse skal du skrive en værdi for at beskrive strukturen.</span><span class="sxs-lookup"><span data-stu-id="112d5-110">In the Description field, type a value to describe the structure.</span></span>
5. <span data-ttu-id="112d5-111">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="112d5-111">Click OK.</span></span>
6. <span data-ttu-id="112d5-112">Klik på Tilføj segment.</span><span class="sxs-lookup"><span data-stu-id="112d5-112">Click Add segment.</span></span>
7. <span data-ttu-id="112d5-113">Listen over segmenter, skal du vælge en økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="112d5-113">In the list of segments, select a financial dimension.</span></span>
    * <span data-ttu-id="112d5-114">For eksempel Butik.</span><span class="sxs-lookup"><span data-stu-id="112d5-114">For example, Store.</span></span>  
8. <span data-ttu-id="112d5-115">Klik på Tilføj segment.</span><span class="sxs-lookup"><span data-stu-id="112d5-115">Click Add segment.</span></span>
9. <span data-ttu-id="112d5-116">Klik på linket til den avancerede regelstruktur for at få den vist.</span><span class="sxs-lookup"><span data-stu-id="112d5-116">In the list, click the link of the advanced rule structure to view it.</span></span>
10. <span data-ttu-id="112d5-117">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="112d5-117">Click Activate.</span></span>
11. <span data-ttu-id="112d5-118">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="112d5-118">Click Activate.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="112d5-119">Anvende en avanceret regelstruktur for en kontostruktur</span><span class="sxs-lookup"><span data-stu-id="112d5-119">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="112d5-120">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="112d5-120">Close the form.</span></span>
2. <span data-ttu-id="112d5-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="112d5-121">Close the page.</span></span>
3. <span data-ttu-id="112d5-122">Gå til Finans > Diagram over konti > Strukturer > Konfigurere kontostrukturer.</span><span class="sxs-lookup"><span data-stu-id="112d5-122">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
4. <span data-ttu-id="112d5-123">Søg på listen, og vælg den kontostruktur, som du vil anvende den avancerede regel for.</span><span class="sxs-lookup"><span data-stu-id="112d5-123">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
5. <span data-ttu-id="112d5-124">Klik på navnet på kontostrukturen for at åbne den.</span><span class="sxs-lookup"><span data-stu-id="112d5-124">Click the name of the account structure to open it.</span></span>
6. <span data-ttu-id="112d5-125">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="112d5-125">Click Edit.</span></span>
    * <span data-ttu-id="112d5-126">Du kan også klikke på Avancerede regler, hvorefter du bliver bedt om at sætte kontostrukturen i udkasttilstand.</span><span class="sxs-lookup"><span data-stu-id="112d5-126">You can also click Advanced rules and you will be prompted to put the account structure in Draft mode.</span></span>  
7. <span data-ttu-id="112d5-127">Klik på Avancerede regler.</span><span class="sxs-lookup"><span data-stu-id="112d5-127">Click Advanced rules.</span></span>
8. <span data-ttu-id="112d5-128">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="112d5-128">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="112d5-129">Skriv en værdi i feltet Avanceret regel.</span><span class="sxs-lookup"><span data-stu-id="112d5-129">In the Advanced rule field, type a value.</span></span>
10. <span data-ttu-id="112d5-130">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="112d5-130">In the Name field, type a value.</span></span>
11. <span data-ttu-id="112d5-131">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="112d5-131">Click Create.</span></span>
12. <span data-ttu-id="112d5-132">Klik på Tilføj nyt kriterie.</span><span class="sxs-lookup"><span data-stu-id="112d5-132">Click Add new criteria.</span></span>
13. <span data-ttu-id="112d5-133">Vælg hovedkontoen eller en økonomisk dimension i feltet Hvor.</span><span class="sxs-lookup"><span data-stu-id="112d5-133">In the Where field, select main account or a financial dimension.</span></span>
14. <span data-ttu-id="112d5-134">Vælg en indstilling i feltet Operatør, f.eks. er mellem og inkluderer.</span><span class="sxs-lookup"><span data-stu-id="112d5-134">In the Operator field, select an option, such as is between and includes.</span></span>
15. <span data-ttu-id="112d5-135">Skriv en værdi i feltet Værdi.</span><span class="sxs-lookup"><span data-stu-id="112d5-135">In the Value field, type a value.</span></span>
16. <span data-ttu-id="112d5-136">Skriv en værdi i feltet via.</span><span class="sxs-lookup"><span data-stu-id="112d5-136">In the through field, type a value.</span></span>
17. <span data-ttu-id="112d5-137">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="112d5-137">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="112d5-138">På listen, kan du finde den avancerede regelstruktur, som du vil bruge, når de kriterier, du har angivet, er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="112d5-138">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
19. <span data-ttu-id="112d5-139">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="112d5-139">Click Add.</span></span>
20. <span data-ttu-id="112d5-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="112d5-140">Close the page.</span></span>
21. <span data-ttu-id="112d5-141">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="112d5-141">Click Activate.</span></span>
22. <span data-ttu-id="112d5-142">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="112d5-142">Click Activate.</span></span>


