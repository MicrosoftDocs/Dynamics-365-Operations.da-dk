---
title: Bogfør anlægsaktivposteringer i posteringslag
description: Denne artikel giver et overblik over bogføringslagets funktionalitet for anlægsaktivposteringer.
author: moaamer
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a80e4d1a081b5bd8c58238b0f154f8fbdc660ccb
ms.sourcegitcommit: f80819c67c0a7475315fc68ce1cb568831e2c0e7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/10/2020
ms.locfileid: "4493666"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="bcd1f-103">Bogfør anlægsaktivposteringer i posteringslag</span><span class="sxs-lookup"><span data-stu-id="bcd1f-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcd1f-104">Denne artikel giver et overblik over bogføringslagets funktionalitet for anlægsaktivposteringer.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="bcd1f-105">Et anlægsaktiv afskrives ofte på forskellige måder til forskellige formål.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="bcd1f-106">Afskrivningen til skattemæssige formål beregnes ud fra de aktuelle skatteregler for at opnå den højest mulige afskrivning før skat, mens afskrivning til bogføringsmæssige formål beregnes ud fra regnskabslove og -standarder.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="bcd1f-107">De forskellige slags afskrivning beregnes og bogføres separat i posteringslagene.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="bcd1f-108">Hver bog, der tilknyttes et anlægsaktiv, oprettes til et bestemt posteringslag med et overordnet afskrivningsformål.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="bcd1f-109">Der er ti posteringslag: aktuelle, operationer, skat og syv brugerdefinerede lag.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="bcd1f-110">Du kan også deaktivere bogføring i finansmodulet for bogen ved at angive feltet Bogfør i finans felt til Nej.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="bcd1f-111">Feltet Posteringslag, angives derefter automatisk til Ingen.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="bcd1f-112">Typisk bruges bøger, der ikke bogføres i finansmodulet, til momsrapporteringen.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="bcd1f-113">Denne fremgangsmåde giver dig yderligere fleksibilitet til at slette historiske posteringer for anlægsaktivkartoteket, fordi de ikke er gemt i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="bcd1f-114">Anlægsaktivkladder defineres ved hjælp af siden Kladdenavne via Finans > Konfiguration af kladde > Kladdenavne.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="bcd1f-115">Hver af de kladder, som du kan bogføre afskrivninger i, defineres ud fra sit kladdenavn for kun ét posteringslag.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="bcd1f-116">Posteringslaget i kladden kan ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="bcd1f-117">Denne begrænsning hjælper med at sikre, at posteringerne for hvert posteringslag holdes adskilt.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="bcd1f-118">Der skal oprettes mindst ét kladdenavn for hvert posteringslag.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="bcd1f-119">Hvis du bruger bøger, der ikke bogføres i finansmodulet, skal du også oprette en kladde, hvor posteringslaget er angivet til Ingen.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="bcd1f-120">Du kan angive finanskonti for anlægsaktivposter på siden Posteringsprofiler for anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="bcd1f-121">For hver posteringsprofil skal du vælge den relevante posteringstype og bog og derefter tildele finanskontiene.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="bcd1f-122">Opret en bogføringsprofilpost for hver bog, der skal bogføres i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

<span data-ttu-id="bcd1f-123">Anlægsaktivet kan angives i dokumenter, der kun understøtter det **Aktuelle** posteringslag, f. eks. **Indkøbsordre**, **Ventende kreditorfaktura**, **Salgsordre** eller **Fritekstfaktura**.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-123">The fixed asset can be entered in documents that only support the **Current** posting layer, like **Purchase order**, **Pending vendor invoice**, **Sales order**, or **Free text invoice**.</span></span> <span data-ttu-id="bcd1f-124">Når du vælger et anlægsaktiv-ID i et af disse dokumenter, filtreres anlægsaktivet til kartoteket med det **Aktuelle** posteringslag og udfyldes automatisk under bogføringen, når systemet kontrollerer, at posteringslaget for anlægsaktiver er **Aktuelt**.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-124">While selecting a fixed asset ID in any of those documents the asset book is filtered to the book with **Current** posting layer, and will be filled in automatically, during posting when the system validates that the fixed asset posting layer is **Current**.</span></span> <span data-ttu-id="bcd1f-125">Hvis denne validering ikke kan fuldføres, vil bogføringsprocessen blive stoppet.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-125">If that validation can't be completed, the posting process will be stopped.</span></span> 

> [!NOTE] 
> <span data-ttu-id="bcd1f-126">Hvis du bruger afledte bøger, kan du bogføre posteringer på forskellige posteringslag samtidig.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-126">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="bcd1f-127">Transaktionerne for det primære kartotek oprettes i en kladde eller kildedokument, der svarer til posteringslaget for kartotekets posteringslag.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-127">The transactions of the primary book are created in a journal or source document where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="bcd1f-128">Under posteringen bogføres de afledte bogposteringer på deres respektive posteringslag.</span><span class="sxs-lookup"><span data-stu-id="bcd1f-128">During posting, the derived book transactions will be posted to the appropriate posting layers.</span></span> 


<span data-ttu-id="bcd1f-129">Yderligere oplysninger finder du i afsnittet [Afledte bøger](derived-books.md) og [Bogfør med afledte bøger](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="bcd1f-129">For more information see, [Derived books](derived-books.md) and [Post with derived books](post-derived-value-models.md).</span></span>



