---
title: Konsoliderede batchordrer
description: I denne artikel beskrives begrebet konsoliderede batchordrer.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 3ca9c920ea333bd21defebc29b40243d3a618a3d
ms.contentlocale: da-dk
ms.lasthandoff: 07/18/2017

---

# <a name="consolidated-batch-orders"></a><span data-ttu-id="cc54d-103">Konsoliderede batchordrer</span><span class="sxs-lookup"><span data-stu-id="cc54d-103">Consolidated batch orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cc54d-104">I denne artikel beskrives begrebet konsoliderede batchordrer.</span><span class="sxs-lookup"><span data-stu-id="cc54d-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="cc54d-105">En bulkvare, der fremstilles, betragtes som en overordnet vare, hvorimod en pakket vare er en underordnet vare.</span><span class="sxs-lookup"><span data-stu-id="cc54d-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="cc54d-106">Forholdet mellem bulkvaren og den pakkede vares udtrykkes i en konvertering af bulkvare.</span><span class="sxs-lookup"><span data-stu-id="cc54d-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="cc54d-107">Denne konvertering af bulkvare er defineret i selve bulkvaren.</span><span class="sxs-lookup"><span data-stu-id="cc54d-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="cc54d-108">Pakkede varer kan være pakket i enten containere i enkeltstørrelse eller flere størrelser, der betragtes som en samlet enhed.</span><span class="sxs-lookup"><span data-stu-id="cc54d-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="cc54d-109">Ved at konsolidere ordrer for en bulkvare, kan du se alle de relaterede batchordrer i en enkel visning, der kan hjælpe dig med at fastslå, om der er udestående opgaver, der skal fuldføres.</span><span class="sxs-lookup"><span data-stu-id="cc54d-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="cc54d-110">En konsolideret batchordre kan indeholde enhver kombination af følgende ordrer:</span><span class="sxs-lookup"><span data-stu-id="cc54d-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="cc54d-111">En enkelt bulkordre og flere pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="cc54d-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="cc54d-112">Flere bulkordrer og flere pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="cc54d-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="cc54d-113">Flere bulkordrer og en enkelt pakket ordre</span><span class="sxs-lookup"><span data-stu-id="cc54d-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="cc54d-114">Kun pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="cc54d-114">Only packed orders</span></span>





