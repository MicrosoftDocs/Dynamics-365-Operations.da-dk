---
title: Oprette en afskrivningskladde for en debitor
description: Denne opgaveguide viser, hvordan du kan konfigurere parametre for afskrivninger og derefter afskrive transaktioner fra siden Rykkere, siden Åbne debitorfakturaer og siden Kunde.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c6526e57cf2ed84161eb7a92c031127bb6c6536a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003295"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="58bfe-103">Oprette en afskrivningskladde for en debitor</span><span class="sxs-lookup"><span data-stu-id="58bfe-103">Create a write-off journal for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58bfe-104">Denne opgaveguide viser, hvordan du kan konfigurere parametre for afskrivninger og derefter afskrive transaktioner fra siden Rykkere, siden Åbne debitorfakturaer og siden Kunde.</span><span class="sxs-lookup"><span data-stu-id="58bfe-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="58bfe-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="58bfe-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="58bfe-106">Konfigurer afskrivningsparametre</span><span class="sxs-lookup"><span data-stu-id="58bfe-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="58bfe-107">Gå til **navigationsruden > Moduler > Kredit og inkasso > Opsætning > Debitorparametre**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="58bfe-108">Klik på fanen **Rykkere**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-108">Click the **Collections** tab.</span></span>
3. <span data-ttu-id="58bfe-109">Udvid eller skjul sektionen **Afskrivning**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-109">Expand or collapse the **Write-off** section.</span></span>
    - <span data-ttu-id="58bfe-110">**Afskrivningskladden** er den finanskladde, der indeholder afskrivningstransaktioner, du opretter.</span><span class="sxs-lookup"><span data-stu-id="58bfe-110">The **Write-off journal** is the general journal that will hold the write-off transactions that you create.</span></span>  
    - <span data-ttu-id="58bfe-111">Du kan knytte en årsagskode til alle afskrivninger.</span><span class="sxs-lookup"><span data-stu-id="58bfe-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="58bfe-112">Du kan overskrive denne standard, når afskrivningen lavet.</span><span class="sxs-lookup"><span data-stu-id="58bfe-112">You can override this default at the time of the write-off.</span></span>  
    - <span data-ttu-id="58bfe-113">Angiv **Separat moms** til Ja, hvis du vil adskille momsen fra den oprindelige transaktion i afskrivningen.</span><span class="sxs-lookup"><span data-stu-id="58bfe-113">Set the **Separate sales tax** to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="58bfe-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58bfe-114">Close the page.</span></span>
