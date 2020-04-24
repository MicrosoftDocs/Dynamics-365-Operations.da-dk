---
title: Estimere en produktionsordre
description: Du kan køre denne procedure ved hjælp af demodatafirmaet USMF eller dine egne datasæt.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bbb541a09809c1f1bfada42094d840a2f6e7764
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207042"
---
# <a name="estimate-a-production-order"></a><span data-ttu-id="02599-103">Estimere en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="02599-103">Estimate a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02599-104">Du kan køre denne procedure ved hjælp af demodatafirmaet USMF eller dine egne datasæt.</span><span class="sxs-lookup"><span data-stu-id="02599-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="02599-105">I begge tilfælde skal du have en åben produktionsordre, der har statussen Oprettet.</span><span class="sxs-lookup"><span data-stu-id="02599-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="02599-106">Dette er den anden procedure ud af syv, der beskriver produktionsordrelivscyklussen.</span><span class="sxs-lookup"><span data-stu-id="02599-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="02599-107">Estimere en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="02599-107">Estimate a production order</span></span>
1. <span data-ttu-id="02599-108">Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="02599-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="02599-109">Vælg en ordre, der har statussen Oprettet i gitteret.</span><span class="sxs-lookup"><span data-stu-id="02599-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="02599-110">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="02599-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="02599-111">Klik på Forkalkulation.</span><span class="sxs-lookup"><span data-stu-id="02599-111">Click Estimate.</span></span>
    * <span data-ttu-id="02599-112">I dette trin beregnes de forkalkulerede omkostninger for en enkelt produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="02599-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="02599-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="02599-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="02599-114">Vis beregningsoplysningerne</span><span class="sxs-lookup"><span data-stu-id="02599-114">View the calculation details</span></span>
1. <span data-ttu-id="02599-115">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="02599-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="02599-116">Klik på Vis beregningsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="02599-116">Click View calculation details.</span></span>
    * <span data-ttu-id="02599-117">Denne side viser kostprisopdelingen.</span><span class="sxs-lookup"><span data-stu-id="02599-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="02599-118">For eksempel kan du se den samlede kostpris pr. enhed for det færdige produkt i den første række.</span><span class="sxs-lookup"><span data-stu-id="02599-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="02599-119">De efterfølgende rækker indeholder omkostninger i henhold til styklisten, produktionsruten, og indirekte omkostninger.</span><span class="sxs-lookup"><span data-stu-id="02599-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  
