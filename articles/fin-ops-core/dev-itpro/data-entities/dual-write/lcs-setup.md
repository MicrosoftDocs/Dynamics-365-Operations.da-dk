---
title: Konfiguration af dobbeltskrivning fra Lifecycle Services
description: Denne artikel beskriver, hvordan du konfigurerer en forbindelse med dobbeltskrivning fra Microsoft Dynamics Lifecycle Services (LCS).
author: laneswenka
ms.date: 05/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: a002bae22044ea10be30340a87a191305f6c6b92
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111964"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Konfiguration af dobbeltskrivning fra Lifecycle Services

[!include [banner](../../includes/banner.md)]



Denne artikel beskriver, hvordan du aktiverer dobbeltskrivning fra Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Forudsætninger

Kunder skal fuldføre Power Platform-integrationen som beskrevet i følgende emner:

- Hvis du endnu ikke bruger Microsoft Power Platform og vil udvide finans og drift-miljøer ved at tilføje platformegenskaber, skal du se [Power Platform-integration – Aktivér under installation af miljøet](../../power-platform/enable-power-platform-integration.md#enable-during-deploy).
- Hvis du allerede har Dataverse- og Power Platform-miljøer, og du vil oprette forbindelse mellem dem i finans og drift-miljøer, skal du se [Power Platform-integration – Aktivere efter installation af miljøet](../../power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="set-up-dual-write-for-new-or-existing-dataverse-environments"></a>Konfigurere dobbeltskrivning for nye eller eksisterende Dataverse-miljøer

Følg disse trin for at konfigurere dobbeltskrivning fra LCS-siden **Miljøoplysninger**:

1. Udvid sektionen **Power Platform-integration** på siden **Miljøoplysninger**.

2. Vælg knappen **Dobbeltskrivningsapplikation**.

    ![Power Platform-integration.](media/powerplat_integration_step2.png)

3. Gennemse vilkår og betingelser, og markér afkrydsningsfeltet **Konfigurer**.

4. Vælg **OK** for at fortsætte.

5. Du kan overvåge status ved at opdatere siden med miljøoplysninger med jævne mellemrum. Konfigurationen tager typisk 30 minutter eller mindre.  

6. Når installationen er fuldført, vises der en meddelelse, som fortæller, om processen lykkedes, eller om der opstod en fejl. Hvis installationen mislykkedes, vises der en relateret fejlmeddelelse. Du skal rette eventuelle fejl, før du går videre til næste trin.

7. Vælg **Link til Power Platform-miljø** for at oprette en kæde mellem Dataverse og databaserne i det aktuelle miljø. Det tager typisk mindre end 5 minutter.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Link til Power Platform-miljø.":::

8. Når sammenkædningen er fuldført, vises der et link. Brug linket til at logge på administrationsområdet med dobbeltskrivning i finans og drift-miljøet. Herfra kan du oprette objekttilknytninger.

## <a name="linking-mismatch"></a>Uoverensstemmende sammenkædning

Det er muligt, at dit dobbeltskrivningsmiljø er kædet sammen med en forekomst af Dataverse, mens LCS ikke er konfigureret til Power Platform-integration. En sådan uoverensstemmelse kan forårsage uventet funktionalitet. Det anbefales, at LCS-miljødetaljerne stemmer overens med det, du er tilsluttet i dobbeltskrivning, så den samme forbindelse kan bruges af forretningshændelser, virtuelle tabeller og tilføjelsesprogrammer.

Hvis dit miljø har en uoverensstemmende sammenkædning, viser LCS en advarsel på siden med dine miljøoplysninger i stil med: "Microsoft har registreret, at dit miljø er kædet sammen via dobbeltskrivning til en anden destination end den, der er angivet i Power Platform-integration, hvilket ikke anbefales."

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform-uoverensstemmelse mellem integrationslink.":::

Hvis du modtager denne advarsel, kan du prøve en af følgende løsninger:

- Hvis LCS-miljøet aldrig er konfigureret til Power Platform-integration, kan du oprette forbindelse til den forekomst af Dataverse, der er konfigureret i dobbeltskrivning, ved at følge instruktionerne i denne artikel.
- Hvis LCS-miljøet allerede er konfigureret til Power Platform-integration, skal du fjerne tilknytningen til dobbeltskrivning og genoprette den til den, der er angivet af LCS , ved hjælp af [scenariet: Nulstil eller rediger sammenkædning](relink-environments.md#scenario-reset-or-change-linking).

Tidligere var en manuel supportanmodning tilgængelig, men det var før mulighed 1 ovenfor eksisterede.  Microsoft understøtter ikke længere manuelle sammenkædningsanmodninger via supportanmodninger.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

