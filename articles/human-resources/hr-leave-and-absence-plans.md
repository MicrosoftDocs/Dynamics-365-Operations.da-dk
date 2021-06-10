---
title: Oprette en orlovs- og fraværsplan
description: Opret orlovsplaner i Dynamics 365 Human Resources for forskellige typer orlov.
author: andreabichsel
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 26d85ce226bd601e3ce0bc789e54a7a1a7ec6812
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057568"
---
# <a name="create-a-leave-and-absence-plan"></a>Oprette en orlovs- og fraværsplan

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Definer orlovs og fraværsplaner i Dynamics 365 Human Resources for hver type orlov, du tilbyder. Orlovs og fraværsplaner kan periodiseres ved forskellige frekvenser, f.eks. årligt, månedligt eller halvmånedligt. Du kan også definere en plan som et tilskud, hvor en enkelt periodisering forekommer på en bestemt dato. Du kan f.eks. oprette en plan, der giver flydende helligdage årligt.

Lagdelte orlovsplaner giver medarbejderne mulighed for at modtage frynsegoder baseret på, hvor meget tid de har tilbragt i en organisation. I lagdelte planer aktiveres automatisk registrering i ekstra frynsegodetimer.

Du kan angive overførte maksimumbeløb eller minimumsaldi for at sikre, at medarbejderne kun bruger de frynsegodetimer, de har periodiseret.

Hvis du f.eks. har en lagdelt plan, kan du tildele en frynsegode på 80 timers betalt fritid (PTO) til nye medarbejdere. Du kan derefter tildele 120 timers tjeneste på 60 måneder.

Du kan også oprette stillingsbaserede orlovsfrynsegoder, f.eks. frynsegodetimer for ledere.

## <a name="create-a-leave-plan"></a>Oprette en orlovsplan

1. På siden **Orlov og fravær** skal du vælge **Opret ny plan**.

2. Under **Oplysninger** skal du angive **Navn**, **Startdato**, **Beskrivelse** og **Orlovstype** for din plan.

Hvis funktionen **Konfigurer flere orlovstyper for en enkelt orlovs- og fraværsplan** er aktiveret, konfigureres orlovstyperne i **Periodiseringsplan** i stedet for under **Detaljer**. For hver post i periodiseringsplanens tabel kan du definere en orlovstype. Når denne funktion er aktiveret, skal du også bruge nye dataenheder til integrationer eller andre scenarier, hvor du skal bruge enheder. 

De nye enheder er:

- Banktransaktion for orlov og fravær V2
- Orlovs- og fraværstilmelding V2
- Orlovs- og fraværsplanniveau V2
- Orlovs- og fraværsplan V2
- Orlovsanmodning V2

 > [!IMPORTANT]
   > Du kan ikke deaktivere denne funktion, når du har aktiveret den.

3. Definer periodiseringer under fanen **Periodiseringer**. Periodiseringer bestemmer, hvornår og hvor ofte en medarbejder tildeles fritid. I dette trin definerer du politikker for, hvornår periodiseringer skal tildeles, og politikker for proportionale værdier af orlovsfordele.

   1. Vælg en værdi på rullelisten **Periodiseringsfrekvens**:

      - Daglig
      - Ugentlig
      - Hver 14. dag
      - Halvmånedligt
      - Månedligt
      - Kvartårlig
      - Halvårligt
      - Årligt
      - Ingen

   2. Vælg en indstilling fra rullelisten **Grundlag for periodiseringsperiode** for at bestemme den startdato, der bruges til beregning af periodiseringsperioder:

      | Grundlag for periodiseringsperiode | Beskrivelse |
      | --- | --- |
      | **Startdato for plan** | Startdatoen for periodiseringsperioden er den dato, hvor planen er tilgængelig. |
      | **Medarbejderspecifik dato** | Startdatoen for periodiseringsperioden afhænger af en medarbejderhændelse:</br><ul><li>Brugerdefineret (du skal angive et periodiseringsdatogrundlag for hver enkelt tilmelding)</li><li>Jubilæumsdato</li><li>Oprindelig ansættelsesdato</li><li>Anciennitetsdato</li><li>Justeret startdato for medarbejder</li><li>Startdato for medarbejder</li></ul> |

   3. Vælg en indstilling fra rullelisten **Dato for periodisering af bonus**:

      - **Slutdato for periodiseringsperiode** – Medarbejderen bliver tildelt fritid fra den sidste dag i bonusperioden. Hvis du vil periodisere det korrekte beløb, skal periodiseringsprocessen omfatte hele perioden. Hvis periodiseringsperioden f.eks. er 1. januar, 2020 til 31. januar 2020, skal du køre periodiseringen for 1. februar 2020 for at medtage januar.

      - **Startdato for periodiseringsperiode** – Medarbejderen bliver tildelt fritid fra den første dag i bonusperioden.

   4. Vælg en indstilling fra rullelisten **Periodiseringspolitik for tilmelding**. Denne værdi definerer, hvordan du kan beregne periodisering, når en medarbejder tilmeldes midt i en periodiseringsperiode.

      - **Forholdsmæssig beregning** – Datointervallet mellem tilmeldings- og startdatoen bruges til at bestemme forskellen i dage. Denne forskel anvendes, når periodiseringer behandles.

      - **Fuld periodisering** – Det fulde periodiserede beløb, baseret på niveauet, tildeles under første periodiseringsbehandling.

      - **Ingen periodisering** – Der tildeles ikke nogen periodisering før næste periodiseringsperiode.

   5. Vælg en indstilling fra rullelisten **Periodiseringspolitik for framelding**. Denne værdi definerer, hvordan du kan beregne periodisering, når en medarbejder frameldes midt i en periodiseringsperiode.

      - **Forholdsmæssig beregning** – Datointervallet mellem tilmeldings- og startdatoen bruges til at bestemme forskellen i dage. Denne forskel anvendes, når periodiseringer behandles.

      - **Fuld periodisering** – Det fulde periodiserede beløb, baseret på niveauet, tildeles under første periodiseringsbehandling.

      - **Ingen periodisering** – Der tildeles ikke nogen periodisering før næste periodiseringsperiode.

