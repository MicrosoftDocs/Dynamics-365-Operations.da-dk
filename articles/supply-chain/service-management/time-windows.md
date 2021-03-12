---
title: Tidsvinduer
description: Du kan bruge tidsvinduer til at optimere planlægningen af serviceordrelinjer.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f64718e6a96cacc005644cbf4286e743111c02f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996495"
---
# <a name="time-windows"></a><span data-ttu-id="6291c-103">Tidsvinduer</span><span class="sxs-lookup"><span data-stu-id="6291c-103">Time windows</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6291c-104">Du kan bruge tidsvinduer til at optimere planlægningen af serviceordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="6291c-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="6291c-105">Du kan konfigurere systemet, så der automatisk oprettes serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="6291c-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="6291c-106">Baseret på de kriterier, der er angivet af et tidsvindue, kan du forbinde så mange serviceordrelinjer som muligt med så få serviceordrer som muligt.</span><span class="sxs-lookup"><span data-stu-id="6291c-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="6291c-107">I tidsvinduer specificeres det, hvor langt en serviceordrelinje kan flyttes fra dens beregnede dato.</span><span class="sxs-lookup"><span data-stu-id="6291c-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="6291c-108">Den beregnede dato er den dato, hvor serviceordrelinjen var planlagt til at forekomme.</span><span class="sxs-lookup"><span data-stu-id="6291c-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="6291c-109">Datoen er baseret på dens intervalindstilling og den serviceperiode, som du har defineret på siden **Oprette serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="6291c-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="6291c-110">Du definerer et tidsvindue ved at bruge værdierne i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="6291c-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="6291c-111">metode</span><span class="sxs-lookup"><span data-stu-id="6291c-111">Method</span></span> | <span data-ttu-id="6291c-112">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6291c-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6291c-113">Uge</span><span class="sxs-lookup"><span data-stu-id="6291c-113">Week</span></span>   | <span data-ttu-id="6291c-114">Den dato, hvor serviceordrelinjen kan flyttes til en hvilken som helst åben dag i samme uge som den oprindeligt beregnede dato.</span><span class="sxs-lookup"><span data-stu-id="6291c-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="6291c-115">Måned</span><span class="sxs-lookup"><span data-stu-id="6291c-115">Month</span></span>  | <span data-ttu-id="6291c-116">Den dato, hvor serviceordrelinjen kan flyttes til en hvilken som helst åben dag i samme måned som den oprindeligt beregnede dato.</span><span class="sxs-lookup"><span data-stu-id="6291c-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="6291c-117">For eksempel er den beregnede dato for en serviceordrelinje 15. februar 2017.</span><span class="sxs-lookup"><span data-stu-id="6291c-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="6291c-118">Serviceordrelinjen kan planlægges for en ugedag mellem 1. februar og 28. februar 2017.</span><span class="sxs-lookup"><span data-stu-id="6291c-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="6291c-119">Manuelt</span><span class="sxs-lookup"><span data-stu-id="6291c-119">Manual</span></span> | <span data-ttu-id="6291c-120">Du definerer det højeste antal dage, som serviceordrelinjen kan flyttes frem og tilbage i forhold til den oprindeligt beregnede dato.</span><span class="sxs-lookup"><span data-stu-id="6291c-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="6291c-121">Hvis du ikke specificerer et tidsvindue til en serviceaftalelinje, skal den serviceordrelinje, der er afledt af serviceaftalen, være på præcis samme dato, som den oprindeligt var planlagt til.</span><span class="sxs-lookup"><span data-stu-id="6291c-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6291c-122">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="6291c-122">Related topics</span></span>

[<span data-ttu-id="6291c-123">Oprette tidsvinduer</span><span class="sxs-lookup"><span data-stu-id="6291c-123">Create time windows</span></span>](create-time-windows.md)

