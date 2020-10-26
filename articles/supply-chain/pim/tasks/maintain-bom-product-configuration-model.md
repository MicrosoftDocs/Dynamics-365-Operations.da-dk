---
title: Vedligeholde styklisten for en produktkonfigurationsmodel
description: Kørsel af denne procedure kræver en eksisterende model til produktkonfiguration.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcdf4b735587b76b7f761f59c56da1ca358a2e37
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985311"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="79858-103">Vedligeholde styklisten for en produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="79858-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="79858-104">Kørsel af denne procedure kræver en eksisterende model til produktkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="79858-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="79858-105">Højttaler af topkvalitet-modellen i demofirmaet USMF bruges til at oprette denne procedure.</span><span class="sxs-lookup"><span data-stu-id="79858-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="79858-106">Tilføj en styklistelinje</span><span class="sxs-lookup"><span data-stu-id="79858-106">Add a BOM line</span></span>
1. <span data-ttu-id="79858-107">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="79858-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="79858-108">Klik på Produktkonfigurationsmodeller.</span><span class="sxs-lookup"><span data-stu-id="79858-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="79858-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="79858-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="79858-110">Vælg Højttaler af topkvalitet for denne procedure.</span><span class="sxs-lookup"><span data-stu-id="79858-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="79858-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="79858-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="79858-112">Udvid afsnittet Styklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="79858-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="79858-113">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="79858-113">Click Add.</span></span>
7. <span data-ttu-id="79858-114">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="79858-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="79858-115">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="79858-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="79858-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="79858-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="79858-117">Tilføj Linjedetaljer i stykliste</span><span class="sxs-lookup"><span data-stu-id="79858-117">Add BOM line details</span></span>
1. <span data-ttu-id="79858-118">Klik på Linjedetaljer i stykliste.</span><span class="sxs-lookup"><span data-stu-id="79858-118">Click BOM line details.</span></span>
2. <span data-ttu-id="79858-119">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="79858-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="79858-120">Du kan f.eks. vælge elementet M0055.</span><span class="sxs-lookup"><span data-stu-id="79858-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="79858-121">For hver stykliste linjeegenskab kan du vælge, om den har en fast værdi eller er knyttet til en attribut.</span><span class="sxs-lookup"><span data-stu-id="79858-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="79858-122">Marker afkrydsningsfeltet Indstil.</span><span class="sxs-lookup"><span data-stu-id="79858-122">Select the Set check box.</span></span>
4. <span data-ttu-id="79858-123">Vælg Ja i feltet Beregning.</span><span class="sxs-lookup"><span data-stu-id="79858-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="79858-124">Når du indstiller egenskaben Beregning til Ja sikrer du, at styklistelinjen medtages i omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="79858-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="79858-125">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="79858-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="79858-126">Marker afkrydsningsfeltet Indstil.</span><span class="sxs-lookup"><span data-stu-id="79858-126">Select the Set check box.</span></span>
7. <span data-ttu-id="79858-127">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="79858-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="79858-128">Antalsfeltet bestemmer, hvor meget af elementet, der skal medtages i styklisten.</span><span class="sxs-lookup"><span data-stu-id="79858-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="79858-129">Dette kunne være en oplagt kandidat til en attributtilknytning.</span><span class="sxs-lookup"><span data-stu-id="79858-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="79858-130">Klik på fanen Dimension.</span><span class="sxs-lookup"><span data-stu-id="79858-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="79858-131">Kontroller, hvis nogen af produktdimensionerne er aktive og derfor skal have en værdi eller en attribut tildelt.</span><span class="sxs-lookup"><span data-stu-id="79858-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="79858-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="79858-132">Click OK.</span></span>

