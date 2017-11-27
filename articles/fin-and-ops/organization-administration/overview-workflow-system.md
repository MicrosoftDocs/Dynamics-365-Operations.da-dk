---
title: Oversigt over arbejdsgang
description: I dette emne beskrives arbejdsgangsystemet i Microsoft Dynamics 365 for Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f4e2167290618aaf6ad144e7db8274514078388b
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="workflow-overview"></a><span data-ttu-id="300c8-103">Oversigt over arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="300c8-103">Workflow overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="300c8-104">I dette emne beskrives arbejdsgangsystemet i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="300c8-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="what-is-workflow"></a><span data-ttu-id="300c8-105">Hvad er en arbejdsgang?</span><span class="sxs-lookup"><span data-stu-id="300c8-105">What is workflow?</span></span>
-----------------

<span data-ttu-id="300c8-106">Udtrykket *arbejdsgang* kan defineres på to måder: som et system og som en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="300c8-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>
### <a name="workflow-is-a-system"></a><span data-ttu-id="300c8-107">Arbejdsgang er et system</span><span class="sxs-lookup"><span data-stu-id="300c8-107">Workflow is a system</span></span>

<span data-ttu-id="300c8-108">Arbejdsgang er et system, som installeres med Finance and Operations, og som kører i AOS (applikationsobjektserveren).</span><span class="sxs-lookup"><span data-stu-id="300c8-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="300c8-109">Arbejdsgangssystemet indeholder funktioner, som du kan bruge til oprette individuelle arbejdsgange eller forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="300c8-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="300c8-110">Arbejdsgang er en forretningsproces</span><span class="sxs-lookup"><span data-stu-id="300c8-110">Workflow is a business process</span></span>

<span data-ttu-id="300c8-111">En arbejdsgang repræsenterer en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="300c8-111">A workflow represents a business process.</span></span> <span data-ttu-id="300c8-112">Den definerer, hvordan et dokument "flyder" eller bevæger sig gennem systemet, ved at vise, hvem der skal udføre en opgave, træffe en beslutning eller godkende et dokument.</span><span class="sxs-lookup"><span data-stu-id="300c8-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="300c8-113">I nedenstående illustration vises f.eks. en arbejdsgang for udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="300c8-113">For example, the following illustration shows a workflow for expense reports.</span></span> 

![Arbejdsgang med elementer, der er tilknyttet brugere](./media/workflow_user.gif) 

<span data-ttu-id="300c8-115">Hvis du bedre vil kunne forstå denne arbejdsgang, kan du antage, at Søren sender en udgiftsrapport for kr. 7.000.</span><span class="sxs-lookup"><span data-stu-id="300c8-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="300c8-116">I dette scenario skal Ivan gennemse de kvitteringer, som Søren har sendt til ham.</span><span class="sxs-lookup"><span data-stu-id="300c8-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="300c8-117">Henrik og Mette skal derefter godkende udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="300c8-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="300c8-118">Antag nu, at Søren sender en udgiftsrapport for kr. 11.000.</span><span class="sxs-lookup"><span data-stu-id="300c8-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="300c8-119">I dette scenario skal Ivan gennemse kvitteringerne, og Henrik, Mette og Dorthe skal godkende udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="300c8-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="300c8-120">Fordele ved at bruge arbejdsgangssystemet</span><span class="sxs-lookup"><span data-stu-id="300c8-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="300c8-121">Der er flere fordele ved at bruge arbejdsgangssystemet i organisationen:</span><span class="sxs-lookup"><span data-stu-id="300c8-121">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="300c8-122">**Ensartede processer** – Du kan definere, hvordan bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter, behandles.</span><span class="sxs-lookup"><span data-stu-id="300c8-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="300c8-123">Ved at bruge arbejdsgangssystemet kan du sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.</span><span class="sxs-lookup"><span data-stu-id="300c8-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="300c8-124">**Synliggørelse af processer** – Du kan spore status, historik og performanceværdier for arbejdsgangsforekomster.</span><span class="sxs-lookup"><span data-stu-id="300c8-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="300c8-125">Dette hjælper dig med at bestemme, om der skal foretages ændringer i arbejdsgangen for at forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="300c8-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="300c8-126">**Centraliseret arbejdsliste** – Brugerne kan få vist en centraliseret arbejdsliste, der viser opgaverne i arbejdsgangen og de godkendelser, der er knyttet til dem.</span><span class="sxs-lookup"><span data-stu-id="300c8-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="300c8-127">Indhold af arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="300c8-127">Workflow content</span></span>

+ [<span data-ttu-id="300c8-128">Arkitektur for arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="300c8-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="300c8-129">Arbejdsgangselementer</span><span class="sxs-lookup"><span data-stu-id="300c8-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="300c8-130">Arbejdsgangshandlinger</span><span class="sxs-lookup"><span data-stu-id="300c8-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="300c8-131">Oprette en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="300c8-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="300c8-132">Konfigurere egenskaberne for arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="300c8-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="300c8-133">Konfigurere en manuel opgave i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="300c8-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="300c8-134">Konfigurere en automatiseret opgave i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="300c8-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="300c8-135">Konfigurere en godkendelsesproces i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="300c8-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="300c8-136">Konfigurere et godkendelsestrin i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="300c8-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="300c8-137">Konfigurere en manuel beslutning i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="300c8-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="300c8-138">Konfigurere en betinget beslutning i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="300c8-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="300c8-139">Konfigurere en parallel aktivitet i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="300c8-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="300c8-140">Konfigurere en parallel gren i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="300c8-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="300c8-141">Konfigurere en arbejdsgang for linjeelement</span><span class="sxs-lookup"><span data-stu-id="300c8-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

