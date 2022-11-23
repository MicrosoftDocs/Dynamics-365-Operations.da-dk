---
title: Dynamics 365 Payment Connector til Adyen, oversigt
description: Denne artikel giver et overblik over Microsoft Dynamics 365 Payment Connector til Adyen.
author: rassadi
ms.date: 11/16/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.openlocfilehash: 6c819e8cf9f5dcb7895ac2633decf0a925c08f2d
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2022
ms.locfileid: "9784986"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>Dynamics 365 Payment Connector til Adyen, oversigt

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over Microsoft Dynamics 365 Payment Connector til Adyen med en omfattende liste over understøttede funktioner. Relaterede artikler dækker Adyen-tilmelding, konfiguration af connectoren, ofte stillede spørgsmål og vejledning til fejlfinding af nogle af de almindelige problemer.

## <a name="key-terms"></a>Vigtige termer

| Periode | Beskrivende tekst |
|---|---|
| Betalingsconnector | En udvidelse, der letter kommunikationen mellem Microsoft Dynamics 365 Commerce (og tilknyttede komponenter) og en betalingstjeneste. Den connector, der er beskrevet i denne artikel, blev implementeret ved hjælp af standard-SDK'et (Software Development Kit) til betalinger. |
| Der findes et kort | Henviser til betalingstransaktioner, hvor der vises et fysisk kort, som bruges på en betalingsterminals connector til Dynamics 365 POS. |
| Der findes ikke et kort | Refererer til betalingstransaktioner, hvor der ikke findes et fysisk kort, f.eks. e-handel eller callcenter-scenarier. I disse scenarier angives betalingsrelaterede oplysninger manuelt på enten et e-handelswebsted, i et callcenterflow eller på en POS- eller betalingsterminal. |

## <a name="supported-features-functionality-versions-and-terminals"></a>Understøttede faciliteter, funktioner, versioner og terminaler

Dynamics 365 Payment Connector til Adyen bruger standardbetalings-SDK. Den har derfor ikke specielle egenskaber, som andre betalingsconnectorer ikke også kan bruge.

### <a name="supported-versions"></a>Understøttede versioner

#### <a name="microsoft-dynamics-365-supported-versions"></a>Microsoft Dynamics 365-understøttede versioner
Den første indbyggede Dynamics 365 Payment Connector til Adyen understøttes i Microsoft Dynamics 365 Finance version 8.1.3 (januar 2019) eller senere og i Microsoft Dynamics 365 Retail version 8.1.3 (2019) eller senere. Men tredjeparter kan stadig udvikle andre betalingsconnectorer til Adyen til tidligere versioner af Microsoft Dynamics 365.

#### <a name="supported-adyen-firmware-versions"></a>Understøttede firmwareversioner af Adyen

I nedenstående liste beskrives de minimum- og maksimumversioner af Adyen-firmware, der understøttes for hver version af Microsoft Dynamics 365 Retail POS.

---

# <a name="10025"></a>[10.0.25](#tab/10-0-25)
### <a name="dynamics-365-retail-pos-version-10025"></a>Dynamics 365 Retail POS version 10.0.25
| Minimumversion af Adyen Firmware | Maksimumversion af Adyen Firmware |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_73p6 |

# <a name="10026"></a>[10.0.26](#tab/10-0-26)
### <a name="dynamics-365-retail-pos-version-10026"></a>Dynamics 365 Retail POS version 10.0.26
| Minimumversion af Adyen Firmware | Maksimumversion af Adyen Firmware |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10027"></a>[10.0.27](#tab/10-0-27)
### <a name="dynamics-365-retail-pos-version-10027"></a>Dynamics 365 Retail POS version 10.0.27
| Minimumversion af Adyen Firmware | Maksimumversion af Adyen Firmware |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10028"></a>[10.0.28](#tab/10-0-28)
### <a name="dynamics-365-retail-pos-version-10028"></a>Dynamics 365 Retail POS version 10.0.28
| Minimumversion af Adyen Firmware | Maksimumversion af Adyen Firmware |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p22 |

# <a name="10029"></a>[10.0.29](#tab/10-0-29)
### <a name="dynamics-365-retail-pos-version-10029"></a>Dynamics 365 Retail POS version 10.0.29
| Minimumversion af Adyen Firmware | Maksimumversion af Adyen Firmware |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

