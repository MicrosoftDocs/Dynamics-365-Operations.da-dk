---
title: Forberede et kanban-procesjob, når materialer ikke er tilgængelige for arbejdscellen
description: Denne procedure drejer sig om at forberede et kanban-procesjob, når visse materialer ikke er tilgængelige for arbejdscellen, og det derfor er nødvendigt at plukke materialer fra lageret.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bba9e5cb7dfddd2a80a37e7a57fdf94a91341e8f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843619"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="21812-103">Forberede et kanban-procesjob, når materialer ikke er tilgængelige for arbejdscellen</span><span class="sxs-lookup"><span data-stu-id="21812-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21812-104">Denne procedure drejer sig om at forberede et kanban-procesjob, når visse materialer ikke er tilgængelige for arbejdscellen, og det derfor er nødvendigt at plukke materialer fra lageret.</span><span class="sxs-lookup"><span data-stu-id="21812-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="21812-105">Proceduren "Klargør et kanban-procesjob, når materialerne er tilgængelige" er en forudsætning for oprettelsen af denne procedure.</span><span class="sxs-lookup"><span data-stu-id="21812-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="21812-106">Denne procedure er beregnet til maskinoperatøren.</span><span class="sxs-lookup"><span data-stu-id="21812-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="21812-107">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="21812-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="21812-108">Gå til Produktionsstyring > Kanban > Kanban-område til procesjob.</span><span class="sxs-lookup"><span data-stu-id="21812-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="21812-109">Klik på rullelisten i feltet Arbejdscelle for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="21812-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="21812-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="21812-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="21812-111">Vælg arbejdscelle 1250.</span><span class="sxs-lookup"><span data-stu-id="21812-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="21812-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="21812-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="21812-113">Vælg kanban 000356.</span><span class="sxs-lookup"><span data-stu-id="21812-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="21812-114">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="21812-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="21812-115">Fjern markeringen af række 4 på listen.</span><span class="sxs-lookup"><span data-stu-id="21812-115">In the list, deselect row 4.</span></span> <span data-ttu-id="21812-116">eller vælg række 4, hvis du ikke har fuldført opgaven "Forberede et kanban-procesjob, når materialer er tilgængelige for arbejdscellen".</span><span class="sxs-lookup"><span data-stu-id="21812-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="21812-117">Slå udvidelsen af sektionen Plukliste til/fra.</span><span class="sxs-lookup"><span data-stu-id="21812-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="21812-118">Ikonet Ingen post under forsyningsstatus angiver, at 48 ea for vare P0002 mangler for arbejdscellen.</span><span class="sxs-lookup"><span data-stu-id="21812-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="21812-119">Overfør materialer til arbejdscelle</span><span class="sxs-lookup"><span data-stu-id="21812-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="21812-120">Slå udvidelsen af sektionen Overførselsjob til/fra.</span><span class="sxs-lookup"><span data-stu-id="21812-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="21812-121">Brug Quick Filter til at filtrere på feltet Varenummer med værdien 'P0002'.</span><span class="sxs-lookup"><span data-stu-id="21812-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="21812-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="21812-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="21812-123">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="21812-123">Click Start.</span></span>
    * <span data-ttu-id="21812-124">Overførsel er i gang.</span><span class="sxs-lookup"><span data-stu-id="21812-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="21812-125">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="21812-125">Click Complete.</span></span>
    * <span data-ttu-id="21812-126">Vare P0002 er nu tilgængelig på pluklisten for kanban-jobbet.</span><span class="sxs-lookup"><span data-stu-id="21812-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="21812-127">Det betyder, at vi kan klargøre kanban med alle de nødvendige materialer.</span><span class="sxs-lookup"><span data-stu-id="21812-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="21812-128">Klik på Klargør.</span><span class="sxs-lookup"><span data-stu-id="21812-128">Click Prepare.</span></span>
    * <span data-ttu-id="21812-129">Bemærk, at et ikon i Jobstatus angiver, at jobbet nu er klart.</span><span class="sxs-lookup"><span data-stu-id="21812-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  

