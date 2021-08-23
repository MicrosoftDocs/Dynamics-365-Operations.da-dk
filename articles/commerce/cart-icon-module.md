---
title: Modulet Indkøbskurvikon
description: I dette emne dækkes modulet for indkøbskurvikonet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5cf86876ba03d510b03237c9c89a1fc069a73482b755a1d72227037c91439e86
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735672"
---
# <a name="cart-icon-module"></a>Ikonmodul for indkøbskurv

[!include [banner](includes/banner.md)]

I dette emne dækkes modulet for indkøbskurvikonet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.

Modulet Indkøbskurvikon repræsenterer indkøbsvognen i overskriftmodulet på siden, og det viser antallet af varer i en indkøbsvogn. Modulet Indkøbskurvikon viser også en indkøbsvognoversigt (også kaldet en minivogn), når der peges på ikonet for indkøbsvognen. Minivognen giver brugeren en oversigt over varerne i indkøbsvognen uden at skulle navigere til siden med indkøbsvogn. Derudover giver det også brugeren mulighed for at gå direkte til betalingssiden, hvis man er tilfreds med oversigten. Det reducerer antallet af sidenavigeringer, og gør betalingen hurtigere. 

Følgende billede viser et eksempel på et indkøbskurvikonmodul, der viser en minivogn i Fabrikam-hovedet.

![Eksempel på et ikonmodul for indkøbsvogn.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Modulegenskaber

- **Vis minivogn** – Hvis denne egenskab er **Sand**, vises en indkøbsvognoversigt (minivogn), når brugere peger på indkøbsvognens ikon. Denne funktionalitet understøttes kun ved visning på skrivebordet.
- **Tillad anonym betaling** – Når denne egenskab er angivet til **Sand**, giver minvognen brugere, som ikke er logget på, tilladelse til at betale ved kassen som gæst. Denne egenskab er tilgængelig i Commerce version 10.0.21 som en del af Commerce-modulets bibliotekspakke.
- **Varerækkefølge** – Denne egenskab styrer den rækkefølge, som varerne vises i i indkøbsvognen. Når du vælger indstillingen **Nye varer tilføjet øverst på listen**, vises nye varer, der føjes til indkøbsvognen, øverst på listen over varer i indkøbsvognen. Når du vælger standardindstillingen **Nye varer tilføjet nederst på listen**, vises nye varer, der føjes til indkøbsvognen, nederst på listen over varer i indkøbsvognen. Denne egenskab er tilgængelig fra og med Commerce version 10.0.21 som en del af Commerce-modulets bibliotekspakke.

> [!IMPORTANT]
> Egenskaberne **Tillad anonym betaling** og **Varerækkefølge** er tilgængelige fra og med Commerce version 10.0.21. De kræver, at Commerce-modulets bibliotekspakkeversion 9.31 er installeret.

## <a name="module-properties-and-slots-in-the-adventure-works-theme"></a>Modulegenskaber og pladser i emnet Adventure Works

I emnet Adventure Works indeholder ikonet for indkøbsvognen to ekstra oplysninger om rullevognen. Disse filtyper inkluderes som en moduldefinitionsudvidelse.

- **Tomme indkøbsvognskampagner** – Dette område kræver et indholdsblokmodul. Når indkøbsvognen er tom, vises det angivne indholdsblokmodul. Modulet til indholdsblokering kan bruges til kampagner, marketingindhold og links til kategorisider for at hjælpe kunderne med at fortsætte deres indkøbsmuligheder.
- **Kampagneindhold** – Dette spil kan bruges til kampagner, som f.eks. "Gratis forsendelse for ordrer $100". Der kan bruges indholdsblok-, tekstblok- og billedlistemoduler i det markedsføringsindholdsinterval.

Følgende billede viser et eksempel på et modul med et ikon for en indkøbsvogn i emnet Adventure Works, der viser kampagneindhold i rullevognen.

![Eksempel på et modul med et indkøbsvognsikon med emnet Adventure Works](./media/AW_minicart.PNG)

> [!IMPORTANT]
> Emnet Adventure Works er tilgængelige pr. Dynamics 365 Commerce version 10.0.20.

## <a name="add-a-cart-icon-module-to-a-page"></a>Føje et indkøbskurvikonmodul til en side

Hvis du vil tilføje et indkøbsvognikonmodul, skal du se [Overskriftsmodul](author-header-module.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Indkøbskurvsmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Leveringsindstillingsmodul](delivery-options-module.md)

[Modul med afhentningsoplysninger](pickup-info-module.md)

[Ordredetaljer-modul](order-confirmation-module.md)

[Gavekortsmodul](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
