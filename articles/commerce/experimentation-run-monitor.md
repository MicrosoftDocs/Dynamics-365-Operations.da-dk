---
title: Køre og overvåge et eksperiment
description: Dette emne beskriver, hvordan du kører og overvåger et eksperiment i en tredjepartstjeneste. Det beskrives også, hvordan du foretager ændringer i variationer, efter at du har startet eksperimentet.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4afc19ed103f204fec61ab20b88f767ad5f05b38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792529"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="9d0a9-104">Køre og overvåge et eksperiment</span><span class="sxs-lookup"><span data-stu-id="9d0a9-104">Run and monitor an experiment</span></span>

<span data-ttu-id="9d0a9-105">Dette emne beskriver, hvordan du kører og overvåger dit eksperiment i en tredjepartsapp og eventuelt ændrer variationer.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="9d0a9-106">Før du udfører trinnene i dette emne, skal du først [publicere](experimentation-preview-publish.md) dit eksperimenter i Commerce.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-106">Before you complete the steps in this topic, you'll first need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> 

<span data-ttu-id="9d0a9-107">I følgende diagram vises alle de trin, der er nødvendige for at konfigurere og køre et eksperiment på et e-handelswebsted i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="9d0a9-108">Yderligere trin behandles i separate emner.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="9d0a9-109">[ ![Eksperimenteringens brugerrejse - køre og overvåge](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="9d0a9-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="9d0a9-110">Når du har publiceret dine variationer, skal du udføre alle de nødvendige trin i Commerce for at køre dit eksperiment.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-110">After you publish your variations, all of the steps you need to do in Commerce to run your experiment are complete.</span></span> <span data-ttu-id="9d0a9-111">Det næste trin er afgørende for, hvilken variation der skal vises for hver enkelt bruger, når de anmoder om en side.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="9d0a9-112">Tredjepartstjenesten foretager denne beslutning, men først skal du aktivere eksperimentet i tjenesten.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="9d0a9-113">Da trinnene til aktivering af et eksperiment varierer fra tjeneste til tjeneste, skal du følge vejledningen til i din tjeneste eller fra udbyderen.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="9d0a9-114">Hvis eksperimentet ikke er aktiveret, kan brugere kun se standardversionen af siden (der vises ingen variationer).</span><span class="sxs-lookup"><span data-stu-id="9d0a9-114">If the experiment is not activated, users will only see the default version of the page (no variations will be displayed).</span></span>

<span data-ttu-id="9d0a9-115">Du skal holde eksperimentet kørende længe nok til at indsamle data til gyldige statistiske resultater.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="9d0a9-116">Brug tredjepartstjenesten til at overvåge de eksperimentrelaterede data og analyser, mens eksperimentet kører.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="9d0a9-117">Justere variationerne</span><span class="sxs-lookup"><span data-stu-id="9d0a9-117">Adjust your variations</span></span>
<span data-ttu-id="9d0a9-118">Hvis du af en eller anden grund har brug for at ændre dine variationer, skal du følge trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9d0a9-119">Hvis du foretager ændringer i et aktivt eksperiment i Commerce eller tredjepartstjenesten, kan resultaterne blive betydeligt påvirket.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="9d0a9-120">Du bør overveje at lade eksperimentet køre færdigt og derefter oprette et nyt eksperimenter med større ændringer.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="9d0a9-121">Vælg **Eksperimenter** i venstre navigationsrude af Commerce-webstedsgeneratoren, og vælg derefter eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-121">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
1. <span data-ttu-id="9d0a9-122">Vælg den variation, du vil opdatere, i rullemenuen.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="9d0a9-123">Foretag de nødvendige ændringer, og gennemse og publicer variationerne.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-123">Make any needed changes, and then preview and publish the variations.</span></span> <span data-ttu-id="9d0a9-124">Du kan finde flere oplysninger i [Gennemse og publicere et eksperiment](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="9d0a9-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="9d0a9-125">Gå til tredjepartstjenesten for at foretage eventuelle ændringer af eksperimentets opsætning.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="9d0a9-126">Forrige trin</span><span class="sxs-lookup"><span data-stu-id="9d0a9-126">Previous step</span></span>
[<span data-ttu-id="9d0a9-127">Gennemse og publicere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="9d0a9-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="9d0a9-128">Næste trin</span><span class="sxs-lookup"><span data-stu-id="9d0a9-128">Next step</span></span>
[<span data-ttu-id="9d0a9-129">Hæve en variation og fuldføre et eksperiment</span><span class="sxs-lookup"><span data-stu-id="9d0a9-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]