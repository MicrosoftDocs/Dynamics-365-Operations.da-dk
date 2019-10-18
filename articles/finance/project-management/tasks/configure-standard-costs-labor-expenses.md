---
title: Konfigurere standardomkostninger for arbejdskraft og udgifter
description: Dette emne forklarer, hvordan du konfigurerer standardomkostninger for arbejdskraft og udgifter for et projekt.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185399"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="621c4-103">Konfigurere standardomkostninger for arbejdskraft og udgifter</span><span class="sxs-lookup"><span data-stu-id="621c4-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="621c4-104">Dette emne forklarer, hvordan du konfigurerer standardomkostninger for arbejdskraft og udgifter for et projekt.</span><span class="sxs-lookup"><span data-stu-id="621c4-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="621c4-105">Denne opgave bruger USSI-datasættet.</span><span class="sxs-lookup"><span data-stu-id="621c4-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="621c4-106">Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Kostpris (time)**.</span><span class="sxs-lookup"><span data-stu-id="621c4-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="621c4-107">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="621c4-107">Select **New**.</span></span>
3. <span data-ttu-id="621c4-108">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="621c4-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="621c4-109">Angiv et tal i feltet **Kostpris**.</span><span class="sxs-lookup"><span data-stu-id="621c4-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="621c4-110">Du kan definere en standardkostpris for projektkategorien, eller du kan definere en kostpris pr. arbejdernummer, projektnummer, kategori, dato eller en kombination af disse.</span><span class="sxs-lookup"><span data-stu-id="621c4-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="621c4-111">Den kostpris, der anvendes, vil være den mest detaljerede kostpris.</span><span class="sxs-lookup"><span data-stu-id="621c4-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="621c4-112">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="621c4-112">Select **Save**.</span></span>
6. <span data-ttu-id="621c4-113">Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Salgspris (time)**.</span><span class="sxs-lookup"><span data-stu-id="621c4-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="621c4-114">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="621c4-114">Select **New**.</span></span>
8. <span data-ttu-id="621c4-115">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="621c4-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="621c4-116">Vælg en indstilling i feltet **Gælder for**.</span><span class="sxs-lookup"><span data-stu-id="621c4-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="621c4-117">Angiv et tal i feltet **Prissætning**.</span><span class="sxs-lookup"><span data-stu-id="621c4-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="621c4-118">Du kan definere en standardsalgspris for timeposteringer eller for en projektkategori.</span><span class="sxs-lookup"><span data-stu-id="621c4-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="621c4-119">Du kan også definere salgspriser pr. arbejdernummer, projektnummer, kategori, posteringsdato eller en kombination af disse.</span><span class="sxs-lookup"><span data-stu-id="621c4-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="621c4-120">Den faktiske salgspris, som anvendes, når en arbejder angiver en postering i timekladden, er salgsprisen med den højeste detaljeringsgrad.</span><span class="sxs-lookup"><span data-stu-id="621c4-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="621c4-121">Hvis der f.eks. både er oprettet en generel salgspris og en arbejderspecifik salgspris, bruges den arbejderspecifikke salgspris.</span><span class="sxs-lookup"><span data-stu-id="621c4-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="621c4-122">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="621c4-122">Select **Save**.</span></span>
12. <span data-ttu-id="621c4-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="621c4-123">Close the page.</span></span>
13. <span data-ttu-id="621c4-124">Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Kostpris (udgift)**.</span><span class="sxs-lookup"><span data-stu-id="621c4-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="621c4-125">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="621c4-125">Select **New**.</span></span>
15. <span data-ttu-id="621c4-126">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="621c4-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="621c4-127">Angiv et tal i feltet **Kostpris**.</span><span class="sxs-lookup"><span data-stu-id="621c4-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="621c4-128">Der kan udfyldes flere felter, men dette er det minimum, der er nødvendigt for at gemme posten.</span><span class="sxs-lookup"><span data-stu-id="621c4-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="621c4-129">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="621c4-129">Select **Save**.</span></span>
18. <span data-ttu-id="621c4-130">Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Salgspris (udgift)**.</span><span class="sxs-lookup"><span data-stu-id="621c4-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="621c4-131">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="621c4-131">Select **New**.</span></span>
20. <span data-ttu-id="621c4-132">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="621c4-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="621c4-133">Vælg en indstilling i feltet **Gælder for**.</span><span class="sxs-lookup"><span data-stu-id="621c4-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="621c4-134">Angiv et tal i feltet **Prissætning**.</span><span class="sxs-lookup"><span data-stu-id="621c4-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="621c4-135">Den faktiske salgspris, som anvendes, når en medarbejder angiver posteringer i en udgiftskladde, er den salgspris, der har det højeste detaljeringsniveau.</span><span class="sxs-lookup"><span data-stu-id="621c4-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="621c4-136">Hvis der f.eks. både er oprettet en generel salgspris og en arbejderspecifik salgspris, anvendes den arbejderspecifikke salgspris.</span><span class="sxs-lookup"><span data-stu-id="621c4-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="621c4-137">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="621c4-137">Select **Save**.</span></span>

