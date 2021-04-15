---
title: Løn på basis af registreringer
description: Dette emne forklarer, hvordan løn beregnes baseret på arbejderregistreringer.
author: johanhoffmann
ms.date: 03/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgCalcApproveWeekView, JmgProdStatusListPagePayrollCostDetails, JmgPayCountTable, JmgPayStatConfig, JmgOvertimeSlize, JmgPayAgreementOverride, JmgPayCountSum, JmgPayAdjustSetup, JmgPayAdjustCostType, JmgPayEmployee, JmgMESBreak, JmgPayAddTable, JmgPayAddTransSelectTransId, JmgPayrollCostDetailsPart, jmgProdStatusListPagePayrollCosts, JmgPayrollCostPart, JmgPayEvents, JmgTermRegPayStatSetup, JmgPayStatGroup, JmgPayAddTrans, JmgPayStatTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c511558735e89db32e88f6efdd2d0cc88a04b61c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814820"
---
# <a name="pay-based-on-registrations"></a>Løn på basis af registreringer

[!include [banner](../includes/banner.md)]

Dette emne forklarer detaljeret, hvordan løn beregnes baseret på arbejderregistreringer. Det indeholder eksempler på, hvordan de forskellige kombinationer af opsætningsindstillinger, der er tilgængelige for beregning, påvirker resultatet. Her er nogle af de områder, der behandles:

- Flekstid
- Overtid
- Pauser
- Switch-koder
- Lønposter
- Lønaftaler
- Beregningsparametre i Tid og fremmøde
- Fravær

## <a name="the-use-of-flex-time"></a>Brugen af flekstid

Perioder af flekstid angives i de tidsprofiler, der bruges i Tid og fremmøde. Der er to fleksprofiltyper: **Fleks+** og **Fleks-**. Når en arbejder registrerer tid i en periode med Fleks+, forøges arbejderens flekssaldo med de timer, der blev arbejdet. Arbejderen modtage ikke nogen kompensation for de timer, der blev arbejdet i perioden med Fleks+. Men arbejderen kan tage fri i perioder med Flex- og få kompensation med timerne, fra hans eller hendes flekssaldo. Derfor betragtes fritid i fleksperioderne som fravær af systemet.

## <a name="scenarios-based-on-flex-periods"></a>Scenarier, der er baseret på fleksperioder

De to scenarier, der følger, er baseret på en fleksprofil, der repræsenterer en arbejdsdag. I begge scenarier skal løn beregnes i overensstemmelse med den fleksperiode, hvor arbejderen stempler ind og ud.

### <a name="flex-profile-for-one-workday"></a>Fleksprofil for én arbejdsdag

| Profiltype  | Start    | Afslutning      | Dag     |
|---------------|----------|----------|---------|
| Overtid     | 00:00 | 06:00 | Mandag  |
| Fleks+         | 06:00 | 07:00 | Mandag  |
| Komme      | 07:00 | 07:00 | Mandag  |
| Normaltid | 07:00 | 14:30 | Mandag  |
| Fleks-         | 14:30 | 15:30 | Mandag  |
| Udstempling     | 15:30 | 15:30 | Mandag  |
| Overtid     | 15:30 | 06:00 | Tirsdag |

### <a name="scenario-1-a-worker-registers-clock-in-during-a-flex-period-and-clock-out-during-a-flex--period"></a>Scenarie 1: En arbejder stempler ind under en periode med Fleks + og stempler ud under en periode med Fleks-

Arbejderens registreringer for den pågældende dag ser sådan ud.

| Kladderegistreringstype | Start    | Afslutning      |
|---------------------------|----------|----------|
| Komme                  | 06:30 | 06:30 |
| Produktionsjob            | 06:30 | 14:45 |
| Udstempling                 | 14:45 | 14:45 |

Arbejderens registreringer for dagen er beregnet og overført til betaling på siden **Godkend** side (**Tid og fremmøde** &gt; **Gennemse og godkend** &gt; **Godkend**). Når registreringerne er beregnet, kan resultatet af beregningen ses under fanen **Tider**. 

For at forstå dette scenario, skal du se følgende felter.

| Fleks+ | Fleks- | Tidspunkt | Løntid |
|--------|--------|------|----------|
| 0,50   | 0.75   | 8,25 | 8,50     |

#### <a name="calculation-of-flex"></a>Beregning af Fleks+

I henhold til fleksprofilen er tiden mellem 06:00 og 07:00 en periode med Fleks+. Hvis arbejderen derfor stempler ind 06:30, optjener han 0,5 time. Denne tid føjes til arbejderens flekskonto.

#### <a name="calculation-of-flex-"></a>Beregning af Fleks-

I overensstemmelse med fleksprofilen starter perioden for Fleks- kl. 14:30 og slutter ved kl. 15:30. Hvis arbejderen derfor stempler ud kl. 14:45, registreres de 45 minutter (0,75 time), der er tilbage af perioden med Flex- som løntid, og den samme tid trækkes fra arbejderens flekskonto. De 45 minutter medtages i løntid, fordi arbejderen får løn for de resterende 45 minutter i perioden med Flex-. Hvis arbejderen er fraværende i perioden med Flex-, trækkes de 45 minutter fra hans flekskonto.

#### <a name="calculation-of-time"></a>Beregning af tid

Tid beregnes som tiden mellem indstemplings- og udstemplingstid, det vil sige fra 06:30 til 14:45, hvilket svarer til 8,25 timer.

#### <a name="calculation-of-pay-time"></a>Beregning af løntid

