---
title: "Indkøbs- og forsyningsarbejdsgange"
description: "I visse organisationer kræves det, at indkøbsrekvisitioner og indkøbsordrer skal godkendes af en anden bruger end den person, som har indtastet transaktionen. Du kan oprette en arbejdsgang for at oprette en godkendelsesproces."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: ce9bc42751cf0f537a0ddb5069aca7c9779a6bb1
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="69639-104">Indkøbs- og forsyningsarbejdsgange</span><span class="sxs-lookup"><span data-stu-id="69639-104">Procurement and sourcing workflows</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="69639-105">I visse organisationer kræves det, at indkøbsrekvisitioner og indkøbsordrer skal godkendes af en anden bruger end den person, som har indtastet transaktionen.</span><span class="sxs-lookup"><span data-stu-id="69639-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="69639-106">Du kan oprette en arbejdsgang for at oprette en godkendelsesproces.</span><span class="sxs-lookup"><span data-stu-id="69639-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="69639-107">En arbejdsgang repræsenterer en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="69639-107">A workflow represents a business process.</span></span> <span data-ttu-id="69639-108">Den definerer, hvordan et dokument "flyder" gennem systemet, og viser, hvem der skal udføre en opgave eller godkende et dokument.</span><span class="sxs-lookup"><span data-stu-id="69639-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="69639-109">Der er flere fordele ved at bruge arbejdsgangssystemet i organisationen:</span><span class="sxs-lookup"><span data-stu-id="69639-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="69639-110">**Ensartede processer** – Du kan bruge arbejdsgangssystemet til at definere godkendelsesprocessen for bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="69639-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="69639-111">Du kan bruge arbejdsgangssystemet som en hjælp til at sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.</span><span class="sxs-lookup"><span data-stu-id="69639-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="69639-112">**Synliggørelse af processer** – Du kan spore status, historik og performanceværdier for en bestemt arbejdsgangsforekomst.</span><span class="sxs-lookup"><span data-stu-id="69639-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="69639-113">Dette hjælper dig med at bestemme, om der skal foretages ændringer i arbejdsgangen for at forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="69639-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="69639-114">**Centraliseret arbejdsliste**– Brugerne kan få vist en centraliseret arbejdsliste for at få vist opgaverne i arbejdsgangen og godkendelser, der er tildelt til dem på tværs af alle arbejdsprocesser, som de deltager i.</span><span class="sxs-lookup"><span data-stu-id="69639-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="69639-115">Dette er tilgængeligt på siden Workflowopgaver.</span><span class="sxs-lookup"><span data-stu-id="69639-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="69639-116">De typer arbejdsgange, du kan oprette</span><span class="sxs-lookup"><span data-stu-id="69639-116">The types of workflows that you can create</span></span>
<span data-ttu-id="69639-117">Der er følgende tilgængelige arbejdsgangstyper for Indkøb og forsyning.</span><span class="sxs-lookup"><span data-stu-id="69639-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="69639-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="69639-118">**Type**</span></span>                         | <span data-ttu-id="69639-119">**Brug denne type til at**</span><span class="sxs-lookup"><span data-stu-id="69639-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="69639-120">Gennemgang af indkøbsrekvisition</span><span class="sxs-lookup"><span data-stu-id="69639-120">Purchase requisition review</span></span>      | <span data-ttu-id="69639-121">Oprette evaluerings- og godkendelsesarbejdsgange for indkøbsrekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="69639-121">Create review and approval workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="69639-122">Evaluering af indkøbsrekvisitionslinjer</span><span class="sxs-lookup"><span data-stu-id="69639-122">Purchase requisition line review</span></span> | <span data-ttu-id="69639-123">Oprette evaluerings- og godkendelsesarbejdsgange for indkøbsrekvisitionslinjer.</span><span class="sxs-lookup"><span data-stu-id="69639-123">Create review and approval workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="69639-124">Arbejdsgang for indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="69639-124">Purchase order workflow</span></span>          | <span data-ttu-id="69639-125">Opret evaluerings- og godkendelsesarbejdsgange for indkøbsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="69639-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="69639-126">Arbejdsgang for indkøbsordrelinje</span><span class="sxs-lookup"><span data-stu-id="69639-126">Purchase order line workflow</span></span>     | <span data-ttu-id="69639-127">Oprette evaluerings- og godkendelsesarbejdsgange for indkøbsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="69639-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="69639-128">Arbejdsgang for ansøgning om tilføjelse af kreditor</span><span class="sxs-lookup"><span data-stu-id="69639-128">Vendor add application workflow</span></span>  | <span data-ttu-id="69639-129">Oprette arbejdsgange for gennemsyn og godkendelse for at tilføje nye kreditorer via kreditoranmodninger.</span><span class="sxs-lookup"><span data-stu-id="69639-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="69639-130">Oprettelse af en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="69639-130">Creating a workflow</span></span>
<span data-ttu-id="69639-131">Hvis du vil oprette en arbejdsgang, skal du gå til Indkøb og forsyning &gt; Opsætning &gt; Indkøbs- og forsyningsarbejdsgange og oprette en ny arbejdsgang ved at vælge den type arbejdsgang, du vil oprette.</span><span class="sxs-lookup"><span data-stu-id="69639-131">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="69639-132">På lærredet for arbejdsgangen kan du trække arbejdsgangselementer til designeren og sammenkæde elementerne til en arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="69639-132">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="69639-133">Arbejdsgangselementerne bør være konfigureret.</span><span class="sxs-lookup"><span data-stu-id="69639-133">The workflow elements should be configured.</span></span> <span data-ttu-id="69639-134">Du kan konfigurere, hvilken deltager der bør træffe foranstaltninger, i forbindelse med arbejdsgangselementer af typerne godkendelse og opgave.</span><span class="sxs-lookup"><span data-stu-id="69639-134">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="69639-135">Deltagertyper</span><span class="sxs-lookup"><span data-stu-id="69639-135">Types of participants</span></span>
----------------------

