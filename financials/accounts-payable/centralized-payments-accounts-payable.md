---
title: Centraliserede kreditorbetalinger
description: "Organisationer, der omfatter flere juridiske enheder, kan oprette og administrere betalinger via en enkelt juridisk enhed, der håndterer alle betalinger. Derfor skal de samme betalinger ikke angives i flere juridiske enheder. Denne artikel indeholder eksempler på, hvordan bogføring for centraliserede betalinger håndteres i forskellige scenarier."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: e7cc68b1b40b6a0361d7c215af466ae5a17a2aaa
ms.lasthandoff: 03/31/2017


---

# <a name="centralized-payments-for-accounts-payable"></a>Centraliserede kreditorbetalinger

[!include[banner](../includes/banner.md)]


Organisationer, der omfatter flere juridiske enheder, kan oprette og administrere betalinger via en enkelt juridisk enhed, der håndterer alle betalinger. Derfor skal de samme betalinger ikke angives i flere juridiske enheder. Denne artikel indeholder eksempler på, hvordan bogføring for centraliserede betalinger håndteres i forskellige scenarier.

Organisationer, der omfatter flere juridiske enheder, kan oprette og administrere betalinger via en juridisk enhed, der håndterer alle betalinger. Derfor skal de samme betalinger ikke angives i flere juridiske enheder. Derudover kan organisationen spare tid, fordi betalingsprocessen er strømlinet.

I organisationer med centraliserede betalinger er der mange juridiske driftsenheder, og hver juridisk driftsenhed administrerer sine egne kreditorfakturaer. Betalinger for alle juridiske driftsenheder genereres fra én juridisk enhed, der kaldes betalingens juridiske enhed. Under udligningsprocessen oprettes de gældende skyldig til- og skyldig fra-posteringer. Du kan angive, hvilken juridisk enhed i organisationen der skal modtage posteringerne af den realiserede gevinst eller det realiserede tab, og hvordan kasserabatposteringer, der er relateret til en betaling for hele virksomheden, skal håndteres. 

I følgende eksempler vises, hvordan bogføring håndteres i forskellige scenarier. Følgende konfiguration antages for alle disse eksempler:

-   De juridiske enheder er Fabrikam, Fabrikam East og Fabrikam West. Betalinger sker fra Fabrikam.
-   Feltet **Bogfør kasserabat** på siden **Mellemregning** er angivet til **Juridisk enhed for fakturaen**.
-   Feltet **Bogfør valutakurstab eller -vinding** på siden **Mellemregning** er angivet til **Juridisk enhed for betalingen**.
-   Kreditoren Fourth Coffee er oprettet som kreditor i de enkelte juridiske enheder. Kreditorerne fra de forskellige juridiske enheder er identificeret som den samme kreditor, fordi de deler det samme globale adresseadressekartoteks-id.

| Register-id | Kreditorkonto | Navn          | Juridisk enhed  |
|--------------|----------------|---------------|---------------|
| 1050         | 3004           | Fourth Coffee | Fabrikam      |
| 1050         | 100            | Fourth Coffee | Fabrikam East |
| 1050         | 3004           | Fourth Coffee | Fabrikam West |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a>Eksempel 1: Kreditorbetaling af faktura fra en anden juridisk enhed
Fabrikam East har en åben faktura for kreditorkonto 100, Fourth Coffee. Fabrikam registrerer og bogfører en betaling til Fabrikams kreditorkonto 3004, Fourth Coffee. Betalingen udlignes med den åbne faktura.

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a>Faktura bogføres i Fabrikam East for kreditor 100

