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
# <a name="in-house-assets-for-servicing"></a>Interne aktiver til service

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Microsoft Dynamics 365 Field Service er designet til at servicere kundeaktiver. Aktivadministration til Dynamics 365 Supply Chain Management er designet til at vedligeholde interne aktiver. Integrationen af disse to apps giver dig mulighed for at bruge Field Service til at servicere kundeaktiver og interne aktiver. Du kan også klassificere aktiverne ud fra funktionel placering eller hierarki og spore serviceringen på et detaljeret niveau.

Du kan finde yderligere oplysninger i [Integrer Dynamics 365 Field Service og Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Skabeloner

Interne aktiver indeholder en samling af centrale enhedstilknytninger, der arbejder sammen under datainteraktion, som vist i følgende tabel.

| Finance and Operations-apps | Modelstyrede apps i Dynamics 365 | Beskrivende tekst |
|-----------------------------|-----------------------------------|-------------|
| Aktivlivscyklusmodeller i Aktivadministration | msdyn\_assetlifecyclemodels | |
| Aktivlivscyklustilstande i Aktivadministration | msdyn\_assetlifecyclestates | |
| Aktiver i Aktivadministration | msdyn\_customerassets | |
| Aktivtyper i Aktivadministration | msdyn\_customerassetcategories | |
| Livcyklusmodeller til funktionel placering i Aktivadministration | msdyn\_functionallocationlifecyclemodels | |
| Livcyklustilstande til funktionel placering i Aktivadministration | msdyn\_functionallocationlifecyclestates | |
| Funktionelle placeringer i Aktivadministration | msdyn\_functionallocations | |
| Funktionelle placeringstyper i Aktivadministration | msdyn\_functionallocationtypes | |
| Producenter i Aktivadministration | msdyn\_manufacturers | |
| Modeller i Aktivadministration | msdyn\_models | |
| Garanti af Aktivadministration | msdyn\_warranties | |

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