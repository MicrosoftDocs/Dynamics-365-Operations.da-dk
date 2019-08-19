---
title: Afstemme fragt manuelt
description: Denne procedure viser, hvordan du afstemmer fragt manuelt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb9c850aa045b72137b8a1d3c8cdae51cf2fd7b6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843235"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="2b4d6-103">Afstemme fragt manuelt</span><span class="sxs-lookup"><span data-stu-id="2b4d6-103">Reconcile freight manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2b4d6-104">Denne procedure viser, hvordan du afstemmer fragt manuelt.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="2b4d6-105">Denne konfiguration vil normalt blive udført af en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="2b4d6-106">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="2b4d6-107">Vælg en last, der skal afstemmes</span><span class="sxs-lookup"><span data-stu-id="2b4d6-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="2b4d6-108">Gå til Transportstyring > Planlægning > Lastplanlægningspanel.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="2b4d6-109">Fjern markeringen i afkrydsningsfeltet Skjul leverede og modtagne.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="2b4d6-110">Vælg på listen den last, som har last-id'et 00006.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="2b4d6-111">Oprette en faktura fra fragtmand</span><span class="sxs-lookup"><span data-stu-id="2b4d6-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="2b4d6-112">Hvis du manuelt afstemmer fragt og ikke automatisk modtager fakturaer fra fragtmænd, kan du oprette en faktura ud fra fragtbrevet.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="2b4d6-113">Klik på Relaterede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-113">Click Related information.</span></span>
2. <span data-ttu-id="2b4d6-114">Klik på Fragtbrevsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="2b4d6-115">Klik på Generér fragtbrevsfaktura.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="2b4d6-116">Skriv en værdi i feltet Faktura.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="2b4d6-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="2b4d6-118">Afstem fakturaen</span><span class="sxs-lookup"><span data-stu-id="2b4d6-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="2b4d6-119">Når du afstemmer en fragtfaktura og et fragtbrev, kan du gøre det linje for linje.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="2b4d6-120">Klik på Afstem fragtbreve og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="2b4d6-121">Udvid sektionen Fakturadetaljer.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="2b4d6-122">Udvid sektionen Oplysninger om uafstemte fragtbreve.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="2b4d6-123">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="2b4d6-124">Klik på Afstem.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-124">Click Match.</span></span>
6. <span data-ttu-id="2b4d6-125">Udvid sektionen Oplysninger om afstemte fragtbreve.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="2b4d6-126">Send fakturaen til godkendelse</span><span class="sxs-lookup"><span data-stu-id="2b4d6-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="2b4d6-127">Klik på Send til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="2b4d6-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-128">Close the page.</span></span>
3. <span data-ttu-id="2b4d6-129">Fjern markeringen i afkrydsningsfeltet Skjul godkendte.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="2b4d6-130">Klik på Kreditorfakturajournaler.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="2b4d6-131">Klik for at følge linket i feltet Referencekladdenummer.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="2b4d6-132">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="2b4d6-132">Click Lines.</span></span>

