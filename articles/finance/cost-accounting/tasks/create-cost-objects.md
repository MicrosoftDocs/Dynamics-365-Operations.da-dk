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
ms.openlocfilehash: f3d2ef7d6549bdeb3ba2afd2a594f36b47c912db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990761"
---
# <a name="create-cost-objects"></a><span data-ttu-id="deccf-103">Oprette omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="deccf-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="deccf-104">Denne fremgangsmåde viser, hvordan du opretter omkostningsobjekter ved at importere den økonomiske dimension af typen Bærer til omkostningsregnskabet via en dataconnector.</span><span class="sxs-lookup"><span data-stu-id="deccf-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="deccf-105">Demofirmaet USMF bruges til at oprette denne procedure.</span><span class="sxs-lookup"><span data-stu-id="deccf-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="deccf-106">Opret nye omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="deccf-106">Create new cost objects</span></span>
1. <span data-ttu-id="deccf-107">Gå til Omkostningsregnskab > Dimensioner > Dimensioner for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="deccf-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="deccf-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="deccf-108">Click New.</span></span>
3. <span data-ttu-id="deccf-109">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="deccf-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="deccf-110">Indtast eller vælg en værdi i feltet Dataconnector for dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="deccf-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="deccf-111">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="deccf-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="deccf-112">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="deccf-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="deccf-113">Konfigurer dataconnectoren</span><span class="sxs-lookup"><span data-stu-id="deccf-113">Configure the data connector</span></span>
1. <span data-ttu-id="deccf-114">Klik på Konfigurer leverandør af dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="deccf-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="deccf-115">Vælg CostCenter for at importere CostCenter-dimensionen til omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="deccf-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="deccf-116">Vælg Bærer i feltet Dimensionens navn.</span><span class="sxs-lookup"><span data-stu-id="deccf-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="deccf-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="deccf-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="deccf-118">Importér bærere</span><span class="sxs-lookup"><span data-stu-id="deccf-118">Import cost centers</span></span>
1. <span data-ttu-id="deccf-119">Klik på Importér dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="deccf-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="deccf-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="deccf-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="deccf-121">Få vist de importerede bærere</span><span class="sxs-lookup"><span data-stu-id="deccf-121">View the imported cost centers</span></span>
1. <span data-ttu-id="deccf-122">Klik på Vis dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="deccf-122">Click View dimension members.</span></span>

