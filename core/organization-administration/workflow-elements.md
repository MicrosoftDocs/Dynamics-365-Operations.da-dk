---
title: Arbejdsgangselementer
description: "I denne artikel beskrives de forskellige elementer, der indgår i en arbejdsgang."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 5620a91ff9f300bed782170307a295ab79fc5b2e
ms.contentlocale: da-dk
ms.lasthandoff: 07/18/2017

---

# <a name="workflow-elements"></a><span data-ttu-id="34ad8-103">Arbejdsgangselementer</span><span class="sxs-lookup"><span data-stu-id="34ad8-103">Workflow elements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="34ad8-104">I denne artikel beskrives de forskellige elementer, der indgår i en arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="34ad8-104">This article describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="34ad8-105">En arbejdsgang består af elementer.</span><span class="sxs-lookup"><span data-stu-id="34ad8-105">A workflow consists of elements.</span></span> <span data-ttu-id="34ad8-106">Følgende afsnit indeholder beskrivelser af hver type element.</span><span class="sxs-lookup"><span data-stu-id="34ad8-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="34ad8-107">Opgaver</span><span class="sxs-lookup"><span data-stu-id="34ad8-107">Tasks</span></span>
<span data-ttu-id="34ad8-108">En *opgave* er en arbejdsenhed, der skal udføres.</span><span class="sxs-lookup"><span data-stu-id="34ad8-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="34ad8-109">To typer af opgaver kan føjes til en arbejdsgang: manuelle opgaver eller automatiserede opgaver.</span><span class="sxs-lookup"><span data-stu-id="34ad8-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="34ad8-110">Manuel opgave</span><span class="sxs-lookup"><span data-stu-id="34ad8-110">Manual task</span></span>

<span data-ttu-id="34ad8-111">En *manuel opgave* er en arbejdsenhed, der skal udføres af en bruger.</span><span class="sxs-lookup"><span data-stu-id="34ad8-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="34ad8-112">En arbejdsgang for en udgiftsrapport kan f.eks. have manuelle opgaver, der kræver, at de brugere, der har fået tildelt opgaven, skal udføre følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="34ad8-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

-   <span data-ttu-id="34ad8-113">Gennemgå de kvitteringer, der er indsendt sammen med en udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="34ad8-113">Review the receipts that are submitted together with an expense report.</span></span>
-   <span data-ttu-id="34ad8-114">Kontakte en medarbejders chef.</span><span class="sxs-lookup"><span data-stu-id="34ad8-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="34ad8-115">Automatiseret opgave</span><span class="sxs-lookup"><span data-stu-id="34ad8-115">Automated task</span></span>

<span data-ttu-id="34ad8-116">En *automatiseret opgave* er en arbejdsenhed, der skal udføres af systemet.</span><span class="sxs-lookup"><span data-stu-id="34ad8-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="34ad8-117">Der kræves ingen brugerindgriben.</span><span class="sxs-lookup"><span data-stu-id="34ad8-117">No human interaction is required.</span></span> <span data-ttu-id="34ad8-118">En arbejdsgang for en salgsordre kan f.eks. have automatiserede opgaver, der kræver, at systemet skal udføre følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="34ad8-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

-   <span data-ttu-id="34ad8-119">Udføre kreditkontrol.</span><span class="sxs-lookup"><span data-stu-id="34ad8-119">Perform a credit check.</span></span>
-   <span data-ttu-id="34ad8-120">Oprette en kundepost for kunden, hvis der ikke allerede findes en post.</span><span class="sxs-lookup"><span data-stu-id="34ad8-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="34ad8-121">Godkendelsesprocesser</span><span class="sxs-lookup"><span data-stu-id="34ad8-121">Approval processes</span></span>
<span data-ttu-id="34ad8-122">En *godkendelsesproces* er en proces, der består af separate trin.</span><span class="sxs-lookup"><span data-stu-id="34ad8-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="34ad8-123">På hvert enkelt godkendelsestrin kan brugeren udføre følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="34ad8-123">At each approval step, the user can perform the following actions:</span></span>

-   <span data-ttu-id="34ad8-124">Godkend dokumentet.</span><span class="sxs-lookup"><span data-stu-id="34ad8-124">Approve the document.</span></span>
-   <span data-ttu-id="34ad8-125">Afvis dokumentet.</span><span class="sxs-lookup"><span data-stu-id="34ad8-125">Reject the document.</span></span>
-   <span data-ttu-id="34ad8-126">Anmode om en ændring af dokumentet.</span><span class="sxs-lookup"><span data-stu-id="34ad8-126">Request a change to the document.</span></span>
-   <span data-ttu-id="34ad8-127">Tildele dokumentet til en anden bruger til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="34ad8-127">Assign the document to another user for approval.</span></span>

