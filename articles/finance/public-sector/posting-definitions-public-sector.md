---
title: Bogføringsdefinitioner i den offentlige sektor
description: Denne artikel indeholder eksempler på bogføringsdefinitioner i den offentlige sektor, som du kan bruge til at oprette reskontrokladdelinjer for oprindelige transaktioner, der opfylder udvalgte kriterier. Eksemplerne omfatter budgetdisponeringer, samlet kontantudligninger, afskrivninger, efterkravsudligninger, avancerede finansposter, finansårsafslutning og beskyttede midler.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetDetailsInquiry, CustGroup, JournalizingDefinition, JournalizingDefinitionTrans, LedgerFund, LedgerParameters, LedgerTransferOpening, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 27271
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2bb46992503013d7c40c2e3ba034ae73bd5988b1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407669"
---
# <a name="posting-definitions-in-the-public-sector"></a>Bogføringsdefinitioner i den offentlige sektor

[!include [banner](../includes/banner.md)]

Denne artikel indeholder eksempler på bogføringsdefinitioner i den offentlige sektor, som du kan bruge til at oprette reskontrokladdelinjer for oprindelige transaktioner, der opfylder udvalgte kriterier. Eksemplerne omfatter budgetdisponeringer, samlet kontantudligninger, afskrivninger, efterkravsudligninger, avancerede finansposter, finansårsafslutning og beskyttede midler.

I denne artikel beskrives bogføringsdefinitionernes tilgængelige funktioner for den offentlige sektor. Før du læser dette emne, skal du være fortrolig med bogføringsdefinitioner.

## <a name="how-do-i-use-these-examples-of-public-sector-posting-definitions"></a>Hvordan bruger jeg disse eksempler på bogføringsdefinitioner til den offentlige sektor?
Du kan konfigurere eksemplerne i denne artikel på siden **Bogføringsdefinitioner**. Hvert eksempel indeholder følgende områder:

-   Bogføringsdefinition – søgekriterier
-   Bogføringsdefinition – genererede poster
-   Posteringer med konti, dimensionsværdier og beløb
-   Finansposter genereret fra bogføringsdefinitionen

Når der er en match mellem kontiene og dimensionsværdierne i ruden **Søgekriterier** for bogføringsdefinitionen og kontiene og dimensionsværdierne i posteringen, genereres der finansposter. Disse poster er baseret på de **oprettede poster** for bogføringsdefinitionen. 

> [!NOTE]
> Knyt en bogføringsdefinition til en bestemt posteringstype ved brug af siden **Definitioner af posteringsbogføring**. Efter at du har knyttet en bogføringsdefinition til en posteringstype og valgt **Brug bogføringsdefinitioner** på siden **Finansparametre**, skal alle posteringer med den valgte posteringstype bruge bogføringsdefinitioner.

## <a name="example-budget-appropriations"></a>Eksempel: Budgetdisponeringer
For organisationerne inden for den offentlige sektor registreres oprindelige budgetsaldi som enten disponeringer til udgifter eller som forventet omsætning. De oprindelige budgetsaldi bruges til at spore de budgetsaldi, der er til rådighed, og sammenholde dem med udgifter og de faktiske indtægter, der indgår.

Der oprettes en bogføringsdefinition som et led i registreringen af budgetregisterposter til finans, og der oprettes en definition for posteringsbogføring for budgetregisterposter med budgettypen **Oprindeligt budget**.

| Kontostruktur | Sammenlign kontonummer\* | Prioritet |
|-------------------|------------------------|----------|
| Udgift           | - - -                  | 1        |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

### <a name="posting-definition--generated-entries-for-match-criteria--row-1"></a>Bogføringsdefinition – genererede poster for søgekriterier – række 1

| Kontostruktur | Genereret kontonummer                | Genereret debet/kredit |
|-------------------|-----------------------------------------|------------------------|
| Saldo           | -36300 (Budgetkonto til pengebalancer) | Samme                   |
| Saldo           | -36350 (Disponeringskonto)          | Balancere              |

### <a name="posting-definition--match-criteria--row-2"></a>Bogføringsdefinition – søgekriterier – række 2

| Kontostruktur | Sammenlign kontonummer\* | Prioritet |
|-------------------|------------------------|----------|
| Indtægter           | - - -                  | 1        |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

### <a name="posting-definition--generated-entries-for-match-criteria--row-2"></a>Bogføringsdefinition – genererede poster for søgekriterier – række 2

| Kontostruktur | Genereret kontonummer                | Genereret debet/kredit |
|-------------------|-----------------------------------------|------------------------|
| Saldo           | -36300 (Budgetkonto til pengebalancer) | Balancere              |
| Saldo           | -36340 (Forventet omsætningskonto)      | Samme                   |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Posteringer med konti, dimensionsværdier og beløb

Du kan angive konti, dimensionsværdier og beløb til budgetkontoposten på siden **Budgetregisterposter**.

| Konto + dimensioner               | Debet | Kredit | Kommentar |
|------------------------------------|-------|--------|---------|
| 101-606400-OU\_1-OU\_3566-Training |       | 250,00 |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Finansposter genereret fra bogføringsdefinitionen

Genererede finansposter oprettes til registrering af de oprindelige budget i hver dimension.

| Konto + dimensioner | Debet  | Kredit | Kommentar |
|----------------------|--------|--------|---------|
| 101-36300            |        | 250,00 |         |
| 101-36350            | 250,00 |        |         |

I dette eksempel matcher middeldimensionen og kontodelen af udgiftskontostrukturen kriterierne for bogføringsdefinitionen. Derfor oprettes de genererede finansposter, når 101-606400-OU\_1-OU\_3566-Training evalueres.

