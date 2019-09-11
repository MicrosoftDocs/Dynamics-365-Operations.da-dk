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
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887405"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="2dc37-103">Foretrukne vedligeholdelsesarbejdere</span><span class="sxs-lookup"><span data-stu-id="2dc37-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="2dc37-104">Du kan angive en præference for, hvilke vedligeholdelsesarbejdere der skal tildeles for at afslutte arbejdsordrer under planlægning af arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="2dc37-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="2dc37-105">Brugen af denne funktion er valgfri, men den kan hjælpe dig med at vælge den mest kvalificerede vedligeholdelsesarbejder til at fuldføre et job baseret på arbejderens færdigheder og kompetencer.</span><span class="sxs-lookup"><span data-stu-id="2dc37-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="2dc37-106">Derfor bruges opsætningen i **Foretrukne vedligeholdelsesarbejdere** under planlægning af arbejdsordrer til at bestemme, om en bestemt vedligeholdelsesarbejder eller arbejdergruppe skal planlægges for en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="2dc37-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="2dc37-107">Kun vedligeholdelsesarbejdere, der er tilgængelige på planlægningstidspunktet, indgår i planlægningen.</span><span class="sxs-lookup"><span data-stu-id="2dc37-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="2dc37-108">Hvis opsætning for en foretrukken vedligeholdelsesarbejder stemmer overens med en arbejdsordre under planlægningen, men vedligeholdelsesarbejderen er allokeret til andre job, planlægges arbejdsordren for en anden tilgængelig vedligeholdelsesarbejder.</span><span class="sxs-lookup"><span data-stu-id="2dc37-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="2dc37-109">Før du kan konfigurere foretrukne vedligeholdelsesarbejdere, skal du først konfigurere de vedligeholdelsesarbejdere og arbejdergrupper, der skal kunne vælges.</span><span class="sxs-lookup"><span data-stu-id="2dc37-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="2dc37-110">Du kan finde en beskrivelse af, hvordan du konfigurerer vedligeholdelsesarbejdere og arbejdergrupper, i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="2dc37-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="2dc37-111">Konfigurere foretrukne arbejdere</span><span class="sxs-lookup"><span data-stu-id="2dc37-111">Set up preferred workers</span></span>

<span data-ttu-id="2dc37-112">En foretrukket vedligeholdelsesarbejder eller arbejdergruppe kan knyttes til en bestemt</span><span class="sxs-lookup"><span data-stu-id="2dc37-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="2dc37-113">handel</span><span class="sxs-lookup"><span data-stu-id="2dc37-113">trade</span></span>  
- <span data-ttu-id="2dc37-114">variant af en vedligeholdelsesjobtype</span><span class="sxs-lookup"><span data-stu-id="2dc37-114">maintenance job type variant</span></span>  
- <span data-ttu-id="2dc37-115">vedligeholdelsesjobtype</span><span class="sxs-lookup"><span data-stu-id="2dc37-115">maintenance job type</span></span>  
- <span data-ttu-id="2dc37-116">kategori for vedligeholdelsesjobtype</span><span class="sxs-lookup"><span data-stu-id="2dc37-116">maintenance job type category</span></span>  
- <span data-ttu-id="2dc37-117">aktiv</span><span class="sxs-lookup"><span data-stu-id="2dc37-117">asset</span></span>  
- <span data-ttu-id="2dc37-118">aktivtype</span><span class="sxs-lookup"><span data-stu-id="2dc37-118">asset type</span></span>  

