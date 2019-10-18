---
title: Bogføre en salgsfaktura med et indbetalingskort
description: Denne procedure fører dig gennem bogføring af en fritekstfaktura med et vedhæftet indbetalingskort i det angivne format.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Denmark
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a80affc8657c6aa6a49ca87c59e24726c457b3f0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175088"
---
# <a name="post-a-sales-invoice-with-a-payment-slip"></a><span data-ttu-id="57349-103">Bogføre en salgsfaktura med et indbetalingskort</span><span class="sxs-lookup"><span data-stu-id="57349-103">Post a sales invoice with a payment slip</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57349-104">Denne procedure fører dig gennem bogføring af en fritekstfaktura med et vedhæftet indbetalingskort i det angivne format.</span><span class="sxs-lookup"><span data-stu-id="57349-104">This procedure walks you through posting a free text invoice with a payment slip attachment in a specified format.</span></span> <span data-ttu-id="57349-105">Indbetalingskortet udskrives med kreditorens id-nummer og fakturanummeret, så indbetalingen kan identificeres.</span><span class="sxs-lookup"><span data-stu-id="57349-105">The payment slip is printed with the creditor identification number and invoice number to identify the payment.</span></span>

<span data-ttu-id="57349-106">Før du kan udføre denne procedure, skal du først oprette et indbetalingskortformat og oprette indbetalingskort til kundefakturaer.</span><span class="sxs-lookup"><span data-stu-id="57349-106">Before you can complete this procedure, you must first set up a payment slip formats and set up payment slips for customer invoices.</span></span> 

<span data-ttu-id="57349-107">Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="57349-107">This procedure was created using the demo data company DEMF.</span></span> <span data-ttu-id="57349-108">Denne funktionalitet er kun tilgængelig for juridiske enheder, hvis primære adresse er i Danmark.</span><span class="sxs-lookup"><span data-stu-id="57349-108">This functionality is available for legal entities whose primary address is in Denmark.</span></span>

1. <span data-ttu-id="57349-109">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="57349-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="57349-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="57349-110">Click New.</span></span>
3. <span data-ttu-id="57349-111">Klik på rullelisten i feltet Kundekonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="57349-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="57349-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="57349-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="57349-113">Du skal først oprette det tilknyttede betalingsbilag i debitorfakturaen for den valgte kunde.</span><span class="sxs-lookup"><span data-stu-id="57349-113">You should set up the associated payment attachment in customer invoice for the selected customer first.</span></span>  
5. <span data-ttu-id="57349-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="57349-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="57349-115">Klik på rullelisten i feltet Valuta for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="57349-115">In the Currency field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="57349-116">Indbetalingskortet kan kun udskrives for salgsordrer med valutaen danske kroner (DKK).</span><span class="sxs-lookup"><span data-stu-id="57349-116">The payment slip can be printed only for sales orders with the currency Danish kroner (DKK).</span></span>  
7. <span data-ttu-id="57349-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="57349-117">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="57349-118">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="57349-118">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="57349-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="57349-119">Click OK.</span></span>
10. <span data-ttu-id="57349-120">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="57349-120">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="57349-121">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="57349-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="57349-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="57349-122">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="57349-123">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="57349-123">Click Save.</span></span>
14. <span data-ttu-id="57349-124">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="57349-124">On the Action Pane, click Invoice.</span></span>
15. <span data-ttu-id="57349-125">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="57349-125">Click Invoice.</span></span>
16. <span data-ttu-id="57349-126">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="57349-126">Click OK.</span></span>
    * <span data-ttu-id="57349-127">Sørg for, at den tilknyttede betaling, der er knyttet til debitorfakturaen, er indstillet til FIK 751 eller FIK 752.</span><span class="sxs-lookup"><span data-stu-id="57349-127">Be sure that the associated payment that is attached to the customer invoice is set to FIK 751 or FIK 752.</span></span>  
17. <span data-ttu-id="57349-128">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="57349-128">Click Yes.</span></span>

