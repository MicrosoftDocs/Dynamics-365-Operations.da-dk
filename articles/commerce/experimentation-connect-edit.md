---
title: Tilslutte et eksperiment og redigere variationer
description: Dette emne indeholder en beskrivelse af, hvordan du kan oprette forbindelse fra et eksperiment i en tredjepartstjeneste til Dynamics 365 Commerce, og hvordan du redigerer variationer til eksperimentet.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 2a33897d01dd98d446c2fb49e417abd9db9f403a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010018"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="2aad5-103">Tilslutte et eksperiment og redigere variationer</span><span class="sxs-lookup"><span data-stu-id="2aad5-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="2aad5-104">Dette emne beskriver, hvordan du kan tilslutte dit eksperiment i Commerce og foretage ændringer i variationerne, så de stemmer overens med hypotesen.</span><span class="sxs-lookup"><span data-stu-id="2aad5-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so that they align with your hypothesis.</span></span> 

<span data-ttu-id="2aad5-105">I følgende diagram vises alle de trin, der er nødvendige for at konfigurere og køre et eksperiment på et e-handelswebsted i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2aad5-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="2aad5-106">Yderligere trin behandles i separate emner.</span><span class="sxs-lookup"><span data-stu-id="2aad5-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="2aad5-107">[ ![Eksperimenteringens brugerrejse - tilslutte og redigere](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="2aad5-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="2aad5-108">Når du har [konfigureret dit eksperiment](experimentation-setup.md) i en tredjepartstjeneste, skal du tilslutte eksperimentet i Dynamics 365 Commerce og redigere eksperimentets variationer.</span><span class="sxs-lookup"><span data-stu-id="2aad5-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="2aad5-109">Overvejelser om planlægning</span><span class="sxs-lookup"><span data-stu-id="2aad5-109">Planning considerations</span></span>

