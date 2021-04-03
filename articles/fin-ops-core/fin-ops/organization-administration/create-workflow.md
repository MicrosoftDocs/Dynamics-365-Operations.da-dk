---
title: Oversigt over oprettelse af arbejdsgange
description: Dette emner beskriver, hvordan du opretter en arbejdsgang.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: a64329780b96ca1e1675ced103c86c7cf0bc3754
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567384"
---
# <a name="create-workflows-overview"></a><span data-ttu-id="e2fca-103">Oversigt over oprettelse af arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="e2fca-103">Create workflows overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2fca-104">Dette emner beskriver, hvordan du opretter en arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="e2fca-104">This topic explains how to create a workflow.</span></span>

## <a name="open-the-workflow-editor"></a><span data-ttu-id="e2fca-105">Åbne arbejdsgangseditoren</span><span class="sxs-lookup"><span data-stu-id="e2fca-105">Open the workflow editor</span></span>

<span data-ttu-id="e2fca-106">De typer arbejdsgange, du kan oprette, afhænger af hvilket modul, du arbejder i.</span><span class="sxs-lookup"><span data-stu-id="e2fca-106">The module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="e2fca-107">Udfør følgende trin for at vælge den type arbejdsgang, der skal oprettes, og for at åbne arbejdsgangseditoren.</span><span class="sxs-lookup"><span data-stu-id="e2fca-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1. <span data-ttu-id="e2fca-108">Åbn det modul, som du vil oprette en ny arbejdsgang for.</span><span class="sxs-lookup"><span data-stu-id="e2fca-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="e2fca-109">For eksempel hvis du vil oprette en arbejdsgang for indkøbsrekvisitioner, skal du klikke på **Indkøb og forsyning**.</span><span class="sxs-lookup"><span data-stu-id="e2fca-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2. <span data-ttu-id="e2fca-110">Klik på **Konfigurer** &gt; **\[Arbejdsgange\] for modulnavn**.</span><span class="sxs-lookup"><span data-stu-id="e2fca-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3. <span data-ttu-id="e2fca-111">Klik på **Ny** i handlingsruden på listesiden.</span><span class="sxs-lookup"><span data-stu-id="e2fca-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4. <span data-ttu-id="e2fca-112">På siden **Opret arbejdsgang** skal du vælge typen af arbejdsgang, du vil oprette, og derefter klikke på **Opret arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="e2fca-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="e2fca-113">Arbejdsgangseditoren vises.</span><span class="sxs-lookup"><span data-stu-id="e2fca-113">The workflow editor appears.</span></span> <span data-ttu-id="e2fca-114">Brug nu følgende procedurer til at designe arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="e2fca-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="e2fca-115">Trække arbejdsgangselementer over på lærredet</span><span class="sxs-lookup"><span data-stu-id="e2fca-115">Drag workflow elements onto the canvas</span></span>

<span data-ttu-id="e2fca-116">Området **Arbejdsgangselementer** i arbejdsgangseditoren indeholder de elementer, du kan føje til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="e2fca-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="e2fca-117">Du kan tilføje elementer i arbejdsgangen ved at trække dem til lærredet.</span><span class="sxs-lookup"><span data-stu-id="e2fca-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="e2fca-118">Forbinde elementerne</span><span class="sxs-lookup"><span data-stu-id="e2fca-118">Connect the elements</span></span>

<span data-ttu-id="e2fca-119">Du kan forbinde et arbejdsgangselement med et andet ved at holde markøren over elementet, indtil der vises forbindelsespunkter.</span><span class="sxs-lookup"><span data-stu-id="e2fca-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="e2fca-120">Klik på et forbindelsespunkt, og træk det til et andet element.</span><span class="sxs-lookup"><span data-stu-id="e2fca-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="e2fca-121">Kontrollér, at alle elementerne forbindes.</span><span class="sxs-lookup"><span data-stu-id="e2fca-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="e2fca-122">Konfigurere arbejdsgangens egenskaber</span><span class="sxs-lookup"><span data-stu-id="e2fca-122">Configure the properties of the workflow</span></span>

<span data-ttu-id="e2fca-123">Følg nedenstående trin for at konfigurere egenskaberne for arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="e2fca-123">Follow these steps to configure the properties of the workflow.</span></span>

