---
title: Tilknytte en dimension for omkostningselement
description: En omkostningscontroller kan bruge denne procedure til at knytte en dimension for et omkostningselement til en dimension for et omkostningselement i den juridiske enhed for MXMF.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52b9f6a5b71349d404fe9621b58f58aab843a71f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "308500"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="f0b64-103">Tilknytte en dimension for omkostningselement</span><span class="sxs-lookup"><span data-stu-id="f0b64-103">Map a cost element dimension</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0b64-104">En omkostningscontroller kan bruge denne procedure til at knytte en dimension for et omkostningselement til en dimension for et omkostningselement i den juridiske enhed for MXMF.</span><span class="sxs-lookup"><span data-stu-id="f0b64-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="f0b64-105">Denne registrering bruger USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="f0b64-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="f0b64-106">Gå til Omkostningsregnskab > Dimensioner > Dimensioner for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="f0b64-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="f0b64-107">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f0b64-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f0b64-108">Vælg Omkostningselementer i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="f0b64-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="f0b64-109">Klik på Tilknytninger af dimensioner.</span><span class="sxs-lookup"><span data-stu-id="f0b64-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="f0b64-110">Klik på Konfigurer tilknytninger fra denne dimension.</span><span class="sxs-lookup"><span data-stu-id="f0b64-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="f0b64-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f0b64-111">Click New.</span></span>
6. <span data-ttu-id="f0b64-112">Indtast eller vælg en værdi i feltet Til dimension.</span><span class="sxs-lookup"><span data-stu-id="f0b64-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="f0b64-113">Vælg MXMF-omkostningselementer i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="f0b64-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="f0b64-114">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f0b64-114">Click New.</span></span>
8. <span data-ttu-id="f0b64-115">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f0b64-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f0b64-116">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="f0b64-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="f0b64-117">I dette eksempel skal du vælge dimensionsmedlem 606400 Udgift til telefon og fax.</span><span class="sxs-lookup"><span data-stu-id="f0b64-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="f0b64-118">Indtast eller vælg en værdi i feltet Til dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="f0b64-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="f0b64-119">I dette eksempel skal du vælge dimensionsmedlem 6001004 Telefono.</span><span class="sxs-lookup"><span data-stu-id="f0b64-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="f0b64-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f0b64-120">Click Save.</span></span>

