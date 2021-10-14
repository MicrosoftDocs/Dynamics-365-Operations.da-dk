---
title: Fjernede eller udfasede funktioner i Dynamics 365 Commerce
description: Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Commerce.
author: josaw
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b582b8b95fcf2ad45aa1bb49eb5594d30874e0f4
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559553"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Fjernede eller udfasede funktioner i Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Commerce.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning. 

> [!NOTE]
> Du kan finde detaljerede oplysninger om objekter i Finance and Operations-apps i [Technical Reference-rapporterne](/dynamics/s-e/). Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finance and Operations-apps.

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>Fjernede eller udfasede funktioner i Commerce 10.0.21-frigivelsen

[!include [banner](../includes/preview-banner.md)]

### <a name="overlapping-discounts-handling-setting-in-commerce-parameters"></a>Indstillinger for håndtering af overlappende rabatter i parametre for handel

Indstillingen for **håndtering af overlappende rabatter** på siden **Handelsparametre** frarådes i versionen af Commerce version 10.0.21. Fremad vil programmet til handelsprissætning bruge en enkelt algoritme til at bestemme den optimale kombination af overlappende rabatter.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | <p>Indstillingen for **håndtering af overlappende rabatter** i parametre for handel styrer, hvordan programmet til handelsprissætning søger i og bestemmer den optimale kombination af overlappende rabatter. Det indeholder i øjeblikket tre muligheder:<p><ul><li> **Bedste performance** – Denne indstilling bruger en avanceret heuridisk algoritme og en [metode til rangering af beregningsværdi](../optimal-combination-overlapping-discounts.md) til at prioritere, evaluere og fastlægge den bedste rabatkombination i rette tid.</li><li>**Afbalanceret beregning** – I det aktuelle kodegrundlag fungerer denne indstilling på samme måde som indstillingen **Bedste performance**. Derfor er det egentlig en dubletindstilling.</li><li>**Udtømmende beregning** – Denne indstilling bruger en gammel algoritme, der gennemgår alle de mulige rabatkombinationer under prisberegningen. I forbindelse med ordrer, der har store linjer og mængder, kan denne indstilling forårsage problemer med ydeevnen.</li></ul><p>For at forenkle konfigurationen, forbedre ydeevnen og reducere antallet af hændelser, der forårsages af den gamle algoritme, vil vi helt fjerne indstillingen for håndtering af **overlappende rabatter** og opdatere den interne logik i programmet Handelsprissætning, så programmet nu kun bruger den avancerede algoritme (det vil sige algoritmen bag indstillingen **Bedste performance**).</p> |
| **Erstattet af en anden funktion?**   | Nr. Det anbefales, at organisationer, der bruger indstillingen **Afbalanceret beregning** eller **Udtømmende beregning**, skifter til indstillingen **Bedste performance**, før denne funktion fjernes. |
| **Produktområder, der er berørt**         | Priser og rabatter |
| **Installationsindstilling**              | Alt |
| **Status**                         | Pr. version 10.0.21 fjernes indstillingen for **håndtering af overlappende rabatter** fra commerce-parametrene i oktober 2022. |

### <a name="retail-sdk-distributed-by-using-lifecycle-services"></a>Retail SDK distribueret via Lifecycle Services

Retail SDK leveres i Lifecycle Services (LCS). Denne distributionsmåde er forældet i version 10.0.21. Fremover vil Retail SDK-referencepakker, -biblioteker og -eksempler blive publiceret i offentlige lagre på GitHub.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Retail SDK leveres i LCS. Det tager et par timer at fuldføre LCS-processen, og processen skal gentages for hver opdatering. Fremover vil Retail SDK-referencepakker, -biblioteker og -eksempler blive publiceret i offentlige lagre på GitHub. Udvidelsesprøver og referencepakker kan nemt forbruges, og opdateringerne fuldføres på få minutter. |
| **Erstattet af en anden funktion?**   |  [Hente Retail SDK-eksempler og -referencepakker fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md) |
| **Produktområder, der er berørt**         | Retail SDK |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udgået: Fra og med version 10.0.21 vil levering af SDK via LCS VM'er blive fjernet i oktober 2022. |

