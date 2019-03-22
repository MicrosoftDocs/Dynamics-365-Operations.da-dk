---
title: Ofte stillede spørgsmål om arbejdsgang
description: Dette emne besvar ofte stillede spørgsmål om arbejdsgangssystemet i Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
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
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/01/2019
ms.locfileid: "773201"
---
# <a name="workflow-system"></a>Arbejdsgangsystem

[!include [banner](../includes/banner.md)]

Dette emne besvar ofte stillede spørgsmål om arbejdsgangssystemet i Microsoft Dynamics 365 for Finance and Operations.

## <a name="notifications"></a>Beskeder

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Hvorfor modtages flere beskeder, når en workflowopgave afvises?
Når en workflowopgave afvises, fuldføres den som afvist. Der oprettes en anden workflowopgave, som tildeles til igangsætteren. Det betyder, at der er en besked til igangsætteren af den afviste workflowopgave, og en særskilt besked til den bruger, der er tildelt til den nye workflowopgave med "ændringsanmodning". 

Hver besked er for en særskilt workflowopgave, men lighedspunkter kan medføre forvirring. Vi ser på forskellige måder at forbedre dette i en senere version.
