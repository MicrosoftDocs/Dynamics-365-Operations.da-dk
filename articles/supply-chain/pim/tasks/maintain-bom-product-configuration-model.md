--- 
title: Vedligeholde styklisten for en produktkonfigurationsmodel
description: "Kørsel af denne procedure kræver en eksisterende model til produktkonfiguration."
author: ShylaThompson
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 9c83b5a100ba039701137eb93ecf3ae5c5d36adc
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="54995-103">Vedligeholde styklisten for en produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="54995-103">Maintain BOM for a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54995-104">Kørsel af denne procedure kræver en eksisterende model til produktkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="54995-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="54995-105">Højttaler af topkvalitet-modellen i demofirmaet USMF bruges til at oprette denne procedure.</span><span class="sxs-lookup"><span data-stu-id="54995-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="54995-106">Tilføj en styklistelinje</span><span class="sxs-lookup"><span data-stu-id="54995-106">Add a BOM line</span></span>
1. <span data-ttu-id="54995-107">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="54995-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="54995-108">Klik på Produktkonfigurationsmodeller.</span><span class="sxs-lookup"><span data-stu-id="54995-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="54995-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="54995-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="54995-110">Vælg Højttaler af topkvalitet for denne procedure.</span><span class="sxs-lookup"><span data-stu-id="54995-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="54995-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="54995-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="54995-112">Udvid afsnittet Styklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="54995-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="54995-113">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="54995-113">Click Add.</span></span>
7. <span data-ttu-id="54995-114">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="54995-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="54995-115">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="54995-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="54995-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="54995-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="54995-117">Tilføj Linjedetaljer i stykliste</span><span class="sxs-lookup"><span data-stu-id="54995-117">Add BOM line details</span></span>
1. <span data-ttu-id="54995-118">Klik på Linjedetaljer i stykliste.</span><span class="sxs-lookup"><span data-stu-id="54995-118">Click BOM line details.</span></span>
2. <span data-ttu-id="54995-119">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="54995-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="54995-120">Du kan f.eks. vælge elementet M0055.</span><span class="sxs-lookup"><span data-stu-id="54995-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="54995-121">For hver stykliste linjeegenskab kan du vælge, om den har en fast værdi eller er knyttet til en attribut.</span><span class="sxs-lookup"><span data-stu-id="54995-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="54995-122">Marker afkrydsningsfeltet Indstil.</span><span class="sxs-lookup"><span data-stu-id="54995-122">Select the Set check box.</span></span>
4. <span data-ttu-id="54995-123">Vælg Ja i feltet Beregning.</span><span class="sxs-lookup"><span data-stu-id="54995-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="54995-124">Når du indstiller egenskaben Beregning til Ja sikrer du, at styklistelinjen medtages i omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="54995-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="54995-125">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="54995-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="54995-126">Marker afkrydsningsfeltet Indstil.</span><span class="sxs-lookup"><span data-stu-id="54995-126">Select the Set check box.</span></span>
7. <span data-ttu-id="54995-127">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="54995-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="54995-128">Antalsfeltet bestemmer, hvor meget af elementet, der skal medtages i styklisten.</span><span class="sxs-lookup"><span data-stu-id="54995-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="54995-129">Dette kunne være en oplagt kandidat til en attributtilknytning.</span><span class="sxs-lookup"><span data-stu-id="54995-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="54995-130">Klik på fanen Dimension.</span><span class="sxs-lookup"><span data-stu-id="54995-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="54995-131">Kontroller, hvis nogen af produktdimensionerne er aktive og derfor skal have en værdi eller en attribut tildelt.</span><span class="sxs-lookup"><span data-stu-id="54995-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="54995-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="54995-132">Click OK.</span></span>


