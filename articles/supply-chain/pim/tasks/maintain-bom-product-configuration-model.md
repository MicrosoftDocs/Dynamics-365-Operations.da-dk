---
title: Vedligeholde styklisten for en produktkonfigurationsmodel
description: Kørsel af denne procedure kræver en eksisterende model til produktkonfiguration.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921311"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="78663-103">Vedligeholde styklisten for en produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="78663-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78663-104">Kørsel af denne procedure kræver en eksisterende model til produktkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="78663-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="78663-105">Højttaler af topkvalitet-modellen i demofirmaet USMF bruges til at oprette denne procedure.</span><span class="sxs-lookup"><span data-stu-id="78663-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>

## <a name="add-a-bom-line"></a><span data-ttu-id="78663-106">Tilføj en styklistelinje</span><span class="sxs-lookup"><span data-stu-id="78663-106">Add a BOM line</span></span>

1. <span data-ttu-id="78663-107">Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.</span><span class="sxs-lookup"><span data-stu-id="78663-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="78663-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="78663-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="78663-109">Vælg Højttaler af topkvalitet for denne procedure.</span><span class="sxs-lookup"><span data-stu-id="78663-109">Select the High end speaker for this procedure.</span></span>  
1. <span data-ttu-id="78663-110">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="78663-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="78663-111">Udvid sektionen **Styklistelinjer**.</span><span class="sxs-lookup"><span data-stu-id="78663-111">Expand the **BOM lines** section.</span></span>
1. <span data-ttu-id="78663-112">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="78663-112">Select **Add**.</span></span>
1. <span data-ttu-id="78663-113">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="78663-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="78663-114">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="78663-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="78663-115">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="78663-115">Select **Save**.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="78663-116">Tilføj Linjedetaljer i stykliste</span><span class="sxs-lookup"><span data-stu-id="78663-116">Add BOM line details</span></span>

1. <span data-ttu-id="78663-117">Vælg **Oplysninger om styklistelinjer**.</span><span class="sxs-lookup"><span data-stu-id="78663-117">Select **BOM line details**.</span></span>
2. <span data-ttu-id="78663-118">Indtast eller vælg en værdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="78663-118">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="78663-119">Du kan f.eks. vælge elementet M0055.</span><span class="sxs-lookup"><span data-stu-id="78663-119">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="78663-120">For hver stykliste linjeegenskab kan du vælge, om den har en fast værdi eller er knyttet til en attribut.</span><span class="sxs-lookup"><span data-stu-id="78663-120">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="78663-121">Marker afkrydsningsfeltet **Indstil**.</span><span class="sxs-lookup"><span data-stu-id="78663-121">Select the **Set** check box.</span></span>
4. <span data-ttu-id="78663-122">Vælg *Ja* i feltet **Beregning**.</span><span class="sxs-lookup"><span data-stu-id="78663-122">Select *Yes* in the **Calculation** field.</span></span>
    * <span data-ttu-id="78663-123">Når du indstiller egenskaben **Beregning** til *Ja*, sikrer du, at styklistelinjen medtages i omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="78663-123">Setting the **Calculation** property to *Yes* ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="78663-124">Vælg fanen **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="78663-124">Select the **Setup** tab.</span></span>
6. <span data-ttu-id="78663-125">Marker afkrydsningsfeltet **Indstil**.</span><span class="sxs-lookup"><span data-stu-id="78663-125">Select the **Set** check box.</span></span>
7. <span data-ttu-id="78663-126">Angiv et tal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="78663-126">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="78663-127">Antalsfeltet bestemmer, hvor meget af elementet, der skal medtages i styklisten.</span><span class="sxs-lookup"><span data-stu-id="78663-127">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="78663-128">Dette kunne være en oplagt kandidat til en attributtilknytning.</span><span class="sxs-lookup"><span data-stu-id="78663-128">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="78663-129">Vælg fanen **Dimension**.</span><span class="sxs-lookup"><span data-stu-id="78663-129">Select the **Dimension** tab.</span></span>
    * <span data-ttu-id="78663-130">Kontroller, hvis nogen af produktdimensionerne er aktive og derfor skal have en værdi eller en attribut tildelt.</span><span class="sxs-lookup"><span data-stu-id="78663-130">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="78663-131">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="78663-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]