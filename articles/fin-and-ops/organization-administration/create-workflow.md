---
title: Oprette en arbejdsgang
description: Dette emner beskriver, hvordan du opretter en arbejdsgang.
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3691379ea08ebebdad9e33359140d007d5d899dd
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="create-a-workflow"></a><span data-ttu-id="fb8b7-103">Oprette en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="fb8b7-103">Create a workflow</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="fb8b7-104">Dette emner beskriver, hvordan du opretter en arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-104">This topic explains how to create a workflow.</span></span>

<a name="open-the-workflow-editor"></a><span data-ttu-id="fb8b7-105">Åbne arbejdsgangseditoren</span><span class="sxs-lookup"><span data-stu-id="fb8b7-105">Open the workflow editor</span></span>
------------------------

<span data-ttu-id="fb8b7-106">Det Microsoft Dynamics 365 for Finance and Operations-modul, du arbejder i, bestemmer typerne af arbejdsgange, du kan oprette.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-106">The Microsoft Dynamics 365 for Finance and Operations module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="fb8b7-107">Udfør følgende trin for at vælge den type arbejdsgang, der skal oprettes, og for at åbne arbejdsgangseditoren.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1.  <span data-ttu-id="fb8b7-108">Åbn det modul, som du vil oprette en ny arbejdsgang for.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="fb8b7-109">For eksempel hvis du vil oprette en arbejdsgang for indkøbsrekvisitioner, skal du klikke på **Indkøb og forsyning**.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2.  <span data-ttu-id="fb8b7-110">Klik på **Konfigurer** &gt; **\[Arbejdsgange\] for modulnavn**.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3.  <span data-ttu-id="fb8b7-111">Klik på **Ny** i handlingsruden på listesiden.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4.  <span data-ttu-id="fb8b7-112">På siden **Opret arbejdsgang** skal du vælge typen af arbejdsgang, du vil oprette, og derefter klikke på **Opret arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="fb8b7-113">Arbejdsgangseditoren vises.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-113">The workflow editor appears.</span></span> <span data-ttu-id="fb8b7-114">Brug nu følgende procedurer til at designe arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="fb8b7-115">Trække arbejdsgangselementer over på lærredet</span><span class="sxs-lookup"><span data-stu-id="fb8b7-115">Drag workflow elements onto the canvas</span></span>
<span data-ttu-id="fb8b7-116">Området **Arbejdsgangselementer** i arbejdsgangseditoren indeholder de elementer, du kan føje til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="fb8b7-117">Du kan tilføje elementer i arbejdsgangen ved at trække dem til lærredet.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="fb8b7-118">Forbinde elementerne</span><span class="sxs-lookup"><span data-stu-id="fb8b7-118">Connect the elements</span></span>
<span data-ttu-id="fb8b7-119">Du kan forbinde et arbejdsgangselement med et andet ved at holde markøren over elementet, indtil der vises forbindelsespunkter.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="fb8b7-120">Klik på et forbindelsespunkt, og træk det til et andet element.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="fb8b7-121">Kontrollér, at alle elementerne forbindes.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="fb8b7-122">Konfigurere arbejdsgangens egenskaber</span><span class="sxs-lookup"><span data-stu-id="fb8b7-122">Configure the properties of the workflow</span></span>
<span data-ttu-id="fb8b7-123">Følg nedenstående trin for at konfigurere egenskaberne for arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-123">Follow these steps to configure the properties of the workflow.</span></span>

