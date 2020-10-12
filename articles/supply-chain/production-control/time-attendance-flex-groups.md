---
title: Fleksgrupper
description: Dette emne beskriver, hvordan fleksgrupper bruges i forbindelse med tid og fremmøde.
author: johanhoffmann
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgFlexGroup, JmgFlexCorrection
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c71ebab0788b6c5d7466a5d71e3c72a7e86e41db
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826497"
---
# <a name="flex-groups"></a>Fleksgrupper

[!include[banner](../includes/banner.md)]

Med fleksibel arbejdstid kan virksomheder minimere betalinger for overtid ved at tilbyde arbejdere ekstra fridage i de perioder, hvor arbejdsbelastningen er lav. Denne funktion er relevant f.eks. inden for områder med sæsonbetingede ændringer i arbejdsbyrden.

Du kan bruge fleksgrupper til at angive følgende regler og principper for en arbejders flekstimer:

- Regler for fleksreguleringer
- Princip for beregning af arbejderens flekssaldo

## <a name="set-up-flexible-working-hours-in-flex-groups"></a>Opsætning af fleksible arbejdstider i fleksgrupper

- Vælg **Tid og fremmøde** \> **Opsætning** \> **Grupper** \> **Fleksgrupper**for at oprette fleksgrupper for flekstimer.

## <a name="associate-workers-with-flex-groups"></a>Tilknyt arbejdere til fleksgrupper

- Vælg **Tid og fremmøde** \> **Opsætning** \> **Arbejdere, der registrerer tid**.

## <a name="rules-for-flex-regulations"></a>Regler for fleksreguleringer

Du kan bruge regler for beregning af flekssaldo til at definere flexgrænser eller det mindste og største antal timer, der er tilladt på arbejderens flekskonto. Fleksgrænserne angives for fleksgruppen. Hvis fleksgrænserne overskrides, kan en arbejders flekssaldo og lønnen reguleres.

Hvis en arbejders tilladte minimum for flekstid overskrides (dvs. antallet timer på flekskontoen er mindre end det angivne minimum), kan du bruge disse metoder til at justere arbejderens flekssaldo ved at foretage en fleksregulering:

- Arbejderens flekskonto kan justeres til det angivne tilladte minimum, uden at fratrække arbejderens løn for det antal af timer, som flekskontoen ligger under end det tilladte minimum.
- Arbejderens løn kan fratrækkes det antal timer, som flekskontoen ligger under det tilladte minimum. Dette fradrag foretages ved at generere lønenheder for en bestemt lønart, der har en negativ eller positiv lønenhed.

Hvis arbejderens tilladte fleksmaksimum overskrides, kan du bruge disse metoder til at justere arbejderens flekssaldo ved at foretage en fleksregulering:

- Arbejderens flekskonto kan reguleres tilbage til det angivne tilladte maksimum uden at kompensere arbejderens løn for det antal af timer, som arbejderen har arbejdet over det tilladte maksimum.
- Det antal timer, som arbejderen har arbejdet over det tilladte maksimum, kan konverteres til løn. Denne konvertering sker ved at generere lønenheder for en bestemt lønart.

Du kan regulere en flekssaldo på følgende tidspunkter:

- Når en betalingsfil, der er baseret på løndata, eksporteres ved hjælp af jobbet **Overfør løn**. Løndataene genereres, når du overfører arbejderens registrering fra siden **Godkend**.
- Når jobbet **Reguler flekssaldo** behandles.

> [!NOTE]
> Fleksreguleringer foretages ikke i den daglige godkendelse og overførsel af arbejderens registreringer på siden **Godkend**.

## <a name="principle-for-calculating-a-workers-flex-balance"></a>Princip for beregning af en arbejders flekssaldo

Princippet for beregning af er de timer, som arbejderens flekssaldo reguleres med, konfigureres for fleksgruppen. Vælg **Tid og fremmøde** \> **Opsætning** \> **Grupper** \> **Fleksgrupper**. 

Følgende to principper kan anvendes:

- **Tid** – Arbejderens flekstimer beregnes kun ud fra arbejderens registrerede tid for dagen. Når arbejderens daglige registreringer beregnes, beregnes antallet af positive og negative flekstimer for dagen ud fra de zoner for Fleks+ og Fleks-, som er defineret i arbejderens arbejdstidsprofil.
- **Lønarter** – Arbejderens flekstimer beregnes ud fra indtægter for lønarterne Fleks + og Fleks-, der er defineret i arbejderens lønaftale. Lønaftalen er tilknyttet den arbejder, der registrerer tid. Du vil muligvis bruge lønarter til at administrere flekskonti, hvis du f.eks. vil øge en arbejders flekskonto med en bestemt faktor i en eller flere flekszoner.

### <a name="scenario-1-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-minimum-is-exceeded"></a>Eksempel 1: Regulering af en arbejders løn og flekskonto, fordi det tilladte minimum for flekssaldoen er overskredet.

En arbejder, der har fleksibel arbejdstid, har en negativ flekskonto.

- **Flekskonto:** -4

Arbejderen er tilknyttet en fleksgruppe med følgende konfiguration:

- **Fleksminimum:** -0,5
- **Minimum for lønart:** 1302
- **Faktor for lønart:** -1,00

Som forskellen mellem arbejderens flekskonto og hans tilladte fleksminimum angiver, har arbejderen overskredet sit tilladte fleksminimum med 3,5 timer.

Når lønadministratoren overfører arbejderens løndata ved at køre jobbet **Overfør til løn** eller **Fleksregulering**, foretages følgende justeringer:

- Arbejderens flekskonto reguleres med 3,5 timer. Derfor bliver flekssaldoen på -4,0 reguleret til arbejderens tilladte fleksminimum på -0,5 timer.
- Der oprettes en lønpost for lønarten 1302. Denne lønpost har en lønenhed på -3,5 timer, der trækkes fra arbejderens løn. I så fald er lønenheden et negativt tal, da den positive regulering af timer på 3,5 ganges med den negative løntypefaktor på -1,0, der er defineret for fleksgruppen. Denne lønenhed skal være en del af den lønfil, der genereres af jobbet **Overfør til løn**.

### <a name="scenario-2-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-maximum-is-exceeded"></a>Scenarie 2: Regulering af en arbejders løn og flekskonto, fordi det tilladte maksimum for flekssaldoen er overskredet.

En arbejder, der har fleksibel arbejdstid, har en positiv flekskonto.

- **Flekskonto:** 6

Arbejderen er tilknyttet en fleksgruppe med følgende konfiguration:

- **Fleksmaksimum:** 2,0
- **Minimum for lønart:** 1302
- **Faktor for lønart:** -1,0

Som forskellen mellem arbejderens flekskonto og hendes tilladte fleksmaksimum angiver, har arbejderen overskredet sit tilladte fleksmaksimum med 4,0 timer.

Når lønadministratoren overfører arbejderens løndata ved at køre jobbet **Overfør til løn** eller **Fleksregulering**, foretages følgende justeringer:

- Arbejderens flekskonto reguleres med -4,0 timer. Derfor bliver flekssaldoen på -6,0 reguleret til arbejderens tilladte fleksmaksimum på 2,0 timer.
- Der oprettes en lønpost for lønarten 1302. Denne lønpost har en lønenhed på 4,0 timer, der føjes til arbejderens løn. I så fald er lønenheden et positivt tal, da den negative regulering af timer på 4,0 ganges med den negative løntypefaktor på -1,0, der er defineret for fleksgruppen. Denne lønenhed skal være en del af den lønfil, der genereres af jobbet **Overfør til løn**.

### <a name="scenario-3-managing-a-workers-flex-balance-based-on-pay-types"></a>Scenarie 3: Administration af en arbejders flekssaldo baseret på lønarter

Som vi har forklaret tidligere kan flekskonti administreres enten baseret på den tid, der er registreret i zonerne Fleks+ og Fleks-, som er defineret af arbejderens arbejdstidsprofil, eller baseret på de lønarter, der er defineret i arbejderens lønaftaler. Hvis der anvendes løntyper reguleres en arbejders flekskonto af de lønposter, der genereres, når du overfører arbejderens registrering fra siden **Godkend**. Du vil muligvis bruge lønarter til at administrere flekskonti, hvis du f.eks. vil øge en arbejders flekskonto med en bestemt faktor i en eller flere flekszoner.

Dette scenario bruger følgende fleksprofil, der repræsenterer en arbejdsdag.

