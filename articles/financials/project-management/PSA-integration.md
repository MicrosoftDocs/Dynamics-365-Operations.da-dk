---
title: Project Service Automation
description: Dette emne indeholder oplysninger om Project Service Automation til integrationsløsningen til Finance and Operations. Denne integrationsløsning bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation via Common Data Service.
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557300"
---
# <a name="project-service-automation"></a>Project Service Automation

[!include[banner](../includes/banner.md)]

Project Service Automation til Finance and Operations-integrationsløsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation via Common Data Service. Integrationsskabelonerne, der er tilgængelige med dataintegrationsfunktionen, muliggør strømmen af projekter, projektkontrakter, projektkontraktlinjer, milepæle i projektkontraktlinjer, projektopgaver, udgiftstransaktionskategorier, timeestimater og udgiftsestimater fra Project Service Automation til Finance and Operations.

> [!NOTE]
> - Hvis du bruger Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, 7.3.0, når du har installeret KB 4132657 og KB 4132660, kan du bruge skabelonerne til at integrere projektopgaver, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og faktiske oplysninger og konfigurere låsning af funktionalitet. Hvis du skal nulstille regnskabsfordelingerne, anbefaler vi, at du også installerer KB 4131710.
> - Hvis du bruger Finance and Operations 7.3.0, skal du installere KB 4074835. Du vil så være i stand til at integrere fastprisprojekter.
> - Hvis du bruger Finance and Operations 7.3.0, og du bringer gebyrtransaktioner fra Project Service Automation, skal du installere KB 4345320 for at medtage disse gebyrer i projektfakturaen.
> - Hvis du bruger Microsoft Dynamics 365 for Finance and Operations version 8.0, kan du bruge projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner.
> - Hvis du bruger Microsoft Dynamics 365 for Finance and Operations version 8.0.1 eller nyere, kan du synkronisere faktiske oplysninger.

Før du kan integrere Project Service Automation med Finance and Operations, skal du konfigurere integrationsparametrene for Project Service Automation. Du kan finde flere oplysninger under [Integrationsparametre for Project Service Automation](PSA-parameters.md).

Denne integrationsløsning muliggør direkte synkronisering i følgende situationer:

- Vedligeholde projektkontrakter i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.
- Oprette projekter i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.
- Vedligeholde projektkontraktlinjer i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.
- Vedligeholde milepæle i projektkontraktlinjer i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.
- Vedligeholde projektopgaver i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.
- Vedligeholde udgiftstransaktionskategorier i Finance and Operations og synkronisere dem direkte fra Finance and Operations til Project Service Automation.
- Oprette projekttimeestimater i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.
- Oprette projektudgiftsestimater i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.
- Oprette faktiske tal for projekttid, udgifter og gebyr i Project Service Automation og oprette projektposteringer i Project Service Automation-integrationskladden, så de kan bogføres i Finance and Operations.

## <a name="data-synchronization"></a>Datasynkronisering

I følgende illustration vises, hvordan data synkroniseres som et led i integrationen mellem Project Service Automation og Finance and Operations.

> [!NOTE]
> Ikke alle skabeloner er tilgængelige for øjeblikket. Skabeloner udgives, efterhånden som de fuldføres.

[![Project Service Automation-integration med Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Systemkrav til Finance and Operations

Når du vil bruge løsningen til integration af Project Service Automation med Finance and Operations, skal du installere Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 med platformsopdatering 12 eller nyere.

## <a name="system-requirements-for-project-service-automation"></a>Systemkravene til Project Service Automation

Når du vil bruge løsningen til integration af Project Service Automation med Finance and Operations, skal du installere følgende komponenter:

- Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 eller nyere
- Kundeemne til kontantløsningen til Microsoft Dynamics 365 for Sales version 1.14.0.0 (v14) eller nyere
- Løsning til integration af Project Service Automation med Finance and Operations til Microsoft Dynamics 365 for Project Service Automation version 1.0.0.0 eller nyere

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Installer løsningen til integration af Project Service Automation med Finance and Operations i din Project Service Automation-forekomst

Hente Project Service Automation til Finance and Operations-integrationsløsning fra [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=57016), og følg vejledningen, der er inkluderet i løsningen.
