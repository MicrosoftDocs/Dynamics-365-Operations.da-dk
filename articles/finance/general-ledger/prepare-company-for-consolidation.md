---
title: Forberede en juridisk enhed til brug i konsolideringsprocessen
description: Under en konsolidering indsamles transaktioner fra flere sæt juridiske enhedskonti til ét sæt juridiske enhedskonti. Dette emne forklarer, hvordan du forbereder en juridisk enhed til en konsolidering.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: f6fce69724945448f961769dd383d1047a5d13c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990292"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a><span data-ttu-id="00b06-104">Forberede en juridisk enhed til brug i konsolideringsprocessen</span><span class="sxs-lookup"><span data-stu-id="00b06-104">Prepare a legal entity for the consolidation process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00b06-105">Under en konsolidering indsamles transaktioner fra flere sæt juridiske enhedskonti til ét sæt juridiske enhedskonti.</span><span class="sxs-lookup"><span data-stu-id="00b06-105">During a consolidation, you gather transactions from several sets of legal entity accounts into a single set of legal entity accounts.</span></span> <span data-ttu-id="00b06-106">Dette emne forklarer, hvordan du forbereder en juridisk enhed til en konsolidering.</span><span class="sxs-lookup"><span data-stu-id="00b06-106">This topic explains how to prepare a legal entity for a consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="00b06-107">Det anbefales, at du bruger Management Reporter til Microsoft Dynamics 365 Finance til at kombinere de økonomiske resultater for flere juridiske enheder i et konsolideret format.</span><span class="sxs-lookup"><span data-stu-id="00b06-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="00b06-108">Du kan bruge Management Reporter til at oprette konsoliderede regnskabsrapporter på tværs af juridiske enheder, bruge Excel til at importere konsolideringsdata fra andre kilder og oversætte beløb til et vilkårligt antal rapporteringsvalutaer uden at skulle køre konsolideringsprocessen i Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="00b06-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

<span data-ttu-id="00b06-109">Du kan udskrive rapporter, f.eks. årsregnskaber, fra den konsoliderede juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="00b06-109">You can print reports, such as financial statements, from the consolidated legal entity.</span></span> <span data-ttu-id="00b06-110">Du kan dog ikke bruge den konsoliderede juridisk enhed til daglige transaktioner.</span><span class="sxs-lookup"><span data-stu-id="00b06-110">However, you can't use the consolidated legal entity for daily transactions.</span></span>

<span data-ttu-id="00b06-111">Du kan konsolidere data fra juridiske enheder, der bruger andre databaser end den konsoliderede juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="00b06-111">You can consolidate data from legal entities that use different databases than the consolidated legal entity.</span></span> <span data-ttu-id="00b06-112">Denne konsolideringsproces kaldes en *importkonsolidering*.</span><span class="sxs-lookup"><span data-stu-id="00b06-112">This consolidation process is referred to as an *import consolidation*.</span></span> <span data-ttu-id="00b06-113">Juridiske enheder kan også bruge den samme database som den konsoliderede juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="00b06-113">Alternatively, the legal entities can use the same database as the consolidated legal entity.</span></span> <span data-ttu-id="00b06-114">Denne konsolideringsproces kaldes en *onlinekonsolidering*.</span><span class="sxs-lookup"><span data-stu-id="00b06-114">This consolidation process is referred to as an *online consolidation*.</span></span>

<span data-ttu-id="00b06-115">Den konsoliderede juridiske enhed indsamler resultater og saldi fra datterselskaber.</span><span class="sxs-lookup"><span data-stu-id="00b06-115">The consolidated legal entity collects the results and balances of the subsidiaries.</span></span> <span data-ttu-id="00b06-116">Hvis du vil forberede en konsolideret juridisk enhed for en konsolidering, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="00b06-116">To prepare a consolidated legal entity for a consolidation, follow these steps.</span></span>

