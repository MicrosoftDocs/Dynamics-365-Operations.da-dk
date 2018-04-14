---
title: Tidsvinduer
description: "Du kan bruge tidsvinduer til at optimere planlægningen af serviceordrelinjer."
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9b215e1645c0f0f60437dc363530e2af3d262c4e
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="time-windows"></a><span data-ttu-id="1fcd2-103">Tidsvinduer</span><span class="sxs-lookup"><span data-stu-id="1fcd2-103">Time windows</span></span>  

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="1fcd2-104">Du kan bruge tidsvinduer til at optimere planlægningen af serviceordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="1fcd2-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="1fcd2-105">Du kan konfigurere systemet, så der automatisk oprettes serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="1fcd2-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="1fcd2-106">Baseret på de kriterier, der er angivet af et tidsvindue, kan du forbinde så mange serviceordrelinjer som muligt med så få serviceordrer som muligt.</span><span class="sxs-lookup"><span data-stu-id="1fcd2-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="1fcd2-107">I tidsvinduer specificeres det, hvor langt en serviceordrelinje kan flyttes fra dens beregnede dato.</span><span class="sxs-lookup"><span data-stu-id="1fcd2-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="1fcd2-108">Den beregnede dato er den dato, hvor serviceordrelinjen var planlagt til at forekomme.</span><span class="sxs-lookup"><span data-stu-id="1fcd2-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="1fcd2-109">Datoen er baseret på dens intervalindstilling og den serviceperiode, som du har defineret på siden **Oprette serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="1fcd2-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="1fcd2-110">Du definerer et tidsvindue ved at bruge værdierne i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="1fcd2-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="1fcd2-111">metode</span><span class="sxs-lookup"><span data-stu-id="1fcd2-111">Method</span></span> | <span data-ttu-id="1fcd2-112">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="1fcd2-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fcd2-113">Uge</span><span class="sxs-lookup"><span data-stu-id="1fcd2-113">Week</span></span>   | <span data-ttu-id="1fcd2-114">Den dato, hvor serviceordrelinjen kan flyttes til en hvilken som helst åben dag i samme uge som den oprindeligt beregnede dato.</span><span class="sxs-lookup"><span data-stu-id="1fcd2-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="1fcd2-115">Måned</span><span class="sxs-lookup"><span data-stu-id="1fcd2-115">Month</span></span>  | <span data-ttu-id="1fcd2-116">Den dato, hvor serviceordrelinjen kan flyttes til en hvilken som helst åben dag i samme måned som den oprindeligt beregnede dato.</span><span class="sxs-lookup"><span data-stu-id="1fcd2-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="1fcd2-117">For eksempel er den beregnede dato for en serviceordrelinje 15. februar 2017.</span><span class="sxs-lookup"><span data-stu-id="1fcd2-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="1fcd2-118">Serviceordrelinjen kan planlægges for en ugedag mellem 1. februar og 28. februar 2017.</span><span class="sxs-lookup"><span data-stu-id="1fcd2-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="1fcd2-119">Manuelt</span><span class="sxs-lookup"><span data-stu-id="1fcd2-119">Manual</span></span> | <span data-ttu-id="1fcd2-120">Du definerer det højeste antal dage, som serviceordrelinjen kan flyttes frem og tilbage i forhold til den oprindeligt beregnede dato.</span><span class="sxs-lookup"><span data-stu-id="1fcd2-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="1fcd2-121">Hvis du ikke specificerer et tidsvindue til en serviceaftalelinje, skal den serviceordrelinje, der er afledt af serviceaftalen, være på præcis samme dato, som den oprindeligt var planlagt til.</span><span class="sxs-lookup"><span data-stu-id="1fcd2-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fcd2-122">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="1fcd2-122">Related topics</span></span>

[<span data-ttu-id="1fcd2-123">Oprette tidsvinduer</span><span class="sxs-lookup"><span data-stu-id="1fcd2-123">Create time windows</span></span>](create-time-windows.md)


