--- 
title: "Konfigurere økonomisk datadeling på tværs af firmaer"
description: "Denne procedure viser, hvordan du kan konfigurere, aktivere, validere og løse konflikter ved deling af data mellem virksomheder."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 784a925fa06148cad780b494c88b9a7af1809c9d
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="49bd0-103">Konfigurere økonomisk datadeling på tværs af firmaer</span><span class="sxs-lookup"><span data-stu-id="49bd0-103">Configure financial cross-company data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49bd0-104">Denne procedure viser, hvordan du kan konfigurere, aktivere, validere og løse konflikter ved deling af data mellem virksomheder.</span><span class="sxs-lookup"><span data-stu-id="49bd0-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="49bd0-105">Den anvender USMF-virksomheden og skabelonen til deling af økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="49bd0-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="49bd0-106">Denne opgavevejledning kræver Dynamics AX-platform 7.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="49bd0-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="49bd0-107">Gå til Systemadministration > Arbejdsområder > Datastyring.</span><span class="sxs-lookup"><span data-stu-id="49bd0-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="49bd0-108">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="49bd0-108">Click Import.</span></span>
3. <span data-ttu-id="49bd0-109">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="49bd0-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="49bd0-110">Vælg typen Pakke i feltet Kildedataformat.</span><span class="sxs-lookup"><span data-stu-id="49bd0-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="49bd0-111">Klik på Overfør.</span><span class="sxs-lookup"><span data-stu-id="49bd0-111">Click Upload.</span></span> <span data-ttu-id="49bd0-112">Naviger til placeringen af pakkefilen for skabelonen til deling af økonomiske data, og vælg filen.</span><span class="sxs-lookup"><span data-stu-id="49bd0-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="49bd0-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="49bd0-113">Click Save.</span></span>
6. <span data-ttu-id="49bd0-114">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="49bd0-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="49bd0-115">Vælg den politik for datadeling, der netop er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="49bd0-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="49bd0-116">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="49bd0-116">Click Import.</span></span>
8. <span data-ttu-id="49bd0-117">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="49bd0-117">Click Close.</span></span>
9. <span data-ttu-id="49bd0-118">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="49bd0-118">Refresh the page.</span></span>
10. <span data-ttu-id="49bd0-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="49bd0-119">Close the page.</span></span>
11. <span data-ttu-id="49bd0-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="49bd0-120">Close the page.</span></span>
12. <span data-ttu-id="49bd0-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="49bd0-121">Close the page.</span></span>
13. <span data-ttu-id="49bd0-122">Gå til Systemadministration > Konfiguration > Konfigurer datadeling på tværs af firma.</span><span class="sxs-lookup"><span data-stu-id="49bd0-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="49bd0-123">Find og vælg Betalingsdage på listen.</span><span class="sxs-lookup"><span data-stu-id="49bd0-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="49bd0-124">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="49bd0-124">Click Add.</span></span>
16. <span data-ttu-id="49bd0-125">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="49bd0-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="49bd0-126">Skriv 'USSI' i feltet Firma.</span><span class="sxs-lookup"><span data-stu-id="49bd0-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="49bd0-127">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="49bd0-127">Click Add.</span></span>
19. <span data-ttu-id="49bd0-128">Skriv 'USMF' i feltet Firma.</span><span class="sxs-lookup"><span data-stu-id="49bd0-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="49bd0-129">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="49bd0-129">Click Save.</span></span>
21. <span data-ttu-id="49bd0-130">Klik på Enable.</span><span class="sxs-lookup"><span data-stu-id="49bd0-130">Click Enable.</span></span>
22. <span data-ttu-id="49bd0-131">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="49bd0-131">Click Yes.</span></span>
23. <span data-ttu-id="49bd0-132">Klik på Find delingsproblemer.</span><span class="sxs-lookup"><span data-stu-id="49bd0-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="49bd0-133">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="49bd0-133">Click Yes.</span></span>
25. <span data-ttu-id="49bd0-134">Klik på Opdater feltværdi.</span><span class="sxs-lookup"><span data-stu-id="49bd0-134">Click Update field value.</span></span>
26. <span data-ttu-id="49bd0-135">Klik på Brug værdi fra firma 1.</span><span class="sxs-lookup"><span data-stu-id="49bd0-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="49bd0-136">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="49bd0-136">Refresh the page.</span></span>
28. <span data-ttu-id="49bd0-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="49bd0-137">Close the page.</span></span>


