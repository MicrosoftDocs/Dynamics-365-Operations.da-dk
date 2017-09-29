--- 
title: Konfigurere indeholdt skat
description: "A-skat er en skat på leverandører, der ikke opretter momstransaktioner."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: dc4c0745235052cb4145bc7083fef1a88c8bb5c9
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="48d58-103">Konfigurere indeholdt skat</span><span class="sxs-lookup"><span data-stu-id="48d58-103">Set up withholding tax</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48d58-104">A-skat er en skat på leverandører, der ikke opretter momstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="48d58-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="48d58-105">A-skat, der beregnes på leverandørbetalinger, er et passiv.</span><span class="sxs-lookup"><span data-stu-id="48d58-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="48d58-106">Derfor er det kun statuskonti eller passivkonti, der kan bruges til bogføring af A-skat.</span><span class="sxs-lookup"><span data-stu-id="48d58-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="48d58-107">Denne opgaveguide viser, hvordan du konfigurerer A-skat.</span><span class="sxs-lookup"><span data-stu-id="48d58-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="48d58-108">Gå til Moms > Indirekte skatter > A-skat > Koder for A-skat.</span><span class="sxs-lookup"><span data-stu-id="48d58-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="48d58-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="48d58-109">Click New.</span></span>
3. <span data-ttu-id="48d58-110">Skrive en værdi i feltet A-skat.</span><span class="sxs-lookup"><span data-stu-id="48d58-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="48d58-111">Angiv navnet for koden for A-skat i feltet Navn på indeholdt skat.</span><span class="sxs-lookup"><span data-stu-id="48d58-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="48d58-112">Vælg hovedkontoen til bogføring af A-skattetilsvar i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="48d58-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="48d58-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="48d58-113">Click Save.</span></span>
7. <span data-ttu-id="48d58-114">Klik på Værdier.</span><span class="sxs-lookup"><span data-stu-id="48d58-114">Click Values.</span></span>
8. <span data-ttu-id="48d58-115">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="48d58-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="48d58-116">Angiv en procentsats, der bruges til beregning af a-skat i feltet Værdi.</span><span class="sxs-lookup"><span data-stu-id="48d58-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="48d58-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="48d58-117">Click Save.</span></span>
11. <span data-ttu-id="48d58-118">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="48d58-118">Close the page.</span></span>
12. <span data-ttu-id="48d58-119">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="48d58-119">Click Save.</span></span>
13. <span data-ttu-id="48d58-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="48d58-120">Close the page.</span></span>
14. <span data-ttu-id="48d58-121">Gå til Moms > Indirekte skatter > A-skat > Grupper for indeholdt skat.</span><span class="sxs-lookup"><span data-stu-id="48d58-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="48d58-122">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="48d58-122">Click New.</span></span>
16. <span data-ttu-id="48d58-123">Angiv identifikatoren for gruppen for indeholdt skat i feltet Grupper for indeholdt skat.</span><span class="sxs-lookup"><span data-stu-id="48d58-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="48d58-124">Skriv navnet på gruppen for indeholdt skat i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="48d58-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="48d58-125">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="48d58-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="48d58-126">Vælg kode for A-skat i feltet Kode for A-skat.</span><span class="sxs-lookup"><span data-stu-id="48d58-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="48d58-127">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="48d58-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="48d58-128">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="48d58-128">Click Save.</span></span>


