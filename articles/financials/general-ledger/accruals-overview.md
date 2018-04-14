---
title: Oversigt over periodiseringer
description: I denne artikel beskrives periodiseringer, og hvordan du konfigurerer dem og opretter transaktioner.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0b4d8e7eb268857ce753415a24e600b8006eb5e3
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="accruals-overview"></a><span data-ttu-id="1075b-103">Oversigt over periodiseringer</span><span class="sxs-lookup"><span data-stu-id="1075b-103">Accruals overview</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="1075b-104">I denne artikel beskrives periodiseringer, og hvordan du konfigurerer dem og opretter transaktioner.</span><span class="sxs-lookup"><span data-stu-id="1075b-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="1075b-105">Periodiseringer bruges i periodiseringsregnskab til at registrere indtægter, der er anerkendt i den periode, der er optjent i, ikke, når betalingen er modtaget, og til at spore udgifter (omkostninger), der registreres, når de opstår, ikke når betalingen foretages.</span><span class="sxs-lookup"><span data-stu-id="1075b-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="1075b-106">Periodiseringsskemaer</span><span class="sxs-lookup"><span data-stu-id="1075b-106">Accrual schemes</span></span>
<span data-ttu-id="1075b-107">Periodiseringsskemaer bruges til at konfigurere udskudte indtægter og omkostninger, og det samme periodiseringsskema kan bruges til både indtægter og omkostninger.</span><span class="sxs-lookup"><span data-stu-id="1075b-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="1075b-108">Periodiseringer af finans omfordeler omkostninger eller indtægter for en kladdelinje, så omkostningerne og indtægterne genkendes i de relevante perioder.</span><span class="sxs-lookup"><span data-stu-id="1075b-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="1075b-109">På siden **Periodiseringsskema** kan du angive de debet- og kreditkonti, der skal bruges, når der anvendes periodiseringsskemaet.</span><span class="sxs-lookup"><span data-stu-id="1075b-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="1075b-110">**Debet** – Den hovedkonto, som du definerer, erstatter debethovedkontoen på kladdebilagslinjen.</span><span class="sxs-lookup"><span data-stu-id="1075b-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="1075b-111">Denne konto bruges også til tilbageførsel af den udelukkelse, der er baseret på posteringer til periodisering af Finans.</span><span class="sxs-lookup"><span data-stu-id="1075b-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="1075b-112">**Kredit** – Den hovedkonto, som du definerer, erstatter kredithovedkontoen på kladdebilagslinjen.</span><span class="sxs-lookup"><span data-stu-id="1075b-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="1075b-113">Denne konto bruges også til tilbageførsel af den udelukkelse, der er baseret på posteringer til periodisering af Finans.</span><span class="sxs-lookup"><span data-stu-id="1075b-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="1075b-114">Når du har bestemt, hvilke konti der skal bruges, kan du angive, hvordan bilagsnummeret oprettes, når der oprettes posteringer til periodisering.</span><span class="sxs-lookup"><span data-stu-id="1075b-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="1075b-115">Du kan også angive, hvor ofte transaktionerne forekommer, det antal gange posteringerne oprettes, og når posteringerne er bogført.</span><span class="sxs-lookup"><span data-stu-id="1075b-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="1075b-116">Når periodiseringsskemaet er blevet oprettet, kan du bruge det i nogle af kladderne ved hjælp af funktionen til periodisering af Finans.</span><span class="sxs-lookup"><span data-stu-id="1075b-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="1075b-117">Periodiseringer af finans</span><span class="sxs-lookup"><span data-stu-id="1075b-117">Ledger accruals</span></span>
<span data-ttu-id="1075b-118">Når du angiver en kladde, kan du klikke på **Finansperiodisering** i menuen **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="1075b-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="1075b-119">Når du derefter vælger periodiseringsskemaet, vises basisbeløbet fra den kladde, der fordeles over perioden som fastlagt i periodiseringsskemaet.</span><span class="sxs-lookup"><span data-stu-id="1075b-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="1075b-120">Hvis du for eksempel betaler en medarbejders forsikring for hele året i januar, og beløbet er 12.000, skal du registrere denne udgift hver måned.</span><span class="sxs-lookup"><span data-stu-id="1075b-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="1075b-121">Du kan vælge startdatoen.</span><span class="sxs-lookup"><span data-stu-id="1075b-121">You can select the start date.</span></span> <span data-ttu-id="1075b-122">Du kan også angive, om det beløb, der er hensat, er baseret på kontoen eller modkontoen.</span><span class="sxs-lookup"><span data-stu-id="1075b-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="1075b-123">Når du har foretaget dine valg, skal du klikke på **Transaktioner** for at få vist alle posteringer, der er oprettet ud fra periodiseringsskemaet.</span><span class="sxs-lookup"><span data-stu-id="1075b-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="1075b-124">Hvis du fordeler 12.000 i forsikringsudgifter over hele året, vil du se 1.000 for hver måned.</span><span class="sxs-lookup"><span data-stu-id="1075b-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="1075b-125">Når du har bogført kladden, kan du få vist posteringerne ved hjælp af forespørgselssiden **Poster på bilag**.</span><span class="sxs-lookup"><span data-stu-id="1075b-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="1075b-126">Hvis du ikke kan anvende et periodiseringsskema (for eksempel når en salgsordrefaktura eller indkøbsordrefakturaen er involveret), kan du kreditere det forudbetalte beløb og debitere udgiftsbeløbet.</span><span class="sxs-lookup"><span data-stu-id="1075b-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="1075b-127">Du kan derefter vælge **Modregn**, når du anvender periodiseringsskemaet.</span><span class="sxs-lookup"><span data-stu-id="1075b-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="1075b-128">Yderligere oplysninger finder du i [Oprette periodiseringsskemaer](tasks/create-accrual-schemes.md) og [Oprette periodiseringsposteringer i finans](tasks/create-ledger-accrual-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="1075b-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>

