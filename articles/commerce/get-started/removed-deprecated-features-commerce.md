---
title: Fjernede eller udfasede funktioner i Dynamics 365 Commerce
description: Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 07/07/2020
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
ms.openlocfilehash: aa18e7446a72a907fcad70f92ea529088b6cecbd
ms.sourcegitcommit: 83c7e5ab54c1cad2e21e33769cc524cfa4213f58
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/07/2020
ms.locfileid: "3539873"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Fjernede eller udfasede funktioner i Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Commerce.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning. 

> [!NOTE]
> Du kan finde detaljerede oplysninger om objekter i Finance and Operations-apps i [Technical Reference-rapporterne](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finance and Operations-apps.

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Fjernede eller udfasede funktioner i Commerce 10.0.11-frigivelsen
### <a name="data-action-hooks"></a>Datahandlings-hooks
|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Funktionen Datahandlings-hooks frarådes på grund af problemer med ydeevnen. |
| **Erstattet af en anden funktion?**   | Vi anbefaler at bruge [datahandlingstilsidesættelser](../e-commerce-extensibility/data-action-overrides.md) til at redigere forretningslogik i datahandlingslaget.|
| **Produktområder, der er berørt**         | Datahandlinger for udvidelse af e-handel |
| **Installationsindstilling**              | Alt |
| **Status**                         | Forældet fra og med version 10.0.11 |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Understøttelse af Retail SDK til Visual Studio 2015, msbuild 14,0 og Retail SDK\Reference-biblioteker og -værktøjer
|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Retail SDK-understøttelsen til Visual Studio 2015 er blevet udfaset og opdateret for at understøtte vs. 2017, msbuild 15,0 og alle referencebiblioteker og Commerce-proxygenerator-værktøjer i mappen RetailSDK\References er flyttet til NuGet-pakker for at forenkle udvidelsesmodellen og opgraderingsprocessen for SDK.|
| **Erstattet af en anden funktion?**   | Det anbefales, at du følger oplysningerne i [Overflytte Retail SDK data fra Visual Studio 2015 til Visual Studio 2017](../dev-itpro/retail-sdk/migrate-sdk.md) for at opdatere systemet. |
| **Produktområder, der er berørt**         | Retail SDK-udvidelser |
| **Installationsindstilling**              | Alt |
| **Status**                         | Forældet fra og med version 10.0.11 |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Retail-serverudvidelse ved hjælp af IEdmModelExtender og CommerceController
|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Retail-serverudvidelse ved hjælp af IEdmModelExtender og CommerceController er blevet udfaset for at levere en forenklet udvidelsesmodel. Den nye implementering vil kun have controller-klassen uden yderligere IEdmModelExtender-klasseimplementering. Dette undgår også afhængigheden med en bestemt OData-version (hvis OData-versionen opdateres, kan udvidelser blive afbrudt). |
| **Erstattet af en anden funktion?**   |  Det anbefales, at du bruger IController-klasseudvidelsesmodelet ved at importere NuGet-pakken (Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Produktområder, der er berørt**         | Retail- serverudvidelser |
| **Installationsindstilling**              | Alt |
| **Status**                         | Forældet fra og med version 10.0.11 |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Hardwarestationsudvidelse ved hjælp af IHardwareStationController
|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Hardwarestationsudvidelse ved hjælp af IHardwareStationController er blevet udfaset for at levere en forenklet udvidelsesmodel. Den nye implementering vil kun have klassen IController uden yderligere klasseimplementering, og for at undgå afhængigheden af de centrale hardwarestationsbiblioteker skal tidligere udvidelser henvise til flere biblioteker. |
| **Erstattet af en anden funktion?**   | Det anbefales, at du bruger IController-klasseudvidelsesmodelet ved at importere NuGet-pakken (Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Produktområder, der er berørt**         | Hardwarestationsudvidelser |
| **Installationsindstilling**              | Alt |
| **Status**                         | Forældet fra og med version 10.0.11 |

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