## <a name="examples-pooled-cash-settlements"></a>Eksempler: Samlede kontantudligninger
Et samlet kontantregnskab består af beløb, der indskydes af individuelle midler på en kombineret finanskonto. Dette forbedrer styring af og opsyn med likvide aktiver og fremmer effektiv administration af overskydende midler. Disse beløb kan administreres ved hjælp af kasserermidler. Derfor skal det passende proportionale beløb af de samlede kontant- og investeringssaldi rapporteres for hver enkelt middel, der deltager i puljen. For at garantere dette skal der føjes relevante forfalden til- og forfalden fra-poster til de udligninger, der overfører beløb fra ét middel til et andet for at udføre udligningen. 

> [!NOTE] 
> Der vises ingen fejlmeddelelse, hvis der ikke er angivet en bogføringsdefinition for udligninger, eller hvis ikke der findes et søgekriterie i bogføringsdefinitionen. Installationer, der ikke bruger samlede kontantudligninger, eller som ikke kræver modposteringer på udligningsbilag, behøver ikke at konfigurere bogføringsdefinitioner for udligninger, når bogføringsdefinitioner er aktiveret for andre posteringer. 

Når det gælder kreditorudligninger, anvendes kreditorbetalinger i et eller flere midler til at registrere de relevante middelegenkapitalstransaktioner i kasserermidler. Når det gælder debitorudligninger, skal debitorkreditten fra betalinger i kasserermidlerne bruges til at udligne tilgodehavender i et eller flere midler. Posteringsposter på kreditorsaldo eller debitorsaldo på de transaktioner, der udlignes, tilbageføres automatisk. Brug af bogføringsdefinitioner til udligning er valgfrit. Bogføringsdefinitionerne anvendes på tidspunktet for udligningen for at generere flere finansposteringer for forfalden til- og forfalden fra-poster for at afstemme udligningsbilaget efter middel. 

Du kan bruge bogføringsdefinitioner til følgende udligningsposteringstyper:

-   Kreditorbetalingskladder, som omfatter kreditorbetalinger mod fakturaer, refusioner og finanskreditbilag og kreditnotaer mod fakturaer
-   Egenveksler, der omfatter betalinger, der bruger udstedelse, genudstedelse, remittering og udligning af egenveksler
-   Debitorbetalingskladder, som omfatter debitorbetalinger, debitorfinanskreditnotaer og kreditnotaer mod fritekstfakturaer, projektfakturaer, rentenotaer og posteringer med rykkere

Du kan konfigurere bogføringsdefinitioner for kreditorbetalingskladder, egenveksler og debitorbetalingskladder på siden **Bogføringsdefinitioner** i feltet **Modul** og ved at vælge **Bank**. Derefter kan du på siden **Definitioner af posteringsbogføring** på fanen **Bank** vælge de relevante transaktionstyper, der skal knyttes til posteringsdefinitionerne.

> [!NOTE] 
> En enkelt bogføringsdefinition, hvis den er defineret bredt, bruges til de fleste scenarier med kreditor- og debitorudligning. Den enkelte bogføringsdefinition skal stadig være tilknyttet betalingskladder for både kreditor og debitor på fanen **Bank**. 

Du kan angive en anden bogføringsdefinition for en bestemt bank og betalingsmåde for kreditor- og debitorbetalingskladder. 

Før bogføringsdefinitioner anvendes på udligninger, skal du udføre følgende opgaver:

-   Knytte hver debitor eller kreditor, der har kassererens midler (999) på oversigtspanelet **Økonomiske dimensioner** på debitorens eller kreditorens side med oplysninger. Kreditor- og debitorbetalinger kan derefter genereres i kassererens midler mod kreditoren eller debitorens samlekonto, der er angivet i kreditor- eller debitorposteringsprofilerne.
-   For at angive standardmidlet i debitor skal du på siden **Debitorgrupper** i handlingsruden klikke på **Opsætning** og derefter klikke på **Økonomiske standarddimensioner**. Kassererens midler bliver derefter til standardmidlet, når nye kunder knyttes til en debitorgruppe.
-   Knyt kassererens middel med hver enkelt bankkonto, der bruges ved udligninger, Den bogførte bankkonto kan derefter blive afstemt efter middel ved hjælp af kreditor- eller debitorbetaling.

Du skal også udføre en af følgende opgaver:

-   **Valgmulighed A:** Angiv en enkelt forfalden til-konto i kassererens midler for alle midler.
-   **Valgmulighed B:** Angiv en anden forfalden til-konto i kassererens midler for hvert enkelt middel.

### <a name="option-a-specify-a-single-due-to-account-for-all-funds"></a>Valgmulighed A: Angiv en enkelt forfalden til-konto for alle midler

Du kan angive en enkelt forfalden til-konto i kassererens midler for alle midler. I dette tilfælde vil et enkelt globalt søgekriterie adressere alle midler (undtagen kassererens midler), og du skal angive følgende søgekriterier og genererede poster i bogføringsdefinitionen.

#### <a name="settlement-posting-definition--match-criteria"></a>Udligningsbogføringsdefinition – søgekriterier

| Kontostruktur | Sammenlign kontonummer\*                 | Prioritet |
|-------------------|----------------------------------------|----------|
| Restværdi           | 999 – Angiv en søgepostering med højere prioritet for kassererens midler, så der ikke genereres modposteringer for dette middel. | 1        |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

#### <a name="settlement-posting-definition--generated-entries-for-match-criteria"></a>Udligningsbogføringsdefinition – genererede poster for søgekriterier

| Kontostruktur | Genereret kontonummer                                                           | Genereret debet/kredit |
|-------------------|------------------------------------------------------------------------------------|------------------------|
|                   | Ingen genererede poster er defineret for søgeposteringen for kassererens midler. |                        |

#### <a name="settlement-posting-definition--match-criteria"></a>Udligningsbogføringsdefinition – søgekriterier

