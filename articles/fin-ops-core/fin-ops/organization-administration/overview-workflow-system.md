---
title: Oversigt over arbejdsgangssystem
description: I dette emne beskrives arbejdsgangssystemet.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 660e01618eea66bc611dd51818694d36993ba9ea
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796990"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="ea614-103">Oversigt over arbejdsgangssystem</span><span class="sxs-lookup"><span data-stu-id="ea614-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea614-104">I dette emne beskrives arbejdsgangssystemet.</span><span class="sxs-lookup"><span data-stu-id="ea614-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="ea614-105">Hvad er en arbejdsgang?</span><span class="sxs-lookup"><span data-stu-id="ea614-105">What is workflow?</span></span>

<span data-ttu-id="ea614-106">Udtrykket *arbejdsgang* kan defineres på to måder: som et system og som en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="ea614-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="ea614-107">Arbejdsgang er et system</span><span class="sxs-lookup"><span data-stu-id="ea614-107">Workflow is a system</span></span>

<span data-ttu-id="ea614-108">Arbejdsgang er et system, der kører på applikationsobjektserveren (AOS).</span><span class="sxs-lookup"><span data-stu-id="ea614-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="ea614-109">Arbejdsgangssystemet indeholder funktioner, som du kan bruge til oprette individuelle arbejdsgange eller forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="ea614-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="ea614-110">Arbejdsgang er en forretningsproces</span><span class="sxs-lookup"><span data-stu-id="ea614-110">Workflow is a business process</span></span>

<span data-ttu-id="ea614-111">En arbejdsgang repræsenterer en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="ea614-111">A workflow represents a business process.</span></span> <span data-ttu-id="ea614-112">Den definerer, hvordan et dokument "flyder" eller bevæger sig gennem systemet, ved at vise, hvem der skal udføre en opgave, træffe en beslutning eller godkende et dokument.</span><span class="sxs-lookup"><span data-stu-id="ea614-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="ea614-113">I nedenstående illustration vises f.eks. en arbejdsgang for udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="ea614-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Arbejdsgang med elementer, der er tilknyttet brugere](./media/workflow_user.gif)

<span data-ttu-id="ea614-115">Hvis du bedre vil kunne forstå denne arbejdsgang, kan du antage, at Søren sender en udgiftsrapport for kr. 7.000.</span><span class="sxs-lookup"><span data-stu-id="ea614-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="ea614-116">I dette scenario skal Ivan gennemse de kvitteringer, som Søren har sendt til ham.</span><span class="sxs-lookup"><span data-stu-id="ea614-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="ea614-117">Henrik og Mette skal derefter godkende udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="ea614-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="ea614-118">Antag nu, at Søren sender en udgiftsrapport for kr. 11.000.</span><span class="sxs-lookup"><span data-stu-id="ea614-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="ea614-119">I dette scenario skal Ivan gennemse kvitteringerne, og Henrik, Mette og Dorthe skal godkende udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="ea614-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="ea614-120">Fordele ved at bruge arbejdsgangssystemet</span><span class="sxs-lookup"><span data-stu-id="ea614-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="ea614-121">Der er flere fordele ved at bruge arbejdsgangssystemet i organisationen:</span><span class="sxs-lookup"><span data-stu-id="ea614-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="ea614-122">**Ensartede processer** – Du kan definere, hvordan bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter, behandles.</span><span class="sxs-lookup"><span data-stu-id="ea614-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="ea614-123">Ved at bruge arbejdsgangssystemet kan du sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.</span><span class="sxs-lookup"><span data-stu-id="ea614-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="ea614-124">**Synliggørelse af processer** – Du kan spore status, historik og performanceværdier for arbejdsgangsforekomster.</span><span class="sxs-lookup"><span data-stu-id="ea614-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="ea614-125">Dette hjælper dig med at bestemme, om der skal foretages ændringer i arbejdsgangen for at forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="ea614-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="ea614-126">**Centraliseret arbejdsliste** – Brugerne kan få vist en centraliseret arbejdsliste, der viser opgaverne i arbejdsgangen og de godkendelser, der er knyttet til dem.</span><span class="sxs-lookup"><span data-stu-id="ea614-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="ea614-127">Indhold af arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="ea614-127">Workflow content</span></span>

+ [<span data-ttu-id="ea614-128">Arkitektur for arbejdsgangssystem</span><span class="sxs-lookup"><span data-stu-id="ea614-128">Workflow system architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="ea614-129">Arbejdsgangselementer</span><span class="sxs-lookup"><span data-stu-id="ea614-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="ea614-130">Handlinger i godkendelsesprocesser i arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="ea614-130">Actions in workflow approval processes</span></span>](workflow-actions.md)
+ [<span data-ttu-id="ea614-131">Oversigt over oprettelse af arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="ea614-131">Create workflows overview</span></span>](create-workflow.md)
+ [<span data-ttu-id="ea614-132">Konfigurere egenskaber for arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="ea614-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="ea614-133">Konfigurere manuelle opgave i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="ea614-133">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="ea614-134">Konfigurere automatiserede opgaver i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="ea614-134">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="ea614-135">Konfigurere godkendelsesprocesser i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="ea614-135">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="ea614-136">Konfigurere godkendelsestrin i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="ea614-136">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="ea614-137">Konfigurere manuelle beslutninger i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="ea614-137">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="ea614-138">Konfigurere betingede beslutninger i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="ea614-138">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="ea614-139">Konfigurere parallelle aktiviteter i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="ea614-139">Configure parallel activities in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="ea614-140">Konfigurere parallelle grene i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="ea614-140">Configure parallel branches in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="ea614-141">Konfigurere arbejdsgange for linjeelementer</span><span class="sxs-lookup"><span data-stu-id="ea614-141">Configure line-item workflows</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="ea614-142">Ofte stillede spørgsmål om arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="ea614-142">Workflow FAQ</span></span>](workflow-FAQ.md)
