---
title: Registrere en kreditorfaktura i fakturakladden
description: Denne opgaveguide viser, hvordan du kan registrere kreditorfakturaer, der ikke er knyttet til indkøbsordrer.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a60a5959046ca9e953bac80aaeb382d07a267643
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227130"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="e2a18-103">Registrere en kreditorfaktura i fakturakladden</span><span class="sxs-lookup"><span data-stu-id="e2a18-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2a18-104">Denne opgaveguide viser, hvordan du kan registrere kreditorfakturaer, der ikke er knyttet til indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="e2a18-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="e2a18-105">Eksempler på denne type faktura omfatter udgifter til vareleverancer og tjenesteydelser.</span><span class="sxs-lookup"><span data-stu-id="e2a18-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="e2a18-106">Denne registrering anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="e2a18-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="e2a18-107">Gå til **Navigationsrude > Moduler > Kreditorer > Arbejdsområder > Kreditorfakturapostering**.</span><span class="sxs-lookup"><span data-stu-id="e2a18-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="e2a18-108">I **Handlingsruden** skal du klikke på **Ny fakturakladde**.</span><span class="sxs-lookup"><span data-stu-id="e2a18-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="e2a18-109">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e2a18-109">Click **New**.</span></span>
4. <span data-ttu-id="e2a18-110">Indtast kladdenavnet eller klik på rullelisten i feltet **Navn** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="e2a18-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="e2a18-111">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="e2a18-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="e2a18-112">Klik på **Linjer** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="e2a18-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="e2a18-113">Indtast den bogføringsdato, der opdaterer Finans, i feltet **Dato**.</span><span class="sxs-lookup"><span data-stu-id="e2a18-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="e2a18-114">Angiv **Kreditorkontoen** i feltet **Konto**.</span><span class="sxs-lookup"><span data-stu-id="e2a18-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="e2a18-115">Angiv fakturanummeret i feltet **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="e2a18-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="e2a18-116">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="e2a18-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="e2a18-117">Angiv et tal i feltet **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="e2a18-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="e2a18-118">Indtast kontonummeret, eller klik på rullelisten i feltet **Modkonto** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="e2a18-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="e2a18-119">**Momsgruppe** hentes som standard fra kreditorkontoen.</span><span class="sxs-lookup"><span data-stu-id="e2a18-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="e2a18-120">**Varemomsgruppen** hentes som standard fra den hovedkonto, der er angivet i feltet **Modkonto**.</span><span class="sxs-lookup"><span data-stu-id="e2a18-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="e2a18-121">**Forfaldsdatoen** beregnes på basis af betalingsbetingelserne.</span><span class="sxs-lookup"><span data-stu-id="e2a18-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="e2a18-122">**Kasserabatten** hentes som standard fra kreditorkontoen.</span><span class="sxs-lookup"><span data-stu-id="e2a18-122">The **Cash discount** will default from the Vendor account.</span></span>
12. <span data-ttu-id="e2a18-123">Hvis du har aktiveret arbejdsgang for kreditorfakturakladde, skal du klikke på **Aarbejdsgang > Send**.</span><span class="sxs-lookup"><span data-stu-id="e2a18-123">If you have enabled Vendor invoice journal workflow, click **Workflow > Submit**.</span></span>
    * <span data-ttu-id="e2a18-124">Når din afsendelse er godkendt, vil datoen blive forskudt til den første dag i den næste åbne periode, hvis posteringsdatoen for bogføring ligger inden for en periode, der er sat i venteposition eller er lukket for finanskontering.</span><span class="sxs-lookup"><span data-stu-id="e2a18-124">When your submission is approved, the date will be advanced to the first day of the next open period, if the transaction posting date falls within a period that is On hold or Closed for ledger posting.</span></span>
12. <span data-ttu-id="e2a18-125">Klik på **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="e2a18-125">Click **Post**.</span></span>
13. <span data-ttu-id="e2a18-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e2a18-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]