<span data-ttu-id="2dc37-119">eller en kombination af disse valg.</span><span class="sxs-lookup"><span data-stu-id="2dc37-119">or a combination of those selections.</span></span> <span data-ttu-id="2dc37-120">Jo flere valg du foretager for den samme post, jo mere specifik bliver din opsætning.</span><span class="sxs-lookup"><span data-stu-id="2dc37-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="2dc37-121">Klik på **Styring af aktiver** > **Opsætning** > **Arbejdere** > **Foretrukne vedligeholdelsesarbejdere**.</span><span class="sxs-lookup"><span data-stu-id="2dc37-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="2dc37-122">Klik på **Ny** for at oprette en ny post.</span><span class="sxs-lookup"><span data-stu-id="2dc37-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="2dc37-123">Start med at oprette en "standardopsætning" for vedligeholdelsesarbejdere eller arbejdergrupper, der ikke har nogen markeringer i de felter, der vises på punktlisten ovenfor.</span><span class="sxs-lookup"><span data-stu-id="2dc37-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="2dc37-124">Det betyder, at du kun foretager valg i feltet **Foretrukken vedligeholdelsesarbejdergruppe** eller i feltet **Foretrukne vedligeholdelsesarbejdere**.</span><span class="sxs-lookup"><span data-stu-id="2dc37-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="2dc37-125">I nedenstående figur kan du se et eksempel i den første post, hvor "Anmodninger" er valgt som foretrukken vedligeholdelsesarbejdergruppe.</span><span class="sxs-lookup"><span data-stu-id="2dc37-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="2dc37-126">Standardopsætningen bruges i forbindelse med planlægningen af arbejdsordrer, hvis der ikke er angivet en mere specifik kombination, som svarer til indholdet af arbejdsordren under planlægningen af arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="2dc37-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="2dc37-127">Gentag trin 2 for at oprette en ny post.</span><span class="sxs-lookup"><span data-stu-id="2dc37-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="2dc37-128">Foretag de nødvendige valg, afhængigt af detaljeringsniveauet for den foretrukne arbejder eller arbejdergruppe.</span><span class="sxs-lookup"><span data-stu-id="2dc37-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="2dc37-129">*Eksempel:* I den sjette post i figuren nedenfor er Shawn Richardson valgt som foretrukken arbejder.</span><span class="sxs-lookup"><span data-stu-id="2dc37-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="2dc37-130">Han vil automatisk blive valgt ved planlægning af en arbejdsordre, der omfatter aktivet "CH-BP1-03-02 og vedligeholdelsesjobtypen"Facilitetsvurdering ", hvis han er tilgængelig på det planlagte tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="2dc37-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="2dc37-131">Når der vælges en foretrukken vedligeholdelsesarbejder under planlægningen af arbejdsordrer, gennemgår Styring af aktiver alle poster med **Foretrukne vedligeholdelsesarbejdere** for at søge efter et muligt match og kontrollere altid den mest specifikke kombination først.</span><span class="sxs-lookup"><span data-stu-id="2dc37-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="2dc37-132">Hvis der ikke findes et match, bruges posten "standard" med et valg i enten feltet **Foretrukken vedligeholdelsesarbejdergruppe** eller feltet **Foretrukken vedligeholdelsesarbejder**.</span><span class="sxs-lookup"><span data-stu-id="2dc37-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![Figur 1](media/02-work-order-scheduling.png)

<span data-ttu-id="2dc37-134">Du kan også konfigurere ansvarlige vedligeholdelsesarbejdere, der kan vælges, når der oprettes en vedligeholdelsesanmodning eller en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="2dc37-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="2dc37-135">I **Alle arbejdsordrer** og **Alle vedligeholdelsesanmodninger** kan du evt. redigere valget, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="2dc37-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="2dc37-136">Se [Ansvarlige vedligeholdelsesarbejdere](../setup-for-maintenance-requests/responsible-workers.md) for at få yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="2dc37-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="2dc37-137">Under planlægningen af arbejdsordren beregnes der forskellige scorer for at bestemme, hvilke arbejdere der skal udføre de job, der vedrører en arbejdsordre (disse scorer konfigureres i **Styring af aktiver** > **Planlægning af arbejdsordrer**-linket).</span><span class="sxs-lookup"><span data-stu-id="2dc37-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="2dc37-138">Hvis to eller flere foretrukne vedligeholdelsesarbejdere eller ansvarlige vedligeholdelsesarbejdere har samme score under planlægningen af arbejdsordrer, vælges én arbejder tilfældigt.</span><span class="sxs-lookup"><span data-stu-id="2dc37-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="2dc37-139">Ellers er det altid arbejderen med den højeste score, der tildeles til at fuldføre en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="2dc37-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

