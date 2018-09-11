--- 
title: Definere kreditorbetalingsbetalinger
description: Konfigurer betalingsbetingelserne kreditorfakturaer.
author: abruer
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 6d9eaf271220437869ff90610e9953a6e2f8a474
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="92654-103">Definere kreditorbetalingsbetalinger</span><span class="sxs-lookup"><span data-stu-id="92654-103">Define vendor payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="92654-104">Konfigurer betalingsbetingelserne kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="92654-104">Set up payment terms for vendor invoices.</span></span> <span data-ttu-id="92654-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="92654-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="92654-106">Gå til Kreditor > Betalingsopsætning > Betalingsbetingelse.</span><span class="sxs-lookup"><span data-stu-id="92654-106">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="92654-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="92654-107">Click New.</span></span>
    * <span data-ttu-id="92654-108">Siden Betalingsbetingelser bruges til at definere, hvordan forfaldsdatoen beregnes.</span><span class="sxs-lookup"><span data-stu-id="92654-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="92654-109">Den bruges ikke til at definere, hvordan kasserabatdatoen beregnes.</span><span class="sxs-lookup"><span data-stu-id="92654-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="92654-110">Indtast en værdi i feltet Betalingsbetingelse.</span><span class="sxs-lookup"><span data-stu-id="92654-110">In the Terms of payment field, type a value.</span></span>
4. <span data-ttu-id="92654-111">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="92654-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="92654-112">Angiv et tal i feltet Dage.</span><span class="sxs-lookup"><span data-stu-id="92654-112">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="92654-113">Det tal, der angives her, skal bruges til at føje til forfaldsdatoen eller til slutningen af den periode, der er identificeret i betalingsmetoden.</span><span class="sxs-lookup"><span data-stu-id="92654-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="92654-114">Hvis du for eksempel vælger Netto, føjes tallet til forfaldsdatoen.</span><span class="sxs-lookup"><span data-stu-id="92654-114">For example, if you select Net, the number will be added to the due date.</span></span> <span data-ttu-id="92654-115">Hvis du vælger Aktuel måned, føjes tallet til den sidste dag i den aktuelle måned til beregning af forfaldsdatoen.</span><span class="sxs-lookup"><span data-stu-id="92654-115">If you select Current month, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="92654-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="92654-116">Click Save.</span></span>
7. <span data-ttu-id="92654-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="92654-117">Close the page.</span></span>
8. <span data-ttu-id="92654-118">Gå til Kreditor > Betalingsopsætning > Kasserabatter.</span><span class="sxs-lookup"><span data-stu-id="92654-118">Go to Accounts payable > Payment setup > Cash discounts.</span></span>
9. <span data-ttu-id="92654-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="92654-119">Click New.</span></span>
10. <span data-ttu-id="92654-120">Angiv et id i feltet Kasserabat.</span><span class="sxs-lookup"><span data-stu-id="92654-120">In the Cash discount field, enter an ID.</span></span>
11. <span data-ttu-id="92654-121">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="92654-121">In the Description field, type a value.</span></span>
12. <span data-ttu-id="92654-122">Hvis leverandøren tilbyder niveauinddelt rabat, skal du vælge den næste kasserabat, når den aktuelle er udløbet.</span><span class="sxs-lookup"><span data-stu-id="92654-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="92654-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="92654-123">Close the page.</span></span>
14. <span data-ttu-id="92654-124">Angiv et tal i feltet Dage.</span><span class="sxs-lookup"><span data-stu-id="92654-124">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="92654-125">Det antal, der er angivet i feltet Dage, skal bruges til at beregne dato for kasserabat ud fra den indstilling, der blev valgt i feltet Netto/Løbende.</span><span class="sxs-lookup"><span data-stu-id="92654-125">The quantity entered in the Days field will be used to calculate the Cash discount date, based on what option was selected in the Net/Current field.</span></span> <span data-ttu-id="92654-126">Hvis der blev valgt Netto, føjes antallet til fakturadatoen for at fastlægge kasserabatdatoen.</span><span class="sxs-lookup"><span data-stu-id="92654-126">If Net was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="92654-127">Hvis der blev valgt Løbende, føjes antallet til slutningen af den aktuelle måned for at fastlægge kasserabatdatoen.</span><span class="sxs-lookup"><span data-stu-id="92654-127">If Current month was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="92654-128">Angiv procenten af kasserabatten i feltet Rabat.</span><span class="sxs-lookup"><span data-stu-id="92654-128">Enter the percentage of the cash discount in the Discount field.</span></span> 
16. <span data-ttu-id="92654-129">Angiv den hovedkonto, som kasserabatten bogføres til for debitorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="92654-129">Enter the main account to which the cash discount will be posted for customer invoices.</span></span>
17. <span data-ttu-id="92654-130">Angiv den hovedkonto, som kasserabatten bogføres til for kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="92654-130">Enter the main account to which the cash discount will be posted for vendor invoices.</span></span>
    * <span data-ttu-id="92654-131">Hvis "Rabatmodkonti" er indstillet til Brug hovedkonto til kreditorrabatter, bruges hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="92654-131">If 'Discount offset accounts' is set to Use main account for vendor discount, then the Main account will be used.</span></span>  <span data-ttu-id="92654-132">Hvis indstillingen er angivet til Konti på fakturalinjerne, bogføres kasserabatten til aktiv/udgiftskonti på fakturalinjerne.</span><span class="sxs-lookup"><span data-stu-id="92654-132">If the option is set to Accounts on the invoice lines, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
18. <span data-ttu-id="92654-133">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="92654-133">Click Save.</span></span>