Løntid er den tid, som en arbejder tildeles betaling for. I dette scenario er arbejderen på arbejde i 8,25 timer (**Tid**). Men **løntid** beregnes som 8,50 timer, fordi arbejderen gives løn i perioden med Flex-, efter at han stemplede ud. Løntiden svarer til de planlagte arbejdstimer, fordi tid i perioden med Fleks+ er føjet til arbejderens flekskonto og ikke til løntiden. Fraværstiden i perioden med Flex- opvejes af løntiden og trækkes fra arbejderens flekskonto.

| Tidspunkt              | Registreringstype | Løntid (timer)      |
|-------------------|-------------------|-----------------------|
| 6:30 - 7:00 | Fleks+             | 0                     |
| 7:00 – 14:45 | Normaltid     | 7,75                  |
| 14:45 – 15:30 | Fleks-             | 0,75 (fraværsperiode) |
|                   | Total             | 8,50                  |

### <a name="scenario-2-a-worker-works-during-the-whole-flex--period-and-also-works-overtime"></a>Scenarie 2: En arbejder er på arbejde under hele perioden med Fleks- og har også overtid

Arbejderens registreringer for den pågældende dag ser sådan ud.

| Kladderegistreringstype | Start    | Afslutning      |
|---------------------------|----------|----------|
| Komme                  | 06:30 | 06:30 |
| Produktionsjob            | 06:30 | 17:00 |
| Udstempling                 | 17:00 | 17:00 |

Når du har beregnet kladderegistreringer på siden **Godkend**, kan du se resultatet af beregningen under fanen **Tider**. For at forstå dette scenarie skal du se følgende felter.

| Fleks+ | Fleks- | Tidspunkt  | Løntid | Lønovertid |
|--------|--------|-------|----------|--------------|
| 0,50   | 0,00   | 10,50 | 10.00    | 1.50         |

#### <a name="calculation-of-flex"></a>Beregning af Fleks+

I henhold til fleksprofilen er tiden mellem 06:00 og 07:00 en periode med Fleks+. Hvis arbejderen derfor stempler ind 06:30, optjener hun 0,5 times tid i Fleks+ på sin flekssaldo.

#### <a name="calculation-of-flex-"></a>Beregning af Fleks-

Da arbejderen arbejder i perioden med Flex-, beregnes Fleks- ikke. Fleks- beregnes kun, hvis arbejderen er fraværende i perioden med Fleks-. Hvis arbejderen arbejder i perioden med Flex-, får hun fra et betalingsperspektiv den lønsats, der er defineret for normaltid. Hvis arbejderen er fraværende i perioden med Flex-, trækkes de 45 minutter fra hendes flekskonto.

#### <a name="calculation-of-time"></a>Beregning af tid

Tiden beregnes som tiden mellem indstempling kl. 06:30 og udstempling kl. 17:00 eller til 10,50 timer.

#### <a name="calculation-of-pay-time"></a>Beregning af løntid

I dette scenario er arbejderen på arbejde i 10,50 timer (**Tid**). Men **Løntid** beregnes som 10,00 timer, fordi arbejderen ikke tildeles løn i perioden med Fleks-.

#### <a name="calculation-of-pay-overtime"></a>Beregning af lønovertid

| Tidspunkt               | Registreringstype | Løntid (timer) |
|--------------------|-------------------|------------------|
| 6:30 - 7:00  | Fleks+             | 0                |
| 7:00 – 14:30  | Normaltid     | 7,50             |
| 14:30 – 15:30  | Fleks-             | 1,00             |
| 15:30 – 17:00 | Overtid          | 1.50             |
|                    | Total             | 10.00            |

### <a name="generation-of-pay-items"></a>Generering af lønposter

Arbejderregistreringer for dagen kan overføres fra siden **Godkend**. Under overførselsprocessen genereres lønposter og overførte registreringer. Lønposter repræsenterer en opdeling af løntid i normaltid, overtid, betalt pausetid og så videre.

For at åbne listen over lønposter skal du vælge **Tid og fremmøde** &gt; **Gennemse og godkend** &gt; **Godkend**. Vælg derefter **Forespørgsel** &gt; **Overførte registreringer**.

Lønenheder er grundlaget for arbejderens løn. Du kan generere en fil, der indeholder oplysninger fra lønenheder og overføre filen til et lønsystem.

Som led i overførselsprocessen overføres tid og omkostninger fra produktion og projektaktiviteter til produktions- og projektkladder for at tage højde for forbruget at tid og omkostninger. De overførte registreringer danner grundlag for tids- og kostpris pr. time for produktionsordrer og projekter. Du kan åbne de overførte registreringer ved hjælp af menuen **Forespørgsel** på siden **Godkend**.

I scenarie 2 genereres f.eks. følgende lønposter.

| Løntype     | Lønart | Lønenheder | Kurs  | Totalomkostning |
|---------------|----------|-----------|-------|------------|
| Normaltid | 1201     | 10,0      | 10    | 100        |
| Overtid      | 1301     | 1.50      | 5     | 7,50       |
|               |          |           | Total | 107,50     |

Lønposten for normaltid har en betalingsenhed på 10 timer, der dækker normaltid, flekstid og overtid. Normaltid, flekstid og overtid samles i én lønposten, fordi alle typerne beregnes som normaltid baseret på standardindstillingen på en parameter på siden **Beregningsparametre** (**Tid og fremmøde** &gt; **Konfiguration** &gt; **Beregningsparametre**). Overtiden beregnes ved hjælp af en ekstra sats på 5 oven på normaltiden.

Hvis du vil skelne klart mellem normaltid og overtid, så lønenheder for lønarterne kun dækker den faktiske tid, der er brugt på normaltid og overtid, skal lønenhederne for normaltid beregnes som 8,50, og lønenhederne for overtid skal beregnes som 1,50.

Hvis du vil konfigurere systemet til at skelne klart mellem normaltid og overtid, skal du udelade overtid fra normaltiden. Du skal også ændre opsætningen af lønarten for overtid, så lønsatsen for overarbejde dækker alle betalinger for de timer, der er brugt på overtid.

