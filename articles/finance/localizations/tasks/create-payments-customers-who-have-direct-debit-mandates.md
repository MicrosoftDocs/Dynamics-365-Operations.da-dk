---
title: Oprette betalinger til en debitor, som har bemyndigelser til direkte debitering
description: Denne procedure viser, hvordan du opretter en ISO20022-fil med direkte debiteringsbetalinger for en kunde, der har direkte debitering konfigureret og en faktura, der skal betales.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a4714f1f1b24554684219fc1d766b4b87cff7bb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441658"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="6618b-103">Oprette betalinger til en debitor, som har bemyndigelser til direkte debitering</span><span class="sxs-lookup"><span data-stu-id="6618b-103">Create payments for a customer who have direct debit mandates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6618b-104">Denne procedure viser, hvordan du opretter en ISO20022-fil med direkte debiteringsbetalinger for en kunde, der har direkte debitering konfigureret og en faktura, der skal betales.</span><span class="sxs-lookup"><span data-stu-id="6618b-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="6618b-105">Oprettelse og bogføring af en faktura er valgfrit.</span><span class="sxs-lookup"><span data-stu-id="6618b-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="6618b-106">I stedet for at en faktura, der skal betales, kan du vælge en bemyndigelse i en kladde, før du genererer en betalingsfil, for at understøtte et scenario for en kundes forudbetaling.</span><span class="sxs-lookup"><span data-stu-id="6618b-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="6618b-107">Det demodatafirma, der bruges til at oprette denne procedure, er DEMF.</span><span class="sxs-lookup"><span data-stu-id="6618b-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="6618b-108">Det er den femte af fem procedurer, der viser processen til debitorbetaling ved hjælp af elektroniske rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="6618b-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="6618b-109">Før du kan fuldføre denne opgave, skal du udføre alle tidligere opgaver.</span><span class="sxs-lookup"><span data-stu-id="6618b-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="6618b-110">Du skal først importere elektroniske rapporteringskonfigurationer for debitorbetaling, konfigurere betalingsmetode, og du skal konfigurere dine virksomheds- og kundeoplysninger.</span><span class="sxs-lookup"><span data-stu-id="6618b-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="6618b-111">Bogføre en fritekstfaktura med et direkte debiteringsoplysninger</span><span class="sxs-lookup"><span data-stu-id="6618b-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="6618b-112">Gå til Debitor > Fakturaer > Alle fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="6618b-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="6618b-113">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6618b-113">Click New.</span></span>
3. <span data-ttu-id="6618b-114">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="6618b-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="6618b-115">Vælg f.eks. DE-010.</span><span class="sxs-lookup"><span data-stu-id="6618b-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="6618b-116">Indtast eller vælg en værdi i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="6618b-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="6618b-117">F.eks.:</span><span class="sxs-lookup"><span data-stu-id="6618b-117">For example.</span></span> <span data-ttu-id="6618b-118">Vælg Elektronisk.</span><span class="sxs-lookup"><span data-stu-id="6618b-118">select Electronic.</span></span>  
5. <span data-ttu-id="6618b-119">Indtast eller vælg en værdi i feltet Id for bemyndigelse til Direct Debit.</span><span class="sxs-lookup"><span data-stu-id="6618b-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="6618b-120">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="6618b-120">Click Add line.</span></span>
7. <span data-ttu-id="6618b-121">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6618b-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="6618b-122">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="6618b-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="6618b-123">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="6618b-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="6618b-124">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="6618b-124">Click Post.</span></span>
11. <span data-ttu-id="6618b-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6618b-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="6618b-126">Oprette en betaling</span><span class="sxs-lookup"><span data-stu-id="6618b-126">Create a payment</span></span>
1. <span data-ttu-id="6618b-127">Gå til Kreditor > Betalinger > Betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="6618b-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="6618b-128">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6618b-128">Click New.</span></span>
3. <span data-ttu-id="6618b-129">Indtast eller vælg en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6618b-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="6618b-130">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="6618b-130">Click Lines.</span></span>
5. <span data-ttu-id="6618b-131">Klik på Betalingsforslag.</span><span class="sxs-lookup"><span data-stu-id="6618b-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="6618b-132">Klik på Opret betalingsforslag.</span><span class="sxs-lookup"><span data-stu-id="6618b-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="6618b-133">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="6618b-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="6618b-134">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="6618b-134">Click Filter.</span></span>
9. <span data-ttu-id="6618b-135">Markér rækken for tabellen Debitorposter og feltet metoden Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="6618b-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="6618b-136">Du kan anvende et hvilket som helst kriterie for valg af debitorposteringer, der skal betales.</span><span class="sxs-lookup"><span data-stu-id="6618b-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="6618b-137">I dette eksempel kan du bruge Elektronisk som en betalingsmåde for at filtrere posteringer.</span><span class="sxs-lookup"><span data-stu-id="6618b-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="6618b-138">Indtast eller vælg en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="6618b-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="6618b-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6618b-139">Click OK.</span></span>
12. <span data-ttu-id="6618b-140">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6618b-140">Click OK.</span></span>
13. <span data-ttu-id="6618b-141">Klik på Opret betalinger.</span><span class="sxs-lookup"><span data-stu-id="6618b-141">Click Create payments.</span></span>
