---
title: Planlægge din lokale kontoplan
description: Denne artikel indeholder oplysninger, der kan hjælpe dig med at planlægge kontoplanen, når du har krav til lovpligtige/lokale krav til din organisation.
author: VeselinaE
ms.date: 10/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts, LedgerConsolidateAccountGroup, MainAccountConsolidateAccount, DimensionDetails, MainAccountDetails
ROBOTS: ''
audience: Application User
ms.devlang: ''
ms.reviewer: twheeloc
ms.tgt_pltfrm: ''
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.search.industry: ''
ms.author: veneva
ms.search.validFrom: 10/07/2021
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78379fd51cf24985fce83e2b6aa9a475af7df363
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946239"
---
# <a name="plan-your-local-chart-of-accounts"></a>Planlægge din lokale kontoplan

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger, der kan hjælpe dig med at planlægge kontoplanen, når din organisation omfatter juridiske enheder, der skal opfylde kravene for specifikke lokaliteter, hvor de gør forretning. Denne artikel bruger følgende begreber til at beskrive kontoplaner:

- **Global** – Den kontoplan, som organisationen bruger globalt. I de fleste tilfælde konsoliderer du til denne kontoplan.
- **Lokal** – En kontoplan, som juridiske enheder i et bestemt land eller område bruger.
- **Delt** – En kontoplan, som mere end én juridisk enhed kan bruge. Både den globale kontoplan og lokale kontoplaner kan deles.

Du kan oprette og dele flere kontoplaner. En delt kontoplan kan bruges af mere end én juridisk enhed, men der kan kun tildeles én kontoplan til hver juridiske enhed. Kontoplanen, der bruges af en juridisk enhed, defineres på siden **Finans**.

Når de designer kontoplanen, søger mange organisationer at oprette en global kontoplan. Den delte kontoplan giver mulighed for oprettelse af en global kontoplan. Det er en fordel at oprette og bruge en enkelt kontoplan. Det er f.eks. nemmere til styring og kontrol, vedligeholdelse og rapportering.

De fleste organisationer foretrækker en global kontoplan, og det er den nemmeste type at implementere. Nogle juridiske enheder kræver dog en lokal kontoplan af følgende årsager:

- Lokale lovpligtige krav
- Krav til lokale regnskabsstandarder
- Branchekrav
- Firmaspecifikke krav til rapportering og analyse

Hvis din organisation kræver, at en juridisk enhed bruger en lokal kontoplan, er der to muligheder for implementering af den:

- Tildel den globale kontoplan, og definer andre metoder til at opfylde de lokale krav.
- Tildel en lokal kontoplan til den juridiske enhed, og definer relationer til den globale kontoplan.

Organisationsstrukturen og rapporteringsstrukturen bestemmer, hvilken mulighed der bruges.

[![Diagram, der viser, hvordan organisationsstrukturen afgør, om der skal bruges en global eller lokal kontoplan](./media/local-chart-of-accounts-diagram.png)](./media/local-chart-of-accounts-diagram.png)

Hvis den globale kontoplan er tildelt til den juridiske enhed, er der følgende muligheder for opfyldelse af lokale rapporteringskrav:

- Foretag lokal konsolidering.
- Brug en økonomisk dimension til at spore den lokale kontoplan.
- Opret lokale hovedkonti i den globale kontoplan.
- Udfør ekstern tilknytning til den lokale kontoplan.

Hvis en lokal kontoplan er tildelt til den juridiske enhed, er den eneste aktuelle mulighed for opfyldelse af globale rapporteringskrav den globale konsolidering:

## <a name="global-chart-of-accounts-assigned-to-a-legal-entity"></a>Global kontoplan, der er tildelt en juridisk enhed

