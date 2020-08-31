---
title: Konfigurere parallelle aktiviteter i en arbejdsgang
description: Udfør følgende procedurer i arbejdsgangseditoren, hvis du vil konfigurere en parallel aktivitet.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 998ee559a092c4acd34a6df05e893bdbf4289099
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698309"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="6d9dd-103">Konfigurere parallelle aktiviteter i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="6d9dd-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d9dd-104">Udfør følgende procedurer i arbejdsgangseditoren, hvis du vil konfigurere en parallel aktivitet.</span><span class="sxs-lookup"><span data-stu-id="6d9dd-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="6d9dd-105">En parallel aktivitet består af grene i en arbejdsgang, der kører samtidigt.</span><span class="sxs-lookup"><span data-stu-id="6d9dd-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="6d9dd-106">Navnet på en parallel aktivitet</span><span class="sxs-lookup"><span data-stu-id="6d9dd-106">Name a parallel activity</span></span>

<span data-ttu-id="6d9dd-107">Udfør følgende trin for at angive et navn på den parallelle aktivitet.</span><span class="sxs-lookup"><span data-stu-id="6d9dd-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="6d9dd-108">Højreklik på den parallelle aktivitet, og klik derefter på **Egenskaber** for at åbne formen **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="6d9dd-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="6d9dd-109">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="6d9dd-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="6d9dd-110">Angiv et entydigt navn på den parallelle aktivitet i feltet **Nanv**.</span><span class="sxs-lookup"><span data-stu-id="6d9dd-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="6d9dd-111">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="6d9dd-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="6d9dd-112">Konfigurere grenene i den parallelle aktivitet</span><span class="sxs-lookup"><span data-stu-id="6d9dd-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="6d9dd-113">Udfør følgende trin for at tilføje og konfigurere grenene i den parallelle aktivitet.</span><span class="sxs-lookup"><span data-stu-id="6d9dd-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="6d9dd-114">Dobbeltklik på den parallelle aktivitet for at få vist grenene i den parallelle aktivitet.</span><span class="sxs-lookup"><span data-stu-id="6d9dd-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="6d9dd-115">Du kan tilføje en gren ved at trække elementet **Gren** fra området **Arbejdsgangselementer** til et indsættelsespunkt på lærredet.</span><span class="sxs-lookup"><span data-stu-id="6d9dd-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="6d9dd-116">I følgende illustration vises et indsættelsespunkt.</span><span class="sxs-lookup"><span data-stu-id="6d9dd-116">The following figure shows an insertion point.</span></span>

    ![Indsættelsespunkt](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="6d9dd-118">Grenenes rækkefølge betyder ikke noget, fordi alle grenene i en parallel aktivitet kører samtidigt.</span><span class="sxs-lookup"><span data-stu-id="6d9dd-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="6d9dd-119">Hvis du vil konfigurere hver gren, skal du se [Konfigurer parallelle grene i en arbejdsgang](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="6d9dd-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>
