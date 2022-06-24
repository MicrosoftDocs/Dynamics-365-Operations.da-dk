---
title: Funktioner til faktureringsplan
description: Denne artikel indeholder en forklaring på funktionerne til faktureringsplaner, f.eks. prissætningsmetoder, eskaleringer og rabatter, justeringsdatoer, proportionalitet, omvendt fakturering og opdelte varegrupper.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: b6cfebc2bbfe06e118bfc96f9ae0df6323805e39
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853577"
---
# <a name="billing-schedule-features"></a>Funktioner til faktureringsplan

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en forklaring på funktionerne i faktureringsplaner og faktureringsplanlinjer. Det beskriver de forskellige metoder, der bruges til prisfastsættelse, hvordan du bruger eskaleringer og rabatter, og hvordan du omvender en faktureringsperiode. Det indeholder også eksempler på forholdsmæssige beregninger og opdelte varegrupper.

## <a name="pricing-methods"></a>Prissætningsmetoder

Du kan bruge en af følgende prissætningsmetoder til at beregne enhedsprisen for en vare:

* Flad
* Standard
* Niveau
* Fladt niveau

### <a name="flat-pricing"></a>Flad prissætning

Når metoden til flad prissætning bruges, kan enhedsprisen for en linjevare i faktureringsplanen på siden **Alle faktureringsplaner** redigeres til enhver værdi, du ønsker. Værdien af **Prisenhed** er altid **1**. Derfor er værdierne af **Enhedspris** og **Nettobeløb** for en vare ens.

### <a name="standard-pricing-without-a-trade-agreement"></a>Standardprissætning (uden samhandelsaftale)

Når standardprissætningsmetoden bruges uden en samhandelsaftale, kan du konfigurere enhedsprisen for en linjevare i faktureringsplanen ved at vælge **Administration af produktoplysninger** på siden **Frigiv produktdetaljer**. Enhedsprisen vises i afsnittet om **Basissalgspris**. Den beregnes som *Pris* &divide; *Prisantal*.

### <a name="standard-pricing-with-a-trade-agreement"></a>Standardprissætning (med samhandelsaftale)

I følgende eksempler vises standardprisberegningerne, når der findes en samhandelsaftale. Du kan oprette samhandelsaftaler fra siden **Frigiv produktdetaljer**.

I begge eksempler bruges en vare, der har følgende prisrammer.

| Fra antal | Til antal | Enhed | Pris | Prisenhed |
|---|---|---|---|---|
| 0 | 100 | Hver | 1.50 | 1 |
| 100 | 200 | Hver | 1.25 | 1 |
| 200 | 999999 | Hver | 1.00 | 1 |

**Eksempel 1**

Fakturaantallet er 250, og standardprissætningsmetoden anvendes. Da antallet er i prisintervallet 200 til 999.999, er enhedsprisen 1,00. 

Nettobeløbet beregnes på følgende måde:

*Nettobeløb* = (*Antal* &times; *Pris*) &divide; *Prisenhed* = (250 &times; 1,00) &divide; 1 = 250

**Eksempel 2**

Fakturaantallet er 100, og standardprissætningsmetoden anvendes. Da fakturaantallet er i prisintervallet 0 til 100, er enhedsprisen 1,50.

> [!NOTE]
> Fakturaantallet er i intervallet 0 til 100 i stedet for intervallet 100 til 200, da et antal i standardantallet matcher, hvis det er *større end eller lig med* antallet "fra" og *mindre end* "til"-antallet.

Nettobeløbet beregnes på følgende måde:

*Nettobeløb* = (100 &times; 1,50) &divide; 1 = 150

### <a name="tier-pricing"></a>Niveauprissætning

I følgende eksempel har en vare følgende prisrammer.

| Fra antal | Til antal | Enhed | Pris | Prisenhed |
|---|---|---|---|---|
| 0 | 100 | Hver | 1.50 | 10 |
| 100 | 200 | Hver | 1.25 | 10 |
| 200 | 999999 | Hver | 1.00 | 10 |

Hvis fakturaantallet er 250, og metoden for niveauprissætning bruges, beregnes varernes priser på følgende måde baseret på prisrammerne:

- **Første 100 varer:** 100 &times; 1,50 = 150,00
- **Næste 100 varer:** 100 &times; 1,25 = 125,00
- **Resterende varer:** 50 &times; 1,00 = 50,00

