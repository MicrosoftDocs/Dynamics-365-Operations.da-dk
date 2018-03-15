--- 
title: " Oprette økonomiske dimensioner for detailkanaler og konfigurere dimensionsværdier for butikker"
description: "Denne fremgangsmåde fører dig gennem oprettelse af en detailkanals økonomiske dimension med dimensionsværdier og trin til at konfigurere økonomiske dimensionsværdier for detailbutikker."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 5ab4df61ab1e1346eaaf5c586f54a06b7b7432e1
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="fc444-103"> Oprette økonomiske dimensioner for detailkanaler og konfigurere dimensionsværdier for butikker</span><span class="sxs-lookup"><span data-stu-id="fc444-103">Create financial dimensions for Retail channels and configure dimension values on stores</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="fc444-104">Denne fremgangsmåde fører dig gennem oprettelse af en detailkanals økonomiske dimension med dimensionsværdier og trin til at konfigurere økonomiske dimensionsværdier for detailbutikker.</span><span class="sxs-lookup"><span data-stu-id="fc444-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="fc444-105">Emnet indeholder ikke andre relaterede trin, f.eks. oprettelse af dimensionssæt og kontostrukturer.</span><span class="sxs-lookup"><span data-stu-id="fc444-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="fc444-106">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="fc444-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="fc444-107">Gå til Finans > Kontoplan > Dimensioner > Økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="fc444-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="fc444-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fc444-108">Click New.</span></span>
3. <span data-ttu-id="fc444-109">Vælg "Detailkanaler" i feltet Brug værdier fra.</span><span class="sxs-lookup"><span data-stu-id="fc444-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="fc444-110">Skriv en værdi i feltet Dimensionsnavn.</span><span class="sxs-lookup"><span data-stu-id="fc444-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="fc444-111">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="fc444-111">Click Activate.</span></span>
6. <span data-ttu-id="fc444-112">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="fc444-112">Click Close.</span></span>
7. <span data-ttu-id="fc444-113">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="fc444-113">Click Activate.</span></span>
8. <span data-ttu-id="fc444-114">Klik på Dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="fc444-114">Click Dimension values.</span></span>
9. <span data-ttu-id="fc444-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="fc444-115">Close the page.</span></span>
10. <span data-ttu-id="fc444-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fc444-116">Click Save.</span></span>
11. <span data-ttu-id="fc444-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="fc444-117">Close the page.</span></span>
12. <span data-ttu-id="fc444-118">Gå til Detail og handel > Kanaler > Detailbutikker > Alle detailbutikker.</span><span class="sxs-lookup"><span data-stu-id="fc444-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="fc444-119">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fc444-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="fc444-120">Slå udvidelsen af sektionen Økonomiske dimensioner til/fra.</span><span class="sxs-lookup"><span data-stu-id="fc444-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="fc444-121">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="fc444-121">Click Edit.</span></span>
16. <span data-ttu-id="fc444-122">Klik på rullelisten i feltet Retailchannel for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="fc444-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="fc444-123">Find og vælg på listen dimensionsværdien for butikken, der skal opdateres.</span><span class="sxs-lookup"><span data-stu-id="fc444-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="fc444-124">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fc444-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="fc444-125">Klik på rullelisten i feltet CostCenter for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="fc444-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="fc444-126">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="fc444-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="fc444-127">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fc444-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="fc444-128">Klik på rullelisten i feltet Afdeling for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="fc444-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="fc444-129">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="fc444-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="fc444-130">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fc444-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="fc444-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fc444-131">Click Save.</span></span>


