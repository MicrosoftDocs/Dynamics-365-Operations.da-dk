---
title: Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management
description: I dette emne beskrives funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597110"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Dette emne opdateres, efterhånden som nye fjernede eller udfasede funktioner dokumenteres til Dynamics 365 Supply Chain Management.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning.

> [!NOTE]
> Du kan finde detaljerede oplysninger om objekter i Finance and Operations-apps i [Technical Reference-rapporterne](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finance and Operations-apps.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Fjernede eller udfasede funktioner i Supply Chain Management 10.0.11-udgaven

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Brug af det indbyggede Supply Chain Management-varedisponeringsprogram til distributionsscenarier

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Med henblik på at forbedre ydeevnen og minimere SQL-databasebelastningen under varedisponeringskørsler erstattes det indbyggede Supply Chain Management-varedisponeringsprogram med Planlægningsoptimering. Planlægningsoptimering giver mulighed for kørsler af hurtig planlægning, der også kan udføres inden for kontorets åbningstider. Dette giver planlæggere mulighed for straks at reagere på behovsmæssige ændringer eller planlægningsparametre. |
| **Erstattet af en anden funktion?**   | Ja, Planlægningsoptimering erstatter det eksisterende indbyggede Supply Chain Management-varedisponeringsprogram. |
| **Produktområder, der er berørt**         | Supply Chain Management – varedisponering |
| **Installationsindstilling**              | Kun skybaseret. Bemærk, at Planlægningsoptimering ikke understøttes med lokale installationer. |
| **Status**                         | Forældet. Fra april 2021 vil distributionsscenarier ikke længere være understøttet med det indbyggede Dynamics 365 Supply Chain Management-varedisponeringsprogram. For distributionsscenarier skal kunderne bruge Planlægningsoptimering til varedisponeringsberegninger. Du kan finde flere oplysninger under [Dokumention til Planlægningsoptimering](https://go.microsoft.com/fwlink/?linkid=2105830). Kunder med lokale installationer af Dynamics 365 Supply Chain Management kan fortsætte med at bruge Supply Chain Management-varedisponeringsprogrammet til distributionsscenarier efter april 2021. Der kommer dog ikke flere funktionsforbedringer. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere meddelelser om fjernede eller udfasede funktioner

Hvis du vil vide mere om funktioner, der er blevet fjernet eller udfaset i tidligere versioner, kan du se [Fjernede eller udfasede funktioner i tidligere versioner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