| Kontostruktur | Sammenlign kontonummer\*                                                                      | Prioritet |
|-------------------|---------------------------------------------------------------------------------------------|----------|
| Restværdi           | Brug en global søgepostering med lavere prioritet for at oprette modposteringer for alle andre midler. | 10       |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

#### <a name="settlement-posting-definition--generated-entries-for-match-criteria"></a>Udligningsbogføringsdefinition – genererede poster for søgekriterier

| Kontostruktur | Genereret kontonummer                                           | Genereret debet/kredit |
|-------------------|--------------------------------------------------------------------|------------------------|
| Saldo           | - 10110 (Egenkapitalkonto i søgeposteringen – kassebeholdning)         | Balancere              |
| Saldo           | 999 - 37000 (Konto til egenkapital i Kassererens midler for alle midler) | Samme                   |

### <a name="option-b-specify-a-different-due-to-account-for-each-fund"></a>Valgmulighed B: Angiv en anden forfalden til-konto for hvert enkelt middel

Du kan angive en anden forfalden til-konto i kassererens midler for hvert enkelt middel. For hvert middel, som et skyldigt beløb til kreditor eller et debitortilgodehavende genereres i (undtagen kassererens midler), skal du angive følgende søgekriterier og genererede posteringer i bogføringsdefinitionen.

#### <a name="settlement-posting-definition--match-criteria"></a>Udligningsbogføringsdefinition – søgekriterier

| Kontostruktur | Sammenlign kontonummer\*                                                                                                                | Prioritet |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|----------|
| Restværdi           | 101 – Hvis der bruges en middelværdi og en tom hovedkonto, gælder søgekriteriet for både tilgodehavender fra kunder og skyldige beløb til kreditorer. | 1        |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

#### <a name="settlement-posting-definition--generated-entries-for-match-criteria"></a>Udligningsbogføringsdefinition – genererede poster for søgekriterier

| Kontostruktur | Genereret kontonummer                                          | Genereret debet/kredit |
|-------------------|-------------------------------------------------------------------|------------------------|
| Saldo           | 101 - 10110 (Konto for egenkapital i midlet 101 – kassebeholdning)           | Balancere              |
| Saldo           | 999 - 37101 (Konto til egenkapital i kassererens midler for midlet 101) | Samme                   |

Du skal tilføje yderligere rækker for **Søgekritierier** for hvert enkelt middel, der har genererede poster, for at afspejle den relevante middelafstemningspost og midlets egenkapitalkonto i kassererens midler. 

Fra kreditor- eller debitorbetalingskladden skal du angive kreditor- eller debitorkonti eller vælge et betalingsforslag og derefter vælge de fakturaer, der skal betales. Når kladden bogføres, sammenlignes kreditor- eller debitorafstemningsposteringer både på fakturaen og betalingen i forhold til udligningens bogføringsdefinition. Hvis søgekriterier findes, føjes de genererede forfalden til- og forfalden fra-poster til udligningsbilaget. 

Følgende bilag er repræsentative for et typisk scenarie for faktura, betaling og udligning.

## <a name="accounts-payable-example"></a>Eksempel på Kreditor
### <a name="accounts-payable-invoice-voucher"></a>Fakturabilag for Kreditor

| Konto + dimensioner | Debet  | Kredit | Kommentar             |
|----------------------|--------|--------|---------------------|
| 101 - 66100 - 150    | 250,00 |        | Udgiftskonto |
| 101 - 24210          |        | 250,00 | Kreditor    |

### <a name="accounts-payable-payment-voucher"></a>Betalingsbilag for Kreditor

| Konto + dimensioner | Debet  | Kredit | Kommentar           |
|----------------------|--------|--------|-------------------|
| 999 - 24210          | 250,00 |        | Oversigt over kreditorer    |
| 999 - 11020          |        | 250,00 | Bank-/kontantkonto |

### <a name="accounts-payable-settlement-voucher"></a>Udligningsbilag for Kreditor

Udligningsbilag for Kreditor åbnes via de relaterede bilag på kreditorbetalingsbilaget. 

I dette eksempel vil værdierne **Overensstemmelseskontonummer** for bogføringsdefinitionen matche kontiene for kreditorafstemningsposteringstypen. Når 999-24210 og 101 – 24210 evalueres, oprettes de genererede finansposter kun for midlet 101, fordi der ingen tilsvarende poster er angivet til kassererens midler (999).

| Konto + dimensioner | Debet  | Kredit | Kommentar                                                                  |
|----------------------|--------|--------|--------------------------------------------------------------------------|
| 999 - 24210          |        | 250,00 | Oversigt over kreditor (genereres af systemet)                                        |
| 101 - 24210          | 250,00 |        | Faktura til betaling (genereres af systemet)                                       |
| 101 - 11010          |        | 250,00 | Egenkapital for midlet 101 (bogføringsdefinition for udligning)                  |
| 999 - 37101          | 250,00 |        | Kasserermidler – forfalder fra midlet 101 (bogføringsdefinition for udligning) |

### <a name="summarizing-the-entries-across-the-invoice-payment-and-settlement-vouchers"></a>Kort beskrivelse af posterne på tværs af faktura, betaling og udligningsbilag

Følgende tabel viser, hvordan de endelige finanskonti påvirkes.

| Konto + dimensioner | Debet  | Kredit | Kommentar                                                                  |
|----------------------|--------|--------|--------------------------------------------------------------------------|
| 999 - 11020          |        | 250,00 | Bank-/kontantkonto                                                        |
| 101 - 66100 - 150    | 250,00 |        | Udgiftskonto                                                      |
| 101 - 11010          |        | 250,00 | Egenkapital for midlet 101 (bogføringsdefinition for udligning)                  |
| 999 - 37101          | 250,00 |        | Kassererens midler – forfalder fra midlet 101 (bogføringsdefinition for udligning) |