<span data-ttu-id="2aad5-110">Før du tilslutter dit eksperiment i Commerce, skal du træffe nogle beslutninger, der påvirker den måde, som Commerce administrerer dit indhold på.</span><span class="sxs-lookup"><span data-stu-id="2aad5-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="2aad5-111">Fastlægge omfanget af dit eksperiment</span><span class="sxs-lookup"><span data-stu-id="2aad5-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="2aad5-112">Når du tilslutter et eksperiment, bliver du bedt om at definere omfanget af eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="2aad5-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="2aad5-113">Eksperimenter defineres som et **delvist** omfang eller **helt** omfang.</span><span class="sxs-lookup"><span data-stu-id="2aad5-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="2aad5-114">Vælg **delvis**, hvis du vil gennemføre et eksperiment på en bestemt del af en side.</span><span class="sxs-lookup"><span data-stu-id="2aad5-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="2aad5-115">Hvis du vælger denne indstilling, skal du identificere, hvilke moduler der er inkluderet i eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="2aad5-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="2aad5-116">Ændringer, der foretages af dele af standardsiden eller-fragmentet, som ikke er relateret til eksperimentet, synkroniseres automatisk på tværs af variationer.</span><span class="sxs-lookup"><span data-stu-id="2aad5-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="2aad5-117">Vælg **hel**, hvis du vil gennemføre et eksperiment på en hel side eller et helt fragment.</span><span class="sxs-lookup"><span data-stu-id="2aad5-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="2aad5-118">Der oprettes separate kopier af standardsiden eller -fragmentet.</span><span class="sxs-lookup"><span data-stu-id="2aad5-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="2aad5-119">Du behøver ikke vælge, hvilke moduler der skal medtages i eksperimentet, fordi hele redigeringsoverfladen kan ændres.</span><span class="sxs-lookup"><span data-stu-id="2aad5-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="2aad5-120">Du kan tilføje, slette eller omarrangere moduler efter behov.</span><span class="sxs-lookup"><span data-stu-id="2aad5-120">You can add, delete, or re-order modules as needed.</span></span> <span data-ttu-id="2aad5-121">Hvis der foretages ændringer af den standardside eller det fragment, som eksperimentet er knyttet til, skal disse ændringer dog synkroniseres manuelt på tværs af alle variationer.</span><span class="sxs-lookup"><span data-stu-id="2aad5-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="2aad5-122">Hvis du knytter dit eksperiment til en side, der bruger et layout, kan du kun give eksperimentet et **helt** omfang.</span><span class="sxs-lookup"><span data-stu-id="2aad5-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="2aad5-123">Beslutte, om du vil planlægge, hvornår dit eksperiment skal publiceres</span><span class="sxs-lookup"><span data-stu-id="2aad5-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="2aad5-124">Hvis du vil planlægge, hvornår dit eksperiment bliver publiceret på dit live websted, skal du sørge for, at det indhold, du vil knytte til eksperimentet, er tilgængeligt i en publiceringsgruppe, *før* du tilslutter forsøget.</span><span class="sxs-lookup"><span data-stu-id="2aad5-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="2aad5-125">Du kan finde flere oplysninger om publiceringsgrupper under [Arbejde med publiceringsgrupper](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="2aad5-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="2aad5-126">Tilslutte dit eksperiment</span><span class="sxs-lookup"><span data-stu-id="2aad5-126">Connect your experiment</span></span>
<span data-ttu-id="2aad5-127">Hvis du vil tilslutte dit eksperiment, skal du starte guiden **Tilslut eksperiment**.</span><span class="sxs-lookup"><span data-stu-id="2aad5-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="2aad5-128">Guiden fører dig gennem de trin, der er nødvendige for at kunne tilslutte dit eksperiment.</span><span class="sxs-lookup"><span data-stu-id="2aad5-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="2aad5-129">Når du har fuldført guiden, er dit eksperiment tilsluttet, og variationer er oprettet og klar til at blive redigeret.</span><span class="sxs-lookup"><span data-stu-id="2aad5-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

<span data-ttu-id="2aad5-130">Benyt følgende fremgangsmåde for at komme i gang med at forbinde dit eksperimenter i Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="2aad5-130">To get started connecting your experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2aad5-131">Hvis du vil starte guiden **Tilslut eksperiment**, skal du vælge **Eksperimenter** i venstre navigationsrude og derefter vælge **Opret forbindelse**.</span><span class="sxs-lookup"><span data-stu-id="2aad5-131">To launch the **Connect experiment** wizard, select **Experiments** in the left navigation pane, and then select **Connect**.</span></span> <span data-ttu-id="2aad5-132">Du kan også få adgang til guiden fra en side- eller fragmenteditor ved at redigere den og vælge **Tilslut eksperiment** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="2aad5-132">Alternatively, you can access the wizard from a page or fragment editor by editing it and selecting **Connect experiment** on the command bar.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2aad5-133">En side kan kun tilsluttes ét eksperiment ad gangen.</span><span class="sxs-lookup"><span data-stu-id="2aad5-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="2aad5-134">Hvis du vil tilslutte en side i et andet eksperiment, skal du først slette det eksperiment, som siden er tilsluttet.</span><span class="sxs-lookup"><span data-stu-id="2aad5-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="2aad5-135">Vælg den side eller det fragment, du vil køre dit eksperiment på.</span><span class="sxs-lookup"><span data-stu-id="2aad5-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="2aad5-136">Indstil eksperimenterens omfang til **delvist** eller **helt**, afhængigt af hvad du har valgt i afsnittet [Fastlægge omfanget af dit eksperiment](#determine-the-scope-of-your-experiment) ovenfor.</span><span class="sxs-lookup"><span data-stu-id="2aad5-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="2aad5-137">Funktionsflaget **Eksperiment på sider eller fragmenter** skal være aktiveret, hvis du vil eksperimentere på en hel side eller et helt fragment.</span><span class="sxs-lookup"><span data-stu-id="2aad5-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="2aad5-138">Se [Eksperimenteren i Dynamics 365 Commerce](experimentation-overview.md) for at få flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="2aad5-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="2aad5-139">Vælg **Opret variationer, og afslut guiden** i det sidste trin af guiden.</span><span class="sxs-lookup"><span data-stu-id="2aad5-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="2aad5-140">Der oprettes variationer til eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="2aad5-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="2aad5-141">Redigere variationerne</span><span class="sxs-lookup"><span data-stu-id="2aad5-141">Edit your variations</span></span>
<span data-ttu-id="2aad5-142">Når du afslutter guiden, oprettes der variationer for dig.</span><span class="sxs-lookup"><span data-stu-id="2aad5-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="2aad5-143">Derefter skal du redigere variationerne, så de afspejler de valg, du skal bruge for at kunne kontrollere hypotesen i eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="2aad5-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="2aad5-144">Vælg en af følgende procedurer, der svarer til det omfang, du valgte til eksperimentet, i afsnittet [Fastlægge omfanget af dit eksperiment](#determine-the-scope-of-your-experiment) ovenfor.</span><span class="sxs-lookup"><span data-stu-id="2aad5-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="2aad5-145">Redigere variationer for eksperimenter med delvist omfang</span><span class="sxs-lookup"><span data-stu-id="2aad5-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="2aad5-146">Følg disse trin, hvis du har defineret omfanget af dit eksperimenter som **delvist** i guiden **Tilslut eksperiment**.</span><span class="sxs-lookup"><span data-stu-id="2aad5-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="2aad5-147">I editorvisning skal du bruge rullemenuen med variationer under kommandolinjen til at redigere de enkelte variationer baseret på din oprindelige hypotese.</span><span class="sxs-lookup"><span data-stu-id="2aad5-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="2aad5-148">Det kan også være en god ide at oprette en kontrol- eller basisvariation ved at lade en af variationerne være uændret.</span><span class="sxs-lookup"><span data-stu-id="2aad5-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="2aad5-149">Vælg det modul, der skal eksperimenteres på, vælg ellipse (...), og vælg derefter **Føj til eksperiment**.</span><span class="sxs-lookup"><span data-stu-id="2aad5-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="2aad5-150">Redigere variationer for eksperimenter med helt omfang</span><span class="sxs-lookup"><span data-stu-id="2aad5-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="2aad5-151">Hvis du har defineret eksperimentets omfang som **helt** i guiden **Tilslut eksperiment**, mens du er i editorvisning, skal du bruge rullemenuen med variationer under kommandolinjen til at redigere de enkelte variationer baseret på din oprindelige hypotese.</span><span class="sxs-lookup"><span data-stu-id="2aad5-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="2aad5-152">Det kan i begge tilfælde være en god ide at oprette en kontrol- eller basisvariation ved at lade en af variationerne være uændret.</span><span class="sxs-lookup"><span data-stu-id="2aad5-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="2aad5-153">Forrige trin</span><span class="sxs-lookup"><span data-stu-id="2aad5-153">Previous step</span></span>
[<span data-ttu-id="2aad5-154">Konfigurere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="2aad5-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="2aad5-155">Næste trin</span><span class="sxs-lookup"><span data-stu-id="2aad5-155">Next step</span></span>
[<span data-ttu-id="2aad5-156">Gennemse og publicere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="2aad5-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)
