---
title: Debitorbogføring
description: Denne artikel indeholder en forklaring på, hvordan bogføringer konfigureres i Debitor, og viser eksempler på bogføringskonfigurationer.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustPaymMode, CustCashDiscount, CommissionPosting, MarkupTable\_Cust, CustPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 492bbd31cae08a93cd68e5ce120d02a62141241b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874568"
---
# <a name="accounts-receivable-posting"></a>Debitorbogføring

[!include [banner](../includes/banner.md)]

Den primære posteringsprofil for modulet **Debitor** er debitorposteringsprofilen. Denne posteringsprofil bestemmer, hvilken samlekonto der bruges, når debitorsaldi bogføres i finansmodulet. En samlekonto er en hovedkonto. Den kaldes også handelskontoen for Debitor.

Du kan finde flere oplysninger i [Debitorposteringsprofiler](../accounts-receivable/customer-posting-profiles.md).

Der findes flere bogføringskonfigurationer end debitorens posteringsprofil i Debitor. Nedenstående afsnit indeholder flere oplysninger om disse øvrige bogføringskonfigurationer.

## <a name="posting-accounts-for-methods-of-payment"></a>Bogføringskonti til betalingsmåder

Betalingsmåder definerer, hvordan en betaling bogføres i finansmodulet. De styrer også funktionaliteten af betalingsoutputtet. Der oprettes typisk én betalingsmåde for hver af de betalingsmåder, din organisation godtager (f.eks. kontant, check, kreditkort, pengeoverførsel og bankoverførsel).

Felterne i sektionen **Bogføring** i oversigtspanelet **Generelt** styrer, hvordan en betaling bogføres i finansmodulet. Du skal først vælge en værdi i feltet **Kontotype**. Den kontotype, du vælger, styrer funktionaliteten i feltet **Betalingskonto**. Det anbefales, at du vælger **Bank** i feltet **Kontotype** og derefter vælger bankkontoen i feltet **Betalingskonto**. Fordelen ved metoden er, at systemet bogfører betalingen til bankreskontroen, som understøtter afstemning og andre kontantrelaterede processer. I tabellen nedenfor vises et eksempel på konfigurationen af posteringsprofilen, hvis du bruger modulet **Kontant- og bankstyring**.

| Bogføringstype | Kontotype | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | Beskrivelse |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Bank | Bank | Bank of Contoso | Bankkonto, der er knyttet til et aktiv | Kredit | Nej | For hver betalingsmåde skal du angive hovedkontoen i feltet **Betalingskonto**. |

Hvis du ikke har planer om at bruge Kontant- og bankstyring, skal du vælge **Finans** i feltet **Kontotype** og derefter vælge hovedkontoen i feltet **Betalingskonto**. I tabellen nedenfor vises et eksempel på konfigurationen af posteringsprofilen, hvis du ikke bruger modulet Kontant- og bankstyring.

| Bogføringstype | Kontotype | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | Beskrivelse |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Ledger | Ledger | 100100: Bank of Contoso | Aktiv | Kredit | Nej | For hver betalingsmåde skal du angive hovedkontoen i feltet **Betalingskonto**. |

## <a name="bridging-accounts"></a>Mellemkonti

Mellemkontering er en totrinsproces, der bruges, når betalinger bogføres. Det er en valgfri funktion, der f.eks. kan bruges sammen med nulsaldobankkonti. Den kan hjælpe med at sikre en mere effektiv og rettidig bankafstemningsproces. I første trin bogføres en betaling på en midlertidig konto (mellemkontoen). I det andet trin tilbageføres og bogføres den bogførte post på bankkontoen, når betalingen er clearet i banken. I følgende tabel vises et eksempel på konfiguration af posteringsprofil til mellemkontering.

| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Finanskladde | 130725 | Ikke-clearet kontant | Passiv | Debet | Ja | For hver betalingsmåde skal du angive hovedkontoen i feltet **Mellemkonto**. |