## <a name="accounts-receivable-example"></a>Eksempel på Debitor
### <a name="accounts-receivable-invoice-voucher"></a>Fakturabilag for Debitor

| Konto + dimensioner | Debet  | Kredit | Kommentar             |
|----------------------|--------|--------|---------------------|
| 101 - 44400          |        | 250,00 | Omsætningskonto     |
| 101 - 11530          | 250,00 |        | Debitor |

### <a name="accounts-receivable-payment-voucher"></a>Betalingsbilag for Debitor

| Konto + dimensioner | Debet  | Kredit | Kommentar           |
|----------------------|--------|--------|-------------------|
| 999 - 11530          |        | 250,00 | Oversigt over debitorer  |
| 999 - 11020          | 250,00 |        | Bank-/kontantkonto |

### <a name="accounts-receivable-settlement-voucher"></a>Debitor – udligningsbilag

Udligningsbilag for Debitor åbnes via de relaterede bilag på debitorbetalingsbilaget.

I dette eksempel vil værdierne **Overensstemmelseskontonummer** for bogføringsdefinitionen matche kontiene for debitorafstemningsposteringstypen. Når 999-11530 og 101 – 11530 evalueres, oprettes de genererede finansposter kun for midlet 101, fordi der ingen tilsvarende poster er angivet til kassererens midler (999).

| Konto + dimensioner | Debet  | Kredit | Kommentar                                                                |
|----------------------|--------|--------|------------------------------------------------------------------------|
| 999 - 11530          | 250,00 |        | Oversigt over debitorer (genereres af systemet)                                    |
| 101 - 11530          |        | 250,00 | Debitorfaktura (genereres af systemet)                                  |
| 101 - 11010          | 250,00 |        | Egenkapital for midlet 101 (bogføringsdefinition for udligning)                |
| 999 - 37101          |        | 250,00 | Kasserermidler – forfalder til midlet 101 (bogføringsdefinition for udligning) |

### <a name="summarizing-the-entries-across-the-invoice-payment-and-settlement-vouchers"></a>Kort beskrivelse af posterne på tværs af faktura, betaling og udligningsbilag

Følgende tabel viser, hvordan de endelige finanskonti påvirkes.

| Konto + dimensioner | Debet  | Kredit | Kommentar                                                                |
|----------------------|--------|--------|------------------------------------------------------------------------|
| 999 - 11020          | 250,00 |        | Bank-/kontantkonto                                                      |
| 101 - 44400          |        | 250,00 | Omsætningskonto                                                        |
| 101 - 11010          | 250,00 |        | Egenkapital for midlet 101 (bogføringsdefinition for udligning)                |
| 999 - 37101          |        | 250,00 | Kasserermidler – forfalder til midlet 101 (bogføringsdefinition for udligning) |

Ud over eksemplet tidligere i dette afsnit kan bogføringsdefinitioner til udligninger, der er knyttet til posteringstypen debitorbetalingskladder, også anvendes i følgende situationer:

-   Afskrivninger på debitor
-   Udligninger af fritekstdebitorfakturaer ved kontantbetaling ved levering (kontantbetaling)

Afskrivninger på debitor kan bruge bogføringsdefinitioner, der er defineret til udligning. Derfor kan der oprettes finanskreditkladder, når saldi bogføres af fonden. Både finans- og debitorkontotypeposter på kladdelinjerne evalueres mod bogføringsdefinitionen for udligningen. Begge bruger den bogføringsdefinition, der er tilknyttet posteringstypen på fanen **Tilgodehavender** på siden **Definitioner af posteringsbogføring**. Afhængigt af hvordan afskrivning skal udføres, kan bogføringsdefinitionen til udligning kræve flere søgekriterier. 

Når bogføringsdefinitionen for afskrivning er konfigureret til afskrivning af saldi til godtgørelse for tvivlsomme tilgodehavender i forhold til aktivkontoen, kan bogføringsdefinitionen for udligning også bruges til afskrivninger, forudsat at søgekriteriet allerede er konfigureret til balancekonti, der har en maske for hovedkontoen. (Få yderligere oplysninger ved at se tidligere eksempler, f.eks. afsnittet "Udligningsbogføringsdefinition – søgekriterier"). 

Hvis bogføringsdefinitionen til afskrivning er konfigureret til at tilbageføre den oprindelige omsætningskonto, skal bogføringsdefinitionen for udligning have de relevante søgekriterier for indtægtsregnskabsstrukturer, især forfald til- og forfald fra-poster på de genererede poster. For hvert middel, der ikke er i kassererens midler (999), skal følgende poster findes i bogføringsdefinitionen til udligning.

### <a name="posting-definition--match-criteria"></a>Bogføringsdefinition – søgekriterier

| Kontostruktur | Sammenlign kontonummer\*                                                     | Prioritet |
|-------------------|---------------------------------------------------------------------------|----------|
| Indtægter           | 101 – Hvis du bruger en middelværdi og en tom hovedkonto, er kriterierne gældende for alle finansposter. | 1        |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

### <a name="posting-definition--generated-entries-for-match-criteria"></a>Bogføringsdefinition – genererede poster for søgekriterier

| Kontostruktur | Genereret kontonummer                                                           | Genereret debet/kredit |
|-------------------|------------------------------------------------------------------------------------|------------------------|
| Saldo           | 101 - 10110 (Konto for egenkapital i midlet 101)                                           | Balancere              |
| Samme              | 999 - 37101 (Kasserers midler – egenkapitalkonto til midler 101. En enkelt konto kan anvendes i stedet for individuelle middelegenkapitalkonti). | Samme                   |

## <a name="accounts-receivable-writeoff-example"></a>Eksempel på debitorafskrivning
### <a name="accounts-receivable-invoice-voucher"></a>Fakturabilag for Debitor

