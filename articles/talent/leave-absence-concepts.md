---
title: Orlovs- og fraværskoncepter
description: I dette emne beskrives orlovs- og fraværskoncepter, og hvordan fritidssaldi bestemmes.
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 03e2557e29194f17a9a586470ced5b352408b07c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460714"
---
# <a name="leave-and-absence-concepts"></a>Orlovs- og fraværskoncepter

De begreber og udtryk, der er beskrevet i dette emne, kan hjælpe dig med at finde ud af, hvordan en medarbejder tildeles fritid, og hvordan denne medarbejders fritidssaldi beregnes. Du kan finde flere oplysninger om håndtering af orlov og fravær under [Orlov og fravær](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).

## <a name="leave-plan-details"></a>Detaljer for orlovsplaner

### <a name="start-date"></a>Igangsæt dato

Startdatoen er den dato, hvor periodiseringsbehandlingen begynder. Startdatoen fungerer også som årsdag, og bruges som sådan til at beregne overførte beløb.

## <a name="accruals"></a>Periodiseringer

Periodiseringer bestemmer, hvornår og hvor ofte en medarbejder tildeles fritid. Regler for, hvornår periodiseringer skal tildeles og regler for proportionalitet, defineres i sektionen **Periodiseringer**, når du opretter planen for orlov og fravær.

### <a name="accrual-frequency"></a>Periodiseringsfrekvens

Periodiseringsfrekvensen definerer, hvor ofte orlov periodiseres eller tildeles. Følgende valgmuligheder er tilgængelige:

- Daglig
- Ugentlig
- Hver 14. dag
- Halvmånedligt
- Månedligt
- Kvartårlig
- Halvårligt
- Årligt
- Ingen

### <a name="accrual-period-basis"></a>Grundlag for periodiseringsperiode

Grundlaget for periodiseringsperioden bestemmer den dato, der bruges til at beregne periodiseringsperioder. Følgende valgmuligheder er tilgængelige:

- **Startdato for plan**
- **Medarbejderspecifik dato** – Når denne indstilling er valgt, bestemmer værdien kilden til værdien for den første dato, der bruges til at beregne periodiseringsperioder. Følgende valgmuligheder er tilgængelige:

    - Brugerdefineret
    - Jubilæumsdato
    - Oprindelig ansættelsesdato
    - Anciennitetsdato
    - Justeret startdato for medarbejder
    - Startdato for medarbejder

### <a name="accrual-award-date"></a>Dato for periodisering af bonus

Dato for periodisering af bonus bestemmer, hvornår en medarbejder tildeles fritid. Følgende valgmuligheder er tilgængelige:

- **Slutdato for periodiseringsperiode** – Medarbejderen bliver tildelt fritid fra den sidste dag i bonusperioden.

    Hvis du vil periodisere det korrekte beløb, skal periodiseringsprocessen omfatte hele perioden. Eksempelvis er periodiseringsperioden 1. januar 2018 til og med 31. januar 2018. Hvis januar skal medtages i dette eksempel, skal periodiseringen køres for 1. februar 2018.

- **Startdato for periodiseringsperiode** – Medarbejderen bliver tildelt fritid fra den første dag i bonusperioden.

### <a name="accrual-policy-on-enrollment"></a>Periodiseringspolitik for tilmelding

Periodiseringspolitikken for tilmeldinger definerer, hvordan periodisering beregnes, når en medarbejder tilmeldes midt i en periodiseringsperiode. Følgende valgmuligheder er tilgængelige:

- **Forholdsmæssig beregning** – Datointervallet mellem tilmeldings- og startdatoen bruges til at bestemme forskellen i dage. Denne forskel anvendes, når periodiseringer behandles.
- **Fuld periodisering** – Det fulde periodiserede beløb, baseret på niveauet, tildeles under første periodiseringsbehandling.
- **Ingen periodisering** – Der tildeles ikke nogen periodisering før næste periodiseringsperiode.

### <a name="accrual-policy-on-unenrollment"></a>Periodiseringspolitik for fjernelse af tilmelding

Periodiseringspolitikken for fjernelse af tilmeldinger definerer, hvordan periodisering beregnes, når en medarbejders tilmelding fjernes midt i en periodiseringsperiode. Følgende valgmuligheder er tilgængelige:

- **Forholdsmæssig beregning** – Datointervallet mellem tilmeldings- og startdatoen bruges til at bestemme forskellen i dage. Denne forskel anvendes, når periodiseringer behandles.
- **Fuld periodisering** – Det fulde periodiserede beløb, baseret på niveauet, tildeles under første periodiseringsbehandling.
- **Ingen periodisering** – Der tildeles ikke nogen periodisering før næste periodiseringsperiode.