5. <span data-ttu-id="58bfe-115">Gå til **Kredit og inkasso > Opsætning > Debitorposteringsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-115">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span> <span data-ttu-id="58bfe-116">Afskrivningskontoen vil blive brugt som udgiftskontoen eller reserveregulering i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="58bfe-116">The write-off account will be used as the expense account or reserve adjustment in the general journal.</span></span>
6. <span data-ttu-id="58bfe-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58bfe-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="58bfe-118">Afskriv hele debitorsaldoen fra siden Aldersfordelte saldi.</span><span class="sxs-lookup"><span data-stu-id="58bfe-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="58bfe-119">Gå til **Kredit > Rykkere > Aldersfordelte saldi**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-119">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="58bfe-120">Marker rækken for den debitor, du vil afskrive.</span><span class="sxs-lookup"><span data-stu-id="58bfe-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="58bfe-121">Du kan for eksempel markere linjen med Birch Company på den.</span><span class="sxs-lookup"><span data-stu-id="58bfe-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="58bfe-122">Klik på **Indsaml** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-122">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="58bfe-123">Klik på **Afskriv**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-123">Click **Write off**.</span></span>
5. <span data-ttu-id="58bfe-124">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-124">Click **OK**.</span></span>
6. <span data-ttu-id="58bfe-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58bfe-125">Close the page.</span></span>
7. <span data-ttu-id="58bfe-126">Gå til **Navigationsrude > Moduler > Finans > Kladdeposteringer > Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-126">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
8. <span data-ttu-id="58bfe-127">Vælg kladdebatchnummeret for den kladde, der indeholder din afskrivning.</span><span class="sxs-lookup"><span data-stu-id="58bfe-127">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="58bfe-128">Der oprettes én linje for at tilbageføre debitorens saldo.</span><span class="sxs-lookup"><span data-stu-id="58bfe-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="58bfe-129">En eller flere linjer oprettes for at bogføre afskrivningen på afskrivningskontoen.</span><span class="sxs-lookup"><span data-stu-id="58bfe-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="58bfe-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58bfe-130">Close the page.</span></span>
10. <span data-ttu-id="58bfe-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58bfe-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="58bfe-132">Afskriv transaktioner fra formen Rykkere.</span><span class="sxs-lookup"><span data-stu-id="58bfe-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="58bfe-133">Gå til **Kredit > Rykkere > Aldersfordelte saldi**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-133">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="58bfe-134">Vælg navnet på den kunde, som har de posteringer, du vil afskrive.</span><span class="sxs-lookup"><span data-stu-id="58bfe-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="58bfe-135">Vælg for eksempel Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="58bfe-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="58bfe-136">Markér rækken for den første transaktion.</span><span class="sxs-lookup"><span data-stu-id="58bfe-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="58bfe-137">Markér rækken for den anden transaktion.</span><span class="sxs-lookup"><span data-stu-id="58bfe-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="58bfe-138">Klik på **Afskriv**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-138">Click **Write off**.</span></span>
6. <span data-ttu-id="58bfe-139">Skriv 'Tab' i feltet **Årsagskommentar**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-139">In the **Reason comment** field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="58bfe-140">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-140">Click **OK**.</span></span>
8. <span data-ttu-id="58bfe-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58bfe-141">Close the page.</span></span>
9. <span data-ttu-id="58bfe-142">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58bfe-142">Close the page.</span></span>
10. <span data-ttu-id="58bfe-143">Gå til **Finans > Kladdeposteringer > Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-143">Go to **General ledger > Journal entries > General journals**.</span></span>
11. <span data-ttu-id="58bfe-144">Vælg kladdebatchnummeret for den kladde, der indeholder din afskrivning.</span><span class="sxs-lookup"><span data-stu-id="58bfe-144">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="58bfe-145">Der oprettes én linje for at tilbageføre debitorens saldo.</span><span class="sxs-lookup"><span data-stu-id="58bfe-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="58bfe-146">En eller flere linjer oprettes for at bogføre afskrivningen på afskrivningskontoen.</span><span class="sxs-lookup"><span data-stu-id="58bfe-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="58bfe-147">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58bfe-147">Close the page.</span></span>
13. <span data-ttu-id="58bfe-148">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58bfe-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="58bfe-149">Afskriv en faktura fra siden Åbne debitorfakturaer</span><span class="sxs-lookup"><span data-stu-id="58bfe-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="58bfe-150">Gå til **navigationsruden > Moduler > Debitor > Fakturaer > Åbne debitorfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-150">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Open customer invoices**.</span></span>
2. <span data-ttu-id="58bfe-151">Markér linjen for en faktura.</span><span class="sxs-lookup"><span data-stu-id="58bfe-151">Mark the line for an invoice.</span></span> <span data-ttu-id="58bfe-152">Du kan for eksempel markere linjen for CIV-000667.</span><span class="sxs-lookup"><span data-stu-id="58bfe-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="58bfe-153">Klik på **Faktura** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-153">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="58bfe-154">Klik på **Afskriv**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-154">Click **Write off**.</span></span>
5. <span data-ttu-id="58bfe-155">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-155">Click **OK**.</span></span>
6. <span data-ttu-id="58bfe-156">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58bfe-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="58bfe-157">Afskriv en debitorsaldo fra siden Kunde.</span><span class="sxs-lookup"><span data-stu-id="58bfe-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="58bfe-158">Gå til **Debitor > Kunder > Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-158">Go to **Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="58bfe-159">Vælg en debitorkonto.</span><span class="sxs-lookup"><span data-stu-id="58bfe-159">Select a customer account.</span></span> <span data-ttu-id="58bfe-160">Vælg for eksempel US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="58bfe-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="58bfe-161">Klik på **Indsaml** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-161">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="58bfe-162">Klik på **Afskriv**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-162">Click **Write off**.</span></span>
5. <span data-ttu-id="58bfe-163">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="58bfe-163">Click **OK**.</span></span>
6. <span data-ttu-id="58bfe-164">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58bfe-164">Close the page.</span></span>

