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
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e8b017455c0821d97f9039d4ebf00d2dfa28eaa
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211633"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="fdd4a-103">Konsoliderede batchordrer</span><span class="sxs-lookup"><span data-stu-id="fdd4a-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdd4a-104">I denne artikel beskrives begrebet konsoliderede batchordrer.</span><span class="sxs-lookup"><span data-stu-id="fdd4a-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="fdd4a-105">En bulkvare, der fremstilles, betragtes som en overordnet vare, hvorimod en pakket vare er en underordnet vare.</span><span class="sxs-lookup"><span data-stu-id="fdd4a-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="fdd4a-106">Forholdet mellem bulkvaren og den pakkede vares udtrykkes i en konvertering af bulkvare.</span><span class="sxs-lookup"><span data-stu-id="fdd4a-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="fdd4a-107">Denne konvertering af bulkvare er defineret i selve bulkvaren.</span><span class="sxs-lookup"><span data-stu-id="fdd4a-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="fdd4a-108">Pakkede varer kan være pakket i enten containere i enkeltstørrelse eller flere størrelser, der betragtes som en samlet enhed.</span><span class="sxs-lookup"><span data-stu-id="fdd4a-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="fdd4a-109">Ved at konsolidere ordrer for en bulkvare, kan du se alle de relaterede batchordrer i en enkel visning, der kan hjælpe dig med at fastslå, om der er udestående opgaver, der skal fuldføres.</span><span class="sxs-lookup"><span data-stu-id="fdd4a-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="fdd4a-110">En konsolideret batchordre kan indeholde enhver kombination af følgende ordrer:</span><span class="sxs-lookup"><span data-stu-id="fdd4a-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="fdd4a-111">En enkelt bulkordre og flere pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="fdd4a-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="fdd4a-112">Flere bulkordrer og flere pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="fdd4a-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="fdd4a-113">Flere bulkordrer og en enkelt pakket ordre</span><span class="sxs-lookup"><span data-stu-id="fdd4a-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="fdd4a-114">Kun pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="fdd4a-114">Only packed orders</span></span>




