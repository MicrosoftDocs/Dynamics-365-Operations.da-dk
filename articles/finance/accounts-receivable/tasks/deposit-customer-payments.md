---
title: Deponere debitorbetalinger
description: Deponer debitorbetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d903f557fbaeb720dd4a34dc1c772be0dcb56eb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140168"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="e5e49-103">Deponere debitorbetalinger</span><span class="sxs-lookup"><span data-stu-id="e5e49-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5e49-104">Deponer debitorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="e5e49-104">Deposit customer payments.</span></span> <span data-ttu-id="e5e49-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="e5e49-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="e5e49-106">Gå til **Navigationsrude > Moduler > Debitor > Betalinger > Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="e5e49-107">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-107">Select **New**.</span></span>
3. <span data-ttu-id="e5e49-108">Vælg **CustPay** i rullemenuen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="e5e49-109">Vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-109">Select **Lines**.</span></span>
5. <span data-ttu-id="e5e49-110">Vælg den kunde, du registrerer betalingen for, i feltet **Konto**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="e5e49-111">Angiv betalingsbeløbet i feltet **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="e5e49-112">Du kan vælge at undlade at udfylde beløbet og få systemet til at beregne det ved at vælge de fakturaer, der blev betalt.</span><span class="sxs-lookup"><span data-stu-id="e5e49-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="e5e49-113">Indtast en værdi i feltet **Betalingsreference**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="e5e49-114">Betalingsreferencen kunne være checknummeret for den betaling, som du indtaster.</span><span class="sxs-lookup"><span data-stu-id="e5e49-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="e5e49-115">Betalingsreferencen er påkrævet, hvis betalingen skal medtages på et indbetalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="e5e49-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="e5e49-116">Marker afkrydsningsfeltet Brug et indbetalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="e5e49-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="e5e49-117">Hvis betalingen skal medtages i indbetalingen, kan du ændre indstillingen til Ja.</span><span class="sxs-lookup"><span data-stu-id="e5e49-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="e5e49-118">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-118">Select **New**.</span></span>
10. <span data-ttu-id="e5e49-119">Vælg kunden for den næste betaling i feltet **Konto**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="e5e49-120">Angiv betalingsbeløbet i feltet **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="e5e49-121">Indtast en værdi i feltet **Betalingsreference**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="e5e49-122">Markér afkrydsningsfeltet **Brug et indbetalingsbilag**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="e5e49-123">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-123">Select **Post**.</span></span> <span data-ttu-id="e5e49-124">Betalinger skal bogføres, før der kan oprettes et indbetalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="e5e49-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="e5e49-125">Dette er for at sikre, at betalingerne ikke ændres, når der genereres et indbetalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="e5e49-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="e5e49-126">Vælg **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-126">Select **Functions**.</span></span>
16. <span data-ttu-id="e5e49-127">Vælg **Indbetalingsbilag**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="e5e49-128">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-128">Select **OK**.</span></span> <span data-ttu-id="e5e49-129">Den første side bruges til at oprette et indbetalingsbilag.</span><span class="sxs-lookup"><span data-stu-id="e5e49-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="e5e49-130">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5e49-130">Select **OK**.</span></span> <span data-ttu-id="e5e49-131">Det andet trin er at udskrive indbetalingsbilaget, men dette trin er ikke påkrævet.</span><span class="sxs-lookup"><span data-stu-id="e5e49-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

