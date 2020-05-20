---
title: Fjernede eller udfasede funktioner i Dynamics 365 Commerce
description: Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335270"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Fjernede eller udfasede funktioner i Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Commerce.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning. 

> [!NOTE]
> Du kan finde detaljerede oplysninger om objekter i Finance and Operations-apps i [Technical Reference-rapporterne](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finance and Operations-apps.

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Fjernede eller udfasede funktioner i Commerce 10.0.10-frigivelsen
### <a name="pos-operation-803---picking-and-receiving"></a>POS-operation 803 – pluk og tilgang
|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Pluk- og tilgangsoperationer frarådes på grund af nyt omdesign af operationerne. |
| **Erstattet af en anden funktion?**   | Ja. Det erstattes af to nye POS-operationer: indgående operation (804) og udgående operation (805).|
| **Produktområder, der er berørt**         | POS-program |
| **Installationsindstilling**              | Alt |
| **Status**                         | Frarådes: Fra og med version 10.0.10 modtager pluk- og tilgangsoperationer ikke længere nye funktionsforbedringer. Der udføres kun kritiske fejlrettelser for denne operation i fremtidige versioner. Alle kunder opfordres til at skifte til de nye [Indgående operationer](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) og [Udgående operationer](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), som fortsat vil være en del af vores langsigtede produktoversigt. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Fjernede eller udfasede funktioner i Commerce 10.0.7-frigivelsen
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities- og GetAvailableInventoryNearby-API'er
|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Nye optimerede API'er er oprettet for at erstatte GetProductAvailabilities- og GetAvailableInventoryNearby-API'erne. |
| **Erstattet af en anden funktion?**   | Ja: Det erstattes af GetEstimatedAvailability- og GetEstimatedProductWarehouseAvailability-API'er. |
| **Produktområder, der er berørt**         | SDK til e-handelsprogrammer |
| **Installationsindstilling**              | Alt |
| **Status**                         | Frarådes: Fra og med version 10.0.7 foretages der ikke længere tekniske investeringer for GetProductAvailabilities og GetAvailableInventoryNearby. Organisationer, der bruger disse API'er i deres e-handelsinstallationer, skal konvertere til de nye GetEstimatedAvailability- og GetEstimatedProductWarehouseAvailability-API'er og aktivere [funktionen Beregning af optimeret produkttilgængelighed](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere meddelelser om fjernede eller udfasede funktioner
Hvis du vil vide mere om funktioner, der er blevet fjernet eller udfaset i tidligere versioner, kan du se [Fjernede eller udfasede funktioner i tidligere versioner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).
