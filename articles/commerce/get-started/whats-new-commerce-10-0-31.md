---
title: Prøveversion af Dynamics 365 Commerce 10.0.31 (februar 2023)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Commerce 10.0.31.
author: josaw1
ms.date: 10/18/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-10-01
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: ed4325095163415d05a56128cb1f0334440fe0e5
ms.sourcegitcommit: c364f50ea0ad50bac5c30724b6ce301d9574b653
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2022
ms.locfileid: "9787520"
---
# <a name="preview-of-dynamics-365-commerce-10031-february-2023"></a>Prøveversion af Dynamics 365 Commerce 10.0.31 (februar 2023)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikel viser funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Commerce forhåndsversion 10.0.31. Denne version har et build-nummer på 10.0.1406 og er tilgængelig i følgende plan:

- **Prøveversion:** oktober 2022
- **Generel tilgængelighed af version (selv-opdatering):** januar 2023
- **Generel tilgængelighed af version (automatisk opdatering):** februar 2023

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Vi opdaterer muligvis denne artikel for at medtage funktioner i det build, som er foretaget, efter denne artikel blev udgivet.

| Funktionsområde | Funktion | Flere oplysninger | Aktiveret af   |
|---|---|---|---|
| Fejlkoder | Commerce har indført standardfejlreferencer, der kan inkluderes i fejl ved betaling via onlinekanal, som vises for onlinekunder.| [Fejlkoder i betalingsmodul](../checkout-module-error-codes.md)  | Til som standard |
| Betalinger | [aktivere Apple Pay med Dynamics 365 Payment Connector til Adyen](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-apple-pay-dynamics-365-payment-connector-adyen)  | E-handelskunder kan bruge Apple Pay på indkøbskurv- og betalingssider ved hjælp af understøttede enheder eller browsere. | Tilmelding af udvikler |
| Betalinger  |  Commerce har tilføjet en egenskab for at begrænse, hvordan brugere anvender tilbagevendende betalingstokens overalt i Commerce headquarters-brugergrænsefladen. Betalingsformularer som f.eks. siden **Callcenter-salgsordrer**, viser ikke længere en kundes tidligere anvendte tilbagevendende betalingstoken til brug i en ny transaktion. Det er kun et bestemt "kort på fil"-input i Commerce-skærmbilledet **Debitorbetalinger** eller efter aftale med en kunde, når de betaler via en salgsordre, der vil blive vist for call center- eller Commerce headquarters-brugerne, når de behandler en betaling for en ny transaktion. | [Begræns brug af betalingstoken](../dev-itpro/limit-token-usage.md)  |  Administration af funktioner<p>*Begræns brugen af betalingstoken til ordrekonteksten*  |
| POS | [Oprette indkøbsordrer fra POS](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/create-purchase-orders-pos)  |  Forbedret handling af indgående lager i POS-programmet, så brugerne kan oprette, redigere og bekræfte indkøbsordreanmodninger. |  Administration af funktioner<p>*Mulighed for at oprette indkøbsordreanmodning i POS*   |
| Yderligere sprog er tilgængelige | Yderligere fire sprog er tilgængelige | Der findes fire nye sprog til brugervalg på listen over foretrukne sprog: Koreansk, Portugisisk (Portugal), Vietnamesisk og Kinesisk (traditionelt). Hvis du vil vælge denne indstilling, skal du gå til **Brugerindstillinger \> Præferencer \> Præferencer af sprog og land/område**. | Lokaliserede indstillinger |  



## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformsopdateringer til Finans- og driftsapps

Microsoft Dynamics 365 Commerce 10.0.31 inkluderer platformopdateringer. Du kan få mere vide i [Platformsopdateringer til version 10.0.31 af programmer til finans og drift (februar 2023)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-31.md). 
  

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af version 10.0.31, ved at logge på Microsoft Dynamics Lifecycle Services og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 2

Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?

Undersøg [Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 2](/dynamics365-release-plan/2022wave2/). Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.

### <a name="removed-and-deprecated-commerce-features"></a>Fjernede og udfasede Commerce-funktioner

Artiklen om [fjernede eller udfasede funktioner i Dynamics 365 Commerce](removed-deprecated-features-commerce.md) beskriver funktioner, der er blevet fjernet eller udfaset for Commerce.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Før en funktion fjernes fra produktet, vil du få besked om udfasning i artiklen [Fjernede eller udfasede funktioner i Dynamics 365 Commerce](removed-deprecated-features-commerce.md) 12 måneder, inden de fjernes.


For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Det er typisk funktionelle opdateringer, der skal foretages i compileren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
