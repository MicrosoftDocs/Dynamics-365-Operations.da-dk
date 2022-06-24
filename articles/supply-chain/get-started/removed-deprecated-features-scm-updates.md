---
title: Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management
description: Denne artikel beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 949fa0df58bc3338c8bc84ecbd4f2ad17117dd12
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865260"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Denne artikel opdateres, efterhånden som nye fjernede eller udfasede funktioner dokumenteres til Dynamics 365 Supply Chain Management.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning.

> [!NOTE]
> Du kan finde detaljerede oplysninger om objekter i Finans- og driftsapps i [Technical Reference-rapporterne](/dynamics/s-e/). Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finans- og driftsapps.


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
| **Årsagen til forældelsen/fjernelsen** | Gældende fra april 2021: *Dynamics 365 for Finance and Operations - Lagersted* (lagerstedsappen) bliver udfaset og vil ikke blive understøttet efter april 2022. Den er nu erstattet af *mobilappen Lokationsstyring*, som blev frigivet med version 10.0.17 af Supply Chain Management. Den nye app er en komplet erstatning, men bruger samme underliggende struktur, hvilket gør migreringen let. Hvis det er nødvendigt, kan de to apps bruges side om side, så brugerne kan tilpasse sig gradvist, efterhånden som de lærer at bruge den nye app.<br><br>Der er flere oplysninger om den nye mobilapp Lokationsstyring i [Mobilappen Lokationsstyring](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) og [Installere og tilslutte mobilappen Lokationsstyring](../warehousing/install-configure-warehouse-management-app.md). |
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
| **Status**                         | Forældet. Inden 1. april 2022 vil produktionsscenarier ikke længere være understøttet for det indbyggede Supply Chain Management-varedisponeringsprogram. På denne dato stopper Microsoft alle aktive udviklinger i produktionsscenarier for det indbyggede planlægningsprogram, vil ikke frigive nye funktioner og vil kun frigive kritiske rettelser. Efter denne dato skal alle firmaer, der har brug for understøttelse af produktionsscenarier, bruge Planlægningsoptimering til beregningerne af deres varedisponering. Planlægningsoptimering forventes at understøtte produktionsscenarier fuldt ud i oktober 2022. Du kan finde flere oplysninger i [dokumentationen til Planlægningsoptimering](../master-planning/planning-optimization/planning-optimization-overview.md).<br><br>Firmaer med lokale installationer af Supply Chain Management kan fortsætte med at bruge det indbyggede varedisponeringsprogram til produktionsscenarier efter april 2022. Der kommer dog ikke flere funktionsforbedringer. |

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
