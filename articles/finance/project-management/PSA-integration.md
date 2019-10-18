---
title: Oversigt over Project Service Automation
description: Dette emne indeholder oplysninger om Dynamics 365 Project Service Automation til Dynamics 365 Finance-integrationsløsningen.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250547"
---
# <a name="project-service-automation-overview"></a>Oversigt over Project Service Automation

[!include[banner](../includes/banner.md)]

Project Service Automation til Finance-integrationsløsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Dynamics 365 Finance og Dynamics 365 Project Service Automation via Common Data Service. Integrationsskabelonerne, der er tilgængelige med dataintegrationsfunktionen, muliggør strømmen af projekter, projektkontrakter, projektkontraktlinjer, milepæle i projektkontraktlinjer, projektopgaver, udgiftstransaktionskategorier, timeestimater og udgiftsestimater fra Project Service Automation til Finance.

> [!NOTE]
> - Hvis du bruger version 7.3.0, skal du installere KB 4074835. Du vil så være i stand til at integrere fastprisprojekter.
> - Hvis du bruger version 7.3.0, og du bringer gebyrtransaktioner fra Project Service Automation, skal du installere KB 4345320 for at medtage disse gebyrer i projektfakturaen.
> - Hvis du bruger version 8.0, kan du bruge projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner.
> - Hvis du bruger version 8.0.1 eller nyere, kan du synkronisere faktiske oplysninger.

Før du kan integrere Project Service Automation med Finance, skal du konfigurere integrationsparametrene for Project Service Automation. Du kan finde flere oplysninger under [Integrationsparametre for Project Service Automation](PSA-parameters.md).

Denne integrationsløsning muliggør direkte synkronisering i følgende situationer:

- Vedligeholde projektkontrakter i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance.
- Oprette projekter i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance.
- Vedligeholde projektkontraktlinjer i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance.
- Vedligeholde milepæle for projektkontraktlinjer i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance.
- Vedligeholde projektopgaver i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance.
- Vedligeholde udgiftstransaktionskategorier i Finance og synkronisere dem direkte fra Finance til Project Service Automation.
- Oprette projekttimeestimater i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance.
- Oprette projektudgiftsestimater i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance.
- Oprette faktiske tal for projekttid, udgifter og gebyr i Project Service Automation og oprette projektposteringer i Project Service Automation-integrationskladden, så de kan bogføres i Finance.

## <a name="data-synchronization"></a>Datasynkronisering

I følgende illustration vises, hvordan data synkroniseres som et led i integrationen mellem Project Service Automation og Finance.

> [!NOTE]
> Ikke alle skabeloner er tilgængelige for øjeblikket. Skabeloner udgives, efterhånden som de fuldføres.

[![Project Service Automation-integration med Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Systemkrav til Finance

Når du vil bruge løsningen til integration af Project Service Automation med Finance, skal du installere Enterprise edition 7.3 med Platform update 12 eller nyere.

## <a name="system-requirements-for-project-service-automation"></a>Systemkravene til Project Service Automation

Når du vil bruge løsningen til integration af Project Service Automation med Finance, skal du installere følgende komponenter:

- Dynamics 365 Project Service Automation version 9.0.0.0 eller nyere
- Løsningen Kundeemne til kontanter til Dynamics 365 Sales, version 1.14.0.0 (v14) eller nyere.
- Løsning til integration af Project Service Automation med Finance til Dynamics 365 Project Service Automation version 1.0.0.0 eller nyere

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Installer løsningen til integration af Project Service Automation med Finance i din Project Service Automation-forekomst.

Download Project Service Automation til Finance-integrationsløsning fra [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), og følg vejledningen, der er inkluderet i løsningen.