Nettobeløbet beregnes på følgende måde:

*Nettobeløb* = (150,00 &divide; 10) + (125,00 &divide; 10) + (50,00 &divide; 10) = 15,00 + 12,50 + 5,00 = 32,50

Når nettobeløbet er beregnet, beregnes enhedsprisen ved at dividere nettobeløbet med antallet:

*Enhedspris* = 32,50 &divide; 250 = 0,13

### <a name="flat-tier-pricing"></a>Flad niveauprissætning

I følgende eksempel har en vare følgende prisrammer.

| Fra antal | Til antal | Enhed | Beløb på fladt niveau | Prisenhed |
|---|---|---|---|---|
| 0 | 50 | Hver | 100.00 | 50 |
| 50 | 200 | Hver | 150.00 | 200 |

I følgende tabel vises fakturaerne og enhedspriserne for de forskellige købsantal. Nettobeløbet beregnes først, og derefter beregnes enhedsprisen.

| Faktura | Antal købt | Enhedspris | Nettobeløb |
|---|---|---|---|
| 1 | 25 | 2,00 &divide; 25 = 0,08 | 100 &divide; 50 = 2,00 |
| 2 | 20 | 2,00 &divide; 20 = 0,10 | 100 &divide; 50 = 2,00 |
| 3 | 50 | 2,00 &divide; 50 = 0,04 | 100 &divide; 50 = 2,00 |
| 4 | 60 | 0,75 &divide; 60 = 0,0125 = 0,01 | 150 &divide; 200 = 0,75 |

## <a name="escalations-and-discounts"></a>Eskaleringer og rabatter

En *eskalering* er en prisstigning for en fremtidig faktureringsperiode, som fakturaen endnu ikke er oprettet for. En *rabat* er et prisfald for en fremtidig faktureringsperiode, som fakturaen endnu ikke er oprettet for.

I abonnementsfakturering kan der ikke anvendes eskaleringer og rabatter på en faktureringsplan. Du kan f.eks. ikke anvende en eskalering på en faktureringsplan tre måneder bagud og behandle den. Du kan med andre ord ikke anvende en prisstigning, der er sket for tre måneder siden.

Du kan anvende en eskalering eller rabat på en faktureringsplan eller faktureringsplanlinje et af følgende steder:

- Listesiden **Alle/Aktive faktureringsplaner**
- En specifik faktureringsplan
- En specifik faktureringsplanlinje

### <a name="apply-an-escalation-or-discount"></a>Anvende en eskalering eller rabat

Hvis du vil anvende en eskalering eller rabat på en faktureringsplan, skal du følge disse trin.

1. Vælg en faktureringsplan eller en faktureringsplanlinje.
2. Vælg **eskalering og rabat** enten under fanen **Eskalering og rabat** eller på faktureringsplanlinjen.
3. Hvis der bruges et forbrugerprisindeks til at beregne eskaleringen eller rabatten, skal du vælge en værdi i feltet **Beregning af forbrugerprisindeks**.
4. Vælg **Ny** for at tilføje en eskalering eller rabatlinje.
5. Markér afkrydsningsfeltet **Rabat** for at få en rabat. Lad afkrydsningsfeltet **Rabat** være ryddet i forbindelse med en eskalering.
6. Angiv felterne **Startdato** og **Frekvens**.
7. Angiv feltet **Slutdato** for udskudte varer, der bruger funktionen til ikke-faktureret omsætning.
8. Angiv feltet **Procent**, **Beløb** eller **Plan for forbrugerprisindeks**.
9. Angiv feltet **Slutdato**.
10. Vælg **OK**.
11. Gentag trin 4 til 10 for hver ekstra eskalering eller rabatlinje, du skal bruge.

### <a name="fields-on-the-billing-schedule-lines-page"></a>Felter på siden Faktureringsplanlinjer

Siden **Faktureringsplanlinjer** indeholder følgende felter.