### <a name="exclude-overtime-from-the-standard-time"></a>Udelade overtid fra normaltiden

På siden **Beregningsparametre** skal du vælge **Overtid** som profilspecifikationstypen og angive indstillingen **Løntid** til **Nej**, som vist her.

| Reg.specifikation | Profilspecifikationstype | Kalkulation   |     | Løngivende         |     |
|--------------------|----------------------------|---------------|-----|--------------|-----|
| Arbejdstid       | Overtid                   | Normaltid | Ja | Løntid     | Nr.  |
|                    |                            | Løntid      | Ja | Lønovertid | Ja |

Når du justerer beregningsparametrene, genereres følgende lønposter.

| Løntype     | Lønart | Lønenheder | Kurs  | Totalomkostning |
|---------------|----------|-----------|-------|------------|
| Normaltid | 1201     | 8,50      | 10    | 85,0       |
| Overtid      | 1301     | 1.50      | september    | 22,50      |
|               |          |           | Total | 107,50     |

> [!NOTE]
> Beregningsparametrene har en anbefalet standardindstilling. Generelt skal du være omhyggelig, når du ændrer disse parametre. For at gendanne de anbefalede standardindstillinger på siden **Beregningsparametre** skal du vælge **Gendan værdier**.

### <a name="allow-a-deviation-from-the-standard-pay-profiles"></a>Tillade en afvigelse fra standardlønprofilerne

På siden **Profiler** (**Tid og fremmøde** &gt; **Konfiguration** &gt; **Tidsprofiler** &gt; **Profiler**), kan du oprette profiltyper, der omfatter Switch-koder og pauser.

### <a name="switch-codes"></a>Switch-koder

Du kan bruge Switch-koder til at tillade arbejdere at afvige fra deres profiltype ved skifte til en anden profiltype. Du kan f.eks. tillade, at en arbejder skifter fra tid på Fleks+ til overtid. En arbejder kan tilføje en Switch-kode under registreringen, eller du kan tildele opgaven med at tilføje en Switch-kode til godkenderen af registreringerne.

Før en Switch-kode kan bruges, skal du angive den som en indirekte aktivitet. Derefter skal du føje Switch-koden til tidsprofilen for den periode, hvor du vil tillade en ændring af profiltype. Følg f.eks. disse trin for at oprette en Switch-kode, der gør det muligt at ændre perioden Fleks+ fra 06:00 til 07:00 AM til overtid.

1. Opret en Switch-kode, der hedder **OTBCI (Konverter fleks til overtid før indstempling)**. Vælg **Tid og fremmøde** &gt; **Administrer indirekte aktiviteter** &gt; **Indirekte aktiviteter**.
2. I kolonnen **Switch-kode** skal du tilføje OTBCI til linjen Fleks+ i tidsprofilen.
3. I kolonnen **Sekundær** skal du tilføje profiltypen **Overtid**.

Overvej følgende fleksprofil, der repræsenterer en arbejdsdag.

| Profiltype  | Start    | Afslutning      | Dag     |
|---------------|----------|----------|---------|
| Overtid     | 00:00 | 06:00 | Mandag  |
| Fleks+         | 06:00 | 07:00 | Mandag  |
| Komme      | 07:00 | 07:00 | Mandag  |
| Normaltid | 07:00 | 14:30 | Mandag  |
| Fleks-         | 14:30 | 15:30 | Mandag  |
| Udstempling     | 15:30 | 15:30 | Mandag  |
| Overtid     | 15:30 | 06:00 | Tirsdag |

Her er arbejderens registreringer for den pågældende dag.

| Kladderegistreringstype | Start    | Afslutning      |
|---------------------------|----------|----------|
| Komme                  | 06:30 | 06:30 |
| Produktionsjob            | 06:30 | 14:45 |
| Udstempling                 | 17:00 | 17:00 |

Der genereres lønposter efter overførslen.

| Løntype     | Lønart | Lønenheder | Kurs  | Totalomkostning |
|---------------|----------|-----------|-------|------------|
| Normaltid | 1201     | 8,50      | 10    | 85,0       |
| Overtid      | 1305     | 1.50      | september    | 22,50      |
|               |          |           | Total | 107,50     |

På siden **Godkend** skal du annullere overførslen og derefter bruge menuen **Switch-kode** til at anvende Switch-koden **OTBCI**. Når du overfører registreringerne endnu en gang, genereres følgende lønposter.

| Løntype     | Lønart | Lønenheder | Kurs  | Totalomkostning |
|---------------|----------|-----------|-------|------------|
| Normaltid | 1201     | 8,50      | 10    | 80,0       |
| Overtid      | 1305     | 2.00      | september    | 30,0       |
|               |          |           | Total | 107,50     |

> [!NOTE]
> Når du anvender Switch-koden, forøges overtid med 0,5 time fra 1,50 til 2,00. 0,5 time er konverteringen af tiden på Fleks+, der er registreret, fra 6:30 til 07:00 til overtid.

### <a name="breaks"></a>Pauser

Pauser fra arbejdet påvirker beregningen af lønnen for arbejderen. Pauser defineres som en type af indirekte aktivitet. De kan defineres som enten **Betalt**, for at tillade at pausen føjes til arbejderens løn, eller **Ubetalt**, for at forhindre at pausen føjes til arbejderens løn. En pause kan også være defineret som enten **Planlagt** eller **Registreret**.

#### <a name="planned-breaks"></a>Planlagte pauser

Hvis en virksomhed har en fast pausetid, f.eks. en fast frokostpause, kan pausen være foruddefineret i tidsprofilen. I dette tilfælde behøver arbejderen ikke at registrere pausen på jobkortsiderne. I stedet tages pausen automatisk i betragtning, når arbejderens registreringer beregnes fra siden **Godkend**.

