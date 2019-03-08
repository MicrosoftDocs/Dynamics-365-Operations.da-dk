---
title: Få vist kladdeposteringer og transaktioner
description: I denne artikel beskrives de forskellige måder, du kan få vist kladdeposter og transaktioner.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9768154e117ca09ae84c6a9c82d43000752c2b34
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "366690"
---
# <a name="view-journal-entries-and-transactions"></a><span data-ttu-id="535bb-103">Få vist kladdeposteringer og transaktioner</span><span class="sxs-lookup"><span data-stu-id="535bb-103">View journal entries and transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="535bb-104">I denne artikel beskrives de forskellige måder, du kan få vist kladdeposter og transaktioner.</span><span class="sxs-lookup"><span data-stu-id="535bb-104">This article explains the various ways that you can view journal entries and transactions.</span></span> 

<span data-ttu-id="535bb-105">Brugere, der ønsker at få vist kladder og transaktioner, har flere måder at få adgang til dataene på.</span><span class="sxs-lookup"><span data-stu-id="535bb-105">Users who want to view journals and transactions have several ways to access the data.</span></span> <span data-ttu-id="535bb-106">De kan drage fordel af forespørgselssider, der giver mulighed for detailudledning, eller de kan bruge forskellige rapportindstillinger i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="535bb-106">They can take advantage of inquiry pages that provide drill-down ability, or they can use various report options in the general ledger.</span></span>

## <a name="voucher-transactions"></a><span data-ttu-id="535bb-107">Bilagstransaktioner</span><span class="sxs-lookup"><span data-stu-id="535bb-107">Voucher transactions</span></span>
<span data-ttu-id="535bb-108">**Bilagsposteringer** er en forespørgselsside, hvor du kan vælge fra forskellige tabeller og felter for at angive kriterier for den saldo eller postering, som du søger efter.</span><span class="sxs-lookup"><span data-stu-id="535bb-108">**Voucher transactions** is an inquiry page where you can select from various tables and fields to specify criteria for the balance or transaction that you're searching for.</span></span> <span data-ttu-id="535bb-109">Du kan for eksempel få vist alle posteringer for en bestemt dato eller en konto, eller alle transaktioner af typen **Igangværende**, der er i et bestemt posteringslag.</span><span class="sxs-lookup"><span data-stu-id="535bb-109">For example, you can view all transactions for a specific date or account, or all transactions of the **Operating** type that are in a specific posting layer.</span></span> <span data-ttu-id="535bb-110">Siden viser kladdenummer, bilag, dato og hovedkontoen som standard, men du kan tilføje flere tabeller, felter og kriterier for at indsnævre søgningen.</span><span class="sxs-lookup"><span data-stu-id="535bb-110">By default, the page shows the journal number, voucher, date, and main account, but you can add additional tables, fields, and criteria to narrow down your search.</span></span>

## <a name="audit-trail"></a><span data-ttu-id="535bb-111">Revisionsspor</span><span class="sxs-lookup"><span data-stu-id="535bb-111">Audit trail</span></span>
<span data-ttu-id="535bb-112">**Revisionsspor** er en forespørgselsside, der viser typer transaktioner, beskrivelser, hvem posteringerne blev oprettet af, og hvornår de blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="535bb-112">**Audit trail** is an inquiry page that shows the types of transactions, descriptions, who the transactions were created by, and when they were created.</span></span> <span data-ttu-id="535bb-113">Fra forespørgselssiden **Revisionsspor** kan du få vist bilagsposteringer.</span><span class="sxs-lookup"><span data-stu-id="535bb-113">From the **Audit trail** inquiry page, you can view the voucher transactions.</span></span>

## <a name="financial-reports"></a><span data-ttu-id="535bb-114">Økonomirapporter</span><span class="sxs-lookup"><span data-stu-id="535bb-114">Financial reports</span></span>
<span data-ttu-id="535bb-115">Du kan også udforske og analysere finansposteringer ved at køre økonomiske rapporter.</span><span class="sxs-lookup"><span data-stu-id="535bb-115">You can also explore and analyze general ledger transactions by running financial reports.</span></span> <span data-ttu-id="535bb-116">Da udformningen af økonomiske rapporter kan være baseret på konti, dimensioner, kontoarter eller en kombination af disse tre, kan du få vist posteringerne ved at foretage detailudledning på forskellige måder.</span><span class="sxs-lookup"><span data-stu-id="535bb-116">Because the design of financial reports can be based on accounts, dimensions, account categories, or a combination of the three, you can view the transactions by drilling down in various ways.</span></span> <span data-ttu-id="535bb-117">Hvis du ønsker yderligere oplysninger til finanstransaktioner, kan du også medtage flere transaktionsegenskaber som led i rapportdesignet.</span><span class="sxs-lookup"><span data-stu-id="535bb-117">If you require more information for general ledger transactions, you can also include multiple transaction properties as part of the report design.</span></span> <span data-ttu-id="535bb-118">Hvis du desuden vil have vist de transaktioner, der udgør en finanssaldo, kan du foretage detailudledning til kontotransaktioner, på samme måde som du kan fra listesiden **Råbalance**.</span><span class="sxs-lookup"><span data-stu-id="535bb-118">Additionally, if you want to see the transactions that make up a general ledger balance, you can drill down to account transactions, just as you can from the **Trial balance** list page.</span></span>

