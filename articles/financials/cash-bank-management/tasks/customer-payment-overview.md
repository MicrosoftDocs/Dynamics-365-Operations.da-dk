---
title: Oversigt over debitorbetalinger
description: Denne opgaveguide fører dig gennem forskellige metoder, der bruges til at angive debitorbetalinger.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e82be0d68165f62bbdc72a70b0675c7418b14ae
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "317401"
---
# <a name="customer-payment-overview"></a><span data-ttu-id="141ae-103">Oversigt over debitorbetalinger</span><span class="sxs-lookup"><span data-stu-id="141ae-103">Customer payment overview</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="141ae-104">Denne opgaveguide fører dig gennem forskellige metoder, der bruges til at angive debitorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="141ae-104">This task guide walks through various methods used to enter customer payments.</span></span> <span data-ttu-id="141ae-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="141ae-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="141ae-106">Gå til Kreditor > Betalinger > Betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="141ae-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="141ae-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="141ae-107">Click New.</span></span>
3. <span data-ttu-id="141ae-108">Vælg den betalingskladde, som debitorbetalingerne gemmes i.</span><span class="sxs-lookup"><span data-stu-id="141ae-108">Select the payment journal which the customer payments will be saved.</span></span>
4. <span data-ttu-id="141ae-109">Vælg eller angiv kladden manuelt.</span><span class="sxs-lookup"><span data-stu-id="141ae-109">Select or manually enter the journal.</span></span>
5. <span data-ttu-id="141ae-110">Klik på Angiv debitorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="141ae-110">Click Enter customer payments.</span></span>
    * <span data-ttu-id="141ae-111">Angivelse af debitorbetalinger bruges til at registrere én debitorbetaling ad gangen.</span><span class="sxs-lookup"><span data-stu-id="141ae-111">Enter customer payments is used to record one customer payment at a time.</span></span> <span data-ttu-id="141ae-112">Du angiver betalingsoplysningerne øverst, og derefter kan du markere de fakturaer, der blev betalt med betalingen fra den samme side.</span><span class="sxs-lookup"><span data-stu-id="141ae-112">You enter the payment information at the top, and then you can mark the invoices that were paid by the payment, all from the same page.</span></span>  
6. <span data-ttu-id="141ae-113">Angiv den debitor, du modtog betalingen fra.</span><span class="sxs-lookup"><span data-stu-id="141ae-113">Enter the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="141ae-114">Hvis du ikke kender debitoren, men ved, at en transaktion er blevet betalt, kan du bruge feltet Transaktion til at angive betalingen.</span><span class="sxs-lookup"><span data-stu-id="141ae-114">If you don't know the customer but do know a transaction that was paid, you can use the Transaction field to enter the payment.</span></span> <span data-ttu-id="141ae-115">Angiv eller vælg fakturaen i feltet Transaktion.</span><span class="sxs-lookup"><span data-stu-id="141ae-115">Enter or select the invoice in the Transaction field.</span></span> <span data-ttu-id="141ae-116">Debitoren bliver automatisk valgt som standard, når du har valgt transaktionen.</span><span class="sxs-lookup"><span data-stu-id="141ae-116">The customer will automatically default after you select the transaction.</span></span>  
7. <span data-ttu-id="141ae-117">I feltet Betalingsreference skal du angive en betalingsreference.</span><span class="sxs-lookup"><span data-stu-id="141ae-117">In the Payment reference field, enter a payment reference.</span></span>
    * <span data-ttu-id="141ae-118">Betalingsreferencen kan være debitorens checknummer eller en reference fra kundens elektronisk betaling.</span><span class="sxs-lookup"><span data-stu-id="141ae-118">The payment reference could be the customer's check number or a reference from the customer's electronic payment.</span></span> <span data-ttu-id="141ae-119">Betalingsreferencen er kun påkrævet, hvis du markerer, at betalingen skal medtages på et indbetalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="141ae-119">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="141ae-120">Vælg, om betalingen skal medtages i et indbetalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="141ae-120">Select whether the payment will be included on a deposit slip.</span></span> 
9. <span data-ttu-id="141ae-121">Angiv beløbet på debitorbetalingen.</span><span class="sxs-lookup"><span data-stu-id="141ae-121">Enter the amount of the customer payment.</span></span>
    * <span data-ttu-id="141ae-122">Det indbetalte beløb angives ikke som et standardbeløb.</span><span class="sxs-lookup"><span data-stu-id="141ae-122">The payment amount will not default.</span></span> <span data-ttu-id="141ae-123">Det skal angives manuelt.</span><span class="sxs-lookup"><span data-stu-id="141ae-123">It must be manually entered.</span></span>  
10. <span data-ttu-id="141ae-124">Markér de fakturaer, der er betalt af debitoren.</span><span class="sxs-lookup"><span data-stu-id="141ae-124">Mark the invoices that were paid by the customer.</span></span>
    * <span data-ttu-id="141ae-125">Hvis betalingen er en forudbetaling, behøver du ikke at markere en faktura til udligning.</span><span class="sxs-lookup"><span data-stu-id="141ae-125">If the payment is a prepayment, you are not required to mark any invoices for settlement.</span></span> <span data-ttu-id="141ae-126">Betalingen kan stadig gemmes og bogføres.</span><span class="sxs-lookup"><span data-stu-id="141ae-126">The payment can still be saved and posted.</span></span> <span data-ttu-id="141ae-127">Udligning til en faktura kan foregå på et senere tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="141ae-127">Settlement to an invoice can happen at a later time.</span></span>  
