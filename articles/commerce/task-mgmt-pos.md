---
title: Opgavestyring i POS
description: I dette emne beskrives opgavestyring i POS-programmet i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cc685fcd584fe2ab5cd9282e8fbefbd284d5b2a2
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036780"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="5b3ba-103">Opgavestyring i POS</span><span class="sxs-lookup"><span data-stu-id="5b3ba-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5b3ba-104">I dette emne beskrives opgavestyring i POS-programmet i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5b3ba-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="5b3ba-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="5b3ba-105">Overview</span></span>

<span data-ttu-id="5b3ba-106">POS-programmet i Dynamics 365 Commerce indeholder funktioner til styring af opgaver, som giver butikschefer og arbejdere mulighed for at administrere opgaver og opdatere opgavestatus.</span><span class="sxs-lookup"><span data-stu-id="5b3ba-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="5b3ba-107">Butiksmedarbejdere kan få adgang til opgaver ved at vælge feltet **Opgaver** på POS-startsiden eller ved at vælge opgavebeskeder.</span><span class="sxs-lookup"><span data-stu-id="5b3ba-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="5b3ba-108">Som standard føres arbejdere til fanen **Mine opgaver**, hvor de kan få vist de opgaver, der er tildelt til dem.</span><span class="sxs-lookup"><span data-stu-id="5b3ba-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="5b3ba-109">De kan imidlertid nemt skifte til fanerne **Forfaldne opgaver**, **Åbne opgaver** og **Opgavelister**.</span><span class="sxs-lookup"><span data-stu-id="5b3ba-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="5b3ba-110">Opgavehandlinger for butikschefer</span><span class="sxs-lookup"><span data-stu-id="5b3ba-110">Task operations for store managers</span></span>

<span data-ttu-id="5b3ba-111">Butikschefer kan udføre følgende opgavehandlinger i POS-programmet ved hjælp af knapperne på kommandolinjen:</span><span class="sxs-lookup"><span data-stu-id="5b3ba-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="5b3ba-112">**Tildel** – Tildel valgte opgaver til en butiksmedarbejder.</span><span class="sxs-lookup"><span data-stu-id="5b3ba-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="5b3ba-113">**Opgavestatus** – Ret statussen af de markerede opgaver.</span><span class="sxs-lookup"><span data-stu-id="5b3ba-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="5b3ba-114">**Filter** – Som standard er det kun aktive opgaver, der vises.</span><span class="sxs-lookup"><span data-stu-id="5b3ba-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="5b3ba-115">Ved at anvende filtre kan ledere imidlertid få vist alle opgaver, også opgaver, der er fuldført eller annulleret.</span><span class="sxs-lookup"><span data-stu-id="5b3ba-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="5b3ba-116">**Ny opgave** – Opret en opgave under en eksisterende opgaveliste, eller opret en opgave med et enkelt formål.</span><span class="sxs-lookup"><span data-stu-id="5b3ba-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="5b3ba-117">Butiksmedarbejdere kan udføre følgende opgavehandlinger i POS-programmet ved hjælp af knapperne på kommandolinjen:</span><span class="sxs-lookup"><span data-stu-id="5b3ba-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="5b3ba-118">**Opgavestatus** – Ret statussen af de markerede opgaver.</span><span class="sxs-lookup"><span data-stu-id="5b3ba-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="5b3ba-119">**Filter** – Som standard er det kun aktive opgaver, der vises.</span><span class="sxs-lookup"><span data-stu-id="5b3ba-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="5b3ba-120">Ved at anvende filtre kan arbejdere imidlertid få vist alle opgaver, også opgaver, der er fuldført eller annulleret.</span><span class="sxs-lookup"><span data-stu-id="5b3ba-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="5b3ba-121">I følgende illustration vises fanen **Mine opgaver** i POS-programmet i Commerce.</span><span class="sxs-lookup"><span data-stu-id="5b3ba-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Fanen Mine opgaver i POS-programmet i Commerce](media/POS-task-management.png)

<span data-ttu-id="5b3ba-123">I følgende illustration vises fanen **Opgavelister**.</span><span class="sxs-lookup"><span data-stu-id="5b3ba-123">The following illustration shows the **Task lists** tab.</span></span>

![Fanen Opgavelister i POS-programmet i Commerce](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="5b3ba-125">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5b3ba-125">Additional resources</span></span>

[<span data-ttu-id="5b3ba-126">Oversigt over opgavestyring</span><span class="sxs-lookup"><span data-stu-id="5b3ba-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="5b3ba-127">Konfigurer opgavestyring</span><span class="sxs-lookup"><span data-stu-id="5b3ba-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="5b3ba-128">Oprette opgavelister og tilføje opgaver</span><span class="sxs-lookup"><span data-stu-id="5b3ba-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="5b3ba-129">Tildele opgavelister til butikker eller medarbejdere</span><span class="sxs-lookup"><span data-stu-id="5b3ba-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)