4. Definer periodiseringsplanen under fanen **Periodiseringsplan**. Periodiseringsplanen bestemmer:

   - Hvordan en medarbejder periodiserer fridage
   - Hvilke beløb medarbejderen skal periodisere
   - Hvilke beløb der skal overføres

   Du kan oprette niveauer, så der tildeles fritid baseret på forskellige niveauer.

   Hvis du har timeansatte, kan du tildele fridage baseret på arbejdstimer i stedet for ansættelsestid i din organisation. Data for arbejdstimer er typisk gemt i et system for tid og fremmøde. Du kan importere almindelige arbejds- og overtidstimer fra systemet til tid og fremmøde og bruge dem som grundlag for en medarbejders bonus.
   
    1. Vælg en indstilling fra rullelisten **Periodiseringstype**:

      - **Måneders tjeneste** - Baserer periodiseringsplanen på måneder i tjenesten.

      - **Antal arbejdstimer** - Baserer periodiseringsplanen på timer, der er arbejdet. Du kan finde flere oplysninger om periodiseringer for arbejdstimer under [Periodisere fravær baseret på antal arbejdstimer](hr-leave-and-absence-plans.md?accrue-time-off-based-on-hours-worked).

      Du kan finde flere oplysninger om periodiseringssaldi under [Periodisere fravær baseret på antal arbejdstimer](hr-leave-and-absence-plans.md?enrollments-and-balances).

    2. Angiv værdier i periodiseringsplanens tabel:

      - **Måneders tjeneste** - Det mindste antal måneder, som medarbejdere skal arbejde for at være berettiget til periodiseringer. Hvis du ikke kræver et minimum, skal du angive værdien til 0.

      - **Antal arbejdstimer** - Det mindste antal timer, som medarbejdere skal arbejde pr. periodiseringsperiode for at være berettiget til periodiseringer. Hvis du ikke kræver et minimum, skal du angive værdien til 0.

      - **Periodiseringsbeløb** - Det antal timer eller dage, som medarbejderen periodiserer pr. periode. Perioden er baseret på periodiseringsfrekvensen.

      - **Mindste saldo** - Du kan bruge en negativ værdi som minimumsaldoen, hvis medarbejderen kan anmode om mere orlov, end der er tilgængelig.

      - **Maksimumoverførsel** - Periodiseringsprocessen regulerer orlovssaldi, der overskrider den maksimale overførte saldo på årsdagen for startdatoen.

      - **Bonusbeløb** - Bonusbeløbet er det indledende antal timer eller dage, der tildeles medarbejdere, når de tilmelder sig orlovsplanen. Beløbet periodiseres ikke for hver periodiseringsperiode.
      
Hvis funktionen **Konfigurer flere orlovstyper for en enkelt orlovs- og fraværsplan** er aktiveret, skal du vælge en indstilling fra **Orlovstype**. 

   > [!IMPORTANT]
   > Du kan ikke deaktivere denne funktion, når du har aktiveret den.

Hvis funktionen **Brug fuldtidsækvivalens** er aktiveret, bruger Human Resources den fuldtidsækvivalens (FTE), der er defineret for stillingen, til at beregne en medarbejders periodisering forholdsmæssigt. Hvis FTE f.eks. er 0,5, og det periodiserede beløb er 10, vil medarbejderen periodisere 5. Du kan kun bruge denne funktion, hvis du aktiverer flere orlovstyper.  

5. Vælg **Gem**.

## <a name="accrue-time-off-based-on-hours-worked"></a>Periodisere fravær baseret på antal arbejdstimer

Hvis du har timeansatte, kan du tildele fridage baseret på arbejdstimer i stedet for ansættelsestid i din organisation. Data for arbejdstimer er typisk gemt i et system for tid og fremmøde. Du kan importere almindelige arbejds- og overtidstimer fra dit system til tid og fremmøde og bruge dem som grundlag for en medarbejders bonus.

Når du vælger arbejdstimer som periodiseringstype, kan du bruge to typer timer til periodisering: normale og overtid. Periodiseringsplaner for behandling af arbejdstimer bruger periodiseringsfrekvensen sammen med grundlaget for periodiseringsperioden til at bestemme timerne, der skal periodiseres.