# <a name="10030"></a>[10.0.30](#tab/10-0-30)
### <a name="dynamics-365-retail-pos-version-10030"></a>Dynamics 365 Retail POS version 10.0.30
| Minimumversion af Adyen Firmware | Maksimumversion af Adyen Firmware |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

---

> [!NOTE]
> Adyen kan frigive mindre versionsopdateringer, efter at Microsoft har testet den overordnede version. Så længe en overordnet version understøttes, er det i orden at have mindre versionsopdateringer i samme overordnede version. Disse opdateringer er normalt meget konkrete rettelser og opfylder ikke forudsætningen for fuld gentest, så længe den samme overordnede firmwareversion er blevet testet tidligere. Opdateringer bør ikke overstige den maksimumversion af Adyen-firmware, der er angivet i dokumentationen. 
>
> Hvis du vil overføre fra en version af Adyen-firmware, der er ældre end version 53, til version 53, skal der være POS KB **4577957** for månedlige opdateringer af Commerce version 10.0.11 til 10.0.14. Hvis en af disse versioner er i brug og ikke omfatter hotfixet, tillader efteropgraderingen af betalingsterminalen kun betalinger via NFC. Når du anvender hotfixet på POS, løses dette problem. Hvis POS-versionen er ældre end version 10.0.11, skal du indsende en supportanmodning med en anmodning om, at der kræves en rettelse til KB **4577957** for en MPOS, der ikke er i drift.
> 
> For Adyen-firmwareversioner fra 59p7 til og med 62p9 anmoder handlingen **Udbetaling på gavekort** om PIN-indtastning to gange i scenarier, hvor gavekortet angives manuelt. Dette problem gentages ikke, når gavekortet swipes. Adyen undersøger sagen. 

### <a name="supported-payment-terminals"></a>Understøttede betalingsterminaler
Dynamics 365 Payment Connector til Adyen benytter enhedsagnostikken [Adyen-betalingsterminal-API](https://www.adyen.com/blog/introducing-the-terminal-api). Den understøtter alle betalingsterminaler, som denne API (Application Programming Interface) understøtter. Du kan se en komplet liste over understøttede betalingsterminaler på siden [Adyen POS-terminaler](https://www.adyen.com/pos-payments/terminals).

I følgende video beskrives egenskaberne for betalingsterminalen Adyen Castles SE1 Android.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5bKeM]

### <a name="supported-payment-instruments"></a>Understøttede betalingsmidler

#### <a name="supported-debit-and-credit-cards"></a>Understøttede debet- og kreditkort

| Brand | Variant | Der findes et kort | e-handel | Callcenter |
|---|---|:-:|:-:|:-:|
| MasterCard | Kredit | ✔ | ✔ | ✔ |
| MasterCard | Debet | ✔ | ✔ | ✔ |
| MasterCard | Alpha Bank Bonus | ✔ | ✔ | ✔ |
| MasterCard | Apple Pay | ✔ |  |  |
| MasterCard | Samsung Pay | ✔ |  |  |
| MasterCard | Maestro | ✔ | ✔ | ✔ |
| MasterCard | Maestro Samsung Pay | ✔ |  |  |
| MasterCard | Maestro UK | ✔ | ✔ | ✔ |
| VISA | Kredit | ✔ | ✔ | ✔ |
| VISA | Debet | ✔ | ✔ | ✔ |
| VISA | Alpha Bank Bonus | ✔ | ✔ | ✔ |
| VISA | Android Pay | ✔ |  |  |
| VISA | Apple Pay | ✔ |  |  |
| VISA | Samsung Pay | ✔ |  |  |
| VISA | VISA Checkout | ✔ | ✔ | ✔ |
| VISA | VISA Dankort | ✔ | ✔ | ✔ |
| VISA | VISA Hipotecario | ✔ | ✔ | ✔ |
| VISA | VISA Aravia Card | ✔ | ✔ | ✔ |
| AMEX | Kredit | ✔ | ✔ | ✔ |
| AMEX | Debet | ✔ | ✔ | ✔ |
| AMEX | Android Pay | ✔ |  |  |
| AMEX | Apple Pay | ✔ |  |  |
| AMEX | Samsung Pay | ✔ |  |  |
| AMEX | AMEX Commercial | ✔ | ✔ | ✔ |
| AMEX | AMEX Consumer | ✔ | ✔ | ✔ |
| AMEX | AMEX Corporate | ✔ | ✔ | ✔ |
| AMEX | AMEX Small Business | ✔ | ✔ | ✔ |
| Find | Standard | ✔ | ✔ | ✔ |
| Find | Android Pay | ✔ |  |  |
| Find | Apple Pay | ✔ |  |  |
| Find | Samsung Pay | ✔ |  |  |
| Diners   | Standard | ✔ | ✔ | ✔ |
| Dineromail | Standard | ✔ | ✔ | ✔ |
| JCB | Standard | ✔ | ✔ | ✔ |
| Union Pay\* | Standard | ✔ |  |  |
| Interac Debit\* | Standard | ✔ |  |  |

