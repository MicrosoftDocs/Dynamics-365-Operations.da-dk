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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2b8a896c764e26c6fbb13714932d7652bf6ddc09
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="07953-103">Konfigurere standardomkostninger for arbejdskraft og udgifter</span><span class="sxs-lookup"><span data-stu-id="07953-103">Configure standard costs for labor and expenses</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="07953-104">Denne procedure viser, hvordan du konfigurerer standardomkostninger for arbejdskraft og udgifter for et projekt.</span><span class="sxs-lookup"><span data-stu-id="07953-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="07953-105">Denne opgave bruger USSI-datasættet.</span><span class="sxs-lookup"><span data-stu-id="07953-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="07953-106">Gå til Projektstyring og regnskab > Opsætning > Priser > Salgspris (time).</span><span class="sxs-lookup"><span data-stu-id="07953-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="07953-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="07953-107">Click New.</span></span>
3. <span data-ttu-id="07953-108">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="07953-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="07953-109">Angiv et tal i feltet Kostpris.</span><span class="sxs-lookup"><span data-stu-id="07953-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="07953-110">Du kan definere en standardkostpris for projektkategorien, eller du kan definere en kostpris pr. arbejdernummer, projektnummer, kategori, dato eller en kombination af disse.</span><span class="sxs-lookup"><span data-stu-id="07953-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="07953-111">Den kostpris, der anvendes, vil være den mest detaljerede kostpris.</span><span class="sxs-lookup"><span data-stu-id="07953-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="07953-112">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="07953-112">Click Save.</span></span>
6. <span data-ttu-id="07953-113">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="07953-113">Close the page.</span></span>
7. <span data-ttu-id="07953-114">Gå til Projektstyring og regnskab > Opsætning > Priser > Salgspris (time).</span><span class="sxs-lookup"><span data-stu-id="07953-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="07953-115">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="07953-115">Click New.</span></span>
9. <span data-ttu-id="07953-116">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="07953-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="07953-117">Vælg en indstilling i feltet Gyldig.</span><span class="sxs-lookup"><span data-stu-id="07953-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="07953-118">Angiv et tal i feltet Prissætning.</span><span class="sxs-lookup"><span data-stu-id="07953-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="07953-119">Du kan definere en standardsalgspris for timeposteringer eller for en projektkategori.</span><span class="sxs-lookup"><span data-stu-id="07953-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="07953-120">Du kan også definere salgspriser pr. arbejdernummer, projektnummer, kategori, posteringsdato eller en kombination af disse.</span><span class="sxs-lookup"><span data-stu-id="07953-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="07953-121">Den faktiske salgspris, som anvendes, når en arbejder angiver en postering i timekladden, er salgsprisen med den højeste detaljeringsgrad.</span><span class="sxs-lookup"><span data-stu-id="07953-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="07953-122">Hvis der f.eks. både er oprettet en generel salgspris og en arbejderspecifik salgspris, bruges den arbejderspecifikke salgspris.</span><span class="sxs-lookup"><span data-stu-id="07953-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="07953-123">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="07953-123">Click Save.</span></span>
13. <span data-ttu-id="07953-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="07953-124">Close the page.</span></span>
14. <span data-ttu-id="07953-125">Gå til Projektstyring og regnskab > Opsætning > Priser > Kostpris (udgift).</span><span class="sxs-lookup"><span data-stu-id="07953-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="07953-126">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="07953-126">Click New.</span></span>
16. <span data-ttu-id="07953-127">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="07953-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="07953-128">Angiv et tal i feltet Kostpris.</span><span class="sxs-lookup"><span data-stu-id="07953-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="07953-129">Der kan udfyldes flere felter, men dette er det minimum, der er nødvendigt for at gemme posten.</span><span class="sxs-lookup"><span data-stu-id="07953-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="07953-130">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="07953-130">Click Save.</span></span>
19. <span data-ttu-id="07953-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="07953-131">Close the page.</span></span>
20. <span data-ttu-id="07953-132">Gå til Projektstyring og regnskab > Opsætning > Priser > Salgspris (udgift).</span><span class="sxs-lookup"><span data-stu-id="07953-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="07953-133">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="07953-133">Click New.</span></span>
22. <span data-ttu-id="07953-134">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="07953-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="07953-135">Vælg en indstilling i feltet Gyldig.</span><span class="sxs-lookup"><span data-stu-id="07953-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="07953-136">Angiv et tal i feltet Prissætning.</span><span class="sxs-lookup"><span data-stu-id="07953-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="07953-137">Den faktiske salgspris, som anvendes, når en medarbejder angiver posteringer i en udgiftskladde, er den salgspris, der har det højeste detaljeringsniveau.</span><span class="sxs-lookup"><span data-stu-id="07953-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="07953-138">Hvis der f.eks. både er oprettet en generel salgspris og en arbejderspecifik salgspris, anvendes den arbejderspecifikke salgspris.</span><span class="sxs-lookup"><span data-stu-id="07953-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="07953-139">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="07953-139">Click Save.</span></span>


