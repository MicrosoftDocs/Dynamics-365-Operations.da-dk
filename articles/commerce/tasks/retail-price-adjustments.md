---
title: " Detailprisjusteringer"
description: Denne procedure gennemgår oprettelse af en prisjustering for handel.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd6459416ca42530401aa439b1b8511657bd9b36
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021980"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="84f43-103"> Detailprisjusteringer</span><span class="sxs-lookup"><span data-stu-id="84f43-103">Retail price adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="84f43-104">Denne procedure gennemgår oprettelse af en prisjustering for handel.</span><span class="sxs-lookup"><span data-stu-id="84f43-104">This procedure will walk through creating a commerce price adjustment.</span></span> <span data-ttu-id="84f43-105">En prisjustering kan angive en vares salgspris direkte eller ændre dens basissalgspris eller salgspris ifølge samhandelsaftale.</span><span class="sxs-lookup"><span data-stu-id="84f43-105">A price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="84f43-106">Proceduren bruger USRT-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="84f43-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="84f43-107">Klik på Styring af prissætning og rabatter.</span><span class="sxs-lookup"><span data-stu-id="84f43-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="84f43-108">Klik på fanen Prisjusteringer.</span><span class="sxs-lookup"><span data-stu-id="84f43-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="84f43-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="84f43-109">Click New.</span></span>
    * <span data-ttu-id="84f43-110">Her kan du oprette alle de mest almindeligt anvendte pris- og rabatregler, herunder rabatter, prisjusteringer, samhandelskladder og prissætningsregler for kategori.</span><span class="sxs-lookup"><span data-stu-id="84f43-110">From here you can create all of the most commonly used price and discount rules, including discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="84f43-111">Klik på Prisjustering.</span><span class="sxs-lookup"><span data-stu-id="84f43-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="84f43-112">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="84f43-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="84f43-113">Udvid sektionen Linjer.</span><span class="sxs-lookup"><span data-stu-id="84f43-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="84f43-114">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="84f43-114">Click Add.</span></span>
    * <span data-ttu-id="84f43-115">I dette eksempel skal du skrive "81126" i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="84f43-115">For this example, enter '81126' in the Product field.</span></span> <span data-ttu-id="84f43-116">Angiv derefter "10,0" i feltet Rabatprocent.</span><span class="sxs-lookup"><span data-stu-id="84f43-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="84f43-117">En prisjustering af typen rabatprocent vil reducere en basissalgspris eller salgspris ifølge samhandelsaftale.</span><span class="sxs-lookup"><span data-stu-id="84f43-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="84f43-118">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="84f43-118">Click Add.</span></span>
    * <span data-ttu-id="84f43-119">I dette eksempel skal du skrive "81125" i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="84f43-119">For this example, enter '81125' in the Product field.</span></span> <span data-ttu-id="84f43-120">Vælg derefter "Kasserabatbeløb" i feltet Rabatmetode.</span><span class="sxs-lookup"><span data-stu-id="84f43-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="84f43-121">Skriv til sidst "5,0" i feltet Kasserabatbeløb.</span><span class="sxs-lookup"><span data-stu-id="84f43-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="84f43-122">En rabat af typen kasserabatbeløb er et beløb taget fra en basispris eller en pris ifølge samhandelsaftale.</span><span class="sxs-lookup"><span data-stu-id="84f43-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="84f43-123">Klik på Prisgrupper.</span><span class="sxs-lookup"><span data-stu-id="84f43-123">Click Price groups.</span></span>
    * <span data-ttu-id="84f43-124">Vælg "RP-Houston"' i feltet Prisgruppe.</span><span class="sxs-lookup"><span data-stu-id="84f43-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="84f43-125">Dette vil knytte prisjusteringen til Houston-butikken.</span><span class="sxs-lookup"><span data-stu-id="84f43-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="84f43-126">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="84f43-126">Click Save.</span></span>
11. <span data-ttu-id="84f43-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="84f43-127">Close the page.</span></span>
12. <span data-ttu-id="84f43-128">Vælg "Aktiveret" i feltet Status.</span><span class="sxs-lookup"><span data-stu-id="84f43-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="84f43-129">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="84f43-129">Click Save.</span></span>
14. <span data-ttu-id="84f43-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="84f43-130">Close the page.</span></span>
15. <span data-ttu-id="84f43-131">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="84f43-131">Refresh the page.</span></span>