| Konto + dimensioner | Debet  | Kredit | Kommentar             |
|----------------------|--------|--------|---------------------|
| 101 - 44400 - -      |        | 250,00 | Omsætningskonto     |
| 101 - 11530          | 250,00 |        | Debitor |

### <a name="accounts-receivable-write-off--general-ledger-credit-voucher"></a>Debitorafskrivning – kreditnota i Finans

I dette eksempel angives bogføringsdefinitionen for afskrivningen for at tilbageføre omsætningskontoen.

| Konto + dimensioner | Debet  | Kredit | Kommentar                                                                |
|----------------------|--------|--------|------------------------------------------------------------------------|
| 999 - 11530          |        | 250,00 | Oversigt over debitorer                                                       |
| 101 - 44400 - -      | 250,00 |        | Bank-/kontantkonto                                                      |
| 101 - 11010          |        | 250,00 | Egenkapital for midlet 101 (bogføringsdefinition for udligning)                |
| 999 - 37101          | 250,00 |        | Kasserermidler – forfalder til midlet 101 (bogføringsdefinition for udligning) |

### <a name="accounts-receivable-write-off--settlement-voucher"></a>Debitorafskrivning – udligningsbilag

I dette eksempel anvendes den kredit, der er oprettet i finansbilaget, på afskrivningsposteringen. Derudover vil værdierne **Overensstemmelseskontonummer** for bogføringsdefinitionen matche kontiene for debitorafstemningsposteringstypen. Derfor er det sådan, at når 999 - 11530 og 101 - 11530 evalueres, oprettes de genererede finansposter kun for midlet 101, fordi der ingen tilsvarende poster er angivet til kassererens midler (999).

| Konto + dimensioner | Debet  | Kredit | Kommentar                                                                |
|----------------------|--------|--------|------------------------------------------------------------------------|
| 999 - 11530          | 250,00 |        | Oversigt over debitorer (genereres af systemet)                                    |
| 101 - 11530          |        | 250,00 | Debitorfaktura (genereres af systemet)                                  |
| 101 - 11010          | 250,00 |        | Egenkapital for midlet 101 (bogføringsdefinition for udligning)                |
| 999 - 37101          |        | 250,00 | Kasserermidler – forfalder til midlet 101 (bogføringsdefinition for udligning) |

### <a name="summarizing-the-entries-across-the-invoice-write-off-credit-and-settlement-vouchers"></a>Kort beskrivelse af posterne på tværs af faktura, afskrivningskredit og udligningsbilag

Der er ingen indflydelse på finanskontiene, når en faktura er afskrevet fuldt ud.

## <a name="accounts-receivable-free-text-invoice-cash-on-delivery-cash-payment-settlement-example"></a>Eksempel på afstemning af debitorfritekstfaktura med kontantbetaling ved levering (kontantbetaling)
Fritekstfakturaer kan bruge betalingsbetingelserne, hvor betalingsmetoden er indstillet til **Efterkrav**, og kontantbetaling er aktiveret. Derfor udligner de sig selv med det samme på tidspunktet for bogføring uden at skulle bruge betalingskladden. Når der opstår denne slags udligning, oprettes der en kreditnota. Denne note bruger den angivne kassebeholdning baseret på betingelserne for betalingsforskydning og de økonomiske dimensioner på kundens samlekonto. I denne form for udligning bliver de relevante konti med tilgodehavender, der er angivet på fakturaen, ikke automatisk tilbageført. Bogføringsdefinitionen for udligning skal derfor omfatte tilbageførsel af bogføringsposter på debitorsaldoen på faktura og kreditnota ud over generering af forfaldsdato-til- og skyldig-fra poster til udligning. 

For at bruge bogføringsdefinitioner til udligning i dette scenarie skal du udføre følgende ekstra opsætningsopgaver:

-   Opret en særskilt betalingsmåde for fritekstfakturaer, der skal udlignes med denne metode.
-   Opret en ny bogføringsdefinition for udligning af fritekstfakturaen med kontantbetaling ved levering.
-   Tilknyt den nye bogføringsdefinitionen (til debitorbetalingskladde mod den specifikke betalingsmåde) under fanen **Bank** på siden **Definitioner af posteringsbogføring**. For at anvende den opsætning af bogføringsdefinition, der er angivet for denne form for udligning, skal du vælge denne entydige betalingsmåde og efterkrav/kontantbetalingsvilkår for betaling på fakturaen.

I posteringsdefinitionen skal du derefter angive følgende søgekriterier og genererede posteringer for kassererens midler (999).

### <a name="posting-definition--match-criteria--row-1"></a>Bogføringsdefinition – søgekriterier – række 1

| Kontostruktur | Sammenlign kontonummer\*                                          | Genereret debet/kredit |
|-------------------|-----------------------------------------------------------------|------------------------|
| Restværdi           | 999 – Dette søgekriterie bruges kun til tilgodehavender i kassererens midler (999). Der kræves kun to genererede poster for dette søgekriterie, fordi forfalden til- og forfalden fra-poster ikke er tilgængelige for kassererens midler. | 1                      |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

### <a name="posting-definition--generated-entries-for-match-criteria--row-1"></a>Bogføringsdefinition – genererede poster for søgekriterier – række 1

| Kontostruktur |                                 Genereret kontonummer                                  | Genereret debet/kredit |
|-------------------|-------------------------------------------------------------------------------------------|------------------------|
|      Saldo      | 999 - 11530 (Debiter debitorsaldoposteringstypeposten på den kreditornota, der udstedes). |       Balancere        |
|       Samme        |                      999 – (Krediter tilgodehavende i 999-midlet).                       |          Samme          |

### <a name="posting-definition--match-criteria--row-2"></a>Bogføringsdefinition – søgekriterier – række 2

