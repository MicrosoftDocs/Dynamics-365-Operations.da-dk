---
title: Oprette og tilknytte en hardwarestation
description: Denne procedure gennemgår oprettelse af en ny hardwarestation.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 80df4fa663d208e28f5c9b031b6610d29286171c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "330557"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="ffb0f-103">Oprette og tilknytte en hardwarestation</span><span class="sxs-lookup"><span data-stu-id="ffb0f-103">Create and associate a hardware station</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ffb0f-104">Denne procedure gennemgår oprettelse af en ny hardwarestation.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="ffb0f-105">En ny hardwareprofil oprettes og bruges til at tilføje nye hardwarestationer til en foruddefineret butik (kanal).</span><span class="sxs-lookup"><span data-stu-id="ffb0f-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="ffb0f-106">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="ffb0f-107">Gå til Oprindelsesdata til handel > Kanaler >..</span><span class="sxs-lookup"><span data-stu-id="ffb0f-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="ffb0f-108">> ..</span><span class="sxs-lookup"><span data-stu-id="ffb0f-108">> ..</span></span> <span data-ttu-id="ffb0f-109">> ..</span><span class="sxs-lookup"><span data-stu-id="ffb0f-109">> ..</span></span> <span data-ttu-id="ffb0f-110">> Hardwarestations profiler.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="ffb0f-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-111">Click New.</span></span>
3. <span data-ttu-id="ffb0f-112">Skriv "TestHWProfile" i feltet Hardwarestation-id.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="ffb0f-113">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ffb0f-114">Angiv et tal i feltet Portnummer.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="ffb0f-115">Klik på rullelisten i feltet Hardwareprofil for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ffb0f-116">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="ffb0f-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ffb0f-118">Klik på rullelisten i feltet Pakkens navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="ffb0f-119">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ffb0f-120">Dette er den standardpakke, der følger med et nyt miljø.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="ffb0f-121">Versionsnummeret kan variere.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-121">The version number may vary.</span></span>  
11. <span data-ttu-id="ffb0f-122">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-122">Click Save.</span></span>
12. <span data-ttu-id="ffb0f-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-123">Close the page.</span></span>
13. <span data-ttu-id="ffb0f-124">Gå til Detail og handel > Kanaler > Alle detailbutikker.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-124">Go to Retail and commerce > Channels > All retail stores.</span></span>
14. <span data-ttu-id="ffb0f-125">Markér række 17 på listen.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="ffb0f-126">Hvis du bruger USRT-demodatafirmaet, er dette Houston-butikken.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="ffb0f-127">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="ffb0f-128">Slå udvidelsen af sektionen Hardwarestationer til/fra.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="ffb0f-129">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-129">Click Add.</span></span>
18. <span data-ttu-id="ffb0f-130">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="ffb0f-131">Klik på rullelisten i feltet Profil-id for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="ffb0f-132">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ffb0f-133">Det skal være den nye hardwarestationsprofil, du oprettede i de forrige trin.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="ffb0f-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="ffb0f-135">Indtast en værdi i feltet Værtsnavn.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="ffb0f-136">Indtast en værdi i feltet Terminal-id for elektronisk pengeoverførsel.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="ffb0f-137">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-137">Click Save.</span></span>

