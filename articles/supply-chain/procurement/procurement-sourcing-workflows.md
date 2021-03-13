---
title: Indkøbs- og forsyningsarbejdsgange
description: I visse organisationer kræves det, at indkøbsrekvisitioner og indkøbsordrer skal godkendes af en anden bruger end den person, som har indtastet transaktionen. Du kan oprette en arbejdsgang for at oprette en godkendelsesproces.
author: RichardLuan
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: af614b7f29144d02a853ef15b008f2a21d3d3aa5
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019748"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="3253a-104">Indkøbs- og forsyningsarbejdsgange</span><span class="sxs-lookup"><span data-stu-id="3253a-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3253a-105">I visse organisationer kræves det, at indkøbsrekvisitioner og indkøbsordrer skal godkendes af en anden bruger end den person, som har indtastet transaktionen.</span><span class="sxs-lookup"><span data-stu-id="3253a-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="3253a-106">Du kan oprette en arbejdsgang for at oprette en godkendelsesproces.</span><span class="sxs-lookup"><span data-stu-id="3253a-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="3253a-107">En arbejdsgang repræsenterer en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="3253a-107">A workflow represents a business process.</span></span> <span data-ttu-id="3253a-108">Den definerer, hvordan et dokument "flyder" gennem systemet, og viser, hvem der skal udføre en opgave eller godkende et dokument.</span><span class="sxs-lookup"><span data-stu-id="3253a-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="3253a-109">Der er flere fordele ved at bruge arbejdsgangssystemet i organisationen:</span><span class="sxs-lookup"><span data-stu-id="3253a-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="3253a-110">**Ensartede processer** – Du kan bruge arbejdsgangssystemet til at definere godkendelsesprocessen for bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="3253a-110">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="3253a-111">Du kan bruge arbejdsgangssystemet som en hjælp til at sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.</span><span class="sxs-lookup"><span data-stu-id="3253a-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="3253a-112">**Synliggørelse af processer** – Du kan spore status, historik og performanceværdier for en bestemt arbejdsgangsforekomst.</span><span class="sxs-lookup"><span data-stu-id="3253a-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="3253a-113">Dette hjælper dig med at bestemme, om der skal foretages ændringer i arbejdsgangen for at forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="3253a-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="3253a-114">**Centraliseret arbejdsliste**– Brugerne kan få vist en centraliseret arbejdsliste for at få vist opgaverne i arbejdsgangen og godkendelser, der er tildelt til dem på tværs af alle arbejdsprocesser, som de deltager i.</span><span class="sxs-lookup"><span data-stu-id="3253a-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="3253a-115">Dette er tilgængeligt på siden Workflowopgaver.</span><span class="sxs-lookup"><span data-stu-id="3253a-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="3253a-116">De typer arbejdsgange, du kan oprette</span><span class="sxs-lookup"><span data-stu-id="3253a-116">The types of workflows that you can create</span></span>

<span data-ttu-id="3253a-117">Der er følgende tilgængelige arbejdsgangstyper for Indkøb og forsyning.</span><span class="sxs-lookup"><span data-stu-id="3253a-117">The following workflow types are available for Procurement and sourcing.</span></span>

| <span data-ttu-id="3253a-118">Type</span><span class="sxs-lookup"><span data-stu-id="3253a-118">Type</span></span> | <span data-ttu-id="3253a-119">Brug denne type til at</span><span class="sxs-lookup"><span data-stu-id="3253a-119">Use this type to</span></span> |
|---|---|
| <span data-ttu-id="3253a-120">Gennemgang af indkøbsrekvisition</span><span class="sxs-lookup"><span data-stu-id="3253a-120">Purchase requisition review</span></span> | <span data-ttu-id="3253a-121">Oprette evaluerings- og godkendelsesarbejdsgange for indkøbsrekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="3253a-121">Create review and approval workflows for purchase requisitions.</span></span> |
| <span data-ttu-id="3253a-122">Evaluering af indkøbsrekvisitionslinjer</span><span class="sxs-lookup"><span data-stu-id="3253a-122">Purchase requisition line review</span></span> | <span data-ttu-id="3253a-123">Oprette evaluerings- og godkendelsesarbejdsgange for indkøbsrekvisitionslinjer.</span><span class="sxs-lookup"><span data-stu-id="3253a-123">Create review and approval workflows for purchase requisition lines.</span></span> |
| <span data-ttu-id="3253a-124">Arbejdsgang for indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="3253a-124">Purchase order workflow</span></span> | <span data-ttu-id="3253a-125">Opret evaluerings- og godkendelsesarbejdsgange for indkøbsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="3253a-125">Create review and approval workflows for purchase orders.</span></span> |
| <span data-ttu-id="3253a-126">Arbejdsgang for indkøbsordrelinje</span><span class="sxs-lookup"><span data-stu-id="3253a-126">Purchase order line workflow</span></span> | <span data-ttu-id="3253a-127">Oprette evaluerings- og godkendelsesarbejdsgange for indkøbsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="3253a-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="3253a-128">Arbejdsgang for ansøgning om tilføjelse af kreditor</span><span class="sxs-lookup"><span data-stu-id="3253a-128">Vendor add application workflow</span></span> | <span data-ttu-id="3253a-129">Oprette arbejdsgange for gennemsyn og godkendelse for at tilføje nye kreditorer via kreditoranmodninger.</span><span class="sxs-lookup"><span data-stu-id="3253a-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="3253a-130">Når du tilføjer en ny arbejdsproces, kan du også se følgende forældede arbejdsprocesser, der er angivet i dialogboksen **Opret arbejdsproces**.</span><span class="sxs-lookup"><span data-stu-id="3253a-130">When you are adding a new workflow, you might also see the following obsolete workflows listed in the **Create workflow** dialog box.</span></span> <span data-ttu-id="3253a-131">Disse er relateret til den *bekræftelse af tilgang*-funktion, der var tilgængelig i [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), men som nu frarådes.</span><span class="sxs-lookup"><span data-stu-id="3253a-131">These are related to the *confirmation of receipt* functionality that was available in [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), but which has now been deprecated.</span></span> <span data-ttu-id="3253a-132">Disse arbejdsprocesser understøttes ikke i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="3253a-132">These workflows are currently unsupported.</span></span>
> 
> - <span data-ttu-id="3253a-133">Arbejdsgang for besked om dato for forfalden til levering</span><span class="sxs-lookup"><span data-stu-id="3253a-133">Delivery due date notification workflow</span></span>
> - <span data-ttu-id="3253a-134">Arbejdsgang for besked om modtaget faktura</span><span class="sxs-lookup"><span data-stu-id="3253a-134">Invoice received notification workflow</span></span>
> - <span data-ttu-id="3253a-135">Arbejdsgang for besked om, at produktkvitteringen mislykkedes</span><span class="sxs-lookup"><span data-stu-id="3253a-135">Product receipt failed notification workflow</span></span>
> - <span data-ttu-id="3253a-136">Arbejdsgang til besked om afvisning af ikke-bekræftet produktkvittering</span><span class="sxs-lookup"><span data-stu-id="3253a-136">Unconfirmed product receipt rejection notification workflow</span></span>