Yderligere oplysninger finder du i [Konfigurere og behandle mellembetalinger](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="posting-accounts-for-customer-cash-discounts"></a>Bogføringskonti for debitorkasserabatter

Hvis din organisation tilbyder kunder kasserabatter til gengæld for hurtig betaling, skal du konfigurere kasserabatkoder og angive, hvordan rabatterne skal bogføres i finansmodulet. Der findes flere indstillinger til angivelse af den hovedkonto, der bruges til at bogføre en debitorkasserabat.

Du kan finde flere oplysninger under [Kasserabatter](../cash-bank-management/cash-discounts.md).

## <a name="posting-accounts-for-payment-fees"></a>Bogføringskonti til betalingsgebyr

Betalingsgebyrer giver dig mulighed for automatisk at føje et gebyr til en debitorbetaling, når der gælder et sæt betingelser. Betalingsgebyrer kan opkræves af debitoren, eller de kan bogføres på din bankkonto som en udgift. Her er nogle eksempler:

- Du opkræver kunderne 3 procent af betalingstotalen, hvis de betaler med kreditkort.
- Din bank pålægger dig $1,00 for hver bankoverførsel, du behandler, og overførselsgebyret udgiftsføres.

Når du konfigurerer et debitorbetalingsgebyr, og du angiver feltet **Gebyr** til **Debitor**, bliver feltet **Hovedkonto** utilgængeligt, og systemet bruger debitorens posteringsprofil til at bogføre gebyret. Hvis du angiver feltet **Gebyr** til **Finans**, skal du angive feltet **Hovedkonto** til den hovedkonto, hvor betalingsgebyret skal bogføres. Denne hovedkonto er som regel en udgiftskonto. I følgende tabel vises et eksempel på konfiguration af posteringsprofil til bogføring af betalingsgebyr.

| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Finanskladde | 618190 | Bankgebyr som udgift | Udgift | Debet | Nej |  Hvis **Finans** er valgt i feltet **Gebyr**, skal du vælge denne konto i feltet **Hovedkonto** for betalingsgebyret. |

Du kan finde flere oplysninger under [Fastlægge gebyrer for debitorbetaling](../accounts-receivable/tasks/establish-customer-payment-fees.md).

## <a name="posting-accounts-for-charges-codes"></a>Bogføringskonti til gebyrkoder

Hvis du skal registrere salgsbeløb foruden linjeelementer, kan du bruge gebyrkoder. Du kan f.eks. opkræve fragt- og ekspeditionsgebyr af dine kunder, eller fragt- og ekspeditionsgebyr kan udgiftsføres internt. Du kan angive, om beløbene skal bogføres til udgiftskonti eller lægges til vareomkostningerne.

Du kan oprette gebyrkoder for Debitor og Kreditor. Når du konfigurerer en gebyrkode, skal du definere bogføringen. Bogføringen styrer både debetkontoen og kreditkontoen. Når du opretter gebyrkoder, kan du vælge den bogføringstype, der bruges. I følgende tabel vises eksempler på typiske gebyrkoder for Debitor.

| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Betalingsgebyr | 411400 | Omsætning – Gebyrer | Indtægter | Kredit | Nej | **Eksempel på utilstrækkelige midler:** Debiter Debitor/kreditor og krediter finanskonto |
| Ordre fragt | 403500 | Omsætning – Fragt | Indtægter | Kredit | Nej | **Eksempel på fragt, der opkræves af en kunde:** Debiter debitor/kreditor og krediter finanskonto |
| Rabat\* | 403200 | Rabat | Indtægter | Debet | Nej | **Eksempel på kunderabat:** Debiter finanskonto, og krediter debitor/kreditor |

\* I eksemplet med rabatten bruges bogføringen kun, når der føjes en gebyrkode til et indkøbsordrehoved eller en indkøbsordrelinje. Den avancerede rabatfunktionalitet, der er tilgængelig i Microsoft Dynamics 365 Supply Chain Management, giver mere styring og automatisering af rabatter. Du kan finde flere oplysninger i [Kunderabatter](../../supply-chain/sales-marketing/tasks/process-customer-rebates.md).

I den foregående tabel vises tre typiske eksempler på bogføringstyper, der kan bruges til gebyrkoder. Den skal bruges som retningslinje og er et eksempel. Den indeholder ikke en omfattende liste over alle de mulige kombinationer eller bogføringstyper, der kan bruges.

Du kan finde flere oplysninger under [Oprette gebyrkoder](../accounts-receivable/create-charges-codes.md).

## <a name="posting-accounts-for-commissions"></a>Bogføringskonti for provisioner

Du kan konfigurere systemet til at beregne provision for en sælger eller en gruppe af sælgere på en bestemt salgsordre. Hvis du aktiverer denne funktion, skal du konfigurere den bogføringskonto, der bruges til beregning af provisionen. Denne konfiguration udføres på siden **Provisionskontering** i modulet **Salg og marketing**.

Du kan finde flere oplysninger i [Konfigurere salgsprovisionsregler](../../supply-chain/sales-marketing/tasks/set-up-sales-commission-rules.md).