### <a name="annual-accrual-frequency"></a>Årlig periodiseringsfrekvens

| Dato for periodiseringsbonus    | Niveau for antal arbejdstimer    | Periodiseringsbeløb        | Datoer for antal arbejdstimer   | Faktiske antal arbejdstimer| Bonus               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 12/31/2018            | 2080                 | 144                   | 01-01-2018 til 31-12-2018  | 2085                | 144                 |        
| 12/31/2018            | 2080                 | 144                   | 01-01-2018 til 31-12-2018  | 2000                | 0                 |


### <a name="monthly-accrual-frequency"></a>Månedlig periodiseringsfrekvens

| Dato for periodiseringsbonus    | Niveau for antal arbejdstimer    | Periodiseringsbeløb        | Datoer for antal arbejdstimer   | Faktiske antal arbejdstimer| Bonus               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 01-08-2018 til 31-08-2018   | 184                 | 12                  |        
| 8/31/2018             | 160                  | 3                     | 01-08-2018 til 31-08-2018   | 184                 | 3                   |

### <a name="semi-monthly-accrual-frequency"></a>Halvmånedlig periodiseringsfrekvens

| Dato for periodiseringsbonus    | Niveau for antal arbejdstimer    | Periodiseringsbeløb        | Datoer for antal arbejdstimer   | Faktiske antal arbejdstimer| Bonus               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 80                   | 6                     | 16-08-2018 til 31-08-2018  | 81                  | 6                  |        
| 8/31/2018             | 80                   | 6                     | 16-08-2018 til 31-08-2018  | 75                  | 0                   |

### <a name="weekly-accrual-frequency"></a>Ugentlig periodiseringsfrekvens

| Dato for periodiseringsbonus    | Niveau for antal arbejdstimer    | Periodiseringsbeløb        | Datoer for antal arbejdstimer   | Faktiske antal arbejdstimer| Bonus               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 40                   | 3                     | 27-08-2018 til 31-08-2018  | 42                  | 3                  |        
| 8/31/2018             | 40                   | 3                     | 27-08-2018 til 31-08-2018  | 35                  | 0                   |

### <a name="employee-assigned-leave-plans"></a>Medarbejdertildelte orlovsplaner

I medarbejderens tildelte orlovsplaner er niveaugrundlaget og typen af timer vist for planer med arbejdstimer. For aktive planer vises også de faktiske arbejdstimer for periodiseringsperioder pr. dags dato.

### <a name="loading-data"></a>Indlæser data

Faktiske timer kan importeres ved hjælp af objektet **Antal brugte timer til orlov og fravær** i datastyringen. Hvis du bruger arbejdstidskalendere, vil importen validere, at de normale arbejdstimer ikke overskrider de planlagte timer i på en dag, der er defineret af kalenderen. Importen validerer også, at antal arbejdstimer for en given dag ikke overstiger 24. 

Følgende oplysninger skal bruges til at importere de faktiske timer, der skal bruges i processen til periodisering af orlov:

- Personalenummer 
- Dato for arbejdsdag
- Type
- Timer

En enkelt dato kan kun have én af hver type tilknyttet.

| Personalenummer       | Dato for arbejdsdag           | Type                  | Timer                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 8/6/2018             | Regulær               | 8                    |       
| 000337                | 8/7/2018             | Regulær               | 8                    |
| 000337                | 8/7/2018             | Overtid              | 3                    |
| 000337                | 8/8/2018             | Regulær               | 8                    |
| 000337                | 8/7/2018             | Regulær               | 8                    |
| 000337                | 8/9/2018             | Regulær               | 8                    |

## <a name="enrollments-and-balances"></a>Tilmeldinger og saldi

### <a name="enrollment-date"></a>Tilmeldingsdato

Tilmeldingsdatoen bestemmer, hvornår medarbejderen kan begynde at periodisere fritid. Hvis medarbejderen f.eks. er tilmeldt en ferieplan den 15. juni 2018, kan vedkommende ikke periodisere fritid før den 15. juni 2018.

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

Periodiseringer behandles den 1.maj 2018 (01-05-2018), så hele perioden er inkluderet.

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

Periodiseringer behandles den 1.maj 2018 (01-05-2018), så hele perioden er inkluderet.

**Resultater**

| Periodiseringsbeløb | Mindste saldo | Maksimumoverførsel | Ønsket beløb | Aktuel saldo (pr. 01-01-2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Aktuel saldo (7) = Periodiseringsbeløb (5 × 3) – Ønsket beløb (8)

### <a name="forecasted-balance"></a>Budgetsaldo

Den *budgetterede saldo* er den samlede orlov på en fremtidig dato. Periodiseringer og regulerede overførsler budgetteres indtil denne dato.

I Human Resources bruges følgende formel:

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
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3.00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1.00           | 9/1/2018        | 2.00    |

## <a name="see-also"></a>Se også

- [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)
- [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md)
- [Periodisere orlovs- og fraværsplaner](hr-leave-and-absence-accrue.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]