## <a name="creating-a-workflow"></a><span data-ttu-id="3253a-137">Oprettelse af en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="3253a-137">Creating a workflow</span></span>

<span data-ttu-id="3253a-138">Hvis du vil oprette en arbejdsgang, skal du gå til Indkøb og forsyning &gt; Opsætning &gt; Indkøbs- og forsyningsarbejdsgange og oprette en ny arbejdsgang ved at vælge den type arbejdsgang, du vil oprette.</span><span class="sxs-lookup"><span data-stu-id="3253a-138">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span> 

<span data-ttu-id="3253a-139">På lærredet for arbejdsgangen kan du trække arbejdsgangselementer til designeren og sammenkæde elementerne til en arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="3253a-139">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="3253a-140">Arbejdsgangselementerne bør være konfigureret.</span><span class="sxs-lookup"><span data-stu-id="3253a-140">The workflow elements should be configured.</span></span> <span data-ttu-id="3253a-141">Du kan konfigurere, hvilken deltager der bør træffe foranstaltninger, i forbindelse med arbejdsgangselementer af typerne godkendelse og opgave.</span><span class="sxs-lookup"><span data-stu-id="3253a-141">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="3253a-142">Deltagertyper</span><span class="sxs-lookup"><span data-stu-id="3253a-142">Types of participants</span></span>

<span data-ttu-id="3253a-143">Du kan knytte et godkendelsestrin til følgende deltagergrupper.</span><span class="sxs-lookup"><span data-stu-id="3253a-143">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="3253a-144">Brugergruppe</span><span class="sxs-lookup"><span data-stu-id="3253a-144">User group</span></span> | <span data-ttu-id="3253a-145">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="3253a-145">Description</span></span> |
|---|---|
| <span data-ttu-id="3253a-146">Deltager</span><span class="sxs-lookup"><span data-stu-id="3253a-146">Participant</span></span> | <span data-ttu-id="3253a-147">Tildel godkendelsestrinnet til medlemmer af en gruppe eller en rolle.</span><span class="sxs-lookup"><span data-stu-id="3253a-147">Assign the approval step to members of a group or role.</span></span> |
| <span data-ttu-id="3253a-148">Hierarki</span><span class="sxs-lookup"><span data-stu-id="3253a-148">Hierarchy</span></span> | <span data-ttu-id="3253a-149">Tildel godkendelsestrinnet til brugere i et bestemt organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="3253a-149">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="3253a-150">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="3253a-150">Workflow user</span></span> | <span data-ttu-id="3253a-151">Tildel godkendelsestrinnet til brugere i denne arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="3253a-151">Assign the approval step to users of this workflow.</span></span> |
| <span data-ttu-id="3253a-152">Kø</span><span class="sxs-lookup"><span data-stu-id="3253a-152">Queue</span></span> | <span data-ttu-id="3253a-153">Tildel godkendelsestrinnet til en workflowopgavekø.</span><span class="sxs-lookup"><span data-stu-id="3253a-153">Assign the approval step to a work item queue.</span></span> |
| <span data-ttu-id="3253a-154">Bruger</span><span class="sxs-lookup"><span data-stu-id="3253a-154">User</span></span> | <span data-ttu-id="3253a-155">Tildel godkendelsestrinnet til bestemte brugere.</span><span class="sxs-lookup"><span data-stu-id="3253a-155">Assign the approval step to specific users.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="3253a-156">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3253a-156">Additional resources</span></span>

- [<span data-ttu-id="3253a-157">Definition af forretningsprocesarbejdsgange for indkøbsrekvisitioner</span><span class="sxs-lookup"><span data-stu-id="3253a-157">Defining business process workflows for purchase requisitions</span></span>](https://www.microsoft.com/download/details.aspx?id=101821)
- [<span data-ttu-id="3253a-158">Arbejdsgang for indkøbsrekvisitioner</span><span class="sxs-lookup"><span data-stu-id="3253a-158">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)
- [<span data-ttu-id="3253a-159">Modtage kreditorer</span><span class="sxs-lookup"><span data-stu-id="3253a-159">Onboard vendors</span></span>](vendor-onboarding.md)
