---
title: Konfigurere intern projektfakturering
description: Dette emne viser, hvordan du opsætter projektfakturering mellem to firmaer i organisationen.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c89b17c09a4f145b5a4ca9cdd127b4e635447d4b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174437"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="cbf1f-103">Konfigurere intern projektfakturering</span><span class="sxs-lookup"><span data-stu-id="cbf1f-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cbf1f-104">Dette emne viser, hvordan du opsætter projektfakturering mellem to firmaer i organisationen.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="cbf1f-105">Denne opgave bruger USSI-datasættet.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="cbf1f-106">Gå i navigationsruden til **Moduler > Kreditor > Kreditorer > Alle kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="cbf1f-107">Find og vælg den ønskede post på listen **Alle kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="cbf1f-108">Vælg **Generelt** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="cbf1f-109">Vælg **Intern handel**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="cbf1f-110">Indstil **Aktiv** til **Ja** for at aktivere intern handel.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="cbf1f-111">Indtast eller vælg en værdi i feltet **Kundens firma**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="cbf1f-112">Indtast eller vælg en værdi i feltet **Min konto**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="cbf1f-113">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-113">Select **Save**.</span></span>
9. <span data-ttu-id="cbf1f-114">Luk siderne for at vende tilbage til startsiden.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="cbf1f-115">Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Opsætning > Parametre for projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="cbf1f-116">Vælg fanen **Intern handel**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="cbf1f-117">Flyt skyderen til **Ja** for at aktivere intern ressourceplanlægning og timesedler.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="cbf1f-118">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="cbf1f-119">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-119">Select **New**.</span></span>
15. <span data-ttu-id="cbf1f-120">Indtast eller vælg en værdi i feltet **Udlånt til (juridisk enhed)**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="cbf1f-121">Markér afkrydsningsfeltet **Periodiser omsætning**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="cbf1f-122">Indtast eller vælg en værdi i feltet **Standardtimeseddelkategori**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="cbf1f-123">Indtast eller vælg en værdi i feltet **Standardudgiftskategori**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="cbf1f-124">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-124">Select **Save**.</span></span>
20. <span data-ttu-id="cbf1f-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-125">Close the page.</span></span>
21. <span data-ttu-id="cbf1f-126">Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Opsætning > Postering > Opsætning af finanskontering**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="cbf1f-127">Vælg en indstilling i feltet **Finanskontotyper**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="cbf1f-128">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-128">Select **New**.</span></span>
24. <span data-ttu-id="cbf1f-129">Angiv de ønskede værdier i feltet **Hovedkonto** for den nye række.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="cbf1f-130">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-130">Select **Save**.</span></span>
26. <span data-ttu-id="cbf1f-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-131">Close the page.</span></span>
27. <span data-ttu-id="cbf1f-132">Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Overfør pris**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="cbf1f-133">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-133">Select **New**.</span></span>
29. <span data-ttu-id="cbf1f-134">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="cbf1f-135">Indtast eller vælg en værdi i feltet **Udlånt til (juridisk enhed)**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="cbf1f-136">Vælg en indstilling i feltet **Overfør prismodel**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="cbf1f-137">Angiv et tal i feltet **Prissætning**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="cbf1f-138">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-138">Select **Save**.</span></span>

