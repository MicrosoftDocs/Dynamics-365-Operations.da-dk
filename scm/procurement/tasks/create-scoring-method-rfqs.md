--- 
title: Oprette en scoremetode for tilbudsanmodninger
description: Denne procedure viser, hvordan du opretter en scoremetode.
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6d72678db60254801c6c899f4d405f1c59de8d65
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="f9c61-103">Oprette en scoremetode for tilbudsanmodninger</span><span class="sxs-lookup"><span data-stu-id="f9c61-103">Create a scoring method for RFQs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9c61-104">Denne procedure viser, hvordan du opretter en scoremetode.</span><span class="sxs-lookup"><span data-stu-id="f9c61-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="f9c61-105">En scoremetode er et sæt af kriterier, der kan bruges til at sammenligne tilbud, der sendes som svar på en tilbudsanmodning.</span><span class="sxs-lookup"><span data-stu-id="f9c61-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="f9c61-106">Det kan f.eks. være, at du vil vurdere en kreditor på dennes tidligere resultater, vurdere, om firmaet er miljøvenligt eller en god samarbejdspartner, eller du vil måske sammenligne bud baseret på pris.</span><span class="sxs-lookup"><span data-stu-id="f9c61-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="f9c61-107">Scoremetoden kan være knyttet til en anmodningstype som standardscoremetode for tilbudsanmodninger af den pågældende type.</span><span class="sxs-lookup"><span data-stu-id="f9c61-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="f9c61-108">Disse opgaver udføres normalt af en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="f9c61-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="f9c61-109">Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="f9c61-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="f9c61-110">Gå til Indkøb og forsyning > Opsætning > Tilbudsanmodning > Scoremetode.</span><span class="sxs-lookup"><span data-stu-id="f9c61-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="f9c61-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f9c61-111">Click New.</span></span>
3. <span data-ttu-id="f9c61-112">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="f9c61-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f9c61-113">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f9c61-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f9c61-114">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f9c61-114">Click Save.</span></span>
6. <span data-ttu-id="f9c61-115">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f9c61-115">Click New.</span></span>
7. <span data-ttu-id="f9c61-116">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="f9c61-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="f9c61-117">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f9c61-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="f9c61-118">Denne beskrivelse vises sammen med navnet på scoremetoden, når der er valgt en scoremetode for en tilbudsanmodning.</span><span class="sxs-lookup"><span data-stu-id="f9c61-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="f9c61-119">Angiv et tal i feltet Interval fra.</span><span class="sxs-lookup"><span data-stu-id="f9c61-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="f9c61-120">Det område, inden for hvilket anmoderen kan angive en score.</span><span class="sxs-lookup"><span data-stu-id="f9c61-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="f9c61-121">Når der er flere scorekriterier på en tilbudsanmodning, føjes de scores, der er angivet, til hinanden, og summen er tilgængelig, så buddene kan sammenlignes.</span><span class="sxs-lookup"><span data-stu-id="f9c61-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="f9c61-122">Angiv et tal i feltet Interval til.</span><span class="sxs-lookup"><span data-stu-id="f9c61-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="f9c61-123">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f9c61-123">Click New.</span></span>
12. <span data-ttu-id="f9c61-124">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="f9c61-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="f9c61-125">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f9c61-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="f9c61-126">Angiv et tal i feltet Interval fra.</span><span class="sxs-lookup"><span data-stu-id="f9c61-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="f9c61-127">Angiv et tal i feltet Interval til.</span><span class="sxs-lookup"><span data-stu-id="f9c61-127">In the Range to field, enter a number.</span></span>