11. <span data-ttu-id="141ae-128">Angiv det samlede beløb på den betaling, der skal udlignes til den markerede faktura</span><span class="sxs-lookup"><span data-stu-id="141ae-128">Enter the amount of the payment that should be settled to the marked invoice.</span></span> 
    * <span data-ttu-id="141ae-129">Dette felt kan bruges, når betalingen er en delvis betaling.</span><span class="sxs-lookup"><span data-stu-id="141ae-129">This field can be used when the payment is for a partial payment.</span></span> <span data-ttu-id="141ae-130">Hvis du ikke indtaster et beløb, fastlægges beløbet, der skal udlignes, automatisk for dig.</span><span class="sxs-lookup"><span data-stu-id="141ae-130">If you don't enter an amount, the amount to settle will automatically be determined for you.</span></span>  
12. <span data-ttu-id="141ae-131">Klik på Gem i kladde.</span><span class="sxs-lookup"><span data-stu-id="141ae-131">Click Save in journal.</span></span>
    * <span data-ttu-id="141ae-132">Før du kan gemme betalingen til kladden, skal du sørge for, at modkontoen er defineret.</span><span class="sxs-lookup"><span data-stu-id="141ae-132">Before you save the payment to the journal, make sure that the offset account is defined.</span></span> <span data-ttu-id="141ae-133">Med Gem i kladde gemmes betalingen, og den flyttes til kladden.</span><span class="sxs-lookup"><span data-stu-id="141ae-133">Using Save in journal will save the payment and move it to the journal.</span></span> <span data-ttu-id="141ae-134">Du kan derefter fortsætte med at angive den næste betaling.</span><span class="sxs-lookup"><span data-stu-id="141ae-134">You can then continue entering the next payment.</span></span>  
13. <span data-ttu-id="141ae-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="141ae-135">Close the page.</span></span>
14. <span data-ttu-id="141ae-136">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="141ae-136">Click Lines.</span></span>
    * <span data-ttu-id="141ae-137">Når du åbner Linjer, kan du se de betalinger, du har registreret på siden på Angiv debitorbetalinger, og som er gemt i kladden.</span><span class="sxs-lookup"><span data-stu-id="141ae-137">When opening Lines, you will see any payments you recorded on the Enter customer payments page and saved into the journal.</span></span> <span data-ttu-id="141ae-138">Du kan også bruge denne side til at angive nye debitorbetalinger eller redigere eksisterende debitorbetalinger, før de bogføres.</span><span class="sxs-lookup"><span data-stu-id="141ae-138">You can also use this page to enter new customer payments, or edit existing customer payment before they are posted.</span></span>  
15. <span data-ttu-id="141ae-139">Klik på Ny for at oprette en anden betaling.</span><span class="sxs-lookup"><span data-stu-id="141ae-139">Click New to create another payment.</span></span> 
16. <span data-ttu-id="141ae-140">Vælg den debitor, du modtog betalingen fra.</span><span class="sxs-lookup"><span data-stu-id="141ae-140">Select the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="141ae-141">Hvis du ikke kender debitoren, men ved, at en faktura er betalt via betalingen, kan du bruge feltet Faktura til manuelt at indtaste eller vælge fakturaen.</span><span class="sxs-lookup"><span data-stu-id="141ae-141">If you don't know the customer but know an invoice paid by the payment, use the Invoice field to manually enter or select the invoice.</span></span> <span data-ttu-id="141ae-142">Debitoren bliver angivet som standard, når fakturaen er valgt.</span><span class="sxs-lookup"><span data-stu-id="141ae-142">The customer will default after the invoice is selected.</span></span>  
17. <span data-ttu-id="141ae-143">Klik på Udlign transaktioner for at markere fakturaer, der er betalt.</span><span class="sxs-lookup"><span data-stu-id="141ae-143">Click Settle transctions to mark invoices that were paid.</span></span>
    * <span data-ttu-id="141ae-144">Du behøver ikke at udligne betalinger til fakturaer.</span><span class="sxs-lookup"><span data-stu-id="141ae-144">You are not required to settle the payment to any invoices.</span></span> <span data-ttu-id="141ae-145">Hvis dette er en forudbetaling, eller hvis du ikke ved, hvilken fakturaen der er betalt, kan du indtaste og bogføre betalingen.</span><span class="sxs-lookup"><span data-stu-id="141ae-145">If this is a prepayment or if you don't know what invoice was paid, you can enter and post the payment.</span></span> <span data-ttu-id="141ae-146">Betalingen kan udlignes med en faktura på et senere tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="141ae-146">The payment can be settled to an invoice at a later point.</span></span>  
18. <span data-ttu-id="141ae-147">Markér fakturaer, der er betalt via betalingen.</span><span class="sxs-lookup"><span data-stu-id="141ae-147">Mark the invoices paid by the payment.</span></span> 
19. <span data-ttu-id="141ae-148">Angiv beløbet på den betaling, der skal udlignes til fakturaen.</span><span class="sxs-lookup"><span data-stu-id="141ae-148">Enter the amount of the payment that will be settled to the invoice.</span></span>
20. <span data-ttu-id="141ae-149">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="141ae-149">Click OK.</span></span>
21. <span data-ttu-id="141ae-150">I feltet Betalingsreference skal du angive en betalingsreference.</span><span class="sxs-lookup"><span data-stu-id="141ae-150">In the Payment reference field, Enter a payment reference.</span></span> <span data-ttu-id="141ae-151">.</span><span class="sxs-lookup"><span data-stu-id="141ae-151">.</span></span>
    * <span data-ttu-id="141ae-152">Betalingsreferencen er kun påkrævet, hvis du markerer, at betalingen skal medtages på et indbetalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="141ae-152">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
22. <span data-ttu-id="141ae-153">Bogfør debitorbetalingerne.</span><span class="sxs-lookup"><span data-stu-id="141ae-153">Post the customer payments.</span></span> 

