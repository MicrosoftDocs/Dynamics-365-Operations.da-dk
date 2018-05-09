--- 
title: "Tilføje en beregning til en produktkonfigurationsmodel"
description: "Denne procedure viser, hvordan du kan føje en ny beregning til en produktkonfigurationsmodel."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 123ae1315c95693af09d7d7c96a071d606ac98f8
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="48d92-103">Tilføje en beregning til en produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="48d92-103">Add a calculation to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48d92-104">Denne procedure viser, hvordan du kan føje en ny beregning til en produktkonfigurationsmodel.</span><span class="sxs-lookup"><span data-stu-id="48d92-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="48d92-105">Den viser, hvordan du kan oprette et logisk udtryk ved at bruge operatoren "Hvis" til at indstille en højttalerhøjde til 10 for hvide højttalere og 15 til ethvert andet kabinetfinish.</span><span class="sxs-lookup"><span data-stu-id="48d92-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="48d92-106">Proceduren bruger komponenten Højttaler af topkvalitet i demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="48d92-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="48d92-107">Tilføje en beregning</span><span class="sxs-lookup"><span data-stu-id="48d92-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="48d92-108">Oprette et beregningsudtryk</span><span class="sxs-lookup"><span data-stu-id="48d92-108">Create calculation expression</span></span>
1. <span data-ttu-id="48d92-109">Klik på udtrykket Rediger.</span><span class="sxs-lookup"><span data-stu-id="48d92-109">Click Edit expression.</span></span>
2. <span data-ttu-id="48d92-110">I feltet ConstraintBody skal du angive 'If[CabinetFinish == "Hvid", 10, 15]'.</span><span class="sxs-lookup"><span data-stu-id="48d92-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="48d92-111">Klik på Valider.</span><span class="sxs-lookup"><span data-stu-id="48d92-111">Click Validate.</span></span>
4. <span data-ttu-id="48d92-112">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="48d92-112">Click Close.</span></span>
5. <span data-ttu-id="48d92-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="48d92-113">Click OK.</span></span>


