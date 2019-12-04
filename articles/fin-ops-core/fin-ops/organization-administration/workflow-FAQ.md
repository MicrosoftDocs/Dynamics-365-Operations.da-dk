---
title: Ofte stillede spørgsmål om arbejdsgang
description: Dette emne besvarer ofte stillede spørgsmål om arbejdsgangssystemet.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0188e8ed3cbbfd7dbccd7d13cf6129e146a919ac
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772691"
---
# <a name="workflow-faq"></a>Ofte stillede spørgsmål om arbejdsgang

[!include [banner](../includes/banner.md)]

Dette emne besvarer ofte stillede spørgsmål om arbejdsgangssystemet.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Hvorfor modtages flere beskeder, når en workflowopgave afvises?
Når en workflowopgave afvises, fuldføres den som afvist. Der oprettes en anden workflowopgave, som tildeles til igangsætteren. Det betyder, at der er en besked til igangsætteren af den afviste workflowopgave, og en særskilt besked til den bruger, der er tildelt til den nye workflowopgave med "ændringsanmodning". 

Hver besked er for en særskilt workflowopgave, men lighedspunkter kan medføre forvirring. Vi ser på forskellige måder at forbedre dette i en senere version.

## <a name="why-are-my-workflow-exports-failing"></a>Hvorfor mislykkes eksporten af mine arbejdsgange?
Der er i øjeblikket en begrænsning i funktionen til eksport af arbejdsgange, som forhindrer, at arbejdsgangens navne overstiger 48 tegn. Hvis du bruger et navn, der er længere end 48 tegn, kan det resultere i, at fejlen "Serveren kunne ikke godkende anmodningen", og/eller forhindre, at en fil kan eksporteres uden en filtype. Følgende blogindlæg indeholder flere detaljer [Fejlfinding i forbindelse med eksport af arbejdsgang](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Kan afsenderen af en arbejdsgang også godkende arbejdsgangen?
Ja, en afsender af en arbejdsgang kan også godkende arbejdsgangen, hvis den er konfigureret på denne måde. Hvis du vil undgå dette, skal du angive **Arbejdsgangsparametre > Generelt > Godkender > Tillad ikke afsenders godkendelse** til **Ja**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Kan jeg føje påmindelser til arbejdsgange for at sende beskeder til brugerne?
Her er nogle få nøgleområder, du kan bemærke om tilføjelse af påmindelser til arbejdsgange for at give beskeder:
- Påmindelser for mekanismer til arbejdsgangsbeskeder
    - Påmindelser kan konfigureres til postændringer. Arbejdsgange ændrer poster, så det er muligt at oprette en påmindelse, der relaterer til en post, der er blevet ændret pga. en arbejdsgang. Men da arbejdsgange har forskellige indbyggede beskedindstillinger, er brug af påmindelser ikke ideel.
- Standardbeskeder fra arbejdsgange 
    - Arbejdsgange har indbyggede mailbeskeder. En kunde kan konfigurere beskederne, så brugerne sendes som mails. Disse beskeder resulterer ikke i Handlingscenter-meddelelser for brugere.
    - I en fremtidig opdatering vil vi tilføje en Handlingscenter-meddelelse, så en bruger får tildelt et arbejdsgangsopgave. 
- Føje beskeder til arbejdsgange
    - Handlingscenter-meddelelser kan oprettes for bestemte brugere, f.eks. en meddelelse, der er oprettet fra en arbejdsgang i X++.
    - [Arbejdsgangsforretningshændelser](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow), som kunden kan bruge til at udløse flows, har de beskeder, de søger.   

Hvis en bruger kort sagt ikke får den rigtige besked fra Handlingscenter, når vedkommende er blevet tildelt en arbejdsgangsopgave, så brug [Arbejdsgangsforretningshændelser](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) med Microsoft Power Automate til at give flere eller andre beskeder.
