---
title: Centraliserede debitorbetalinger
description: Organisationer, der omfatter flere juridiske enheder, kan oprette og administrere betalinger via en enkelt juridisk enhed, der håndterer alle betalinger. Derfor skal den samme transaktion ikke angives i flere juridiske enheder. Denne artikel indeholder eksempler på, hvordan bogføring for centraliserede betalinger håndteres i forskellige scenarier.
author: ShivamPandey-msft
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 07a715c85bd1dadcf7a9848c4387241b1b866fb2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841183"
---
# <a name="centralized-payments-for-accounts-receivable"></a>Centraliserede debitorbetalinger

[!include [banner](../includes/banner.md)]

Organisationer, der omfatter flere juridiske enheder, kan oprette og administrere betalinger via en enkelt juridisk enhed, der håndterer alle betalinger. Derfor skal den samme transaktion ikke angives i flere juridiske enheder. Denne artikel indeholder eksempler på, hvordan bogføring for centraliserede betalinger håndteres i forskellige scenarier.

Organisationer, der omfatter flere juridiske enheder, kan oprette og administrere betalinger via en juridisk enhed, der håndterer alle betalinger. Derfor skal den samme transaktion ikke angives i flere juridiske enheder. Desuden sparer organisationen tid, fordi processer for betalingsforslag, udligninger og redigering af åbne og lukkede transaktioner for centraliserede betalinger er strømlinet. 

I organisationer med centraliserede betalinger er der mange juridiske driftsenheder, og hver juridisk driftsenhed administrerer sine egne oplysninger om fakturaer, der skal betales. Betalinger for alle juridiske driftsenheder modtages af én juridisk enhed, der omtales som betalingens juridiske enhed. Under udligningsprocessen oprettes de gældende skyldig til- og skyldig fra-posteringer. Du kan angive, hvilken juridisk enhed i organisationen der modtager transaktionerne af den realiserede gevinst eller det realiserede tab, og hvordan kasserabattransaktioner, der vedrører en centraliseret betaling, håndteres. På kladdelinjen for centraliserede betalinger skal **Kontotype** indstilles til Debitor. **Modkontotype** skal indstilles til Bank eller Finans. Bankkontoen skal være i det aktuelle firma. 

I følgende eksempler vises, hvordan bogføring håndteres i forskellige scenarier. Følgende konfiguration antages for alle disse eksempler:

-   De juridiske enheder er Fabrikam, Fabrikam East og Fabrikam West. Debitorbetalinger angives i Fabrikam.
-   Feltet **Bogfør kasserabat** på siden **Mellemregning** er angivet til **Juridisk enhed for fakturaen**.
-   Feltet **Bogfør valutakurstab eller -vinding** på siden **Mellemregning** er angivet til **Juridisk enhed for betalingen**.
-   Kunden Northwind Traders er oprettet som kunde i de enkelte juridiske enheder. Kunder fra de forskellige juridiske enheder er identificeret som den samme debitor, fordi de deler det samme globale adresse-adressekartoteks-id.

| Adressekartoteks-id | Kundekonto | Navn              | Juridisk enhed  |
|-----------------|------------------|-------------------|---------------|
| 4050            | 4000             | Northwind Traders | Fabrikam      |
| 4050            | 4000             | Northwind Traders | Fabrikam East |
| 4050            | 10000            | Northwind Traders | Fabrikam West |

## <a name="example-1-customer-payment-of-invoice-from-another-legal-entity"></a>Eksempel 1: Debitorbetaling af faktura fra en anden juridisk enhed
Fabrikam modtager en betaling på 600,00 til Fabrikam-debitorkonto 4000, Northwind Traders. Betalingen udlignes med en åben faktura for debitorkonto 4000 i Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-customer-4000"></a>Faktura bogføres i Fabrikam East for debitor 4000

| Konto                             | Debetbeløb | Kreditbeløb |
|-------------------------------------|--------------|---------------|
| Debitor (Fabrikam East) | 600,00       |               |
| Salg (Fabrikam East)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Betaling modtages og bogføres i Fabrikam for debitor 4000

