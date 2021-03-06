---
title: Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management
description: I dette emne beskrives funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: a7a9fb619ce3488ad4e3e79292af7acc359b83c5
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193224"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Dette emne opdateres, efterhånden som nye fjernede eller udfasede funktioner dokumenteres til Dynamics 365 Supply Chain Management.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning.

> [!NOTE]
> Du kan finde detaljerede oplysninger om objekter i Finance and Operations-apps i [Technical Reference-rapporterne](/dynamics/s-e/). Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finance and Operations-apps.


## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10019-release"></a>Fjernede eller udfasede funktioner i Supply Chain Management 10.0.19-udgaven

### <a name="job-card-device"></a>Jobkortenhed

| &nbsp;  | &nbsp;  |
|---|---|
| **Årsagen til forældelsen/fjernelsen** | [Jobkortenheden](../production-control/config-job-card-device.md) erstattes af den nye [grænseflade til produktionsudførelse](../production-control/production-floor-execution-configure.md). |
| **Erstattet af en anden funktion?**   | Ja, [jobkortenheden](../production-control/config-job-card-device.md) skal erstattes af den nye [grænseflade til produktionsudførelse](../production-control/production-floor-execution-configure.md). |
| **Produktområder, der er berørt** | Supply Chain Management – produktionsstyring |
| **Installationsindstilling** | Cloud og det lokale miljø |
| **Status** | Forældet. Jobkortenheden modtager understøttelse med fejl- og sikkerhedsrettelser, men der vil ikke længere blive leveret funktionsforbedringer. Efter april 2022 vil jobkortenheden ikke længere være understøttet, og kunderne bliver bedt om at flytte til den nye grænseflade til produktionsudførelse. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Fjernede eller udfasede funktioner i Supply Chain Management 10.0.18-udgaven

