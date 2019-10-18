---
title: Tilbageføre kladdebogføring
description: I dette emne beskrives funktioner, der giver mulighed for at tilbageføre bilag fra bilagstransaktionslisten eller fra økonomikladder.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248579"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="3286d-103">Tilbageføre kladdebogføring</span><span class="sxs-lookup"><span data-stu-id="3286d-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3286d-104">Dette emne indeholder en beskrivelser af Microsoft Dynamics 365 Finance-funktioner, der giver dig mulighed for at tilbageføre en hel kladde eller tilbageføre et eller flere bilag fra listen med bilagstransaktioner, uanset deres oprindelse.</span><span class="sxs-lookup"><span data-stu-id="3286d-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="3286d-105">Tilbageføre kladder</span><span class="sxs-lookup"><span data-stu-id="3286d-105">Reversing journals</span></span>

<span data-ttu-id="3286d-106">Du kan tilbageføre kladdelinjer enkeltvist.</span><span class="sxs-lookup"><span data-stu-id="3286d-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="3286d-107">Med tilbageførsel af kladdebogføring kan du også tilbageføre en hel økonomikladde.</span><span class="sxs-lookup"><span data-stu-id="3286d-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="3286d-108">Sådan tilbagefører du en kladde:</span><span class="sxs-lookup"><span data-stu-id="3286d-108">To reverse a journal:</span></span> 
- <span data-ttu-id="3286d-109">Åbn økonomikladden, og filtrer på bogførte kladder</span><span class="sxs-lookup"><span data-stu-id="3286d-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="3286d-110">Klik på menuen Tilbagefør øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="3286d-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="3286d-111">Du kan se det samlede antal bilag og bilagslinjer samt det samlede beløb for de linjer, der tilbageføres</span><span class="sxs-lookup"><span data-stu-id="3286d-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="3286d-112">Vælg Ja for at bruge de eksisterende transaktionsdatoer eller nej for at angive en ny.</span><span class="sxs-lookup"><span data-stu-id="3286d-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="3286d-113">I nogle tilfælde kan perioden for den oprindelige transaktion være lukket, så du skal angive en ny transaktionsdato for tilbageførslen.</span><span class="sxs-lookup"><span data-stu-id="3286d-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="3286d-114">Hvis du har valgt Nej, skal du angive en transaktionsdato for tilbageførslen.</span><span class="sxs-lookup"><span data-stu-id="3286d-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="3286d-115">Indtast en kommentar, der skal føjes til den tilbageførte transaktion</span><span class="sxs-lookup"><span data-stu-id="3286d-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="3286d-116">Klik på knappen Tilbagefør</span><span class="sxs-lookup"><span data-stu-id="3286d-116">Click the Reverse button</span></span>

<span data-ttu-id="3286d-117">Transaktionerne tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="3286d-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="3286d-118">Hvis antallet af bilagslinjer overstiger 100 linjer, køres tilbageførslen ved hjælp af batchprocessen.</span><span class="sxs-lookup"><span data-stu-id="3286d-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="3286d-119">Du kan gennemse resultaterne af tilbageførslen ved at få vist kommentarerne i batchjobbet, der blev kørt.</span><span class="sxs-lookup"><span data-stu-id="3286d-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="3286d-120">Alle fejl vil blive angivet i batchjobbets historik.</span><span class="sxs-lookup"><span data-stu-id="3286d-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="3286d-121">Hvis antallet af bilagslinjer er 100 linjer eller mindre, køres tilbageførselsprocessen med det samme.</span><span class="sxs-lookup"><span data-stu-id="3286d-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="3286d-122">Resultaterne vises i en dialogboks, der viser eventuelle bilag, der ikke kunne tilbageføres, og årsagen til, at de ikke kunne tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="3286d-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="3286d-123">Klik på OK for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="3286d-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="3286d-124">Tilbageførsel af bilag fra listen over bilagstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="3286d-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="3286d-125">Du kan også tilbageføre bilag fra **bilagstransaktionslisten** på tværs af alle reskontroer.</span><span class="sxs-lookup"><span data-stu-id="3286d-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="3286d-126">Derudover kan du tilbageføre mere end ét bilag ad gangen.</span><span class="sxs-lookup"><span data-stu-id="3286d-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="3286d-127">Sådan tilbagefører du et eller flere bilag:</span><span class="sxs-lookup"><span data-stu-id="3286d-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="3286d-128">Klik på menuen Tilbagefør øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="3286d-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="3286d-129">Du kan se det samlede antal bilag og bilagslinjer samt det samlede beløb for de linjer, der tilbageføres</span><span class="sxs-lookup"><span data-stu-id="3286d-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="3286d-130">Vælg Ja for at bruge de eksisterende transaktionsdatoer eller nej for at angive en ny.</span><span class="sxs-lookup"><span data-stu-id="3286d-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="3286d-131">I nogle tilfælde kan perioden for den oprindelige transaktion være lukket, så du skal angive en ny transaktionsdato for tilbageførslen.</span><span class="sxs-lookup"><span data-stu-id="3286d-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="3286d-132">Hvis du har valgt Nej, skal du angive en transaktionsdato for tilbageførslen.</span><span class="sxs-lookup"><span data-stu-id="3286d-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="3286d-133">Indtast en kommentar, der skal føjes til den tilbageførte transaktion</span><span class="sxs-lookup"><span data-stu-id="3286d-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="3286d-134">Klik på knappen Tilbagefør</span><span class="sxs-lookup"><span data-stu-id="3286d-134">Click the Reverse button</span></span>

<span data-ttu-id="3286d-135">Transaktionerne tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="3286d-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="3286d-136">Hvis antallet af bilagslinjer overstiger 100 linjer, køres tilbageførslen ved hjælp af batchprocessen.</span><span class="sxs-lookup"><span data-stu-id="3286d-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="3286d-137">Du kan gennemse resultaterne af tilbageførslen ved at få vist kommentarerne i batchjobbet, der blev kørt.</span><span class="sxs-lookup"><span data-stu-id="3286d-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="3286d-138">Alle fejl vil blive angivet i batchjobbets historik.</span><span class="sxs-lookup"><span data-stu-id="3286d-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="3286d-139">Hvis antallet af bilagslinjer er 100 linjer eller mindre, køres tilbageførselsprocessen med det samme.</span><span class="sxs-lookup"><span data-stu-id="3286d-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="3286d-140">Resultaterne vises i en dialogboks, der viser eventuelle bilag, der ikke kunne tilbageføres, og årsagen til, at de ikke kunne tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="3286d-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="3286d-141">Klik på OK for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="3286d-141">Click on Ok to close the dialog.</span></span>

