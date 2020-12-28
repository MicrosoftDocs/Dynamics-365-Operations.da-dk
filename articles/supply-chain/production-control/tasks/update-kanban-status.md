---
title: Opdatere status for kanban
description: Når en kanban bliver tømt ved en fejltagelse eller en modtaget kanban skal tømmes, skal du opdatere kanban-statussen.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb8559c0843d7e6e538b5b29dc394a50d05462ee
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424795"
---
# <a name="update-kanban-status"></a><span data-ttu-id="c79d5-103">Opdatere status for kanban</span><span class="sxs-lookup"><span data-stu-id="c79d5-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c79d5-104">Når en kanban bliver tømt ved en fejltagelse eller en modtaget kanban skal tømmes, skal du opdatere kanban-statussen.</span><span class="sxs-lookup"><span data-stu-id="c79d5-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="c79d5-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="c79d5-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c79d5-106">Denne procedure er beregnet til den tilsynsførende.</span><span class="sxs-lookup"><span data-stu-id="c79d5-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="c79d5-107">Find kanban.</span><span class="sxs-lookup"><span data-stu-id="c79d5-107">Find the kanban.</span></span>
1. <span data-ttu-id="c79d5-108">Gå til Produktionsstyring > Kanban > Kanbans.</span><span class="sxs-lookup"><span data-stu-id="c79d5-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="c79d5-109">Åbn kolonnefilteret Status på håndteringsenhed.</span><span class="sxs-lookup"><span data-stu-id="c79d5-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="c79d5-110">Klik på Ryd.</span><span class="sxs-lookup"><span data-stu-id="c79d5-110">Click Clear.</span></span>
    * <span data-ttu-id="c79d5-111">Dette nulstiller filtrene.</span><span class="sxs-lookup"><span data-stu-id="c79d5-111">This resets the filters.</span></span>  
4. <span data-ttu-id="c79d5-112">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="c79d5-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c79d5-113">Filtrer f.eks. efter feltet Kortnummer med værdien '000149'.</span><span class="sxs-lookup"><span data-stu-id="c79d5-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="c79d5-114">Ændre statussen Tømt til Modtaget</span><span class="sxs-lookup"><span data-stu-id="c79d5-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="c79d5-115">Klik på Fortryd tømning af materialehåndteringsenhed.</span><span class="sxs-lookup"><span data-stu-id="c79d5-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="c79d5-116">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c79d5-116">Click OK.</span></span>
    * <span data-ttu-id="c79d5-117">Bemærk, at Status på håndteringsenhed er Modtaget.</span><span class="sxs-lookup"><span data-stu-id="c79d5-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="c79d5-118">Ændre statussen Modtaget til Tømt</span><span class="sxs-lookup"><span data-stu-id="c79d5-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="c79d5-119">Klik på Tøm kanban.</span><span class="sxs-lookup"><span data-stu-id="c79d5-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="c79d5-120">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c79d5-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c79d5-121">Bemærk, at Status på håndteringsenhed er Tømt.</span><span class="sxs-lookup"><span data-stu-id="c79d5-121">Notice that the Handling unit status is Emptied.</span></span>  

