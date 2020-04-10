---
title: Konfigurere kreditorer og kreditorbankkonti for ISO20022-kreditoverførsler
description: Denne fremgangsmåde viser, hvordan du konfigurerer kreditoren og de kreditorspecifikke bankkontooplysninger, der kræves til generering af ISO20022-kreditoroverførsel eller andre betalingsfiler.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4809a352f87cc3d88429461a06dfe36189ed5f31
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138963"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="669c4-103">Konfigurere kreditorer og kreditorbankkonti for ISO20022-kreditoverførsler</span><span class="sxs-lookup"><span data-stu-id="669c4-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="669c4-104">Denne fremgangsmåde viser, hvordan du konfigurerer kreditoren og de kreditorspecifikke bankkontooplysninger, der kræves til generering af ISO20022-kreditoroverførsel eller andre betalingsfiler.</span><span class="sxs-lookup"><span data-stu-id="669c4-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="669c4-105">Det demodatafirma, der bruges til at oprette denne procedure, er DEMF.</span><span class="sxs-lookup"><span data-stu-id="669c4-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="669c4-106">Det er den fjerde procedure af fem, der illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="669c4-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="669c4-107">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="669c4-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="669c4-108">Konfigurer bankoplysninger</span><span class="sxs-lookup"><span data-stu-id="669c4-108">Set up bank details</span></span>
1. <span data-ttu-id="669c4-109">Gå til Kreditor > Kreditorer > Alle kreditorer.</span><span class="sxs-lookup"><span data-stu-id="669c4-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="669c4-110">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="669c4-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="669c4-111">Filtrer f.eks. efter feltet Kreditorkonto med værdien "DE-001".</span><span class="sxs-lookup"><span data-stu-id="669c4-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="669c4-112">Klik på DE-001 åbne kreditoroplysninger.</span><span class="sxs-lookup"><span data-stu-id="669c4-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="669c4-113">Klik på Kreditor i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="669c4-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="669c4-114">Klik på Bankkonti.</span><span class="sxs-lookup"><span data-stu-id="669c4-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="669c4-115">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="669c4-115">Click Edit.</span></span>
    * <span data-ttu-id="669c4-116">Hvis der ikke er nogen bankkonto, skal du oprette en ny.</span><span class="sxs-lookup"><span data-stu-id="669c4-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="669c4-117">Skriv "COBADEFFXXX" i feltet SWIFT-kode.</span><span class="sxs-lookup"><span data-stu-id="669c4-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="669c4-118">Angiv "DE36200400000628808808" i feltet IBAN.</span><span class="sxs-lookup"><span data-stu-id="669c4-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="669c4-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="669c4-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="669c4-120">Konfigurer en betalingsmåde for kreditoren</span><span class="sxs-lookup"><span data-stu-id="669c4-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="669c4-121">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="669c4-121">Click Edit.</span></span>
2. <span data-ttu-id="669c4-122">Vis eller skjul sektionen Betaling.</span><span class="sxs-lookup"><span data-stu-id="669c4-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="669c4-123">Klik på rullelisten i feltet Betalingsmåde for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="669c4-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="669c4-124">Klik på linket i rækken SEPA CT på listen.</span><span class="sxs-lookup"><span data-stu-id="669c4-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="669c4-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="669c4-125">Click Save.</span></span>

