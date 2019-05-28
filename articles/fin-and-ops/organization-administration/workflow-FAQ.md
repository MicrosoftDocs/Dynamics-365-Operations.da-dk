---
title: Ofte stillede spørgsmål om arbejdsgang
description: Dette emne besvar ofte stillede spørgsmål om arbejdsgangssystemet i Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509285"
---
# <a name="workflow-system"></a>Arbejdsgangsystem

[!include [banner](../includes/banner.md)]

Dette emne besvar ofte stillede spørgsmål om arbejdsgangssystemet i Microsoft Dynamics 365 for Finance and Operations.

## <a name="notifications"></a>Beskeder

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Hvorfor modtages flere beskeder, når en workflowopgave afvises?
Når en workflowopgave afvises, fuldføres den som afvist. Der oprettes en anden workflowopgave, som tildeles til igangsætteren. Det betyder, at der er en besked til igangsætteren af den afviste workflowopgave, og en særskilt besked til den bruger, der er tildelt til den nye workflowopgave med "ændringsanmodning". 

Hver besked er for en særskilt workflowopgave, men lighedspunkter kan medføre forvirring. Vi ser på forskellige måder at forbedre dette i en senere version.

### <a name="why-are-my-workflow-exports-failing"></a>Hvorfor mislykkes eksporten af mine arbejdsgange?
Der er i øjeblikket en begrænsning i funktionen til eksport af arbejdsgange, som forhindrer, at arbejdsgangens navne overstiger 48 tegn. Hvis du bruger et navn, der er længere end 48 tegn, kan det resultere i, at fejlen "Serveren kunne ikke godkende anmodningen", og/eller forhindre, at en fil kan eksporteres uden en filtype. Følgende blogindlæg indeholder flere detaljer [Fejlfinding i forbindelse med eksport af arbejdsgang](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).
