---
title: Arbejdsgangsystem
description: I dette emne beskrives arbejdsgangssystemet i Microsoft Dynamics 365 for Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
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
ms.openlocfilehash: 7eb6d743131937081ce83b31988d792185cb28b2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "308638"
---
# <a name="workflow-system"></a><span data-ttu-id="5c87a-103">Arbejdsgangsystem</span><span class="sxs-lookup"><span data-stu-id="5c87a-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c87a-104">I dette emne beskrives arbejdsgangssystemet i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5c87a-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="5c87a-105">Hvad er en arbejdsgang?</span><span class="sxs-lookup"><span data-stu-id="5c87a-105">What is workflow?</span></span>

<span data-ttu-id="5c87a-106">Udtrykket *arbejdsgang* kan defineres på to måder: som et system og som en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="5c87a-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="5c87a-107">Arbejdsgang er et system</span><span class="sxs-lookup"><span data-stu-id="5c87a-107">Workflow is a system</span></span>

<span data-ttu-id="5c87a-108">Arbejdsgang er et system, som installeres med Finance and Operations, og som kører i AOS (applikationsobjektserveren).</span><span class="sxs-lookup"><span data-stu-id="5c87a-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="5c87a-109">Arbejdsgangssystemet indeholder funktioner, som du kan bruge til oprette individuelle arbejdsgange eller forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="5c87a-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="5c87a-110">Arbejdsgang er en forretningsproces</span><span class="sxs-lookup"><span data-stu-id="5c87a-110">Workflow is a business process</span></span>

<span data-ttu-id="5c87a-111">En arbejdsgang repræsenterer en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="5c87a-111">A workflow represents a business process.</span></span> <span data-ttu-id="5c87a-112">Den definerer, hvordan et dokument "flyder" eller bevæger sig gennem systemet, ved at vise, hvem der skal udføre en opgave, træffe en beslutning eller godkende et dokument.</span><span class="sxs-lookup"><span data-stu-id="5c87a-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="5c87a-113">I nedenstående illustration vises f.eks. en arbejdsgang for udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="5c87a-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Arbejdsgang med elementer, der er tilknyttet brugere](./media/workflow_user.gif)

<span data-ttu-id="5c87a-115">Hvis du bedre vil kunne forstå denne arbejdsgang, kan du antage, at Søren sender en udgiftsrapport for kr. 7.000.</span><span class="sxs-lookup"><span data-stu-id="5c87a-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="5c87a-116">I dette scenario skal Ivan gennemse de kvitteringer, som Søren har sendt til ham.</span><span class="sxs-lookup"><span data-stu-id="5c87a-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="5c87a-117">Henrik og Mette skal derefter godkende udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="5c87a-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="5c87a-118">Antag nu, at Søren sender en udgiftsrapport for kr. 11.000.</span><span class="sxs-lookup"><span data-stu-id="5c87a-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="5c87a-119">I dette scenario skal Ivan gennemse kvitteringerne, og Henrik, Mette og Dorthe skal godkende udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="5c87a-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="5c87a-120">Fordele ved at bruge arbejdsgangssystemet</span><span class="sxs-lookup"><span data-stu-id="5c87a-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="5c87a-121">Der er flere fordele ved at bruge arbejdsgangssystemet i organisationen:</span><span class="sxs-lookup"><span data-stu-id="5c87a-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="5c87a-122">**Ensartede processer** – Du kan definere, hvordan bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter, behandles.</span><span class="sxs-lookup"><span data-stu-id="5c87a-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="5c87a-123">Ved at bruge arbejdsgangssystemet kan du sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.</span><span class="sxs-lookup"><span data-stu-id="5c87a-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="5c87a-124">**Synliggørelse af processer** – Du kan spore status, historik og performanceværdier for arbejdsgangsforekomster.</span><span class="sxs-lookup"><span data-stu-id="5c87a-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="5c87a-125">Dette hjælper dig med at bestemme, om der skal foretages ændringer i arbejdsgangen for at forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="5c87a-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="5c87a-126">**Centraliseret arbejdsliste** – Brugerne kan få vist en centraliseret arbejdsliste, der viser opgaverne i arbejdsgangen og de godkendelser, der er knyttet til dem.</span><span class="sxs-lookup"><span data-stu-id="5c87a-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="5c87a-127">Indhold af arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="5c87a-127">Workflow content</span></span>

+ [<span data-ttu-id="5c87a-128">Arkitektur for arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="5c87a-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="5c87a-129">Arbejdsgangselementer</span><span class="sxs-lookup"><span data-stu-id="5c87a-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="5c87a-130">Arbejdsgangshandlinger</span><span class="sxs-lookup"><span data-stu-id="5c87a-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="5c87a-131">Oprette en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="5c87a-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="5c87a-132">Konfigurere egenskaberne for arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="5c87a-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="5c87a-133">Konfigurere en manuel opgave i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="5c87a-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="5c87a-134">Konfigurere en automatiseret opgave i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="5c87a-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="5c87a-135">Konfigurere en godkendelsesproces i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="5c87a-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="5c87a-136">Konfigurere et godkendelsestrin i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="5c87a-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="5c87a-137">Konfigurere en manuel beslutning i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="5c87a-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="5c87a-138">Konfigurere en betinget beslutning i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="5c87a-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="5c87a-139">Konfigurere en parallel aktivitet i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="5c87a-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="5c87a-140">Konfigurere en parallel gren i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="5c87a-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="5c87a-141">Konfigurere en arbejdsgang for linjeelement</span><span class="sxs-lookup"><span data-stu-id="5c87a-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)