## <a name="lineitem-workflow-elements"></a><span data-ttu-id="34ad8-128">Elementer i arbejdsgang for linjeelement</span><span class="sxs-lookup"><span data-stu-id="34ad8-128">Lineitem workflow elements</span></span>
<span data-ttu-id="34ad8-129">En arbejdsgang kan oprettes for at behandle enten dokumenter eller linjeelementerne i et dokument.</span><span class="sxs-lookup"><span data-stu-id="34ad8-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="34ad8-130">Du har f.eks. oprettet en godkendelsesarbejdsgang for timesedler.</span><span class="sxs-lookup"><span data-stu-id="34ad8-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="34ad8-131">(Vi vil henvise til denne arbejdsproces som *dokumentarbejdsgangen*). Du kan tilføje en *arbejdsgang for linjeelement* til denne dokumentarbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="34ad8-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="34ad8-132">Når elementet i linjeelementet køres, sendes hvert linjeelement i dokumentet til behandling.</span><span class="sxs-lookup"><span data-stu-id="34ad8-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="34ad8-133">Det kan være, at du vil have alle linjeelementer behandlet af samme arbejdsgang for linjeelement, eller at du vil måske have hvert enkelt linjeelement behandlet af en særskilt arbejdsgang for linjeelement.</span><span class="sxs-lookup"><span data-stu-id="34ad8-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="34ad8-134">Antag, at en medarbejder har sendt en timeseddel, der ligner nedenstående figur.</span><span class="sxs-lookup"><span data-stu-id="34ad8-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span> <span data-ttu-id="34ad8-135">![Arbejdsgang med linjeelementer](./media/workflow_lineitemworkflow.gif) I dette scenario kan du muligvis oprette følgende arbejdsgange for linjeelementer:</span><span class="sxs-lookup"><span data-stu-id="34ad8-135">![Workflow with line items](./media/workflow_lineitemworkflow.gif) In this scenario, you might want to create the following line-item workflows:</span></span>

-   <span data-ttu-id="34ad8-136">**Arbejdsgang for linjeelement 1** – denne arbejdsgang bruges til at behandle linjeelementer, hvor projekt-id er 1111.</span><span class="sxs-lookup"><span data-stu-id="34ad8-136">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
-   <span data-ttu-id="34ad8-137">**Arbejdsgang for linjeelement 2** – denne arbejdsgang bruges til at behandle linjeelementer, hvor projekt-id er 2222.</span><span class="sxs-lookup"><span data-stu-id="34ad8-137">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
-   <span data-ttu-id="34ad8-138">**Arbejdsgang for linjeelement 3** – denne arbejdsgang bruges til at behandle linjeelementer, hvor projekt-id er 3333.</span><span class="sxs-lookup"><span data-stu-id="34ad8-138">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flowcontrol-elements"></a><span data-ttu-id="34ad8-139">Flowstyringselementer</span><span class="sxs-lookup"><span data-stu-id="34ad8-139">Flowcontrol elements</span></span>
<span data-ttu-id="34ad8-140">Følgende elementer sætter dig i stand til at designe arbejdsgange, der har alternative forgreninger eller grene, der kører samtidigt.</span><span class="sxs-lookup"><span data-stu-id="34ad8-140">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="34ad8-141">Manuel beslutning</span><span class="sxs-lookup"><span data-stu-id="34ad8-141">Manual decision</span></span>

<span data-ttu-id="34ad8-142">En *manuel beslutning* er et punkt, hvor en arbejdsgang deles i to grene.</span><span class="sxs-lookup"><span data-stu-id="34ad8-142">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="34ad8-143">En bruger skal træffe en beslutning, og med denne beslutning bestemmes det, hvilken gren der bliver brugt til behandling af det sendte dokument.</span><span class="sxs-lookup"><span data-stu-id="34ad8-143">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="34ad8-144">Betinget beslutning</span><span class="sxs-lookup"><span data-stu-id="34ad8-144">Conditional decision</span></span>

<span data-ttu-id="34ad8-145">En *betinget beslutning* er også et punkt, hvor en arbejdsgang deles i to grene.</span><span class="sxs-lookup"><span data-stu-id="34ad8-145">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="34ad8-146">Men systemet bestemmer, hvilken forgrening der bruges til at behandle det sendte dokument.</span><span class="sxs-lookup"><span data-stu-id="34ad8-146">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="34ad8-147">For at træffe denne beslutning evaluerer systemet dokumentet for at afgøre, om det opfylder de angivne betingelser.</span><span class="sxs-lookup"><span data-stu-id="34ad8-147">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="34ad8-148">Parallel aktivitet</span><span class="sxs-lookup"><span data-stu-id="34ad8-148">Parallel activity</span></span>

<span data-ttu-id="34ad8-149">En *parallel aktivitet* er et arbejdsgangselement, der omfatter to eller flere arbejdsgangsgrene, som kører samtidigt.</span><span class="sxs-lookup"><span data-stu-id="34ad8-149">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="34ad8-150">Underarbejdsgang</span><span class="sxs-lookup"><span data-stu-id="34ad8-150">Subworkflow</span></span>

<span data-ttu-id="34ad8-151">En *underarbejdsgang* er en arbejdsgang, der køres inden for rammerne af en anden arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="34ad8-151">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>




