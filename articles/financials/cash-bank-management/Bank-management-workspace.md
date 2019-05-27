---
title: Arbejdsområde for bankstyring
description: Dette emne indeholder oplysninger om arbejdsområdet Bankstyring. Dette arbejdsområde viser oplysninger, der er relateret til et firmas bankkonti og indeholder en oversigtsvisning og en analyseside. Oversigtsvisningen indeholder oversigtsfelter, bankkontooplysninger, et saldodiagram og relaterede oplysninger. Analysesiden bruger funktionerne i Microsoft Power BI til at vise grafik, der vedrører bankkontosaldi.
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: fdc0d1e5ea02cdcff9f7f5ede4ab685f54365698
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547950"
---
# <a name="bank-management-workspace"></a><span data-ttu-id="e1453-106">Arbejdsområde for bankstyring</span><span class="sxs-lookup"><span data-stu-id="e1453-106">Bank management workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1453-107">Arbejdsområdet **Bankstyring** viser oplysninger, der er relateret til firmaets bankkonti.</span><span class="sxs-lookup"><span data-stu-id="e1453-107">The **Bank management** workspace shows information that is related to company bank accounts.</span></span> <span data-ttu-id="e1453-108">Arbejdsområdet indeholder en **Oversigt**-visning og siden **Analyser**.</span><span class="sxs-lookup"><span data-stu-id="e1453-108">This workspace includes a **Summary** view and an **Analytics** page.</span></span> <span data-ttu-id="e1453-109">**Oversigt**-visningen indeholder oversigtsfelter, bankkontooplysninger, et saldodiagram og relaterede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="e1453-109">The **Summary** view shows summary tiles, bank account information, a balance chart, and related information.</span></span> <span data-ttu-id="e1453-110">**Analyse**-siden bruger funktionerne i Microsoft Power BI til at vise grafik, der vedrører bankkontosaldi.</span><span class="sxs-lookup"><span data-stu-id="e1453-110">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to bank account balances.</span></span>

## <a name="summary-view"></a><span data-ttu-id="e1453-111">Oversigtsvisning</span><span class="sxs-lookup"><span data-stu-id="e1453-111">Summary view</span></span>

### <a name="summary"></a><span data-ttu-id="e1453-112">Resume</span><span class="sxs-lookup"><span data-stu-id="e1453-112">Summary</span></span>

<span data-ttu-id="e1453-113">Felterne i afsnittet **Oversigt** giver et overblik over dine bankkonti og giver hurtig adgang til de sider, du oftest skal bruge.</span><span class="sxs-lookup"><span data-stu-id="e1453-113">The tiles in the **Summary** section give an overview of your bank accounts and provide quick access to the pages that you most often have to use.</span></span> <span data-ttu-id="e1453-114">Bankafstemningsoplysningerne gælder kun for den avancerede bankkontoafstemningsfunktion.</span><span class="sxs-lookup"><span data-stu-id="e1453-114">The bank reconciliation information is specific to the Advanced bank reconciliation functionality.</span></span> <span data-ttu-id="e1453-115">Der findes kun oplysninger for de bankkonti, hvor indstillingen **Avanceret bankafstemning** er sat til **Ja** på siden **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="e1453-115">Information is included only for those bank accounts that have the **Advanced bank reconciliation** option set to **Yes** on the **Bank account** page.</span></span> <span data-ttu-id="e1453-116">Fra afsnittet **Oversigt** kan du importere elektroniske bankfiler for bankkonti på tværs af alle juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="e1453-116">From the **Summary** section, you can import electronic bank files for bank accounts across all legal entities.</span></span>

### <a name="bank-accounts"></a><span data-ttu-id="e1453-117">Bankkonti</span><span class="sxs-lookup"><span data-stu-id="e1453-117">Bank accounts</span></span>

<span data-ttu-id="e1453-118">De enkelte bankkonti i den juridiske enhed er repræsenteret af et kort i afsnittet **Bankkonti**.</span><span class="sxs-lookup"><span data-stu-id="e1453-118">Each bank account in the legal entity is represented by a card in the **Bank accounts** section.</span></span> <span data-ttu-id="e1453-119">Den aktuelle saldo er vist, og du kan finde frem til de posteringer, der udgør saldobeløbet i denne oversigt.</span><span class="sxs-lookup"><span data-stu-id="e1453-119">The current balance is shown, and you can drill down to the transactions that make up that summary balance amount.</span></span> <span data-ttu-id="e1453-120">Med beløbet i **Mellemposteringer** kan du også finde frem til de posteringer, der udgør oversigtsbeløbet.</span><span class="sxs-lookup"><span data-stu-id="e1453-120">The **Bridged transactions** amount also lets you drill down to the transactions that make up that summary amount.</span></span> <span data-ttu-id="e1453-121">Mellemposteringer er de ventende posteringer, der er bogført ved hjælp af mellemposteringsfunktioner, men endnu ikke er afstemt.</span><span class="sxs-lookup"><span data-stu-id="e1453-121">Bridged transactions are any pending transactions that have been posted by using bridging functionality, but that haven't yet been cleared.</span></span> <span data-ttu-id="e1453-122">Beløbet i **Afventende saldo** er den aktuelle saldo minus de mellemposterede eller ventende transaktioner.</span><span class="sxs-lookup"><span data-stu-id="e1453-122">The **Pending balance** amount is the current balance minus the bridged, or pending, transactions.</span></span>

