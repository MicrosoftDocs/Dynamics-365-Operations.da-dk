---
title: Ofte stillede spørgsmål om asynkron oprettelsestilstand for kunde
description: Denne artikel indeholder svar på ofte stillede spørgsmål om asynkron oprettelsestilstand for kunde i Microsoft Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 35c999695ed33c4fc9731a5b8dd4d679cf55fa44
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229868"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>Ofte stillede spørgsmål om asynkron oprettelsestilstand for kunde

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Denne artikel indeholder svar på ofte stillede spørgsmål om asynkron oprettelsestilstand for kunde i Microsoft Microsoft Dynamics 365 Commerce.

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>Hvorfor kan jeg ikke aktivere funktionen "Aktivér redigering af kunder i asynkron tilstand"?

Før du aktiverer funktionen **Aktivér redigering af kunder i asynkron tilstand**, skal du aktivere følgende funktioner:

- Ydelsesforbedringer for kundeordrer og kundetransaktioner
- Aktivér udvidet asynkron kundeoprettelse
- Aktivér asynkron oprettelse af kundeadresser

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>Hvorfor kan jeg stadig se realtidsserviceopkald, der er foretaget til Commerce headquarters, efter funktionen "Aktivér redigering af kunder i asynkron tilstand" er aktiveret?

Dette problem opstår, når Commerce Data Exchange-job (CDX) ikke er blevet kørt, for at sikre, at funktionstilstanden og andre kanalmetadata synkroniseres med kanalen. Før du forsøger at køre scenariet igen, skal du sikre dig, at følgende CDX-job køres Commerce headquarters:

- 1110 (global konfiguration)
- 1010 (kunder)
- 1070 (kanalkonfiguration)

Data, der cachelagres i CSU (Commerce Scale Unit), afspejles muligvis ikke omgående i Commerce headquarters, når CDX-job er blevet kørt.

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>Hvorfor viser Commerce headquarters ikke kundeoprettelse eller -opdateringer fra POS eller e-handelskanal?

Kontrollér, at følgende handlinger er udført i den rækkefølge, de er angivet i her.

1. Kør CDX P-job i Commerce headquarters for at sikre, at der er adgang til de asynkrone kundedata, der er gemt i tabellerne **RETAILASYNCCUSTOMERV2**, **RETAILASYNCADDRESSV2**, **RETAILASYNCCUSTOMERCONTACT**, **RETAILASYNCCUSTOMERAFFILIATION** og **RETAILASYNCCUSTOMERATTRIBUTEV2**, i Commerce headquarters.
1. Kør batchjobbet **Synkroniser kunder og kanalanmodninger** i Commerce headquarters. Når batchjobbet er udført korrekt, angives feltet **OnlineOperationCompleted** til **1** for alle poster, der er behandlet korrekt fra de tidligere nævnte tabeller.
