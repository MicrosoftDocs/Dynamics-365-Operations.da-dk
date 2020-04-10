---
title: Indtaste fakturadata under kreditorer ved hjælp af en godkendelseskladde
description: Dette emne viser, hvordan du kan bruge indgangsbogen til at oprette fakturaer og derefter bruge godkendelseskladden til at opdatere udgiftskonti.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 788397b5c9a3f42e373f7cdad256c1ee3d058e57
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143759"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="c8685-103">Indtaste fakturadata under kreditorer ved hjælp af en godkendelseskladde</span><span class="sxs-lookup"><span data-stu-id="c8685-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8685-104">Dette emne viser, hvordan du kan bruge indgangsbogen til at oprette fakturaer og derefter bruge godkendelseskladden til at opdatere udgiftskonti.</span><span class="sxs-lookup"><span data-stu-id="c8685-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="c8685-105">Oprette og bogføre fakturaen</span><span class="sxs-lookup"><span data-stu-id="c8685-105">Create and post and invoice</span></span>
1. <span data-ttu-id="c8685-106">Gå i navigationsruden til **Moduler > Kreditorer > Fakturaer > Indgangsbog**.</span><span class="sxs-lookup"><span data-stu-id="c8685-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="c8685-107">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c8685-107">Select **New**.</span></span>
3. <span data-ttu-id="c8685-108">Vælg navnet på den indgangsbog, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="c8685-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="c8685-109">Vælg **Linjer** for at åbne bogen og angive udgiftslinjer.</span><span class="sxs-lookup"><span data-stu-id="c8685-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="c8685-110">Vælg en kreditor.</span><span class="sxs-lookup"><span data-stu-id="c8685-110">Select a vendor.</span></span> <span data-ttu-id="c8685-111">Angiv eller vælg for eksempel `US-104`.</span><span class="sxs-lookup"><span data-stu-id="c8685-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="c8685-112">Skriv en værdi i feltet **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="c8685-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="c8685-113">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="c8685-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="c8685-114">Angiv et tal i feltet **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="c8685-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="c8685-115">Vælg en godkender på rullelisten i feltet **Godkendt af**.</span><span class="sxs-lookup"><span data-stu-id="c8685-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="c8685-116">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="c8685-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="c8685-117">Godkende en faktura</span><span class="sxs-lookup"><span data-stu-id="c8685-117">Approve an invoice</span></span>
1. <span data-ttu-id="c8685-118">Gå i navigationsruden til **Moduler > Kreditorer > Fakturaer > Godkendelse af faktura**.</span><span class="sxs-lookup"><span data-stu-id="c8685-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="c8685-119">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c8685-119">Select **New**.</span></span>
3. <span data-ttu-id="c8685-120">Vælg navnet på den kladde til fakturagodkendelse, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="c8685-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="c8685-121">Vælg **Linjer** for at få vist en side, hvor du vil kunne vælge de fakturaer, du vil godkende.</span><span class="sxs-lookup"><span data-stu-id="c8685-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="c8685-122">Vælg **Find bilag** for at få vist alle fakturaer, der er klar til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="c8685-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="c8685-123">Markér den faktura, du har oprettet, og klik derefter på **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="c8685-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="c8685-124">De bilag, som du har markeret ovenfor, flyttes til denne liste, når du har valgt dem.</span><span class="sxs-lookup"><span data-stu-id="c8685-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="c8685-125">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8685-125">Select **OK**.</span></span>
8. <span data-ttu-id="c8685-126">Vælg feltet **Kontonummer** for at føje en udgiftskonto til fakturaen.</span><span class="sxs-lookup"><span data-stu-id="c8685-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="c8685-127">Angiv et kontonummer, og flyt markøren fra feltet.</span><span class="sxs-lookup"><span data-stu-id="c8685-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="c8685-128">Angiv for eksempel `600120`.</span><span class="sxs-lookup"><span data-stu-id="c8685-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="c8685-129">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="c8685-129">Select **Post**.</span></span>
11. <span data-ttu-id="c8685-130">Vælg **Bilag** for at få vist de poster, der blev bogført.</span><span class="sxs-lookup"><span data-stu-id="c8685-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="c8685-131">Kontoen til fakturaer, der afventer godkendelse, tilbageføres og erstattes med kontoen til faktiske udgifter.</span><span class="sxs-lookup"><span data-stu-id="c8685-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

