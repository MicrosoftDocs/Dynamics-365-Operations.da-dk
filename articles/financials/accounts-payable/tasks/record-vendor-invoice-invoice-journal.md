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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97dd03a96389ab22e441acd0af1ad35852570be4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837006"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="7f662-103">Registrere en kreditorfaktura i fakturakladden</span><span class="sxs-lookup"><span data-stu-id="7f662-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f662-104">Denne opgaveguide viser, hvordan du kan registrere kreditorfakturaer, der ikke er knyttet til indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="7f662-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="7f662-105">Eksempler på denne type faktura omfatter udgifter til vareleverancer og tjenesteydelser.</span><span class="sxs-lookup"><span data-stu-id="7f662-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="7f662-106">Denne registrering anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="7f662-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="7f662-107">Gå til **Navigationsrude > Moduler > Kreditorer > Arbejdsområder > Kreditorfakturapostering**.</span><span class="sxs-lookup"><span data-stu-id="7f662-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="7f662-108">I **Handlingsruden** skal du klikke på **Ny fakturakladde**.</span><span class="sxs-lookup"><span data-stu-id="7f662-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="7f662-109">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7f662-109">Click **New**.</span></span>
4. <span data-ttu-id="7f662-110">Indtast kladdenavnet eller klik på rullelisten i feltet **Navn** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="7f662-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="7f662-111">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7f662-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="7f662-112">Klik på **Linjer** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="7f662-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="7f662-113">Indtast den bogføringsdato, der opdaterer Finans, i feltet **Dato**.</span><span class="sxs-lookup"><span data-stu-id="7f662-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="7f662-114">Angiv **Kreditorkontoen** i feltet **Konto**.</span><span class="sxs-lookup"><span data-stu-id="7f662-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="7f662-115">Angiv fakturanummeret i feltet **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="7f662-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="7f662-116">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7f662-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="7f662-117">Angiv et tal i feltet **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="7f662-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="7f662-118">Indtast kontonummeret, eller klik på rullelisten i feltet **Modkonto** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="7f662-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="7f662-119">**Momsgruppe** hentes som standard fra kreditorkontoen.</span><span class="sxs-lookup"><span data-stu-id="7f662-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="7f662-120">**Varemomsgruppen** hentes som standard fra den hovedkonto, der er angivet i feltet **Modkonto**.</span><span class="sxs-lookup"><span data-stu-id="7f662-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="7f662-121">**Forfaldsdatoen** beregnes på basis af betalingsbetingelserne.</span><span class="sxs-lookup"><span data-stu-id="7f662-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="7f662-122">**Kasserabatten** hentes som standard fra kreditorkontoen.</span><span class="sxs-lookup"><span data-stu-id="7f662-122">The **Cash discount** will default from the Vendor account.</span></span>  
12. <span data-ttu-id="7f662-123">Klik på **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="7f662-123">Click **Post**.</span></span>
13. <span data-ttu-id="7f662-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7f662-124">Close the page.</span></span>

