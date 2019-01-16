---
title: Konfigurere parallelle aktiviteter i en arbejdsgang
description: "Udfør følgende procedurer i arbejdsgangseditoren, hvis du vil konfigurere en parallel aktivitet."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 01c1fa876dd66ba6f0e1cdcecff56f424e117bd9
ms.contentlocale: da-dk
ms.lasthandoff: 12/18/2018

---

# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="f1c15-103">Konfigurere parallelle aktiviteter i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="f1c15-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1c15-104">Udfør følgende procedurer i arbejdsgangseditoren, hvis du vil konfigurere en parallel aktivitet.</span><span class="sxs-lookup"><span data-stu-id="f1c15-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="f1c15-105">En parallel aktivitet består af grene i en arbejdsgang, der kører samtidigt.</span><span class="sxs-lookup"><span data-stu-id="f1c15-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="f1c15-106">Navnet på en parallel aktivitet</span><span class="sxs-lookup"><span data-stu-id="f1c15-106">Name a parallel activity</span></span>

<span data-ttu-id="f1c15-107">Udfør følgende trin for at angive et navn på den parallelle aktivitet.</span><span class="sxs-lookup"><span data-stu-id="f1c15-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="f1c15-108">Højreklik på den parallelle aktivitet, og klik derefter på **Egenskaber** for at åbne formen **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="f1c15-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="f1c15-109">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="f1c15-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="f1c15-110">Angiv et entydigt navn på den parallelle aktivitet i feltet **Nanv**.</span><span class="sxs-lookup"><span data-stu-id="f1c15-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="f1c15-111">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="f1c15-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="f1c15-112">Konfigurere grenene i den parallelle aktivitet</span><span class="sxs-lookup"><span data-stu-id="f1c15-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="f1c15-113">Udfør følgende trin for at tilføje og konfigurere grenene i den parallelle aktivitet.</span><span class="sxs-lookup"><span data-stu-id="f1c15-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="f1c15-114">Dobbeltklik på den parallelle aktivitet for at få vist grenene i den parallelle aktivitet.</span><span class="sxs-lookup"><span data-stu-id="f1c15-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="f1c15-115">Du kan tilføje en gren ved at trække elementet **Gren** fra området **Arbejdsgangselementer** til et indsættelsespunkt på lærredet.</span><span class="sxs-lookup"><span data-stu-id="f1c15-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="f1c15-116">I følgende illustration vises et indsættelsespunkt.</span><span class="sxs-lookup"><span data-stu-id="f1c15-116">The following figure shows an insertion point.</span></span>

    ![Indsættelsespunkt](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="f1c15-118">Grenenes rækkefølge betyder ikke noget, fordi alle grenene i en parallel aktivitet kører samtidigt.</span><span class="sxs-lookup"><span data-stu-id="f1c15-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="f1c15-119">Hvis du vil konfigurere hver gren, skal du se [Konfigurere en parallel gren](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="f1c15-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>

