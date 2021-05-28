---
title: Rapporten Indirekte omkostninger under afvikling omfatter slettede produktionsordrer
description: Rapporten Indirekte omkostninger under afvikling indeholder oplysninger om produktionsordrer, der er delvist behandlet og senere slettet.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026372"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a><span data-ttu-id="89f4f-103">Rapporten Indirekte omkostninger under afvikling omfatter slettede produktionsordrer</span><span class="sxs-lookup"><span data-stu-id="89f4f-103">The Indirect costs in process report includes deleted production orders</span></span>

<span data-ttu-id="89f4f-104">KB-nummer: 4612748</span><span class="sxs-lookup"><span data-stu-id="89f4f-104">KB number: 4612748</span></span>

## <a name="symptoms"></a><span data-ttu-id="89f4f-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="89f4f-105">Symptoms</span></span>

<span data-ttu-id="89f4f-106">Rapporten **Indirekte omkostninger under afvikling** indeholder oplysninger om produktionsordrer, der er delvist behandlet og senere slettet.</span><span class="sxs-lookup"><span data-stu-id="89f4f-106">The **Indirect costs in process** report presents information about production orders that were partially processed and later deleted.</span></span>

## <a name="resolution"></a><span data-ttu-id="89f4f-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="89f4f-107">Resolution</span></span>

<span data-ttu-id="89f4f-108">Når du tilbagefører en produktionsordre, tilbageføres også alle posteringerne for den pågældende produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="89f4f-108">When you reverse a production order, you also reverse all the transactions of that production order.</span></span> <span data-ttu-id="89f4f-109">Når du sletter produktionsordren, består alle posteringer, der er relateret til den, i reskontrotabellerne og finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="89f4f-109">When you delete the production order, the subledger tables and general ledger persist all transactions that are related to it.</span></span> <span data-ttu-id="89f4f-110">Rapporterne vil vise posteringerne i reskontrotabellerne.</span><span class="sxs-lookup"><span data-stu-id="89f4f-110">The reports will show the transactions in the subledger tables.</span></span> <span data-ttu-id="89f4f-111">For den specifikke produktionsordre skal nettoværdien være 0,00.</span><span class="sxs-lookup"><span data-stu-id="89f4f-111">For the specific production order, the net value should be 0.00.</span></span>