## <a name="accrual-schedule"></a>Periodiseringstidsplan

Periodiseringstidsplanen bestemmer, hvordan en medarbejder vil periodisere fritid, og hvilke beløb vedkommende vil periodisere og overføre. Du kan oprette niveauer, så der tildeles fritid baseret på forskellige niveauer.

### <a name="months-of-service"></a>Måneders tjeneste

Værdien **Måneders tjeneste** angiver det mindste antal måneder, som medarbejdere skal arbejde for at være berettiget til periodiseringer. Hvis der ikke kræves et minimum for medarbejdere, kan du indstille værdien til **0**.

### <a name="hours-worked"></a>Antal arbejdstimer

Værdien **Antal arbejdstimer** angiver det mindste antal timer, som medarbejdere skal arbejde pr. periodiseringsperiode for at være berettiget til periodiseringer. Hvis der ikke kræves et minimum for medarbejdere, kan du indstille værdien til **0**.

### <a name="accrual-amount"></a>Periodiseringsbeløb

Periodiseringsbeløbet er det antal timer eller dage, som medarbejderen periodiserer pr. periode. Perioden er baseret på periodiseringsfrekvensen.

### <a name="minimum-balance"></a>Mindste saldo

En negativ værdi kan bruges til minimumsaldoen, hvis medarbejderen kan anmode om mere orlov, end han eller hun er berettiget til.

### <a name="maximum-carry-forward"></a>Maksimumoverførsel

Periodiseringsprocessen regulerer orlovssaldi, der overskrider den maksimale overførte saldo på årsdagen for startdatoen.

### <a name="grant-amount"></a>Bonusbeløb

Bonusbeløbet er det indledende antal timer eller dage, der tildeles medarbejdere, når de tilmelder sig orlovsplanen. Beløbet periodiseres ikke for hver periodiseringsperiode.

## <a name="enrollments-and-balances"></a>Tilmeldinger og saldi

### <a name="enrollment-date"></a>Tilmeldingsdato

Tilmeldingsdatoen bestemmer, hvornår medarbejderen kan begynde at periodisere fritid. Hvis medarbejderen f.eks. er tilmeldt en ferieplan den 15. juni 2018, kan hun ikke periodisere fritid før den 15. juni 2018.

### <a name="current-balance"></a>Aktuel saldo

Den aktuelle saldo er den samlede orlov, der er tilgængelig for anmodninger om fritid. Dette omfatter periodiseringer, godkendte anmodninger og reguleringer til og med den aktuelle dato.

### <a name="current-balance-examples"></a>Eksempler på aktuel saldo

#### <a name="annual-plan"></a>Årlig plan

**Planopsætning**

| Startdato for plan | Tilmeldingsdato | Periodiseringsfrekvens | Grundlag for periodiseringsperiode | Dato for periodisering af bonus    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Årlig            | Startdato for plan      | Slut på periodiseringsperiode |

Periodiseringer behandles den 1. januar 2019 (01-01-2019), så hele perioden er inkluderet.

**Resultater**

