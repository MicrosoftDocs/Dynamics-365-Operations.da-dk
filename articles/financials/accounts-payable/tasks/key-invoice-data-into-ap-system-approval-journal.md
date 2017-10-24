--- 
title: "Indtaste fakturadata under kreditorer ved hjælp af en godkendelseskladde"
description: Denne opgaveguide viser, hvordan du kan bruge indgangsbogen til at oprette fakturaer og derefter bruge godkendelseskladden til at opdatere udgiftskonti.
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 604345d357e5019e334017b2b6d0413f40818acc
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="7575e-103">Indtaste fakturadata under kreditorer ved hjælp af en godkendelseskladde</span><span class="sxs-lookup"><span data-stu-id="7575e-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7575e-104">Denne opgaveguide viser, hvordan du kan bruge indgangsbogen til at oprette fakturaer og derefter bruge godkendelseskladden til at opdatere udgiftskonti.</span><span class="sxs-lookup"><span data-stu-id="7575e-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="7575e-105">Oprette og bogføre fakturaen</span><span class="sxs-lookup"><span data-stu-id="7575e-105">Create and post and invoice</span></span>
1. <span data-ttu-id="7575e-106">Gå til Kreditor > Fakturaer > Indgangsbog.</span><span class="sxs-lookup"><span data-stu-id="7575e-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="7575e-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7575e-107">Click New.</span></span>
3. <span data-ttu-id="7575e-108">Vælg navnet på den indgangsbog, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="7575e-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="7575e-109">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7575e-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7575e-110">Klik på Linjer for at åbne bogen og angive udgiftslinjer.</span><span class="sxs-lookup"><span data-stu-id="7575e-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="7575e-111">Vælg en kreditor.</span><span class="sxs-lookup"><span data-stu-id="7575e-111">Select a vendor.</span></span> <span data-ttu-id="7575e-112">Angiv eller vælg for eksempel US-104</span><span class="sxs-lookup"><span data-stu-id="7575e-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="7575e-113">Skriv en værdi i feltet Faktura.</span><span class="sxs-lookup"><span data-stu-id="7575e-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="7575e-114">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="7575e-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="7575e-115">Angiv et tal i feltet Kredit.</span><span class="sxs-lookup"><span data-stu-id="7575e-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="7575e-116">Klik på rullelisten i feltet Godkendt af for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="7575e-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="7575e-117">Fremhæv en godkender, og klik på Vælg for at vælge den pågældende godkender.</span><span class="sxs-lookup"><span data-stu-id="7575e-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="7575e-118">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="7575e-118">Click Post.</span></span>
13. <span data-ttu-id="7575e-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7575e-119">Close the page.</span></span>
14. <span data-ttu-id="7575e-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7575e-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="7575e-121">Godkende en faktura</span><span class="sxs-lookup"><span data-stu-id="7575e-121">Approve an invoice</span></span>
1. <span data-ttu-id="7575e-122">Gå til Kreditor > Fakturaer > Fakturagodkendelse.</span><span class="sxs-lookup"><span data-stu-id="7575e-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="7575e-123">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7575e-123">Click New.</span></span>
3. <span data-ttu-id="7575e-124">Vælg navnet på den kladde til fakturagodkendelse, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="7575e-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="7575e-125">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7575e-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7575e-126">Klik på linjer for at få vist en side, hvor du vil kunne vælge de fakturaer, du vil godkende.</span><span class="sxs-lookup"><span data-stu-id="7575e-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="7575e-127">Vælg Find bilag for at få vist alle fakturaer, der er klar til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="7575e-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="7575e-128">Markér den faktura, du oprettede.</span><span class="sxs-lookup"><span data-stu-id="7575e-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="7575e-129">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="7575e-129">Click Select.</span></span>
    * <span data-ttu-id="7575e-130">De bilag, som du har markeret ovenfor, flyttes til denne liste, når du har valgt dem.</span><span class="sxs-lookup"><span data-stu-id="7575e-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="7575e-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7575e-131">Click OK.</span></span>
10. <span data-ttu-id="7575e-132">Klik på i feltet Kontonummer for at føje en udgiftskonto til fakturaen.</span><span class="sxs-lookup"><span data-stu-id="7575e-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="7575e-133">Angiv et kontonummer, og flyt markøren fra feltet.</span><span class="sxs-lookup"><span data-stu-id="7575e-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="7575e-134">Indtast for eksempel 600120.</span><span class="sxs-lookup"><span data-stu-id="7575e-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="7575e-135">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="7575e-135">Click Post.</span></span>
13. <span data-ttu-id="7575e-136">Klik på Bilag for at få vist de poster, der blev bogført.</span><span class="sxs-lookup"><span data-stu-id="7575e-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="7575e-137">Kontoen til fakturaer, der afventer godkendelse, tilbageføres og erstattes med kontoen til faktiske udgifter.</span><span class="sxs-lookup"><span data-stu-id="7575e-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  