#### <a name="registered-breaks"></a>Registrerede pauser

Hvis en virksomhed ikke bruger planlagte pauser, kan medarbejderne registrere pauser i løbet af arbejdsdagen. Registrerede pauser kan bruges, f.eks. hvis en arbejder anvender en flekstidsprofil, der ikke har defineret komme og gå-tider. Registrerede pauser er en type af indirekte aktivitet. Arbejderen registrerer pausen på terminalsiden **Jobkort** eller på enhedssiden **Jobkort**. På begge disse sider kan brugeren vælge typen af pause på en liste over foruddefinerede pauseaktiviteter.

#### <a name="paid-and-unpaid-breaks"></a>Betalte og ubetalte pauser

Pauseaktiviteter kan sættes op som **Betalt** eller **Ubetalt**. En betalt pause medtages i beregningen af løntid, og systemet bruger den lønart, der er defineret i lønaftalen for registreringstypen **Pause**.

### <a name="example-of-a-planned-break"></a>Eksempel på en planlagt pause

Se på følgende arbejdstidsprofil, der indeholder en ubetalte pause til frokost.

| Profiltype  | Start    | Afslutning      | Dag     |
|---------------|----------|----------|---------|
| Overtid     | 00:00 | 06:00 | Mandag  |
| Fleks+         | 06:00 | 07:00 | Mandag  |
| Komme      | 07:00 | 07:00 | Mandag  |
| Normaltid | 07:00 | 12:00 | Mandag  |
| Pause         | 12:00 | 12:30 | Mandag  |
| Normaltid | 12:30 | 14:30 | Mandag  |
| Fleks-         | 14:30 | 15:30 | Mandag  |
| Udstempling     | 15:30 | 15:30 | Mandag  |
| Overtid     | 15:30 | 06:00 | Tirsdag |

Her er arbejderens registreringer for den pågældende dag.

| Kladderegistreringstype | Start    | Afslutning      |
|---------------------------|----------|----------|
| Komme                  | 06:30 | 06:30 |
| Produktionsjob            | 06:30 | 14:45 |
| Udstempling                 | 17:00 | 17:00 |

Når du har beregnet kladderegistreringer på siden **Godkend**, kan du se resultatet af beregningen under fanen **Tider**. For at forstå dette scenarie skal du se følgende felter.

| Fleks+ | Fleks- | Tidspunkt  | Løntid | Ikke-løngivende pausetid | Lønovertid |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 | 9,50     | 0,5                 | 1.50         |

> [!NOTE] 
> Systemet beregnede 0,5 time ubetalte pausetid og tiden er ikke en del af løntiden.

### <a name="example-of-a-registered-break"></a>Eksempel på en registreret pause

Se på følgende arbejdstidsprofil, der ikke indeholder planlagte pauser.

| Profiltype  | Start    | Afslutning      | Dag     |
|---------------|----------|----------|---------|
| Overtid     | 00:00 | 06:00 | Mandag  |
| Fleks+         | 06:00 | 07:00 | Mandag  |
| Komme      | 07:00 | 07:00 | Mandag  |
| Normaltid | 07:00 | 14:30 | Mandag  |
| Fleks-         | 14:30 | 15:30 | Mandag  |
| Udstempling     | 15:30 | 15:30 | Mandag  |
| Overtid     | 15:30 | 06:00 | Tirsdag |

Her er arbejderens registreringer for den pågældende dag.

| Kladderegistreringstype | Start    | Afslutning      |
|---------------------------|----------|----------|
| Komme                  | 06:30 | 06:30 |
| Produktionsjob            | 06:30 | 17:00 |
| Pause                     | 12:03 | 12:32 |
| Udstempling                 | 17:00 | 17:00 |

Når registreringerne beregnes, beregnes tiden for aktiviteterne.

| Kladderegistreringstype | Start    | Afslutning      | Tidspunkt  |
|---------------------------|----------|----------|-------|
| Komme                  | 06:30 | 06:30 |       |
| Produktionsjob            | 06:30 | 17:00 | 10.00 |
| Pause                     | 12:03 | 12:32 | 0,50  |
| Udstempling                 | 17:00 | 17:00 |       |

> [!NOTE]
> Tiden for pausen køres parallelt med tiden for aktiviteten (et produktionsjob, i dette eksempel). Denne funktionsmåde bruges altid til pauseaktiviteter. Når registreringerne beregnes, trækkes pausetiden fra aktivitetstiden. I dette tilfælde har produktionsjobbet en varighed på 10,50 timer, men tiden beregnes som 10, fordi der er trukket 0,5 times pausetid fra aktivitetstiden.

Når du har beregnet kladderegistreringer på siden **Godkend**, kan du se resultatet af beregningen under fanen **Tider**. For at forstå dette scenarie skal du se følgende felter.

| Fleks+ | Fleks- | Tidspunkt  | Løntid | Ikke-løngivende pausetid | Lønovertid |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 | 9,50     | 0,5                 | 1.50         |

Hvis den planlagte pause havde været betalt i stedet for ubetalte, ville resultatet af beregningen se ud som følger.

| Fleks+ | Fleks- | Tidspunkt  | Løntid | Løngivende pausetid | Lønovertid |
|--------|--------|-------|----------|-----------------|--------------|
| 0,50   | 0,00   | 10,50 | 10.00    | 0,5             | 1.50         |

### <a name="pay-items-and-paid-breaks"></a>Lønposter og betalte pauser

Når du overfører registreringer på siden **Godkend**, oprettes der lønposter. Der oprettes en separat lønpost for betalte pauser.

