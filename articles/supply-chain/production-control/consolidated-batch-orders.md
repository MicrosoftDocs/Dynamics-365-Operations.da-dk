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
ms.search.scope: Core, Operations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: faeb90aa3366a58b746c0b397dd950bfb8c9024f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424796"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="7f3b0-103">Konsoliderede batchordrer</span><span class="sxs-lookup"><span data-stu-id="7f3b0-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f3b0-104">I denne artikel beskrives begrebet konsoliderede batchordrer.</span><span class="sxs-lookup"><span data-stu-id="7f3b0-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="7f3b0-105">En bulkvare, der fremstilles, betragtes som en overordnet vare, hvorimod en pakket vare er en underordnet vare.</span><span class="sxs-lookup"><span data-stu-id="7f3b0-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="7f3b0-106">Forholdet mellem bulkvaren og den pakkede vares udtrykkes i en konvertering af bulkvare.</span><span class="sxs-lookup"><span data-stu-id="7f3b0-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="7f3b0-107">Denne konvertering af bulkvare er defineret i selve bulkvaren.</span><span class="sxs-lookup"><span data-stu-id="7f3b0-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="7f3b0-108">Pakkede varer kan være pakket i enten containere i enkeltstørrelse eller flere størrelser, der betragtes som en samlet enhed.</span><span class="sxs-lookup"><span data-stu-id="7f3b0-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="7f3b0-109">Ved at konsolidere ordrer for en bulkvare, kan du se alle de relaterede batchordrer i en enkel visning, der kan hjælpe dig med at fastslå, om der er udestående opgaver, der skal fuldføres.</span><span class="sxs-lookup"><span data-stu-id="7f3b0-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="7f3b0-110">En konsolideret batchordre kan indeholde enhver kombination af følgende ordrer:</span><span class="sxs-lookup"><span data-stu-id="7f3b0-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="7f3b0-111">En enkelt bulkordre og flere pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="7f3b0-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="7f3b0-112">Flere bulkordrer og flere pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="7f3b0-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="7f3b0-113">Flere bulkordrer og en enkelt pakket ordre</span><span class="sxs-lookup"><span data-stu-id="7f3b0-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="7f3b0-114">Kun pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="7f3b0-114">Only packed orders</span></span>