| Konto                          | Debetbeløb | Kreditbeløb |
|----------------------------------|--------------|---------------|
| Udgift (Fabrikam East)          | 600,00       |               |
| Kreditor (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Betaling registreres og bogføres i Fabrikam for kreditor 3004

| Konto                     | Debetbeløb | Kreditbeløb |
|-----------------------------|--------------|---------------|
| Kreditor (Fabrikam) | 600,00       |               |
| Kontant (Fabrikam)             |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikams betaling udlignes med fakturaen fra Fabrikam East

**Fabrikam-bogføring**

| Konto                           | Debetbeløb | Kreditbeløb |
|-----------------------------------|--------------|---------------|
| Forfalden fra Fabrikam East (Fabrikam) | 600,00       |               |
| Kreditor (Fabrikam)       |              | 600,00        |

**Fabrikam East-bogføring**

| Konto                          | Debetbeløb | Kreditbeløb |
|----------------------------------|--------------|---------------|
| Kreditor (Fabrikam East) | 600,00       |               |
| Forfalden til Fabrikam (Fabrikam East)  |              | 600,00        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Eksempel 2: Kreditorbetaling af faktura fra en anden juridisk enhed med kasserabat
Fabrikam East har en åben faktura for kreditor 100, Fourth Coffee. Der er en kontantrabat på 20,00 for fakturaen. Fabrikam registrerer og bogfører en betaling på 580,00 for Fabrikam-kreditoren 3004, Fourth Coffee. Betalingen udlignes med de åbne fakturaer fra Fabrikam East. Kasserabatten bogføres på fakturaens juridiske enhed, Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Faktura bogføres i Fabrikam East for Fabrikam East-kreditoren 100

| Konto                          | Debetbeløb | Kreditbeløb |
|----------------------------------|--------------|---------------|
| Udgift (Fabrikam East)          | 600,00       |               |
| Kreditor (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Betaling registreres og bogføres i Fabrikam for Fabrikam-kreditoren 3004

| Konto                     | Debetbeløb | Kreditbeløb |
|-----------------------------|--------------|---------------|
| Kreditor (Fabrikam) | 580,00       |               |
| Kontant (Fabrikam)             |              | 580,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikams betaling udlignes med fakturaen fra Fabrikam East

**Fabrikam-bogføring**

| Konto                           | Debetbeløb | Kreditbeløb |
|-----------------------------------|--------------|---------------|
| Forfalden fra Fabrikam East (Fabrikam) | 580,00       |               |
| Kreditor (Fabrikam)       |              | 580,00        |

**Fabrikam East-bogføring**

| Konto                          | Debetbeløb | Kreditbeløb |
|----------------------------------|--------------|---------------|
| Kreditor (Fabrikam East) | 580,00       |               |
| Forfalden til Fabrikam (Fabrikam East)  |              | 580,00        |
| Kreditor (Fabrikam East) | 20,00        |               |
| Kasserabat (Fabrikam East)    |              | 20,00         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a>Eksempel 3: Kreditorbetaling af faktura fra en anden juridisk enhed med realiseret valutakurstab
Fabrikam East har en åben faktura for kreditor 100, Fourth Coffee. Fabrikam registrerer og bogfører en betaling for Fabrikam-kreditoren 3004, Fourth Coffee. Betalingen udlignes med den åbne faktura fra Fabrikam East. En valutakursFanerpostering genereres under udligningsprocessen.

-   Valutakurs for euro (EUR) til USD på fakturadatoen: 1,2062
-   Valutakurs for EUR til USD på betalingsdatoen: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Faktura bogføres i Fabrikam East for Fabrikam East-kreditoren 100

| Konto                          | Debetbeløb            | Kreditbeløb           |
|----------------------------------|-------------------------|-------------------------|
| Udgift (Fabrikam East)          | 600,00 EUR / 723,72 USD |                         |
| Kreditor (Fabrikam East) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Betaling registreres og bogføres i Fabrikam for Fabrikam-kreditoren 3004

| Konto                     | Debetbeløb            | Kreditbeløb           |
|-----------------------------|-------------------------|-------------------------|
| Kreditor (Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Kontant (Fabrikam)             |                         | 600,00 EUR / 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikams betaling udlignes med fakturaen fra Fabrikam East

**Fabrikam-bogføring**

| Konto                           | Debetbeløb            | Kreditbeløb           |
|-----------------------------------|-------------------------|-------------------------|
| Forfalden fra Fabrikam East (Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Kreditor (Fabrikam)       |                         | 600,00 EUR / 736,62 USD |
| Realiseret tab (Fabrikam)          | 0,00 EUR / 12,90 USD    |                         |
| Forfalden fra Fabrikam East (Fabrikam) |                         | 0,00 EUR / 12,90 USD    |

**Fabrikam East-bogføring**

| Konto                          | Debetbeløb            | Kreditbeløb           |
|----------------------------------|-------------------------|-------------------------|
| Kreditor (Fabrikam East) | 600,00 EUR / 736,62 USD |                         |
| Forfalden til Fabrikam (Fabrikam East)  |                         | 600,00 EUR / 736,62 USD |
| Forfalden til Fabrikam (Fabrikam East)  | 0,00 EUR / 12,90 USD    |                         |
| Kreditor (Fabrikam East) |                         | 0,00 EUR / 12,90 USD    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a>Eksempel 4: Kreditorbetaling af faktura fra en anden juridisk enhed med kasserabat og realiseret valutakurstab
Fabrikam East har en åben faktura for kreditor 100, Fourth Coffee. Der gælder en kontantrabat for fakturaen, og der oprettes en momspostering. Fabrikam bogfører en betaling for Fabrikam-kreditoren 3004, Fourth Coffee. Betalingen udlignes med den åbne faktura fra Fabrikam East. En valutakursFanerpostering genereres under udligningsprocessen. Kasserabatten bogføres på fakturaens juridiske enhed (Fabrikam East), og valutakurstabet bogføres på betalingens juridiske enhed (Fabrikam).

-   Valutakurs for EUR til USD pr. fakturadatoen: 1,2062
-   Valutakurs for EUR til USD pr. betalingsdatoen: 1,2277

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a>Fakturaen bogføres, og der oprettes en momspostering i Fabrikam East for kreditor 100

| Konto                          | Debetbeløb            | Kreditbeløb           |
|----------------------------------|-------------------------|-------------------------|
| Udgift (Fabrikam East)          | 564,07 EUR / 680,38 USD |                         |
| Moms (Fabrikam East)        | 35,93 EUR / 43,34 USD   |                         |
| Kreditor (Fabrikam East) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Betaling registreres og bogføres i Fabrikam for kreditor 3004

| Konto                     | Debetbeløb            | Kreditbeløb           |
|-----------------------------|-------------------------|-------------------------|
| Kreditor (Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Kontant (Fabrikam East)        |                         | 588,72 EUR / 722,77 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikams betaling udlignes med fakturaen fra Fabrikam East

**Fabrikam-bogføring**

| Konto                           | Debetbeløb            | Kreditbeløb           |
|-----------------------------------|-------------------------|-------------------------|
| Forfalden fra Fabrikam East (Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Kreditor (Fabrikam)       |                         | 588,72 EUR / 722,77 USD |
| Realiseret tab (Fabrikam)          | 0,00 EUR / 12,66 USD    |                         |
| Forfalden fra Fabrikam East (Fabrikam) |                         | 0,00 EUR / 12,66 USD    |

**Fabrikam East-bogføring**

| Konto                          | Debetbeløb            | Kreditbeløb           |
|----------------------------------|-------------------------|-------------------------|
| Kreditor (Fabrikam East) | 588,72 EUR / 722,77 USD |                         |
| Forfalden til Fabrikam (Fabrikam East)  |                         | 588,72 EUR / 722,77 USD |
| Forfalden til Fabrikam (Fabrikam East)   | 0,00 EUR / 12,66 USD    |                         |
| Kreditor (Fabrikam East) |                         | 0,00 EUR / 12,66 USD    |
| Kreditor (Fabrikam East) | 11,28 EUR / 13,61 USD   |                         |
| Kontantrabat (Fabrikam East)    |                         | 11,28 EUR / 13,61 USD   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a>Eksempel 5: Kreditorkreditnota med primær betaling
Fabrikam opretter en betaling på 75,00 til kreditoren 3004, Fourth Coffee. Betalingen udlignes med en åben faktura for Fabrikam West-kreditoren 3004 og en åben kreditnota for Fabrikam East-kreditoren 100. Betalingen vælges som primær betaling på siden **Udlign transaktioner**.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Faktura bogføres på Fabrikam West for kreditor 3004

| Konto                          | Debetbeløb | Kreditbeløb |
|----------------------------------|--------------|---------------|
| Udgift (Fabrikam West)          | 100,00       |               |
| Kreditor (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Kreditnota bogføres i Fabrikam East for kreditor 100

| Konto                          | Debetbeløb | Kreditbeløb |
|----------------------------------|--------------|---------------|
| Kreditor (Fabrikam East) | 25,00        |               |
| Indkøbsreturneringer (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Betaling bogføres i Fabrikam for kreditor 3004

| Konto                     | Debetbeløb | Kreditbeløb |
|-----------------------------|--------------|---------------|
| Kreditor (Fabrikam) | 75,00        |               |
| Kontant (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam-betaling udlignes med Fabrikam West-faktura og Fabrikam East-kreditnota

**Fabrikam-bogføring**

| Konto                           | Debetbeløb | Kreditbeløb |
|-----------------------------------|--------------|---------------|
| Kreditor (Fabrikam)       | 25,00        |               |
| Forfalden til Fabrikam East (Fabrikam)   |              | 25,00         |
| Forfalden fra Fabrikam West (Fabrikam) | 100,00       |               |
| Kreditor (Fabrikam)       |              | 100,00        |

**Fabrikam East-bogføring**

| Konto                           | Debetbeløb | Kreditbeløb |
|-----------------------------------|--------------|---------------|
| Forfalden fra Fabrikam (Fabrikam East) | 25,00        |               |
| Kreditor (Fabrikam East)  |              | 25,00         |

**Fabrikam West-bogføring**

| Konto                          | Debetbeløb | Kreditbeløb |
|----------------------------------|--------------|---------------|
| Kreditor (Fabrikam West) | 100,00       |               |
| Forfalden til Fabrikam (Fabrikam West)  |              | 100,00        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a>Eksempel 6: Kreditorkreditnota uden primær betaling
Fabrikam opretter en betaling på 75,00 til kreditoren 3004, Fourth Coffee. Betalingen udlignes med en åben faktura for Fabrikam West-kreditoren 3004 og en åben kreditnota for Fabrikam East-kreditoren 100. Betalingen vælges ikke som primær betaling på siden **Udlign transaktioner**.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Faktura bogføres på Fabrikam West for kreditor 3004

| Konto                          | Debetbeløb | Kreditbeløb |
|----------------------------------|--------------|---------------|
| Udgift (Fabrikam West)          | 100,00       |               |
| Kreditor (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Kreditnota bogføres i Fabrikam East for kreditor 100

| Konto                          | Debetbeløb | Kreditbeløb |
|----------------------------------|--------------|---------------|
| Kreditor (Fabrikam East) | 25,00        |               |
| Indkøbsreturneringer (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Betaling bogføres i Fabrikam for kreditor 3004

| Konto                     | Debetbeløb | Kreditbeløb |
|-----------------------------|--------------|---------------|
| Kreditor (Fabrikam) | 75,00        |               |
| Kontant (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam-betaling udlignes med Fabrikam West-faktura og Fabrikam East-kreditnota

**Fabrikam-bogføring**

| Konto                           | Debetbeløb | Kreditbeløb |
|-----------------------------------|--------------|---------------|
| Forfalden fra Fabrikam West (Fabrikam) | 75,00        |               |
| Kreditor (Fabrikam)       |              | 75,00         |

**Fabrikam East-bogføring**

| Konto                                | Debetbeløb | Kreditbeløb |
|----------------------------------------|--------------|---------------|
| Forfalden fra Fabrikam West (Fabrikam East) | 25,00        |               |
| Kreditor (Fabrikam East)       |              | 25,00         |

**Fabrikam West-bogføring**

| Konto                              | Debetbeløb | Kreditbeløb |
|--------------------------------------|--------------|---------------|
| Kreditor (Fabrikam West)     | 75,00        |               |
| Forfalden til Fabrikam (Fabrikam West)      |              | 75,00         |
| Kreditor (Fabrikam West)     | 25,00        |               |
| Forfalden til Fabrikam East (Fabrikam West) |              | 25,00         |






