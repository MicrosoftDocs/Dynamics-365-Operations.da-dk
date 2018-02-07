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
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="3a9c9-103"> Oprette økonomiske dimensioner for detailkanaler og konfigurere dimensionsværdier for butikker</span><span class="sxs-lookup"><span data-stu-id="3a9c9-103">Create financial dimensions for Retail channels and configure dimension values on stores</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3a9c9-104">Denne fremgangsmåde fører dig gennem oprettelse af en detailkanals økonomiske dimension med dimensionsværdier og trin til at konfigurere økonomiske dimensionsværdier for detailbutikker.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="3a9c9-105">Emnet indeholder ikke andre relaterede trin, f.eks. oprettelse af dimensionssæt og kontostrukturer.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="3a9c9-106">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="3a9c9-107">Gå til Finans > Kontoplan > Dimensioner > Økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="3a9c9-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-108">Click New.</span></span>
3. <span data-ttu-id="3a9c9-109">Vælg "Detailkanaler" i feltet Brug værdier fra.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="3a9c9-110">Skriv en værdi i feltet Dimensionsnavn.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="3a9c9-111">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-111">Click Activate.</span></span>
6. <span data-ttu-id="3a9c9-112">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-112">Click Close.</span></span>
7. <span data-ttu-id="3a9c9-113">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-113">Click Activate.</span></span>
8. <span data-ttu-id="3a9c9-114">Klik på Dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-114">Click Dimension values.</span></span>
9. <span data-ttu-id="3a9c9-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-115">Close the page.</span></span>
10. <span data-ttu-id="3a9c9-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-116">Click Save.</span></span>
11. <span data-ttu-id="3a9c9-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-117">Close the page.</span></span>
12. <span data-ttu-id="3a9c9-118">Gå til Detail og handel > Kanaler > Detailbutikker > Alle detailbutikker.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="3a9c9-119">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="3a9c9-120">Slå udvidelsen af sektionen Økonomiske dimensioner til/fra.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="3a9c9-121">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-121">Click Edit.</span></span>
16. <span data-ttu-id="3a9c9-122">Klik på rullelisten i feltet Retailchannel for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="3a9c9-123">Find og vælg på listen dimensionsværdien for butikken, der skal opdateres.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="3a9c9-124">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="3a9c9-125">Klik på rullelisten i feltet CostCenter for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="3a9c9-126">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="3a9c9-127">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="3a9c9-128">Klik på rullelisten i feltet Afdeling for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="3a9c9-129">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="3a9c9-130">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="3a9c9-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3a9c9-131">Click Save.</span></span>


