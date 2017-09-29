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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 80853a06e599786e2dcaf049ac733c47dfe4d9a5
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="842e8-104">Indkøbs- og forsyningsarbejdsgange</span><span class="sxs-lookup"><span data-stu-id="842e8-104">Procurement and sourcing workflows</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="842e8-105">I visse organisationer kræves det, at indkøbsrekvisitioner og indkøbsordrer skal godkendes af en anden bruger end den person, som har indtastet transaktionen.</span><span class="sxs-lookup"><span data-stu-id="842e8-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="842e8-106">Du kan oprette en arbejdsgang for at oprette en godkendelsesproces.</span><span class="sxs-lookup"><span data-stu-id="842e8-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="842e8-107">En arbejdsgang repræsenterer en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="842e8-107">A workflow represents a business process.</span></span> <span data-ttu-id="842e8-108">Den definerer, hvordan et dokument "flyder" gennem systemet, og viser, hvem der skal udføre en opgave eller godkende et dokument.</span><span class="sxs-lookup"><span data-stu-id="842e8-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="842e8-109">Der er flere fordele ved at bruge arbejdsgangssystemet i organisationen:</span><span class="sxs-lookup"><span data-stu-id="842e8-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="842e8-110">**Ensartede processer** – Du kan bruge arbejdsgangssystemet til at definere godkendelsesprocessen for bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="842e8-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="842e8-111">Du kan bruge arbejdsgangssystemet som en hjælp til at sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.</span><span class="sxs-lookup"><span data-stu-id="842e8-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="842e8-112">**Synliggørelse af processer** – Du kan spore status, historik og performanceværdier for en bestemt arbejdsgangsforekomst.</span><span class="sxs-lookup"><span data-stu-id="842e8-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="842e8-113">Dette hjælper dig med at bestemme, om der skal foretages ændringer i arbejdsgangen for at forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="842e8-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="842e8-114">**Centraliseret arbejdsliste**– Brugerne kan få vist en centraliseret arbejdsliste for at få vist opgaverne i arbejdsgangen og godkendelser, der er tildelt til dem på tværs af alle arbejdsprocesser, som de deltager i.</span><span class="sxs-lookup"><span data-stu-id="842e8-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="842e8-115">Dette er tilgængeligt på siden Workflowopgaver.</span><span class="sxs-lookup"><span data-stu-id="842e8-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="842e8-116"> De typer arbejdsgange, du kan oprette</span><span class="sxs-lookup"><span data-stu-id="842e8-116">The types of workflows that you can create</span></span>
<span data-ttu-id="842e8-117">Der er følgende tilgængelige arbejdsgangstyper for Indkøb og forsyning.</span><span class="sxs-lookup"><span data-stu-id="842e8-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="842e8-118">**Skriv**</span><span class="sxs-lookup"><span data-stu-id="842e8-118">**Type**</span></span>                         | <span data-ttu-id="842e8-119">**Brug denne type til at**</span><span class="sxs-lookup"><span data-stu-id="842e8-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="842e8-120">Gennemgang af indkøbsrekvisition</span><span class="sxs-lookup"><span data-stu-id="842e8-120">Purchase requisition review</span></span>      | <span data-ttu-id="842e8-121">Oprette evalueringsarbejdsgange for indkøbsrekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="842e8-121">Create review workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="842e8-122">Evaluering af indkøbsrekvisitionslinjer</span><span class="sxs-lookup"><span data-stu-id="842e8-122">Purchase requisition line review</span></span> | <span data-ttu-id="842e8-123">Oprette evalueringsarbejdsgange for indkøbsrekvisitionslinjer.</span><span class="sxs-lookup"><span data-stu-id="842e8-123">Create review workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="842e8-124">Arbejdsgang for indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="842e8-124">Purchase order workflow</span></span>          | <span data-ttu-id="842e8-125">Opret evaluerings- og godkendelsesarbejdsgange for indkøbsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="842e8-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="842e8-126">Arbejdsgang for indkøbsordrelinje</span><span class="sxs-lookup"><span data-stu-id="842e8-126">Purchase order line workflow</span></span>     | <span data-ttu-id="842e8-127">Oprette evaluerings- og godkendelsesarbejdsgange for indkøbsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="842e8-127">Create review and approve workflows for purchase order lines.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="842e8-128">Oprettelse af en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="842e8-128">Creating a workflow</span></span>
<span data-ttu-id="842e8-129">Hvis du vil oprette en arbejdsgang, skal du gå til Indkøb og forsyning &gt; Opsætning &gt; Indkøbs- og forsyningsarbejdsgange og oprette en ny arbejdsgang ved at vælge den type arbejdsgang, du vil oprette.</span><span class="sxs-lookup"><span data-stu-id="842e8-129">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="842e8-130">På lærredet for arbejdsgangen kan du trække arbejdsgangselementer til designeren og sammenkæde elementerne til en arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="842e8-130">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="842e8-131">Arbejdsgangselementerne bør være konfigureret.</span><span class="sxs-lookup"><span data-stu-id="842e8-131">The workflow elements should be configured.</span></span> <span data-ttu-id="842e8-132">Du kan konfigurere, hvilken deltager der bør træffe foranstaltninger, i forbindelse med arbejdsgangselementer af typerne godkendelse og opgave.</span><span class="sxs-lookup"><span data-stu-id="842e8-132">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="842e8-133">Deltagertyper</span><span class="sxs-lookup"><span data-stu-id="842e8-133">Types of participants</span></span>
----------------------

