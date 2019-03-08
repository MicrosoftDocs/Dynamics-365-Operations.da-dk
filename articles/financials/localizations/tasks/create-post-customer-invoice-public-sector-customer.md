---
title: Oprette og bogføre en debitorfaktura for en debitor i den offentlige sektor
description: Denne procedure hjælper dig med at oprette og bogføre en salgsordrefaktura for en debitor ved hjælp af elektronisk OIOUBL-fakturering.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, ContactPersonLookup, SalesEditLines,  CustInvoiceJournal, ERFormatMappingRunJobTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Denmark
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99b46c536f0e8ee0872d01969869d3e59e875142
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "370302"
---
# <a name="create-and-post-a-customer-invoice-for-a-public-sector-customer"></a><span data-ttu-id="68440-103">Oprette og bogføre en debitorfaktura for en debitor i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="68440-103">Create and post a customer invoice for a public sector customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="68440-104">Denne procedure hjælper dig med at oprette og bogføre en salgsordrefaktura for en debitor ved hjælp af elektronisk OIOUBL-fakturering.</span><span class="sxs-lookup"><span data-stu-id="68440-104">This procedure walks you through creating and posting a sales order invoice for a customer using OIOUBL electronic invoicing.</span></span> 



<span data-ttu-id="68440-105">Den blev oprettet ved hjælp af demodatafirmaet USMF med primær adresse for en juridisk enhed i Danmark.</span><span class="sxs-lookup"><span data-stu-id="68440-105">It was created using the demo data company USMF with a legal entity primary address in Denmark.</span></span>



<span data-ttu-id="68440-106">Det er den femte af seks procedurer, der viser den afsluttende proces til oprettelse af e-fakturaer ved hjælp af elektroniske rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="68440-106">This is the fifth procedure out of six illustrating end to end process of generating e-invoices using electronic reporting configurations.</span></span> <span data-ttu-id="68440-107">Den er baseret på OIOUBL-e-fakturaen, der er fælles for Danmark, Østrig og Norge.</span><span class="sxs-lookup"><span data-stu-id="68440-107">It is based on OIOUBL e-invoice example which is common for Denmark, Austria and Norway.</span></span> <span data-ttu-id="68440-108">Du kan finde mindre forskelle for andre landespecifikke e-fakturaimplementeringer, som spansk eller italiensk, i tilgængelige WIKI-artikler.</span><span class="sxs-lookup"><span data-stu-id="68440-108">In order to find minor differences for other country specific e-Invoice implementations, like Spanish or Italian, please refer to available WIKI articles.</span></span>



<span data-ttu-id="68440-109">Før du kan udføre denne procedure, skal du udføre følgende procedurer: 'Importere elektroniske rapporteringskonfigurationer for elektronisk OIOUBL-fakturering', 'Konfigurere elektronisk OIOUBL-fakturering' og 'Konfigurere en debitorkonto til elektronisk OIOUBL-fakturering'.</span><span class="sxs-lookup"><span data-stu-id="68440-109">Before you can complete this procedure, you must complete the following procedures: ‘Import OIOUBL electronic invoicing electronic reporting configurations’, ‘Set up OIOUBL electronic invoicing’ and ‘Set up a customer account for OIOUBL electronic invoicing’.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="68440-110">Oprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="68440-110">Create a sales order</span></span>
1. <span data-ttu-id="68440-111">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="68440-111">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="68440-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="68440-112">Click New.</span></span>
3. <span data-ttu-id="68440-113">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="68440-113">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="68440-114">Vælg en kunde, der er aktiveret til elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="68440-114">Select a customer that is enabled for electronic invoicing.</span></span>  
4. <span data-ttu-id="68440-115">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="68440-115">Click OK.</span></span>
5. <span data-ttu-id="68440-116">Vælg en visning for salgsordreoverskrift.</span><span class="sxs-lookup"><span data-stu-id="68440-116">Select a sales order header view.</span></span>
6. <span data-ttu-id="68440-117">Indtast eller vælg en værdi i feltet Kontakt.</span><span class="sxs-lookup"><span data-stu-id="68440-117">In the Contact field, enter or select a value.</span></span>
7. <span data-ttu-id="68440-118">Skriv en værdi i feltet Debitorrekvisition.</span><span class="sxs-lookup"><span data-stu-id="68440-118">In the Customer requisition field, type a value.</span></span>
8. <span data-ttu-id="68440-119">Skriv en værdi i feltet Kundereference.</span><span class="sxs-lookup"><span data-stu-id="68440-119">In the Customer reference field, type a value.</span></span>
9. <span data-ttu-id="68440-120">Udvid sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="68440-120">Expand the Setup section.</span></span>
10. <span data-ttu-id="68440-121">Vælg en visning for salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="68440-121">Select a sales order line view.</span></span>
11. <span data-ttu-id="68440-122">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="68440-122">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="68440-123">Du kan bruge varenummer 'D0001'.</span><span class="sxs-lookup"><span data-stu-id="68440-123">You may use an item number 'D0001'.</span></span>  
12. <span data-ttu-id="68440-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="68440-124">Click Save.</span></span>

## <a name="post-an-invoice-for-a-sales-order"></a><span data-ttu-id="68440-125">Bogføre en faktura for en salgsordre</span><span class="sxs-lookup"><span data-stu-id="68440-125">Post an invoice for a sales order</span></span>
1. <span data-ttu-id="68440-126">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="68440-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="68440-127">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="68440-127">Click Invoice.</span></span>
3. <span data-ttu-id="68440-128">Udvid sektionen Parametre.</span><span class="sxs-lookup"><span data-stu-id="68440-128">Expand the Parameters section.</span></span>
4. <span data-ttu-id="68440-129">Vælg "Alle" i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="68440-129">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="68440-130">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="68440-130">Click OK.</span></span>
6. <span data-ttu-id="68440-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="68440-131">Click OK.</span></span>

## <a name="generate-oioubl-electronic-invoice"></a><span data-ttu-id="68440-132">Oprette elektronisk OIOUBL faktura</span><span class="sxs-lookup"><span data-stu-id="68440-132">Generate OIOUBL electronic invoice</span></span>
1. <span data-ttu-id="68440-133">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="68440-133">Click Invoice.</span></span>
2. <span data-ttu-id="68440-134">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="68440-134">On the Action Pane, click Invoice.</span></span>
3. <span data-ttu-id="68440-135">Klik på Send.</span><span class="sxs-lookup"><span data-stu-id="68440-135">Click Send.</span></span>
4. <span data-ttu-id="68440-136">Klik på Oprindelig.</span><span class="sxs-lookup"><span data-stu-id="68440-136">Click Original.</span></span>

## <a name="view-an-oioubl-electronic-invoice"></a><span data-ttu-id="68440-137">Se en elektronisk OIOUBL faktura</span><span class="sxs-lookup"><span data-stu-id="68440-137">View an OIOUBL electronic invoice</span></span>
1. <span data-ttu-id="68440-138">Gå til Virksomhedsadministration > Elektronisk rapportering > Elektroniske rapporteringsjob.</span><span class="sxs-lookup"><span data-stu-id="68440-138">Go to Organization administration > Electronic reporting > Electronic reporting jobs.</span></span>
2. <span data-ttu-id="68440-139">Klik på Vis filer.</span><span class="sxs-lookup"><span data-stu-id="68440-139">Click Show files.</span></span>
3. <span data-ttu-id="68440-140">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="68440-140">Click Open.</span></span>