| Periodiseringsbeløb | Mindste saldo | Maksimumoverførsel | Ønsket beløb | Aktuel saldo (pr. 01-01-2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Aktuel saldo (160) = Periodiseringsbeløb (200) – Ønsket beløb (40)

#### <a name="semimonthly-plan"></a>Halvmånedlig plan

**Planopsætning**

| Startdato for plan | Tilmeldingsdato | Periodiseringsfrekvens | Grundlag for periodiseringsperiode | Dato for periodisering af bonus    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Halvmånedligt       | Startdato for plan      | Slut på periodiseringsperiode |

Periodiseringer behandles den 1. maj 2018 (05-01-2018), så hele perioden er inkluderet.

**Resultater**

| Periodiseringsbeløb | Mindste saldo | Maksimumoverførsel | Ønsket beløb | Aktuel saldo (pr. 01-01-2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 22                               |

Aktuel saldo (22) = Periodiseringsbeløb (5 × 6) – Ønsket beløb (8)

#### <a name="monthly-plan"></a>Månedlig plan

**Planopsætning**

| Startdato for plan | Tilmeldingsdato | Periodiseringsfrekvens | Grundlag for periodiseringsperiode | Dato for periodisering af bonus    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Halvmånedligt       | Startdato for plan      | Slut på periodiseringsperiode |

Periodiseringer behandles den 1. maj 2018 (05-01-2018), så hele perioden er inkluderet.

**Resultater**

| Periodiseringsbeløb | Mindste saldo | Maksimumoverførsel | Ønsket beløb | Aktuel saldo (pr. 01-01-2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Aktuel saldo (7) = Periodiseringsbeløb (5 × 3) – Ønsket beløb (8)

### <a name="forecasted-balance"></a>Budgetteret saldo

Den *budgetterede saldo* er den samlede orlov på en fremtidig dato. Periodiseringer og regulerede overførsler budgetteres indtil denne dato.

Følgende formel bruges:

Budgetteret saldo mandag = Aktuel saldo – Anmodninger + Periodiseringer – Reguleret overførsel

### <a name="forecasted-balance-examples"></a>Eksempler på budgetterede saldi

#### <a name="annual-plan"></a>Årlig plan

**Planopsætning**

| Startdato for plan | Tilmeldingsdato | Periodiseringsfrekvens | Grundlag for periodiseringsperiode | Dato for periodisering af bonus    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Årlig            | Startdato for plan      | Slut på periodiseringsperiode |

Periodiseringer behandles den 15. februar 2019 (15-02-2019), så hele perioden er inkluderet.

**Resultater**

| Periodiseringsbeløb | Mindste saldo | Maksimumoverførsel | Aktuel saldo | Budgetteret saldo (pr. 15-02-2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20             | 0               | 20                    | 40              | 40                                   |

Budgetteret saldo (40) = Periodiseringsbeløb (20) + Aktuel saldo (40) – Reguleret overførsel (20)

#### <a name="semimonthly-plan"></a>Halvmånedlig plan

**Planopsætning**

| Startdato for plan | Tilmeldingsdato | Periodiseringsfrekvens | Grundlag for periodiseringsperiode | Dato for periodisering af bonus    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Halvmånedligt       | Startdato for plan      | Slut på periodiseringsperiode |

Periodiseringer behandles den 15. februar 2019 (15-02-2019), så hele perioden er inkluderet.

**Resultater**

| Periodiseringsbeløb | Mindste saldo | Maksimumoverførsel | Aktuel saldo | Budgetteret saldo (pr. 15-02-2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5              | 0               | 20                    | 40              | 35                                   |

Budgetteret saldo (35) = Periodiseringsbeløb (5 × 3) + Aktuel saldo (40) – Reguleret overførsel (20)

#### <a name="monthly-plan"></a>Månedlig plan

**Planopsætning**

| Startdato for plan | Tilmeldingsdato | Periodiseringsfrekvens | Grundlag for periodiseringsperiode | Dato for periodisering af bonus    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Halvmånedligt       | Startdato for plan      | Slut på periodiseringsperiode |

Periodiseringer behandles den 15. februar 2019 (15-02-2019), så hele perioden er inkluderet.

**Resultater**

| Periodiseringsbeløb | Mindste saldo | Maksimumoverførsel | Aktuel saldo | Budgetteret saldo (pr. 15-02-2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10             | 0               | 20                    | 40              | 30                                   |

Budgetteret saldo (30) = Periodiseringsbeløb (10 × 1) + Aktuel saldo (40) – Reguleret overførsel (20)

### <a name="proration-balance-examples"></a>Eksempler på proportionalitetssaldo

#### <a name="prorated-monthly-plan"></a>Forholdsmæssigt beregnet månedlige plan

**Planopsætning**

| Startdato for plan | Periodiseringsfrekvens | Grundlag for periodiseringsperiode |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Månedligt           | Startdato for plan      |

**Resultater**

| Medarbejder            | Måneders tjeneste | Tilmeldingsdato | Igangsæt dato | Periodiseringsbeløb | Behandling af periodisering | Restværdi |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2,53    |

#### <a name="full-accrual-monthly-plan"></a>Fuld månedlig periodiseringsplan

**Planopsætning**

| Startdato for plan | Periodiseringsfrekvens | Grundlag for periodiseringsperiode |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Månedligt           | Startdato for plan      |

**Resultater**

| Medarbejder            | Måneders tjeneste | Tilmeldingsdato | Igangsæt dato | Periodiseringsbeløb | Behandling af periodisering | Restværdi |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>Ingen månedlig periodiseringsplan

**Planopsætning**

| Startdato for plan | Periodiseringsfrekvens | Grundlag for periodiseringsperiode |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Månedligt           | Startdato for plan      |

**Resultater**

| Medarbejder            | Måneders tjeneste | Tilmeldingsdato | Igangsæt dato | Periodiseringsbeløb | Behandling af periodisering | Restværdi |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2.00    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]