| Felt | Beskrivelse |
|---|---|
| Varenummer | Varenummeret til faktureringsplanlinjen. Dette felt er kun tilgængeligt, når siden åbnes fra en faktureringsplanlinjevare. |
| Beregning af forbrugerprisindeks | <p>Vælg den metode, der skal bruges til at beregne eskaleringen af forbrugerprisindekset:</p><ul><li>**Tidligere forbrugerprisindeks** – Brug den tidligere værdi af forbrugerprisindekset til eskaleringsberegningen.</li><li>**Basisforbrugerprisindeks** – Brug basisværdien af forbrugerprisindekset til eskaleringsberegningen.</li></ul> |
| **Linje**-gitter | |
| Rabat | <p>Brug afkrydsningsfeltet til at angive, om ændringen i beløbet er en eskalering eller rabat:</p><ul><li>**Markeret** – Ændringen anvender en rabat på faktureringsplanen eller faktureringsplanlinjen.</li><li>**Ryddet** – Ændringen anvender en eskalering på en faktureringsplan eller en planlægningslinje.</li></ul><p>Indstillingen af dette afkrydsningsfelt kan ikke ændres for varer, der bruger funktionen til ikke-faktureret omsætning. Rabatter kan desuden ikke anvendes på varer, hvor der bruges indtægtsfordeling.</p> |
| Startdato | Vælg startdatoen for eskaleringen eller rabatten. |
| Frekvens | Vælg frekvensen af eskalering eller rabat: **Ingen**, **Månedlig**, **Kvartalsvis**, **Halvårlig** eller **Årlig**. |
| Procentdel | Angiv den procentvise eskalering eller rabat. |
| Beløb | Angiv beløbet for eskaleringen eller rabatten. |
| Plan for forbrugerprisindeks | Vælg den plan for forbrugerprisindeks, der skal bruges til beregninger. |
| Slutdato | <p>Vælg slutdatoen for eskaleringen eller rabatten.</p><p>**Bemærk:** Dette felt er påkrævet for varer, der bruger funktionen for ikke-faktureret omsætning.</p> |
| Nummer på udskydelsesplan | <p>Nummeret på udskydelsesplanen.</p><p>Dette felt er kun tilgængeligt, når siden åbnes fra en faktureringsplanlinje.</p> |
| Kladdebatchnummer | <p>Kladdens batchnummer.</p><p>Dette felt er kun tilgængeligt, når siden åbnes fra en faktureringsplanlinje.</p> |
| Slutrabatbeløb | <p>Summen af rabatbeløb for alle linjer i gitteret.</p><p>Dette felt er kun tilgængeligt, når siden åbnes fra en faktureringsplanlinje.</p> |
| Aktuelt kortsigtet ikke-faktureret omsætningsbeløb | <p>Det aktuelle kortsigtede ikke-fakturerede omsætningsbeløb.</p><p>Dette beløb vises, når der er valgt en kortsigtet udskydelsesmetode på siden **Faktureringsparametre for tilbagevendende kontrakter**, og kontiene for linjevaren er konfigureret på siden **Opsætning af ikke-faktureret indtægt**.</p> |
| Aktuelt langsigtet ikke-faktureret omsætningsbeløb | <p>Det aktuelle langsigtede ikke-fakturerede omsætningsbeløb.</p><p>Dette beløb vises, når der er valgt en kortsigtet udskydelsesmetode på siden **Faktureringsparametre for tilbagevendende kontrakter**, og kontiene for linjevaren er konfigureret på siden **Opsætning af ikke-faktureret indtægt**.</p> |

## <a name="proration-examples"></a>Eksempler på proportionalitet

Beregninger af proportionalitet kan baseres på antallet af dage eller antallet af måneder. Den metode, der bruges til beregning af proportionalitet, er angivet på siden **Faktureringsparametre for tilbagevendende kontrakter**. Proportionalitetsmetoden har indflydelse på, hvordan beløbene beregnes for en faktureringsplan i følgende situationer:

- Indledende oprettelse
- Anvendelse af en eskalering eller rabat
- Ophør
- Placering eller fjernelse på hold
- Tilføjelse af support eller fornyelse

Proportionalitetsmetoden har også indflydelse på beregningerne i rapporten over månedlige tilbagevendende indtægter (MRR).

### <a name="example-1"></a>Eksempel 1

Det årlige beløb for en faktureringsplan er $ 5.000. Startdatoen er 12. august 2019, og slutdatoen er 22. december 2019. Faktureringsfrekvensen er årlig. Det forholdsmæssige beløb beregnes på følgende måder, afhængigt af om der bruges daglig eller månedlig beregningsmetode:

- **Dagligt**

    - *Antal dage* = *Slutdato* – *Startdato* + 1 = 133 dage
    - *Antal dage i året* = 11. august 2020 – 12. august 2019 + 1 = 366 dage
    - *Forholdsmæssigt beløb* = 5.000 &times; (133 &divide; 366) = 1816,94

- **Månedligt**

    - *Startmåneds andel* = (31 - 12 + 1) &divide; 31 = 20 &divide; 31
    - *Midtermåneder* = 3
    - *Slutmåneds andel* = 22 &divide; 31
    - Forholdsmæssigt beløb = 5.000 &divide; 12 &times; \[(20 &divide; 31) + 3 + (22 &divide; 31)\] = 1814,52

### <a name="example-2"></a>Eksempel 2

Det årlige beløb for en faktureringsplan er $ 12.000. Startdatoen er 1. august 2019, og slutdatoen er 31. december 2019. Faktureringsfrekvensen er årlig. Det forholdsmæssige beløb beregnes på følgende måder, afhængigt af beregningsmetoden:

- **Dagligt**

    - *Antal dage* = *Slutdato* – *Startdato* + 1 = 153 dage
    - *Antal dage i året* = 31. juli 2020 – 1. august 2019 + 1 = 366 dage
    - *Forholdsmæssigt beløb* = 12.000 &times; (153 &divide; 366) = 5016,39

- **Månedligt (Hel måned)**

    - *Antal måneder* = 5
    - *Måneder i alt* = 12
    - *Forholdsmæssigt beløb* = (12.000 &times; 5) &divide; 12 = 5.000

## <a name="reversing-a-period-billing"></a>Omvendt periodefakturering

I dette eksempel er der kun én linje i en faktureringsplan:

- Fakturering sker en gang om måneden i 12 måneder fra januar til og med december.
- Der er oprettet fakturaer for alle perioder frem til og med april.

Du vil omvende fakturaen for faktureringsperioden i april.

Hvis der endnu ikke er oprettet en salgsfaktura for faktureringsperioden i april, kan du slette salgsordren. I dette tilfælde fjernes statussen **Faktureret** for detaljerne. Men da der er oprettet en faktura for faktureringsperioden, kan statussen **Faktureret** for detaljerne ikke ryddes. Hvis du vil omvende faktureringen for april, skal du derfor oprette en modkreditnota for linjen.

1. Opret en planlinje for samme vare på siden **Alle faktureringsplaner**.
2. Ret varens værdi af **Antal** til negativ af det oprindelige antal.
3. Angiv feltet **Faktureringsfrekvens** til **Én gang**.
4. Opdater start- og slutdatoerne, så de svarer til datoerne på den faktureringsdetaljelinje, du vil oprette en kreditnota for. I dette eksempel skal du angive startdatoen til 1. april 2019 og slutdatoen til 30. april 2019.
5. Gem ændringerne.
6. Åbn siden **Generér faktura**, og opret den salgsordre, der har kreditnotaen for den angivne periode.
7. Valgfrit: Bogfør fakturaen.

Når du gennemgår linjerne i faktureringsplanen, bemærker du, at den nye linje har et link til kreditnotaen. Den oprindelige linje har stadig et link til den oprindelige faktura for april.

## <a name="split-item-group-examples"></a>Eksempler på opdeling af varegrupper

I dette eksempel er følgende opsætning på plads:

- På siden **Faktureringsparametre for tilbagevendende kontrakter** vælges **Opdel efter varegruppe**, og feltet **Entydig planlægningstype** er angivet til **Kunde**.
- Der er oprettet tre varegrupper: **PREFIX**, **DATAHUB** og **SPP**.
- Kunde US-001 har flere faktureringsplaner, hvor varegruppen er PREFIX eller DATAHUB.
- Kunde US-002 har flere faktureringsplaner, hvor varegruppen er PREFIX eller SPP.

| Faktureringsplannummer | Kunde | Varegruppe |
|---|---|---|
| SCH001 | US-001 | PREFIX |
| SCH002 | US-001 | DATAHUB |
| SCH003 | US-002 | PREFIX |
| SCH004 | US-002 | SPP |

Kunde US-001 køber en fornyelsesvare, der tilhører varegruppen PREFIX. Denne transaktion er en ny salgsordre.