Lønsatsen for en betalt pause bestemmes af den lønart, der er angivet i lønaftalerne for pausen. I stedet for at bruge en lønart, kan du angive kostprisen pr. time for pausen i et defineret datointerval.

Se på følgende tidsprofil.

| Profiltype  | Start    | Afslutning      | Dag     |
|---------------|----------|----------|---------|
| Overtid     | 00:00 | 06:00 | Mandag  |
| Fleks+         | 06:00 | 07:00 | Mandag  |
| Komme      | 07:00 | 07:00 | Mandag  |
| Normaltid | 07:00 | 14:30 | Mandag  |
| Fleks-         | 14:30 | 15:30 | Mandag  |
| Udstempling     | 15:30 | 15:30 | Mandag  |
| Overtid     | 15:30 | 06:00 | Tirsdag |

Her er arbejderens registreringer for den pågældende dag.

| Kladderegistreringstype | Start    | Afslutning      | Tidspunkt |
|---------------------------|----------|----------|------|
| Komme                  | 07:00 | 07:00 |      |
| Produktionsjob            | 07:00 | 15:00 | 7,5  |
| Pause (betalt)              | 12:00 | 12:30 | 0,5  |
| Udstempling                 | 15:00 | 15:00 |      |

I dette eksempel er lønarten for normaltid angivet til **1201**, og der er angivet en lønsats på **10** i lønaftalen. Den betalte pause har en lønart på **1301** og en lønsats på **8**. Når registreringerne overføres, genereres følgende lønposter.

| Løntype     | Lønart | Lønenheder | Kurs |
|---------------|----------|-----------|------|
| Normaltid | 1201     | 7,50      | 10   |
| Fleks-         | 1201     | 0,50      | 10   |
| Pause (betalt)  | 1301     | 0,50      | 8    |

## <a name="how-the-cost-of-paid-breaks-is-allocated-to-projects-and-production-orders"></a>Sådan allokeres omkostningerne for betalte pauser til projekter og produktionsordrer

Timeomkostningerne på projektaktiviteter og produktionsjob kan konfigureres, så de bestemmes enten ved lønsatser, der er beregnet i Tid og fremmøde, eller ved de omkostningsarter, der er defineret for aktiviteterne.

For at konfigurere omkostningskategorien skal du vælge **Produktionsstyring** &gt; **Konfiguration** &gt; **Produktionsudførelse** &gt; **Produktionsordrestandarder** og angive feltet **Omkostningsart** til enten **Ja** eller **Nej**.

- **Nej** – Omkostninger beregnes på grundlag af lønsatser, der er defineret for registreringstyper i Tid og fremmøde.
- **Ja** – Omkostninger beregnes ud fra omkostningskategorier for produktions- og projektaktiviteter.

### <a name="cost-calculation-based-on-pay-rates-that-are-calculated-in-time-and-attendance"></a>Omkostningsberegning baseret på lønsatser, der er beregnet i Tid og fremmøde

Følgende eksempel viser, hvordan de timemæssige omkostninger beregnes, når omkostningerne er konfigureret, så de beregnes ud fra lønsatser.

Omkostningssatsen pr. time, der bruges til produktionsordrer og projekter, beregnes under overførselsprocessen. For at få vist timesatsen pr. aktivitet, skal du åbne siden **Godkend** i Tid og fremmøde og derefter vælge **Forespørgsel** &gt; **Overførte registreringer**. Du kan finde omkostningssatsen pr. time pr. registrering under fanen **Kostpriser**.

Se på følgende tilmeldinger, der bruger den samme tidsprofil som det foregående eksempel.

| Kladderegistreringstype | Start    | Afslutning      | Tidspunkt |
|---------------------------|----------|----------|------|
| Komme                  | 07:00 | 07:00 |      |
| Proces (Order: 4711)     | 07:00 | 11:00 | 4    |
| Proces (Order: 4712)     | 11:00 | 15:00 | 3,50 |
| Pause (betalt)              | 12:00 | 12:30 | 0,50 |
| Udstempling                 | 15:00 | 15:00 |      |

Når registreringerne er overført, genereres følgende overførte registreringer.

| Registreringstype     | Tidspunkt | Kostpris pr. time |
|-----------------------|------|---------------------|
| Komme              | 0,00 | 0,00                |
| Proces (Order: 4711) | 4,00 | 10.00               |
| Proces (Order: 4712) | 3,50 | 11,14               |
| Pause (betalt)          | 0,50 | 0,00                |
| Udstempling             | 0,00 | 0,00                |

Beregningen af kostpris pr. time for den betalte pause afhænger af en indstilling for de direkte lønudgifter. Vælg **Tid og fremmøde** &gt; **Konfiguration** &gt; **Parametre for tid og fremmøde**. Under fanen **Kostpris** under **Direkte lønudgifter** i feltet **Normaltid** kan du vælge **Ja**, **Nej** eller **Fordeling**.

- **Ja** – Denne værdi bruges til det foregående eksempel. Omkostningerne fordeles til den produktions- eller projektaktiviteten, der kører parallelt med aktiviteten betalt pause. I eksemplet er denne aktivitet produktionsjobbet til ordre 4712. Kostprisen pr. time for det betalte pause er 0 (nul), som du kan se, og tildeles til det job, der kører parallelt med pausen.

    Den betalte pause har en varighed på 0,5 time, og lønsatsen er 8. Derfor er de samlede omkostninger for den betalte pause 4. De samlede omkostninger fordeles derefter til procesjobbet på 3,5 timer. Derfor bidrager den betalte pause med 1,14 pr. time til omkostningerne (4 ÷ 3,5 = 1,14).