<span data-ttu-id="842e8-134">Du kan knytte et godkendelsestrin til følgende deltagergrupper.</span><span class="sxs-lookup"><span data-stu-id="842e8-134">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="842e8-135">Brugergruppe</span><span class="sxs-lookup"><span data-stu-id="842e8-135">User group</span></span>    | <span data-ttu-id="842e8-136">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="842e8-136">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="842e8-137">Deltager</span><span class="sxs-lookup"><span data-stu-id="842e8-137">Participant</span></span>   | <span data-ttu-id="842e8-138">Tildel godkendelsestrinnet til medlemmer af en gruppe eller en rolle.</span><span class="sxs-lookup"><span data-stu-id="842e8-138">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="842e8-139">Hierarki</span><span class="sxs-lookup"><span data-stu-id="842e8-139">Hierarchy</span></span>     | <span data-ttu-id="842e8-140">Tildel godkendelsestrinnet til brugere i et bestemt organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="842e8-140">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="842e8-141">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="842e8-141">Workflow user</span></span> | <span data-ttu-id="842e8-142">Tildel godkendelsestrinnet til brugere i denne arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="842e8-142">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="842e8-143">Kø</span><span class="sxs-lookup"><span data-stu-id="842e8-143">Queue</span></span>         | <span data-ttu-id="842e8-144">Tildel godkendelsestrinnet til en workflowopgavekø.</span><span class="sxs-lookup"><span data-stu-id="842e8-144">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="842e8-145">Bruger</span><span class="sxs-lookup"><span data-stu-id="842e8-145">User</span></span>          | <span data-ttu-id="842e8-146">Tildel godkendelsestrinnet til bestemte brugere.</span><span class="sxs-lookup"><span data-stu-id="842e8-146">Assign the approval step to specific users.</span></span>                               |



<a name="see-also"></a><span data-ttu-id="842e8-147">Se også</span><span class="sxs-lookup"><span data-stu-id="842e8-147">See also</span></span>
--------

[<span data-ttu-id="842e8-148">Definition af forretningsprocesarbejdsgange for indkøbsrekvisitioner</span><span class="sxs-lookup"><span data-stu-id="842e8-148">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[<span data-ttu-id="842e8-149">Arbejdsgang for indkøbsrekvisitioner</span><span class="sxs-lookup"><span data-stu-id="842e8-149">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)




