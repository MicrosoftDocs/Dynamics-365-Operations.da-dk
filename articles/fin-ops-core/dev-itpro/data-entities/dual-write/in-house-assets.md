---
title: Interne aktiver til service
description: Dette emne beskriver, hvordan du kan bruge Microsoft Dynamics 365 Field Service til at servicere både kundeaktiver og interne aktiver.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: ebda6b5679ec601513fb6d046725b396e69fe0f3
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941408"
---
# <a name="in-house-assets-for-servicing"></a>Interne aktiver til service

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service er designet til at servicere kundeaktiver. Aktivadministration til Dynamics 365 Supply Chain Management er designet til at vedligeholde interne aktiver. Integrationen af disse to apps giver dig mulighed for at bruge Field Service til at servicere kundeaktiver og interne aktiver. Du kan også klassificere aktiverne ud fra funktionel placering eller hierarki og spore serviceringen på et detaljeret niveau.

Du kan finde yderligere oplysninger i [Integrer Dynamics 365 Field Service og Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Skabeloner

Interne aktiver indeholder en samling af centrale tabeltilknytninger, der arbejder sammen under datainteraktion, som vist i følgende tabel.

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]