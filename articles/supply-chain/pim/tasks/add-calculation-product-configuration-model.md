---
title: Tilføje en beregning til en produktkonfigurationsmodel
description: Denne procedure viser, hvordan du kan føje en ny beregning til en produktkonfigurationsmodel.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e703c6d505f1e2e77f454732301de7a6c130c58a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986497"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="6963b-103">Tilføje en beregning til en produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="6963b-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6963b-104">Denne procedure viser, hvordan du kan føje en ny beregning til en produktkonfigurationsmodel.</span><span class="sxs-lookup"><span data-stu-id="6963b-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="6963b-105">Den viser, hvordan du kan oprette et logisk udtryk ved at bruge operatoren "Hvis" til at indstille en højttalerhøjde til 10 for hvide højttalere og 15 til ethvert andet kabinetfinish.</span><span class="sxs-lookup"><span data-stu-id="6963b-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="6963b-106">Proceduren bruger komponenten Højttaler af topkvalitet i demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="6963b-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="6963b-107">Tilføje en beregning</span><span class="sxs-lookup"><span data-stu-id="6963b-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="6963b-108">Oprette et beregningsudtryk</span><span class="sxs-lookup"><span data-stu-id="6963b-108">Create calculation expression</span></span>
1. <span data-ttu-id="6963b-109">Klik på udtrykket Rediger.</span><span class="sxs-lookup"><span data-stu-id="6963b-109">Click Edit expression.</span></span>
2. <span data-ttu-id="6963b-110">I feltet ConstraintBody skal du angive 'If[CabinetFinish == "Hvid", 10, 15]'.</span><span class="sxs-lookup"><span data-stu-id="6963b-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="6963b-111">Klik på Valider.</span><span class="sxs-lookup"><span data-stu-id="6963b-111">Click Validate.</span></span>
4. <span data-ttu-id="6963b-112">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="6963b-112">Click Close.</span></span>
5. <span data-ttu-id="6963b-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6963b-113">Click OK.</span></span>

