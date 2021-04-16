---
title: Oversigt over direkte debitering (SEPA)
description: Det Fælles eurobetalingsområde (SEPA) er nedsat af Europa-Kommissionen og bestemmer, at alle elektroniske betalinger behandles som indenlandske, uanset det land/område, hvor personen, virksomheden eller organisationen og banken er placeret. Der er ingen forskel imellem nationale betalinger og betalinger, der involverer udlandet. SEPA omfatter de 28 EU-medlemsstater, foruden Island, Liechtenstein, Norge, Schweiz, Monaco og San Marino. SEPA er med til at danne et enkelt marked for betalingstransaktioner inden for Det Europæiske Økonomiske Samarbejdsområde (EEA). I sidste ende forventes SEPA at reducere antallet af betalingsformater, som banker, virksomheder og enkeltpersoner skal arbejde med.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 11144
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf3872a47a92509af5857c0c1aec0d4da4095d19
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835262"
---
# <a name="sepa-direct-debit-overview"></a>Oversigt over direkte debitering (SEPA)

[!include [banner](../includes/banner.md)]

Det Fælles eurobetalingsområde (SEPA) er nedsat af Europa-Kommissionen og bestemmer, at alle elektroniske betalinger behandles som indenlandske, uanset det land/område, hvor personen, virksomheden eller organisationen og banken er placeret. Der er ingen forskel imellem nationale betalinger og betalinger, der involverer udlandet. SEPA omfatter de 28 EU-medlemsstater, foruden Island, Liechtenstein, Norge, Schweiz, Monaco og San Marino. SEPA er med til at danne et enkelt marked for betalingstransaktioner inden for Det Europæiske Økonomiske Samarbejdsområde (EEA). I sidste ende forventes SEPA at reducere antallet af betalingsformater, som banker, virksomheder og enkeltpersoner skal arbejde med.   

<a name="what-is-the-goal-of-sepa-direct-debits"></a>Hvad er målet for direkte SEPA-debiteringer?
---------------------------------------

En direkte SEPA-debitering gør det muligt for en kreditor at indsamle midler fra en debitors bankkonto, forudsat at der er tildelt en signeret bemyndigelse af kunden til kreditor. Kunden signerer en bemyndigelse, som autoriserer kreditoren til at opkræve en betaling og beder kundens bank om at betale opkrævningen. 

Direkte SEPA-debiteringer opretter – for første gang – et betalingsinstrument, der kan bruges til både nationale og europæiske direkte debiteringer over de 32 SEPA-lande/-områder. 

Der er to tilgængelige ordninger: SEPA Core-ordningen til direkte debitering og SEPA Business to Business (B2B)-ordningen til direkte debitering. Begge ordninger bruger det samme filformat.

