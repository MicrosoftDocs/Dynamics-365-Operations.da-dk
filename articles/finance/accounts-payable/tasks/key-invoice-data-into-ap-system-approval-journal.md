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
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0fee32d9fd1ab89b1a8cedb2e1965674586d4e7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227178"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="2c8e0-103">Indtaste fakturadata under kreditorer ved hjælp af en godkendelseskladde</span><span class="sxs-lookup"><span data-stu-id="2c8e0-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c8e0-104">Dette emne viser, hvordan du kan bruge indgangsbogen til at oprette fakturaer og derefter bruge godkendelseskladden til at opdatere udgiftskonti.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="2c8e0-105">Oprette og bogføre fakturaen</span><span class="sxs-lookup"><span data-stu-id="2c8e0-105">Create and post and invoice</span></span>
1. <span data-ttu-id="2c8e0-106">Gå i navigationsruden til **Moduler > Kreditorer > Fakturaer > Indgangsbog**.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="2c8e0-107">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-107">Select **New**.</span></span>
3. <span data-ttu-id="2c8e0-108">Vælg navnet på den indgangsbog, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="2c8e0-109">Vælg **Linjer** for at åbne bogen og angive udgiftslinjer.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="2c8e0-110">Vælg en kreditor.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-110">Select a vendor.</span></span> <span data-ttu-id="2c8e0-111">Angiv eller vælg for eksempel `US-104`.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="2c8e0-112">Skriv en værdi i feltet **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="2c8e0-113">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="2c8e0-114">Angiv et tal i feltet **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="2c8e0-115">Vælg en godkender på rullelisten i feltet **Godkendt af**.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="2c8e0-116">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="2c8e0-117">Godkende en faktura</span><span class="sxs-lookup"><span data-stu-id="2c8e0-117">Approve an invoice</span></span>
1. <span data-ttu-id="2c8e0-118">Gå i navigationsruden til **Moduler > Kreditorer > Fakturaer > Godkendelse af faktura**.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="2c8e0-119">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-119">Select **New**.</span></span>
3. <span data-ttu-id="2c8e0-120">Vælg navnet på den kladde til fakturagodkendelse, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="2c8e0-121">Vælg **Linjer** for at få vist en side, hvor du vil kunne vælge de fakturaer, du vil godkende.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="2c8e0-122">Vælg **Find bilag** for at få vist alle fakturaer, der er klar til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="2c8e0-123">Markér den faktura, du har oprettet, og klik derefter på **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="2c8e0-124">De bilag, som du har markeret ovenfor, flyttes til denne liste, når du har valgt dem.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="2c8e0-125">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-125">Select **OK**.</span></span>
8. <span data-ttu-id="2c8e0-126">Vælg feltet **Kontonummer** for at føje en udgiftskonto til fakturaen.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="2c8e0-127">Angiv et kontonummer, og flyt markøren fra feltet.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="2c8e0-128">Angiv for eksempel `600120`.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="2c8e0-129">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-129">Select **Post**.</span></span>
11. <span data-ttu-id="2c8e0-130">Vælg **Bilag** for at få vist de poster, der blev bogført.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="2c8e0-131">Kontoen til fakturaer, der afventer godkendelse, tilbageføres og erstattes med kontoen til faktiske udgifter.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]