---
title: "Arbejdsområde for kreditorsamarbejdsfakturering"
description: "Dette emne forklarer, hvordan du kan få vist kreditorfakturaer og sende fakturaer fra arbejdsområdet for kreditorsamarbejdsfakturaer."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 6b05dbef279b06fefc1eccd87689693edf2a418e
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="d50ed-103">Arbejdsområde for kreditorsamarbejdsfakturering</span><span class="sxs-lookup"><span data-stu-id="d50ed-103">Vendor collaboration invoicing workspace</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d50ed-104">Dette emne forklarer, hvordan du kan få vist kreditorfakturaer og sende fakturaer fra arbejdsområdet for kreditorsamarbejdsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="d50ed-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="d50ed-105">**Kreditorsamarbejdsfakturaer**-arbejdsområdet kan bruges til at få vist oplysninger om kreditorfakturaen og sende fakturaer til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ved hjælp af arbejdsgangfunktioner.</span><span class="sxs-lookup"><span data-stu-id="d50ed-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="d50ed-106">Arbejdsområde for kreditorsamarbejdsfakturering</span><span class="sxs-lookup"><span data-stu-id="d50ed-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="d50ed-107">Oversigt over felter</span><span class="sxs-lookup"><span data-stu-id="d50ed-107">Summary tiles</span></span>

<span data-ttu-id="d50ed-108">**Oversigt**-fliserne giver en oversigt over fakturaer for den valgte kreditor.</span><span class="sxs-lookup"><span data-stu-id="d50ed-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="d50ed-109">Du kan få vist fakturaer efter deres tilstand.</span><span class="sxs-lookup"><span data-stu-id="d50ed-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="d50ed-110">Udkast til fakturaer er ikke sendt til arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="d50ed-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="d50ed-111">Sendte, ikke godkendte fakturaer er de fakturaer, som kreditoren har sendt, men de er ikke blevet bogført i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d50ed-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in Finance and Operations.</span></span>
-   <span data-ttu-id="d50ed-112">Godkendte, ikke betalte fakturaer er de fakturaer, som er blevet bogført i Finance and Operations, men de er ikke betalt fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="d50ed-112">Approved, not paid invoices are those that have been posted in Finance and Operations, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="d50ed-113">Betalte fakturaer er dem, der er blevet betalt fuldt ud i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d50ed-113">Paid invoices are those that have been fully paid in Finance and Operations.</span></span>

<span data-ttu-id="d50ed-114">Klik på et felt åbner en filtreret visning af siden **Fakturaliste**.</span><span class="sxs-lookup"><span data-stu-id="d50ed-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>
### <a name="tabular-lists"></a><span data-ttu-id="d50ed-115">Tabellister</span><span class="sxs-lookup"><span data-stu-id="d50ed-115">Tabular lists</span></span>

<span data-ttu-id="d50ed-116">I sektionen **Tabellister** er status for fakturering opdelt på samme måde som oversigtsfelterne: kladde og sendt, ikke godkendte lister.</span><span class="sxs-lookup"><span data-stu-id="d50ed-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="d50ed-117">Mens du er i kladdetilstand, kan en faktura sendes til arbejdsgangen eller slettes.</span><span class="sxs-lookup"><span data-stu-id="d50ed-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="d50ed-118">Den sidste tabelliste er en mulighed for at finde fakturaer.</span><span class="sxs-lookup"><span data-stu-id="d50ed-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="d50ed-119">Du kan filtrere, når du søger, for at give mulighed for hurtigere søgninger.</span><span class="sxs-lookup"><span data-stu-id="d50ed-119">You can filter as you search, to allow for faster searches.</span></span>
<span data-ttu-id="d50ed-120">Alle kreditorfakturaer (listeside)</span><span class="sxs-lookup"><span data-stu-id="d50ed-120">All vendor invoices list page</span></span>
-----------------------------

<span data-ttu-id="d50ed-121">Du kan få vist alle bogførte og ikke-bogførte fakturaer på siden med listen **Kreditorsamarbejdsfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="d50ed-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="d50ed-122">Du kan bruge denne listeside til at få vist betalingsstatus for fakturaerne.</span><span class="sxs-lookup"><span data-stu-id="d50ed-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="d50ed-123">Statusserne for betaling omfatter ikke-bogførte, ubetalte, delvist betalte og betalte.</span><span class="sxs-lookup"><span data-stu-id="d50ed-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="d50ed-124">Oprettelse af en ny faktura ud fra en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="d50ed-124">Creating a new invoice from a purchase order</span></span>
--------------------------------------------

<span data-ttu-id="d50ed-125">Du kan oprette en ny kreditorfaktura ved at vælge handlingen **Ny** i **Kreditorsamarbejdsfakturaer**-arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="d50ed-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="d50ed-126">Indkøbsordrenummer og fakturanummer skal oplyses af kreditoren.</span><span class="sxs-lookup"><span data-stu-id="d50ed-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="d50ed-127">Som standard vises alle linjerne fra kreditorens indkøbsordre på den nye faktura.</span><span class="sxs-lookup"><span data-stu-id="d50ed-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="d50ed-128">Oplysninger om antal og omkostninger kan redigeres, inden du sender kreditorfakturaen til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="d50ed-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="d50ed-129">Du kan vedhæfte filer, noter, billeder og URL-adresser til en faktura, inden du sender den.</span><span class="sxs-lookup"><span data-stu-id="d50ed-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>



<span data-ttu-id="d50ed-130">Yderligere oplysninger finder du i [Samarbejde med kreditorer ved hjælp af kreditorportalen](../../supply-chain/procurement/collaborate-vendors-vendor-portal.md)</span><span class="sxs-lookup"><span data-stu-id="d50ed-130">For more information, see [Collaborating with vendors by using the Vendor portal](../../supply-chain/procurement/collaborate-vendors-vendor-portal.md)</span></span>




