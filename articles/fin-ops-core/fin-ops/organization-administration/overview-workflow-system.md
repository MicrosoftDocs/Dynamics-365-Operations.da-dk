---
title: Oversigt over arbejdsgangssystem
description: I dette emne beskrives arbejdsgangssystemet.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e5e795ca6f7831ecd3fa28be9782f0b287eea6e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189999"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="c9f11-103">Oversigt over arbejdsgangssystem</span><span class="sxs-lookup"><span data-stu-id="c9f11-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9f11-104">I dette emne beskrives arbejdsgangssystemet.</span><span class="sxs-lookup"><span data-stu-id="c9f11-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="c9f11-105">Hvad er en arbejdsgang?</span><span class="sxs-lookup"><span data-stu-id="c9f11-105">What is workflow?</span></span>

<span data-ttu-id="c9f11-106">Udtrykket *arbejdsgang* kan defineres på to måder: som et system og som en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="c9f11-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="c9f11-107">Arbejdsgang er et system</span><span class="sxs-lookup"><span data-stu-id="c9f11-107">Workflow is a system</span></span>

<span data-ttu-id="c9f11-108">Arbejdsgang er et system, der kører på applikationsobjektserveren (AOS).</span><span class="sxs-lookup"><span data-stu-id="c9f11-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="c9f11-109">Arbejdsgangssystemet indeholder funktioner, som du kan bruge til oprette individuelle arbejdsgange eller forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="c9f11-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="c9f11-110">Arbejdsgang er en forretningsproces</span><span class="sxs-lookup"><span data-stu-id="c9f11-110">Workflow is a business process</span></span>

<span data-ttu-id="c9f11-111">En arbejdsgang repræsenterer en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="c9f11-111">A workflow represents a business process.</span></span> <span data-ttu-id="c9f11-112">Den definerer, hvordan et dokument "flyder" eller bevæger sig gennem systemet, ved at vise, hvem der skal udføre en opgave, træffe en beslutning eller godkende et dokument.</span><span class="sxs-lookup"><span data-stu-id="c9f11-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="c9f11-113">I nedenstående illustration vises f.eks. en arbejdsgang for udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="c9f11-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Arbejdsgang med elementer, der er tilknyttet brugere](./media/workflow_user.gif)

<span data-ttu-id="c9f11-115">Hvis du bedre vil kunne forstå denne arbejdsgang, kan du antage, at Søren sender en udgiftsrapport for kr. 7.000.</span><span class="sxs-lookup"><span data-stu-id="c9f11-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="c9f11-116">I dette scenario skal Ivan gennemse de kvitteringer, som Søren har sendt til ham.</span><span class="sxs-lookup"><span data-stu-id="c9f11-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="c9f11-117">Henrik og Mette skal derefter godkende udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="c9f11-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="c9f11-118">Antag nu, at Søren sender en udgiftsrapport for kr. 11.000.</span><span class="sxs-lookup"><span data-stu-id="c9f11-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="c9f11-119">I dette scenario skal Ivan gennemse kvitteringerne, og Henrik, Mette og Dorthe skal godkende udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="c9f11-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="c9f11-120">Fordele ved at bruge arbejdsgangssystemet</span><span class="sxs-lookup"><span data-stu-id="c9f11-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="c9f11-121">Der er flere fordele ved at bruge arbejdsgangssystemet i organisationen:</span><span class="sxs-lookup"><span data-stu-id="c9f11-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="c9f11-122">**Ensartede processer** – Du kan definere, hvordan bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter, behandles.</span><span class="sxs-lookup"><span data-stu-id="c9f11-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="c9f11-123">Ved at bruge arbejdsgangssystemet kan du sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.</span><span class="sxs-lookup"><span data-stu-id="c9f11-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="c9f11-124">**Synliggørelse af processer** – Du kan spore status, historik og performanceværdier for arbejdsgangsforekomster.</span><span class="sxs-lookup"><span data-stu-id="c9f11-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="c9f11-125">Dette hjælper dig med at bestemme, om der skal foretages ændringer i arbejdsgangen for at forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="c9f11-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="c9f11-126">**Centraliseret arbejdsliste** – Brugerne kan få vist en centraliseret arbejdsliste, der viser opgaverne i arbejdsgangen og de godkendelser, der er knyttet til dem.</span><span class="sxs-lookup"><span data-stu-id="c9f11-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="c9f11-127">Indhold af arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c9f11-127">Workflow content</span></span>

+ [<span data-ttu-id="c9f11-128">Arkitektur for arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c9f11-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="c9f11-129">Arbejdsgangselementer</span><span class="sxs-lookup"><span data-stu-id="c9f11-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="c9f11-130">Arbejdsgangshandlinger</span><span class="sxs-lookup"><span data-stu-id="c9f11-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="c9f11-131">Oprette en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c9f11-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="c9f11-132">Konfigurere egenskaberne for arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c9f11-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="c9f11-133">Konfigurere en manuel opgave i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c9f11-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="c9f11-134">Konfigurere en automatiseret opgave i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c9f11-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="c9f11-135">Konfigurere en godkendelsesproces i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c9f11-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="c9f11-136">Konfigurere et godkendelsestrin i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c9f11-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="c9f11-137">Konfigurere en manuel beslutning i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c9f11-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="c9f11-138">Konfigurere en betinget beslutning i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c9f11-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="c9f11-139">Konfigurere en parallel aktivitet i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c9f11-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="c9f11-140">Konfigurere en parallel gren i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c9f11-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="c9f11-141">Konfigurere en arbejdsgang for linjeelementer</span><span class="sxs-lookup"><span data-stu-id="c9f11-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="c9f11-142">Ofte stillede spørgsmål om arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c9f11-142">Workflow FAQ</span></span>](workflow-FAQ.md)
