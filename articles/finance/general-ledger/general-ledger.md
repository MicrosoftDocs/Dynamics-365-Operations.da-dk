---
title: Oversigt over finans og økonomirapportering
description: Brug finansregnskabet til at definere og administrere finansposter for den juridiske enhed.
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4cad11bcd1b1674055a07b5093093e33d3ac556
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771793"
---
# <a name="general-ledger-and-financial-reporting-overview"></a><span data-ttu-id="7793d-103">Oversigt over finans og økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="7793d-103">General ledger and Financial reporting overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7793d-104">Brug finansregnskabet til at definere og administrere finansposter for den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="7793d-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="7793d-105">Finansregnskabet er et register over debet- og kreditposter.</span><span class="sxs-lookup"><span data-stu-id="7793d-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="7793d-106">Disse poster er klassificeret ved hjælp af konti, som er opført i en kontoplan.</span><span class="sxs-lookup"><span data-stu-id="7793d-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="7793d-107">Planlægge din kontoplan</span><span class="sxs-lookup"><span data-stu-id="7793d-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="7793d-108">Hovedkontotyper</span><span class="sxs-lookup"><span data-stu-id="7793d-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="7793d-109">Du kan fordele eller distribuere pengebeløb til en eller flere konti eller kombinationer af konto/dimension baseret på fordelingsregler.</span><span class="sxs-lookup"><span data-stu-id="7793d-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="7793d-110">Der er to typer fordelinger: fast og variabel.</span><span class="sxs-lookup"><span data-stu-id="7793d-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="7793d-111">Du kan også udligne posteringer mellem finanskonti og værdiregulere posteringer i udenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="7793d-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="7793d-112">Ved udgangen af regnskabsåret skal du generere ultimoposter og forberede alle konti til det næste regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="7793d-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="7793d-113">Du kan bruge konsolideringsfunktionen til at kombinere de økonomiske resultater for et antal juridiske enheder for datterselskaber på samme tid, i en konsolideret organisation.</span><span class="sxs-lookup"><span data-stu-id="7793d-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="7793d-114">Datterselskaberne kan være i samme database eller i forskellige databaser.</span><span class="sxs-lookup"><span data-stu-id="7793d-114">The subsidiaries can be in the same database or in separate databases.</span></span>

- [<span data-ttu-id="7793d-115">Oversigt over konsolidering og eliminering</span><span class="sxs-lookup"><span data-stu-id="7793d-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="7793d-116">Kontosaldi i Finans</span><span class="sxs-lookup"><span data-stu-id="7793d-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="7793d-117">Økonomiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="7793d-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="7793d-118">[![Forretningsproces](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="7793d-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="7793d-119">Moms</span><span class="sxs-lookup"><span data-stu-id="7793d-119">Sales tax</span></span>
<span data-ttu-id="7793d-120">Alle virksomheder inddriver og betaler skatter til forskellige skattemyndigheder.</span><span class="sxs-lookup"><span data-stu-id="7793d-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="7793d-121">Reglerne og satserne varierer afhængigt af land/område, stat, region og by.</span><span class="sxs-lookup"><span data-stu-id="7793d-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="7793d-122">Reglerne skal desuden opdateres regelmæssigt, når skattemyndighederne ændrer kravene.</span><span class="sxs-lookup"><span data-stu-id="7793d-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="7793d-123">Momskoder indeholder grundlæggende oplysninger om, hvor meget du skal inddrive og betale til myndighederne.</span><span class="sxs-lookup"><span data-stu-id="7793d-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="7793d-124">Når du konfigurerer momskoder, skal du definere de beløb eller procentsatser, der skal inddrives.</span><span class="sxs-lookup"><span data-stu-id="7793d-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="7793d-125">Du skal også definerer de forskellige metoder, der bruges til at anvende disse beløb eller procentsatser på transaktionsbeløb.</span><span class="sxs-lookup"><span data-stu-id="7793d-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="7793d-126">Emnerne i dette afsnit indeholder oplysninger om, hvordan du kan konfigurere momskoder til de metoder og satser, skattemyndighederne kræver.</span><span class="sxs-lookup"><span data-stu-id="7793d-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="7793d-127">Momsoversigt</span><span class="sxs-lookup"><span data-stu-id="7793d-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="7793d-128">Momssatser baseret på beregningsgrundlaget og beregningsmåderne</span><span class="sxs-lookup"><span data-stu-id="7793d-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="7793d-129">Momsafregninger og afrundingsregler</span><span class="sxs-lookup"><span data-stu-id="7793d-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="7793d-130">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7793d-130">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="7793d-131">Nyheder og funktioner under udvikling</span><span class="sxs-lookup"><span data-stu-id="7793d-131">What's new and in development</span></span>

<span data-ttu-id="7793d-132">Gå til [Microsoft Dynamics 365-udgivelsesplaner](https://go.microsoft.com/fwlink/?linkid=2010158) for at se, hvilke nye funktioner der er planlagt.</span><span class="sxs-lookup"><span data-stu-id="7793d-132">Go to the [Microsoft Dynamics 365 release plans](https://go.microsoft.com/fwlink/?linkid=2010158) to see what new features have been planned.</span></span> 

#### <a name="blogs"></a><span data-ttu-id="7793d-133">Blogs</span><span class="sxs-lookup"><span data-stu-id="7793d-133">Blogs</span></span>

<span data-ttu-id="7793d-134">Du kan finde meninger, nyheder og andre oplysninger i [Microsoft Dynamics 365-bloggen](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) og [Microsoft Dynamics 365 Finance and Operations - Finans-bloggen](https://community.dynamics.com/365/financeandoperations/b/financials).</span><span class="sxs-lookup"><span data-stu-id="7793d-134">You can find opinions, news, and other information on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) and the [Microsoft Dynamics 365 Finance and Operations - Financials blog](https://community.dynamics.com/365/financeandoperations/b/financials).</span></span>

<span data-ttu-id="7793d-135">[Microsoft Dynamics Operations Partner Community-bloggen](https://community.dynamics.com/partner/b/operationspartnercommunityblog) giver Microsoft Dynamics-partnere en samlet ressource, hvor de kan finde oplysninger om nyheder og populære tendenser i MBS Operations.</span><span class="sxs-lookup"><span data-stu-id="7793d-135">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

### <a name="videos"></a><span data-ttu-id="7793d-136">Videoer</span><span class="sxs-lookup"><span data-stu-id="7793d-136">Videos</span></span>

<span data-ttu-id="7793d-137">Se de Sådan-videoer, der er nu tilgængelige på [Microsoft Dynamics 365 YouTube-kanalen](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span><span class="sxs-lookup"><span data-stu-id="7793d-137">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="7793d-138">Fællesskabsblogge</span><span class="sxs-lookup"><span data-stu-id="7793d-138">Community blogs</span></span>

- [<span data-ttu-id="7793d-139">Værd at vide om Finans i Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7793d-139">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)