Hvis du skal tildele en juridisk enhed den globale kontoplan, er der fire muligheder for konfiguration af systemet som beskrevet tidligere. Til alle fire muligheder konfigureres en enkelt kontoplan, som er kædet sammen med hver juridiske enhed på siden **Finans**. Derefter bruger hver mulighed en anden metode til at opfylde kravene til lokalisering. Følgende afsnit beskriver trinnene på højt niveau for at konfigurere systemet til kravene til lokalisering. De beskriver også fordelene og ulemperne ved de forskellige muligheder.

### <a name="do-local-consolidation"></a>Foretage lokal konsolidering

Lokal konsolidering er den anbefalede fremgangsmåde for opfyldelse af krav til lokale kontoplaner og anvendelse af den systemfunktionalitet, der er udviklet til dette formål.

#### <a name="set-up-consolidation-for-a-local-chart-of-accounts"></a>Konfigurere konsolidering for en lokal kontoplan

1. Opret en enkelt global kontoplan, der indeholder alle nødvendige hovedkonti.
2. I hver juridiske enhed skal du tildele den globale kontoplan på siden **Finans**.
3. Opret en juridisk enhed til konsolidering for hver lokalisering, der kræves.
4. Udfør ét af følgende trin:

    - Hvis der kun kræves én lokalisering, skal du konfigurere koncernkontoen på **Hovedkonto**-siden eller bruge siderne **Koncerngrupper** og **Flere koncernkonti**.
    - Hvis der kræves mere end én lokalisering, eller hvis både kontonummeret og kontonavnet kræver oversættelse, skal du bruge siderne **Koncerngrupper** og **Flere koncernkonti** til at repræsentere kravene til lokalisering.

5. Kør konsolideringsprocessen for at transformere værdien fra kildens juridiske enhed, der bruger den globale kontoplan, til det konsoliderede regnskab, der bruger den lokale kontoplan.

#### <a name="advantages"></a>Fordele

- Denne metode giver en gennemført måde at arbejde på i hele organisationen.
- Der udføres én oversættelse af den lokale position.
- Denne metode understøtter oversættelse af både hovedkonto-id'et og navnet på hver hovedkonto.
- Det understøtter flere lokaliseringer.

#### <a name="disadvantages"></a>Ulemper

- Der oprettes en ekstra konsolideret regnskab.
- Der fuldføres en ekstra konsolideringsproces.
- Denne metode kan først rapportere i det lokaliserede diagram, når konsolideringsprocessen er fuldført.

### <a name="use-a-financial-dimension-to-track-the-local-chart-of-accounts"></a>Bruge en økonomisk dimension til at spore den lokale kontoplan

Denne metode bruger en økonomisk dimension, hvor de økonomiske dimensionsværdier repræsenterer de lokale hovedkonti, der kræves til lokalisering. Det fungerer godt, hvis der kun kræves én lokalisering. Den bliver dog mindre anvendelig, når du tilføjer flere lokaliseringer og økonomiske dimensioner.

#### <a name="set-up-a-financial-dimension-for-a-local-chart-of-accounts"></a>Konfigurere en økonomisk dimension til en lokal kontoplan

1. Opret en enkelt global kontoplan, der indeholder alle nødvendige hovedkonti.
2. I hver juridiske enhed skal du tildele den globale kontoplan på siden **Finans**.
3. Opret en økonomisk dimension, der repræsenterer den lokale kontoplan.
4. Opret økonomiske dimensionsværdier, der repræsenterer hovedkontiene i den lokale kontoplan.
5. Opdater kontostrukturen, så den indeholder den økonomiske dimension "lokal kontoplan".
6. Sørg for, at den økonomiske dimension "lokale kontoplaner" altid har en værdi, og at den ikke tillader en tom værdi. Overvej at bruge afledte dimensioner eller faste dimensioner.
7. Opret et økonomisk dimensionssæt, hvor den økonomiske dimension "lokal kontoplan" er den første valgte økonomiske dimension. Det økonomiske dimensionssæt kan bruges, når råbalancen oprettes.

#### <a name="advantages"></a>Fordele

