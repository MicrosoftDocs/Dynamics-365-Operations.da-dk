--- 
title: "Konfigurere kreditorer og kreditorbankkonti for ISO20022-kreditoverførsler"
description: "Denne fremgangsmåde viser, hvordan du konfigurerer kreditoren og de kreditorspecifikke bankkontooplysninger, der kræves til generering af ISO20022-kreditoroverførsel eller andre betalingsfiler."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7b489587097f2f10663a7cfb745ce1d17985b432
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="583aa-103">Konfigurere kreditorer og kreditorbankkonti for ISO20022-kreditoverførsler</span><span class="sxs-lookup"><span data-stu-id="583aa-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="583aa-104">Denne fremgangsmåde viser, hvordan du konfigurerer kreditoren og de kreditorspecifikke bankkontooplysninger, der kræves til generering af ISO20022-kreditoroverførsel eller andre betalingsfiler.</span><span class="sxs-lookup"><span data-stu-id="583aa-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="583aa-105">Det demodatafirma, der bruges til at oprette denne procedure, er DEMF.</span><span class="sxs-lookup"><span data-stu-id="583aa-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="583aa-106">Det er den fjerde procedure af fem, der illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="583aa-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="583aa-107">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="583aa-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="583aa-108">Konfigurer bankoplysninger</span><span class="sxs-lookup"><span data-stu-id="583aa-108">Set up bank details</span></span>
1. <span data-ttu-id="583aa-109">Gå til Kreditor > Kreditorer > Alle kreditorer.</span><span class="sxs-lookup"><span data-stu-id="583aa-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="583aa-110">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="583aa-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="583aa-111">Filtrer f.eks. efter feltet Kreditorkonto med værdien "DE-001".</span><span class="sxs-lookup"><span data-stu-id="583aa-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="583aa-112">Klik på DE-001 åbne kreditoroplysninger.</span><span class="sxs-lookup"><span data-stu-id="583aa-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="583aa-113">Klik på Kreditor i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="583aa-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="583aa-114">Klik på Bankkonti.</span><span class="sxs-lookup"><span data-stu-id="583aa-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="583aa-115">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="583aa-115">Click Edit.</span></span>
    * <span data-ttu-id="583aa-116">Hvis der ikke er nogen bankkonto, skal du oprette en ny.</span><span class="sxs-lookup"><span data-stu-id="583aa-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="583aa-117">Skriv "COBADEFFXXX" i feltet SWIFT-kode.</span><span class="sxs-lookup"><span data-stu-id="583aa-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="583aa-118">Angiv "DE36200400000628808808" i feltet IBAN.</span><span class="sxs-lookup"><span data-stu-id="583aa-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="583aa-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="583aa-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="583aa-120">Konfigurer en betalingsmåde for kreditoren</span><span class="sxs-lookup"><span data-stu-id="583aa-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="583aa-121">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="583aa-121">Click Edit.</span></span>
2. <span data-ttu-id="583aa-122">Vis eller skjul sektionen Betaling.</span><span class="sxs-lookup"><span data-stu-id="583aa-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="583aa-123">Klik på rullelisten i feltet Betalingsmåde for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="583aa-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="583aa-124">Klik på linket i rækken SEPA CT på listen.</span><span class="sxs-lookup"><span data-stu-id="583aa-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="583aa-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="583aa-125">Click Save.</span></span>