| Konto                        | Debetbeløb | Kreditbeløb |
|--------------------------------|--------------|---------------|
| Kontant (Fabrikam)                | 600,00       |               |
| Debitor (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikams betaling udlignes med fakturaen fra Fabrikam East

**Fabrikam-bogføring**

| Konto                         | Debetbeløb | Kreditbeløb |
|---------------------------------|--------------|---------------|
| Debitor (Fabrikam)  | 600,00       |               |
| Forfalden til Fabrikam East (Fabrikam) |              | 600,00        |

**Fabrikam East-bogføring**

| Konto                             | Debetbeløb | Kreditbeløb |
|-------------------------------------|--------------|---------------|
| Forfalden fra Fabrikam (Fabrikam East)   | 600,00       |               |
| Debitor (Fabrikam East) |              | 600,00        |

## <a name="example-2-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Eksempel 2: Debitorbetaling af faktura fra en anden juridisk enhed med kasserabat
Fabrikam modtager en betaling på 580,00 til Fabrikam-debitor 4000, Northwind Traders. Fabrikam East har en åben faktura for kreditor 4000. Der er en kontantrabat på 20,00 for fakturaen. Betalingen udlignes med de åbne fakturaer fra Fabrikam East. Kasserabatten bogføres på fakturaens juridiske enhed, Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Faktura bogføres i Fabrikam East for Fabrikam East-debitor 4000

| Konto                             | Debetbeløb | Kreditbeløb |
|-------------------------------------|--------------|---------------|
| Debitor (Fabrikam East) | 580.00       |               |
| Salg (Fabrikam East)               |              | 580.00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Betaling modtages og bogføres i Fabrikam for Fabrikam-debitor 4000

| Konto                        | Debetbeløb | Kreditbeløb |
|--------------------------------|--------------|---------------|
| Kontant (Fabrikam)                | 600,00       |               |
| Debitor (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikams betaling udlignes med fakturaen fra Fabrikam East

**Fabrikam-bogføring**

| Konto                         | Debetbeløb | Kreditbeløb |
|---------------------------------|--------------|---------------|
| Debitor (Fabrikam)  | 580,00       |               |
| Forfalden til Fabrikam East (Fabrikam) |              | 580,00        |

**Fabrikam East-bogføring**

| Konto                             | Debetbeløb | Kreditbeløb |
|-------------------------------------|--------------|---------------|
| Forfalden fra Fabrikam (Fabrikam East)   | 580,00       |               |
| Debitor (Fabrikam East) |              | 580,00        |
| Kontantrabat (Fabrikam East)       | 20,00        |               |
| Debitor (Fabrikam East) |              | 20,00         |

## <a name="example-3-customer-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-gain"></a>Eksempel 3: Debitorbetaling af faktura fra en anden juridisk enhed med realiseret kursgevinst
Fabrikam modtager en betaling på 600,00 euro til Fabrikam-debitor 4000, Northwind Traders. Betalingen udlignes med en åben faktura for debitorkonto 4000 i Fabrikam East. Der oprettes en kursgevinstpostering under udligningsprocessen.

-   Valutakurs for EUR til USD på fakturadatoen: 1,2062
-   Valutakurs for EUR til USD på betalingsdatoen: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Faktura bogføres i Fabrikam East for Fabrikam East-debitor 4000

| Konto                             | Debetbeløb            | Kreditbeløb           |
|-------------------------------------|-------------------------|-------------------------|
| Debitor (Fabrikam East) | 600,00 EUR / 723,72 USD |                         |
| Salg (Fabrikam East)               |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Betaling modtages og bogføres i Fabrikam for Fabrikam-debitor 4000

| Konto                        | Debetbeløb            | Kreditbeløb           |
|--------------------------------|-------------------------|-------------------------|
| Kontant (Fabrikam)                | 600,00 EUR / 736,62 USD |                         |
| Debitor (Fabrikam) |                         | 600,00 EUR / 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikams betaling udlignes med fakturaen fra Fabrikam East

**Fabrikam-bogføring**

| Konto                         | Debetbeløb            | Kreditbeløb           |
|---------------------------------|-------------------------|-------------------------|
| Debitor (Fabrikam)  | 600,00 EUR / 736,62 USD |                         |
| Forfalden til Fabrikam East (Fabrikam) |                         | 600,00 EUR / 736,62 USD |
| Forfalden til Fabrikam East (Fabrikam) | 0,00 EUR / 12,90 USD    |                         |
| Realiseret gevinst (Fabrikam)        |                         | 0,00 EUR / 12,90 USD    |

**Fabrikam East-bogføring**

| Konto                             | Debetbeløb            | Kreditbeløb           |
|-------------------------------------|-------------------------|-------------------------|
| Forfalden fra Fabrikam (Fabrikam East)   | 600,00 EUR / 736,62 USD |                         |
| Debitor (Fabrikam East) |                         | 600,00 EUR / 736,62 USD |
| Debitor (Fabrikam East) | 0,00 EUR / 12,90 USD    |                         |
| Forfalden fra Fabrikam (Fabrikam East)   |                         | 0,00 EUR / 12,90 USD    |

## <a name="example-4-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-gain"></a>Eksempel 4: Debitorbetaling af faktura fra en anden juridisk enhed med kasserabat og realiseret kursgevinst
Fabrikam bogfører en betaling for Fabrikam-debitor 4000, Northwind Traders, for en åben faktura i Fabrikam East. Der gælder en kontantrabat for fakturaen, og der oprettes en momspostering. Betalingen udlignes med den åbne faktura fra Fabrikam East. Der oprettes en kursgevinstpostering under udligningsprocessen. Kasserabatten bogføres på fakturaens juridiske enhed (Fabrikam East), og kursgevinsten bogføres på betalingens juridiske enhed (Fabrikam).

-   Valutakurs for EUR til USD på fakturadatoen: 1,2062
-   Valutakurs for EUR til USD på betalingsdatoen: 1,2277

### <a name="free-text-invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-customer-4000"></a>Fritekstfakturaen bogføres, og der oprettes en momspostering i Fabrikam East for debitor 4000

| Konto                             | Debetbeløb            | Kreditbeløb           |
|-------------------------------------|-------------------------|-------------------------|
| Debitor (Fabrikam East) | 638,22 EUR / 769,82 USD |                         |
| Salg (Fabrikam East)               |                         | 600,00 EUR / 723,72 USD |
| Moms (Fabrikam East)           |                         | 38,22 EUR / 46,10 USD   |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Betaling modtages og bogføres i Fabrikam for debitor 4000

| Konto                        | Debetbeløb            | Kreditbeløb           |
|--------------------------------|-------------------------|-------------------------|
| Kontant (Fabrikam)                | 626,22 EUR / 768,81 USD |                         |
| Debitor (Fabrikam) |                         | 626,22 EUR / 768,81 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikams betaling udlignes med fakturaen fra Fabrikam East

**Fabrikam-bogføring**

| Konto                         | Debetbeløb            | Kreditbeløb           |
|---------------------------------|-------------------------|-------------------------|
| Debitor (Fabrikam)  | 626,22 EUR / 768,81 USD |                         |
| Forfalden til Fabrikam East (Fabrikam) |                         | 626,22 EUR / 768,81 USD |
| Forfalden til Fabrikam East (Fabrikam) | 0,00 EUR / 13,46 USD    |                         |
| Realiseret gevinst (Fabrikam)        |                         | 0,00 EUR / 13,46 USD    |

**Fabrikam East-bogføring**

| Konto                             | Debetbeløb            | Kreditbeløb           |
|-------------------------------------|-------------------------|-------------------------|
| Forfalden fra Fabrikam (Fabrikam East)   | 626,22 EUR / 768,81 USD |                         |
| Debitor (Fabrikam East) |                         | 626,22 EUR / 768,81 USD |
| Debitor (Fabrikam East)  | 0,00 EUR / 13,46 USD    |                         |
| Forfalden fra Fabrikam (Fabrikam East)   |                         | 0,00 EUR / 13,46 USD    |
| Kontantrabat (Fabrikam East)       | 12,00 EUR / 14,47 USD   |                         |
| Debitor (Fabrikam East) |                         | 12,00 EUR / 14,47 USD   |

## <a name="example-5-customer-credit-note-with-primary-payment"></a>Eksempel 5: Debitorkreditnota med primær betaling
Fabrikam modtager en betaling på 75,00 fra debitor 4000, Northwind Traders. Betalingen udlignes med en åben faktura for Fabrikam West-debitoren 10000 og en åben kreditnota for Fabrikam East-debitoren 4000. Betalingen vælges som primær betaling på siden **Udlign transaktioner**.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Faktura bogføres i Fabrikam West for debitor 10000

| Konto                             | Debetbeløb | Kreditbeløb |
|-------------------------------------|--------------|---------------|
| Debitor (Fabrikam West) | 100,00       |               |
| Salg (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Kreditnota bogføres i Fabrikam East for debitor 4000

| Konto                             | Debetbeløb | Kreditbeløb |
|-------------------------------------|--------------|---------------|
| Returvarer (Fabrikam East)       | 25,00        |               |
| Debitor (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Betaling bogføres i Fabrikam for debitor 4000

| Konto                        | Debetbeløb | Kreditbeløb |
|--------------------------------|--------------|---------------|
| Kontant (Fabrikam)                | 75,00        |               |
| Debitor (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam-betaling udlignes med Fabrikam West-faktura og Fabrikam East-kreditnota

**Fabrikam-bogføring**

| Konto                           | Debetbeløb | Kreditbeløb |
|-----------------------------------|--------------|---------------|
| Forfalden fra Fabrikam East (Fabrikam) | 25,00        |               |
| Debitor (Fabrikam)    |              | 25,00         |
| Debitor (Fabrikam)    | 100,00       |               |
| Forfalden til Fabrikam West (Fabrikam)   |              | 100,00        |

**Fabrikam East-bogføring**

| Konto                             | Debetbeløb | Kreditbeløb |
|-------------------------------------|--------------|---------------|
| Debitor (Fabrikam East) | 25,00        |               |
| Forfalden til Fabrikam (Fabrikam East)     |              | 25,00         |

**Fabrikam West-bogføring**

| Konto                             | Debetbeløb | Kreditbeløb |
|-------------------------------------|--------------|---------------|
| Forfalden fra Fabrikam (Fabrikam West)   | 100,00       |               |
| Debitor (Fabrikam West) |              | 100,00        |

## <a name="example-6-customer-credit-note-without-primary-payment"></a>Eksempel 6: Debitorkreditnota uden primær betaling
Fabrikam modtager en betaling på 75,00 fra debitor 4000, Northwind Traders. Betalingen udlignes med en åben faktura for Fabrikam West-debitoren 10000 og en åben kreditnota for Fabrikam East-debitoren 4000. Betalingen vælges ikke som primær betaling på siden **Udlign transaktioner**.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Faktura bogføres i Fabrikam West for debitor 10000

| Konto                             | Debetbeløb | Kreditbeløb |
|-------------------------------------|--------------|---------------|
| Debitor (Fabrikam West) | 100,00       |               |
| Salg (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Kreditnota bogføres i Fabrikam East for debitor 4000

| Konto                             | Debetbeløb | Kreditbeløb |
|-------------------------------------|--------------|---------------|
| Returvarer (Fabrikam East)       | 25,00        |               |
| Debitor (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Betaling bogføres i Fabrikam for debitor 4000

| Konto                        | Debetbeløb | Kreditbeløb |
|--------------------------------|--------------|---------------|
| Kontant (Fabrikam)                | 75,00        |               |
| Debitor (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam-betaling udlignes med Fabrikam West-faktura og Fabrikam East-kreditnota

**Fabrikam-bogføring**

| Konto                         | Debetbeløb | Kreditbeløb |
|---------------------------------|--------------|---------------|
| Debitor (Fabrikam)  | 75,00        |               |
| Forfalden til Fabrikam West (Fabrikam) |              | 75,00         |

**Fabrikam East-bogføring**

| Konto                              | Debetbeløb | Kreditbeløb |
|--------------------------------------|--------------|---------------|
| Debitor (Fabrikam East)  | 25,00        |               |
| Forfalden til Fabrikam West (Fabrikam East) |              | 25,00         |

**Fabrikam West-bogføring**

| Konto                                | Debetbeløb | Kreditbeløb |
|----------------------------------------|--------------|---------------|
| Forfalden fra Fabrikam (Fabrikam West)      | 75,00        |               |
| Debitor (Fabrikam West)    |              | 75,00         |
| Forfalden fra Fabrikam East (Fabrikam West) | 25,00        |               |
| Debitor (Fabrikam West)    |              | 25,00         |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]