- Hovedkontiene i både globale og lokale kontoplaner findes på transaktionsniveau. Hovedkontoen er global, og den økonomiske dimensionsværdi er lokal.
- Denne metode giver mulighed for rapportering i realtid og visninger af både den globale økonomiske position og den lokale økonomiske position.

#### <a name="disadvantages"></a>Ulemper

- Hvis feltet **Værdier, der bruges til samlekonto** er angivet til **Regnskabsfordelinger** i finansparametre, bruges de økonomiske dimensioner, der repræsenterer hovedkontoen for udgift/aktiv/omsætning, forkert til samlekontoen Debitor og Kreditor. Vi anbefaler, at du angiver feltet til et kildedokument i stedet for at sikre, at de korrekte økonomiske dimensionsværdier bruges.
- Hvis der kræves mange lokale kontoplaner, og der bruges én økonomisk dimension til dem alle, kan listen over de økonomiske dimensionsværdier, der bruges, blive lang og vanskelig at arbejde med.
- Hvis der kræves mange lokale kontoplaner, og der bruges en separat økonomisk dimension til at repræsentere hver enkelt, kan systemets anvendelighed og ydeevne påvirkes, når der tilføjes økonomiske dimensioner og økonomiske dimensionssæt.
- Det anbefales, at du nøje overvejer antallet af økonomiske dimensioner, du har brug for, antallet af værdier i hver enkelt og antallet af økonomiske dimensionssæt, da alle disse faktorer kan påvirke systemets ydeevne.

### <a name="create-local-main-accounts-in-the-global-chart-of-accounts"></a>Oprette lokale hovedkonti i den globale kontoplan

*Hvad kopieditoren spurgte om*: I denne metode omfatter de lokale hovedkonti i den globale kontoplan hovedkontiene i den lokale kontoplan i den globale kontoplan.

*Oprindelig version:* De lokale hovedkonti i den globale kontoplan er en metode, hvor de lokale hovedkonti for kontoplanen er medtaget i den globale kontoplan.

*Skal det siges sådan*: I denne metode indgår de lokale hovedkonti i den lokale kontoplan i den globale kontoplan.


#### <a name="set-up-local-main-accounts-in-the-global-chart-of-accounts"></a>Konfigurere lokale hovedkonti i den globale kontoplan

1. Opret en enkelt kontoplan, der indeholder hovedkontiene til både den globale kontoplan og den lokale kontoplan.
2. I hver juridiske enhed skal du tildele kontoplanen på siden **Finans**.
3. Opret totalkonti i kontoplanen for at opsummere de hovedkonti, der repræsenterer samme formål.
4. Opret juridiske enheders tilsidesættelser på hver lokal konto for at forhindre transaktioner fra andre juridiske enheder, som den lokale konto ikke er beregnet til.
5. Opret juridiske enheders tilsidesættelser på hver globale konto for at forhindre transaktioner fra de juridiske enheder for lokalisering.

#### <a name="advantages"></a>Fordele

- Du kan se både den globale økonomiske situation og den lokale økonomiske situation i realtid i bestemte rapporter og i specifikke visninger i systemet, f.eks. en økonomisk balancerapport. Du kan også få adgang til den ved hjælp af knappen **Periode** på totalkontoen.
- Du har ikke et ekstra segment i finanskontoen.

#### <a name="disadvantages"></a>Ulemper

- Brugen af totalkonti og synlighed er begrænset. Totalkonti kan f.eks. ikke ses på listesiden **Råbalance**.
- Vedligeholdelse kræver ekstra indsats.
- Det kræver ekstra manuelt arbejde at oprette økonomirapporter.

### <a name="do-external-mapping-to-the-local-chart-of-accounts"></a>Udføre ekstern tilknytning til den lokale kontoplan

I tilknytningen af en global kontoplan antages det, at du administrerer tilknytningen og lokaliseringerne uden for systemet. I denne metode skal du blot oprette en enkelt global kontoplan i Microsoft Dynamics 365 Finance og håndtere kravene uden for systemet.

