---
title: Handlinger i godkendelsesprocesser i arbejdsgang
description: I denne artikel beskrives de handlinger, som hver deltager i godkendelsen af en arbejdsproces kan foretage.
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 829ee16b8fd72a0808a657419524487d9c1b3123
ms.contentlocale: da-dk
ms.lasthandoff: 12/18/2018

---

# <a name="actions-in-workflow-approval-processes"></a><span data-ttu-id="76b5e-103">Handlinger i godkendelsesprocesser i arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="76b5e-103">Actions in workflow approval processes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76b5e-104">I denne artikel beskrives de handlinger, som hver deltager i godkendelsen af en arbejdsproces kan foretage.</span><span class="sxs-lookup"><span data-stu-id="76b5e-104">This article explains the actions that each participant in a workflow approval process can take.</span></span>

<span data-ttu-id="76b5e-105">En arbejdsgang kan involvere flere persongrupper: igangsætteren, opgavemodtagere, beslutningstagere og godkendere.</span><span class="sxs-lookup"><span data-stu-id="76b5e-105">A workflow can involve several groups of people: the originator, task assignees, decision makers, and approvers.</span></span> <span data-ttu-id="76b5e-106">I arbejdsgangen for følgende udgiftsrapport er Søren igangsætter, medlemmerne af køen er opgavemodtagere, John er opgavemodtager og Henrik, Mette og Dorthe er godkendere.</span><span class="sxs-lookup"><span data-stu-id="76b5e-106">For example, in the following expense report workflow, Sam is the originator, the members of the queue are task assignees, John is a decision maker, and Frank, Sue, and Ann are approvers.</span></span>

<span data-ttu-id="76b5e-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span><span class="sxs-lookup"><span data-stu-id="76b5e-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span></span>

<span data-ttu-id="76b5e-108">Følgende afsnit indeholder beskrivelser af de arbejdsgangshandlinger, som hver gruppe kan udføre.</span><span class="sxs-lookup"><span data-stu-id="76b5e-108">The following sections explain the workflow actions that each group can perform.</span></span>

## <a name="actions-that-an-originator-can-perform"></a><span data-ttu-id="76b5e-109">Handlinger, som igangsætteren kan udføre</span><span class="sxs-lookup"><span data-stu-id="76b5e-109">Actions that an originator can perform</span></span>

<span data-ttu-id="76b5e-110">Igangsætteren starter en arbejdsgangsforekomst ved at sende et dokument til behandling.</span><span class="sxs-lookup"><span data-stu-id="76b5e-110">The originator starts a workflow instance by submitting a document for processing.</span></span> <span data-ttu-id="76b5e-111">Når Søren f.eks. vil sende sin udgiftsrapport, skal han klikke på knappen **Send** på siden **Udgiftsrapport**.</span><span class="sxs-lookup"><span data-stu-id="76b5e-111">For example, Sam must click the **Submit** button on the **Expense report** page to submit his expense report.</span></span>

## <a name="actions-that-a-task-assignee-can-perform"></a><span data-ttu-id="76b5e-112">Handlinger, som en opgavemodtager kan udføre</span><span class="sxs-lookup"><span data-stu-id="76b5e-112">Actions that a task assignee can perform</span></span>

<span data-ttu-id="76b5e-113">En opgave kan tildeles til flere personer eller til en workflowopgavekø, som overvåges af flere personer.</span><span class="sxs-lookup"><span data-stu-id="76b5e-113">A task can be assigned to multiple people or to a work item queue that is monitored by several people.</span></span> <span data-ttu-id="76b5e-114">Men en opgave kan kun fuldføres af én person.</span><span class="sxs-lookup"><span data-stu-id="76b5e-114">However, only one person can complete a task.</span></span> <span data-ttu-id="76b5e-115">Søren har f.eks. sendt en udgiftsrapport og har sendt sine kvitteringer til sin organisations udgiftsrapportafdeling til gennemsyn.</span><span class="sxs-lookup"><span data-stu-id="76b5e-115">For example, Sam has submitted an expense report and has routed his receipts to his organization's Expense Reports department for review.</span></span>