### <a name="dynamics-365-for-finance-and-operations---warehousing-the-warehouse-app"></a>Dynamics 365 for Finance and Operations – Lagersted (lagerstedsappen)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Gældende fra april 2021, *Dynamics 365 for Finance and Operations – Lagersted* (lagerstedsappen) bliver frarådet og vil ikke blive understøttet efter april 2022. Den er nu erstattet af *mobilappen Lokationsstyring*, som blev frigivet med version 10.0.17 af Supply Chain Management. Den nye app er en komplet erstatning, men bruger samme underliggende struktur, hvilket gør migreringen let. Hvis det er nødvendigt, kan de to apps bruges side om side, så brugerne kan tilpasse sig gradvist, efterhånden som de lærer at bruge den nye app.<br><br>Der er flere oplysninger om den nye mobilapp Lokationsstyring i [Mobilappen Lokationsstyring](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) og [Installere og tilslutte mobilappen Lokationsstyring](../warehousing/install-configure-warehouse-management-app.md). |
| **Erstattet af en anden funktion?**   | Ja, erstattet af den nye mobilapp Lokationsstyring. |
| **Produktområder, der er berørt**         | Supply Chain Management – lagerstedsapp |
| **Installationsindstilling**              | Cloud og det lokale miljø |
| **Status**                         | Forældet. Lagerstedsappen modtager understøttelse med fejl- og sikkerhedsrettelser, men der vil ikke længere leveres funktionsforbedringer. Efter april 2022 understøttes den gamle lagerstedsapp ikke længere, og kunderne bliver bedt om at flytte til den nye mobilapp Lokationsstyring. Den gamle lagerstedsapp fjernes derefter fra Microsoft Store og Google Play Butik.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Fjernede eller udfasede funktioner i Supply Chain Management 10.0.15-udgaven

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-understøttelse af Dynamics 365 udfases

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Microsoft Internet Explorer 11-understøttelsen af alle Dynamics 365-produkter udfases fra december 2020, og Internet Explorer 11 understøttes ikke efter august 2021.<br><br>Dette vil påvirke kunder, der bruger Dynamics 365-produkter, som er udviklet til brug via en Internet Explorer 11-grænseflade. Efter august 2021 er Internet Explorer 11 ikke understøttet for sådanne Dynamics 365-produkter. |
| **Erstattet af en anden funktion?**   | Vi anbefaler, at kunderne overgår til Microsoft Edge.|
| **Produktområder, der er berørt**         | Alle Dynamics 365-produkter |
| **Installationsindstilling**              | Alt|
| **Status**                         | Forældet. Internet Explorer 11 understøttes ikke efter august 2021.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Brug af det indbyggede Supply Chain Management-varedisponeringsprogram til produktionsscenarier

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Med henblik på at forbedre ydeevnen og minimere SQL-databasebelastningen under varedisponeringskørsler erstattes det indbyggede Supply Chain Management-varedisponeringsprogram med Planlægningsoptimering. Planlægningsoptimering giver mulighed for kørsler af hurtig planlægning, der også kan udføres inden for kontorets åbningstider. Dette giver planlæggere mulighed for straks at reagere på behovsmæssige ændringer eller planlægningsparametre. |
| **Erstattet af en anden funktion?**   | Ja, Planlægningsoptimering erstatter det eksisterende indbyggede Supply Chain Management-varedisponeringsprogram. |
| **Produktområder, der er berørt**         | Supply Chain Management – varedisponering |
| **Installationsindstilling**              | Kun skybaseret. Bemærk, at Planlægningsoptimering ikke understøttes med lokale installationer. |
| **Status**                         | Forældet. Inden 1. april 2022 vil produktionsscenarier ikke længere være understøttet med det indbyggede Dynamics 365 Supply Chain Management-varedisponeringsprogram. For produktionsscenarier skal kunderne bruge Planlægningsoptimering til varedisponeringsberegninger. Du kan finde flere oplysninger under [Dokumention til Planlægningsoptimering](../master-planning/planning-optimization/planning-optimization-overview.md). Kunder med lokale installationer af Dynamics 365 Supply Chain Management kan fortsætte med at bruge Supply Chain Management-varedisponeringsprogrammet til produktionsscenarier efter april 2022. Der kommer dog ikke flere funktionsforbedringer. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Fjernede eller udfasede funktioner i Supply Chain Management 10.0.11-udgaven

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Brug af det indbyggede Supply Chain Management-varedisponeringsprogram til distributionsscenarier

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Med henblik på at forbedre ydeevnen og minimere SQL-databasebelastningen under varedisponeringskørsler erstattes det indbyggede Supply Chain Management-varedisponeringsprogram med Planlægningsoptimering. Planlægningsoptimering giver mulighed for kørsler af hurtig planlægning, der også kan udføres inden for kontorets åbningstider. Dette giver planlæggere mulighed for straks at reagere på behovsmæssige ændringer eller planlægningsparametre. |
| **Erstattet af en anden funktion?**   | Ja, Planlægningsoptimering erstatter det eksisterende indbyggede Supply Chain Management-varedisponeringsprogram. |
| **Produktområder, der er berørt**         | Supply Chain Management – varedisponering |
| **Installationsindstilling**              | Kun skybaseret. Bemærk, at Planlægningsoptimering ikke understøttes med lokale installationer. |
| **Status**                         | Forældet. Inden 1. april 2021 vil distributionsscenarier ikke længere være understøttet med det indbyggede Dynamics 365 Supply Chain Management-varedisponeringsprogram. For distributionsscenarier skal kunderne bruge Planlægningsoptimering til varedisponeringsberegninger. Du kan finde flere oplysninger under [Dokumention til Planlægningsoptimering](../master-planning/planning-optimization/planning-optimization-overview.md). Kunder med lokale installationer af Dynamics 365 Supply Chain Management kan fortsætte med at bruge Supply Chain Management-varedisponeringsprogrammet til distributionsscenarier efter april 2021. Der kommer dog ikke flere funktionsforbedringer. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere meddelelser om fjernede eller udfasede funktioner

Hvis du vil vide mere om funktioner, der er blevet fjernet eller udfaset i tidligere versioner, kan du se [Fjernede eller udfasede funktioner i tidligere versioner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
