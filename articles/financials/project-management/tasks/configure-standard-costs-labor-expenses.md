---
title: Konfigurere standardomkostninger for arbejdskraft og udgifter
description: Denne procedure viser, hvordan du konfigurerer standardomkostninger for arbejdskraft og udgifter for et projekt.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f89590c87aec1a7200e95aeac6b2765fc64bb623
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "339389"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="c4923-103">Konfigurere standardomkostninger for arbejdskraft og udgifter</span><span class="sxs-lookup"><span data-stu-id="c4923-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4923-104">Denne procedure viser, hvordan du konfigurerer standardomkostninger for arbejdskraft og udgifter for et projekt.</span><span class="sxs-lookup"><span data-stu-id="c4923-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="c4923-105">Denne opgave bruger USSI-datasættet.</span><span class="sxs-lookup"><span data-stu-id="c4923-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="c4923-106">Gå til Projektstyring og regnskab > Opsætning > Priser > Salgspris (time).</span><span class="sxs-lookup"><span data-stu-id="c4923-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="c4923-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c4923-107">Click New.</span></span>
3. <span data-ttu-id="c4923-108">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="c4923-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="c4923-109">Angiv et tal i feltet Kostpris.</span><span class="sxs-lookup"><span data-stu-id="c4923-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="c4923-110">Du kan definere en standardkostpris for projektkategorien, eller du kan definere en kostpris pr. arbejdernummer, projektnummer, kategori, dato eller en kombination af disse.</span><span class="sxs-lookup"><span data-stu-id="c4923-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="c4923-111">Den kostpris, der anvendes, vil være den mest detaljerede kostpris.</span><span class="sxs-lookup"><span data-stu-id="c4923-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="c4923-112">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c4923-112">Click Save.</span></span>
6. <span data-ttu-id="c4923-113">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c4923-113">Close the page.</span></span>
7. <span data-ttu-id="c4923-114">Gå til Projektstyring og regnskab > Opsætning > Priser > Salgspris (time).</span><span class="sxs-lookup"><span data-stu-id="c4923-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="c4923-115">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c4923-115">Click New.</span></span>
9. <span data-ttu-id="c4923-116">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="c4923-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="c4923-117">Vælg en indstilling i feltet Gyldig.</span><span class="sxs-lookup"><span data-stu-id="c4923-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="c4923-118">Angiv et tal i feltet Prissætning.</span><span class="sxs-lookup"><span data-stu-id="c4923-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="c4923-119">Du kan definere en standardsalgspris for timeposteringer eller for en projektkategori.</span><span class="sxs-lookup"><span data-stu-id="c4923-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="c4923-120">Du kan også definere salgspriser pr. arbejdernummer, projektnummer, kategori, posteringsdato eller en kombination af disse.</span><span class="sxs-lookup"><span data-stu-id="c4923-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="c4923-121">Den faktiske salgspris, som anvendes, når en arbejder angiver en postering i timekladden, er salgsprisen med den højeste detaljeringsgrad.</span><span class="sxs-lookup"><span data-stu-id="c4923-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="c4923-122">Hvis der f.eks. både er oprettet en generel salgspris og en arbejderspecifik salgspris, bruges den arbejderspecifikke salgspris.</span><span class="sxs-lookup"><span data-stu-id="c4923-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="c4923-123">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c4923-123">Click Save.</span></span>
13. <span data-ttu-id="c4923-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c4923-124">Close the page.</span></span>
14. <span data-ttu-id="c4923-125">Gå til Projektstyring og regnskab > Opsætning > Priser > Kostpris (udgift).</span><span class="sxs-lookup"><span data-stu-id="c4923-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="c4923-126">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c4923-126">Click New.</span></span>
16. <span data-ttu-id="c4923-127">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="c4923-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="c4923-128">Angiv et tal i feltet Kostpris.</span><span class="sxs-lookup"><span data-stu-id="c4923-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="c4923-129">Der kan udfyldes flere felter, men dette er det minimum, der er nødvendigt for at gemme posten.</span><span class="sxs-lookup"><span data-stu-id="c4923-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="c4923-130">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c4923-130">Click Save.</span></span>
19. <span data-ttu-id="c4923-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c4923-131">Close the page.</span></span>
20. <span data-ttu-id="c4923-132">Gå til Projektstyring og regnskab > Opsætning > Priser > Salgspris (udgift).</span><span class="sxs-lookup"><span data-stu-id="c4923-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="c4923-133">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c4923-133">Click New.</span></span>
22. <span data-ttu-id="c4923-134">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="c4923-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="c4923-135">Vælg en indstilling i feltet Gyldig.</span><span class="sxs-lookup"><span data-stu-id="c4923-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="c4923-136">Angiv et tal i feltet Prissætning.</span><span class="sxs-lookup"><span data-stu-id="c4923-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="c4923-137">Den faktiske salgspris, som anvendes, når en medarbejder angiver posteringer i en udgiftskladde, er den salgspris, der har det højeste detaljeringsniveau.</span><span class="sxs-lookup"><span data-stu-id="c4923-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="c4923-138">Hvis der f.eks. både er oprettet en generel salgspris og en arbejderspecifik salgspris, anvendes den arbejderspecifikke salgspris.</span><span class="sxs-lookup"><span data-stu-id="c4923-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="c4923-139">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c4923-139">Click Save.</span></span>

