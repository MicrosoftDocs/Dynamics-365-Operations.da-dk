--- 
title: Oprette omkostningsobjekter
description: "Denne procedure viser, hvordan du opretter omkostningsobjekter ved at importere den økonomiske Dynamics 365 for Finance and Operations-dimension af typen Bærer til omkostningsregnskabet via en dataconnector."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
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
ms.openlocfilehash: 2c76a26ea63d1fd44c20fbee271d2767b8ea68b1
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="830fd-103">Oprette omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="830fd-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="830fd-104">Denne procedure viser, hvordan du opretter omkostningsobjekter ved at importere den økonomiske Dynamics 365 for Finance and Operations-dimension af typen Bærer til omkostningsregnskabet via en dataconnector.</span><span class="sxs-lookup"><span data-stu-id="830fd-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="830fd-105">Demofirmaet USMF bruges til at oprette denne procedure.</span><span class="sxs-lookup"><span data-stu-id="830fd-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="830fd-106">Denne fremgangsmåde er til en Omkostningsregnskab-funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="830fd-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="830fd-107">Opret nye omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="830fd-107">Create new cost objects</span></span>
1. <span data-ttu-id="830fd-108">Gå til Omkostningsregnskab > Dimensioner > Dimensioner for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="830fd-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="830fd-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="830fd-109">Click New.</span></span>
3. <span data-ttu-id="830fd-110">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="830fd-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="830fd-111">Indtast eller vælg en værdi i feltet Dataconnector for dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="830fd-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="830fd-112">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="830fd-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="830fd-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="830fd-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="830fd-114">Konfigurer dataconnectoren</span><span class="sxs-lookup"><span data-stu-id="830fd-114">Configure the data connector</span></span>
1. <span data-ttu-id="830fd-115">Klik på Konfigurer leverandør af dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="830fd-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="830fd-116">Vælg CostCenter for at importere CostCenter-dimensionen til omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="830fd-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="830fd-117">Vælg Bærer i feltet Dimensionens navn.</span><span class="sxs-lookup"><span data-stu-id="830fd-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="830fd-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="830fd-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="830fd-119">Importér bærere</span><span class="sxs-lookup"><span data-stu-id="830fd-119">Import cost centers</span></span>
1. <span data-ttu-id="830fd-120">Klik på Importér dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="830fd-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="830fd-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="830fd-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="830fd-122">Få vist de importerede bærere</span><span class="sxs-lookup"><span data-stu-id="830fd-122">View the imported cost centers</span></span>
1. <span data-ttu-id="830fd-123">Klik på Vis dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="830fd-123">Click View dimension members.</span></span>