\*Adyen leverer ikke tilbagevendende korttokens til Interac- og Union Pay-kort, så de kan ikke understøttes for transaktioner uden kort.

#### <a name="supported-gift-cards"></a>Understøttede gavekort
| Skema | Der findes et kort | Der findes ikke et kort |
|---|:-:|---|
| Givex | ✔ | ✔ |
| SVS | ✔ | ✔ |

Hvis du vil understøtte disse eksterne gavekortskemaer via Dynamics 365 Payment Connector til Adyen, skal du udføre yderligere trin. Du kan finde flere oplysninger under [Understøttelse af eksterne gavekort](/dynamics365/unified-operations/retail/dev-itpro/gift-card).

#### <a name="supported-wallets"></a>Understøttede tegnebøger

| Skema | Der findes et kort | Der findes ikke et kort |
|---|---|---|
| Alipay | Understøttelse tilføjes i en senere version. | Nej |
| WeChat | Understøttelse tilføjes i en senere version. | Nej |

#### <a name="supported-card-present-input-methods"></a>Understøttede inputmetoder, når der findes et kort
| Inputmetode | Understøttet | Notater |
|---|:-:|---|
| Stik ned | ✔ | |
| Stryg | ✔ | |
| Tryk | ✔ | |
| Manuel indtastning via POS-brugergrænsefladen. |  | Understøttes ikke i øjeblikket |
| Manuel indtastning via betalingsterminal. | ✔ | Understøtter manuel indtastning af kredit-, debet- og gavekort med pinkode. | 


#### <a name="supported-card-present-countries"></a>Understøttede lande/områder, når der findes et kort

Følgende lande/områder har tilgængelige Commerce-komponenter og understøttelse af kort fra Adyen. Du kan se, om der aktuelt er international tilgængelighed af Commerce, ved at gå til [siden International tilgængelighed](/dynamics365/get-started/availability).

| Land/område | Understøttet |
| --- | :-: |
| Australien | ✔ |
| Østrig | ✔ |
| Belgien | ✔ |
| Canada | ✔ |
| Tjekkiet | ✔ |
| Danmark | ✔ |
| Estland | ✔ |
| Finland | ✔ |
| Frankrig | ✔ |
| Tyskland | ✔ |
| Hong Kong SAR | ✔ |
| Ungarn | ✔ |
| Island | ✔ |
| Irland | ✔ |
| Italien | ✔ |
| Japan | Fremtidig version |
| Letland | ✔ |
| Litauen | ✔ |
| Malaysia | ✔ |
| Nederlandene | ✔ |
| New Zealand | ✔ |
| Norge | ✔ |
| Polen | ✔ |
| Singapore | ✔ |
| Schweiz | ✔ |
| Spanien | ✔ |
| Sverige | ✔ |
| Schweiz | ✔ |
| Storbritannien | ✔ |
| United States | ✔ |
| Brasilien | Fremtidig version |

#### <a name="supported-card-not-present-countries"></a>Understøttede lande/områder, når der ikke findes et kort