| Salgsordrenr. | Kunde | Hovedvare | Fornyelsesvare | Fornyelsesvaregruppe | Faktureringsplannummer |
|---|---|---|---|---|---|
| SO0001 | US-001 | D0001 | D0002 | PREFIX | SCH001 |

Når fakturaen for salgsordren bogføres, føjes fornyelsesvaren til den eksisterende faktureringsplan (SCH001) for kunden. I denne faktureringsplan bruges varegruppen PREFIX. Alle fornyelsesvarer, der tilhører samme varegruppe, placeres i samme faktureringsplan.

**Overskrift**
 
| Faktureringsplannummer | Kunde | Varegruppe |
|---|---|---| 
| SCH001 | US-001 | PREFIX |

**Linje**

| Faktureringsplannummer | Kunde | Varegruppe |
|---|---|---|
| SCH001 | US-001 | D0002 |

Kunde US-001 køber nu en fornyelsesvare, der tilhører varegruppen SPP. Denne transaktion er en ny salgsordre.

| Salgsordrenr. | Kunde | Hovedvare | Fornyelsesvare | Fornyelsesvaregruppe | Faktureringsplannummer |
|---|---|---|---|---|---|
| SO0002 | US-001 | D0003 | D0004 | SPP | |

Aktuelt har kunde US-001 ikke en faktureringsplan, der bruger SPP-varegruppen. Derfor oprettes der en ny faktureringsplan.

**Overskrift**

| Faktureringsplannummer| Kunde | Varegruppe |
|---|---|---|
| SCH005 | US-001 | SPP |

**Linje**

| Faktureringsplannummer | Kunde | Varegruppe |
|---|---|---|
| SCH005 | US-001 | D0004 |

### <a name="multiple-billing-schedules-for-the-same-end-user-and-customer"></a>Flere faktureringsplaner for samme slutbruger og kunde

I dette eksempel er følgende opsætning på plads:

- På siden **Faktureringsparametre for tilbagevendende kontrakter** vælges **Opdel efter varegruppe**, og feltet **Entydig planlægningstype** er angivet til **Slutbruger**.
- På siden **Slutbrugere** er følgende relation for kunder og slutbrugere konfigureret.

    | Kundekonto | Slutbrugerkonto |
    |---|---|
    | US-001 | US-221 |

Flere faktureringsplaner er oprettet for kombinationen af kunde og slutbruger Da **Opdel efter varegruppe** er valgt på siden **Faktureringsparametre for tilbagevendende kontrakter**, kan der oprettes flere faktureringsplaner for samme kunde- og slutbrugerrelation.

| Faktureringsplannummer | Kunde | Slutbrugerkonto | Overskriftsvaregruppe |
|---|---|---|---|
| SCH005 | US-001 | US-221 | IG1 |
| SCH006 | US-001 | US-221 | IG2 |
| SCH007 | US-001 | US-221 | IG3 |

På siden **Vareopsætning** kan du oprette relationer for support og fornyelse af varer.

| Varekode | Varerelation | Supportvare | Fornyelsesvare | Fornyelsesvaregruppe |
|---|---|---|---|---|
| Tabellen | D001 | ITEM27 | D007 | IG1 |
| Tabellen | D002 | ITEM28 | D005 | IG2 |
| Tabellen | D003 | ITEM29 | D006 | IG3 |

Der oprettes nu en salgsordre for kunde US-001. Denne salgsordre indeholder varer fra siden **Vareopsætning**. Når du opretter salgsordren, skal du åbne siden **Support og fornyelsesproces** og indstille feltet **Slutbrugerkonto** og eventuelle andre obligatoriske oplysninger for fornyelsesvaren.

Når fakturaen for transaktionen oprettes og bogføres, oprettes der forskellige faktureringsplaner for kombinationen af kunde/slutbruger og varegruppe. Der kan knyttes mere end én linje på samme salgsordre til samme faktureringsplan.

| Salgsordrenr. | Kunde | Slutbrugerkonto | Hovedvare | Supportvare | Fornyelsesvare | Faktureringsplannummer |
|---|---|---|---|---|---|---|
| SO0001 | US-001 | US-221 | D001 | ITEM27 | D007 | SCH005 |
| SO0001 | US-001 | US-221 | D002 | ITEM28 | D005 | SCH006 |
| SO0001 | US-001 | US-221 | D003 | ITEM29 | D006 | SCH005 |
