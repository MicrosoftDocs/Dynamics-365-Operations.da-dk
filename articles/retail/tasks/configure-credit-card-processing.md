--- 
title: " Konfigurere kreditkortbehandling"
description: "Denne procedure gennemgår visning af listen over betalingsudbydere, og hvordan du konfigurerer en betalingskonto for debitor."
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f70b49bf64d254f0020ecd585032f666f2e14059
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="72660-103"> Konfigurere kreditkortbehandling</span><span class="sxs-lookup"><span data-stu-id="72660-103">Configure credit card processing</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="72660-104">Denne procedure gennemgår visning af listen over betalingsudbydere, og hvordan du konfigurerer en betalingskonto for debitor.</span><span class="sxs-lookup"><span data-stu-id="72660-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="72660-105">Denne procedure bruger USRT-firmaets demodata og er beregnet til administratorer og it-medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="72660-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="72660-106">Få vist en liste over betalingsudbydere</span><span class="sxs-lookup"><span data-stu-id="72660-106">View a list of payment providers</span></span>
1. <span data-ttu-id="72660-107">Gå til Debitor > Betalingsopsætning > Betalingstjenester.</span><span class="sxs-lookup"><span data-stu-id="72660-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="72660-108">Klik på Vis tilgængelige udbydere.</span><span class="sxs-lookup"><span data-stu-id="72660-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="72660-109">Konfigurer betalingskonto</span><span class="sxs-lookup"><span data-stu-id="72660-109">Configure payment account</span></span>
1. <span data-ttu-id="72660-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="72660-110">Click New.</span></span>
2. <span data-ttu-id="72660-111">Indtast en værdi i feltet Betalingstjeneste.</span><span class="sxs-lookup"><span data-stu-id="72660-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="72660-112">Vælg en indstilling i feltet Betalingsconnector.</span><span class="sxs-lookup"><span data-stu-id="72660-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="72660-113">Slå udvidelsen af sektionen Betalingstjenestekonto til/fra .</span><span class="sxs-lookup"><span data-stu-id="72660-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="72660-114">Skriv "PROD" i feltet Miljø:.</span><span class="sxs-lookup"><span data-stu-id="72660-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="72660-115">Klik på Kreditkorttyper.</span><span class="sxs-lookup"><span data-stu-id="72660-115">Click Credit card types.</span></span>
7. <span data-ttu-id="72660-116">Klik på rullelisten i feltet Betalingskladde for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="72660-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="72660-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="72660-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="72660-118">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="72660-118">Click Add.</span></span>
10. <span data-ttu-id="72660-119">Skriv en værdi i feltet Valuta.</span><span class="sxs-lookup"><span data-stu-id="72660-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="72660-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="72660-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="72660-121">Klik på rullelisten i feltet Betalingskladde for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="72660-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="72660-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="72660-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="72660-123">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="72660-123">Click Add.</span></span>
15. <span data-ttu-id="72660-124">Skriv en værdi i feltet Valuta.</span><span class="sxs-lookup"><span data-stu-id="72660-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="72660-125">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="72660-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="72660-126">Du kan gentage disse trin for så mange korttyper, du har brug for.</span><span class="sxs-lookup"><span data-stu-id="72660-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="72660-127">Klik på rullelisten i feltet Betalingskladde for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="72660-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="72660-128">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="72660-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="72660-129">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="72660-129">Click Add.</span></span>
20. <span data-ttu-id="72660-130">Skriv en værdi i feltet Valuta.</span><span class="sxs-lookup"><span data-stu-id="72660-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="72660-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="72660-131">Click Save.</span></span>
22. <span data-ttu-id="72660-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="72660-132">Close the page.</span></span>
23. <span data-ttu-id="72660-133">Klik på Valider.</span><span class="sxs-lookup"><span data-stu-id="72660-133">Click Validate.</span></span>
24. <span data-ttu-id="72660-134">Klik i afkrydsningsfeltet Standardprocessor til nye kreditkort.</span><span class="sxs-lookup"><span data-stu-id="72660-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="72660-135">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="72660-135">Click Save.</span></span>