<span data-ttu-id="76b5e-116">Medlemmerne af udgiftsrapportafdelingen for Adventure Works overvåger køen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-116">The members of the Adventure Works Expense Reports department monitor the queue.</span></span> <span data-ttu-id="76b5e-117">Julie, der er medlem af denne afdeling, har accepteret opgaven med at gennemse Sørens udgiftsrapport og kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="76b5e-117">Julie, a member of that department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="76b5e-118">Hun kan nu udføre en af følgende handlinger: fuldføre, afvise, delegere, anmode om ændring, tildele eller frigive.</span><span class="sxs-lookup"><span data-stu-id="76b5e-118">She can now perform one of the following actions: complete, reject, delegate, request change, reassign, or release.</span></span>

> [!NOTE]
> <span data-ttu-id="76b5e-119">Det vil variere, hvilke handlinger der er tilgængelige, afhængigt af hvordan softwareudvikleren har designet opgaven.</span><span class="sxs-lookup"><span data-stu-id="76b5e-119">The actions that are available vary, depending on how the software developer designed the task.</span></span>

### <a name="complete"></a><span data-ttu-id="76b5e-120">Fuldføre</span><span class="sxs-lookup"><span data-stu-id="76b5e-120">Complete</span></span>

<span data-ttu-id="76b5e-121">Når en bruger fuldfører en opgave, tildeles det dokument, der blev sendt til behandling, til den næste bruger i arbejdsgangen, hvis der er en næste bruger.</span><span class="sxs-lookup"><span data-stu-id="76b5e-121">When a user completes a task, the document that was submitted for processing is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="76b5e-122">Hvis opgaven ikke skal behandles yderligere, afsluttes arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-122">If no additional processing is required, the workflow process ends.</span></span>

<span data-ttu-id="76b5e-123">For eksempel har Julie, der er medlem af udgiftsrapportafdelingen for Adventure Works, accepteret opgaven med at gennemse Sørens udgiftsrapport og kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="76b5e-123">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="76b5e-124">Når Julie har fuldført gennemsynet, tildeles John dokumentet til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="76b5e-124">After Julie completes her review, the document is assigned to John.</span></span>

### <a name="reject"></a><span data-ttu-id="76b5e-125">Afvis</span><span class="sxs-lookup"><span data-stu-id="76b5e-125">Reject</span></span>

<span data-ttu-id="76b5e-126">Når en bruger afviser et dokument, afsluttes arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-126">When a user rejects a document, the workflow process ends.</span></span>

<span data-ttu-id="76b5e-127">For eksempel har Julie, der er medlem af udgiftsrapportafdelingen for Adventure Works, accepteret opgaven med at gennemse Sørens udgiftsrapport og kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="76b5e-127">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="76b5e-128">Hvis Julie afviser udgiftsrapporten, afsluttes arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-128">If Julie rejects the expense report, the workflow process ends.</span></span>

<span data-ttu-id="76b5e-129">Søren kan derefter sende udgiftsrapporten igen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-129">Sam can then resubmit the expense report.</span></span> <span data-ttu-id="76b5e-130">Han kan foretage ændringer først, eller han kan sende den oprindelige version igen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-130">He can make changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="76b5e-131">Hvis Søren sender udgiftsrapporten igen, starter arbejdsgangsprocessen ved den manuelle gennemsynsopgave.</span><span class="sxs-lookup"><span data-stu-id="76b5e-131">If Sam resubmits the expense report, the workflow process starts at the manual review task.</span></span>

### <a name="delegate"></a><span data-ttu-id="76b5e-132">deleger</span><span class="sxs-lookup"><span data-stu-id="76b5e-132">Delegate</span></span>

<span data-ttu-id="76b5e-133">Når en bruger delegerer en opgave, tildeles opgaven til en anden bruger.</span><span class="sxs-lookup"><span data-stu-id="76b5e-133">When a user delegates a task, the task is assigned to another user.</span></span>

