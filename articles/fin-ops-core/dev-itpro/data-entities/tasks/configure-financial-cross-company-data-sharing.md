---
title: Konfigurere økonomisk datadeling på tværs af firmaer
description: Denne procedure viser, hvordan du kan konfigurere, aktivere, validere og løse konflikter ved deling af data mellem virksomheder.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 98eeae9f50238aae172e4a217d40be39ee46a0b8
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142955"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="abf80-103">Konfigurere økonomisk datadeling på tværs af firmaer</span><span class="sxs-lookup"><span data-stu-id="abf80-103">Configure financial cross-company data sharing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="abf80-104">Denne procedure viser, hvordan du kan konfigurere, aktivere, validere og løse konflikter ved deling af data mellem virksomheder.</span><span class="sxs-lookup"><span data-stu-id="abf80-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="abf80-105">Den anvender USMF-virksomheden og skabelonen til deling af økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="abf80-105">It uses the USMF company and the Financial data sharing template.</span></span>

<span data-ttu-id="abf80-106">Denne opgavevejledning kræver Dynamics AX-platform 7.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="abf80-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="abf80-107">Gå til **Navigationsrude > Moduler > Systemadministration > Arbejdsområder > Datastyring**.</span><span class="sxs-lookup"><span data-stu-id="abf80-107">Go to **Navigation pane > Modules > System administration > Workspaces > Data management**.</span></span>
2. <span data-ttu-id="abf80-108">Klik på **Importér**.</span><span class="sxs-lookup"><span data-stu-id="abf80-108">Click **Import**.</span></span>
3. <span data-ttu-id="abf80-109">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="abf80-109">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="abf80-110">Vælg typen 'Pakke' i feltet **Kildedataformat**.</span><span class="sxs-lookup"><span data-stu-id="abf80-110">In the **Source data format** field, select the 'Package' type.</span></span> <span data-ttu-id="abf80-111">Klik på **Overfør**.</span><span class="sxs-lookup"><span data-stu-id="abf80-111">Click **Upload**.</span></span> <span data-ttu-id="abf80-112">Naviger til placeringen af pakkefilen for skabelonen til deling af økonomiske data, og vælg filen.</span><span class="sxs-lookup"><span data-stu-id="abf80-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>
5. <span data-ttu-id="abf80-113">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="abf80-113">Click **Save**.</span></span>
6. <span data-ttu-id="abf80-114">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="abf80-114">In the list, mark the selected row.</span></span> <span data-ttu-id="abf80-115">Vælg den politik for datadeling, der netop er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="abf80-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="abf80-116">Klik på **Importér**.</span><span class="sxs-lookup"><span data-stu-id="abf80-116">Click **Import**.</span></span>
8. <span data-ttu-id="abf80-117">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="abf80-117">Click **Close**.</span></span>
9. <span data-ttu-id="abf80-118">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="abf80-118">Refresh the page.</span></span>
10. <span data-ttu-id="abf80-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="abf80-119">Close the page.</span></span>
11. <span data-ttu-id="abf80-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="abf80-120">Close the page.</span></span>
12. <span data-ttu-id="abf80-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="abf80-121">Close the page.</span></span>
13. <span data-ttu-id="abf80-122">Gå til **Navigationsrude > Moduler > Systemadministration > Opsætning > Konfigurer datadeling på tværs af firma**.</span><span class="sxs-lookup"><span data-stu-id="abf80-122">Go to **Navigation pane > Modules > System administration > Setup > Configure cross-company data sharing**.</span></span>
14. <span data-ttu-id="abf80-123">Find og vælg **Betalingsdage** på listen.</span><span class="sxs-lookup"><span data-stu-id="abf80-123">In the list, find and select **Payment days**.</span></span>
15. <span data-ttu-id="abf80-124">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="abf80-124">Click **Add**.</span></span>
16. <span data-ttu-id="abf80-125">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="abf80-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="abf80-126">Skriv 'USSI' i feltet **Firma**.</span><span class="sxs-lookup"><span data-stu-id="abf80-126">In the **Company** field, type 'USSI'.</span></span>
18. <span data-ttu-id="abf80-127">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="abf80-127">Click **Add**.</span></span>
19. <span data-ttu-id="abf80-128">Skriv 'USMF' i feltet **Firma**.</span><span class="sxs-lookup"><span data-stu-id="abf80-128">In the **Company** field, type 'USMF'.</span></span>
20. <span data-ttu-id="abf80-129">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="abf80-129">Click **Save**.</span></span>
21. <span data-ttu-id="abf80-130">Klik på **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="abf80-130">Click **Enable**.</span></span>
22. <span data-ttu-id="abf80-131">Klik på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="abf80-131">Click **Yes**.</span></span>
23. <span data-ttu-id="abf80-132">Klik på **Find delingsproblemer**.</span><span class="sxs-lookup"><span data-stu-id="abf80-132">Click **Find sharing issues**.</span></span>
24. <span data-ttu-id="abf80-133">Klik på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="abf80-133">Click **Yes**.</span></span>
25. <span data-ttu-id="abf80-134">Klik på **Opdater feltværdi**.</span><span class="sxs-lookup"><span data-stu-id="abf80-134">Click **Update field value**.</span></span>
26. <span data-ttu-id="abf80-135">Klik på **Brug værdi fra firma 1**.</span><span class="sxs-lookup"><span data-stu-id="abf80-135">Click **Use value from company 1**.</span></span>
27. <span data-ttu-id="abf80-136">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="abf80-136">Refresh the page.</span></span>
28. <span data-ttu-id="abf80-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="abf80-137">Close the page.</span></span>

