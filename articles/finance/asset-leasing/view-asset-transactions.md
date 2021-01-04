---
title: Få vist forpligtelses-, aktiv- og udgiftstransaktioner
description: Dette emne forklarer, hvordan du får vist posteringer for et leaset aktiv. Disse posteringer omfatter leasede passivposteringer og faste posteringer, der er bogført.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7008891d194dc990d13a9f56db155c6990aae0c0
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441773"
---
# <a name="view-liability-asset-and-expense-transactions"></a><span data-ttu-id="883a3-104">Få vist forpligtelses-, aktiv- og udgiftstransaktioner</span><span class="sxs-lookup"><span data-stu-id="883a3-104">View liability, asset, and expense transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="883a3-105">Dette emne forklarer, hvordan du får vist posteringer for et leaset aktiv.</span><span class="sxs-lookup"><span data-stu-id="883a3-105">This topic explains how to view transactions for a leased asset.</span></span> <span data-ttu-id="883a3-106">Disse posteringer omfatter leasede passivposteringer og faste posteringer, der er bogført.</span><span class="sxs-lookup"><span data-stu-id="883a3-106">These transactions include lease liability transactions and executory expense transactions that have been posted.</span></span> <span data-ttu-id="883a3-107">De opbrugte værdier for passiv- og ROUs-aktiverne bruges i flere rapporter.</span><span class="sxs-lookup"><span data-stu-id="883a3-107">The carrying values of the liability and right-of-use (ROU) asset are used on several reports.</span></span> <span data-ttu-id="883a3-108">De bruges også til at beregne reguleringsværdier.</span><span class="sxs-lookup"><span data-stu-id="883a3-108">They are also used to calculate adjustment values.</span></span>

## <a name="liability-transactions"></a><span data-ttu-id="883a3-109">Forpligtelsestransaktioner</span><span class="sxs-lookup"><span data-stu-id="883a3-109">Liability transactions</span></span>

<span data-ttu-id="883a3-110">Hvis du vil have vist leasede passivposteringer, skal du vælge en leasingaftale på siden **Leasingoversigt** og derefter vælge **Kartoteker** for at åbne de kartoteker, der er tilknyttet leasingposten.</span><span class="sxs-lookup"><span data-stu-id="883a3-110">To view the lease liability transactions, select a lease on the **Lease summary** page, and then select **Books** to open the books that are attached to the lease record.</span></span> <span data-ttu-id="883a3-111">Når der er bogført en første godkendelse, en faktura eller en rentekladde, skal du vælge **Ansvarsposteringer**.</span><span class="sxs-lookup"><span data-stu-id="883a3-111">After an initial recognition, an invoice, or an interest journal has been posted, select **Liability transactions**.</span></span>

<span data-ttu-id="883a3-112">På siden **Ansvarsposteringer** vises de transaktioner, der enten øger eller reducerer leasingforpligtelsen.</span><span class="sxs-lookup"><span data-stu-id="883a3-112">The **Liability transactions** page shows the transactions that either increase or decrease the lease liability.</span></span> <span data-ttu-id="883a3-113">Negative beløb på denne side repræsenterer kreditposteringer i standardapplikationen.</span><span class="sxs-lookup"><span data-stu-id="883a3-113">Negative amounts on this page represent credit transactions in the standard application.</span></span> <span data-ttu-id="883a3-114">Renteperiodiseringer vises som negative værdier og øger den samlede leasingforpligtelse.</span><span class="sxs-lookup"><span data-stu-id="883a3-114">Any interest accruals are shown as negative values and increase the total lease liability.</span></span> <span data-ttu-id="883a3-115">Eventuelle leasingreguleringer vises som positive eller negative værdier, afhængigt af arten og virkningen af leasingkartoteket.</span><span class="sxs-lookup"><span data-stu-id="883a3-115">Any lease adjustments are shown as positive or negative values, depending on the nature and impact of the lease book.</span></span> <span data-ttu-id="883a3-116">Den aktuelle nettosaldo for leasingforpligtelse for den valgte leasingaftale vises nederst til venstre på siden.</span><span class="sxs-lookup"><span data-stu-id="883a3-116">The current net total balance of the lease liability for the selected lease is shown at the bottom left of the page.</span></span>

## <a name="asset-transactions"></a><span data-ttu-id="883a3-117">Aktivtransaktioner</span><span class="sxs-lookup"><span data-stu-id="883a3-117">Asset transactions</span></span>

<span data-ttu-id="883a3-118">Hvis du vil have vist aktivposteringer for leasingen, skal du vælge en leasingaftale på siden **Leasingoversigt** og derefter vælge **Kartoteker** for at åbne de leasingkartoteker, der er tilknyttet leasingposten.</span><span class="sxs-lookup"><span data-stu-id="883a3-118">To view the lease asset transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="883a3-119">Vælg derefter **Aktivtransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="883a3-119">Then select **Asset transactions**.</span></span>

<span data-ttu-id="883a3-120">På siden **Aktivposter** vises de transaktioner, der enten øger eller reducerer aktivets anlægsaktiv og de akkumulerede afskrivningskonti.</span><span class="sxs-lookup"><span data-stu-id="883a3-120">The **Asset transaction** page shows the transactions that either increase or decrease the lease asset and accumulated depreciation accounts.</span></span> <span data-ttu-id="883a3-121">Debiteringer vises som positive værdier, og krediteringer vises som negative værdier som på siden **Ansvarsposteringer**.</span><span class="sxs-lookup"><span data-stu-id="883a3-121">Debits are shown as positive values, and credits are shown as negative values, as on the **Liability transactions** page.</span></span> <span data-ttu-id="883a3-122">Den bogførte første genkendelse og den næste af den akkumulerede afskrivning vises nederst til venstre på siden som aktivsaldo.</span><span class="sxs-lookup"><span data-stu-id="883a3-122">The posted initial recognition and the next of accumulated depreciation are shown at the bottom left of the page as the asset balance.</span></span> 

## <a name="expenses-transactions"></a><span data-ttu-id="883a3-123">Udgiftsposteringer</span><span class="sxs-lookup"><span data-stu-id="883a3-123">Expenses transactions</span></span>

<span data-ttu-id="883a3-124">Hvis du vil have vist udgiftsposteringer for leasingen, skal du vælge en leasingaftale på siden **Leasingoversigt** og derefter vælge **Kartoteker** for at åbne de leasingkartoteker, der er tilknyttet leasingposten.</span><span class="sxs-lookup"><span data-stu-id="883a3-124">To view the lease expense transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="883a3-125">Vælg derefter **Udgiftsposteringer**.</span><span class="sxs-lookup"><span data-stu-id="883a3-125">Then select **Expense transactions**.</span></span>

<span data-ttu-id="883a3-126">På siden **Udgiftsposteringer** vises alle de udgifter, der er bogført i forhold til leasingaftalen, f. eks. renteudgifter, afskrivningsudgifter og eventuelle afviklede omkostninger.</span><span class="sxs-lookup"><span data-stu-id="883a3-126">The **Expense transactions** page shows all the expenses that have been posted against the lease, such as interest expenses, depreciation expenses, and any executory costs.</span></span>