| Kontostruktur | Sammenlign kontonummer\*                                                | Prioritet |
|-------------------|-----------------------------------------------------------------------|----------|
| Restværdi           | 101 – Når det gælder søgekriterier, der ikke er i kassererens midler, kræves der fire sæt genererede poster. To poster tilbagefører debitorsaldoposteringstypeposter på kreditnota og faktura, og to yderligere poster genererer de nødvendige forfald til- og forfald fra-poster. | 1        |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

### <a name="posting-definition--generated-entries-for-match-criteria--row-2"></a>Bogføringsdefinition – genererede poster for søgekriterier – række 2

| Kontostruktur | Genereret kontonummer                                          | Genereret debet/kredit |
|-------------------|-------------------------------------------------------------------|------------------------|
| Saldo           | 999 - 11530 (Debiter debitorsaldoposteringstypeposten på den kreditornota, der udstedes).  | Balancere              |
| Samme              | 999 – (Krediter tilgodehavende i 101-midlet).                         | Samme                   |
| Saldo           | 101 - 10110 (Konto for egenkapital i midlet 101)                           | Balancere              |
| Samme              | 999 - 37101 (Kasserers midler – egenkapitalkonto til midler 101. En enkelt konto kan anvendes i stedet for individuelle middelegenkapitalkonti). | Samme                   |

## <a name="accounts-receivable-cashondelivery-cash-payment-settlement-example"></a>Eksempel på debitorafstemning ved kontantbetaling ved levering (kontantbetaling)
### <a name="accounts-receivable-invoice-voucher"></a>Fakturabilag for Debitor

| Konto + dimensioner | Debet  | Kredit | Kommentar                          |
|----------------------|--------|--------|----------------------------------|
| 101 - 44400 - -      |        | 250,00 | Omsætningskonto i 101-midlet      |
| 999 - 44400 - -      |        | 250,00 | Omsætningskonto i 999-midlet      |
| 101 - 11530          | 250,00 |        | Debitor i 101-midlet  |
| 999 - 11535          | 250,00 |        | Debitor i 999-midlet  |
| 999-11530            |        | 500,00 | Oversigt over debitorer                 |
| 999 - 11020          | 500,00 |        | Kontantkonto ved betalingsvilkår |

Dette omfatter flere kreditposter i bilaget.

### <a name="accounts-receivable-settlement-voucher"></a>Debitor – udligningsbilag

I dette eksempel vil værdierne **Overensstemmelseskontonummer** for bogføringsdefinitionen kun matche kontiene for debitorafstemningsposteringstypen på fakturaen.

| Konto + dimensioner | Debet  | Kredit | Kommentar                                                                |
|----------------------|--------|--------|------------------------------------------------------------------------|
| 999 - 11530          | 250,00 |        | Oversigt over debitorer (bogføringsdefinition til udligning)                   |
| 101 - 11530          |        | 250,00 | Debitorfaktura (bogføringsdefinition til udligning)                 |
| 101 - 11010          | 250,00 |        | Egenkapital for midlet 101 (bogføringsdefinition for udligning)                |
| 999 - 37101          |        | 250,00 | Kasserermidler – forfalder til midlet 101 (bogføringsdefinition for udligning) |
| 999 - 11530          | 250,00 |        | Oversigt over debitorer (bogføringsdefinition til udligning)                   |
| 999 - 11535          |        | 250,00 | Oversigt over debitorer (bogføringsdefinition til udligning)                   |

### <a name="summarizing-the-entries-across-the-invoice-payment-and-settlement-vouchers"></a>Kort beskrivelse af posterne på tværs af faktura, betaling og udligningsbilag

Følgende tabel viser, hvordan de endelige finanskonti påvirkes.

| Konto + dimensioner | Debet  | Kredit | Kommentar                                                                |
|----------------------|--------|--------|------------------------------------------------------------------------|
| 999 - 11020          | 500,00 |        | Kontantkonto ved betalingsvilkår                                       |
| 101 - 44400 - -      |        | 250,00 | Omsætning i 101-midlet                                                    |
| 999 - 44400 - -      |        | 250,00 | Omsætning i 999-midlet                                                    |
| 101 - 11010          | 250,00 |        | Egenkapital for midlet 101 (bogføringsdefinition for udligning)                |
| 999 - 37101          |        | 250,00 | Kassererens midler – forfalder til midlet 101 (bogføringsdefinition for udligning) |

## <a name="example-advanced-ledger-entries"></a>Eksempel: avancerede finansposter
Når du opretter avancerede finansposter, skal du vælge en standardbogføringsdefinition. Derefter kan du for hver avanceret finanspostlinje enten bruge standardbogføringsdefinitionen eller vælge en anden. Bogføringsdefinitionerne genererer regnskabsfordelinger og kladdeposteringer for reskontro, der opretter, ændrer eller tilbagefører finansposterne og opdaterer finanskontiene. Du kan indstille hver bogføringsdefinition for appen Finans. Men du behøver ikke at tilknytte bogføringsdefinitionen med en transaktionstype, som du gør for andre bogføringsdefinitioner. I stedet vælger du bogføringsdefinitionen i den avancerede finanspost. 

I dette scenarie blev kreditorfakturaen AP\_0949 fejlagtigt bogført til kapitalforbedringsmidlet 300-12300-51002 i stedet for til det generelle middel 100-39810-51001. Følgende eksempel viser, hvordan en avanceret finanspost kan bruge en bogføringsdefinition til at debitere kapitalforbedringsmidlet og kreditere det generelle middel.

### <a name="posting-definition--match-criteria--row-1"></a>Bogføringsdefinition – søgekriterier – række 1

| Kontostruktur | Sammenlign kontonummer\* | Prioritet |
|-------------------|------------------------|----------|
| Restværdi           | 300- -                 | 1        |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

