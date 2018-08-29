--- 
title: "Konfigurere økonomisk datadeling på tværs af firmaer"
description: "Denne procedure viser, hvordan du kan konfigurere, aktivere, validere og løse konflikter ved deling af data mellem virksomheder."
author: aprilolson
manager: AnnBe
ms.date: 06/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 5ae6b30d2d0948efbf86f2c2693e643b383f8406
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="configure-cross-company-financial-data-sharing"></a><span data-ttu-id="ad7df-103">Konfigurere økonomisk datadeling på tværs af firmaer</span><span class="sxs-lookup"><span data-stu-id="ad7df-103">Configure cross-company financial data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad7df-104">Denne procedure viser, hvordan du kan konfigurere, aktivere, validere og løse konflikter ved deling af data mellem virksomheder.</span><span class="sxs-lookup"><span data-stu-id="ad7df-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="ad7df-105">Den anvender USMF-virksomheden og skabelonen til deling af økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="ad7df-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="ad7df-106">Denne opgavevejledning kræver Dynamics AX-platform 7.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="ad7df-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="ad7df-107">Gå til Systemadministration > Arbejdsområder > Datastyring.</span><span class="sxs-lookup"><span data-stu-id="ad7df-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="ad7df-108">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="ad7df-108">Click Import.</span></span>
3. <span data-ttu-id="ad7df-109">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ad7df-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ad7df-110">Vælg typen Pakke i feltet Kildedataformat.</span><span class="sxs-lookup"><span data-stu-id="ad7df-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="ad7df-111">Klik på Overfør.</span><span class="sxs-lookup"><span data-stu-id="ad7df-111">Click Upload.</span></span> <span data-ttu-id="ad7df-112">Naviger til placeringen af pakkefilen for skabelonen til deling af økonomiske data, og vælg filen.</span><span class="sxs-lookup"><span data-stu-id="ad7df-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="ad7df-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ad7df-113">Click Save.</span></span>
6. <span data-ttu-id="ad7df-114">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ad7df-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ad7df-115">Vælg den politik for datadeling, der netop er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="ad7df-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="ad7df-116">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="ad7df-116">Click Import.</span></span>
8. <span data-ttu-id="ad7df-117">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="ad7df-117">Click Close.</span></span>
9. <span data-ttu-id="ad7df-118">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="ad7df-118">Refresh the page.</span></span>
10. <span data-ttu-id="ad7df-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ad7df-119">Close the page.</span></span>
11. <span data-ttu-id="ad7df-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ad7df-120">Close the page.</span></span>
12. <span data-ttu-id="ad7df-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ad7df-121">Close the page.</span></span>
13. <span data-ttu-id="ad7df-122">Gå til Systemadministration > Konfiguration > Konfigurer datadeling på tværs af firma.</span><span class="sxs-lookup"><span data-stu-id="ad7df-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="ad7df-123">Find og vælg Betalingsdage på listen.</span><span class="sxs-lookup"><span data-stu-id="ad7df-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="ad7df-124">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ad7df-124">Click Add.</span></span>
16. <span data-ttu-id="ad7df-125">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ad7df-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="ad7df-126">Skriv 'USSI' i feltet Firma.</span><span class="sxs-lookup"><span data-stu-id="ad7df-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="ad7df-127">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ad7df-127">Click Add.</span></span>
19. <span data-ttu-id="ad7df-128">Skriv 'USMF' i feltet Firma.</span><span class="sxs-lookup"><span data-stu-id="ad7df-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="ad7df-129">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ad7df-129">Click Save.</span></span>
21. <span data-ttu-id="ad7df-130">Klik på Enable.</span><span class="sxs-lookup"><span data-stu-id="ad7df-130">Click Enable.</span></span>
22. <span data-ttu-id="ad7df-131">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="ad7df-131">Click Yes.</span></span>
23. <span data-ttu-id="ad7df-132">Klik på Find delingsproblemer.</span><span class="sxs-lookup"><span data-stu-id="ad7df-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="ad7df-133">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="ad7df-133">Click Yes.</span></span>
25. <span data-ttu-id="ad7df-134">Klik på Opdater feltværdi.</span><span class="sxs-lookup"><span data-stu-id="ad7df-134">Click Update field value.</span></span>
26. <span data-ttu-id="ad7df-135">Klik på Brug værdi fra firma 1.</span><span class="sxs-lookup"><span data-stu-id="ad7df-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="ad7df-136">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="ad7df-136">Refresh the page.</span></span>
28. <span data-ttu-id="ad7df-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ad7df-137">Close the page.</span></span>


