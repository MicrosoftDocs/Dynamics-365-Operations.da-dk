---
title: Konfigurere firmas bankkonti for ISO20022-kreditoverførsler
description: Denne procedure viser, hvordan du konfigurerer de firmaspecifikke bankkontooplysninger, der kræves til generering af SEPA-betalingsfilen.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a84408ea24e4221b041782b681c2a2bf1bd8436
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552417"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="47914-103">Konfigurere firmas bankkonti for ISO20022-kreditoverførsler</span><span class="sxs-lookup"><span data-stu-id="47914-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47914-104">Denne procedure viser, hvordan du konfigurerer de firmaspecifikke bankkontooplysninger, der kræves til generering af SEPA-betalingsfilen.</span><span class="sxs-lookup"><span data-stu-id="47914-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="47914-105">Du kan angive oplysninger, der kræves for at oprette ISO 20022-kreditoverførselsformatet, men afhængigt af formatet kan der være andre oplysninger, der kræves, såsom firma-id eller sorteringskode.</span><span class="sxs-lookup"><span data-stu-id="47914-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="47914-106">Det demodatafirma, der bruges til at oprette denne procedure, er DEMF.</span><span class="sxs-lookup"><span data-stu-id="47914-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="47914-107">Det er den anden procedure af fem, der illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="47914-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="47914-108">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="47914-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="47914-109">Konfigurer IBAN- og SWIFT-kode</span><span class="sxs-lookup"><span data-stu-id="47914-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="47914-110">Gå til Kontant- og bankstyring > Bankkonti.</span><span class="sxs-lookup"><span data-stu-id="47914-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="47914-111">Brug Quick Filter til at filtrere på feltet Bankkonto med værdien "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="47914-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="47914-112">Klik på DEMF OPER for at åbne bankkontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="47914-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="47914-113">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="47914-113">Click Edit.</span></span>
5. <span data-ttu-id="47914-114">Udvid sektionen Yderligere identifikation.</span><span class="sxs-lookup"><span data-stu-id="47914-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="47914-115">Angiv "DE89370400440532013000" i feltet IBAN.</span><span class="sxs-lookup"><span data-stu-id="47914-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="47914-116">Skriv "DEUTDEFF" i feltet SWIFT-kode.</span><span class="sxs-lookup"><span data-stu-id="47914-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="47914-117">Bemærk, at SWIFT\BIC ikke er påkrævet for mange betalingsformater, men det anbefales at få det registreret for en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="47914-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="47914-118">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="47914-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="47914-119">Konfigurer den juridiske enheds bankkonto</span><span class="sxs-lookup"><span data-stu-id="47914-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="47914-120">Gå til Virksomhedsadministration > Organisationer > Juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="47914-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="47914-121">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="47914-121">Click Edit.</span></span>
3. <span data-ttu-id="47914-122">Udvid sektionen Bankkontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="47914-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="47914-123">Indtast eller vælg en værdi i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="47914-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="47914-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="47914-124">Click Save.</span></span>