### <a name="posting-definition--generated-entries-for-match-criteria--row-1"></a>Bogføringsdefinition – genererede poster for søgekriterier – række 1

| Kontostruktur | Genereret kontonummer | Genereret debet/kredit |
|-------------------|--------------------------|------------------------|
| Saldo           | 300-11001                | Balancere              |
| Saldo           | 900-11001                | Balancere              |
| Saldo           | 900-37300                | Samme                   |

### <a name="posting-definition--match-criteria--row-2"></a>Bogføringsdefinition – søgekriterier – række 2

| Kontostruktur | Sammenlign kontonummer\* | Prioritet |
|-------------------|------------------------|----------|
| Restværdi           | 100 - -                | 1        |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

### <a name="posting-definition--generated-entries-for-match-criteria--row-2"></a>Bogføringsdefinition – genererede poster for søgekriterier – række 2

| Kontostruktur | Genereret kontonummer | Genereret debet/kredit |
|-------------------|--------------------------|------------------------|
| Saldo           | 100-11001                | Balancere              |
| Saldo           | 900-11001                | Balancere              |
| Saldo           | 900-37301                | Samme                   |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Posteringer med konti, dimensionsværdier og beløb

| Konto + dimensioner | Debet | Kredit | Kommentar                    |
|----------------------|-------|--------|----------------------------|
| 300-12300-51002      | 350   |        | Avanceret finanspostlinje |
| 100-39810-51001      |       | 350    | Avanceret finanspostlinje |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Finansposter genereret fra bogføringsdefinitionen

| Konto + dimensioner | Debet | Kredit | Kommentar       |
|----------------------|-------|--------|---------------|
| 300-11001            |       | 350    | Oversigtspost |
| 900-11001            |       | 350    | Oversigtspost |
| 900-37300            | 350   |        | Oversigtspost |
| 100-11001            | 350   |        | Oversigtspost |
| 900-11001            | 350   |        | Oversigtspost |
| 900-37301            |       | 350    | Oversigtspost |

## <a name="examples-general-ledger-year-end-close"></a>Eksempel: årsafslutning for Finans
Organisationer bruger bogføringsdefinitioner i forbindelse med ultimo ved årsafslutningen af finanskonti. Bogføringsdefinitioner kan bruges til afslutning af konti til pengebalancer eller overførsel af årets resultat på basis af den klasseattribut, der er angivet for midlerne (dimensionen), kombineret med kontoens afslutningstypeattribut. Det er et krav, at der bruges bogføringsdefinitioner ved afslutning af finanskonti og til overførsel af saldi til primoperioden i det nye regnskabsår. 

> [!NOTE]
> For at bruge bogføringsdefinitioner til ultimo og primo ved årsafslutning skal du udføre følgende opsætningsopgaver:

-   På siden **Økonomiparametre** i afsnittet **Finans** på oversigtspanelet **Årsafslutning** skal du vælge indstillingen **Opret ultimoposteringer ved overførsel**.
-   På siden **Hovedkonti - kontoplan: %1** skal du oprette en konto til lukning.

Følgende eksempler på bogføringsdefinitioner viser ultimo for midler for offentlige myndigheder og beskyttede midler.

### <a name="governmental-funds-example"></a>Eksempler på midler fra offentlige myndigheder

#### <a name="governmental-funds--posting-definition--match-criteria--row-1"></a>Midler fra offentlige myndigheder – bogføringsdefinition – søgekriterier – række 1

| Kontostruktur | Sammenlign kontonummer\* | Prioritet |
|-------------------|------------------------|----------|
| Udgift           | - - -                  | 1        |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

#### <a name="governmental-funds--posting-definition--generated-entries-for-match-criteria--row-1"></a>Midler fra offentlige myndigheder – bogføringsdefinition – genererede poster for søgekriterier – række 1

| Kontostruktur | Genereret kontonummer          | Genereret debet/kredit |
|-------------------|-----------------------------------|------------------------|
| Kontostruktur | -37300 (Saldo for midler, der ikke er hensat) | Balancere              |

#### <a name="governmental-funds--posting-definition--match-criteria--row-2"></a>Midler fra offentlige myndigheder – bogføringsdefinition – søgekriterier – række 2

| Kontostruktur | Sammenlign kontonummer\* | Prioritet |
|-------------------|------------------------|----------|
| Udgift           | - - -                  | 1        |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

#### <a name="governmental-funds--posting-definition--generated-entries-for-match-criteria--row-2"></a>Midler fra offentlige myndigheder – bogføringsdefinition – genererede poster for søgekriterier – række 2

| Kontostruktur | Genereret kontonummer          | Genereret debet/kredit |
|-------------------|-----------------------------------|------------------------|
| Kontostruktur | -37300 (Saldo for midler, der ikke er hensat) | Balancere              |

#### <a name="governmental-funds--posting-definition--match-criteria--row-3"></a>Midler fra offentlige myndigheder – bogføringsdefinition – søgekriterier – række 3

| Kontostruktur | Sammenlign kontonummer\* | Prioritet |
|-------------------|------------------------|----------|
| Indtægter           | - - -                  | 1        |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

#### <a name="governmental-funds--posting-definition--generated-entries-for-match-criteria--row-3"></a>Midler fra offentlige myndigheder – bogføringsdefinition – genererede poster for søgekriterier – række 3

| Kontostruktur | Genereret kontonummer          | Genereret debet/kredit |
|-------------------|-----------------------------------|------------------------|
| Kontostruktur | -37300 (Saldo for midler, der ikke er hensat) | Balancere              |

Når du har oprettet bogføringsdefinitionen, skal du tildele den til transaktionstypen **Finans, ultimo** på siden **Definitioner af posteringsbogføring**.

