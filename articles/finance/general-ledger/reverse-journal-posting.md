---
title: Tilbageføre kladdebogføring
description: I dette emne beskrives funktioner, der giver mulighed for at tilbageføre bilag fra bilagstransaktionslisten eller fra økonomikladder.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3244d857a9135249130672501f8b766ff9a0680
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441569"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="f21bc-103">Tilbageføre kladdebogføring</span><span class="sxs-lookup"><span data-stu-id="f21bc-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f21bc-104">Dette emne indeholder en beskrivelser af Microsoft Dynamics 365 Finance-funktioner, der giver dig mulighed for at tilbageføre en hel kladde eller tilbageføre et eller flere bilag fra listen med bilagstransaktioner, uanset deres oprindelse.</span><span class="sxs-lookup"><span data-stu-id="f21bc-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="f21bc-105">Tilbageføre kladder</span><span class="sxs-lookup"><span data-stu-id="f21bc-105">Reversing journals</span></span>

<span data-ttu-id="f21bc-106">Du kan tilbageføre kladdelinjer enkeltvist.</span><span class="sxs-lookup"><span data-stu-id="f21bc-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="f21bc-107">Med tilbageførsel af kladdebogføring kan du også tilbageføre en hel økonomikladde.</span><span class="sxs-lookup"><span data-stu-id="f21bc-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="f21bc-108">Sådan tilbagefører du en kladde:</span><span class="sxs-lookup"><span data-stu-id="f21bc-108">To reverse a journal:</span></span> 

- <span data-ttu-id="f21bc-109">Åbn økonomikladden, og filtrer på bogførte kladder.</span><span class="sxs-lookup"><span data-stu-id="f21bc-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="f21bc-110">Vælg menuen **Tilbagefør** øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="f21bc-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="f21bc-111">Du kan se det samlede antal bilag og bilagslinjer samt det samlede beløb for de linjer, der tilbageføres</span><span class="sxs-lookup"><span data-stu-id="f21bc-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="f21bc-112">Vælg **Ja** for at bruge de eksisterende transaktionsdatoer eller **Nej** for at angive en ny.</span><span class="sxs-lookup"><span data-stu-id="f21bc-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="f21bc-113">I nogle tilfælde kan perioden for den oprindelige transaktion være lukket, så du skal angive en ny transaktionsdato for tilbageførslen.</span><span class="sxs-lookup"><span data-stu-id="f21bc-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="f21bc-114">Hvis du har valgt **Nej**, skal du angive en transaktionsdato for tilbageførslen.</span><span class="sxs-lookup"><span data-stu-id="f21bc-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="f21bc-115">Indtast en kommentar, der skal føjes til den tilbageførte transaktion.</span><span class="sxs-lookup"><span data-stu-id="f21bc-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="f21bc-116">Vælg knappen **Tilbagefør**.</span><span class="sxs-lookup"><span data-stu-id="f21bc-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="f21bc-117">Transaktionerne tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="f21bc-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="f21bc-118">Hvis antallet af bilagslinjer overstiger 100 linjer, køres tilbageførslen ved hjælp af batchprocessen.</span><span class="sxs-lookup"><span data-stu-id="f21bc-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="f21bc-119">Du kan gennemse resultaterne ved at få vist kommentarerne i batchjobbet.</span><span class="sxs-lookup"><span data-stu-id="f21bc-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="f21bc-120">Alle transaktioner, der ikke kunne tilbageføres, vises i historikken for batchjobbet.</span><span class="sxs-lookup"><span data-stu-id="f21bc-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="f21bc-121">Hvis antallet af bilagslinjer er 100 linjer eller mindre, køres tilbageførselsprocessen med det samme.</span><span class="sxs-lookup"><span data-stu-id="f21bc-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="f21bc-122">Resultaterne vises i en dialogboks med eventuelle bilag, der ikke kunne tilbageføres, og årsagen til, at de ikke kunne tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="f21bc-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="f21bc-123">Vælg **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f21bc-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="f21bc-124">Tilbageførsel af bilag fra listen over bilagstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="f21bc-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="f21bc-125">Du kan også tilbageføre bilag fra **bilagstransaktionslisten** på tværs af alle reskontroer.</span><span class="sxs-lookup"><span data-stu-id="f21bc-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="f21bc-126">Derudover kan du tilbageføre mere end ét bilag ad gangen.</span><span class="sxs-lookup"><span data-stu-id="f21bc-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="f21bc-127">Sådan tilbagefører du et eller flere bilag:</span><span class="sxs-lookup"><span data-stu-id="f21bc-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="f21bc-128">Vælg menuen **Tilbagefør** øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="f21bc-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="f21bc-129">Du kan se det samlede antal bilag og bilagslinjer samt det samlede beløb for de linjer, der tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="f21bc-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="f21bc-130">Vælg **Ja** for at bruge de eksisterende transaktionsdatoer eller **Nej** for at angive en ny.</span><span class="sxs-lookup"><span data-stu-id="f21bc-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="f21bc-131">I nogle tilfælde kan perioden for den oprindelige transaktion være lukket, så du skal angive en ny transaktionsdato for tilbageførslen.</span><span class="sxs-lookup"><span data-stu-id="f21bc-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="f21bc-132">Hvis du har valgt **Nej**, skal du angive en transaktionsdato for tilbageførslen.</span><span class="sxs-lookup"><span data-stu-id="f21bc-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="f21bc-133">Indtast en kommentar, der beskriver tilbageførselstransaktionen.</span><span class="sxs-lookup"><span data-stu-id="f21bc-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="f21bc-134">Vælg knappen **Tilbagefør**.</span><span class="sxs-lookup"><span data-stu-id="f21bc-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="f21bc-135">Transaktionerne tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="f21bc-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="f21bc-136">Hvis antallet af bilagslinjer overstiger 100, køres tilbageførslen ved hjælp af batchprocessen.</span><span class="sxs-lookup"><span data-stu-id="f21bc-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="f21bc-137">Du kan gennemse resultaterne ved at få vist kommentarerne i batchjobbet.</span><span class="sxs-lookup"><span data-stu-id="f21bc-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="f21bc-138">Alle transaktioner, der ikke kunne tilbageføres, noteres i historikken for batchjobbet.</span><span class="sxs-lookup"><span data-stu-id="f21bc-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="f21bc-139">Hvis antallet af bilagslinjer er 100 linjer eller derunder, køres tilbageførselsprocessen med det samme.</span><span class="sxs-lookup"><span data-stu-id="f21bc-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="f21bc-140">Resultaterne vises i en dialogboks med eventuelle bilag, der ikke kunne tilbageføres, og årsagen hertil.</span><span class="sxs-lookup"><span data-stu-id="f21bc-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="f21bc-141">Vælg **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f21bc-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="f21bc-142">Transaktioner kan kun tilbageføres, hvis de opfylder forretningsreglerne for tilbageførsel af dem.</span><span class="sxs-lookup"><span data-stu-id="f21bc-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="f21bc-143">Kreditorbetalinger kan ikke tilbageføres ved hjælp af den funktion, der er beskrevet i dette emne.</span><span class="sxs-lookup"><span data-stu-id="f21bc-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="f21bc-144">Kreditorbetalinger skal tilbageføres ved at følge trinnene i [Tilbageføre en kreditorbetaling](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span><span class="sxs-lookup"><span data-stu-id="f21bc-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>