## <a name="what-is-the-core-direct-debit-scheme"></a>Hvad er Core-ordningen til direkte debitering?
SEPA Core-ordningen til direkte debitering er en basisordning. Den har følgende attributter:
-   Pengeoverførslen er i euro (selv om bankkontiene kan indeholde penge i andre valutaer).
-   Kunden og kreditoren skal hver have en konto hos et kreditinstitut, der er placeret inden for SEPA.
-   Kunden skal give kreditoren en underskrevet bemyndigelse.
-   Bemyndigelser udløber 36 måneder efter den sidste påbegyndte opkrævning.
-   Kreditoren skal gemme bemyndigelser, så længe de er gyldige og mindst i 14 måneder efter den sidste opkrævning.
-   Ordningen kan bruges til enkelte (engangs) eller direkte debiteringsopkrævninger.
-   Kunderne har – uden at skulle retfærdiggøre det – ret til at modtage refusion op til otte uger efter debitering på deres konto.

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a>Hvad er SEPA Business to Business (B2B)-ordningen til direkte debitering?
SEPA B2B-ordningen til direkte debitering gælder for business-to-business-transaktioner og bygger på SEPA Core-ordningen til direkte debitering. De vigtigste forskelle er:
-   SEPA B2B-ordningen til direkte debitering er ikke tilladt, når kunden er en privatperson (forbruger).
-   Kunden har ikke ret til refusion for en transaktion, der er autoriseret.
-   Kundens banker skal sikre, at opkrævningen er autoriseret ved at bekræfte, at den stemmer overens med bemyndigelsesoplysningerne. Kundens banker og kunder skal blive enige om den bekræftelse, der skal udføres for hver direkte debitering.
-   Ordningen giver en kortere tidslinje til at præsentere direkte debiteringer og reducerer returnereringsperioden.

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a>Kan jeg bruge COR1-skemaet til direkte debitering-bemyndigelse?
Ja. Du kan bruge COR1-skemaet til SEPA direkte debiteringsmandater i Østrig, Belgien, Tyskland, Frankrig, Italien, Spanien og Nederlandene. Skemaet indeholder en kortere periode i anmeldelsen for samlingen direkte debitering for kreditor.

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a>Hvad er IBAN-numre (International Bank Account Number) og BIC-koder (Bank Identifier Code)?
IBAN-numre og BIC-koder bruges til at identificere alle konti i de 32 SEPA-lande/områder. Angiv BIC i feltet SWIFT-kode og IBAN-nummer i feltet IBAN. Begge felter findes i oversigtspanelet Ekstra id under fanen Bankkonto på siden Bankkonti. Dette gælder for både kreditorens bankkonto og kundens bankkonto.

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a>Hvor kan jeg indtaste kreditoridentifikatorer (id'er til direkte debitering)?
Hver kreditor er i SEPA identificeret med en entydig kreditoridentifikator. Denne identifikator giver kunden og kundens bank mulighed for at filtrere hver direkte debitering og derefter behandle eller afvise den direkte debitering efter kundens anvisninger. Kreditorerne skal anmode om denne identifikator via deres bank. Angiv dette id i feltet Direct Debit-id for bankkontoen for den juridiske enhed.

## <a name="what-are-mandates"></a>Hvad er bemyndigelser?
Kunden signerer en bemyndigelse, som autoriserer kreditoren til at opkræve en betaling og beder kundens bank om at betale opkrævningen. Kunden kan udstede bemyndigelsen i papirformat eller elektronisk. Som standard udløber bemyndigelsen 36 måneder efter den sidste initiering af den direkte debitering.

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a>Hvor skal jeg angive filformatet til den direkte SEPA-debitering (ISO 20022)?
SEPA's dataformater er baseret på meddelelsesstandarderne i ISO 20022. Du skal markere afkrydsningsfeltet Generiske elektronisk rapportering og vælge formatet SEPA direkte debet som en formatkonfiguration til eksport, når du konfigurerer betalingsmåden Kreditor. Denne betalingsmåde bruges, når du opretter en betalingsfil i en debitorbetalingskladde.

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a>I hvilke filformater kan jeg oprette betalingsfiler til SEPA direkte debitering?
Du kan oprette elektroniske betalingsfiler for direkte SEPA-debiteringer i følgende formater:
-   Betalingsfiler til SEPA direkte debitering i filformatet XML-PAIN.008.001.02 for Belgien, Tyskland, Spanien, Frankrig, Italien og Nederlandene.
-   Betalingsfiler til SEPA direkte debitering i filformatet XML-PAIN.008.001.02 for Østrig og i XML-filformatet PAIN.008.003.02 for Tyskland.

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a>Hvordan fungerer refusion og returneringer i direkte SEPA-debiteringer?
I henhold til begge SEPA-ordninger til direkte debitering har kunderne visse refusionsrettigheder . Kunden er berettiget til at tilbagekalde autoriserede transaktioner i en periode på otte uger efter forfaldsdato – uden at skulle give en årsag. Perioden er udvidet til 13 måneder efter forfaldsdatoen ved uautoriserede transaktioner. Tilbageførsler af betalinger, der er foretaget, udføres manuelt ved hjælp af knappen Annuller betaling på siden Kundetransaktioner.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]