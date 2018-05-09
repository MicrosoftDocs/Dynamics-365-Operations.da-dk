--- 
title: "Fastlægge gebyrer for debitorbetaling"
description: Opret betalingsgebyrer for debitorbetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 02449aff2273d30e0d0d847e137e3283aef1839b
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="b8bca-103">Fastlægge gebyrer for debitorbetaling</span><span class="sxs-lookup"><span data-stu-id="b8bca-103">Establish customer payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8bca-104">Opret betalingsgebyrer for debitorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="b8bca-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="b8bca-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="b8bca-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="b8bca-106">Gå til Debitor > Betalingsopsætning > Betalingsgebyr.</span><span class="sxs-lookup"><span data-stu-id="b8bca-106">Go to Accounts receivable > Payments setup > Payment fee.</span></span>
2. <span data-ttu-id="b8bca-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b8bca-107">Click New.</span></span>
3. <span data-ttu-id="b8bca-108">Angiv et gebyr-id i feltet Gebyr-id.</span><span class="sxs-lookup"><span data-stu-id="b8bca-108">In the Fee ID field, enter a Fee ID.</span></span>
    * <span data-ttu-id="b8bca-109">Gebyr-id'et vises i betalingskladder, så gør det så beskrivende, at det fremgår, hvilket gebyr der vurderes.</span><span class="sxs-lookup"><span data-stu-id="b8bca-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="b8bca-110">Skriv et gebyrnavn i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="b8bca-110">In the Name field, enter a fee Name.</span></span>
5. <span data-ttu-id="b8bca-111">Angiv en beskrivelse af gebyret i feltet Gebyrbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b8bca-111">In the Fee description field, enter a description for the fee.</span></span>
6. <span data-ttu-id="b8bca-112">Vælg, om gebyret opkræves til kunden eller en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="b8bca-112">Select whether the fee will be charged to the Customer or a Ledger account.</span></span>
    * <span data-ttu-id="b8bca-113">Hvis kunden har vurderer gebyret, skal du vælge Kunde.</span><span class="sxs-lookup"><span data-stu-id="b8bca-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="b8bca-114">Hvis gebyret skal henføres til din organisation som en udgift, skal du vælge Finans.</span><span class="sxs-lookup"><span data-stu-id="b8bca-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="b8bca-115">For denne opgave skal du vælge Debitor.</span><span class="sxs-lookup"><span data-stu-id="b8bca-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="b8bca-116">Vælg den type kladde, som kan bruge dette betalingsgebyr.</span><span class="sxs-lookup"><span data-stu-id="b8bca-116">Select the type of  journal that can use this payment fee.</span></span>
    * <span data-ttu-id="b8bca-117">Hvis disse gebyrer bruges til debitorbetalinger, vil kladdetypen sandsynligvis være Debitorbetaling.</span><span class="sxs-lookup"><span data-stu-id="b8bca-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="b8bca-118">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b8bca-118">Click Save.</span></span>
9. <span data-ttu-id="b8bca-119">Klik på Opsætning af betalingsgebyr.</span><span class="sxs-lookup"><span data-stu-id="b8bca-119">Click Payment fee setup.</span></span>
    * <span data-ttu-id="b8bca-120">Opsætningen Betalingsgebyr bruges til at definere kriterier for, hvornår betalingsgebyret vil blive vurderet.</span><span class="sxs-lookup"><span data-stu-id="b8bca-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="b8bca-121">Du kan for eksempel definere, at gebyret beregnes, hvis bankkontoen er USMF OPER, og betalingsmetoden er check.</span><span class="sxs-lookup"><span data-stu-id="b8bca-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="b8bca-122">Vælg enten Tabel, Gruppe eller Alle for at definere, hvilke bankkonti der skal pålignes dette gebyr.</span><span class="sxs-lookup"><span data-stu-id="b8bca-122">Select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span>
    * <span data-ttu-id="b8bca-123">Hvis du vælger Alle, kan alle bankkonti blive pålignet dette gebyr.</span><span class="sxs-lookup"><span data-stu-id="b8bca-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="b8bca-124">Hvis du vælger Tabel, kan kun den bankkonto, som du vælger, blive pålignet dette gebyr.</span><span class="sxs-lookup"><span data-stu-id="b8bca-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="b8bca-125">Hvis du vælger Gruppe, kan kun bankkontiene i den valgte bankgruppe blive pålignet dette gebyr.</span><span class="sxs-lookup"><span data-stu-id="b8bca-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="b8bca-126">Vælg enten en bankgruppe eller en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="b8bca-126">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="b8bca-127">Hvis du valgte Tabel, vil opslaget vise bankkonti.</span><span class="sxs-lookup"><span data-stu-id="b8bca-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="b8bca-128">Hvis du valgte Gruppe, vil opslaget vise bankgrupper.</span><span class="sxs-lookup"><span data-stu-id="b8bca-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="b8bca-129">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b8bca-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="b8bca-130">Vælg den betalingsmåde, som dette gebyr skal pålignes for.</span><span class="sxs-lookup"><span data-stu-id="b8bca-130">Select the Method of payment for which this fee will be assessed.</span></span>
    * <span data-ttu-id="b8bca-131">Du kan for eksempel påligne kunderne et gebyr, hvis de betaler via check i stedet for at bruge elektronisk betaling.</span><span class="sxs-lookup"><span data-stu-id="b8bca-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="b8bca-132">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b8bca-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="b8bca-133">Angiv en betalingsvaluta, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="b8bca-133">If relevant, enter a payment currency.</span></span>
    * <span data-ttu-id="b8bca-134">Betalingsvalutaen bruges som et yderligere kriterium for, om gebyret vil blive vurderet.</span><span class="sxs-lookup"><span data-stu-id="b8bca-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="b8bca-135">Banken kan for eksempel opkræve et ekstra gebyr for betalinger i USD, da de normalt kun foretager transaktioner i EUR.</span><span class="sxs-lookup"><span data-stu-id="b8bca-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="b8bca-136">Vælg, om gebyret skal være en procent, et beløb eller et interval.</span><span class="sxs-lookup"><span data-stu-id="b8bca-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="b8bca-137">Angiv enten procent eller beløb af gebyret.</span><span class="sxs-lookup"><span data-stu-id="b8bca-137">Enter either percentage or amount of the fee.</span></span>
    * <span data-ttu-id="b8bca-138">Hvis feltet Procent/Beløb er Procent, angives værdien her som en procent.</span><span class="sxs-lookup"><span data-stu-id="b8bca-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="b8bca-139">Hvis feltet Procent/Beløb er Beløb, vil den værdi, du angiver her, være et beløb.</span><span class="sxs-lookup"><span data-stu-id="b8bca-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="b8bca-140">Hvis feltet Procent/Beløb er Interval, kan du bruge fanen Interval til at definere niveauerne.</span><span class="sxs-lookup"><span data-stu-id="b8bca-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="b8bca-141">Vælg valutaen for gebyret i feltet Valuta for gebyr.</span><span class="sxs-lookup"><span data-stu-id="b8bca-141">In the Fee currency field, select the currency of the fee.</span></span>
    * <span data-ttu-id="b8bca-142">Dette er den valuta, som gebyret vil blive oprettet i.</span><span class="sxs-lookup"><span data-stu-id="b8bca-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="b8bca-143">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b8bca-143">Click Save.</span></span>


