---
title: Behandle livshændelser
description: Under hele medarbejderens livscyklus i Microsoft Dynamics 365 Human Resources, kan de enkelte medarbejdere opleve forskellige ændringer i livshændelser.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 504408505168947ac725b5ee9764ecd994a64631
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429214"
---
# <a name="process-life-events"></a><span data-ttu-id="63b4e-103">Behandle livshændelser</span><span class="sxs-lookup"><span data-stu-id="63b4e-103">Process life events</span></span>

<span data-ttu-id="63b4e-104">Under hele medarbejderens livscyklus i Microsoft Dynamics 365 Human Resources, kan de enkelte medarbejdere opleve forskellige ændringer i livshændelser.</span><span class="sxs-lookup"><span data-stu-id="63b4e-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="63b4e-105">Det kan f.eks. være ægteskab, ændring i ansættelsesforhold eller ændringer af afhængig/modtager-forhold.</span><span class="sxs-lookup"><span data-stu-id="63b4e-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="63b4e-106">Hvis du vil bruge livshændelser, skal du aktivere livshændelser i formularen med parametre for frynsegoder, konfigurere typer af livshændelser og konfigurere indstillinger for livshændelser for plantyper.</span><span class="sxs-lookup"><span data-stu-id="63b4e-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="63b4e-107">Før du kan behandle livshændelser, skal du allerede have kørt åben tilmelding mindst en gang i løbet af en ansættelsesperiode.</span><span class="sxs-lookup"><span data-stu-id="63b4e-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="63b4e-108">I USA sker åbne tilmeldinger typisk én gang om året.</span><span class="sxs-lookup"><span data-stu-id="63b4e-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="63b4e-109">Uden for USA kan der køres en åben tilmelding på tidspunktet for ansættelsen.</span><span class="sxs-lookup"><span data-stu-id="63b4e-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="63b4e-110">En arbejder behøver ikke at vælge en frynsegodeplan, for at der kan behandles livshændelser, men de skal have været medtaget i en åben tilmeldingsbehandling.</span><span class="sxs-lookup"><span data-stu-id="63b4e-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="63b4e-111">Brug behandling af livshændelser, når du har arbejdere, der har en livshændelse, som finder sted på en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="63b4e-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="63b4e-112">Denne hændelse behandler alle de livshændelser, der ikke er behandlet (som f.eks. fremtidige livshændelser eller livshændelser, der er tilføjet, og som ikke er specifikke for én arbejder – det kan f.eks. være et nyt frynsegode).</span><span class="sxs-lookup"><span data-stu-id="63b4e-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="63b4e-113">Realtidslivshændelser er skjulte.</span><span class="sxs-lookup"><span data-stu-id="63b4e-113">Real-time life events are hidden.</span></span>

<span data-ttu-id="63b4e-114">Hvis dags dato f.eks. er 1. februar, og arbejder Karina Smith er den 14. februar planlagt til at ændre juridisk enhed, vil systemet behandle alle hændelser indtil den 15. februar, hvis du kører behandling af livshændelser for 15. februar.</span><span class="sxs-lookup"><span data-stu-id="63b4e-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="63b4e-115">Vælg **Behandling af livshændelser** under **Behandling** i arbejdsområdet **Frynsegodeadministration**.</span><span class="sxs-lookup"><span data-stu-id="63b4e-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="63b4e-116">Angiv værdier for følgende felter i dialogboksen **Kør behandling af livshændelse**:</span><span class="sxs-lookup"><span data-stu-id="63b4e-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="63b4e-117">Felt</span><span class="sxs-lookup"><span data-stu-id="63b4e-117">Field</span></span> | <span data-ttu-id="63b4e-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="63b4e-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="63b4e-119">**Tilmeldingsperiode**</span><span class="sxs-lookup"><span data-stu-id="63b4e-119">**Enrollment period**</span></span> | <span data-ttu-id="63b4e-120">Den tilmeldingsperiode, der skal behandles livshændelser for.</span><span class="sxs-lookup"><span data-stu-id="63b4e-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="63b4e-121">**Juridisk enhed**</span><span class="sxs-lookup"><span data-stu-id="63b4e-121">**Legal entity**</span></span> | <span data-ttu-id="63b4e-122">Den juridiske enhed, der skal behandles livshændelser for.</span><span class="sxs-lookup"><span data-stu-id="63b4e-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="63b4e-123">**Dato for livshændelse**</span><span class="sxs-lookup"><span data-stu-id="63b4e-123">**Life event date**</span></span> | <span data-ttu-id="63b4e-124">Systemet behandler alle hændelser under den tilmeldingsperiode, der indtræffer indtil denne dato.</span><span class="sxs-lookup"><span data-stu-id="63b4e-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="63b4e-125">**Arbejdstråd**</span><span class="sxs-lookup"><span data-stu-id="63b4e-125">**Worker**</span></span> | <span data-ttu-id="63b4e-126">Den arbejder, der skal behandles livshændelser for.</span><span class="sxs-lookup"><span data-stu-id="63b4e-126">The worker to process life events for.</span></span> <span data-ttu-id="63b4e-127">Hvis du ikke udfylder dette felt, behandles livshændelser for alle arbejdere.</span><span class="sxs-lookup"><span data-stu-id="63b4e-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="63b4e-128">Hvis du vil køre processen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="63b4e-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="63b4e-129">Angiv oplysninger om processen.</span><span class="sxs-lookup"><span data-stu-id="63b4e-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="63b4e-130">Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="63b4e-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="63b4e-131">Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="63b4e-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="63b4e-132">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="63b4e-132">Select **OK**.</span></span> <span data-ttu-id="63b4e-133">Processen køres med de parametre, du angiver.</span><span class="sxs-lookup"><span data-stu-id="63b4e-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="63b4e-134">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="63b4e-134">Select **OK**.</span></span>