- **Fordeling** – Den betalte pause fordeles jævnt på de job, der er registreret for den pågældende dag. Hvis denne værdi bruges til det foregående eksempel, genereres følgende overførte registreringer.

    | Registreringstype     | Tidspunkt | Kostpris pr. time |
    |-----------------------|------|---------------------|
    | Komme              | 0,00 | 0,00                |
    | Proces (Order: 4711) | 4,00 | 10,53               |
    | Proces (Order: 4712) | 3,50 | 10,53               |
    | Pause (betalt)          | 0,50 | 0,00                |
    | Udstempling             | 0,00 | 0,00                |

    Den samlede procestid for de to produktionsjob er 7,5 timer, og de samlede omkostninger for den betalte pause er 4. Derfor er pausens omkostninger beregnet som 0,53 (= 4 ÷ 7,5).

- **Nej** – Omkostningerne for den betalte pause øger ikke timesatsen for procesaktiviteterne.

    | Registreringstype     | Tidspunkt | Kostpris pr. time |
    |-----------------------|------|---------------------|
    | Komme              | 0,00 | 0,00                |
    | Proces (Order: 4711) | 4,00 | 10.00               |
    | Proces (Order: 4712) | 3,50 | 10.00               |
    | Pause (betalt)          | 0,50 | 0,00                |
    | Udstempling             | 0,00 | 0,00                |

## <a name="absence"></a>Fravær

En fraværskode bruges til at registrere tidsrummet for en arbejders fravær. På samme måde som pauser og Switch-koder er en fraværskode en slags en indirekte aktivitet. Fraværstid kan enten være planlagt eller registreret, og fravær kan enten være gyldigt eller ugyldigt. En aftale hos lægen, et seminar eller indkaldelse som domsmand er eksempler på gyldigt fravær. Ugyldigt fravær er fravær uden god begrundelse, f.eks. når en arbejder kommer for sent på arbejde. Normalt medføre gyldigt fravær ikke et fradrag i arbejderens løn, mens ugyldigt fravær forårsager et fradrag.

### <a name="planned-absence"></a>Planlagt fravær

Du kan oprette planlagt fravær for arbejdere på siden **Opret planlagt fravær** (**Tid og fremmøde** &gt; **Opret planlagt fravær**). Der registreres det planlagte fravær som et fraværsjob for en bestemt dato og et bestemt tidsinterval.

Jobbet er baseret på en forespørgsel. Du kan derfor oprette planlagt fravær for flere arbejdere, f.eks. arbejdere, der tilhører den samme beregningsgruppe. Hvis der er planlagt fravær for en enkelt arbejder, kan du angive registreringen enten fra siden **Fremmøde** eller siden **Tidsregistrering arbejdere** side.

- Hvis du vil angive en fraværsregistrering fra siden **Fremmøde** skal du vælge **Tid og fremmøde** &gt; **Forespørgsler og rapporter** &gt; **Fremmøde** &gt; **Fremmøde** og derefter vælge **Fraværsregistrering**.
- Hvis du vil angive en fraværsregistrering fra siden *<strong><em>Tidsregistreringsarbejder</em></strong>*, skal du vælge <strong>Tid og fremmøde</strong> &gt; <strong>Opsætning</strong> &gt; <strong>Tidsregistreringsarbejder</strong> og derefter på fanen <strong>Tid</strong> under <strong>Tidstildeling</strong> vælge <strong>Fraværsregistreringer</strong>.

Du kan bruge rapporten **Planlagt fravær** til at få vist en oversigt over planlagt fravær for arbejdere. Hvis du vil åbne rapporten, skal du vælge **Tid og fremmøde** &gt; **Forespørgsler og rapporter** &gt; **Fraværsrapporter** &gt; **Planlagt fravær**.

### <a name="registered-absence"></a>Registreret fravær

Generelt betragtes arbejdere som fraværende, hvis de ikke er på arbejde i en periode mellem deres planlagte komme-tid og deres planlagte gå-tid. Hvis arbejdere kommer senere end planlagt, eller hvis de går tidligere end planlagt, bliver de bedt om at vælge en fraværskode for at angive årsagen til fraværet. Der kan konfigureres en fraværskode, så den kan anvendes til registrering. Det er kun de relevante koder, der kan vælges på listen.

## <a name="scenarios-based-on-various-combinations-of-work-hour-registrations"></a>Scenarier, der er baseret på forskellige kombinationer af arbejdstimeregistreringer

Scenarierne nedenfor viser de lønenheder og poster til godkendelse, der genereres for arbejdere på basis af deres registreringer. Alle scenarierne er baseret på følgende tidsprofil.

| Profiltype  | Start    | Afslutning      | Dag     |
|---------------|----------|----------|---------|
| Overtid     | 00:00 | 06:00 | Mandag  |
| Fleks+         | 06:00 | 07:00 | Mandag  |
| Komme      | 07:00 | 07:00 | Mandag  |
| Normaltid | 07:00 | 14:30 | Mandag  |
| Fleks-         | 14:30 | 15:30 | Mandag  |
| Udstempling     | 15:30 | 15:30 | Mandag  |
| Overtid     | 15:30 | 06:00 | Tirsdag |

### <a name="scenario-1-the-worker-clocks-in-later-than-planned"></a>Scenarie 1: Arbejderen stempler ind senere end planlagt

Arbejderen stempler ind kl. 08:30. Da hans planlagte komme-tid er 07:00, kommer han 1,50 time for sent på arbejde. Da de 1,50 time betragtes som fraværstid, bliver arbejderen bedt om at vælge en fraværskode. Arbejderen forlader arbejdet kl. 15:30 , som er det planlagte gå-tidspunkt. Når arbejderens registreringer beregnes og godkendes, vises fraværsregistreringen sammen med den fraværskode, som arbejderen har valgt ved komme-registreringen, for tidsintervallet mellem 07:00 og 08:30.

