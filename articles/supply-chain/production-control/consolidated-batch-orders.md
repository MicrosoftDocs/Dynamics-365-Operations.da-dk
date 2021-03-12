---
title: Konsoliderede batchordrer
description: I denne artikel beskrives begrebet konsoliderede batchordrer.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2098cb458821146f6d1bf029591493ac745626f1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966449"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="85de7-103">Konsoliderede batchordrer</span><span class="sxs-lookup"><span data-stu-id="85de7-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85de7-104">I denne artikel beskrives begrebet konsoliderede batchordrer.</span><span class="sxs-lookup"><span data-stu-id="85de7-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="85de7-105">En bulkvare, der fremstilles, betragtes som en overordnet vare, hvorimod en pakket vare er en underordnet vare.</span><span class="sxs-lookup"><span data-stu-id="85de7-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="85de7-106">Forholdet mellem bulkvaren og den pakkede vares udtrykkes i en konvertering af bulkvare.</span><span class="sxs-lookup"><span data-stu-id="85de7-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="85de7-107">Denne konvertering af bulkvare er defineret i selve bulkvaren.</span><span class="sxs-lookup"><span data-stu-id="85de7-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="85de7-108">Pakkede varer kan være pakket i enten containere i enkeltstørrelse eller flere størrelser, der betragtes som en samlet enhed.</span><span class="sxs-lookup"><span data-stu-id="85de7-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="85de7-109">Ved at konsolidere ordrer for en bulkvare, kan du se alle de relaterede batchordrer i en enkel visning, der kan hjælpe dig med at fastslå, om der er udestående opgaver, der skal fuldføres.</span><span class="sxs-lookup"><span data-stu-id="85de7-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="85de7-110">En konsolideret batchordre kan indeholde enhver kombination af følgende ordrer:</span><span class="sxs-lookup"><span data-stu-id="85de7-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="85de7-111">En enkelt bulkordre og flere pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="85de7-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="85de7-112">Flere bulkordrer og flere pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="85de7-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="85de7-113">Flere bulkordrer og en enkelt pakket ordre</span><span class="sxs-lookup"><span data-stu-id="85de7-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="85de7-114">Kun pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="85de7-114">Only packed orders</span></span>




