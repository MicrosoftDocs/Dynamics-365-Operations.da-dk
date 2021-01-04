---
title: Oprette omkostningsobjekter
description: Denne fremgangsmåde viser, hvordan du opretter omkostningsobjekter ved at importere den økonomiske dimension af typen Bærer til omkostningsregnskabet via en dataconnector.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55f5f6e5048f70e744cb3dc82a2a279aae69b4af
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441695"
---
# <a name="create-cost-objects"></a><span data-ttu-id="ce8bc-103">Oprette omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="ce8bc-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ce8bc-104">Denne fremgangsmåde viser, hvordan du opretter omkostningsobjekter ved at importere den økonomiske dimension af typen Bærer til omkostningsregnskabet via en dataconnector.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="ce8bc-105">Demofirmaet USMF bruges til at oprette denne procedure.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="ce8bc-106">Opret nye omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="ce8bc-106">Create new cost objects</span></span>
1. <span data-ttu-id="ce8bc-107">Gå til Omkostningsregnskab > Dimensioner > Dimensioner for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="ce8bc-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-108">Click New.</span></span>
3. <span data-ttu-id="ce8bc-109">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ce8bc-110">Indtast eller vælg en værdi i feltet Dataconnector for dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="ce8bc-111">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="ce8bc-112">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="ce8bc-113">Konfigurer dataconnectoren</span><span class="sxs-lookup"><span data-stu-id="ce8bc-113">Configure the data connector</span></span>
1. <span data-ttu-id="ce8bc-114">Klik på Konfigurer leverandør af dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="ce8bc-115">Vælg CostCenter for at importere CostCenter-dimensionen til omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="ce8bc-116">Vælg Bærer i feltet Dimensionens navn.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="ce8bc-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="ce8bc-118">Importér bærere</span><span class="sxs-lookup"><span data-stu-id="ce8bc-118">Import cost centers</span></span>
1. <span data-ttu-id="ce8bc-119">Klik på Importér dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="ce8bc-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="ce8bc-121">Få vist de importerede bærere</span><span class="sxs-lookup"><span data-stu-id="ce8bc-121">View the imported cost centers</span></span>
1. <span data-ttu-id="ce8bc-122">Klik på Vis dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-122">Click View dimension members.</span></span>

