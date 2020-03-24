---
title: Interne aktiver til service
description: I dette emne beskrives, hvordan du kan bruge Microsoft Dynamics 365 Field Service til at servicere kundeaktiver og interne aktiver.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: d931811e9fbea3c10f83b048a3c3fbeda5396d39
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112411"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="6308d-103">Interne aktiver til service</span><span class="sxs-lookup"><span data-stu-id="6308d-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6308d-104">Microsoft Dynamics 365 Field Service er designet til at servicere kundeaktiver.</span><span class="sxs-lookup"><span data-stu-id="6308d-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="6308d-105">Aktivadministration til Dynamics 365 Supply Chain Management er designet til at vedligeholde interne aktiver.</span><span class="sxs-lookup"><span data-stu-id="6308d-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="6308d-106">Integrationen af disse to apps giver dig mulighed for at bruge Field Service til at servicere kundeaktiver og interne aktiver.</span><span class="sxs-lookup"><span data-stu-id="6308d-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="6308d-107">Du kan også klassificere aktiverne ud fra funktionel placering eller hierarki og spore serviceringen på et detaljeret niveau.</span><span class="sxs-lookup"><span data-stu-id="6308d-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="6308d-108">Du kan finde yderligere oplysninger i [Integrer Dynamics 365 Field Service og Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="6308d-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="6308d-109">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="6308d-109">Templates</span></span>

<span data-ttu-id="6308d-110">Interne aktiver indeholder en samling af centrale enhedstilknytninger, der arbejder sammen under datainteraktion, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="6308d-110">In-house-assets include a collection of core entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="6308d-111">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="6308d-111">Finance and Operations apps</span></span> | <span data-ttu-id="6308d-112">Modelstyrede apps i Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6308d-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="6308d-113">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="6308d-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="6308d-114">Aktivlivscyklusmodeller i Aktivadministration</span><span class="sxs-lookup"><span data-stu-id="6308d-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="6308d-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="6308d-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="6308d-116">Aktivlivscyklustilstande i Aktivadministration</span><span class="sxs-lookup"><span data-stu-id="6308d-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="6308d-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="6308d-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="6308d-118">Aktiver i Aktivadministration</span><span class="sxs-lookup"><span data-stu-id="6308d-118">Asset management assets</span></span> | <span data-ttu-id="6308d-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="6308d-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="6308d-120">Aktivtyper i Aktivadministration</span><span class="sxs-lookup"><span data-stu-id="6308d-120">Asset management asset types</span></span> | <span data-ttu-id="6308d-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="6308d-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="6308d-122">Livcyklusmodeller til funktionel placering i Aktivadministration</span><span class="sxs-lookup"><span data-stu-id="6308d-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="6308d-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="6308d-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="6308d-124">Livcyklustilstande til funktionel placering i Aktivadministration</span><span class="sxs-lookup"><span data-stu-id="6308d-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="6308d-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="6308d-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="6308d-126">Funktionelle placeringer i Aktivadministration</span><span class="sxs-lookup"><span data-stu-id="6308d-126">Asset management functional locations</span></span> | <span data-ttu-id="6308d-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="6308d-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="6308d-128">Funktionelle placeringstyper i Aktivadministration</span><span class="sxs-lookup"><span data-stu-id="6308d-128">Asset management functional location types</span></span> | <span data-ttu-id="6308d-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="6308d-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="6308d-130">Producenter i Aktivadministration</span><span class="sxs-lookup"><span data-stu-id="6308d-130">Asset management manufacturers</span></span> | <span data-ttu-id="6308d-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="6308d-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="6308d-132">Modeller i Aktivadministration</span><span class="sxs-lookup"><span data-stu-id="6308d-132">Asset management models</span></span> | <span data-ttu-id="6308d-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="6308d-133">msdyn\_models</span></span> | |
| <span data-ttu-id="6308d-134">Garanti af Aktivadministration</span><span class="sxs-lookup"><span data-stu-id="6308d-134">Asset management warranty</span></span> | <span data-ttu-id="6308d-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="6308d-135">msdyn\_warranties</span></span> | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]
