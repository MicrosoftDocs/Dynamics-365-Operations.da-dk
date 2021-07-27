---
title: Modulet Indkøbskurvikon
description: I dette emne dækkes modulet for indkøbskurvikonet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.openlocfilehash: e0238e9d464fc1d44cbc5091638ac7270d5b6ae3
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479298"
---
# <a name="cart-icon-module"></a>Ikonmodul for indkøbskurv

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

I dette emne dækkes modulet for indkøbskurvikonet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.

Modulet Indkøbskurvikon repræsenterer indkøbsvognen i overskriftmodulet på siden, og det viser antallet af varer i en indkøbsvogn. Modulet Indkøbskurvikon viser også en indkøbsvognoversigt (også kaldet en minivogn), når der peges på ikonet for indkøbsvognen. Minivognen giver brugeren en oversigt over varerne i indkøbsvognen uden at skulle navigere til siden med indkøbsvogn. Derudover giver det også brugeren mulighed for at gå direkte til betalingssiden, hvis man er tilfreds med oversigten. Det reducerer antallet af sidenavigeringer, og gør betalingen hurtigere. 

Følgende billede viser et eksempel på et indkøbskurvikonmodul, der viser en minivogn i Fabrikam-hovedet.

![Eksempel på et ikonmodul for indkøbsvogn.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Modulegenskaber

- **Vis minivogn** – Hvis sand, aktiverer denne egenskab en indkøbsvognoversigt (minivogn), som vises, når man peger på indkøbsvognens ikon. Denne funktionalitet understøttes kun ved visning på skrivebordet.

## <a name="module-properties-in-the-adventure-works-theme"></a>Modulegenskaber i emnet Adventure Works

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
