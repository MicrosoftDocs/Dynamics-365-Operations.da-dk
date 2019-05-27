---
title: Forberede et kanban-procesjob, når materialer er tilgængelige for arbejdscellen
description: Denne opgave fokuserer på at klargøre et kanban-procesjob, når alle materialerne ikke er tilgængelige for arbejdscellen.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 714196ba92fe3f57c80809930ed54705a4e75078
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552549"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="ab2b9-103">Forberede et kanban-procesjob, når materialer er tilgængelige for arbejdscellen</span><span class="sxs-lookup"><span data-stu-id="ab2b9-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ab2b9-104">Denne opgave fokuserer på at klargøre et kanban-procesjob, når alle materialerne ikke er tilgængelige for arbejdscellen.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="ab2b9-105">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="ab2b9-106">Denne opgave er beregnet til maskinoperatøren.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="ab2b9-107">Gå til Kanban-område til procesjob.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="ab2b9-108">Klik på rullelisten i feltet Arbejdscelle for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="ab2b9-109">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ab2b9-110">Vælg arbejdscelle 1250, og klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="ab2b9-111">Markér række 4 på listen.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="ab2b9-112">I det rene demofirma er Kanban 000329 i række 4 det første job, der ikke er fuldført endnu.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="ab2b9-113">Slå udvidelsen af sektionen Plukliste til/fra.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="ab2b9-114">Kontrollér, at forsyningsstatus er tilgængelig for alle varer på pluklisten.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="ab2b9-115">Hvis flere job er markeret, viser pluklisten summen af alle varer, der er nødvendige for de valgte job.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="ab2b9-116">Klik på Klargør.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-116">Click Prepare.</span></span>
    * <span data-ttu-id="ab2b9-117">Klargøringsprocessen er nu fuldført.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-117">The preparation process is now completed.</span></span> <span data-ttu-id="ab2b9-118">Det markerede afkrydsningsfelt for alle rækker på pluklisten angiver, at forsyningsstatus er plukket.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  

