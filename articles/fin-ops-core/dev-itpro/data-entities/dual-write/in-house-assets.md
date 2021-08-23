---
title: Interne aktiver til service
description: Dette emne beskriver, hvordan du kan bruge Microsoft Dynamics 365 Field Service til at servicere både kundeaktiver og interne aktiver.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 0700025288bda1b2c67cc3ff26dc2e737216a5f8f5265464c6c62d9cb890b580
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742304"
---
# <a name="in-house-assets-for-servicing"></a>Interne aktiver til service

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Field Service er designet til at servicere kundeaktiver. Aktivadministration til Dynamics 365 Supply Chain Management er designet til at vedligeholde interne aktiver. Integrationen af disse to apps giver dig mulighed for at bruge Field Service til at servicere kundeaktiver og interne aktiver. Du kan også klassificere aktiverne ud fra funktionel placering eller hierarki og spore serviceringen på et detaljeret niveau.

Du kan finde yderligere oplysninger i [Integrer Dynamics 365 Field Service og Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Skabeloner

Interne aktiver indeholder en samling af centrale tabeltilknytninger, der arbejder sammen under datainteraktion, som vist i følgende tabel.

| Finance and Operations-apps | Kundeengagementapps | Betegnelse |
|-----------------------------|-----------------------------------|-------------|
[Aktivlivscyklusmodeller i Aktivadministration](mapping-reference.md#119) | msdyn_assetlifecyclemodels | |
[Aktivlivscyklustilstande i Aktivadministration](mapping-reference.md#120) | msdyn_assetlifecyclestates | |
[Aktivtyper i Aktivadministration](mapping-reference.md#124) | msdyn_customerassetcategories | |
[Aktiver i Aktivadministration](mapping-reference.md#125) | msdyn_customerassets | |
[Livcyklusmodeller til funktionel placering i Aktivadministration](mapping-reference.md#134) | msdyn_functionallocationlifecyclemodels | |
[Livcyklustilstande til funktionel placering i Aktivadministration](mapping-reference.md#135) | msdyn_functionallocationlifecyclestates | |
[Funktionelle placeringstyper i Aktivadministration](mapping-reference.md#137) | msdyn_functionallocationtypes | |
[Funktionelle placeringer i Aktivadministration](mapping-reference.md#136) | msdyn_functionallocations | |
[Producenter i Aktivadministration](mapping-reference.md#153) | msdyn_manufacturers | |
[Modeller i Aktivadministration](mapping-reference.md#154) | msdyn_models | |
[Garanti af Aktivadministration](mapping-reference.md#209) | msdyn_warranties | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
