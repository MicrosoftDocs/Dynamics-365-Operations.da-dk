---
title: Rapportere status for en mobil jobenhed
description: Denne procedure viser, hvordan du starter og rapporterer status for et produktionsjob i jobenhedens registreringsformular.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationTouch, JmgRegistrationTouchUserConfiguration, JmgRegistrationTouchStart, JmgRegistrationTouchReportFeedback, JmgRegistrationTouchAssignedJobs, JmgRegistrationTouchBreak, JmgRegistrationTouchLeave, JmgRegistrationTouchIndirectActivity, JmgDialogForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 199ccc03cee1f6328ff42063a480146b0a361711
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843571"
---
# <a name="report-progress-on-a-mobile-job-device"></a><span data-ttu-id="2d504-103">Rapportere status for en mobil jobenhed</span><span class="sxs-lookup"><span data-stu-id="2d504-103">Report progress on a mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d504-104">Denne procedure viser, hvordan du starter og rapporterer status for et produktionsjob i jobenhedens registreringsformular.</span><span class="sxs-lookup"><span data-stu-id="2d504-104">This procedure shows you how to start and report progress on a production job in the job device registration form.</span></span>



<span data-ttu-id="2d504-105">Rollen Systemadministratoren eller Maskinpasser skal være tilknyttet brugerkontoen, for at du kan køre denne procedure.</span><span class="sxs-lookup"><span data-stu-id="2d504-105">To be able to run this procedure you must have the System administator or Machine Operator role associated with the user account.</span></span>

1. <span data-ttu-id="2d504-106">Gå til Produktionsstyring > Produktionsudførelse > Jobkortenhed.</span><span class="sxs-lookup"><span data-stu-id="2d504-106">Go to Production control > Manufacturing execution > Job card device.</span></span>
2. <span data-ttu-id="2d504-107">Angiv arbejderens kort i feltet WorkerTextField.</span><span class="sxs-lookup"><span data-stu-id="2d504-107">In the WorkerTextField field, enter the badge of a worker.</span></span> <span data-ttu-id="2d504-108">Skriv "123" for Christina Portra i USMF-demodataene.</span><span class="sxs-lookup"><span data-stu-id="2d504-108">In the USMF demo data type '123' for Christina Portra..</span></span>
3. <span data-ttu-id="2d504-109">Klik på Log på.</span><span class="sxs-lookup"><span data-stu-id="2d504-109">Click Log in.</span></span>
4. <span data-ttu-id="2d504-110">Klik på knappen Filtrer.</span><span class="sxs-lookup"><span data-stu-id="2d504-110">Click the Filter button.</span></span>
5. <span data-ttu-id="2d504-111">Markér eller fjern markeringen af afkrydsningsfeltet Anvend konfigurationsfilter.</span><span class="sxs-lookup"><span data-stu-id="2d504-111">Check or uncheck the Apply configuration filter check box.</span></span> <span data-ttu-id="2d504-112">Hvis du indstiller et filter, kan du bruge produktionsenhed 110 i USMF.</span><span class="sxs-lookup"><span data-stu-id="2d504-112">If you set a filter you can use production unit 110 in USMF.</span></span>
6. <span data-ttu-id="2d504-113">Vælg i ressourcegruppen, hvilke produktionsjob arbejderen kan arbejde på, i feltet Produktionsenhed.</span><span class="sxs-lookup"><span data-stu-id="2d504-113">In the Production unit field, select the ressource group for which production jobs the worker can work on.</span></span>
7. <span data-ttu-id="2d504-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2d504-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2d504-115">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2d504-115">Click OK.</span></span>
9. <span data-ttu-id="2d504-116">Klik på knappen Start job.</span><span class="sxs-lookup"><span data-stu-id="2d504-116">Click the Start job button.</span></span>
10. <span data-ttu-id="2d504-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2d504-117">Click OK.</span></span>
11. <span data-ttu-id="2d504-118">Klik på knappen Rapport i gang.</span><span class="sxs-lookup"><span data-stu-id="2d504-118">Click the Report progress button.</span></span>
12. <span data-ttu-id="2d504-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2d504-119">Click OK.</span></span>
13. <span data-ttu-id="2d504-120">Klik på knappen Næste job.</span><span class="sxs-lookup"><span data-stu-id="2d504-120">Click the Next job button.</span></span>
14. <span data-ttu-id="2d504-121">Klik på Tildelt til for at se en oversigt over alle produktionsjob-knappen.</span><span class="sxs-lookup"><span data-stu-id="2d504-121">Click the Assigned to see an overview of all production jobs button.</span></span>
15. <span data-ttu-id="2d504-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="2d504-122">Close the page.</span></span>
16. <span data-ttu-id="2d504-123">Klik på knappen Pause.</span><span class="sxs-lookup"><span data-stu-id="2d504-123">Click the Break button.</span></span>
17. <span data-ttu-id="2d504-124">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="2d504-124">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="2d504-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2d504-125">Click OK.</span></span>
19. <span data-ttu-id="2d504-126">Klik på knappen Afslutter job.</span><span class="sxs-lookup"><span data-stu-id="2d504-126">Click the Leaving button.</span></span>
20. <span data-ttu-id="2d504-127">Vælg for at logge af.</span><span class="sxs-lookup"><span data-stu-id="2d504-127">Select to log out.</span></span>
21. <span data-ttu-id="2d504-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2d504-128">Click OK.</span></span>
22. <span data-ttu-id="2d504-129">Log på igen i feltet WorkerTextField.</span><span class="sxs-lookup"><span data-stu-id="2d504-129">In the WorkerTextField field, log in again.</span></span> <span data-ttu-id="2d504-130">Du kan vælge arbejderen "123" i USMF-demodata.</span><span class="sxs-lookup"><span data-stu-id="2d504-130">You can select worker '123' in USMF demo data.</span></span>
23. <span data-ttu-id="2d504-131">Klik på Log på.</span><span class="sxs-lookup"><span data-stu-id="2d504-131">Click Log in.</span></span>
24. <span data-ttu-id="2d504-132">Klik på Stop pause.</span><span class="sxs-lookup"><span data-stu-id="2d504-132">Click Stop break.</span></span>
25. <span data-ttu-id="2d504-133">Klik på knappen Aktivitet.</span><span class="sxs-lookup"><span data-stu-id="2d504-133">Click the Activity button.</span></span>
26. <span data-ttu-id="2d504-134">Klik på Annuller.</span><span class="sxs-lookup"><span data-stu-id="2d504-134">Click Cancel.</span></span>
27. <span data-ttu-id="2d504-135">Klik på knappen Afslutter job.</span><span class="sxs-lookup"><span data-stu-id="2d504-135">Click the Leaving button.</span></span>
28. <span data-ttu-id="2d504-136">Vælg for at stemple ud.</span><span class="sxs-lookup"><span data-stu-id="2d504-136">Select to clock out.</span></span>
29. <span data-ttu-id="2d504-137">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2d504-137">Click OK.</span></span>
30. <span data-ttu-id="2d504-138">Vælg en årsag til, at du stempler ud tidligt.</span><span class="sxs-lookup"><span data-stu-id="2d504-138">Select a reason why you are clocking out early.</span></span>

