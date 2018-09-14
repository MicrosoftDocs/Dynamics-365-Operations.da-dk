--- 
title: Konfigurere debitorer og debitorbankkonti for direkte ISO20022-debiteringer
description: "Denne opgave fører dig gennem oprettelse af en debitorbankkonto og en bemyndigelsen til direkte kundedebitering, som er nødvendige for at generere en kundebetalingsfil som ISO20022 Direct Debit."
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e7d7d79b1d496223b027d800beca105ecaa0bd4c
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="2e7e7-103">Konfigurere debitorer og debitorbankkonti for direkte ISO20022-debiteringer</span><span class="sxs-lookup"><span data-stu-id="2e7e7-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2e7e7-104">Denne opgave fører dig gennem oprettelse af en debitorbankkonto og en bemyndigelsen til direkte kundedebitering, som er nødvendige for at generere en kundebetalingsfil som ISO20022 Direct Debit.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="2e7e7-105">Afhængigt af de formater for debitorbetalinger, der er konfigureret, kræves der yderligere oplysninger, der ikke er dækket i denne procedure, for en kunde eller en debitorbankkonto.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="2e7e7-106">Denne opgave blev oprettet ved hjælp af demodatafirmaet DEMF med primær adresse for en juridisk enhed i Tyskland.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="2e7e7-107">Det er den fjerde procedure af fem, der illustrerer kundens betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="2e7e7-108">Konfigurer en debitorbankkonto</span><span class="sxs-lookup"><span data-stu-id="2e7e7-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="2e7e7-109">Gå til Debitor > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="2e7e7-110">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2e7e7-111">Filtrer f.eks. efter feltet Konto med værdien "DE-010".</span><span class="sxs-lookup"><span data-stu-id="2e7e7-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="2e7e7-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2e7e7-113">Klik på Kunde i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="2e7e7-114">Klik på Bankkonti.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="2e7e7-115">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-115">Click New.</span></span>
7. <span data-ttu-id="2e7e7-116">Skriv en værdi i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="2e7e7-117">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="2e7e7-118">Du kan f.eks. skrive 'EUR bank'.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="2e7e7-119">Indtast eller vælg en værdi i feltet Bankgrupper.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="2e7e7-120">Skriv en værdi i feltet IBAN.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="2e7e7-121">Skriv f.eks. 'DE36200400000628808808'.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="2e7e7-122">Indtast en værdi i feltet SWIFT-kode.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="2e7e7-123">For eksempel: Angiv "COBADEFFXXX".</span><span class="sxs-lookup"><span data-stu-id="2e7e7-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="2e7e7-124">Bemærk, at SWIFT\BIC ikke er påkrævet for mange betalingsformater, men det anbefales at få det registreret for en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="2e7e7-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-125">Click Save.</span></span>
13. <span data-ttu-id="2e7e7-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-126">Close the page.</span></span>
14. <span data-ttu-id="2e7e7-127">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-127">Click Edit.</span></span>
15. <span data-ttu-id="2e7e7-128">Udvid sektionen Betalingsstandarder.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="2e7e7-129">Indtast eller vælg en værdi i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="2e7e7-130">Tilføj en bemyndigelse til direkte debet</span><span class="sxs-lookup"><span data-stu-id="2e7e7-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="2e7e7-131">Udvid sektionen Bemyndigelser til Direct Debit.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="2e7e7-132">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-132">Click Add.</span></span>
3. <span data-ttu-id="2e7e7-133">Indtast eller vælg en værdi i feltet Kreditors bankkonto.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="2e7e7-134">Vælg for eksempel DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="2e7e7-135">Angiv en dato i feltet Dato for signatur.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="2e7e7-136">Klik på Ja for at bekræfte datoopdateringen.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="2e7e7-137">Indtast eller vælg en værdi i feltet Sted for signatur.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="2e7e7-138">Angiv et tal i feltet Forventet antal betalinger.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="2e7e7-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-139">Click OK.</span></span>
9. <span data-ttu-id="2e7e7-140">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2e7e7-140">Click Save.</span></span>