I tidsprofilen kan du konfigurere registreringstypen **Komme**, så der er en tolerance, når arbejdere kommer for sent på arbejde. Hvis du f.eks. opretter en tolerance på 5, bliver arbejderen kun bedt om at angive en fraværskode, hvis han kommer senere end 07:05.

Fordi arbejderen i dette tilfælde ikke har en god grund til at komme for sent på arbejde, vælger han en fraværskode, der er defineret for ulovligt fravær. En fraværskode anses for egnet til ulovligt fravær, hvis indstillingen for overtidsfradrag er aktiveret for den fraværsgruppe, som fraværskoden hører til. Hvis du vil angive indstillingen, skal du vælge **Tid og fremmøde** &gt; **Konfiguration** &gt; **Grupper** &gt; **Fraværsgrupper** og derefter vælge afkrydsningsfeltet **Modregn overtid**.

Sådan ser arbejderens registreringer for dagen ud på siden **Godkend** efter beregningen.

| Kladderegistreringstype         | Start    | Afslutning      | Tidspunkt |
|-----------------------------------|----------|----------|------|
| Fravær (ugyldigt - for sent på arbejde) | 07:00 | 08:30 | 1.5  |
| Komme                          | 08:30 | 08:30 |      |
| Produktionsjob                    | 07:30 | 15:30 | 7.0  |
| Udstempling                         | 15:30 | 15:30 |      |

Her er den resulterende lønpost, når registreringerne er overført.

| Løntype     | Lønart | Lønenheder | Kurs |
|---------------|----------|-----------|------|
| Normaltid | 1201     | 7:00      | 10   |

### <a name="scenario-2-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-standard-time-period"></a>Scenarie 2: Arbejderen stempler ud før den planlagte gå-tid i en standardtidsperiode

Arbejderen stempler ind kl. 07:00 og stempler tidligt ud kl. 13.00. Da 13:00 ligger før det planlagte gå-tidspunkt kl. 15:30, og 13:00 er i en standardtidsperiode, bliver arbejderen bedt om at vælge en fraværskode. Arbejderen vælger en fraværskode for aftale hos en læge, der er defineret som gyldigt fravær. Lønsatsen for gyldigt fravær er defineret i lønaftalerne for registreringstypen **Fravær** (**Tid og fremmøde** &gt; **Konfiguration** &gt; **Løn** &gt; **Lønaftaler**).

Sådan ser arbejderens registreringer for dagen ud på siden **Godkend** efter beregningen.

| Kladderegistreringstype              | Start    | Afslutning      | Tidspunkt |
|----------------------------------------|----------|----------|------|
| Komme                               | 07:00 | 07:00 |      |
| Produktionsjob                         | 07:00 | 13:00 | 4.0  |
| Udstempling                              | 13:00 | 13:00 |      |
| Fravær (gyldigt – aftale hos læge) | 13:00 | 15:30 | 3.5  |

Her er den resulterende lønpost, når registreringerne er overført.

| Løntype     | Lønart | Lønenheder | Kurs |
|---------------|----------|-----------|------|
| Normaltid | 1201     | 7,50      | 10   |

### <a name="scenario-3-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-flex--period"></a>Scenarie 3: Arbejderen stempler ud før den planlagte gå-tid i en periode med Fleks-

Arbejderen stempler ind kl. 07:00 og stempler ud kl. 14:15, hvilket er i den planlagte periode for Fleks-. Tiden mellem den faktiske gå-tid og den planlagte gå-tid betragtes ikke som fravær, og arbejderen bliver ikke bedt om at vælge en fraværskode. Beløbet trækkes fra arbejderens flekskonto, og arbejderen tildeles løn i den resterende del af perioden for Fleks-, fra 14:15 til 15:30.

Sådan ser arbejderens registreringer for dagen ud på siden **Godkend** efter beregningen.

| Kladderegistreringstype | Start    | Afslutning      | Tidspunkt |
|---------------------------|----------|----------|------|
| Komme                  | 07:00 | 07:00 |      |
| Produktionsjob            | 07:00 | 14:15 | 7,25 |
| Udstempling                 | 14:15 | 14:15 |      |

Her er den resulterende lønpost, når registreringerne er overført.

| Løntype     | Lønart | Lønenheder | Kurs |
|---------------|----------|-----------|------|
| Normaltid | 1201     | 8,50      | 10   |

### <a name="scenario-4-the-worker-clocks-in-late-and-clocks-out-after-the-planned-clock-out-time-during-an-overtime-period"></a>Scenarie 4: Arbejderen stempler for sent ind og stempler ud efter den planlagte gå-tid i en overtidsperiode

Arbejderen stempler ind for sent kl. 09:30, og for at kompensere for sit sene fremmøde arbejder han derefter over og stempler ud kl. 17:00. Fordi arbejderen kom for sent og kompenserede ved at arbejde længere, vil firmaet ikke tildele arbejderen overtidsbetaling for de timer, han har arbejdet mellem det planlagte gå-tidspunkt kl. 15:30 PM og det faktiske gå-tidspunkt kl. 17:00, selvom denne periode er defineret som overtid i arbejdstidsprofilen.

For at håndtere dette scenarie skal fraværskoden konfigureres til at reducere overtidstimer med eventuelle timer fra ulovligt fravær, som arbejderen har samme dag. Vælg **Tid og fremmøde** &gt; **Konfiguration** &gt; **Grupper** &gt; **Fraværsgrupper** og derefter vælge afkrydsningsfeltet **Modregn overtid** for at modregne overtid i timer for ulovligt fravær.

Sådan ser arbejderens registreringer for dagen ud på siden **Godkend** efter beregningen.

