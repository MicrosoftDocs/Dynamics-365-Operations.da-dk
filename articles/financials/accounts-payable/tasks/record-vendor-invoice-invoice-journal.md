---
title: Registrere en kreditorfaktura i fakturakladden
description: Denne opgaveguide viser, hvordan du kan registrere kreditorfakturaer, der ikke er knyttet til indkøbsordrer.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 775f3764d34cecbfc071ff7420d32c7832b42308
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556324"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="4cb5f-103">Registrere en kreditorfaktura i fakturakladden</span><span class="sxs-lookup"><span data-stu-id="4cb5f-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4cb5f-104">Denne opgaveguide viser, hvordan du kan registrere kreditorfakturaer, der ikke er knyttet til indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="4cb5f-105">Eksempler på denne type faktura omfatter udgifter til vareleverancer og tjenesteydelser.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="4cb5f-106">Denne registrering anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="4cb5f-107">Gå til Kreditor > Arbejdsområder > Kreditorfakturapostering.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="4cb5f-108">Klik på Ny fakturakladde.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="4cb5f-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-109">Click New.</span></span>
4. <span data-ttu-id="4cb5f-110">Indtast kladdenavnet eller klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="4cb5f-111">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="4cb5f-112">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-112">Click Lines.</span></span>
    * <span data-ttu-id="4cb5f-113">Indtast den bogføringsdato, der opdaterer Finans, i feltet Dato.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="4cb5f-114">Angiv kreditorkontoen i feltet Konto.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="4cb5f-115">Angiv fakturanummeret i feltet Faktura.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="4cb5f-116">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="4cb5f-117">Angiv et tal i feltet Kredit.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="4cb5f-118">Indtast kontonummeret, eller klik på rullelisten i feltet Modkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="4cb5f-119">Momsgruppen hentes som standard fra kreditorkontoen.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="4cb5f-120">Varemomsgruppen hentes som standard fra den hovedkonto, der er angivet i feltet Modkonto.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="4cb5f-121">Forfaldsdatoen beregnes på basis af betalingsbetingelserne.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="4cb5f-122">Kasserabatten hentes som standard fra kreditorkontoen.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="4cb5f-123">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-123">Click Post.</span></span>
13. <span data-ttu-id="4cb5f-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4cb5f-124">Close the page.</span></span>