## <a name="ledger-reports"></a><span data-ttu-id="535bb-119">Finansrapporter</span><span class="sxs-lookup"><span data-stu-id="535bb-119">Ledger reports</span></span>
<span data-ttu-id="535bb-120">Ud over de økonomiske rapporter, kan du bruge følgende finansrapporter til at få vist finanstransaktioner:</span><span class="sxs-lookup"><span data-stu-id="535bb-120">In addition to the financial reports, you can use the following ledger reports to view general ledger transactions:</span></span>

-   <span data-ttu-id="535bb-121">**Dimensionsopgørelse** – Denne rapport viser transaktioner efter dag og konto, og der er også mulighed for at få vist transaktioner efter dimension og periode.</span><span class="sxs-lookup"><span data-stu-id="535bb-121">**Dimension statement** – This report shows transactions by day and account, and there are also options to show transactions by dimension and period.</span></span>
-   <span data-ttu-id="535bb-122">**Finansposteringsliste** – Denne rapport viser transaktioner i transaktions-, regnskabs- og rapporteringsvaluta for et regnskab.</span><span class="sxs-lookup"><span data-stu-id="535bb-122">**Ledger transaction list** – This report shows transactions in transaction, accounting, and reporting currencies for an account.</span></span>
-   <span data-ttu-id="535bb-123">**Udskrift af kladden** – i denne rapport vises resultatet af en bogført kladde.</span><span class="sxs-lookup"><span data-stu-id="535bb-123">**Print journal** – This report shows the result of a posted journal.</span></span> <span data-ttu-id="535bb-124">Du kan køre rapporten efter kladdebatchnummer eller kladdetypen eller tilføje flere felter.</span><span class="sxs-lookup"><span data-stu-id="535bb-124">You can run the report by journal batch number or journal type, or add additional fields.</span></span>
-   <span data-ttu-id="535bb-125">**Bogførte posteringer efter kladde** – Denne rapport viser de transaktioner, der er bogført i en kladde grupperet efter bilag.</span><span class="sxs-lookup"><span data-stu-id="535bb-125">**Posted transactions by journal** – This report shows the transactions that have been posted to a journal, grouped by voucher.</span></span>
-   <span data-ttu-id="535bb-126">**Posteringsliste pr. dato** – Denne rapport viser alle posteringer efter dato sammen med kladdenummer, bilag og finanskonto.</span><span class="sxs-lookup"><span data-stu-id="535bb-126">**Transaction list by date** – This report shows all the transactions by date, together with the journal number, voucher, and ledger account.</span></span> <span data-ttu-id="535bb-127">Den viser også transaktionerne i transaktions-, regnskabs- og rapporteringsvalutaer.</span><span class="sxs-lookup"><span data-stu-id="535bb-127">It also shows the transactions in the transaction, accounting, and reporting currencies.</span></span>
-   <span data-ttu-id="535bb-128">**Transaktionsoprindelse** – Denne transaktionsrapport viser kontoen efter kladde og efter transaktions-, regnskabs- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="535bb-128">**Transaction origin** – This transaction report shows the account by journal, and by transaction, accounting, and reporting currency.</span></span> <span data-ttu-id="535bb-129">Den viser også hver linje i kladden, der blev brugt som en forskydning.</span><span class="sxs-lookup"><span data-stu-id="535bb-129">It also shows each line of the journal that was used as an offset.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="535bb-130">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="535bb-130">Additional resources</span></span>
- [<span data-ttu-id="535bb-131">Kontosaldi i Finans</span><span class="sxs-lookup"><span data-stu-id="535bb-131">General ledger account balances</span></span>](general-ledger-account-balances.md) 
- [<span data-ttu-id="535bb-132">Sporing af regnskabskilde</span><span class="sxs-lookup"><span data-stu-id="535bb-132">Accounting source explorer</span></span>](../accounts-payable/accounting-source-explorer.md)
- [<span data-ttu-id="535bb-133">Økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="535bb-133">Financial reporting</span></span>](financial-reporting-getting-started.md)
- [<span data-ttu-id="535bb-134">Se kladdeposteringer</span><span class="sxs-lookup"><span data-stu-id="535bb-134">View journal entries</span></span>](tasks/view-journal-entries-or-transactions.md)