<span data-ttu-id="76b5e-134">For eksempel har Julie, der er medlem af udgiftsrapportafdelingen for Adventure Works, accepteret opgaven med at gennemse Sørens udgiftsrapport og kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="76b5e-134">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="76b5e-135">Julie delegerer denne opgaven til sin assistent, Tim.</span><span class="sxs-lookup"><span data-stu-id="76b5e-135">Julie delegates this task to Tim, who is her assistant.</span></span>

<span data-ttu-id="76b5e-136">Tim udfører derefter opgaven på vegne af Julie.</span><span class="sxs-lookup"><span data-stu-id="76b5e-136">Tim then acts on behalf of Julie.</span></span> <span data-ttu-id="76b5e-137">Når Tim derfor har fuldført gennemsynsopgaven, bliver udgiftsrapporten tildelt John til godkendelse – ligesom hvis Julie havde fuldført opgaven.</span><span class="sxs-lookup"><span data-stu-id="76b5e-137">Therefore, when Tim completes his review, the expense report is assigned to John, just as if Julie had completed the task.</span></span>

### <a name="request-change"></a><span data-ttu-id="76b5e-138">Anmode om ændring</span><span class="sxs-lookup"><span data-stu-id="76b5e-138">Request change</span></span>

<span data-ttu-id="76b5e-139">Når en bruger anmoder om en ændring af et dokument, der er sendt, sendes dokumentet tilbage til igangsætteren.</span><span class="sxs-lookup"><span data-stu-id="76b5e-139">When a user requests a change to a document that was submitted, the document is sent back to the originator.</span></span>

<span data-ttu-id="76b5e-140">For eksempel har Julie, der er medlem af udgiftsrapportafdelingen for Adventure Works, accepteret opgaven med at gennemse Sørens udgiftsrapport og kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="76b5e-140">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="76b5e-141">Julie bemærker nogle fejl i udgiftsrapporten og anmoder om at måtte foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="76b5e-141">Julie notices some errors on the expense report and requests changes.</span></span> <span data-ttu-id="76b5e-142">Udgiftsrapporten sendes tilbage til Søren.</span><span class="sxs-lookup"><span data-stu-id="76b5e-142">The expense report is sent back to Sam.</span></span>

<span data-ttu-id="76b5e-143">Søren kan sende udgiftsrapporten igen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-143">Sam can resubmit the expense report.</span></span> <span data-ttu-id="76b5e-144">Han kan foretage de ønskede ændringer først, eller han kan sende den oprindelige version igen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-144">He can make the requested changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="76b5e-145">Hvis Søren sender udgiftsrapporten igen, skal et medlem af workflowopgavekøen gennemse udgiftsrapporten og kvitteringerne igen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-145">If Sam resubmits the expense report, a member of the work item queue must review the expense report and the receipts again.</span></span>

### <a name="reassign"></a><span data-ttu-id="76b5e-146">Tildel igen</span><span class="sxs-lookup"><span data-stu-id="76b5e-146">Reassign</span></span>

<span data-ttu-id="76b5e-147">Medlemmerne af en workflowopgavekø kan tildele de dokumenter, som er i køen, igen til en anden kø.</span><span class="sxs-lookup"><span data-stu-id="76b5e-147">The members of a work item queue can reassign documents that are in that queue to another queue.</span></span>

<span data-ttu-id="76b5e-148">For eksempel overvåger Julie, der er medlem af udgiftsrapportafdelingen for Adventure Works, køen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-148">For example, Julie, a member of the Adventure Works Expense Reports department, is monitoring the queue.</span></span> <span data-ttu-id="76b5e-149">Hun kan udligne arbejdsbyrden ved igen at tildele udgiftsrapporten og de tilhørende kvitteringer til en anden kø.</span><span class="sxs-lookup"><span data-stu-id="76b5e-149">To help balance the workload, she can reassign the expense report, and the receipts that are included with it, to another queue.</span></span>

### <a name="release"></a><span data-ttu-id="76b5e-150">Udlevering</span><span class="sxs-lookup"><span data-stu-id="76b5e-150">Release</span></span>

