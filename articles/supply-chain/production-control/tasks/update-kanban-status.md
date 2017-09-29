--- 
title: Opdatere status for kanban
description: "Når en kanban bliver tømt ved en fejltagelse eller en modtaget kanban skal tømmes, skal du opdatere kanban-statussen."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
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
ms.openlocfilehash: 3c2b5a5fbfc5bd83cc68ffafaa243dac9244c003
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="update-kanban-status"></a><span data-ttu-id="261c4-103">Opdatere status for kanban</span><span class="sxs-lookup"><span data-stu-id="261c4-103">Update kanban status</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="261c4-104">Når en kanban bliver tømt ved en fejltagelse eller en modtaget kanban skal tømmes, skal du opdatere kanban-statussen.</span><span class="sxs-lookup"><span data-stu-id="261c4-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="261c4-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="261c4-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="261c4-106">Denne procedure er beregnet til den tilsynsførende.</span><span class="sxs-lookup"><span data-stu-id="261c4-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="261c4-107">Find kanban.</span><span class="sxs-lookup"><span data-stu-id="261c4-107">Find the kanban.</span></span>
1. <span data-ttu-id="261c4-108">Gå til Produktionsstyring > Kanban > Kanbans.</span><span class="sxs-lookup"><span data-stu-id="261c4-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="261c4-109">Åbn kolonnefilteret Status på håndteringsenhed.</span><span class="sxs-lookup"><span data-stu-id="261c4-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="261c4-110">Klik på Ryd.</span><span class="sxs-lookup"><span data-stu-id="261c4-110">Click Clear.</span></span>
    * <span data-ttu-id="261c4-111">Dette nulstiller filtrene.</span><span class="sxs-lookup"><span data-stu-id="261c4-111">This resets the filters.</span></span>  
4. <span data-ttu-id="261c4-112">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="261c4-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="261c4-113">Filtrer f.eks. efter feltet Kortnummer med værdien '000149'.</span><span class="sxs-lookup"><span data-stu-id="261c4-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="261c4-114">Ændre statussen Tømt til Modtaget</span><span class="sxs-lookup"><span data-stu-id="261c4-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="261c4-115">Klik på Fortryd tømning af materialehåndteringsenhed.</span><span class="sxs-lookup"><span data-stu-id="261c4-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="261c4-116">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="261c4-116">Click OK.</span></span>
    * <span data-ttu-id="261c4-117">Bemærk, at Status på håndteringsenhed er Modtaget.</span><span class="sxs-lookup"><span data-stu-id="261c4-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="261c4-118">Ændre statussen Modtaget til Tømt</span><span class="sxs-lookup"><span data-stu-id="261c4-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="261c4-119">Klik på Tøm kanban.</span><span class="sxs-lookup"><span data-stu-id="261c4-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="261c4-120">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="261c4-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="261c4-121">Bemærk, at Status på håndteringsenhed er Tømt.</span><span class="sxs-lookup"><span data-stu-id="261c4-121">Notice that the Handling unit status is Emptied.</span></span>  