Følgende lande/områder understøttes af Adyen til transaktioner, når der ikke findes et kort. [Kontakt Adyen](https://www.adyen.com/contact/sales) for at få oplysninger om understøttelse for et bestemt land/område. Du kan se, om der aktuelt er international tilgængelighed af Commerce, ved at gå til [siden International tilgængelighed](/dynamics365/get-started/availability).

| Land/område | 
| --- |
| Argentina |
| Armenien |
| Australien |
| Østrig |
| Bahrain |
| Belgien |
| Brasilien |
| Bulgarien |
| Canada |
| Chile |
| Kina |
| Colombia |
| Kroatien |
| Cypern |
| Tjekkiet  |
| Danmark |
| Egypten |
| Estland |
| Finland |
| Frankrig |
| Georgia |
| Tyskland |
| Gibraltar |
| Grækenland |
| Guernsey |
| Hong Kong SAR |
| Ungarn |
| Island |
| Indien |
| Indonesien |
| Irland |
| Isle of Man |
| Israel |
| Italien |
| Japan |
| Jersey |
| Korea |
| Kuwait |
| Letland |
| Litauen |
| Luxembourg |
| Malaysia |
| Malta |
| Mexico |
| Marokko |
| Nederlandene |
| New Zealand |
| Norge |
| Peru |
| Polen |
| Portugal |
| Qatar |
| Rumænien |
| Saudi-Arabien |
| Serbien |
| Singapore |
| Slovakiet |
| Slovenien |
| Sydafrika |
| Spanien |
| Sverige |
| Schweiz |
| Taiwan |
| Tanzania |
| Thailand |
| Tyrkiet |
| De Forenede Arabiske Emirater (UAE) |
| Storbritannien |
| USA, herunder Puerto Rico  |

#### <a name="supported-dynamics-365-payment-features"></a>Understøttede Dynamics 365-betalingsfunktioner

Følgende tabel viser det sæt funktioner, som Dynamics 365 Payment Connector til Adyen understøtter. Disse funktioner bruger forbedringer, der blev introduceret i betalings-SDK og visse komponenter i december 2018. De er ikke eksklusive for Dynamics 365 Payment Connector til Adyen. Du kan finde flere oplysninger om, hvordan disse forbedringer integreres med et anden betalingsconnector, i [Oprette komplet integration af betaling for en betalingsterminal](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension).

| Skema | Der findes et kort | Der findes ikke et kort |
|---|:-:|:-:|
| [Udbetaling af gavekortsaldo](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [Beskyttelse mod duplikerede betalinger](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| Opdeling i tokens for omni-kanaler | ✔ | ✔ |
| Sammenkædede refusioner | ✔<br>(Fra og med 10.0.1) | ✔<br>(Fra og med 10.0.1) |
| [Gemme onlinebetalinger](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>(Fra og med 10.0.2) | 
| [Eksterne gavekort til callcenter og e-handel](./gift-card.md) | ✔<br>(Fra og med 10.0.10) | 
| [Omdirigering til effektiv kundegodkendelse af betaling (SCA)](../adyen_redirect.md) | | ✔<br>(Fra og med 10.0.12) |
| [Dedikerede betalingsterminaler og anmodninger om printer og kasseterminal](../pos-multi-hws.md) | ✔<br>(Fra og med 10.0.12) | |
| [Understøttelse af drikkepenge på SDK-niveau via Adyen-connectoren](tipping.md) | ✔<br>(Fra og med 10.0.14) | |
| [Trinvis dataindlæsning til ordrefakturering](incremental-capture.md) |  | ✔<br>(Fra og med 10.0.18) |
| [Kontantbetalinger](../wallets.md) |  | ✔<br>(Fra og med 10.0.20) |
| [Google Pay med Adyen](google-pay-adyen.md) |  | ✔<br>(Fra og med 10.0.27) |

## <a name="next-steps"></a>Næste trin

Du kan finde oplysninger om tilmelding til og konfigurering af Dynamics 365 Payment Connector til Adyen i [Dynamics 365 Payment Connector til Adyen](adyen-connector-setup.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere Dynamics 365 Payment Connector til Adyen](adyen-connector-setup.md)

[Dynamics 365 Payment Connector til Adyen, ofte stillede spørgsmål](adyen-connector-faq.md)

[Fejlfinde Dynamics 365 Payment Connector til Adyen](adyen-connector-troubleshoot.md)

[Ofte stillede spørgsmål om betalinger](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