| Profiltype  | Start    | Afslutning      |
|---------------|----------|----------|
| Fleks+         | 12:00 | 08:00 |
| Komme      | 08:00 | 08:00 |
| Fleks-         | 08:00 | 09:00 |
| Normaltid | 09:00 | 11:30 |
| Lønpause    | 11:30 | 12:00 |
| Fleks-         | 12:00 | 04:00 |
| Udstempling     | 04:00 | 04:00 |
| Fleks+         | 04:00 | 12:00 |

I så fald vil du kunne administrere arbejderens flekssaldo baseret på lønarter. Derfor skal du angive indstillingen **Baseret på lønkategorier** til **Ja** for arbejderens fleksgruppe.

For at tage højde for flekstimerne skal du også definere en ny lønart. I dette scenarie hedder lønarten **FlexCnt**.

| Lønart | Betegnelse  |
|----------|--------------|
| FlexCnt  | Flekstidstæller |

Følg derefter disse trin for at konfigurere en lønart og tilføje linjer af den nye lønart til en lønprofil.

1. Vælg **Tid og fremmøde** \> **Opsætning** \> **Grupper** \> **Fleksgrupper**, og vælg derefter **Ny**.
2. Både i feltet **Fleks+** **Fleks -** skal du angive den nye lønart **FlexCnt**.
3. Vælg **Tid og fremmøde** \> **Opsætning** \> **Lønaftaler**, og vælg derefter **Aftalelinjer**.
4. For **Mandag** for profiltypen **Fleks+** skal du tilføje følgende tre linjer.

    | Lønart | Betegnelse  | Fra tidspunkt | Til klokken  | Minimum | Maksimum  | Faktor |
    |----------|--------------|-----------|----------|---------|---------|--------|
    | FlexCnt  | Flekstidstæller | 12:00  | 06:00 | 00:00   | 00:00   | 1,00   |
    | FlexCnt  | Flekstidstæller | 06:00  | 12:00 | 00:00   | 02,00   | 1.50   |
    | FlexCnt  | Flekstidstæller | 06:00  | 12:00 | 02,00   | 06,00   | 2.00   |

    > [!NOTE]
    > Hver linje bruges til et andet tidsinterval og har en anden faktor. De flekstimer, som arbejderen arbejder i et tidsinterval, ganges med faktoren for den pågældende linje. De timer, der arbejdes fra 06:00 til 08:00 ganges f.eks. med 1,50. Faktoren angives i feltet **Faktor** på fanen **Generelt** på siden **Lønaftalelinjer**.

Arbejderen angiver følgende registreringer for dagen.

| Kladderegistreringstype | Start    | Afslutning      |
|---------------------------|----------|----------|
| Komme                  | 07:00 | 07:00 |
| Produktionsjob            | 07:00 | 09:00 |
| Udstempling                 | 09:00 | 09:00 |

Det beløb, der skal betales, beregnes på siden **Godkend** ud fra arbejderens registrering. Når registreringen er beregnet, kan du se resultatet på fanen **Tider**. I dette scenarie skal du være opmærksom på følgende felter.

| Fleks+ | Fleks- | Tidspunkt  | Løntid |
|--------|--------|-------|----------|
| 6,00   | 0,00   | 13,50 | 08,00    |

Mængden af positiv flekstid er seks timer, og beregningen baseres på flekszonerne i tidsprofilen. Beløbet består af en times positiv flekstid fra 07:00 til 08:00 og fem timers positiv flekstid fra 16:00 til 21:00.

Når du overfører registreringerne, vil du bemærke, at værdien for Fleks+ ændres fra 6,0 timer til 8,0 timer.

| Fleks+ | Fleks- | Tidspunkt  | Løntid |
|--------|--------|-------|----------|
| 8,00   | 0,00   | 13,50 | 08,00    |

Ændringen optræder efter overførslen, fordi flekstimerne beregnes ud fra lønarter i stedet for tid. Tabellen nedenfor viser, hvordan de otte timer er beregnet.

| Fra     | Til       | Tidspunkt | Faktor    | Flekskonto |
|----------|----------|------|-----------|--------------|
| 07:00 | 08:00 | 1    | 1         | 1            |
| 04:00 | 06:00 | 2    | 1         | 2            |
| 06:00 | 08:00 | 2    | 1.5       | 3            |
| 08:00 | 09:00 | 1    | 2         | 2            |
|          |          |      | **Total** | **8**        |
