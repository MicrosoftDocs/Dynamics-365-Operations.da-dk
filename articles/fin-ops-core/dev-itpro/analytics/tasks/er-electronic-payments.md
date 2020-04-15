---
title: Generere elektroniske dokumenter for betalinger ved hjælp af en formatkonfiguration
description: Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan bruge en ny formatkonfiguration for elektronisk rapportering (ER) til at generere elektroniske dokumenter til behandling af betalinger.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fa39a9d459022e391f99e284d41d82215cc10e2b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142564"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="776c6-103">Generere elektroniske dokumenter for betalinger ved hjælp af en formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="776c6-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="776c6-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan bruge en ny formatkonfiguration for elektronisk rapportering (ER) til at generere elektroniske dokumenter til behandling af betalinger.</span><span class="sxs-lookup"><span data-stu-id="776c6-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="776c6-105">Disse trin kan udføres i GBSI-eksempelfirmaet.</span><span class="sxs-lookup"><span data-stu-id="776c6-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="776c6-106">Du skal først fuldføre proceduren "Opret en konfiguration med format som et betalingsdokument" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="776c6-106">To complete these steps, you must first complete the steps in the "Create a configuration with format of payment document" procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="776c6-107">Ændre konfigurationen af den elektroniske betalingsmåde</span><span class="sxs-lookup"><span data-stu-id="776c6-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="776c6-108">Gå til Kreditor > Opsætning af betaling > Betalingsmåder.</span><span class="sxs-lookup"><span data-stu-id="776c6-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="776c6-109">Skifte sektionen Filformat for at udvide den, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="776c6-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="776c6-110">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="776c6-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="776c6-111">Filtrer for eksempel efter feltet Betalingsmåde med værdien 'Electronic'.</span><span class="sxs-lookup"><span data-stu-id="776c6-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="776c6-112">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="776c6-112">Click Edit.</span></span>
5. <span data-ttu-id="776c6-113">Angiv feltet Generisk elektronisk rapportering til Ja.</span><span class="sxs-lookup"><span data-stu-id="776c6-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="776c6-114">Vælg Ja for at bruge det generelle elektroniske rapporteringsmønster til generering af betalingsfiler.</span><span class="sxs-lookup"><span data-stu-id="776c6-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="776c6-115">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="776c6-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="776c6-116">Vælg formatkonfigurationen BACS (UK fiktivt).</span><span class="sxs-lookup"><span data-stu-id="776c6-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="776c6-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="776c6-117">Click Save.</span></span>
9. <span data-ttu-id="776c6-118">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="776c6-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="776c6-119">Teste formatet for genererede betalingsfiler</span><span class="sxs-lookup"><span data-stu-id="776c6-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="776c6-120">Gå til Kreditor > Betalinger > Betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="776c6-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="776c6-121">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="776c6-121">Click New.</span></span>
3. <span data-ttu-id="776c6-122">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="776c6-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="776c6-123">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="776c6-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="776c6-124">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="776c6-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="776c6-125">Vælg VendPay.</span><span class="sxs-lookup"><span data-stu-id="776c6-125">Select VendPay.</span></span>  
6. <span data-ttu-id="776c6-126">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="776c6-126">Click Save.</span></span>
7. <span data-ttu-id="776c6-127">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="776c6-127">Click Lines.</span></span>
8. <span data-ttu-id="776c6-128">Skriv 'DEMF' i feltet Firma.</span><span class="sxs-lookup"><span data-stu-id="776c6-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="776c6-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="776c6-129">DEMF</span></span>  
9. <span data-ttu-id="776c6-130">I feltet Konto skal du angive værdien "DE-01001".</span><span class="sxs-lookup"><span data-stu-id="776c6-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="776c6-131">DE - 01001</span><span class="sxs-lookup"><span data-stu-id="776c6-131">DE-01001</span></span>  
10. <span data-ttu-id="776c6-132">Skriv 'Betaling' i feltet 'Beskrivelse'.</span><span class="sxs-lookup"><span data-stu-id="776c6-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="776c6-133">Betaling</span><span class="sxs-lookup"><span data-stu-id="776c6-133">Payment</span></span>  
11. <span data-ttu-id="776c6-134">Angiv et tal i feltet Debet.</span><span class="sxs-lookup"><span data-stu-id="776c6-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="776c6-135">1000</span><span class="sxs-lookup"><span data-stu-id="776c6-135">1000</span></span>  
12. <span data-ttu-id="776c6-136">Klik på fanen Betaling.</span><span class="sxs-lookup"><span data-stu-id="776c6-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="776c6-137">Klik på rullelisten i feltet Betalingsmåde for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="776c6-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="776c6-138">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="776c6-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="776c6-139">Vælg den elektroniske værdi.</span><span class="sxs-lookup"><span data-stu-id="776c6-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="776c6-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="776c6-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="776c6-141">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="776c6-141">Click Save.</span></span>
17. <span data-ttu-id="776c6-142">Klik på Generer betalinger.</span><span class="sxs-lookup"><span data-stu-id="776c6-142">Click Generate payments.</span></span>
18. <span data-ttu-id="776c6-143">Klik på rullelisten i feltet Betalingsmåde for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="776c6-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="776c6-144">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="776c6-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="776c6-145">Vælg den elektroniske værdi.</span><span class="sxs-lookup"><span data-stu-id="776c6-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="776c6-146">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="776c6-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="776c6-147">Vælg den elektroniske værdi.</span><span class="sxs-lookup"><span data-stu-id="776c6-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="776c6-148">Skriv en værdi i feltet Filnavn.</span><span class="sxs-lookup"><span data-stu-id="776c6-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="776c6-149">Skriv for eksempel 'betalinger'.</span><span class="sxs-lookup"><span data-stu-id="776c6-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="776c6-150">Klik på rullelisten i feltet Bankkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="776c6-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="776c6-151">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="776c6-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="776c6-152">Vælg værdien GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="776c6-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="776c6-153">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="776c6-153">Click OK.</span></span>
25. <span data-ttu-id="776c6-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="776c6-154">Click OK.</span></span>
    * <span data-ttu-id="776c6-155">Analysér den oprettede betalingsfil i XML-format.</span><span class="sxs-lookup"><span data-stu-id="776c6-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="776c6-156">Sammenlign det med det designede dokumentlayout og de definerede attributter for betalingstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="776c6-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  

