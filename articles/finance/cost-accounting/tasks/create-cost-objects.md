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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91c25c52a2c6dc7f096a494577b361ff30406e9c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236788"
---
# <a name="create-cost-objects"></a><span data-ttu-id="e16cb-103">Oprette omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="e16cb-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e16cb-104">Denne fremgangsmåde viser, hvordan du opretter omkostningsobjekter ved at importere den økonomiske dimension af typen Bærer til omkostningsregnskabet via en dataconnector.</span><span class="sxs-lookup"><span data-stu-id="e16cb-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="e16cb-105">Demofirmaet USMF bruges til at oprette denne procedure.</span><span class="sxs-lookup"><span data-stu-id="e16cb-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="e16cb-106">Opret nye omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="e16cb-106">Create new cost objects</span></span>
1. <span data-ttu-id="e16cb-107">Gå til Omkostningsregnskab > Dimensioner > Dimensioner for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="e16cb-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="e16cb-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e16cb-108">Click New.</span></span>
3. <span data-ttu-id="e16cb-109">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e16cb-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e16cb-110">Indtast eller vælg en værdi i feltet Dataconnector for dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="e16cb-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="e16cb-111">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e16cb-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="e16cb-112">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e16cb-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="e16cb-113">Konfigurer dataconnectoren</span><span class="sxs-lookup"><span data-stu-id="e16cb-113">Configure the data connector</span></span>
1. <span data-ttu-id="e16cb-114">Klik på Konfigurer leverandør af dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="e16cb-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="e16cb-115">Vælg CostCenter for at importere CostCenter-dimensionen til omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="e16cb-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="e16cb-116">Vælg Bærer i feltet Dimensionens navn.</span><span class="sxs-lookup"><span data-stu-id="e16cb-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="e16cb-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e16cb-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="e16cb-118">Importér bærere</span><span class="sxs-lookup"><span data-stu-id="e16cb-118">Import cost centers</span></span>
1. <span data-ttu-id="e16cb-119">Klik på Importér dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="e16cb-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="e16cb-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e16cb-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="e16cb-121">Få vist de importerede bærere</span><span class="sxs-lookup"><span data-stu-id="e16cb-121">View the imported cost centers</span></span>
1. <span data-ttu-id="e16cb-122">Klik på Vis dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="e16cb-122">Click View dimension members.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]