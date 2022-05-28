---
title: Oprette gebyrkoder
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere gebyrkoder for både Kreditor og Debitor.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MarkupTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e8526fa0f3c6e3d1b545703f6e6ef72f558b57bd
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735021"
---
# <a name="create-charges-codes"></a>Oprette gebyrkoder

Dette emne indeholder en forklaring på, hvordan du kan konfigurere gebyrkoder for både Kreditor og Debitor. Hvis din organisation kræver, at salgs- eller købsbeløb kan spores i tillæg til linjeelementer i en salgsordre eller indkøbsordre, kan du bruge gebyrkoder til dette formål. For eksempel betaler du fragt og forsikring på en indkøbsordre, og disse beløb specificeres separat på indkøbsordren. Du kan i dette tilfælde angive, om beløbene skal bogføres til udgiftskonti eller lægges til vareomkostningerne.

## <a name="set-up-charges-codes-for-accounts-receivable"></a>Oprette gebyrkoder for Debitor

Benyt følgende fremgangsmåde for at oprette gebyrkoder for Debitor.

1. Gå til **Debitor** &gt; **Konfiguration af gebyrer** &gt; **Gebyrkode**.
2. Vælg **Ny**.
3. Indtast en kode for gebyret i feltet **Gebyrkode**.
3. Angiv en beskrivelse af gebyret i feltet **Beskrivelse**.
4. Valgfrit: Vælg en momsgruppe i feltet **Varemomsgruppe**.
5. Angiv i oversigtspanelet **Postering**, hvordan gebyret automatisk debiteres og krediteres.
6. Hvis du har valgt **Finanskonto** som debet- eller kredittype, skal du angive en bogføringstype i felterne **Postering** og angive hovedkontoen i felterne **Konto**.

### <a name="example"></a>Eksempel

Din kunde betaler gebyret. Derfor føjes det til salgsordretotalerne. Du angiver følgende bogføringsoplysninger:

- I feltet **Type** i sektionen **Debet** skal du vælge **Debitor/Kreditor** for at føje fakturagebyret til debitors konto.
- Vælg **Finanskonto** i feltet **Type** i afsnittet **Kredit**. Derefter skal du vælge hovedkontoen for indtægter fra fakturagebyrer i feltet **Konto**.

> [!NOTE]
> Du kan angive en anden valuta for gebyrtransaktionen, hvis debet- eller kredittypen for den valgte kode enten er **Finanskonto** eller **Vare**.

Du kan udskrive teksten til gebyr på det sprog, der et tilknyttet debitoren. Vælg **Oversættelser** for at angive teksten til gebyrkoden på andre sprog.

## <a name="set-up-charges-codes-for-accounts-payable"></a>Oprette gebyrkoder for Kreditor

Benyt følgende fremgangsmåde for at oprette gebyrkoder for Kreditor.

1. Udfør ét af følgende trin:

    - Gå til **Kreditor** &gt; **Konfiguration** af **gebyrer** &gt; **Gebyrkode**.
    - Gå til **Indkøb og forsyning** &gt; **Opsætning** &gt; **Gebyrer** &gt; **Gebyrkode**.

2. Vælg **Ny**.
3. Indtast en kode for gebyret i feltet **Gebyrkode**.
3. Angiv en beskrivelse af gebyret i feltet **Beskrivelse**.
4. Valgfrit: Vælg en momsgruppe i feltet **Varemomsgruppe**.
5. Valgfrit: Angiv i feltet **Maks. beløb** det maksimale beløb, der er tilladt for gebyrkoden.

    Dette felt bruges til at validere gebyrer for kreditorfakturaer. Hvis du vil aktivere validering af gebyrer, skal du markere afkrydsningsfeltet **Aktivér validering af fakturasammenholdelse** under fanen **Fakturavalidering** på siden **Kreditorparametre**.

    > [!IMPORTANT]
    > Når du skal validere fakturagebyrer, skal du også oprette en forekomst af en politikregeltype, der er baseret på gebyrer for den konkrete politik for kreditorfaktura.

6. Angiv i oversigtspanelet **Postering**, hvordan gebyret automatisk debiteres og krediteres.
7. Hvis du har valgt **Finanskonto** som debet- eller kredittype, skal du angive en bogføringstype i felterne **Debetkontering** og **Kreditkontering** og angive hovedkontoen i felterne **Debetkonto** og **Kreditkonto**.
8. Hvis du vil aktivere sammenligning af gebyrværdier for en faktura, der indeholder gebyrer fra hovedet eller linjerne i den tilsvarende indkøbsordre, skal du markere afkrydsningsfeltet **Sammenlign værdier på indkøbsordre og faktura**.

### <a name="example"></a>Eksempel

Du kan registrere gebyret som en udgift, der er en del af det samlede beløb for indkøbsordren eller kreditorfakturaen. Benyt følgende fremgangsmåde for at konfigurere bogføringsoplysninger. 

- I feltet **Type** i sektionen **Kredit** skal du vælge **Debitor/Kreditor** for at føje fakturagebyret til kreditors konto.
- Vælg **Finanskonto** i feltet **Type** i afsnittet **Debit**. Derefter skal du vælge hovedkontoen for udgifter fra fakturagebyrer i feltet **Konto**.

Benyt følgende fremgangsmåde for at konfigurere bogføringsoplysninger, så enhedsgebyret føjes til varens kostpris.

- I feltet **Type** i sektionen **Kredit** skal du vælge **Debitor/Kreditor** for at føje fakturagebyret til kreditors konto.
- I feltet **Type** i sektionen **Debet** skal du vælge **Vare** for at føje gebyret til vareomkostningerne.

> [!NOTE]
> Måske vil du bruge en anden valuta end den, der er angivet på indkøbsordren eller fakturaen. Du kan angive en anden valuta, hvis debet- eller kredittypen for den valgte gebyrkode enten er **Finanskonto** eller **Vare**.

Du kan udskrive teksten til gebyr på det sprog, der et tilknyttet debitoren. Vælg **Oversættelser** for at angive teksten til gebyrkoden på andre sprog.
