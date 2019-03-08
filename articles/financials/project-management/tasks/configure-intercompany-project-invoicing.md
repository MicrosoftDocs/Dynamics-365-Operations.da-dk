---
title: Konfigurere intern projektfakturering
description: Denne procedure viser, hvordan du opsætter projektfakturering mellem to firmaer i organisationen.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2fe06978d3a1c41a1133a568cca61df05b49d235
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "352752"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="d4e45-103">Konfigurere intern projektfakturering</span><span class="sxs-lookup"><span data-stu-id="d4e45-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4e45-104">Denne procedure viser, hvordan du opsætter projektfakturering mellem to firmaer i organisationen.</span><span class="sxs-lookup"><span data-stu-id="d4e45-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="d4e45-105">Denne opgave bruger USSI-datasættet.</span><span class="sxs-lookup"><span data-stu-id="d4e45-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="d4e45-106">Gå til Kreditor > Kreditorer > Alle kreditorer.</span><span class="sxs-lookup"><span data-stu-id="d4e45-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="d4e45-107">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d4e45-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d4e45-108">Klik på Generelt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d4e45-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="d4e45-109">Klik på Intern.</span><span class="sxs-lookup"><span data-stu-id="d4e45-109">Click Intercompany.</span></span>
5. <span data-ttu-id="d4e45-110">Indstil Aktiv til Ja for at aktivere intern handel.</span><span class="sxs-lookup"><span data-stu-id="d4e45-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="d4e45-111">Indtast eller vælg en værdi i feltet Kundens firma.</span><span class="sxs-lookup"><span data-stu-id="d4e45-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="d4e45-112">Indtast eller vælg en værdi i feltet Min konto.</span><span class="sxs-lookup"><span data-stu-id="d4e45-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="d4e45-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d4e45-113">Click Save.</span></span>
9. <span data-ttu-id="d4e45-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d4e45-114">Close the page.</span></span>
10. <span data-ttu-id="d4e45-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d4e45-115">Close the page.</span></span>
11. <span data-ttu-id="d4e45-116">Gå til Projektstyring og regnskab > Opsætning > Parametre for projektstyring og regnskab.</span><span class="sxs-lookup"><span data-stu-id="d4e45-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="d4e45-117">Klik på fanen Intern.</span><span class="sxs-lookup"><span data-stu-id="d4e45-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="d4e45-118">Flyt glideren til Ja for at aktivere intern ressourceplanlægning og timesedler.</span><span class="sxs-lookup"><span data-stu-id="d4e45-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="d4e45-119">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d4e45-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="d4e45-120">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d4e45-120">Click New.</span></span>
16. <span data-ttu-id="d4e45-121">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d4e45-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="d4e45-122">Indtast eller vælg en værdi i feltet Udlånt til (juridisk enhed).</span><span class="sxs-lookup"><span data-stu-id="d4e45-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="d4e45-123">Marker afkrydsningsfeltet Periodiser omsætning.</span><span class="sxs-lookup"><span data-stu-id="d4e45-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="d4e45-124">Indtast eller vælg en værdi i feltet Standardtimeseddelkategori.</span><span class="sxs-lookup"><span data-stu-id="d4e45-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="d4e45-125">Indtast eller vælg en værdi i feltet Standardudgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="d4e45-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="d4e45-126">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d4e45-126">Click Save.</span></span>
22. <span data-ttu-id="d4e45-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d4e45-127">Close the page.</span></span>
23. <span data-ttu-id="d4e45-128">Gå til Projektstyring og regnskab > Opsætning > Bogføring > Opsætning af finanskontering.</span><span class="sxs-lookup"><span data-stu-id="d4e45-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="d4e45-129">Vælg en indstilling i feltet Finanskontotyper.</span><span class="sxs-lookup"><span data-stu-id="d4e45-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="d4e45-130">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d4e45-130">Click New.</span></span>
26. <span data-ttu-id="d4e45-131">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d4e45-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="d4e45-132">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d4e45-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="d4e45-133">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="d4e45-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="d4e45-134">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d4e45-134">Click Save.</span></span>
30. <span data-ttu-id="d4e45-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d4e45-135">Close the page.</span></span>
31. <span data-ttu-id="d4e45-136">Gå til Projektstyring og regnskab > Opsætning > Priser > Overfør pris.</span><span class="sxs-lookup"><span data-stu-id="d4e45-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="d4e45-137">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d4e45-137">Click New.</span></span>
33. <span data-ttu-id="d4e45-138">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="d4e45-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="d4e45-139">Indtast eller vælg en værdi i feltet Udlånt til (juridisk enhed).</span><span class="sxs-lookup"><span data-stu-id="d4e45-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="d4e45-140">Vælg en indstilling i feltet Overfør prismodel.</span><span class="sxs-lookup"><span data-stu-id="d4e45-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="d4e45-141">Angiv et tal i feltet Prissætning.</span><span class="sxs-lookup"><span data-stu-id="d4e45-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="d4e45-142">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d4e45-142">Click Save.</span></span>

