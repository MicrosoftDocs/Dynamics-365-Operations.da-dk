---
title: Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration
description: Denne artikel giver et overblik over Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0b674f40b6bb433bc5e2c9216d649a7f15169442
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887082"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration

[!include [banner](includes/banner.md)]

Denne artikel giver et overblik over Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.

Dynamics 365 Commerce integrerer med Teams for at hjælpe kunder og deres medarbejdere med at forbedre produktivitet ved at synkronisere opgavestyring mellem de to programmer. Med den problemfri opgavestyring, som integration af Commerce og Teams giver, kan butikschefer og medarbejdere oprette opgavelister, tildele opgaver til flere butikker og spore status for opgaver på tværs af butikker fra det ene eller andet program.

Integration af Commerce og Teams er tilgængelig fra og med Commerce version 10.0.18.

## <a name="key-features"></a>Hovedfunktioner

Her er nogle af de vigtigste funktioner, som Commerce- og Microsoft Teams-integration indeholder:

- Klargøre Teams ved at udnytte veldefinerede oplysninger fra Commerce, f.eks. organisationsstruktur og oplysninger om butikker, arbejdere, tilladelser og forretningssituation.
- Nemt synkronisere løbende ændringer (f.eks. tilføjelse af nye butikker eller ansættelse af nye medarbejdere) mellem Commerce og Teams, men beholde Commerce som den overordnede kilde til data i organisationsstrukturen.
- Integrer opgavestyring mellem Commerce og Teams for at hjælpe butiksmedarbejdere, butikschefer, regionchefer og kommunikationsmedarbejdere med at håndtere opgavestyring fra begge programmer.

## <a name="prerequisites-for-using-integration-features"></a>Forudsætninger for brug af integrationsfunktioner

Følgende forudsætninger skal være tilstede, før du kan begynde at bruge Microsoft Teams-integrationsfunktioner:

- Microsoft 365 Business-standardlicens (denne licens inkluderer Teams).
- Azure Active Directory-konti (Azure AD) for alle butikschefer og arbejdere
- POS-systemer, der er konfigureret med Azure AD-godkendelse

## <a name="conceptual-architecture"></a>Grundlæggende arkitektur

I følgende illustration vises den grundlæggende arkitektur for integration af Dynamics 365 Commerce og Microsoft Teams med en San Francisco-butik som eksempel. Både Teams og Commerce POS-programmet bruger Microsoft Planner som lager, så opgaver, der udgives fra Teams, vises i POS-programmet, og ad hoc-opgaver, der er oprettet af butikschefer i POS-programmet, vises i Teams, hvilket medfører en problemfri opgavestyring mellem programmerne.    

![Arkitektur for integration af Commerce og Teams.](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration](enable-teams-integration.md)

[Klargøre Microsoft Teams fra Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Administrere brugerroller i Microsoft Teams](manage-user-roles-teams.md)

[Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams](map-stores-existing-teams.md)

[Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration](teams-integration-faq.md)