| Kladderegistreringstype         | Start    | Afslutning      | Tidspunkt |
|-----------------------------------|----------|----------|------|
| Fravær (ugyldigt - for sent på arbejde) | 07:00 | 09:30 | 1.5  |
| Komme                          | 09:30 | 09:30 |      |
| Produktionsjob                    | 09:30 | 17:00 | 7,5  |
| Udstempling                         | 17:30 | 17:30 |      |

Hvis afkrydsningsfeltet **Modregn overtid** er markeret for den valgte fraværskode, fratrækkes de timer, hvor arbejderen var fraværende ulovligt, fra overtidsbetalingen. I dette tilfælde genereres følgende lønposter, når registreringerne er overført.

| Løntype     | Lønart | Lønenheder | Kurs |
|---------------|----------|-----------|------|
| Normaltid | 1201     | 9,00      | 10   |
| Overtid      | 1301     | 0,5       | september   |

Her modregnes de 1,5 times ulovligt fravær fra 07:00 til 09:30 i de 2,0 timers overarbejde fra 15:30 til 17:30. Resultatet af registreringen er 1,5 times normaltid og 0,5 times overarbejde.

Hvis afkrydsningsfeltet **Modregn overtid** derimod ikke er markeret for den valgte fraværskode, tildeles arbejderen overtidsbetaling, selvom han kom for sent og havde et ugyldigt fravær. I dette tilfælde genereres følgende lønposter, når registreringerne er overført.

| Løntype     | Lønart | Lønenheder | Kurs |
|---------------|----------|-----------|------|
| Normaltid | 1201     | 7,50      | 10   |
| Overtid      | 1301     | 2,0       | september   |

### <a name="scenario-5-the-worker-clocks-out-before-the-planned-clock-out-time-and-can-convert-the-absence-period-to-a-flex--period"></a>Scenarie 5: Arbejderen stempler ud før den planlagte gå-tid og kan konvertere fraværdsperioden til en perioden med Fleks-

Følgende eksempel viser, hvordan en arbejders flekskonto kan reduceres ved at konvertere fraværsperioden til en periode i Fleks-.

Arbejderen stempler ind kl. 7.00 og stempler ud på kl. 13.00. Hun har fået en aftale med sin overordnede om, at hun kan gå hjem til weekenden, hvis hun fratrækker disse timer fra sin flekskonto. Når arbejderen stempler ud kl. 13:00, bliver hun bedt om at vælge en fraværskode, fordi perioden med fravær i den resterende del af den arbejdsdag, der er påvirket, ikke er i en planlagt periode med Fleks-. For at konvertere den resterende del af en arbejdsdag til en periode med Fleks-, kan arbejderen vælge en fraværskode, der er konfigureret til at reducere hendes flekskonto.

For at reducere saldoen for flekstimer for arbejdere, der registrerer fravær på en arbejdsdag, skal du vælge **Tid og fremmøde** &gt; **Konfiguration** &gt; **Grupper** &gt; **Fraværsgrupper** og markere afkrydsningsfeltet **Reducer fleks**.

Sådan ser arbejderens registreringer for dagen ud på siden **Godkend** før beregningen.

| Kladderegistreringstype | Start    | Afslutning      | Tidspunkt |
|---------------------------|----------|----------|------|
| Komme                  | 07:00 | 07:00 |      |
| Produktionsjob            | 07:00 | 13:00 | 6,0  |
| Udstempling                 | 13:00 | 13:00 |      |

Hvis medarbejderen vælger en fraværskode for ulovligt fravær, vil den resulterende lønpost se sådan ud, når registreringen er overført.

| Løntype     | Lønart | Lønenheder | Kurs |
|---------------|----------|-----------|------|
| Normaltid | 1201     | 6,00      | 10   |

Hvis medarbejderen vælger en fraværskode for gyldigt fravær, og fraværskoden er konfigureret til at reducere hendes flekskonto, ser de resulterende lønenheder sådan ud, når registreringerne er overført.

| Løntype     | Lønart | Lønenheder | Kurs |
|---------------|----------|-----------|------|
| Normaltid | 1201     | 8,50      | 10   |

I så fald reduceres arbejderens flekssaldo med timerne mellem den faktiske gå-tid og den planlagte gå-tid (dvs. 2,5 timer fra 13:00 til 15:30).

> [!NOTE]
> Vi anbefaler ikke, at du markerer både afkrydsningsfeltet **Fratræk fleks** og afkrydsningsfeltet **Modregn overtid** for en fraværskode, fordi denne konfiguration vil fratrække de ugyldige timer fra arbejderens overtidstimer og samtidig reducere arbejderens flekskonto.

### <a name="scenario-6-there-is-no-planned-absence-for-the-day-and-no-worker-attendance-for-the-day"></a>Scenarie 6: Der er ikke planlagt fravær for dagen, og der er intet arbejderfremmøde for dagen

Hvis arbejderen ikke møder på arbejde på en arbejdsdag, og der er ikke planlagt fravær for arbejderen på denne dag, bruges en standardfraværskode til beregning af arbejderens registreringer. For at definere standardfraværskoder skal du vælge **Tid og fremmøde** &gt; **Parametre for tid og fremmøde**. Du kan derefter vælge en fraværskode i følgende felter:

- Automatisk indsættelse af fleks-
- Automatisk indsættelse af fravær

Når de daglige registreringer beregnes for en arbejder, der er aktiveret til flekstimer, bruges den fraværskode, der er angivet i feltet **Automatisk indsættelse af fleks-**, som en standardfraværskode. Hvis arbejderen ikke er aktiveret til flekstimer, bruges den fraværskode, der er angivet i feltet **Automatisk indsættelse af fravær**. Hvis en virksomhed har en kombination af arbejdere, der er aktiveret til flekstimer, og arbejdere, der ikke er aktiveret til flekstid, skal begge parametre konfigureres.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]