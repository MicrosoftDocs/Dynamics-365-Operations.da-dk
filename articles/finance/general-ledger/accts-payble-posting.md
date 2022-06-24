---
title: Kreditorbogføringer
description: Denne artikel indeholder en forklaring på, hvordan bogføringer konfigureres i Kreditor, og viser eksempler på bogføringskonfigurationer.
author: rachel-profitt
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting, VendPaymMode, VendCashDiscount, MarkupTable\_Vend, VendPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b3593e01ed4d0a88b5816803f1d67fa7ed5e0f6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908003"
---
# <a name="accounts-payable-posting"></a>Kreditorbogføring

[!include [banner](../includes/banner.md)]

Den primære posteringsprofil for modulet **Kreditor** er kreditorposteringsprofilen. Denne posteringsprofil bestemmer, hvilken samlekonto der bruges, når kreditorsaldi bogføres i finansmodulet. En samlekonto er en hovedkonto. Den kaldes også handelskontoen for Kreditor.

Du kan finde flere oplysninger i [Kreditorposteringsprofiler](../accounts-payable/vendor-posting-profiles.md).

Der findes flere bogføringskonfigurationer end kreditorens posteringsprofil i Kreditor. Nedenstående afsnit indeholder flere oplysninger om disse øvrige bogføringskonfigurationer.

## <a name="methods-of-payment-posting-accounts"></a>Bogføringskonti til betalingsmåder

Betalingsmåder definerer, hvordan en betaling bogføres i finansmodulet. De styrer også funktionaliteten af betalingsoutputtet. Der oprettes typisk én betalingsmåde for hver af de betalingsmåder, din organisation foretager (f.eks. kontant, check, kreditkort, pengeoverførsel og tråd).

Felterne i sektionen **Bogføring** i oversigtspanelet **Generelt** på siden **Betalingsmåder** (**Kreditor > Opsætning af betaling > Betalingsmåder**) styrer, hvordan en betaling bogføres i finansmodulet. Du skal først vælge en værdi i feltet **Kontotype**. Den kontotype, du vælger, styrer funktionaliteten i feltet **Betalingskonto**. Det anbefales, at du vælger **Bank** i feltet **Kontotype** og derefter vælger bankkontoen i feltet **Betalingskonto**. Fordelen ved metoden er, at systemet bogfører betalingen til bankreskontroen, som understøtter afstemning og andre kontantrelaterede processer. I tabellen nedenfor vises et eksempel på konfigurationen af posteringsprofilen, hvis du bruger modulet **Kontant- og bankstyring**.

| Bogføringstype | Kontotype | Eksempel på betalingskontonavn | Kontotype | Debet/Kredit? | Clearingkonto | Beskrivelse |
|--------------|--------------|------------------------------|--------------|---------------|------------------|-------------|
| Bank | Bank | Bank of America | Bankkonto, der er knyttet til et aktiv | Debet | Nej | For hver betalingsmåde skal du angive hovedkontoen i feltet **Betalingskonto**. |

Hvis du ikke har planer om at bruge Kontant- og bankstyring, skal du vælge **Finans** i feltet **Kontotype** og derefter vælge hovedkontoen i feltet **Betalingskonto**. I tabellen nedenfor vises et eksempel på konfigurationen af posteringsprofilen, hvis du **ikke** bruger modulet Kontant- og bankstyring.

| Bogføringstype | Kontotype |Eksempel på betalingskonto | Kontotype | Debet/Kredit? | Clearingkonto | Beskrivelse |
|--------------|--------------|------------------------|--------------|---------------|------------------|-------------|
| Ledger | Ledger | 100100: Bank of America | Aktiv | Debet | Nej | For hver betalingsmåde skal du angive hovedkontoen i feltet **Betalingskonto**. |

## <a name="bridging-accounts"></a>Mellemkonti

Mellemkontering er en totrinsproces, der bruges, når betalinger bogføres. Det er en valgfri funktion, der f.eks. kan bruges sammen med nulsaldobankkonti. Den kan hjælpe med at sikre en mere effektiv og rettidig bankafstemningsproces. I første trin bogføres en betaling på en midlertidig konto (mellemkontoen). I det andet trin tilbageføres og bogføres den bogførte post på bankkontoen, når betalingen er clearet i banken. I følgende tabel vises et eksempel på konfiguration af posteringsprofil til mellemkontering.

| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Finanskladde | 130725 | Ikke-clearet kontant | Passiv | Debet | Ja | For hver betalingsmåde skal du angive hovedkontoen i feltet **Mellemkonto**. |

