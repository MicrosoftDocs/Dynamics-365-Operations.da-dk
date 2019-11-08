---
title: Opsæt foretrukne vedligeholdelsesarbejdere
description: Dette emne beskriver, hvordan du konfigurerer foretrukne vedligeholdelsesarbejdere i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3501cb49cbc8b3060da03b3d2e9badc949910a48
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652189"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="4ce2e-103">Opsæt foretrukne vedligeholdelsesarbejdere</span><span class="sxs-lookup"><span data-stu-id="4ce2e-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4ce2e-104">Du kan under planlægning af arbejdsordrer angive en præference for, hvilken vedligeholdelsesarbejder eller vedligeholdelsesgruppe der skal tildeles for at afslutte arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="4ce2e-105">Brugen af denne funktion er valgfri, men den kan hjælpe dig med at vælge den mest kvalificerede vedligeholdelsesarbejder til at fuldføre et job baseret på arbejderens færdigheder og kompetencer.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="4ce2e-106">Kun vedligeholdelsesarbejdere, der er tilgængelige på planlægningstidspunktet, indgår i planlægningen.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="4ce2e-107">Hvis opsætning for en foretrukken vedligeholdelsesarbejder stemmer overens med en arbejdsordre under planlægningen, men vedligeholdelsesarbejderen er allokeret til andre job, planlægges arbejdsordren for en anden tilgængelig vedligeholdelsesarbejder.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="4ce2e-108">Før du kan konfigurere foretrukne vedligeholdelsesarbejdere, skal du først konfigurere vedligeholdelsesarbejdere og arbejdergrupper.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="4ce2e-109">Du kan finde en beskrivelse af, hvordan du konfigurerer vedligeholdelsesarbejdere og arbejdergrupper, under [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="4ce2e-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="4ce2e-110">Konfigurere foretrukne arbejdere</span><span class="sxs-lookup"><span data-stu-id="4ce2e-110">Set up preferred workers</span></span>

<span data-ttu-id="4ce2e-111">En foretrukket vedligeholdelsesarbejder eller arbejdergruppe kan knyttes til en eller flere af følgende:</span><span class="sxs-lookup"><span data-stu-id="4ce2e-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="4ce2e-112">handel</span><span class="sxs-lookup"><span data-stu-id="4ce2e-112">trade</span></span>  
- <span data-ttu-id="4ce2e-113">variant af en vedligeholdelsesjobtype</span><span class="sxs-lookup"><span data-stu-id="4ce2e-113">maintenance job type variant</span></span>  
- <span data-ttu-id="4ce2e-114">vedligeholdelsesjobtype</span><span class="sxs-lookup"><span data-stu-id="4ce2e-114">maintenance job type</span></span>  
- <span data-ttu-id="4ce2e-115">kategori for vedligeholdelsesjobtype</span><span class="sxs-lookup"><span data-stu-id="4ce2e-115">maintenance job type category</span></span>  
- <span data-ttu-id="4ce2e-116">aktiv</span><span class="sxs-lookup"><span data-stu-id="4ce2e-116">asset</span></span>  
- <span data-ttu-id="4ce2e-117">aktivtype</span><span class="sxs-lookup"><span data-stu-id="4ce2e-117">asset type</span></span>  

<span data-ttu-id="4ce2e-118">Jo flere valg du foretager for den samme post, jo mere specifik bliver din opsætning.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="4ce2e-119">Klik på **Styring af aktiver** > **Opsætning** > **Arbejdere** > **Foretrukne vedligeholdelsesarbejdere**.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="4ce2e-120">Klik på **Ny** for at oprette en ny post.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="4ce2e-121">Start med at oprette en "standard"-vedligeholdelsesarbejder eller -arbejdergruppe.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="4ce2e-122">Det betyder, at du kun foretager valg i feltet **Foretrukken vedligeholdelsesarbejdergruppe** eller i feltet **Foretrukne vedligeholdelsesarbejdere**.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="4ce2e-123">I nedenstående skærmbillede kan du se et eksempel i den første post, hvor "Anmodninger" er valgt som **Foretrukken vedligeholdelsesarbejdergruppe**.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="4ce2e-124">Denne standardopsætning bruges i forbindelse med planlægningen af arbejdsordrer, hvis der ikke er angivet en mere specifik kombination, som svarer til indholdet af arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="4ce2e-125">Gentag trin 2 for at oprette en ny post.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="4ce2e-126">Foretag de nødvendige valg, afhængigt af detaljeringsniveauet for den foretrukne arbejder eller arbejdergruppe.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="4ce2e-127">*Eksempel:* skærmbilledet nedenfor er Shawn Richardson valgt som foretrukken arbejder.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="4ce2e-128">Han vil automatisk blive valgt under planlægning af en arbejdsordre, der omfatter aktivet "CH-BP1-03-02 og vedligeholdelsesjobtypen"Facilitetsvurdering ", hvis han er ledig på det planlagte tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="4ce2e-129">Når der vælges en foretrukken vedligeholdelsesarbejder under planlægningen af arbejdsordrer, gennemgår Styring af aktiver alle poster med **Foretrukne vedligeholdelsesarbejdere** for at søge efter et muligt match og kontrollere altid den mest specifikke kombination først.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="4ce2e-130">Hvis der ikke findes et match, bruges posten "standard" med et valg i enten feltet **Foretrukken vedligeholdelsesarbejdergruppe** eller feltet **Foretrukken vedligeholdelsesarbejder**.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![Figur 1](media/02-work-order-scheduling.png)

<span data-ttu-id="4ce2e-132">Du kan også konfigurere *ansvarlige* vedligeholdelsesarbejdere, der kan vælges, når der oprettes en vedligeholdelsesanmodning eller en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="4ce2e-133">I **Alle arbejdsordrer** og **Alle vedligeholdelsesanmodninger** kan du redigere valget, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="4ce2e-134">Se [Ansvarlige vedligeholdelsesarbejdere](../setup-for-maintenance-requests/responsible-workers.md) for at få yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="4ce2e-135">Under planlægningen af arbejdsordren beregnes der forskellige scorer for at bestemme, hvilke arbejdere der skal udføre de job, der vedrører en arbejdsordre (disse scorer konfigureres i **Styring af aktiver** > **Planlægning af arbejdsordrer**-linket).</span><span class="sxs-lookup"><span data-stu-id="4ce2e-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="4ce2e-136">Hvis to eller flere foretrukne vedligeholdelsesarbejdere eller ansvarlige vedligeholdelsesarbejdere har samme score under planlægningen af arbejdsordrer, vælges én arbejder tilfældigt.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="4ce2e-137">Ellers er det altid arbejderen med den højeste score, der tildeles til at fuldføre en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="4ce2e-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

