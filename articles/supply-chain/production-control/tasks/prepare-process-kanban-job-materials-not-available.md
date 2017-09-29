--- 
title: "Forberede et kanban-procesjob, når materialer ikke er tilgængelige for arbejdscellen"
description: "Denne procedure drejer sig om at forberede et kanban-procesjob, når visse materialer ikke er tilgængelige for arbejdscellen, og det derfor er nødvendigt at plukke materialer fra lageret."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5a47af6910a9686e74ab6d1069dd02079e60cb8a
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="75e7c-103">Forberede et kanban-procesjob, når materialer ikke er tilgængelige for arbejdscellen</span><span class="sxs-lookup"><span data-stu-id="75e7c-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="75e7c-104">Denne procedure drejer sig om at forberede et kanban-procesjob, når visse materialer ikke er tilgængelige for arbejdscellen, og det derfor er nødvendigt at plukke materialer fra lageret.</span><span class="sxs-lookup"><span data-stu-id="75e7c-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="75e7c-105">Proceduren "Klargør et kanban-procesjob, når materialerne er tilgængelige" er en forudsætning for oprettelsen af denne procedure.</span><span class="sxs-lookup"><span data-stu-id="75e7c-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="75e7c-106">Denne procedure er beregnet til maskinoperatøren.</span><span class="sxs-lookup"><span data-stu-id="75e7c-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="75e7c-107">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="75e7c-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="75e7c-108">Gå til Produktionsstyring > Kanban > Kanban-område til procesjob.</span><span class="sxs-lookup"><span data-stu-id="75e7c-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="75e7c-109">Klik på rullelisten i feltet Arbejdscelle for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="75e7c-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="75e7c-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="75e7c-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="75e7c-111">Vælg arbejdscelle 1250.</span><span class="sxs-lookup"><span data-stu-id="75e7c-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="75e7c-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="75e7c-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="75e7c-113">Vælg kanban 000356.</span><span class="sxs-lookup"><span data-stu-id="75e7c-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="75e7c-114">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="75e7c-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="75e7c-115">Fjern markeringen af række 4 på listen.</span><span class="sxs-lookup"><span data-stu-id="75e7c-115">In the list, deselect row 4.</span></span> <span data-ttu-id="75e7c-116">eller vælg række 4, hvis du ikke har fuldført opgaven "Forberede et kanban-procesjob, når materialer er tilgængelige for arbejdscellen".</span><span class="sxs-lookup"><span data-stu-id="75e7c-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="75e7c-117">Slå udvidelsen af sektionen Plukliste til/fra.</span><span class="sxs-lookup"><span data-stu-id="75e7c-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="75e7c-118">Ikonet Ingen post under forsyningsstatus angiver, at 48 ea for vare P0002 mangler for arbejdscellen.</span><span class="sxs-lookup"><span data-stu-id="75e7c-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="75e7c-119">Overfør materialer til arbejdscelle</span><span class="sxs-lookup"><span data-stu-id="75e7c-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="75e7c-120">Slå udvidelsen af sektionen Overførselsjob til/fra.</span><span class="sxs-lookup"><span data-stu-id="75e7c-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="75e7c-121">Brug Quick Filter til at filtrere på feltet Varenummer med værdien 'P0002'.</span><span class="sxs-lookup"><span data-stu-id="75e7c-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="75e7c-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="75e7c-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="75e7c-123">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="75e7c-123">Click Start.</span></span>
    * <span data-ttu-id="75e7c-124">Overførsel er i gang.</span><span class="sxs-lookup"><span data-stu-id="75e7c-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="75e7c-125">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="75e7c-125">Click Complete.</span></span>
    * <span data-ttu-id="75e7c-126">Vare P0002 er nu tilgængelig på pluklisten for kanban-jobbet.</span><span class="sxs-lookup"><span data-stu-id="75e7c-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="75e7c-127">Det betyder, at vi kan klargøre kanban med alle de nødvendige materialer.</span><span class="sxs-lookup"><span data-stu-id="75e7c-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="75e7c-128">Klik på Klargør.</span><span class="sxs-lookup"><span data-stu-id="75e7c-128">Click Prepare.</span></span>
    * <span data-ttu-id="75e7c-129">Bemærk, at et ikon i Jobstatus angiver, at jobbet nu er klart.</span><span class="sxs-lookup"><span data-stu-id="75e7c-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  