### <a name="retail-deployable-package-and-combined-pos-hardware-station-and-cloud-scale-unit-installers"></a>Retail-installationspakke og kombinerede installationsprogrammer for POS, Hardwarestation og Cloud Scale Unit

Retail-installationspakker, der er genereret ved hjælp af Retail SDK MSBuild, udgår i 10.0.21. Fremover skal du bruge Cloud Scale Unit-pakken (CSU) til CSU-udvidelser (Commerce Runtime, kanaldatabase, API'er for Headless Commerce, Betalinger og Cloud Point of Sale (POS)). Brug installationsprogrammer kun til udvidelser for POS, Hardwarestation og Cloud Scale Unit i lokalt miljø.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | En Retail-installationspakke er en kombineret pakke, der indeholder et komplet sæt udvidelsespakker og -installationsprogrammer. Denne kombinerede pakke gør installationen kompleks, når CSU-udvidelser anvendes til Cloud Scale Unit og installationsprogrammerne installeres i butikker. Installationsprogrammerne indeholder filtypenavnet og basisproduktet, hvilket gør opdateringerne vanskelige. Ved hver opgradering kræves der en kodefletning og en pakkegenerering. For at forenkle denne proces er udvidelsespakkerne nu adskilt i komponenter, så de er lette at installere og administrere. Med den nye fremgangsmåde er udvidelser og basisproduktinstallationsprogrammer adskilt og kan serviceres og opgraderes uafhængigt af hinanden uden kodefletning eller ompakning.|
| **Erstattet af en anden funktion?**   | CSU-udvidelser, installationsprogrammer til POS-udvidelser, installationsprogrammer til udvidelse af Hardwarestation |
| **Produktområder, der er berørt**         | Dynamics 365 Commerce-udvidelse og -installation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udgået: Fra og med version 10.0.21 fjernes understøttelsen af installationen af RetailDeployablePackage i LCS i oktober 2022. |

Du kan finde flere oplysninger i:

+ [Generere en separat pakke til Commerce Cloud Scale Unit (CSU)](../dev-itpro/retail-sdk/retail-sdk-packaging.md#generate-a-separate-package-for-commerce-cloud-scale-unit-csu)
+ [Oprette en udvidelsespakke til Modern POS](../dev-itpro/pos-extension/mpos-extension-packaging.md)
+ [Integrere POS i en ny hardwareenhed](../dev-itpro/hardware-device-extension.md)
+ Kodeeksempler
    + [Cloud Scale Unit](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit)
    + [POS, CSU og Hardwarestation](https://github.com/microsoft/Dynamics365Commerce.InStore)

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>ModernPos.Sln og CloudPOs.sln i Retail SDK

Udvikling af POS-udvidelse ved hjælp af ModernPos.sln, CloudPOs.sln, POS. Extension.csproj, og POS-mappen udgår i version 10.0.21. Fremover skal du bruge den POS-uafhængige installationspakke til SDK for POS-udvidelser.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Hvis der er POS-udvidelser i tidligere versioner af Retail SDK, kræves der en kodefletning og ompakning for at opdatere til den seneste version af POS. Kodefletningen var en tidskrævende opgraderingsproces, og du skulle vedligeholde hele Retail SDK i lageret. Du skulle også kompilere POS. App-kerneprojektet. Ved hjællp af den uafhængige pakningsmodel skal du kun vedligeholde udvidelsen. Opdateringsprocessen til den seneste version af POS-udvidelserne er lige så let som at opdatere versionen af den NuGet-pakke, som dit projekt forbruger. Udvidelser kan installeres uafhængigt, og tjenester bruger installationsprogrammer for udvidelserne. Den grundlæggende POS kan installeres og vedligeholdes separat, og der kræves ingen kodefletning eller ompakning med basisinstallationsprogrammet eller -koden. |
| **Erstattet af en anden funktion?**   | [POS-uafhængige SDK-pakker](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **Produktområder, der er berørt**         | Dynamics 365 Commerce POS-udvidelse og -installation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udgået: Pr. version 10.0.21 fjernes understøttelsen af kombinerede POS-pakker og udvidelsesmodellen ved hjælp af ModernPos.Sln, CloudPOs.sln og POS. Extensons.csproj i Retail SDK i oktober 2022. |

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Fjernede eller udfasede funktioner i Commerce 10.0.17-frigivelsen

### <a name="full-dataset-generation-interval-is-deprecated"></a>Det frarådes at bruge det fulde interval for generering af datasæt

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Fra og med denne version af formen **Parametre for Commerce-planlægger** i Dynamics 365 headquarters frarådes det **fulde interval for oprettelse af datasæt i dage**. Når du starter i denne version, fjernes feltet visuelt, så værdien ikke kan redigeres. Dette vil forblive værdien **0**. |
| **Erstattet af en anden funktion?**   | Ingen |
| **Produktområder, der er berørt**         | Dynamics 365 Commerce |
| **Installationsindstilling**              | Alt|
| **Status**                         | Forældet. Brug ikke dette felt, eller rediger værdien i det.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Fjernede eller udfasede funktioner i Commerce 10.0.15-frigivelsen

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-understøttelse af Dynamics 365 udfases

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Microsoft Internet Explorer 11-understøttelsen af alle Dynamics 365-produkter udfases fra december 2020, og Internet Explorer 11 understøttes ikke efter august 2021.<br><br>Dette vil påvirke kunder, der bruger Dynamics 365-produkter, som er udviklet til brug via en Internet Explorer 11-grænseflade. Efter august 2021 er Internet Explorer 11 ikke understøttet for sådanne Dynamics 365-produkter. |
| **Erstattet af en anden funktion?**   | Vi anbefaler, at kunderne overgår til Microsoft Edge.|
| **Produktområder, der er berørt**         | Alle Dynamics 365-produkter |
| **Installationsindstilling**              | Alt|
| **Status**                         | Forældet. Internet Explorer 11 understøttes ikke efter august 2021.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Fjernede eller udfasede funktioner i Commerce 10.0.11-frigivelsen
### <a name="data-action-hooks"></a>Datahandlings-hooks
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Funktionen Datahandlings-hooks frarådes på grund af problemer med ydeevnen. |
| **Erstattet af en anden funktion?**   | Vi anbefaler at bruge [datahandlingstilsidesættelser](../e-commerce-extensibility/data-action-overrides.md) til at redigere forretningslogik i datahandlingslaget.|
| **Produktområder, der er berørt**         | Datahandlinger for udvidelse af e-handel |
| **Installationsindstilling**              | Alt |
| **Status**                         | Forældet fra og med version 10.0.11 |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Understøttelse af Retail SDK til Visual Studio 2015, msbuild 14,0 og Retail SDK\Reference-biblioteker og -værktøjer
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Retail SDK-understøttelsen til Visual Studio 2015 er blevet udfaset og opdateret for at understøtte vs. 2017, msbuild 15,0 og alle referencebiblioteker og Commerce-proxygenerator-værktøjer i mappen RetailSDK\References er flyttet til NuGet-pakker for at forenkle udvidelsesmodellen og opgraderingsprocessen for SDK.|
| **Erstattet af en anden funktion?**   | Det anbefales, at du følger oplysningerne i [Overflytte Retail SDK data fra Visual Studio 2015 til Visual Studio 2017](../dev-itpro/retail-sdk/migrate-sdk.md) for at opdatere systemet. |
| **Produktområder, der er berørt**         | Retail SDK-udvidelser |
| **Installationsindstilling**              | Alt |
| **Status**                         | Forældet fra og med version 10.0.11 |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Retail-serverudvidelse ved hjælp af IEdmModelExtender og CommerceController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Retail-serverudvidelse ved hjælp af IEdmModelExtender og CommerceController er blevet udfaset for at levere en forenklet udvidelsesmodel. Den nye implementering vil kun have controller-klassen uden yderligere IEdmModelExtender-klasseimplementering. Dette undgår også afhængigheden med en bestemt OData-version (hvis OData-versionen opdateres, kan udvidelser blive afbrudt). |
| **Erstattet af en anden funktion?**   |  Det anbefales, at du bruger IController-klasseudvidelsesmodelet ved at importere NuGet-pakken (Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Produktområder, der er berørt**         | Retail- serverudvidelser |
| **Installationsindstilling**              | Alt |
| **Status**                         | Forældet fra og med version 10.0.11 |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Hardwarestationsudvidelse ved hjælp af IHardwareStationController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Hardwarestationsudvidelse ved hjælp af IHardwareStationController er blevet udfaset for at levere en forenklet udvidelsesmodel. Den nye implementering vil kun have klassen IController uden yderligere klasseimplementering, og for at undgå afhængigheden af de centrale hardwarestationsbiblioteker skal tidligere udvidelser henvise til flere biblioteker. |
| **Erstattet af en anden funktion?**   | Det anbefales, at du bruger IController-klasseudvidelsesmodelet ved at importere NuGet-pakken (Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Produktområder, der er berørt**         | Hardwarestationsudvidelser |
| **Installationsindstilling**              | Alt |
| **Status**                         | Forældet fra og med version 10.0.11 |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Fjernede eller udfasede funktioner i Commerce 10.0.10-frigivelsen
### <a name="pos-operation-803---picking-and-receiving"></a>POS-operation 803 – pluk og tilgang
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Pluk- og tilgangsoperationer frarådes på grund af nyt omdesign af operationerne. |
| **Erstattet af en anden funktion?**   | Ja. Det erstattes af to nye POS-operationer: indgående operation (804) og udgående operation (805).|
| **Produktområder, der er berørt**         | POS-program |
| **Installationsindstilling**              | Alt |
| **Status**                         | Frarådes: Fra og med version 10.0.10 modtager pluk- og tilgangsoperationer ikke længere nye funktionsforbedringer. Der udføres kun kritiske fejlrettelser for denne operation i fremtidige versioner. Alle kunder opfordres til at skifte til de nye [Indgående operationer](../pos-inbound-inventory-operation.md) og [Udgående operationer](../pos-outbound-inventory-operation.md), som fortsat vil være en del af vores langsigtede produktoversigt. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Fjernede eller udfasede funktioner i Commerce 10.0.7-frigivelsen
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities- og GetAvailableInventoryNearby-API'er
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Nye optimerede API'er er oprettet for at erstatte GetProductAvailabilities- og GetAvailableInventoryNearby-API'erne. |
| **Erstattet af en anden funktion?**   | Ja: Det erstattes af GetEstimatedAvailability- og GetEstimatedProductWarehouseAvailability-API'er. |
| **Produktområder, der er berørt**         | SDK til e-handelsprogrammer |
| **Installationsindstilling**              | Alt |
| **Status**                         | Frarådes: Fra og med version 10.0.7 foretages der ikke længere tekniske investeringer for GetProductAvailabilities og GetAvailableInventoryNearby. Organisationer, der bruger disse API'er i deres e-handelsinstallationer, skal konvertere til de nye GetEstimatedAvailability- og GetEstimatedProductWarehouseAvailability-API'er og aktivere [funktionen Beregning af optimeret produkttilgængelighed](../calculated-inventory-retail-channels.md).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere meddelelser om fjernede eller udfasede funktioner
Hvis du vil vide mere om funktioner, der er blevet fjernet eller udfaset i tidligere versioner, kan du se [Fjernede eller udfasede funktioner i tidligere versioner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