<span data-ttu-id="76b5e-151">Et medlem af en workflowopgavekø kan undertiden acceptere en opgave, men derefter indse, at han eller hun ikke kan fuldføre opgaven.</span><span class="sxs-lookup"><span data-stu-id="76b5e-151">Occasionally, a member of a work item queue might accept a task, but then decide that he or she can't complete the task.</span></span> <span data-ttu-id="76b5e-152">I så fald kan den person, der har accepteret opgaven, frigive dokumentet tilbage til workflowopgavekøen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-152">In this case, the person who accepted the task can release the document back to the work item queue.</span></span>

<span data-ttu-id="76b5e-153">For eksempel har Julie, der er medlem af udgiftsrapportafdelingen for Adventure Works, accepteret opgaven med at gennemse Sørens udgiftsrapport og kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="76b5e-153">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="76b5e-154">Hvis Julie beslutter, at hun ikke kan fuldføre opgaven, kan hun frigive dokumentet.</span><span class="sxs-lookup"><span data-stu-id="76b5e-154">If Julie decides that she can't complete the task, she can release the document.</span></span> <span data-ttu-id="76b5e-155">Udgiftsrapporten returneres til køen, så andre medlemmer af udgiftsrapportafdelingen for Adventure Works kan fuldføre opgaven.</span><span class="sxs-lookup"><span data-stu-id="76b5e-155">The expense report is returned to the queue, so that other members of the Adventure Works Expense Reports department can complete the task.</span></span>

## <a name="actions-that-a-decision-maker-can-perform"></a><span data-ttu-id="76b5e-156">Handlinger, som en beslutningstager kan udføre</span><span class="sxs-lookup"><span data-stu-id="76b5e-156">Actions that a decision maker can perform</span></span>

<span data-ttu-id="76b5e-157">Når et dokument tildeles en beslutningstager, er det ofte fordi, der er et spørgsmål, som beslutningstageren skal besvare.</span><span class="sxs-lookup"><span data-stu-id="76b5e-157">Typically, a document is assigned to a decision maker, because there is a question that the decision maker must answer.</span></span> <span data-ttu-id="76b5e-158">Svaret på spørgsmålet er typisk **Ja** eller **Nej**, **Sand** eller **Falsk**.</span><span class="sxs-lookup"><span data-stu-id="76b5e-158">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="76b5e-159">Hvis beslutningstageren ikke vælger et af disse svar, kan han eller hun uddelegere beslutningen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-159">If the decision maker doesn't select one of those choices, he or she can delegate the decision.</span></span>

### <a name="choice-1-or-choice-2"></a><span data-ttu-id="76b5e-160">\[[Valg 1]\] eller \[[Valg 2]\]</span><span class="sxs-lookup"><span data-stu-id="76b5e-160">\[Choice 1\] or \[Choice 2\]</span></span>

<span data-ttu-id="76b5e-161">En beslutningstager skal besvare et spørgsmål, der har relation til dokumentet.</span><span class="sxs-lookup"><span data-stu-id="76b5e-161">A decision maker must answer a question that is related to the document.</span></span> <span data-ttu-id="76b5e-162">Svaret på spørgsmålet er typisk **Ja** eller **Nej**, **Sand** eller **Falsk**.</span><span class="sxs-lookup"><span data-stu-id="76b5e-162">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="76b5e-163">Det svar, beslutningstageren vælger, bestemmer, hvilken gren i arbejdsgangen der bliver brugt til behandling af dokumentet.</span><span class="sxs-lookup"><span data-stu-id="76b5e-163">The answer that the decision maker selects determines the workflow branch that is used to process the document.</span></span>

<span data-ttu-id="76b5e-164">For eksempel er Sørens udgiftsrapport tildelt til John.</span><span class="sxs-lookup"><span data-stu-id="76b5e-164">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="76b5e-165">John skal beslutte, om oplysningerne i dokumentet kræver et opkald til Sørens chef.</span><span class="sxs-lookup"><span data-stu-id="76b5e-165">John must decide whether the information in the document requires a call to Sam's manager.</span></span> <span data-ttu-id="76b5e-166">Hvis John beslutter, at et opkald er nødvendigt, tildeles udgiftsrapporten til Agnete, som derefter skal ringe til Sørens chef.</span><span class="sxs-lookup"><span data-stu-id="76b5e-166">If John decides that a call is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="76b5e-167">Hvis John beslutter, at et opkald ikke er nødvendigt, tildeles udgiftsrapporten til Henrik til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="76b5e-167">If John decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

