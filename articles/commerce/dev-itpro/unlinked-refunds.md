---
title: Behandle refusioner, der ikke er sammenkædet med Dynamics 365 Commerce Payment Connector til Adyen
description: Denne artikel beskriver, hvordan ikke-sammenkædede refusioner fungerer, når Microsoft Dynamics 365 Payment Connector for Adyen bruges.
author: BrianShook
ms.date: 10/07/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 2b2bee7ad45bbff82c8b7de2741925fde29d8583
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284305"
---
# <a name="process-unlinked-refunds-with-the-dynamics-365-commerce-payment-connector-for-adyen"></a>Behandle refusioner, der ikke er sammenkædet med Dynamics 365 Commerce Payment Connector til Adyen

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan ikke-sammenkædede refusioner fungerer, når [Microsoft Dynamics 365 Payment Connector for Adyen](adyen-connector.md) bruges. De gennemser også muligheden for at behandle en refusion i forhold til en ny betalingsmåde i POS eller callcenter.

Dynamics 365 Payment Connector for Adyen understøtter muligheden for at behandle refusioner ved hjælp af en anden betalingsmetode end den, der blev brugt til den oprindelige transaktion. Selvom det anbefales, at du bruger [tilknyttede refusioner](linked-refunds.md) til at behandle en refusion i forhold til den oprindelige betalingsmåde, der er angivet, er refusioner af en anden metode påkrævet i visse scenarier. Det kort, der blev brugt til den oprindelige betaling, kan f.eks. nu være udløbet eller tabt, eller det kan være annulleret af brugeren.

## <a name="prerequisites"></a>Forudsætninger

Følgende forudsætninger skal være fuldført, før Dynamics 365 Payment Connector for Adyen kan behandle ikke-sammenkædede refusioner:

- Oprette [betalingsmåder](../payment-methods.md).
- Konfigurer [omni-kanal-betalinger](../omni-channel-payments.md).

## <a name="additional-configuration"></a>Yderligere konfiguration

Dynamics 365-betalingsconnector til Adyen indeholder en out-of-box-implementering for alle de understøttede refusionsscenarier, der beskrives i næste afsnit. Kunder, som ikke bruger den out-of-box-implementering af Dynamics 365 Payment Connector for Adyen, skal konfigurere den connector, der understøtter opdeling i tokens af kreditkort.

## <a name="supported-refund-scenarios"></a>Understøttede refusionsscenarier

Dynamics 365 Commerce understøtter refusioner af tidligere godkendte og bekræftede transaktioner. Refusioner kan bestå af enten en fuld refusion eller en delvis refusion af transaktionen. Refusioner kan ikke overstige det fulde beløb af den oprindelige betalingsgodkendelse. Ikke-sammenkædede refusioner understøttes kun i POS og call center.

## <a name="enable-unlinked-refunds-functionality"></a>Aktivere funktionen til ikke-sammenkædede refusioner

Hvis du vil aktivere funktionen for ikke-sammenkædede refusioner i Commerce Headquarters, skal du udføre disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af Headquarters \> Parametre \> Delte Commerce-parametre**.
1. Indstil derefter **Brug omni-kanalbetalinger** til **Ja** på fanen **Omni-kanalbetalinger**.

### <a name="supported-payment-method-variants"></a>Understøttede betalingsmetodevarianter

Følgende betalingsmetodevarianter understøtter ikke-sammenkædede refusioner ud af feltet:

- Kort
- Tegnebog

Ikke alle betalingsmetodevarianter understøtter refusioner, der ikke er sammenkædet. Følgende tabel indeholder en liste over almindelige betalingsmåder og viser hver enkelt metodes supportfunktionalitet for sammenkædede og ikke-sammenkædede refusioner.

| Betalingsmetode        | Sammenkædet refusion | Ikke-sammenkædet refusion |
|-----------------------|:-------------:|:---------------:|
| amexcommercial        | Ja           | Ja             |
| amexconsumer          | Ja           | Ja             |
| amexcorporate         | Ja           | Ja             |
| amexdebit             | Ja           | Ja             |
| amexprepaid           | Ja           | Ja             |
| amexprepaidreloadable | Ja           | Ja             |
| amexsmallbusiness     | Ja           | Ja             |
| find              | Ja           | Ja             |
| maestro               | Ja           | Ja             |
| maestrouk             | Ja           | Ja             |
| mc                    | Ja           | Ja             |
| mcalphabankbonus      | Ja           | Ja             |
| mcprepaidanonymous    | Ja           | Ja             |
| visa                  | Ja           | Ja             |
| visaalphabankbonus    | Ja           | Ja             |
| visacheckout          | Ja           | Ja             |
| visadankort           | Ja           | Ja             |
| visahipotecario       | Ja           | Ja             |
| visasaraivacard       | Ja           | Ja             |
| vpay                  | Ja           | Ja             |
| givex                 | **Nej**        | Ja             |
| svs                   | **Nej**        | Ja             |
| cup                   | Ja           | Ja             |
| diners                | Ja           | Ja             |
| interac               | **Nej**        | Ja             |
| jcb                   | Ja           | Ja             |
| jcb_applepay          | Ja           | Ja             |
| unionpay              | Ja           | Ja             |

### <a name="process-an-unlinked-refund-in-pos"></a>Behandle en refusion, der ikke er sammenkædet i POS

En kunde returnerer en vare til en POS-kasserer inden for den tilladte periode for returneringer og har en gyldig kvittering. Under returneringens returnering indeholder dialogboksen **Returbetaling** en indstilling for **valg af betalingsmåde**. Kassereren kan derefter vælge en betalingsmetode blandt de understøttede betalingsmåder til refundering (kort og kort).

### <a name="process-an-unlinked-refund-in-call-center"></a>Behandle en refusion, der ikke er sammenkædet i call center

Når der behandles en ikke-sammenkædet refusion mod en ordre i callcenter, vælger en callcenter-medarbejder en betalingsmåde, der er forskellig fra den oprindelige metode. Medarbejderen bliver derefter bedt om at få vist en PIN-kode til ændring af administratorens personlige identifikationsnummer. Pinkoden skal bruges, før den anden betalingsmåde kan behandles med henblik på refusionen.

#### <a name="set-up-an-administrator-override-pin-for-call-center"></a>Konfigurere en pinkode til administratorændring for callcenter

Hvis du vil konfigurere en administratorændrings-PIN for callcenter i Commerce headquarters, skal du følge disse trin.

1. Gå til **Opsætning af callcenter \> Detail og handel \> Kanalopsætning**, eller søg efter "Tilsidesæt tilladelser".
1. Vælg den rolle, der skal tillades tilladelser til ikke-sammenkædet behandling af refusion for.
1. Indstil **Tillad alternativ betaling** til **Ja** i oversigtspanelet **Returneringer**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dynamics 365 Payment Connector til Adyen](adyen-connector.md)

[Sammenkædede refusioner af tidligere godkendte og bekræftede transaktioner](linked-refunds.md)
