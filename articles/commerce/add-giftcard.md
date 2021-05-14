---
title: Gavekortmodul
description: I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962757"
---
# <a name="gift-card-module"></a>Gavekortsmodul

[!include [banner](includes/banner.md)]

I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Gavekortmoduler kan bruges i betalingsmoduler til at acceptere gavekort og er en almindelig betalingsform i e-handelstransaktioner. Gavekortmodulet understøtter Dynamics 365-, SVS- og Givex-gavekort. SVS- og Givex-gavekort indløses via betalingsudbyderen Adyen. Du kan se flere oplysninger om understøttelse af eksterne gavekort som f.eks. SVS og Givex i emnet [Understøttelse af eksterne gavekort](./dev-itpro/gift-card.md).

> [!NOTE]
> Understøttelse til indløsning af SVS- og Givex-gavekort i betalingsprocessen er tilgængelig i Dynamics 365 Commerce version 10.0.11. 

Der er to tilgængelige gavekortmoduler:

- **Gavekort** – Dette modul kan bruges på en betalingsside til at indløse et gavekort som betalingsmiddel. 
- **Saldokontrol for gavekort** – Dette modul kan bruges på enhver side til at kontrollere saldoen for et gavekort. Dette modul er tilgængeligt i Commerce version 10.0.14 og nyere.

> [!NOTE]
> Understøttelse af saldokontrolmodulet til gavekort er tilgængelig i Dynamics 365 Commerce version 10.0.14.

Det følgende billede viser et eksempel på et gavekortmodul på en betalingsside.

![Eksempel på et gavekortmodul](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Modulegenskaber

- **Vis yderligere felter** – Denne egenskab definerer, hvilke felter der skal vises for gavekort ud over gavekortnummeret, der altid vises som standard. Nogle gavekort understøtter f.eks. visning af en pinkode, og andre understøtter visning af en pinkode og udløbsdato. Denne egenskab kan også angives til "Ingen", hvilket kun viser gavekortnummeret og ingen yderligere felter.

Understøttede værdier:
-   Pinkode
-   Udløbsdato
-   Pinkode og udløbsdato 
-   None

## <a name="site-settings-for-gift-card-modules"></a>Indstillinger for websted for gavekortmoduler

I Commerce-webstedsgenerator under **Indstillinger for websted \> Udvidelser** er der en indstilling for gavekortmodulet, der kaldes **Understøttet gavekorttype**. Denne indstilling understøtter tre værdier:
- **Dynamics 365-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsning af Dynamics 365-gavekort. Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.
- **SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsning af SVS- og Givex-gavekort. Denne indstilling understøttes for anonyme brugere og brugere, der er logget på e-handelswebstedet.
- **Dynamics 365-, SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet indløsning af Dynamics 365-, Givex- og SVS-gavekort. Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.

> [!IMPORTANT]
> Disse indstillinger er tilgængelige i Dynamics 365 Commerce version 10.0.11 og er kun nødvendige, hvis du har brug for understøttelse af SVS- eller Givex-gavekort. Hvis du opdaterer fra en ældre version af Dynamics 365 Commerce, skal du opdatere filen appsettings.json manuelt. Oplysninger om opdatering af filen appsettings.json finder du under [Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a>Udvide interne gavekort til brug i udstillingsvinduer for e-handel

Interne gavekort er som standard ikke optimeret til brug i udstillingsvinduer for e-handel. Før du tillader brug af interne gavekort til betaling, skal du konfigurere dem med udvidelser, der gør dem mere sikre. Her er de gavekortområder, som du skal udvide, før du tillader, at interne gavekort bruges i produktionen:

- **Gavekortnummer** – Nummerserier bruges til generering af gavekortnumre til interne gavekort. Da nummerserier er forudsigelige, skal du udvide genereringen af gavekortnumre, så der anvendes tilfældige og kryptografisk sikre strenge til de gavekortnumre, der udstedes.
- **GetBalance** – API'en for **GetBalance** bruges til at få vist gavekortsaldi. Denne API er som standard offentlig. Hvis der ikke kræves en PIN-kode for at få vist gavekortsaldi, er der risiko for, at brute force-angreb kan bruge API'en for **GetBalance** til at forsøge at få vist gavekortnumre med saldi. Når du implementerer både PIN-krav for interne gavekort og API-begrænsning, kan du reducere risikoen.
- **PIN-kode** – Interne gavekort understøtter som standard ikke PIN-koder. Du skal udvide interne gavekort, så der kræves en PIN-kode for at få vist saldi. Denne funktionalitet kan også bruges til at låse gavekort efter flere forkerte forsøg på at indtaste PIN-koden.

## <a name="enable-gift-card-payments-for-guest-checkout"></a>Aktivere gavekortbetalinger for gæsters betaling

Som standard er gavekortbetalinger ikke aktiveret for gæsters (anonyme) betaling. Hvis du vil aktivere denne funktion, skal du benytte denne fremgangsmåde.

1. I Commerce-hovedkvarteret skal du gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS \> POS-handlinger**.
1. Vælg og hold (eller højreklik på) gitterhovedet, og vælg derefter **Indsæt kolonner**.
1. Markér afkrydsningsfeltet **AllowChecknymousAccess** i dialogboksen **Indsæt kolonner**.
1. Vælg **Opdater**.
1. For handlingerne **520** (gavekortsaldo) og **214** skal du angive værdien for **AllowSynonymousAccess** til **1**.
1. Vælg **Gem**.
1. Kør planlægningsjobbet **1090** for at synkronisere ændringerne med kanaldatabasen. 

## <a name="add-a-gift-card-module-to-a-page"></a>Føje et gavekortmodul til en side

Du kan få flere oplysninger om, hvordan du føjer et gavekortmodul til en betalingsside og angiver de påkrævede egenskaber, i [Betalingsmodul](add-checkout-module.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Indkøbskurvsmodul](add-cart-module.md)

[Ikonmodul for indkøbskurv](cart-icon-module.md)

[Betalingsmodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Leveringsindstillingsmodul](delivery-options-module.md)

[Modul med afhentningsoplysninger](pickup-info-module.md)

[Ordredetaljer-modul](order-confirmation-module.md)

[Understøttelse af eksterne gavekort](./dev-itpro/gift-card.md)

[Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