### <a name="delegate"></a><span data-ttu-id="76b5e-168">Delegere</span><span class="sxs-lookup"><span data-stu-id="76b5e-168">Delegate</span></span>

<span data-ttu-id="76b5e-169">Når en beslutningstager uddelegerer en beslutning, tildeles dokumentet til en anden bruger, som skal træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-169">When a decision maker delegates a decision, the document is assigned to another user who must make the decision.</span></span>

<span data-ttu-id="76b5e-170">For eksempel er Sørens udgiftsrapport tildelt til John.</span><span class="sxs-lookup"><span data-stu-id="76b5e-170">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="76b5e-171">John uddelegerer beslutningen til sin assistent, Maria.</span><span class="sxs-lookup"><span data-stu-id="76b5e-171">John delegates the decision to Maria, who is his assistant.</span></span>

<span data-ttu-id="76b5e-172">Maria udfører derefter opgaven på vegne af John.</span><span class="sxs-lookup"><span data-stu-id="76b5e-172">Maria then acts on behalf of John.</span></span> <span data-ttu-id="76b5e-173">Hvis Maria beslutter, at et opkald til Sørens chef er nødvendigt, tildeles udgiftsrapporten til Agnete, som derefter skal ringe til Sørens chef.</span><span class="sxs-lookup"><span data-stu-id="76b5e-173">If Maria decides that a call to Sam's manager is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="76b5e-174">Hvis Maria beslutter, at et opkald ikke er nødvendigt, tildeles udgiftsrapporten til Henrik til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="76b5e-174">If Maria decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

## <a name="actions-that-an-approver-can-perform"></a><span data-ttu-id="76b5e-175">Handlinger, som godkenderen kan udføre</span><span class="sxs-lookup"><span data-stu-id="76b5e-175">Actions that an approver can perform</span></span>

<span data-ttu-id="76b5e-176">Når et dokument er tildelt en godkender, kan godkenderen udføre en af følgende handlinger: godkende, afvise, delegere eller anmode om ændring.</span><span class="sxs-lookup"><span data-stu-id="76b5e-176">When a document is assigned to an approver, the approver can perform one of the following actions: approve, reject, delegate, or request change.</span></span>

### <a name="approve"></a><span data-ttu-id="76b5e-177">Godkende</span><span class="sxs-lookup"><span data-stu-id="76b5e-177">Approve</span></span>

<span data-ttu-id="76b5e-178">Når en godkender har godkendt et dokument, tildeles dokumentet til den næste bruger i arbejdsgangen, hvis der er en næste bruger.</span><span class="sxs-lookup"><span data-stu-id="76b5e-178">When an approver approves a document, the document is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="76b5e-179">Hvis opgaven ikke skal behandles yderligere, afsluttes arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-179">If no additional processing is required, the workflow process ends.</span></span>

<span data-ttu-id="76b5e-180">For eksempel har Søren sendt en udgiftsrapport på kr. 6.000, og dette dokument er tildelt til Henrik.</span><span class="sxs-lookup"><span data-stu-id="76b5e-180">For example, Sam has submitted an expense report for USD 6,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="76b5e-181">Hvis Henrik godkender dokumentet, tildeles det til Mette til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="76b5e-181">When Frank approves the document, it's assigned to Sue for approval.</span></span> <span data-ttu-id="76b5e-182">Når Mette har godkendt udgiftsrapporten, er arbejdsgangsprocessen afsluttet.</span><span class="sxs-lookup"><span data-stu-id="76b5e-182">When Sue approves the expense report, the workflow process ends.</span></span>

### <a name="reject"></a><span data-ttu-id="76b5e-183">Afvis</span><span class="sxs-lookup"><span data-stu-id="76b5e-183">Reject</span></span>

<span data-ttu-id="76b5e-184">Når en godkender afviser et dokument, afsluttes arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-184">When an approver rejects a document, the workflow process ends.</span></span>

