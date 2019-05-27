---
title: Straksafskrivning
description: Denne artikel indeholder en oversigt over funktionerne til bonusafskrivning.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e05c0c195ddb948547ae008d050686bbcdc6ed3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567472"
---
# <a name="bonus-depreciation"></a><span data-ttu-id="3cab2-103">Straksafskrivning</span><span class="sxs-lookup"><span data-stu-id="3cab2-103">Bonus depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3cab2-104">Denne artikel indeholder en oversigt over funktionerne til bonusafskrivning.</span><span class="sxs-lookup"><span data-stu-id="3cab2-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="3cab2-105">Du kan bruge straksafskrivning til ekstra- eller straksafskrivning det første år, et anlægsaktiv er taget i anvendelse og afskrives.</span><span class="sxs-lookup"><span data-stu-id="3cab2-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="3cab2-106">Straksafskrivning skal foretages før eventuelle andre afskrivningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="3cab2-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="3cab2-107">Det er derfor bedst at bruge straksafskrivning med bøger, hvor bogføring til Finans-funktionalitet er deaktiveret.</span><span class="sxs-lookup"><span data-stu-id="3cab2-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="3cab2-108">Du kan bruge indstillingen **Slet transaktioner, der ikke er bogført i Finans** til at slette historiske transaktioner for bøger, der ikke bogføres i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="3cab2-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="3cab2-109">Du kan derefter tilpasse straksafskrivning senere i aktivets levetid ved at slette afskrivningstransaktioner, der tidligere er bogført.</span><span class="sxs-lookup"><span data-stu-id="3cab2-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="3cab2-110">Du kan beregne straksafskrivningen ved hjælp af forslagsprocessen, eller du kan oprette manuelle transaktioner til straksafskrivning.</span><span class="sxs-lookup"><span data-stu-id="3cab2-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="3cab2-111">Du kan ikke oprette transaktioner til straksafskrivning, hvis der findes afskrivningstransaktioner eller transaktioner til afskrivningsregulering for den pågældende afskrivningsmodel.</span><span class="sxs-lookup"><span data-stu-id="3cab2-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="3cab2-112">Når du bruger forslagsprocessen til beregning af straksafskrivning, inkluderes alle eksisterende transaktioner i beregningen af grundlaget.</span><span class="sxs-lookup"><span data-stu-id="3cab2-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="3cab2-113">Beregningen inkluderer også eventuelle tidligere straksafskrivninger, som du har angivet manuelt for aktivet.</span><span class="sxs-lookup"><span data-stu-id="3cab2-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="3cab2-114">Når der skal foretages mere end én straksafskrivning for et aktiv, tages prioriteten i betragtning.</span><span class="sxs-lookup"><span data-stu-id="3cab2-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="3cab2-115">Hver straksafskrivning reducerer anlægsaktivgrundlaget for den efterfølgende straksafskrivning.</span><span class="sxs-lookup"><span data-stu-id="3cab2-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="3cab2-116">Restværdien medtages ikke i anlægsaktivgrundlaget ved beregninger af straksafskrivning, og afskrivningsprincippet gælder ikke for straksafskrivningen.</span><span class="sxs-lookup"><span data-stu-id="3cab2-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="3cab2-117">I USA er det i øjeblikket sådan, at visse anlægsaktiver gælder som Section 179-anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="3cab2-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="3cab2-118">En Section 179-afskrivning giver mulighed for at afskrive alle eller nogle af omkostningerne for et bestemt anlægsaktiv, op til en vis grænse.</span><span class="sxs-lookup"><span data-stu-id="3cab2-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="3cab2-119">Du kan få dækning for omkostningen ved at afskrive den i det år, hvor anlægsaktivet tages i anvendelse.</span><span class="sxs-lookup"><span data-stu-id="3cab2-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="3cab2-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="3cab2-120">Example</span></span>
<span data-ttu-id="3cab2-121">Følgende straksafskrivninger er tilknyttet en aktivbog:</span><span class="sxs-lookup"><span data-stu-id="3cab2-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="3cab2-122">**Section 179:** 1.000,00, Prioritet 1</span><span class="sxs-lookup"><span data-stu-id="3cab2-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="3cab2-123">**Fritagelseszone:** 30 procent, Prioritet 2</span><span class="sxs-lookup"><span data-stu-id="3cab2-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="3cab2-124">Omkostningerne ved anskaffelsen af anlægsaktivet er 5.000,00.</span><span class="sxs-lookup"><span data-stu-id="3cab2-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="3cab2-125">Når straksafskrivningen beregnes, vil beløbet for den første straksafskrivning være 1.000,00 for Section 179-afskrivningen.</span><span class="sxs-lookup"><span data-stu-id="3cab2-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="3cab2-126">Det næste straksafskrivningsbeløb i afskrivningen for Liberty Zone beregnes som følger:</span><span class="sxs-lookup"><span data-stu-id="3cab2-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="3cab2-127">Anskaffelsesomkostninger – 1.000 (Section 179-afskrivning) x 30 % = 1.200</span><span class="sxs-lookup"><span data-stu-id="3cab2-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="3cab2-128">Hvis beløbet i straksafskrivningen er større end det resterende beløb for anskaffelsesomkostningen, vil beløbet for straksafskrivningen enten være resultatet af den beregnede straksafskrivning eller den resterende anskaffelsesomkostning afhængigt af, hvilket beløb der er mindst.</span><span class="sxs-lookup"><span data-stu-id="3cab2-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="3cab2-129">Hvis den tilbageværende anskaffelsesomkostning er 0 (nul) eller mindre end nul, genereres der ikke afskrivningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="3cab2-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="3cab2-130">Når straksafskrivningen beregnes ved hjælp af forslagsprocessen, oprettes der en transaktion for straksafskrivningen for alle de relevante straksafskrivningsposter, der er tilknyttet aktivbogen.</span><span class="sxs-lookup"><span data-stu-id="3cab2-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="3cab2-131">Du kan oprette et ubegrænset antal straksafskrivningsposter.</span><span class="sxs-lookup"><span data-stu-id="3cab2-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="3cab2-132">Når du har tildelt aktivgruppebogen disse poster, anvendes de i aktivbogen.</span><span class="sxs-lookup"><span data-stu-id="3cab2-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="3cab2-133">Straksafskrivningen angives som enten en procentsats eller et fast beløb.</span><span class="sxs-lookup"><span data-stu-id="3cab2-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="3cab2-134">Når du bogfører afskrivningsforslag, bogføres transaktionerne for straksafskrivningen i bogen som andre transaktioner end afskrivningstransaktionerne.</span><span class="sxs-lookup"><span data-stu-id="3cab2-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>