#### <a name="governmental-funds--transactions-with-the-accounts-dimension-values-and-amounts"></a>Midler fra offentlige myndigheder – posteringer med konti, dimensionsværdier og beløb

Saldoen for finanskontiene via den valgte periode vises på siden **Primoposter**.

| Konto + dimensioner | Debet  | Kredit | Kommentar |
|----------------------|--------|--------|---------|
| 101-66100-130        | 250,00 |        |         |

#### <a name="governmental-funds--ledger-entries-generated-from-the-posting-definition"></a>Midler fra offentlige myndigheder – finansposter genereret fra bogføringsdefinitionen

Genererede finansposter oprettes til registrering af ultimoposteringen.

| Konto + dimensioner | Debet  | Kredit | Kommentar |
|----------------------|--------|--------|---------|
| 101-66100-130-       |        | 250,00 |         |
| 101-37300            | 250,00 |        |         |

I dette eksempel defineres midlet 101 som klassen **Offentlig** på siden **Midler** i Finans. På siden **Definitioner af posteringsbogføring** er ultimo-transaktionstypen **Finans** knyttet til klassen **Offentlig** og bogføringsdefinitionen. 

Bogføringsdefinitionen leder efter en overensstemmelse på en hvilken som helst kontodel af udgiftskontostrukturen. Når 101-66100-130- evalueres, bruges der derfor samme finanskonto, beløbet tilbageføres for at afslutte kontoen, og den genererede reguleringspost i finans oprettes.

### <a name="proprietary-funds-example"></a>Eksempel med beskyttede midler

#### <a name="proprietary-funds--posting-definition--match-criteria--row-1"></a>Beskyttede midler – bogføringsdefinition – søgekriterier – række 1

| Kontostruktur | Sammenlign kontonummer\* | Prioritet |
|-------------------|------------------------|----------|
| Restværdi           | - - -                  | 1        |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

#### <a name="proprietary-funds--posting-definition--generated-entries-for-match-criteria--row-1"></a>Beskyttede midler – bogføringsdefinition – genererede poster for søgekriterier – række 1

| Kontostruktur | Genereret kontonummer   | Genereret debet/kredit |
|-------------------|----------------------------|------------------------|
| Kontostruktur | -37310 (Overført resultat) | Balancere              |

#### <a name="proprietary-funds--posting-definition--match-criteria--row-2"></a>Beskyttede midler – bogføringsdefinition – søgekriterier – række 2

| Kontostruktur | Sammenlign kontonummer\* | Prioritet |
|-------------------|------------------------|----------|
| Udgift           | - - -                  | 1        |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

#### <a name="proprietary-funds--posting-definition--generated-entries-for-match-criteria--row-2"></a>Beskyttede midler – bogføringsdefinition – genererede poster for søgekriterier – række 2

| Kontostruktur | Genereret kontonummer   | Genereret debet/kredit |
|-------------------|----------------------------|------------------------|
| Kontostruktur | -37310 (Overført resultat) | Balancere              |

#### <a name="proprietary-funds--posting-definition--match-criteria--row-3"></a>Beskyttede midler – bogføringsdefinition – søgekriterier – række 3

| Kontostruktur | Sammenlign kontonummer\* | Prioritet |
|-------------------|------------------------|----------|
| Indtægter           | - - -                  | 1        |

\*Hvis feltet **Sammenlign kontonummer** er tomt, betyder det, at alle matchende konti i den definerede kontostruktur vil indgå i matchningsreglen.

#### <a name="proprietary-funds--posting-definition--generated-entries-for-match-criteria--row-3"></a>Beskyttede midler – bogføringsdefinition – genererede poster for søgekriterier – række 3

| Kontostruktur | Genereret kontonummer   | Genereret debet/kredit |
|-------------------|----------------------------|------------------------|
| Kontostruktur | -37310 (Overført resultat) | Balancere              |

Når du har oprettet bogføringsdefinitionen, skal du tildele den til ultimo-transaktionstypen **Finans** på siden **Definitioner af posteringsbogføring**.

#### <a name="proprietary-funds--transactions-with-the-accounts-dimension-values-and-amounts"></a>Beskyttede midler – posteringer med konti, dimensionsværdier og beløb

Saldoen for finanskontiene via den valgte periode vises på siden **Primoposter**.

| Konto + dimensioner | Debet  | Kredit | Kommentar |
|----------------------|--------|--------|---------|
| 601-66100-130        | 250,00 |        |         |

#### <a name="proprietary-funds--ledger-entries-generated-from-the-posting-definition"></a>Beskyttede midler – finansposter genereret fra bogføringsdefinitionen

Genererede finansposter oprettes til registrering af ultimoposteringen.

| Konto + dimensioner | Debet  | Kredit | Kommentar |
|----------------------|--------|--------|---------|
| 601-66100-130-       |        | 250,00 |         |
| 601-37310            | 250,00 |        |         |

I dette eksempel defineres midler med betegnelsen 601 som klassen **Privat** på siden **Midler**. På siden **Definitioner af posteringsbogføring** er ultimo-transaktionstypen **Finans** knyttet til klassen **Privat** og bogføringsdefinitionen. 

Bogføringsdefinitionen leder efter en overensstemmelse på en hvilken som helst kontodel af udgiftskontostrukturen. Når 601-66100-130- evalueres, bruges der derfor samme finanskonto, beløbet tilbageføres for at afslutte kontoen, og den genererede reguleringspost i finans oprettes.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Kreditorer](../accounts-payable/accounts-payable.md)

[Kreditor i den offentlige sektor](accounts-payable-public-sector.md)

[Debitor i den offentlige sektor](accounts-receivable-public-sector.md)

[Budgetlægning i den offentlige sektor](budgeting-public-sector.md)

[Finans i den offentlige sektor](general-ledger-public-sector.md)



