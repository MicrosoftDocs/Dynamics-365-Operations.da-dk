---
title: Konfiguration af dobbeltskrivning fra Lifecycle Services
description: Dette emne beskriver, hvordan du konfigurerer en forbindelse med dobbeltskrivning fra Microsoft Dynamics Lifecycle Services (LCS).
author: laneswenka
ms.date: 08/03/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 9f461837c65c30eace3358c231618aedf428f487
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675291"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Konfiguration af dobbeltskrivning fra Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emne beskriver, hvordan du aktiverer dobbeltskrivning fra Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Forudsætninger

Du skal fuldføre Power Platform-integrationen som beskrevet i følgende emner:

+ [Power Platform-integration – Aktiveres under installation af miljøet](../../power-platform/enable-power-platform-integration.md#enable-during-deploy)
+ [Power Platform-integration – Aktivere efter installation af miljøet](../../power-platform/enable-power-platform-integration.md#enable-after-deploy)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Konfigurere dobbeltskrivning for nye Dataverse-miljøer

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

8. Når sammenkædningen er fuldført, vises der et link. Brug linket til at logge på administrationsområdet med dobbeltskrivning i Finance and Operations-miljøet. Herfra kan du oprette objekttilknytninger.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Konfigurere dobbeltskrivning for et eksisterende Dataverse-miljø

Hvis du vil konfigurere dobbeltskrivning for et eksisterende Dataverse-miljø, skal du oprette en Microsoft-[supportanmodning](../../lifecycle-services/lcs-support.md). Anmodningen skal indeholde:

+ Dit Finance and Operations-miljø-id.
+ Dit miljønavn fra Lifecycle Services.
+ Dataverse-organisations-id'et eller Power Platform-miljø-id'et fra Power Platform Administration. I din anmodning skal du anmode om, at id'et skal være den forekomst, der bruges til Power Platform-integration.

> [!NOTE]
> Du kan ikke fjerne sammenkædningen mellem miljøer ved hjælp af LCS. Hvis du vil fjerne sammenkædningen mellem et miljø, skal du åbne arbejdsområdet **Dataintegration** i Finance and Operations-miljøet og derefter vælge **Fjern sammenkædning**.

## <a name="linking-mismatch"></a>Uoverensstemmende sammenkædning

Det er muligt, at LCS-miljøet er kædet sammen med én Dataverse-forekomst, mens dit dobbeltskrivningsmiljø er knyttet til en anden Dataverse-forekomst. Denne uoverensstemmende sammenkædning kan medføre uventede funktionsmåder, og det kan ende med, at der sendes data til det forkerte miljø. Det anbefalede miljø, der skal bruges til dobbeltskrivning, er det, der oprettes som en del af Power Platform-integrationen, som på sigt vil være den eneste forbindelse mellem miljøer.

Hvis dit miljø her uoverensstemmende sammenkædning, viser LCS en advarsel på siden med dine miljøoplysninger i stil med "Microsoft har registreret, at dit miljø er kædet sammen via dobbeltskrivning til en anden destination end den, der er angivet i Power Platform Integration, hvilket ikke anbefales":

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform-uoverensstemmelse mellem integrationslink.":::

Hvis denne fejl opstår, er der to muligheder alt efter dine behov:

+ [Fjern og genopret linket til dobbeltskrivningsmiljøer (Nulstil eller rediger sammenkædning)](relink-environments.md#scenario-reset-or-change-linking), som det er angivet på siden med dine LCS-miljødetaljer. Dette er den ideelle løsning, da du kan køre den uden Microsoft support.  
+ Hvis du vil beholde dit link i dobbeltskrivning, kan du bede Microsoft Support om hjælp til at ændre Power Platform-integrationen, så den bruger dit eksisterende Dataverse-miljø som dokumenteret i forrige afsnit.  

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
