--- 
title: Konfigurere standardomkostninger for arbejdskraft og udgifter
description: Denne procedure viser, hvordan du konfigurerer standardomkostninger for arbejdskraft og udgifter for et projekt.
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 432b5b195b29fb03786cb0560e277735b531b7d7
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="5a1f7-103">Konfigurere standardomkostninger for arbejdskraft og udgifter</span><span class="sxs-lookup"><span data-stu-id="5a1f7-103">Configure standard costs for labor and expenses</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5a1f7-104">Denne procedure viser, hvordan du konfigurerer standardomkostninger for arbejdskraft og udgifter for et projekt.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="5a1f7-105">Denne opgave bruger USSI-datasættet.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="5a1f7-106">Gå til Projektstyring og regnskab > Opsætning > Priser > Salgspris (time).</span><span class="sxs-lookup"><span data-stu-id="5a1f7-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="5a1f7-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-107">Click New.</span></span>
3. <span data-ttu-id="5a1f7-108">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="5a1f7-109">Angiv et tal i feltet Kostpris.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="5a1f7-110">Du kan definere en standardkostpris for projektkategorien, eller du kan definere en kostpris pr. arbejdernummer, projektnummer, kategori, dato eller en kombination af disse.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="5a1f7-111">Den kostpris, der anvendes, vil være den mest detaljerede kostpris.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="5a1f7-112">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-112">Click Save.</span></span>
6. <span data-ttu-id="5a1f7-113">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-113">Close the page.</span></span>
7. <span data-ttu-id="5a1f7-114">Gå til Projektstyring og regnskab > Opsætning > Priser > Salgspris (time).</span><span class="sxs-lookup"><span data-stu-id="5a1f7-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="5a1f7-115">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-115">Click New.</span></span>
9. <span data-ttu-id="5a1f7-116">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="5a1f7-117">Vælg en indstilling i feltet Gyldig.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="5a1f7-118">Angiv et tal i feltet Prissætning.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="5a1f7-119">Du kan definere en standardsalgspris for timeposteringer eller for en projektkategori.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="5a1f7-120">Du kan også definere salgspriser pr. arbejdernummer, projektnummer, kategori, posteringsdato eller en kombination af disse.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="5a1f7-121">Den faktiske salgspris, som anvendes, når en arbejder angiver en postering i timekladden, er salgsprisen med den højeste detaljeringsgrad.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="5a1f7-122">Hvis der f.eks. både er oprettet en generel salgspris og en arbejderspecifik salgspris, bruges den arbejderspecifikke salgspris.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="5a1f7-123">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-123">Click Save.</span></span>
13. <span data-ttu-id="5a1f7-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-124">Close the page.</span></span>
14. <span data-ttu-id="5a1f7-125">Gå til Projektstyring og regnskab > Opsætning > Priser > Kostpris (udgift).</span><span class="sxs-lookup"><span data-stu-id="5a1f7-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="5a1f7-126">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-126">Click New.</span></span>
16. <span data-ttu-id="5a1f7-127">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="5a1f7-128">Angiv et tal i feltet Kostpris.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="5a1f7-129">Der kan udfyldes flere felter, men dette er det minimum, der er nødvendigt for at gemme posten.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="5a1f7-130">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-130">Click Save.</span></span>
19. <span data-ttu-id="5a1f7-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-131">Close the page.</span></span>
20. <span data-ttu-id="5a1f7-132">Gå til Projektstyring og regnskab > Opsætning > Priser > Salgspris (udgift).</span><span class="sxs-lookup"><span data-stu-id="5a1f7-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="5a1f7-133">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-133">Click New.</span></span>
22. <span data-ttu-id="5a1f7-134">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="5a1f7-135">Vælg en indstilling i feltet Gyldig.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="5a1f7-136">Angiv et tal i feltet Prissætning.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="5a1f7-137">Den faktiske salgspris, som anvendes, når en medarbejder angiver posteringer i en udgiftskladde, er den salgspris, der har det højeste detaljeringsniveau.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="5a1f7-138">Hvis der f.eks. både er oprettet en generel salgspris og en arbejderspecifik salgspris, anvendes den arbejderspecifikke salgspris.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="5a1f7-139">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="5a1f7-139">Click Save.</span></span>