<span data-ttu-id="76b5e-185">For eksempel har Søren sendt en udgiftsrapport på kr. 12.000, og dette dokument er tildelt til Mette.</span><span class="sxs-lookup"><span data-stu-id="76b5e-185">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="76b5e-186">Hvis Mette afviser udgiftsrapporten, afsluttes arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-186">If Sue rejects the expense report, the workflow process ends.</span></span>

<span data-ttu-id="76b5e-187">Søren kan sende udgiftsrapporten igen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-187">Sam can resubmit the expense report.</span></span> <span data-ttu-id="76b5e-188">Han kan udføre ændringerne først, eller han kan sende den oprindelige version af udgiftsrapporten igen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-188">He can make changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="76b5e-189">Hvis Søren sender udgiftsrapporten igen, starter arbejdsgangsprocessen ved godkendelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-189">If Sam resubmits the expense report, the workflow process starts at the approval process.</span></span>

### <a name="delegate"></a><span data-ttu-id="76b5e-190">Delegere</span><span class="sxs-lookup"><span data-stu-id="76b5e-190">Delegate</span></span>

<span data-ttu-id="76b5e-191">Når en godkender delegerer et dokument, tildeles dokumentet til en anden bruger til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="76b5e-191">When an approver delegates a document, the document is assigned to another user for approval.</span></span>

<span data-ttu-id="76b5e-192">For eksempel har Søren sendt en udgiftsrapport på kr. 12.000, og dette dokument er tildelt til Henrik.</span><span class="sxs-lookup"><span data-stu-id="76b5e-192">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="76b5e-193">Henrik delegerer udgiftsrapporten til Dorthe.</span><span class="sxs-lookup"><span data-stu-id="76b5e-193">Frank delegates the expense report to Ann.</span></span>

<span data-ttu-id="76b5e-194">Dorthe udfører derefter opgaven på vegne af Henrik.</span><span class="sxs-lookup"><span data-stu-id="76b5e-194">Ann then acts on behalf of Frank.</span></span> <span data-ttu-id="76b5e-195">Når Dorthe derfor godkender dokumentet, tildeles det til Mette til godkendelse – ligesom hvis Henrik havde godkendt det.</span><span class="sxs-lookup"><span data-stu-id="76b5e-195">Therefore, when Ann approves the document, it's assigned to Sue for approval, just as if Frank had approved it.</span></span> <span data-ttu-id="76b5e-196">Når Mette har godkendt dokumentet, sendes det til Dorthe til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="76b5e-196">After Sue approves the document, it's sent to Ann for approval.</span></span>

### <a name="request-change"></a><span data-ttu-id="76b5e-197">Anmod om ændring</span><span class="sxs-lookup"><span data-stu-id="76b5e-197">Request change</span></span>

<span data-ttu-id="76b5e-198">Når en godkender anmoder om en ændring i et dokument, sendes dokumentet tilbage til igangsætteren.</span><span class="sxs-lookup"><span data-stu-id="76b5e-198">When an approver requests a change to a document, the document is sent back to the originator.</span></span>

<span data-ttu-id="76b5e-199">For eksempel har Søren sendt en udgiftsrapport på kr. 12.000, og dette dokument er tildelt til Mette.</span><span class="sxs-lookup"><span data-stu-id="76b5e-199">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="76b5e-200">Hvis Mette anmoder om en ændring, sendes dokumentet tilbage til Søren.</span><span class="sxs-lookup"><span data-stu-id="76b5e-200">If Sue requests a change, the expense report is sent back to Sam.</span></span>

<span data-ttu-id="76b5e-201">Søren kan sende udgiftsrapporten igen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-201">Sam can resubmit the expense report.</span></span> <span data-ttu-id="76b5e-202">Han kan udføre de ønskede ændringer først, eller han kan sende den oprindelige version af udgiftsrapporten igen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-202">He can make the requested changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="76b5e-203">Hvis Søren sender udgiftsrapporten igen, sendes den til Henrik til godkendelse, fordi Henrik er den første godkender i godkendelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="76b5e-203">If Sam resubmits the expense report, it's sent to Frank for approval, because Frank is the first approver in the approval process.</span></span>

