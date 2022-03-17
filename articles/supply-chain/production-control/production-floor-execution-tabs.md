---
title: Designe grænsefladen til kørsel af produktion
description: Dette emne beskriver, hvordan du kan designe indholdet af brugergrænsefladen for hver konfiguration.
author: johanhoffmann
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration, JmgProductionFloorExecutionConfigurationTab
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ee206ced76dbdd356c77d34a4b8f197879e9a3f0
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384766"
---
# <a name="design-the-production-floor-execution-interface"></a>Designe grænsefladen til kørsel af produktion

[!include [banner](../includes/banner.md)]

Du kan designe indholdet af brugergrænsefladen for hver konfiguration, der bruges af grænsefladen til kørsel af produktion. Arbejdere i én arbejdscelle skal f.eks. kunne åbne jobinstruktioner i produktionen, mens der i en anden arbejdscelle ikke er brug for instruktioner. Hvis det er tilfældet, skal der oprettes to konfigurationer, én med en knap til åbning af vedhæftede dokumenter og én uden denne knap.

## <a name="design-a-tab"></a>Designe en fane

På siden **Konfigurer kørsel af produktion** kan du oprette og konfigurere faner ved at vælge **Design faner** i handlingsruden.

Hver fane er inddelt i fire sektioner, som vist i følgende illustration.

![Fanelayout.](media/pfe-tab-layout.png "Fanelayout")

Følgende elementer vises i illustrationen:

1. Primær værktøjslinje
1. Sekundær værktøjslinje
1. Hovedvisning
1. Detaljeret visning

Følg disse trin for at oprette og konfigurere en ny fane:

1. Gå til **Produktionsstyring \> Opsætning \> Produktionsudførelse \> Konfigurer kørsel af produktionsudstyr**.

1. Vælg **Design faner** i handlingsruden for at åbne siden **Design faner**.

    ![Siden Design faner.](media/pfe-design-tabs.png "Siden Design faner")

1. Vælg **Ny** i handlingsrude.

1. Foretag følgende indstillinger i overskriften på siden:

    - **Fanenavn** – Angiv et navn til fanen.
    - **Hovedvisning** – Vælg mellem de foruddefinerede joblister (*Aktive job*, *Alle job*, *Mine job* og *Min maskine*).
    - **Detaljevisning** – Vælg mellem en tom værdi eller **Jobdetaljer**. Hvis du vælger den tomme værdi, vil der ikke være detaljeret visning under fanen. Hvis du vælger **Jobdetaljer**, indeholder detaljeret visning en detaljeret beskrivelse af det job, der er valgt på joblisten i hovedvisningen.

1. Vælg, hvilke knapper der skal være tilgængelige på den primære værktøjslinje, i sektionen **Primær værktøjslinje**. I kolonnen **Tilgængelige handlinger** vises en liste over alle de knapper, der kan tilføjes. I kolonnerne **Valgte handlinger** vises en liste over alle de knapper, der er medtaget i den aktuelle konfiguration. Brug knapperne mellem kolonnerne til at flytte markerede elementer mellem kolonnerne efter behov. Brug op- og ned-knapperne ud for kolonnen **Valgte handlinger** til at styre den rækkefølge, som knapperne vises i i brugergrænsefladen.

1. Vælg, hvilke knapper der skal være tilgængelige på den sekundære værktøjslinje, i sektionen **Sekundær værktøjslinje**. I kolonnen **Tilgængelige handlinger** vises en liste over alle de knapper, der kan tilføjes. I kolonnerne **Valgte handlinger** vises en liste over alle de knapper, der er medtaget i den aktuelle konfiguration. Brug knapperne mellem kolonnerne til at flytte markerede elementer mellem kolonnerne efter behov. Brug op- og ned-knapperne ud for kolonnen **Valgte handlinger** til at styre den rækkefølge, som knapperne vises i i brugergrænsefladen.

## <a name="associate-a-tab-with-a-configuration"></a>Knytte en fane til en konfiguration

Når du har designet alle de faner, du har brug for, kan du knytte dem til en konfiguration.

1. Gå til **Produktionsstyring \> Opsætning \> Produktionsudførelse \> Konfigurer kørsel af produktionsudstyr**.

    ![Konfiguration af udførelse af produktionsgulv.](media/pfe-config-prod-floor-execution.png "Konfiguration af udførelse af produktionsgulv")

1. Vælg **Tilføj** i oversigtspanelet **Valg af fane**.

1. Der føjes en ny række til gitteret. For denne nye række skal du vælge navnet på en fane, som du vil føje til konfigurationen.

1. Fortsæt med at tilføje flere faner efter behov.

1. Brug knapperne **Flyt op** og **Flyt ned** på værktøjslinjen til at arrangere fanerne efter behov. Fanerne vises fra venstre mod højre i den rækkefølge, der vises i skærmbilledet ovenfor (fanen øverst vises til venstre).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
