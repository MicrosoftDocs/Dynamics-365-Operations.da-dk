---
title: Vedligehold rute for en produktmodel
description: Kørsel af denne procedure kræver, at der findes en model til produktkonfiguration.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921259"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="62816-103">Vedligehold rute for en produktmodel</span><span class="sxs-lookup"><span data-stu-id="62816-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="62816-104">Kørsel af denne procedure kræver, at der findes en model til produktkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="62816-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="62816-105">Denne procedure bruger modellen Højttaler af topkvalitet i demofirmaet USMF til at føre dig gennem processen.</span><span class="sxs-lookup"><span data-stu-id="62816-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="62816-106">Tilføj en ruteoperation</span><span class="sxs-lookup"><span data-stu-id="62816-106">Add a route operation</span></span>

1. <span data-ttu-id="62816-107">Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.</span><span class="sxs-lookup"><span data-stu-id="62816-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="62816-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="62816-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="62816-109">Vælg modellen Højttaler af topkvalitet til denne øvelse.</span><span class="sxs-lookup"><span data-stu-id="62816-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="62816-110">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="62816-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="62816-111">Udvid sektionen **Ruteoperationer**.</span><span class="sxs-lookup"><span data-stu-id="62816-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="62816-112">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="62816-112">Select **Add**.</span></span>
1. <span data-ttu-id="62816-113">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="62816-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="62816-114">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="62816-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="62816-115">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="62816-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="62816-116">Angiv oplysninger om ruteoperation</span><span class="sxs-lookup"><span data-stu-id="62816-116">Enter route operation details</span></span>

1. <span data-ttu-id="62816-117">Vælg **Oplysninger om ruteoperation**.</span><span class="sxs-lookup"><span data-stu-id="62816-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="62816-118">Indtast eller vælg en værdi i feltet **Operation**.</span><span class="sxs-lookup"><span data-stu-id="62816-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="62816-119">I feltet **Oper.nr.**</span><span class="sxs-lookup"><span data-stu-id="62816-119">In the **Oper. No.**</span></span> <span data-ttu-id="62816-120">skal du angive et tal.</span><span class="sxs-lookup"><span data-stu-id="62816-120">field, enter a number.</span></span>
    * <span data-ttu-id="62816-121">Operationsnumre bestemmer ruteforløbet.</span><span class="sxs-lookup"><span data-stu-id="62816-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="62816-122">Hver egenskab for en ruteoperation kan få en statisk værdi eller kan knyttes til en attribut.</span><span class="sxs-lookup"><span data-stu-id="62816-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="62816-123">Tilknytning til en attribut medfører, at værdien angives som en del af konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="62816-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="62816-124">Indtast eller vælg en værdi i feltet **Rutegruppe**.</span><span class="sxs-lookup"><span data-stu-id="62816-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="62816-125">Rutegruppen afgør den væsentlige funktionsmåde i forbindelse med efterkalkulation, forbrug og installation.</span><span class="sxs-lookup"><span data-stu-id="62816-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="62816-126">Vælg fanen **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="62816-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="62816-127">Vælg fanen **Tider**.</span><span class="sxs-lookup"><span data-stu-id="62816-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="62816-128">Indtast et tal i feltet **Behandlingsantal**.</span><span class="sxs-lookup"><span data-stu-id="62816-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="62816-129">Bestem, hvor mange der vil blive behandlet under én handling.</span><span class="sxs-lookup"><span data-stu-id="62816-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="62816-130">Indtast et tal i feltet **Timer/tid**.</span><span class="sxs-lookup"><span data-stu-id="62816-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="62816-131">Indtast tidsforholdet.</span><span class="sxs-lookup"><span data-stu-id="62816-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="62816-132">Marker afkrydsningsfeltet **Indstil**.</span><span class="sxs-lookup"><span data-stu-id="62816-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="62816-133">Indtast et tal i feltet **Kørselstid**.</span><span class="sxs-lookup"><span data-stu-id="62816-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="62816-134">Bestemme behandlingstiden for den mængde, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="62816-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="62816-135">Vælg fanen **Ressourcebehov**.</span><span class="sxs-lookup"><span data-stu-id="62816-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="62816-136">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="62816-136">Select **Add**.</span></span>
1. <span data-ttu-id="62816-137">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="62816-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="62816-138">Vælg en indstilling i feltet **Kravtype**.</span><span class="sxs-lookup"><span data-stu-id="62816-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="62816-139">Beslut, om du vil angive bestemte ressourcer eller egenskaber, som de skal have.</span><span class="sxs-lookup"><span data-stu-id="62816-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="62816-140">Indtast eller vælg en værdi i feltet **Krav**.</span><span class="sxs-lookup"><span data-stu-id="62816-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="62816-141">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="62816-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]