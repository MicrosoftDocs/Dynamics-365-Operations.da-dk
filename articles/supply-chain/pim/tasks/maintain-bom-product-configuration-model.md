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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12eb2d8fcdae5d60efa19e5443a01ab9bd104267
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258797"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="741d0-103">Vedligeholde styklisten for en produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="741d0-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="741d0-104">Kørsel af denne procedure kræver en eksisterende model til produktkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="741d0-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="741d0-105">Højttaler af topkvalitet-modellen i demofirmaet USMF bruges til at oprette denne procedure.</span><span class="sxs-lookup"><span data-stu-id="741d0-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="741d0-106">Tilføj en styklistelinje</span><span class="sxs-lookup"><span data-stu-id="741d0-106">Add a BOM line</span></span>
1. <span data-ttu-id="741d0-107">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="741d0-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="741d0-108">Klik på Produktkonfigurationsmodeller.</span><span class="sxs-lookup"><span data-stu-id="741d0-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="741d0-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="741d0-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="741d0-110">Vælg Højttaler af topkvalitet for denne procedure.</span><span class="sxs-lookup"><span data-stu-id="741d0-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="741d0-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="741d0-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="741d0-112">Udvid afsnittet Styklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="741d0-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="741d0-113">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="741d0-113">Click Add.</span></span>
7. <span data-ttu-id="741d0-114">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="741d0-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="741d0-115">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="741d0-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="741d0-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="741d0-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="741d0-117">Tilføj Linjedetaljer i stykliste</span><span class="sxs-lookup"><span data-stu-id="741d0-117">Add BOM line details</span></span>
1. <span data-ttu-id="741d0-118">Klik på Linjedetaljer i stykliste.</span><span class="sxs-lookup"><span data-stu-id="741d0-118">Click BOM line details.</span></span>
2. <span data-ttu-id="741d0-119">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="741d0-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="741d0-120">Du kan f.eks. vælge elementet M0055.</span><span class="sxs-lookup"><span data-stu-id="741d0-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="741d0-121">For hver stykliste linjeegenskab kan du vælge, om den har en fast værdi eller er knyttet til en attribut.</span><span class="sxs-lookup"><span data-stu-id="741d0-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="741d0-122">Marker afkrydsningsfeltet Indstil.</span><span class="sxs-lookup"><span data-stu-id="741d0-122">Select the Set check box.</span></span>
4. <span data-ttu-id="741d0-123">Vælg Ja i feltet Beregning.</span><span class="sxs-lookup"><span data-stu-id="741d0-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="741d0-124">Når du indstiller egenskaben Beregning til Ja sikrer du, at styklistelinjen medtages i omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="741d0-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="741d0-125">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="741d0-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="741d0-126">Marker afkrydsningsfeltet Indstil.</span><span class="sxs-lookup"><span data-stu-id="741d0-126">Select the Set check box.</span></span>
7. <span data-ttu-id="741d0-127">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="741d0-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="741d0-128">Antalsfeltet bestemmer, hvor meget af elementet, der skal medtages i styklisten.</span><span class="sxs-lookup"><span data-stu-id="741d0-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="741d0-129">Dette kunne være en oplagt kandidat til en attributtilknytning.</span><span class="sxs-lookup"><span data-stu-id="741d0-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="741d0-130">Klik på fanen Dimension.</span><span class="sxs-lookup"><span data-stu-id="741d0-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="741d0-131">Kontroller, hvis nogen af produktdimensionerne er aktive og derfor skal have en værdi eller en attribut tildelt.</span><span class="sxs-lookup"><span data-stu-id="741d0-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="741d0-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="741d0-132">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]