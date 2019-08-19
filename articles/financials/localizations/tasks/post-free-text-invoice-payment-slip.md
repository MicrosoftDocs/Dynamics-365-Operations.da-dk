---
title: Bogføre en fritekstfaktura med et indbetalingskort
description: Du kan bogføre en fritekstfaktura med et vedhæftet indbetalingskort i det angivne format.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, SRSPrintDestinationSettingsForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Denmark
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1a92acfcc0c1a2f575b36e0ed7dafbc688301db
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852616"
---
# <a name="post-a-free-text-invoice-with-a-payment-slip"></a><span data-ttu-id="f06d2-103">Bogføre en fritekstfaktura med et indbetalingskort</span><span class="sxs-lookup"><span data-stu-id="f06d2-103">Post a free text invoice with a payment slip</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f06d2-104">Du kan bogføre en fritekstfaktura med et vedhæftet indbetalingskort i det angivne format.</span><span class="sxs-lookup"><span data-stu-id="f06d2-104">You can post a free text invoice with a payment slip attachment in a specified format.</span></span> <span data-ttu-id="f06d2-105">Indbetalingskortet udskrives med kreditorens id-nummer og fakturanummeret, så indbetalingen kan identificeres.</span><span class="sxs-lookup"><span data-stu-id="f06d2-105">The payment slip is printed with the creditor identification number and invoice number to identify the payment.</span></span>



<span data-ttu-id="f06d2-106">Denne procedure fører dig gennem bogføring af en fritekstfaktura med et indbetalingskort.</span><span class="sxs-lookup"><span data-stu-id="f06d2-106">This procedure walks you through posting a free text invoice with a payment slip.</span></span>



<span data-ttu-id="f06d2-107">Før du kan udføre denne procedure, skal du oprette et indbetalingskortformater og oprette indbetalingskort til kundefakturaer.</span><span class="sxs-lookup"><span data-stu-id="f06d2-107">Before you can complete this procedure, you must set up a payment slip formats and setup payment slip for customer invoices.</span></span> 

<span data-ttu-id="f06d2-108">Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="f06d2-108">This procedure was created using the demo data company DEMF.</span></span> 

<span data-ttu-id="f06d2-109">Denne funktionalitet er kun tilgængelig for juridiske enheder, hvis primære adresse er i Danmark.</span><span class="sxs-lookup"><span data-stu-id="f06d2-109">This functionality is available for legal entities whose primary address is in Denmark.</span></span> 



1. <span data-ttu-id="f06d2-110">Gå til Debitor > Fakturaer > Alle fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="f06d2-110">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="f06d2-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f06d2-111">Click New.</span></span>
3. <span data-ttu-id="f06d2-112">Klik på rullelisten i feltet Kundekonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f06d2-112">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f06d2-113">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f06d2-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f06d2-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f06d2-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f06d2-115">Klik på rullelisten i feltet Valuta for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f06d2-115">In the Currency field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f06d2-116">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f06d2-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f06d2-117">Indbetalingskortet kan kun udskrives for en fritekstfaktura med valutaen danske kroner (DKK).</span><span class="sxs-lookup"><span data-stu-id="f06d2-117">The payment slip can be printed only for free text invoice with currency Danish kroner (DKK).</span></span>  
8. <span data-ttu-id="f06d2-118">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f06d2-118">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f06d2-119">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f06d2-119">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="f06d2-120">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f06d2-120">In the Description field, type a value.</span></span>
11. <span data-ttu-id="f06d2-121">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="f06d2-121">In the Main account field, specify the desired values.</span></span>
12. <span data-ttu-id="f06d2-122">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="f06d2-122">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="f06d2-123">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f06d2-123">Click Save.</span></span>
14. <span data-ttu-id="f06d2-124">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="f06d2-124">Click Post.</span></span>
15. <span data-ttu-id="f06d2-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f06d2-125">Click OK.</span></span>
16. <span data-ttu-id="f06d2-126">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f06d2-126">Click OK.</span></span>

