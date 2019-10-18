---
title: Oprette en kladdepostering ved hjælp af en skabelon
description: Bogførte kladdebilag kan gemmes som bilagsskabeloner og anvendes i et nyt kladdebilag.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: babbc5ee067743d368680970556f8e5d3d8585f0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176921"
---
# <a name="create-a-journal-entry-using-template"></a><span data-ttu-id="a4947-103">Oprette en kladdepostering ved hjælp af en skabelon</span><span class="sxs-lookup"><span data-stu-id="a4947-103">Create a journal entry using template</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a4947-104">Bogførte kladdebilag kan gemmes som bilagsskabeloner og anvendes i et nyt kladdebilag.</span><span class="sxs-lookup"><span data-stu-id="a4947-104">Posted journal vouchers can be saved as Voucher templates and applied in a new journal voucher.</span></span> <span data-ttu-id="a4947-105">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="a4947-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="a4947-106">Gå til **Navigationsrude > Moduler > Finans > Kladdeposteringer > Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="a4947-106">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
2. <span data-ttu-id="a4947-107">Klik på **Ny** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="a4947-107">On the **Action pane**, click **New**.</span></span> <span data-ttu-id="a4947-108">Denne procedure starter med at oprette og bogføre et kladdebilag, men alle tidligere bogførte kladdebilag kan gemmes som en skabelon.</span><span class="sxs-lookup"><span data-stu-id="a4947-108">This procedure starts by creating and posting a journal voucher, but any previously posted journal voucher can be saved as a template.</span></span>  
3. <span data-ttu-id="a4947-109">Klik på rullelisten i feltet **Navn** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a4947-109">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a4947-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="a4947-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a4947-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a4947-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a4947-112">Klik på **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="a4947-112">Click **Lines**.</span></span>
7. <span data-ttu-id="a4947-113">Skriv en værdi i feltet **Kontotype**.</span><span class="sxs-lookup"><span data-stu-id="a4947-113">In the **Account type** field, type a value.</span></span>
8. <span data-ttu-id="a4947-114">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a4947-114">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="a4947-115">Skriv en værdi i feltet **Debet**.</span><span class="sxs-lookup"><span data-stu-id="a4947-115">In the **Debit** field, type a value.</span></span>
10. <span data-ttu-id="a4947-116">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a4947-116">Click **New**.</span></span>
11. <span data-ttu-id="a4947-117">Skriv en værdi i feltet **Kontotype**.</span><span class="sxs-lookup"><span data-stu-id="a4947-117">In the **Account type** field, type a value.</span></span>
12. <span data-ttu-id="a4947-118">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a4947-118">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="a4947-119">Skriv en værdi i feltet **Debet**.</span><span class="sxs-lookup"><span data-stu-id="a4947-119">In the **Debit** field, type a value.</span></span>
14. <span data-ttu-id="a4947-120">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a4947-120">Click **New**.</span></span>
14. <span data-ttu-id="a4947-121">I feltet **Konto** skal du angive de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="a4947-121">In the **Account** field, specify the desired values.</span></span>
15. <span data-ttu-id="a4947-122">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a4947-122">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="a4947-123">Angiv en værdi i feltet **Kredit** for at afstemme bilaget.</span><span class="sxs-lookup"><span data-stu-id="a4947-123">In the **Credit** field, type a value to balance the voucher.</span></span>
17. <span data-ttu-id="a4947-124">Klik på **Bogfør** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="a4947-124">On the **Action pane**, click **Post**.</span></span>
18. <span data-ttu-id="a4947-125">Klik på **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="a4947-125">Click **Functions**.</span></span>
19. <span data-ttu-id="a4947-126">Klik på **Gem bilagsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="a4947-126">Click **Save voucher** template.</span></span>
20. <span data-ttu-id="a4947-127">Denne procedure forudsætter en **Procentskabelon**-type.</span><span class="sxs-lookup"><span data-stu-id="a4947-127">This procedure assumes a **Percent Template** type.</span></span> <span data-ttu-id="a4947-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a4947-128">Click OK.</span></span>
    - <span data-ttu-id="a4947-129">Procent: Beløbene i bilaget konverteres til procentfaktorer, som betyder, at alle beløb kan anvendes, når skabelonen Bilag er valgt.</span><span class="sxs-lookup"><span data-stu-id="a4947-129">Percent: The amounts in the voucher are converted into percentage factors, which allows any amount to be applied when the Voucher template is selected.</span></span>
    - <span data-ttu-id="a4947-130">Beløb: De faktiske beløb gemmes og anvendes.</span><span class="sxs-lookup"><span data-stu-id="a4947-130">Amount: The actual amounts will be stored and applied.</span></span>  
21. <span data-ttu-id="a4947-131">Klik på **Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="a4947-131">Click **General journals**.</span></span>
22. <span data-ttu-id="a4947-132">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a4947-132">Click **New**.</span></span>
23. <span data-ttu-id="a4947-133">Klik på rullelisten i feltet **Navn** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a4947-133">In the **Name** field, click the drop-down button to open the lookup.</span></span>
24. <span data-ttu-id="a4947-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a4947-134">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="a4947-135">Klik på **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="a4947-135">Click **Lines**.</span></span>
26. <span data-ttu-id="a4947-136">Klik på **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="a4947-136">Click **Functions**.</span></span>
27. <span data-ttu-id="a4947-137">Klik på **Vælg bilagsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="a4947-137">Click **Select voucher template**.</span></span>
28. <span data-ttu-id="a4947-138">Find den skabelon, du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="a4947-138">Find the template that you created earlier.</span></span> <span data-ttu-id="a4947-139">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4947-139">Click **OK**.</span></span> <span data-ttu-id="a4947-140">Du skal muligvis klikke på **Forrige trin** og derefter vælge den rigtige skabelon, hvis der findes en anden skabelon.</span><span class="sxs-lookup"><span data-stu-id="a4947-140">You may need to click **Previous step** and then select the correct template if other templates exist.</span></span>  
29. <span data-ttu-id="a4947-141">Angiv beløbet, der skal anvendes til bilaget, i feltet **Beløb**.</span><span class="sxs-lookup"><span data-stu-id="a4947-141">In the **Amount** field, enter the amount to be applied to the voucher.</span></span> <span data-ttu-id="a4947-142">Feltet **Beløb** vises kun, hvis bilagsskabelon er af typen Procent.</span><span class="sxs-lookup"><span data-stu-id="a4947-142">The **Amount** field is only displayed if the voucher template is of type Percent.</span></span>  
30. <span data-ttu-id="a4947-143">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4947-143">Click **OK**.</span></span>