1. <span data-ttu-id="00b06-117">Gå til **Finans \> Opsætning \> Organisation \> Juridiske enheder**.</span><span class="sxs-lookup"><span data-stu-id="00b06-117">Go to **General ledger \> Setup \> Organization \> Legal entities**.</span></span>
2. <span data-ttu-id="00b06-118">Vælg **Ny** for at oprette en ny juridisk enhed, som skal være den konsoliderede juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="00b06-118">Select **New** to create the legal entity that will be the consolidated legal entity.</span></span>
3. <span data-ttu-id="00b06-119">Markér afkrydsningsfeltet **Brug til økonomisk konsolideringsproces**, og angiv derefter oplysninger om den konsoliderede juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="00b06-119">Select the **Use for financial consolidation process** check box, and then enter information about the consolidated legal entity.</span></span> <span data-ttu-id="00b06-120">Sørg for at indtaste oplysningerne nøjagtigt som de skal vises på opgørelser for den konsoliderede juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="00b06-120">Be sure to enter this information exactly as you want it to appear on financial statements for the consolidated legal entity.</span></span>
4. <span data-ttu-id="00b06-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="00b06-121">Close the page.</span></span>
5. <span data-ttu-id="00b06-122">Vælg den konsoliderede juridiske enhed i feltet øverst til højre på siden, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="00b06-122">Select the consolidated legal entity in the field in the upper-right corner of the page, and then select **OK**.</span></span>
6. <span data-ttu-id="00b06-123">Gå til **Finans \> Opsætning \> Finans**.</span><span class="sxs-lookup"><span data-stu-id="00b06-123">Go to **General ledger \> Setup \> Ledger**.</span></span>
7. <span data-ttu-id="00b06-124">Vælg kontoplan, regnskabskalenderen, regnskabsvaluta, en valgfri rapporteringsvaluta og standardvalutakurstypen for den konsoliderede juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="00b06-124">Select the chart of accounts, the fiscal calendar, the accounting currency, an optional reporting currency, and the default type of exchange rate for the consolidated legal entity.</span></span> 
8. <span data-ttu-id="00b06-125">Gå til **Finans \> Opsætning \> Valuta \> Valutakurser**.</span><span class="sxs-lookup"><span data-stu-id="00b06-125">Go to **General ledger \> Setup \> Currency \> Currency exchange rates**.</span></span>
9. <span data-ttu-id="00b06-126">Angiv valutakurser i relevante perioder for valutaerne for de underliggende juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="00b06-126">Set up currency exchange rates in relevant periods for the currencies of the subsidiary legal entities.</span></span>
10. <span data-ttu-id="00b06-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="00b06-127">Close the page.</span></span>
11. <span data-ttu-id="00b06-128">Hvis den konsoliderede juridiske enhed har datterselskaber, der bruger fremmede valutaer, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="00b06-128">If the consolidated legal entity has subsidiaries that use foreign currencies, follow these steps:</span></span>

    1. <span data-ttu-id="00b06-129">Gå til **Finans \> Opsætning \> Bogføring \> Konti til automatiske posteringer**.</span><span class="sxs-lookup"><span data-stu-id="00b06-129">Go to **General ledger \> Setup \> Posting \> Accounts for automatic transactions**.</span></span>
    2. <span data-ttu-id="00b06-130">Vælg en relevant konto i feltet **Bogføringstype** :</span><span class="sxs-lookup"><span data-stu-id="00b06-130">In the **Posting type** field, select an appropriate account:</span></span>

        - <span data-ttu-id="00b06-131">Hvis den juridiske enhed har udenlandske datterselskaber, der er økonomisk eller driftsmæssige afhængige af den overordnede juridiske enhed, skal du vælge en passende konto til **Driftsregnskab for bogføringstypen for konsolideringsafvigelser**-typen.</span><span class="sxs-lookup"><span data-stu-id="00b06-131">If the legal entity has foreign subsidiaries that are financially or operationally interdependent with the parent legal entity, select an appropriate account for the **Profit and loss account for consolidation differences** posting type.</span></span>
        - <span data-ttu-id="00b06-132">Hvis du konsoliderer et datterselskab, som er økonomisk og driftsmæssigt uafhængigt af den overordnede juridiske enhed, eller en juridisk enhed, der indeholder resultaterne fra flere datterselskaber, som er økonomisk og driftsmæssigt uafhængige af den overordnede juridiske enhed, og hvis du bruger oversættelsesmetoder til konsolidering af data, skal du vælge en relevant konto for bogføringstypen **Driftsregnskab for bogføringstypen for konsolideringsafvigelser**.</span><span class="sxs-lookup"><span data-stu-id="00b06-132">If you're consolidating a subsidiary that is financially and operationally independent of the parent legal entity, or a legal entity that contains the results of several subsidiaries that are financially and operationally independent of the parent legal entity, and if you're using translation methods to consolidate the data, select an appropriate account for the **Balance account for consolidation differences** posting type.</span></span>

    3. <span data-ttu-id="00b06-133">Vælg de hovedkonti, der skal bruges til værdireguleringer af fremmed valuta, i feltet **Hovedkonto**.</span><span class="sxs-lookup"><span data-stu-id="00b06-133">In the **Main account** field, select the main accounts that should be used for foreign currency revaluation adjustments.</span></span>
    4. <span data-ttu-id="00b06-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="00b06-134">Close the page.</span></span>

    <span data-ttu-id="00b06-135">Hvis du opretter den konsoliderede juridiske enhed tidligt i en periode, kan du regulere de udenlandske valutabeløb som valutakursændringer under konsolideringsperioden.</span><span class="sxs-lookup"><span data-stu-id="00b06-135">If you create the consolidated legal entity early in a period, you can revalue foreign currency amounts as exchange rates change during the consolidation period.</span></span>

<span data-ttu-id="00b06-136">Den konsoliderede juridiske enhed er nu konfigureret til det periodiske job **Konsolider**.</span><span class="sxs-lookup"><span data-stu-id="00b06-136">The consolidated legal entity is now set up for the **Consolidate** periodic job.</span></span> <span data-ttu-id="00b06-137">Du kan enten udføre en importkonsolidering eller en onlinekonsolidering.</span><span class="sxs-lookup"><span data-stu-id="00b06-137">You can do either an import consolidation or an online consolidation.</span></span>

- <span data-ttu-id="00b06-138">Du kan udføre en importkonsolidering ved at gå til **Finans \> Periodisk \> Konsolider \> Konsolider \[Importer fra\]**.</span><span class="sxs-lookup"><span data-stu-id="00b06-138">To do an import consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Import from\]**.</span></span>
- <span data-ttu-id="00b06-139">Du kan udføre en online-konsolidering ved at gå til **Finans \> Periodisk \> Konsolider \> Konsolider \[Online\]**.</span><span class="sxs-lookup"><span data-stu-id="00b06-139">To do an online consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Online\]**.</span></span>

> [!NOTE]
> <span data-ttu-id="00b06-140">Inden du kan behandle konsolideringen, skal du klargøre de underordnede juridiske enheder til konsolidering.</span><span class="sxs-lookup"><span data-stu-id="00b06-140">Before you can process the consolidation, you must prepare the subsidiary legal entities for consolidation.</span></span> <span data-ttu-id="00b06-141">Du kan finde flere oplysninger i [Konfigurere en juridisk datterselskabsenhed til konsolidering](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="00b06-141">For more information, see [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>
