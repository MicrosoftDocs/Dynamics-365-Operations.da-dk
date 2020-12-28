---
title: Oprette og bogføre en fritekstfaktura for en debitor i den offentlige sektor
description: Denne procedure hjælper dig med at oprette og bogføre en fritekstfaktura for en debitor ved hjælp af elektronisk OIOUBL-fakturering.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, ContactPersonLookup, CustPostInvoiceJob
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Denmark
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35e515bb5b95e88f821996b5940d48512f83cb00
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407715"
---
# <a name="create-and-post-a-free-text-invoice-for-a-public-sector-customer"></a><span data-ttu-id="b054b-103">Oprette og bogføre en fritekstfaktura for en debitor i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="b054b-103">Create and post a free text invoice for a public sector customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b054b-104">Denne procedure hjælper dig med at oprette og bogføre en fritekstfaktura for en debitor ved hjælp af elektronisk OIOUBL-fakturering.</span><span class="sxs-lookup"><span data-stu-id="b054b-104">This procedure walks you through creating and posting a free text invoice for a customer using OIOUBL electronic invoicing.</span></span> 



<span data-ttu-id="b054b-105">Den blev oprettet ved hjælp af demodatafirmaet USMF med primær adresse for en juridisk enhed i Danmark.</span><span class="sxs-lookup"><span data-stu-id="b054b-105">It was created using the demo data company USMF with a legal entity primary address in Denmark.</span></span>



<span data-ttu-id="b054b-106">Det er den fjerde af seks procedurer, der viser den afsluttende proces til oprettelse af e-fakturaer ved hjælp af elektroniske rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="b054b-106">This is the fourth procedure out of six illustrating end to end process of generating e-invoices using electronic reporting configurations.</span></span> <span data-ttu-id="b054b-107">Den er baseret på OIOUBL-e-fakturaen, der er fælles for Danmark, Østrig og Norge.</span><span class="sxs-lookup"><span data-stu-id="b054b-107">It is based on OIOUBL e-invoice example which is common for Denmark, Austria and Norway.</span></span> <span data-ttu-id="b054b-108">Du kan finde mindre forskelle for andre landespecifikke e-fakturaimplementeringer, som spansk eller italiensk, i tilgængelige WIKI-artikler.</span><span class="sxs-lookup"><span data-stu-id="b054b-108">In order to find minor differences for other country specific e-Invoice implementations, like Spanish or Italian, please refer to available WIKI articles.</span></span>



<span data-ttu-id="b054b-109">Før du kan udføre denne procedure, skal du udføre følgende procedurer: 'Importere elektroniske rapporteringskonfigurationer for elektronisk OIOUBL-fakturering', 'Konfigurere elektronisk OIOUBL-fakturering' og 'Konfigurere en debitorkonto til elektronisk OIOUBL-fakturering'.</span><span class="sxs-lookup"><span data-stu-id="b054b-109">Before you can complete this procedure, you must complete the following procedures: 'Import OIOUBL electronic invoicing electronic reporting configurations', 'Set up OIOUBL electronic invoicing' and 'Set up a customer account for OIOUBL electronic invoicing'.</span></span>

1. <span data-ttu-id="b054b-110">Gå til Debitor > Fakturaer > Alle fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="b054b-110">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="b054b-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b054b-111">Click New.</span></span>
3. <span data-ttu-id="b054b-112">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="b054b-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="b054b-113">En kunde, der er valgt til fritekstfakturaen, skal være aktiveret til elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="b054b-113">A customer selected for the free text invoice must be enabled for electronic invoicing.</span></span>  
4. <span data-ttu-id="b054b-114">Vælg en visning for overskrift for fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="b054b-114">Select a free text invoice header view.</span></span>
5. <span data-ttu-id="b054b-115">Udvid afsnittet Kunde.</span><span class="sxs-lookup"><span data-stu-id="b054b-115">Expand the Customer section.</span></span>
6. <span data-ttu-id="b054b-116">Skriv en værdi i feltet Debitorrekvisition.</span><span class="sxs-lookup"><span data-stu-id="b054b-116">In the Customer requisition field, type a value.</span></span>
7. <span data-ttu-id="b054b-117">Skriv en værdi i feltet Kundereference.</span><span class="sxs-lookup"><span data-stu-id="b054b-117">In the Customer reference field, type a value.</span></span>
8. <span data-ttu-id="b054b-118">Indtast eller vælg en værdi i feltet Kontakt.</span><span class="sxs-lookup"><span data-stu-id="b054b-118">In the Contact field, enter or select a value.</span></span>
9. <span data-ttu-id="b054b-119">Vælg en visning for fritekstfakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="b054b-119">Select a free text invoice lines view.</span></span>
10. <span data-ttu-id="b054b-120">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b054b-120">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="b054b-121">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b054b-121">In the Description field, type a value.</span></span>
12. <span data-ttu-id="b054b-122">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="b054b-122">In the Main account field, specify the desired values.</span></span>
13. <span data-ttu-id="b054b-123">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="b054b-123">In the Unit price field, enter a number.</span></span>
14. <span data-ttu-id="b054b-124">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="b054b-124">Click Post.</span></span>
15. <span data-ttu-id="b054b-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b054b-125">Click OK.</span></span>

## <a name="generate-an-oioubl-electronic-invoice"></a><span data-ttu-id="b054b-126">Oprette en elektronisk OIOUBL faktura</span><span class="sxs-lookup"><span data-stu-id="b054b-126">Generate an OIOUBL electronic invoice</span></span>
1. <span data-ttu-id="b054b-127">Klik på Send.</span><span class="sxs-lookup"><span data-stu-id="b054b-127">Click Send.</span></span>
2. <span data-ttu-id="b054b-128">Klik på Oprindelig.</span><span class="sxs-lookup"><span data-stu-id="b054b-128">Click Original.</span></span>
    * <span data-ttu-id="b054b-129">Du kan kontrollere jobstatus og hente den faktiske fil på siden Elektroniske rapporteringsjob.</span><span class="sxs-lookup"><span data-stu-id="b054b-129">You can verify the status of the job and download the actual file on the Electronic reporting jobs page.</span></span>  