1.  <span data-ttu-id="fb8b7-124">Klik på lærredet for at sikre, at der ikke er markeret noget arbejdsgangselement.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2.  <span data-ttu-id="fb8b7-125">Klik på **Egenskaber** for at åbne siden **Egenskaber** for arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3.  <span data-ttu-id="fb8b7-126">Følg procedurerne i emnet [Konfigurere egenskaberne for en arbejdsgang](configure-workflow-properties.md).</span><span class="sxs-lookup"><span data-stu-id="fb8b7-126">Follow the procedures in the [Configure the properties of a workflow](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="fb8b7-127">Konfigurere arbejdsgangselementer</span><span class="sxs-lookup"><span data-stu-id="fb8b7-127">Configure the elements of the workflow</span></span>
<span data-ttu-id="fb8b7-128">Konfigurer hvert af de elementer, du har trukket over på lærredet.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="fb8b7-129">Du kan finde flere oplysninger om konfiguration af hvert enkelt arbejdsgangselement i følgende emner.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-129">For information about how to configure each workflow element, see the following topics:</span></span>

-   [<span data-ttu-id="fb8b7-130">Konfigurere en manuel opgave</span><span class="sxs-lookup"><span data-stu-id="fb8b7-130">Configure a manual task</span></span>](configure-manual-task-workflow.md)
-   [<span data-ttu-id="fb8b7-131">Konfigurere en automatiseret opgave</span><span class="sxs-lookup"><span data-stu-id="fb8b7-131">Configure an automated task</span></span>](configure-automated-task-workflow.md)
-   [<span data-ttu-id="fb8b7-132">Konfigurere en godkendelsesproces</span><span class="sxs-lookup"><span data-stu-id="fb8b7-132">Configure an approval process</span></span>](configure-approval-process-workflow.md)
-   [<span data-ttu-id="fb8b7-133">Konfigurere et godkendelsestrin</span><span class="sxs-lookup"><span data-stu-id="fb8b7-133">Configure an approval step</span></span>](configure-approval-step-workflow.md)
-   [<span data-ttu-id="fb8b7-134">Konfigurere en manuel beslutning</span><span class="sxs-lookup"><span data-stu-id="fb8b7-134">Configure a manual decision</span></span>](configure-manual-decision-workflow.md)
-   [<span data-ttu-id="fb8b7-135">Konfigurere en betinget beslutning</span><span class="sxs-lookup"><span data-stu-id="fb8b7-135">Configure a conditional decision</span></span>](configure-conditional-decision-workflow.md)
-   [<span data-ttu-id="fb8b7-136">Konfigurere en parallel aktivitet</span><span class="sxs-lookup"><span data-stu-id="fb8b7-136">Configure a parallel activity</span></span>](configure-parallel-activity-workflow.md)
-   [<span data-ttu-id="fb8b7-137">Konfigurere en parallel gren</span><span class="sxs-lookup"><span data-stu-id="fb8b7-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
-   [<span data-ttu-id="fb8b7-138">Konfigurere en arbejdsgang for linjeelement</span><span class="sxs-lookup"><span data-stu-id="fb8b7-138">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="fb8b7-139">Rette fejl eller afhjælpe advarsler</span><span class="sxs-lookup"><span data-stu-id="fb8b7-139">Resolve any errors or warnings</span></span>
<span data-ttu-id="fb8b7-140">I ruden **Fejl og advarsler** nederst i arbejdsgangseditoren vises meddelelser, der er genereret i forbindelse med arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="fb8b7-141">Du kan finde det element, hvor der er opstået en fejl eller advarsel, ved at dobbeltklikke på fejl- eller advarselsmeddelelsen.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="fb8b7-142">Alle fejl skal rettes og advarsler afhjælpes, før du kan aktivere arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="fb8b7-143">Gemme og aktivere arbejdsgangen</span><span class="sxs-lookup"><span data-stu-id="fb8b7-143">Save and activate the workflow</span></span>
<span data-ttu-id="fb8b7-144">Udfør følgende trin, når du er klar til at gemme og aktivere arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="fb8b7-145">Klik på **Gem og luk** for at lukke arbejdsgangseditoren og for at åbne siden **Gem arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2.  <span data-ttu-id="fb8b7-146">Angiv kommentarer om de ændringer, du har foretaget i arbejdsgangen, og klik derefter på **OK**.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3.  <span data-ttu-id="fb8b7-147">Hvis alle fejl og advarsler er løst, vises siden **Aktivér arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="fb8b7-148">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="fb8b7-148">Select one of the following options:</span></span>
    -   <span data-ttu-id="fb8b7-149">Hvis du vil aktivere denne version af arbejdsgangen, skal du klikke på **Aktivér den nye version**.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="fb8b7-150">Når en arbejdsgang er aktiv, kan brugerne sende dokumenter til behandling og godkendelse i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    -   <span data-ttu-id="fb8b7-151">Hvis du ikke vil aktivere denne version, skal du klikke på **Aktivér ikke den nye version**.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="fb8b7-152">Du kan aktivere arbejdsgangen senere.</span><span class="sxs-lookup"><span data-stu-id="fb8b7-152">You can activate the workflow later.</span></span>






