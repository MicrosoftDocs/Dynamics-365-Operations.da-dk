---
title: Foretag fordelinger
description: Denne artikel indeholder oplysninger om allokeringer, indstillinger for behandling af dem i Microsoft Dynamics 365 for Finance and Operations, og hvordan de kan bruges i budgetplanlægning. Tildelinger bruges til at distribuere beløb på tværs af flere finanskontokombinationer. De hjælper med at sikre, at udgifter eller indtægter debiteres for det rigtige objekt i regnskabet.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac531726e04ebec4da9062f47726568723364cce
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567208"
---
# <a name="process-allocations"></a><span data-ttu-id="01f66-105">Foretag fordelinger</span><span class="sxs-lookup"><span data-stu-id="01f66-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01f66-106">Denne artikel indeholder oplysninger om allokeringer, indstillinger for behandling af dem i Microsoft Dynamics 365 for Finance and Operations, og hvordan de kan bruges i budgetplanlægning.</span><span class="sxs-lookup"><span data-stu-id="01f66-106">This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Finance and Operations, and how they can be used in budget planning.</span></span> <span data-ttu-id="01f66-107">Tildelinger bruges til at distribuere beløb på tværs af flere finanskontokombinationer.</span><span class="sxs-lookup"><span data-stu-id="01f66-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="01f66-108">De hjælper med at sikre, at udgifter eller indtægter debiteres for det rigtige objekt i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="01f66-108">They help guarantee that expenses or revenue is charged to the correct object in accounting.</span></span>

<span data-ttu-id="01f66-109">Microsoft Dynamics 365 for Finance and Operations indeholder følgende funktioner, der understøtter denne proces:</span><span class="sxs-lookup"><span data-stu-id="01f66-109">Microsoft Dynamics 365 for Finance and Operations provides the following capabilities to support this process:</span></span>

-   <span data-ttu-id="01f66-110">Tildel transaktionsbeløb manuelt, ved hjælp af handlingen Opdel i regnskabsfordelinger eller ved at anvende standardskabeloner til økonomiske dimensioner for et dokument.</span><span class="sxs-lookup"><span data-stu-id="01f66-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="01f66-111">Yderligere oplysninger finder du i afsnittet [Regnskabsfordelinger.](../accounts-payable/accounting-distributions.md)</span><span class="sxs-lookup"><span data-stu-id="01f66-111">For more information, see [Accounting distributions.](../accounts-payable/accounting-distributions.md)</span></span>
-   <span data-ttu-id="01f66-112">Fordel automatisk posteringsbeløb baseret på fordelingsbetingelserne, der er defineret for enkelte hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="01f66-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="01f66-113">Poster på fordelingskonti vil blive genereret for hver kladde, der er baseret på finanskontoen procentdel og destination, hver gang en regnskabspost opfylder de kriterier, der er defineret som kilde for finanskontoen.</span><span class="sxs-lookup"><span data-stu-id="01f66-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="01f66-114">Tildel automatisk finanssaldi eller faste beløb, der er baseret på fordelingsregler for Finans.</span><span class="sxs-lookup"><span data-stu-id="01f66-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="01f66-115">Fordelingsreglerne for finans behandles med jævne mellemrum ved hjælp af fordelingskladder.</span><span class="sxs-lookup"><span data-stu-id="01f66-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="01f66-116">Fordelinger i budgetplanlægning</span><span class="sxs-lookup"><span data-stu-id="01f66-116">Allocations in budget planning</span></span>

<span data-ttu-id="01f66-117">Finansfordelingsregler kan bruges til budgetplaner.</span><span class="sxs-lookup"><span data-stu-id="01f66-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="01f66-118">Når du bruger finansfordelingsregler i budgetplanlægningen, fungerer allokeringsreglerne på samme måde, som de ville i Finans, men kildedata og destinationsdata kommer fra budgetplanen.</span><span class="sxs-lookup"><span data-stu-id="01f66-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="01f66-119">Du kan manuelt vælge finansfordelingsregler, som skal bruges til budgetplaner.</span><span class="sxs-lookup"><span data-stu-id="01f66-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="01f66-120">Du kan også bruge en fordelingstidsplan, der kører som en del af en arbejdsgangproces.</span><span class="sxs-lookup"><span data-stu-id="01f66-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="01f66-121">Du kan ikke bruge interne finansfordelingsregler til budgetplanlæsning.</span><span class="sxs-lookup"><span data-stu-id="01f66-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>





