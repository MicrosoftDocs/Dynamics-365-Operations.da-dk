---
title: Oprette en kladdepostering ved hjælp af en skabelon
description: Bogførte kladdebilag kan gemmes som bilagsskabeloner og anvendes i et nyt kladdebilag.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a749740b62e39202d502a112f947679f85ca085
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "316803"
---
# <a name="create-a-journal-entry-using-template"></a><span data-ttu-id="dab66-103">Oprette en kladdepostering ved hjælp af en skabelon</span><span class="sxs-lookup"><span data-stu-id="dab66-103">Create a journal entry using template</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dab66-104">Bogførte kladdebilag kan gemmes som bilagsskabeloner og anvendes i et nyt kladdebilag.</span><span class="sxs-lookup"><span data-stu-id="dab66-104">Posted journal vouchers can be saved as Voucher templates and applied in a new journal voucher.</span></span> <span data-ttu-id="dab66-105">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="dab66-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="dab66-106">Finans > Kladdeposteringer > Finanskladder.</span><span class="sxs-lookup"><span data-stu-id="dab66-106">General ledger > Journal entries > General journals.</span></span> <span data-ttu-id="dab66-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="dab66-107">Click New.</span></span>
    * <span data-ttu-id="dab66-108">Denne procedure starter med at oprette og bogføre et kladdebilag, men alle tidligere bogførte kladdebilag kan gemmes som en skabelon.</span><span class="sxs-lookup"><span data-stu-id="dab66-108">This procedure starts by creating and posting a journal voucher, but any previously posted journal voucher can be saved as a template.</span></span>  
2. <span data-ttu-id="dab66-109">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="dab66-109">In the Name field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="dab66-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="dab66-110">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="dab66-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="dab66-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="dab66-112">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="dab66-112">Click Lines.</span></span>
6. <span data-ttu-id="dab66-113">Angiv en konto for kontotypen.</span><span class="sxs-lookup"><span data-stu-id="dab66-113">Enter an account for the Account type.</span></span>
7. <span data-ttu-id="dab66-114">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="dab66-114">In the Description field, type a value.</span></span>
8. <span data-ttu-id="dab66-115">Indtast et beløb i feltet Debet.</span><span class="sxs-lookup"><span data-stu-id="dab66-115">Enter an amount in the Debit field.</span></span>
9. <span data-ttu-id="dab66-116">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="dab66-116">Click New.</span></span>
10. <span data-ttu-id="dab66-117">Angiv en anden konto for kontotypen.</span><span class="sxs-lookup"><span data-stu-id="dab66-117">Enter a different account for the Account type.</span></span>
11. <span data-ttu-id="dab66-118">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="dab66-118">In the Description field, type a value.</span></span>
12. <span data-ttu-id="dab66-119">Indtast et beløb i feltet Debet.</span><span class="sxs-lookup"><span data-stu-id="dab66-119">Enter an amount in the Debit field.</span></span>
13. <span data-ttu-id="dab66-120">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="dab66-120">Click New.</span></span>
14. <span data-ttu-id="dab66-121">I feltet Konto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="dab66-121">In the Account field, specify the desired values.</span></span>
15. <span data-ttu-id="dab66-122">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="dab66-122">In the Description field, type a value.</span></span>
16. <span data-ttu-id="dab66-123">Angiv et beløb i feltet Kredit for at afstemme bilaget.</span><span class="sxs-lookup"><span data-stu-id="dab66-123">Enter an amount in the Credit field to balance the voucher.</span></span>
17. <span data-ttu-id="dab66-124">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="dab66-124">Click Post.</span></span>
18. <span data-ttu-id="dab66-125">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="dab66-125">Click Functions.</span></span>
19. <span data-ttu-id="dab66-126">Klik på Gem bilagsskabelon.</span><span class="sxs-lookup"><span data-stu-id="dab66-126">Click Save voucher template.</span></span>
20. <span data-ttu-id="dab66-127">Denne procedure forudsætter en procentskabelontype.</span><span class="sxs-lookup"><span data-stu-id="dab66-127">This procedure assumes a Percent Template type.</span></span> <span data-ttu-id="dab66-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="dab66-128">Click OK.</span></span>
    * <span data-ttu-id="dab66-129">• Procent: Beløbene i bilaget konverteres til procentfaktorer, som betyder, at alle beløb kan anvendes, når skabelonen Bilag er valgt.</span><span class="sxs-lookup"><span data-stu-id="dab66-129">• Percent: The amounts in the voucher are converted into percentage factors, which allows any amount to be applied when the Voucher template is selected.</span></span>  <span data-ttu-id="dab66-130">• Beløb: De faktiske beløb gemmes og anvendes.</span><span class="sxs-lookup"><span data-stu-id="dab66-130">• Amount: The actual amounts will be stored and applied.</span></span>  
21. <span data-ttu-id="dab66-131">Klik på Finanskladder.</span><span class="sxs-lookup"><span data-stu-id="dab66-131">Click General journals.</span></span>
22. <span data-ttu-id="dab66-132">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="dab66-132">Click New.</span></span>
23. <span data-ttu-id="dab66-133">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="dab66-133">In the Name field, click the drop-down button to open the lookup.</span></span>
24. <span data-ttu-id="dab66-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="dab66-134">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="dab66-135">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="dab66-135">Click Lines.</span></span>
26. <span data-ttu-id="dab66-136">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="dab66-136">Click Functions.</span></span>
27. <span data-ttu-id="dab66-137">Klik på Vælg bilagsskabelon.</span><span class="sxs-lookup"><span data-stu-id="dab66-137">Click Select voucher template.</span></span>
28. <span data-ttu-id="dab66-138">Find den skabelon, du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="dab66-138">Find the template that you created earlier.</span></span> <span data-ttu-id="dab66-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="dab66-139">Click OK.</span></span>
    * <span data-ttu-id="dab66-140">Du skal muligvis klikke på trinnet Forrige og derefter vælge den rigtige skabelon, hvis der findes en anden skabelon.</span><span class="sxs-lookup"><span data-stu-id="dab66-140">You may need to click Previous step and then select the correct template if other templates exist.</span></span>  
29. <span data-ttu-id="dab66-141">Angiv beløbet, der skal anvendes til bilaget, i feltet Beløb.</span><span class="sxs-lookup"><span data-stu-id="dab66-141">In the Amount field, enter the amount to be applied to the voucher.</span></span>
    * <span data-ttu-id="dab66-142">Beløbsfeltet vises kun, hvis bilagsskabelon er af typen Procent.</span><span class="sxs-lookup"><span data-stu-id="dab66-142">The amount field is only displayed if the voucher template is of type Percent.</span></span>  
30. <span data-ttu-id="dab66-143">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="dab66-143">Click OK.</span></span>

