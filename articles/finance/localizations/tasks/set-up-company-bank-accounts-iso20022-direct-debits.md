---
title: Konfigurere firmas bankkonti for direkte ISO20022-debiteringer
description: Denne opgave fører dig gennem oprettelse af firmaspecifikke bankkontooplysninger, der skal bruges til generering af kundebetalingsfiler.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89c4a8d3cb504df97bad5679bf12b3cdb5931d95
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185698"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="21bca-103">Konfigurere firmas bankkonti for direkte ISO20022-debiteringer</span><span class="sxs-lookup"><span data-stu-id="21bca-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21bca-104">Denne opgave fører dig gennem oprettelse af firmaspecifikke bankkontooplysninger, der skal bruges til generering af kundebetalingsfiler.</span><span class="sxs-lookup"><span data-stu-id="21bca-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="21bca-105">Denne procedure bruger formatet ISO 20022 for Direct Debit som eksempel.</span><span class="sxs-lookup"><span data-stu-id="21bca-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="21bca-106">Andre formater kan kræve yderligere konfigurationsoplysninger som firma-id eller sorteringskode.</span><span class="sxs-lookup"><span data-stu-id="21bca-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="21bca-107">Denne opgave blev oprettet ved hjælp af demodatafirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="21bca-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="21bca-108">Det er den anden procedure af fem, der illustrerer kundens betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="21bca-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="21bca-109">Konfigurer IBAN- og SWIFT-koderne.</span><span class="sxs-lookup"><span data-stu-id="21bca-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="21bca-110">Gå til Kontant- og bankstyring > Bankkonti.</span><span class="sxs-lookup"><span data-stu-id="21bca-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="21bca-111">Brug Quick Filter til at filtrere på feltet Bankkonto med værdien "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="21bca-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="21bca-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="21bca-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="21bca-113">For eksempel: Klik på "DEMF OPER" for at åbne bankkontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="21bca-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="21bca-114">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="21bca-114">Click Edit.</span></span>
5. <span data-ttu-id="21bca-115">Udvid eller skjul sektionen Yderligere identifikation.</span><span class="sxs-lookup"><span data-stu-id="21bca-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="21bca-116">Skriv en værdi i feltet IBAN.</span><span class="sxs-lookup"><span data-stu-id="21bca-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="21bca-117">Skriv f.eks. 'DE89370400440532013000'.</span><span class="sxs-lookup"><span data-stu-id="21bca-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="21bca-118">Indtast en værdi i feltet SWIFT-kode.</span><span class="sxs-lookup"><span data-stu-id="21bca-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="21bca-119">For eksempel: Angiv "DEUTDEFF".</span><span class="sxs-lookup"><span data-stu-id="21bca-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="21bca-120">Bemærk, at SWIFT\BIC ikke er påkrævet for mange betalingsformater, men det anbefales at få det registreret for en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="21bca-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="21bca-121">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="21bca-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="21bca-122">Konfigurer en bankkonto for den juridiske enhed</span><span class="sxs-lookup"><span data-stu-id="21bca-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="21bca-123">Gå til Virksomhedsadministration > Organisationer > Juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="21bca-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="21bca-124">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="21bca-124">Click Edit.</span></span>
3. <span data-ttu-id="21bca-125">Udvid eller skjul sektionen Bankkontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="21bca-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="21bca-126">Klik på rullelisten i feltet Bankkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="21bca-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="21bca-127">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="21bca-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="21bca-128">For eksempel: Vælg "DEMF OPER"-bankkonto.</span><span class="sxs-lookup"><span data-stu-id="21bca-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="21bca-129">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="21bca-129">Click Save.</span></span>