Yderligere oplysninger finder du i [Konfigurere og behandle mellembetalinger](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="customer-cash-discounts-posting-accounts"></a>Bogføringskonti for debitorkasserabatter

Hvis din organisation modtager kasserabatter fra kreditorer til gengæld for hurtig betaling, skal du konfigurere kasserabatkoder og angive, hvordan rabatterne skal bogføres i finansmodulet. Der findes flere indstillinger til angivelse af den hovedkonto, der bruges til at bogføre en debitorkasserabat.

Du kan finde flere oplysninger under [Kasserabatter](../cash-bank-management/cash-discounts.md).

## <a name="payment-fee-posting-accounts"></a>Bogføringskonti til betalingsgebyr

Betalingsgebyrer giver dig mulighed for automatisk at føje et gebyr til en kreditorbetaling, når der gælder et sæt betingelser. Betalingsgebyrer kan betales til kreditoren, eller de kan bogføres på din bankkonto som en udgift. Her er nogle eksempler:

- En leverandør opkræver 3 procent af betalingstotalen, hvis du betaler med kreditkort.
- Din bank pålægger dig $1,00 for hver bankoverførsel, du behandler, og overførselsgebyret udgiftsføres.

Når du konfigurerer et kreditorbetalingsgebyr, og du angiver feltet **Gebyr** til **Kreditor**, bliver feltet **Hovedkonto** utilgængeligt, og systemet bruger kreditorens posteringsprofil til at bogføre gebyret. Hvis du angiver feltet **Gebyr** til **Finans**, skal du angive feltet **Hovedkonto** til den hovedkonto, hvor betalingsgebyret skal bogføres. Denne hovedkonto er som regel en udgiftskonto. I følgende tabel vises et eksempel på konfiguration af posteringsprofil til bogføring af betalingsgebyr.

| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|----------------|------------------|-------------|
| Finanskladde | 618190 | Bankgebyr som udgift | Udgift | Debet | Nej | Hvis **Finans** er valgt i feltet **Gebyr**, skal du vælge denne konto i feltet **Hovedkonto** på siden **Betalingsgebyr**. |

Du kan finde flere oplysninger under [Definere kreditorbetalingsgebyrer](../accounts-payable/tasks/define-vendor-payment-fees.md).

## <a name="charges-code-posting-accounts"></a>Bogføringskonti til gebyrkode

Hvis du skal registrere salgsbeløb foruden linjeelementer, kan du bruge gebyrkoder. Din leverandør kan f.eks. opkræve fragt- og ekspeditionsgebyr af dig, eller fragt- og ekspeditionsgebyr kan udgiftsføres internt. Du kan angive, om beløbene skal bogføres til udgiftskonti eller lægges til vareomkostningerne.

Du kan oprette gebyrkoder for Debitor og Kreditor. Når du konfigurerer en gebyrkode, skal du definere bogføringen. Bogføringen styrer både debetkontoen og kreditkontoen. Når du opretter gebyrkoder, kan du vælge den bogføringstype, der bruges for de enkelte gebyrkoder. I følgende tabel vises eksempler på typiske gebyrkoder for Kreditor på siden **Gebyrkoder**.

| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Indkøbsgebyr | Lad feltet stå tomt. | Ikke tilgængelig | Vare | Debet | Nej | **Eksempel på et indkøbsgebyr for en vare:** </p><ul><li>**Debettype**-felt = **Vare**</li><li>  **Kredittype**-felt = **Debitor/Kreditor**.</li><li> Ved varebogføringen anvendes hovedkontoen fra lagerposteringsprofilen. |
| Ordre fragt | 600120 | Fragt ind | Indtægter | Debet | Nej | **F.eks. fragt, der betales til en kreditor:** </p><ul><li>**Debettype**-felt = **Finanskonto**</li><li> **Kredittype**-felt = **Debitor/Kreditor** |
| Rabat\* | 503160 | Kreditorrabat (kontra vareforbrug)| Udgift | Kredit | Nej | **Eksempel på en kreditorrabat:**</p><ul><li>**Debettype**-felt = **Debitor/Kreditor**</li><li>**Kredittype**-felt = **Finanskonto** |

\* I eksemplet med rabatten bruges bogføringen kun, når der føjes en gebyrkode til et indkøbsordrehoved eller en indkøbsordrelinje. Den avancerede rabatfunktionalitet, der er tilgængelig i Microsoft Dynamics 365 Supply Chain Management, giver mere styring og automatisering af rabatter. Deer er flere oplysninger i [Kreditorrabatter](../../supply-chain//procurement/vendor-rebates.md).

I den foregående tabel vises tre typiske eksempler på bogføringstyper, der kan bruges til gebyrkoder. Den skal bruges som retningslinje og er et udvalg af eksempler. Den indeholder ikke en omfattende liste over alle de mulige kombinationer eller bogføringstyper, der kan bruges.

Du kan finde flere oplysninger under [Oprette gebyrkoder](../accounts-receivable/create-charges-codes.md).