<span data-ttu-id="e1453-123">Kortet viser også, hvornår bankkontoen sidst blev afstemt.</span><span class="sxs-lookup"><span data-stu-id="e1453-123">The card also shows when the bank account was last reconciled.</span></span> <span data-ttu-id="e1453-124">Disse oplysninger vises kun, hvis Avanceret bankafstemning er aktiveret for bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="e1453-124">This information is shown only if Advanced bank reconciliation is enabled for the bank account.</span></span>

### <a name="balance"></a><span data-ttu-id="e1453-125">Restværdi</span><span class="sxs-lookup"><span data-stu-id="e1453-125">Balance</span></span>

<span data-ttu-id="e1453-126">**Saldo**-diagrammet viser enten historiske saldooplysninger for den bankkonto, der er valgt i afsnittet **Bankkonti**, eller en oversigt over historiske saldooplysninger for alle bankkonti i den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="e1453-126">The **Balance** chart shows either historic balance information for the bank account that is selected in the **Bank accounts** section or a summary of historic balance information for all bank accounts in the legal entity.</span></span> <span data-ttu-id="e1453-127">Disse oplysninger er tilgængelige for forskellige perioder: den aktuelle uge, den aktuelle måned, indeværende år, de sidste fem år og alle perioder (den fulde historik for bankkontoen).</span><span class="sxs-lookup"><span data-stu-id="e1453-127">This information is available for various periods: the current week, the current month, the current year, the last five years, and all periods (the full history of the bank account).</span></span> 

<span data-ttu-id="e1453-128">Hvis du får vist **Saldo**-diagrammet for en enkelt bankkonto, vises historiske saldi i bankkontoens valuta.</span><span class="sxs-lookup"><span data-stu-id="e1453-128">If you're viewing the **Balance** chart for a single bank account, the historic balances are shown in the bank account currency.</span></span> <span data-ttu-id="e1453-129">Hvis du får vist diagrammet for alle bankkonti i den juridisk enhed, vises historiske saldi i regnskabsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="e1453-129">If you're viewing the chart for all bank accounts in the legal entity, the historic balances are shown in the accounting currency.</span></span>

<span data-ttu-id="e1453-130">Oplysninger om, hvornår dataene sidst blev opdateret, vises øverst i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="e1453-130">Information about when the data was last updated appears at the top of the chart.</span></span> <span data-ttu-id="e1453-131">Du kan opdatere dataene efter behov.</span><span class="sxs-lookup"><span data-stu-id="e1453-131">You can update the data as you require.</span></span>

### <a name="related-information"></a><span data-ttu-id="e1453-132">Relaterede oplysninger</span><span class="sxs-lookup"><span data-stu-id="e1453-132">Related information</span></span>

<span data-ttu-id="e1453-133">Fra afsnittet **Relaterede oplysninger** kan du åbne siden **Finanskladde** for at foretage bankoverførsler.</span><span class="sxs-lookup"><span data-stu-id="e1453-133">From the **Related information** section, you can open the **General journal** page to complete bank transfers.</span></span> <span data-ttu-id="e1453-134">Du kan også hurtigt åbne siderne **Bankposteringer** og **Mellemposteringer**.</span><span class="sxs-lookup"><span data-stu-id="e1453-134">You can also quickly open the **Bank transactions** and **Bridged transactions** pages.</span></span>

## <a name="analytics-view"></a><span data-ttu-id="e1453-135">Visningen Analyser</span><span class="sxs-lookup"><span data-stu-id="e1453-135">Analytics view</span></span>

<span data-ttu-id="e1453-136">Siden **Analyser** giver vigtige oplysninger om bankkonti i det aktuelle firma.</span><span class="sxs-lookup"><span data-stu-id="e1453-136">The **Analytics** page provides important metrics about the bank accounts in the current company.</span></span> <span data-ttu-id="e1453-137">Siden indeholder følgende visualiseringer:</span><span class="sxs-lookup"><span data-stu-id="e1453-137">The following visualizations are available on the page:</span></span>

-   <span data-ttu-id="e1453-138">Den samlede banksaldo i systemvalutaen</span><span class="sxs-lookup"><span data-stu-id="e1453-138">Total bank balance in system currency</span></span>
-   <span data-ttu-id="e1453-139">Saldo pr. juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="e1453-139">Balance by legal entity</span></span>
-   <span data-ttu-id="e1453-140">Dagens faktisk vs. budgetteret saldo i bankkontoens valuta</span><span class="sxs-lookup"><span data-stu-id="e1453-140">Today’s actual vs forecasted balance in bank account currency</span></span>
-   <span data-ttu-id="e1453-141">Saldo pr. bankkonto</span><span class="sxs-lookup"><span data-stu-id="e1453-141">Balance by bank account</span></span>
-   <span data-ttu-id="e1453-142">Saldo pr. valuta</span><span class="sxs-lookup"><span data-stu-id="e1453-142">Balance by currency</span></span>

<span data-ttu-id="e1453-143">Du kan få vist bankanalyser på tværs af alle regnskaber fra arbejdsområdet **Oversigt over kontanter - alle firmaer**.</span><span class="sxs-lookup"><span data-stu-id="e1453-143">You can view bank analytics across all companies from the **Cash overview – all companies** workspace.</span></span>
