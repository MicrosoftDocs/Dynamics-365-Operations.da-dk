---
title: Afstemme fragt manuelt
description: Denne procedure viser, hvordan du afstemmer fragt manuelt.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc4fc51955544df4d0156a4c83bcc5b5a0e13df3
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425002"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="e5681-103">Afstemme fragt manuelt</span><span class="sxs-lookup"><span data-stu-id="e5681-103">Reconcile freight manually</span></span>

<span data-ttu-id="e5681-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="e5681-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="e5681-105">Denne procedure viser, hvordan du afstemmer fragt manuelt.</span><span class="sxs-lookup"><span data-stu-id="e5681-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="e5681-106">Denne konfiguration vil normalt blive udført af en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="e5681-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="e5681-107">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="e5681-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="e5681-108">Vælg en last, der skal afstemmes</span><span class="sxs-lookup"><span data-stu-id="e5681-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="e5681-109">Gå til Transportstyring > Planlægning > Lastplanlægningspanel.</span><span class="sxs-lookup"><span data-stu-id="e5681-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="e5681-110">Fjern markeringen i afkrydsningsfeltet Skjul leverede og modtagne.</span><span class="sxs-lookup"><span data-stu-id="e5681-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="e5681-111">Vælg på listen den last, som har last-id'et 00006.</span><span class="sxs-lookup"><span data-stu-id="e5681-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="e5681-112">Oprette en faktura fra fragtmand</span><span class="sxs-lookup"><span data-stu-id="e5681-112">Create a carrier invoice</span></span>
<span data-ttu-id="e5681-113">Hvis du manuelt afstemmer fragt og ikke automatisk modtager fakturaer fra fragtmænd, kan du oprette en faktura ud fra fragtbrevet.</span><span class="sxs-lookup"><span data-stu-id="e5681-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="e5681-114">Klik på Relaterede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="e5681-114">Click Related information.</span></span>
2. <span data-ttu-id="e5681-115">Klik på Fragtbrevsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="e5681-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="e5681-116">Klik på Generér fragtbrevsfaktura.</span><span class="sxs-lookup"><span data-stu-id="e5681-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="e5681-117">Skriv en værdi i feltet Faktura.</span><span class="sxs-lookup"><span data-stu-id="e5681-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="e5681-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e5681-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="e5681-119">Afstem fakturaen</span><span class="sxs-lookup"><span data-stu-id="e5681-119">Reconcile the invoice</span></span>
<span data-ttu-id="e5681-120">Når du afstemmer en fragtfaktura og et fragtbrev, kan du gøre det linje for linje.</span><span class="sxs-lookup"><span data-stu-id="e5681-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="e5681-121">Klik på Afstem fragtbreve og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="e5681-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="e5681-122">Udvid sektionen Fakturadetaljer.</span><span class="sxs-lookup"><span data-stu-id="e5681-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="e5681-123">Udvid sektionen Oplysninger om uafstemte fragtbreve.</span><span class="sxs-lookup"><span data-stu-id="e5681-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="e5681-124">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e5681-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="e5681-125">Klik på Afstem.</span><span class="sxs-lookup"><span data-stu-id="e5681-125">Click Match.</span></span>
6. <span data-ttu-id="e5681-126">Udvid sektionen Oplysninger om afstemte fragtbreve.</span><span class="sxs-lookup"><span data-stu-id="e5681-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="e5681-127">Send fakturaen til godkendelse</span><span class="sxs-lookup"><span data-stu-id="e5681-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="e5681-128">Klik på Send til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="e5681-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="e5681-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5681-129">Close the page.</span></span>
3. <span data-ttu-id="e5681-130">Fjern markeringen i afkrydsningsfeltet Skjul godkendte.</span><span class="sxs-lookup"><span data-stu-id="e5681-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="e5681-131">Klik på Kreditorfakturajournaler.</span><span class="sxs-lookup"><span data-stu-id="e5681-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="e5681-132">Klik for at følge linket i feltet Referencekladdenummer.</span><span class="sxs-lookup"><span data-stu-id="e5681-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="e5681-133">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="e5681-133">Click Lines.</span></span>