1. <span data-ttu-id="e2fca-124">Klik på lærredet for at sikre, at der ikke er markeret noget arbejdsgangselement.</span><span class="sxs-lookup"><span data-stu-id="e2fca-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2. <span data-ttu-id="e2fca-125">Klik på **Egenskaber** for at åbne siden **Egenskaber** for arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="e2fca-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3. <span data-ttu-id="e2fca-126">Følg procedurerne i emnet [Konfigurer egenskaberne for arbejdsgange](configure-workflow-properties.md).</span><span class="sxs-lookup"><span data-stu-id="e2fca-126">Follow the procedures in the [Configure workflow properties](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="e2fca-127">Konfigurere arbejdsgangselementer</span><span class="sxs-lookup"><span data-stu-id="e2fca-127">Configure the elements of the workflow</span></span>

<span data-ttu-id="e2fca-128">Konfigurer hvert af de elementer, du har trukket over på lærredet.</span><span class="sxs-lookup"><span data-stu-id="e2fca-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="e2fca-129">Du kan finde flere oplysninger om konfiguration af hvert enkelt arbejdsgangselement i følgende emner.</span><span class="sxs-lookup"><span data-stu-id="e2fca-129">For information about how to configure each workflow element, see the following topics:</span></span>

- [<span data-ttu-id="e2fca-130">Konfigurere manuelle opgave i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="e2fca-130">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
- [<span data-ttu-id="e2fca-131">Konfigurere automatiserede opgaver i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="e2fca-131">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
- [<span data-ttu-id="e2fca-132">Konfigurere godkendelsesprocesser i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="e2fca-132">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
- [<span data-ttu-id="e2fca-133">Konfigurere godkendelsestrin i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="e2fca-133">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
- [<span data-ttu-id="e2fca-134">Konfigurere manuelle beslutninger i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="e2fca-134">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
- [<span data-ttu-id="e2fca-135">Konfigurere betingede beslutninger i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="e2fca-135">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
- [<span data-ttu-id="e2fca-136">Konfigurere parallelle grene i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="e2fca-136">Configure parallel branches in a workflow</span></span>](configure-parallel-activity-workflow.md)
- [<span data-ttu-id="e2fca-137">Konfigurere en parallel gren</span><span class="sxs-lookup"><span data-stu-id="e2fca-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
- [<span data-ttu-id="e2fca-138">Konfigurere arbejdsgange for linjeelementer</span><span class="sxs-lookup"><span data-stu-id="e2fca-138">Configure line-item workflows</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="e2fca-139">Rette fejl eller afhjælpe advarsler</span><span class="sxs-lookup"><span data-stu-id="e2fca-139">Resolve any errors or warnings</span></span>

<span data-ttu-id="e2fca-140">I ruden **Fejl og advarsler** nederst i arbejdsgangseditoren vises meddelelser, der er genereret i forbindelse med arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="e2fca-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="e2fca-141">Du kan finde det element, hvor der er opstået en fejl eller advarsel, ved at dobbeltklikke på fejl- eller advarselsmeddelelsen.</span><span class="sxs-lookup"><span data-stu-id="e2fca-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="e2fca-142">Alle fejl skal rettes og advarsler afhjælpes, før du kan aktivere arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="e2fca-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="e2fca-143">Gemme og aktivere arbejdsgangen</span><span class="sxs-lookup"><span data-stu-id="e2fca-143">Save and activate the workflow</span></span>

<span data-ttu-id="e2fca-144">Udfør følgende trin, når du er klar til at gemme og aktivere arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="e2fca-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1. <span data-ttu-id="e2fca-145">Klik på **Gem og luk** for at lukke arbejdsgangseditoren og for at åbne siden **Gem arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="e2fca-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2. <span data-ttu-id="e2fca-146">Angiv kommentarer om de ændringer, du har foretaget i arbejdsgangen, og klik derefter på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2fca-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3. <span data-ttu-id="e2fca-147">Hvis alle fejl og advarsler er løst, vises siden **Aktivér arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="e2fca-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="e2fca-148">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="e2fca-148">Select one of the following options:</span></span>

    - <span data-ttu-id="e2fca-149">Hvis du vil aktivere denne version af arbejdsgangen, skal du klikke på **Aktivér den nye version**.</span><span class="sxs-lookup"><span data-stu-id="e2fca-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="e2fca-150">Når en arbejdsgang er aktiv, kan brugerne sende dokumenter til behandling og godkendelse i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="e2fca-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    - <span data-ttu-id="e2fca-151">Hvis du ikke vil aktivere denne version, skal du klikke på **Aktivér ikke den nye version**.</span><span class="sxs-lookup"><span data-stu-id="e2fca-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="e2fca-152">Du kan aktivere arbejdsgangen senere.</span><span class="sxs-lookup"><span data-stu-id="e2fca-152">You can activate the workflow later.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]