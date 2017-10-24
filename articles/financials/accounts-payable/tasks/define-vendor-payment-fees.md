--- 
title: Definere kreditorbetalingsgebyrer
description: Konfigurer kreditorbetalingsgebyrer.
author: abruer
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
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f62d07ffa1ee4a525f0f266922bc88e5ac8d5ada
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="eb8db-103">Definere kreditorbetalingsgebyrer</span><span class="sxs-lookup"><span data-stu-id="eb8db-103">Define vendor payment fees</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb8db-104">Konfigurer kreditorbetalingsgebyrer.</span><span class="sxs-lookup"><span data-stu-id="eb8db-104">Set up vendor payment fees.</span></span> <span data-ttu-id="eb8db-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="eb8db-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="eb8db-106">Gå til Kreditor > Betalingsopsætning > Betalingsgebyr.</span><span class="sxs-lookup"><span data-stu-id="eb8db-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="eb8db-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="eb8db-107">Click New.</span></span>
3. <span data-ttu-id="eb8db-108">Indtast en værdi i feltet Gebyr-id.</span><span class="sxs-lookup"><span data-stu-id="eb8db-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="eb8db-109">Gebyr-id skal beskrive, hvor dette gebyr skal bruges, f.eks. "EFT_Fee".</span><span class="sxs-lookup"><span data-stu-id="eb8db-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="eb8db-110">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="eb8db-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="eb8db-111">Indtast en værdi i feltet Gebyrbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="eb8db-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="eb8db-112">Tilføj en beskrivelse for at give flere detaljer om, hvornår gebyret pålignes.</span><span class="sxs-lookup"><span data-stu-id="eb8db-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="eb8db-113">Vælg enten kreditor eller finans i feltet Gebyr.</span><span class="sxs-lookup"><span data-stu-id="eb8db-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="eb8db-114">Finans bruges, når gebyret skal være udgiftsført til organisationen.</span><span class="sxs-lookup"><span data-stu-id="eb8db-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="eb8db-115">Kreditor bruges, når gebyret vil blive pålignet kreditoren.</span><span class="sxs-lookup"><span data-stu-id="eb8db-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="eb8db-116">Angiv en hovedkonto for, hvor gebyret være udgiftsført.</span><span class="sxs-lookup"><span data-stu-id="eb8db-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="eb8db-117">Denne indstilling kan kun vælges, når Finans vælges i indstillingen Gebyr.</span><span class="sxs-lookup"><span data-stu-id="eb8db-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="eb8db-118">Vælg den kladde, som dette gebyr kan bruges i.</span><span class="sxs-lookup"><span data-stu-id="eb8db-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="eb8db-119">For et betalingsgebyr for en kreditor skal du vælge kladden "Kreditorbetaling".</span><span class="sxs-lookup"><span data-stu-id="eb8db-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="eb8db-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="eb8db-120">Click Save.</span></span>
10. <span data-ttu-id="eb8db-121">Klik på Opsætning af betalingsgebyr.</span><span class="sxs-lookup"><span data-stu-id="eb8db-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="eb8db-122">Fortsæt til opsætningen Betalingsgebyr for at definere, hvornår gebyret skal bruges som standard i den kladde, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="eb8db-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="eb8db-123">Vælg enten Tabel, Gruppe eller Alle.</span><span class="sxs-lookup"><span data-stu-id="eb8db-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="eb8db-124">Tabellen bruges til at vælge en enkelt bankkonto. Gruppe bruges til at vælge en bankgruppe, og Alle er til brug af denne gebyropsætning for alle bankkonti</span><span class="sxs-lookup"><span data-stu-id="eb8db-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="eb8db-125">Vælg enten en bankgruppe eller en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="eb8db-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="eb8db-126">Opslaget viser bankgruppe, hvis du har valgt Gruppe og vil vise bankkonti, hvis du har valgt Tabel.</span><span class="sxs-lookup"><span data-stu-id="eb8db-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="eb8db-127">Vælg betalingsmåden, som dette gebyr pålignes for.</span><span class="sxs-lookup"><span data-stu-id="eb8db-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="eb8db-128">Vælg betalingsspecifikationen for den valgte betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="eb8db-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="eb8db-129">Betalingsspecifikationen bruges med elektronisk pengeoverførsel som betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="eb8db-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="eb8db-130">Vælg, om gebyret er en procent, et beløb eller et interval.</span><span class="sxs-lookup"><span data-stu-id="eb8db-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="eb8db-131">Angiv procentdelen eller beløbet af gebyret.</span><span class="sxs-lookup"><span data-stu-id="eb8db-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="eb8db-132">Hvis gebyret er en procent, kan du indtaste procentdelen.</span><span class="sxs-lookup"><span data-stu-id="eb8db-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="eb8db-133">Hvis gebyret er et beløb, kan du angive beløbet for gebyret.</span><span class="sxs-lookup"><span data-stu-id="eb8db-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="eb8db-134">Hvis gebyret er et interval, skal du bruge fanen Interval til definerede niveauinddelte gebyrer.</span><span class="sxs-lookup"><span data-stu-id="eb8db-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="eb8db-135">I feltet Valuta for gebyr skal du vælge den valuta, som gebyret pålignes i.</span><span class="sxs-lookup"><span data-stu-id="eb8db-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="eb8db-136">Denne valuta er til gebyret.</span><span class="sxs-lookup"><span data-stu-id="eb8db-136">This currency is for the fee.</span></span> <span data-ttu-id="eb8db-137">Betalingsvalutaen bruges til at definere, hvornår gebyrreglen bør pålignes vurderet ud fra betalingens valuta.</span><span class="sxs-lookup"><span data-stu-id="eb8db-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="eb8db-138">Din bank kan for eksempel opkræve et gebyr, når der foretages en betaling i EUR, men alle andre betalinger pålignes ikke et gebyr.</span><span class="sxs-lookup"><span data-stu-id="eb8db-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="eb8db-139">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="eb8db-139">Click Save.</span></span>


