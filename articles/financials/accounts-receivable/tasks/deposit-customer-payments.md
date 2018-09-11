--- 
title: Deponere debitorbetalinger
description: Deponer debitorbetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: e40a468373a3358bba9eff328a774c3f65242226
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="deposit-customer-payments"></a><span data-ttu-id="8a5b7-103">Deponere debitorbetalinger</span><span class="sxs-lookup"><span data-stu-id="8a5b7-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a5b7-104">Deponer debitorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-104">Deposit customer payments.</span></span> <span data-ttu-id="8a5b7-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="8a5b7-106">Gå til Kreditor > Betalinger > Betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="8a5b7-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-107">Click New.</span></span>
3. <span data-ttu-id="8a5b7-108">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8a5b7-109">Vælg betalingskladden.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="8a5b7-110">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-110">Click Lines.</span></span>
6. <span data-ttu-id="8a5b7-111">Vælg den debitor, du registrerer betalingen for, i feltet Konto.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="8a5b7-112">Angiv beløbet i betalingen i feltet Kredit.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="8a5b7-113">Du kan vælge at undlade at udfylde beløbet og få systemet til at beregne det ved at vælge de fakturaer, der blev betalt.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="8a5b7-114">Indtast en værdi i feltet Betalingsreference.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="8a5b7-115">Betalingsreferencen kunne være checknummeret for den betaling, som du indtaster.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="8a5b7-116">Betalingsreferencen er påkrævet, hvis betalingen skal medtages på et indbetalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="8a5b7-117">Marker afkrydsningsfeltet Brug et indbetalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="8a5b7-118">Hvis betalingen skal medtages i indbetalingen, kan du ændre indstillingen til Ja.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="8a5b7-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-119">Click New.</span></span>
11. <span data-ttu-id="8a5b7-120">Vælg kunden for den næste betaling i feltet Konto.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="8a5b7-121">Angiv betalingsbeløbet i feltet Kredit.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="8a5b7-122">Indtast en værdi i feltet Betalingsreference.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="8a5b7-123">Marker afkrydsningsfeltet Brug et indbetalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="8a5b7-124">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-124">Click Post.</span></span>
    * <span data-ttu-id="8a5b7-125">Betalinger skal bogføres, før der kan oprettes et indbetalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="8a5b7-126">Dette er for at sikre, at betalingerne ikke ændres, når der genereres et indbetalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="8a5b7-127">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-127">Click Functions.</span></span>
17. <span data-ttu-id="8a5b7-128">Klik på Indbetalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="8a5b7-129">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-129">Click OK.</span></span>
    * <span data-ttu-id="8a5b7-130">Den første side bruges til at oprette et indbetalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="8a5b7-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-131">Click OK.</span></span>
    * <span data-ttu-id="8a5b7-132">Det andet trin er at udskrive indbetalingsbilaget, men dette trin er ikke påkrævet.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-132">The second step is to print the deposit slip, but this step is not required.</span></span>  


