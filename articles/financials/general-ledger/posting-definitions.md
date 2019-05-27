---
title: Bogføringsdefinitioner
description: Denne artikel indeholder oplysninger om bogføringsdefinitioner, og hvordan du definerer og kæder dem sammen. Til understøttede bogføringstyper og -dokumenter kan du bruge bogføringsdefinitioner i stedet for posteringsprofiler til at klassificere hovedkonti og økonomiske dimensioner på regnskabsposter.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e9d1e593f58e8fc9e12ddac7664b6e67ecda6a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561008"
---
# <a name="posting-definitions"></a><span data-ttu-id="5a83e-104">Bogføringsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="5a83e-104">Posting definitions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a83e-105">Denne artikel indeholder oplysninger om bogføringsdefinitioner, og hvordan du definerer og kæder dem sammen.</span><span class="sxs-lookup"><span data-stu-id="5a83e-105">This article provides information about posting definitions, and how to define and link them.</span></span> <span data-ttu-id="5a83e-106">Til understøttede bogføringstyper og -dokumenter kan du bruge bogføringsdefinitioner i stedet for posteringsprofiler til at klassificere hovedkonti og økonomiske dimensioner på regnskabsposter.</span><span class="sxs-lookup"><span data-stu-id="5a83e-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span>

<span data-ttu-id="5a83e-107">Til understøttede bogføringstyper og -dokumenter kan du bruge bogføringsdefinitioner i stedet for posteringsprofiler til at klassificere hovedkonti og økonomiske dimensioner på regnskabsposter.</span><span class="sxs-lookup"><span data-stu-id="5a83e-107">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="5a83e-108">Du kan se de understøttede dokumenter og bogføringstyper på siden **Definitioner af posteringsbogføring**.</span><span class="sxs-lookup"><span data-stu-id="5a83e-108">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="5a83e-109">Hvis du vil bruge bogføringsdefinitioner, skal du vælge indstillingen **Brug bogføringsdefinitioner** på siden **Finansparametre**.</span><span class="sxs-lookup"><span data-stu-id="5a83e-109">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="5a83e-110">Selv når du bruger bogføringsdefinitioner, skal du stadig definere posteringsprofiler for de oprindelige poster og de ikke-understøttede bogføringsprofiler og -dokumenter.</span><span class="sxs-lookup"><span data-stu-id="5a83e-110">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="5a83e-111">Du skal bruge bogføringsdefinitioner for at kunne aktivere indeholder bogføring af behæftelser for indkøbsordrer og bogføring af budgetreservationer for indkøbsrekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="5a83e-111">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="5a83e-112">Definition af bogføringsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="5a83e-112">Defining posting definitions</span></span>
<span data-ttu-id="5a83e-113">Brug siden **Bogføringsdefinitioner** til at angive søgekriterier og definere de poster, der skal genereres, når der opstår et match.</span><span class="sxs-lookup"><span data-stu-id="5a83e-113">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="5a83e-114">Søgekriterierne evalueres som regnskabsfordelinger for de oprindelige poster.</span><span class="sxs-lookup"><span data-stu-id="5a83e-114">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="5a83e-115">På siden **Bogføringsdefinitioner** kan du også tildele prioritetsnumre til posteringslinjer for at styre den rækkefølge, linjerne evalueres i.</span><span class="sxs-lookup"><span data-stu-id="5a83e-115">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="5a83e-116">De linjer, der har det laveste prioritetsnummer, evalueres først.</span><span class="sxs-lookup"><span data-stu-id="5a83e-116">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="5a83e-117">For eksempel evalueres alle linjer, der har prioritet 1, og derefter linjer, der har en prioritet 2, osv.</span><span class="sxs-lookup"><span data-stu-id="5a83e-117">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="5a83e-118">Når der er overensstemmelse, ignoreres de andre søgekriterier.</span><span class="sxs-lookup"><span data-stu-id="5a83e-118">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="5a83e-119">Desuden er det kun de kriterier i gruppen, der matcher den oprindelige transaktion, der opretter genererede poster.</span><span class="sxs-lookup"><span data-stu-id="5a83e-119">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="5a83e-120">Du kan validere dine bogføringsdefinitioner ved hjælp af guiden **Test bogføringsdefinition**.</span><span class="sxs-lookup"><span data-stu-id="5a83e-120">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="5a83e-121">Når du definerer et eksempel på en oprindelig postering for en bogføringsdefinition, kan du se de genererede poster.</span><span class="sxs-lookup"><span data-stu-id="5a83e-121">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="5a83e-122">Du kan bruge bogføringsdefinitionsversioner sammen med ikrafttrædelsesdatoer.</span><span class="sxs-lookup"><span data-stu-id="5a83e-122">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="5a83e-123">Du kan f.eks. oprette en fremtidig version af en bogføringsdefinition til bogføring på en anden finanskonti i et nyt regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="5a83e-123">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="5a83e-124">Brug siden **Definitioner af posteringsbogføring** til at tildele bogføringsdefinitioner til transaktionstyper.</span><span class="sxs-lookup"><span data-stu-id="5a83e-124">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="5a83e-125">Tilknytning af bogføringsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="5a83e-125">Linking posting definitions</span></span>
<span data-ttu-id="5a83e-126">Du kan sammenkæde én bogføringsdefinition med en anden, når du opretter dem.</span><span class="sxs-lookup"><span data-stu-id="5a83e-126">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="5a83e-127">Kriterierne for den definition, du har sammenkædet til, tages derefter i betragtning sammen med kriterierne for den aktuelle bogføringsdefinition.</span><span class="sxs-lookup"><span data-stu-id="5a83e-127">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="5a83e-128">Denne funktion hjælper dig med at spare tid, fordi du ikke behøver at indtaste kriterierne igen på oversigtspanelet **Poster** på siden **Bogføringsdefinitioner** for den aktuelle bogføringsdefinition, hvis du allerede har angivet linjerne for en anden definition.</span><span class="sxs-lookup"><span data-stu-id="5a83e-128">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="5a83e-129">I diagrammerne eller tabellerne kan du alle de sammenkædninger, du kan komme til at bruge.</span><span class="sxs-lookup"><span data-stu-id="5a83e-129">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="5a83e-130">For at undgå konflikter med den aktuelle bogføringsdefinition bør du sikre dig, at linjerne i alle bogføringsdefinitioner, som du sammenkæder til, er entydige.</span><span class="sxs-lookup"><span data-stu-id="5a83e-130">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="5a83e-131">Der er følgende begrænsninger, når du opretter sammenkædninger i bogføringsdefinitioner:</span><span class="sxs-lookup"><span data-stu-id="5a83e-131">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="5a83e-132">En given bogføringsdefinition kan enten sammenkædes med en anden bogføringsdefinition, eller der kan oprettes en sammenkædning til den fra en anden bogføringsdefinition, men ikke begge dele.</span><span class="sxs-lookup"><span data-stu-id="5a83e-132">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="5a83e-133">Men en bogføringsdefinition kan blive kædet samme med flere bogføringsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="5a83e-133">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="5a83e-134">Du kan oprette sammenkædninger blandt bogføringsdefinitioner i samme modul.</span><span class="sxs-lookup"><span data-stu-id="5a83e-134">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="5a83e-135">Du kan tildele en bogføringsdefinition til alle posteringstyper, men posteringstypen skal være i samme modul som bogføringsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5a83e-135">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="5a83e-136">Brug siden **Definitioner af posteringsbogføring** for at se, hvilket modul en transaktionstype er i.</span><span class="sxs-lookup"><span data-stu-id="5a83e-136">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="5a83e-137">Yderligere oplysninger finder du i afsnittet [Eksempler på posteringsdefinitioner](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="5a83e-137">For more information, see [Posting definitions examples](example-posting-definitions.md).</span></span> 