#### <a name="set-up-external-mapping-to-a-local-chart-of-accounts"></a>Konfigurere ekstern tilknytning til en lokal kontoplan

1. Opret en enkelt global kontoplan, der indeholder alle nødvendige hovedkonti.
2. I hver juridiske enhed skal du tildele den globale kontoplan på siden **Finans**.
3. Udfør tilknytning til den lokale kontoplan uden for Finance.

#### <a name="advantages"></a>Fordele

- Denne metode giver en ensartet måde at arbejde på i hele organisationen.

#### <a name="disadvantages"></a>Ulemper

- Der er ingen tilgængelig lokal rapportering fra systemet.
- Denne metode giver ofte fejl, når der oprettes økonomirapporter.

## <a name="local-chart-of-accounts-assigned-to-legal-entity"></a>Lokal kontoplan, der er tildelt en juridisk enhed

Hvis din organisation beslutter ikke at bruge en global kontoplan på tværs af juridiske enheder, oprettes der en separat kontoplan for hver enkelt entydige lokale kontoplan. Hver juridiske enhed knyttes derefter til den tilsvarende kontoplan på siden **Finans**.

### <a name="do-global-consolidation"></a>Foretage global konsolidering

I denne metode bruges et konsolideret regnskab til at opsummere og kombinere saldi fra hver enkelt lokale virksomhed til den samlede globale kontoplan i det konsoliderede regnskab. Denne metode kræver, at du vedligeholder en tilknytning af hver lokale kontoplan til den globale kontoplan i det konsoliderede regnskab.

#### <a name="set-up-global-consolidation"></a>Konfigurere global konsolidering

1. Opret en separat kontoplan for hver juridiske enhed, der har andre lokale kontoplaner. Hvis juridiske enheder har samme lokale kontoplan, er der kun brug for én lokal kontoplan, og den kan deles.
2. I hver juridiske enhed skal du tildele den relevante kontoplan på siden **Finans**.
3. Valgfrit: Opret en kontoplan til den globale kontoplan for hvert konsoliderede regnskab, som har en anden global kontoplan.
4. Opret en juridisk enhed til konsolidering for hvert påkrævede konsolideringsniveau, og tildel den relevante kontoplan på siden **Finans**.
5. Udfør ét af følgende trin:

    - Hvis der kun kræves én konsolidering, skal du konfigurere koncernkontoen på siden **Hovedkonto**.
    - Hvis der kræves mere end én konsolidering, eller hvis både kontonummeret og kontonavnet kræver oversættelse, skal du bruge siderne **Koncerngrupper** og **Flere koncernkonti** til at repræsentere kravene til den globale kontoplan.

6. Kør konsolideringsprocessen for at overføre saldi fra de lokale juridiske enheder til den konsoliderede juridiske enhed. Denne konsoliderede juridiske enhed bruger de koncernkonti, du har defineret i trin 5.

#### <a name="advantages"></a>Fordele

- Formatet for de lokale regnskabsstandarder anvendes indbygget.
- Denne metode gør det lettere for det lokale finansteam at arbejde.

#### <a name="disadvantages"></a>Ulemper

- Der er ingen tilgængelig visning i realtid af den globale position.
- Konsolideringsprocessen kan blive kørt oftere.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Planlægge din kontoplan](plan-chart-of-accounts.md)
- [Konfigurere finans](configure-ledger.md)
- [Økonomiske dimensioner og bogføring](Default-dimensions.md#balancing-dimension)
- [Økonomiske dimensionsopsætninger](financial-dimension-sets.md)
- [Oversigt over konsolidering og eliminering](../budgeting/consolidation-elimination-overview.md)
- [Koncernkontogrupper og supplerende koncernkonti](../budgeting/consolidation-account-groups-consolidation-accounts.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
