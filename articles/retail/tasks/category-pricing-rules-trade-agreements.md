--- 
title: " Regler for kategoriprissætning til oprettelse af samhandelsaftaler"
description: "Denne procedure viser, hvordan du opretter salgsprissamhandelsaftaler ved hjælp af en kategoriprissætningsregel."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 4c67b3d24504f0f1c884b52598150cc5751afc5b
ms.contentlocale: da-dk
ms.lasthandoff: 01/19/2018

---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="80490-103"> Regler for kategoriprissætning til oprettelse af samhandelsaftaler</span><span class="sxs-lookup"><span data-stu-id="80490-103">Category pricing rules to create trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="80490-104">Denne procedure viser, hvordan du opretter salgsprissamhandelsaftaler ved hjælp af en kategoriprissætningsregel.</span><span class="sxs-lookup"><span data-stu-id="80490-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="80490-105">Det demodatafirma, der bruges til at oprette denne opgave, er USRT.</span><span class="sxs-lookup"><span data-stu-id="80490-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="80490-106">Denne opgave er tiltænkt rollen Detailproduktchef.</span><span class="sxs-lookup"><span data-stu-id="80490-106">This task is intended for the Retail merchandising manager role.</span></span>

1. <span data-ttu-id="80490-107">Klik på Styring af prissætning og rabatter.</span><span class="sxs-lookup"><span data-stu-id="80490-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="80490-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="80490-108">Click New.</span></span>
3. <span data-ttu-id="80490-109">Klik på Regel for kategoripriser.</span><span class="sxs-lookup"><span data-stu-id="80490-109">Click Category price rule.</span></span>
4. <span data-ttu-id="80490-110">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="80490-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="80490-111">Vælg en indstilling i feltet Kontokode.</span><span class="sxs-lookup"><span data-stu-id="80490-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="80490-112">En kontokode af typen "Gruppe" bruges til at konfigurere salgsprissamhandelsaftaler, der er specifikke for kanaler, fordelskundeprogrammer, kataloger og tilhørsforhold.</span><span class="sxs-lookup"><span data-stu-id="80490-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="80490-113">Indtast eller vælg en værdi i feltet Kontovalg.</span><span class="sxs-lookup"><span data-stu-id="80490-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="80490-114">Indtast eller vælg en værdi i feltet Kategori.</span><span class="sxs-lookup"><span data-stu-id="80490-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="80490-115">Angiv et tal i feltet Beløb/procent.</span><span class="sxs-lookup"><span data-stu-id="80490-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="80490-116">Indtast eller vælg en værdi i feltet Afrundingsversion.</span><span class="sxs-lookup"><span data-stu-id="80490-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="80490-117">Klik på Generér handelsaftaler.</span><span class="sxs-lookup"><span data-stu-id="80490-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="80490-118">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="80490-118">Click Next.</span></span>
12. <span data-ttu-id="80490-119">Indtast en dato i feltet Fra dato.</span><span class="sxs-lookup"><span data-stu-id="80490-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="80490-120">Indtast en dato i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="80490-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="80490-121">Vælg Ja i feltet Find næste.</span><span class="sxs-lookup"><span data-stu-id="80490-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="80490-122">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="80490-122">Click Next.</span></span>
16. <span data-ttu-id="80490-123">Klik på Finish.</span><span class="sxs-lookup"><span data-stu-id="80490-123">Click Finish.</span></span>
    * <span data-ttu-id="80490-124">Dette opretter en samhandelskladde og åbnes den til korrektur.</span><span class="sxs-lookup"><span data-stu-id="80490-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="80490-125">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="80490-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="80490-126">Samhandelskladder, der oprettes ud fra Kategoriprissætningsregler, bogføres ikke.</span><span class="sxs-lookup"><span data-stu-id="80490-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="80490-127">Du kan gennemse og redigere de priser, der genereres, før de bogføres.</span><span class="sxs-lookup"><span data-stu-id="80490-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="80490-128">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="80490-128">Click Edit.</span></span>
19. <span data-ttu-id="80490-129">Indtast et tal i feltet Beløb i valuta.</span><span class="sxs-lookup"><span data-stu-id="80490-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="80490-130">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="80490-130">Click Post.</span></span>
21. <span data-ttu-id="80490-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="80490-131">Click OK.</span></span>
22. <span data-ttu-id="80490-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="80490-132">Close the page.</span></span>
23. <span data-ttu-id="80490-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="80490-133">Close the page.</span></span>
24. <span data-ttu-id="80490-134">Klik på fanen Regler for kategoripriser.</span><span class="sxs-lookup"><span data-stu-id="80490-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="80490-135">Kanalbestemte Kategoriprissætningsregler bliver vist i denne liste.</span><span class="sxs-lookup"><span data-stu-id="80490-135">Channel specific Category pricing rules will show in this list.</span></span>  