<span data-ttu-id="69639-136">Du kan knytte et godkendelsestrin til følgende deltagergrupper.</span><span class="sxs-lookup"><span data-stu-id="69639-136">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="69639-137">Brugergruppe</span><span class="sxs-lookup"><span data-stu-id="69639-137">User group</span></span>    | <span data-ttu-id="69639-138">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="69639-138">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="69639-139">Deltager</span><span class="sxs-lookup"><span data-stu-id="69639-139">Participant</span></span>   | <span data-ttu-id="69639-140">Tildel godkendelsestrinnet til medlemmer af en gruppe eller en rolle.</span><span class="sxs-lookup"><span data-stu-id="69639-140">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="69639-141">Hierarki</span><span class="sxs-lookup"><span data-stu-id="69639-141">Hierarchy</span></span>     | <span data-ttu-id="69639-142">Tildel godkendelsestrinnet til brugere i et bestemt organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="69639-142">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="69639-143">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="69639-143">Workflow user</span></span> | <span data-ttu-id="69639-144">Tildel godkendelsestrinnet til brugere i denne arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="69639-144">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="69639-145">Kø</span><span class="sxs-lookup"><span data-stu-id="69639-145">Queue</span></span>         | <span data-ttu-id="69639-146">Tildel godkendelsestrinnet til en workflowopgavekø.</span><span class="sxs-lookup"><span data-stu-id="69639-146">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="69639-147">Bruger</span><span class="sxs-lookup"><span data-stu-id="69639-147">User</span></span>          | <span data-ttu-id="69639-148">Tildel godkendelsestrinnet til bestemte brugere.</span><span class="sxs-lookup"><span data-stu-id="69639-148">Assign the approval step to specific users.</span></span>                               |



<a name="see-also"></a><span data-ttu-id="69639-149">Se også</span><span class="sxs-lookup"><span data-stu-id="69639-149">See also</span></span>
--------

[<span data-ttu-id="69639-150">Definition af forretningsprocesarbejdsgange for indkøbsrekvisitioner</span><span class="sxs-lookup"><span data-stu-id="69639-150">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[<span data-ttu-id="69639-151">Arbejdsgang for indkøbsrekvisitioner</span><span class="sxs-lookup"><span data-stu-id="69639-151">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)

[<span data-ttu-id="69639-152">Onboarding af kreditorer</span><span class="sxs-lookup"><span data-stu-id="69639-152">Onboarding vendors</span></span>](vendor-onboarding.md)


