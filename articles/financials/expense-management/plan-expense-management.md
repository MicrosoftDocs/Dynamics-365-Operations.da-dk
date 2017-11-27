---
title: Konfigurer udgiftsstyring
description: "I denne artikel beskrives de overvejelser og de beslutninger, du skal foretage i planlægningsprocessen, før du konfigurerer Udgiftsstyring i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4fad62c5da11e88e07f4e9d4343c4ac1a487bdd8
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="configure-expense-management"></a>Konfigurer udgiftsstyring

[!include[banner](../includes/banner.md)]


I denne emne beskrives de overvejelser og de beslutninger, du skal foretage i planlægningsprocessen, før du konfigurerer Udgiftsstyring i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. Du kan gemme oplysninger om bl.a betalingsmetoderne, rejserekvisitioner, udgiftsrapporter og politikker i området Udgiftsstyring.

Da mange af de beslutninger, du foretager, når du planlægger din konfiguration for udgiftsstyring, er baseret på organisationens hierarki og økonomiske struktur, skal du referere til planlægningsdokumenterne for de pågældende områder.

## <a name="intercompany-expenses"></a>Interne udgifter

Når du aktiverer interne udgifter, giver du juridiske enheder og medarbejdere mulighed for at pådrage dig udgifter på vegne af en anden juridisk enhed og opkræve betaling fra den juridiske enhed med ansættelsen i organisationen. En medarbejder i juridisk enhed A fuldfører f.eks. et projekt for juridisk enhed B, og projektet indebærer rejserelaterede udgifter. Hvis interne udgifter er aktiveret, kan medarbejderen derefter indsende en udgiftsrapport, der bogfører udgiften til juridisk enhed B, og udgiften skal derefter betales af juridisk enhed A. Hvis organisationen ikke har flere juridiske enheder, behøver du ikke at aktivere interne udgifter.

**Beslutning:** Vil du aktivere interne udgifter?

## <a name="financial-management"></a>Økonomistyring

Udgiftsstyring er tæt integreret med den finansielle forvaltning af organisationen. Mange af konfigurationerne for udgiftsstyring baseres på de beslutninger, du har foretaget om virksomhedens økonomi. I følgende afsnit beskrives de forskellige områder, der kræver planlægning og beslutninger, der er baseret på organisationens finansielle beslutninger og vejledning fra ledelsen.

### <a name="per-diems"></a>Diæter

Du skal definere medarbejderen pr. diæt, som organisationen stiller til rådighed. Da diæter normalt bruges til at dække udgifter som måltider, logi og andre omkostninger, kan du oprette regler for diætgodtgørelser, som organisationen tilbyder. Diætsatser kan baseres på tidspunktet på året, rejselokationen eller begge. Når du definerer en diætregel, kan du angive, at du vil tilbageholde en procentdel af en diætsats, hvis en arbejder modtager ekstra måltider eller tjenester. Du kan også definere diætsatsniveauer for at angive et minimum- og maksimumantal timer, en diætsats kan gælde for en arbejders rejse.

**Beslutninger:**

- Standarddiætregler for første og sidste dag:

    - Hvad er det mindste antal timer, en medarbejder kan gøre krav på for en dag og stadig få en diæt?
    - Er der en reduktion af det beløb, der tilbydes for måltider for den første og sidste dag? Hvis der er en reduktion af, hvad er procentdelen for reduktionen?
    - Er der en reduktion af det beløb, der tilbydes for et hotel for den første og sidste dag? Hvis der er en reduktion af, hvad er procentdelen for reduktionen?
    - Er der en reduktion af det beløb, der tilbydes for andre udgifter, der påløber den første og sidste dag? Hvis der er en reduktion af, hvad er procentdelen for reduktionen?

- Standarddiætregler:

    - Er der en procentvis reduktion i diætgodtgørelsen til hvert måltid, hvis for eksempel måltidet er gratis? Hvis der er en reduktion af, hvad er procentdelen for reduktion for hvert måltid?
    - Beregnes nedsættelsen for måltider pr. dag, pr. rejse eller med antallet af måltider pr. dag?
    - Skal diætbeløb afrundes på almindelig måde eller rundes op?
    - Bliver diæter beregnet baseret på en 24-timers periode eller en kalenderdag?

- Diætregler, der er baseret på lokalitet:

    - Varierer diætsatser efter lokalitet? Hvilke lokalitet medtages?
    - Hvis diætsatser varierer i henhold til lokalitet, hvilken procentdel af beløbet tilbydes så for hver lokalitet for følgende typer udgifter:

        - Måltider
        - Hotel
        - Øvrige udgifter

### <a name="expense-management-journals-and-accounts"></a>Administration af udgiftskladder og konti

Udgiftsstyring kræver, at du bruger flere kladder og konti. For eksempel skal du beslutte, om den samme konto bruges til kontantforskud og tvister om kreditkort.

**Beslutninger:**

- Hvilken finanskladde skal godkendte udgiftsrapporter bogføres til?
- Hvilken konto bruges der til kontantforskud?
- Skal kontantforskud bogføres med det samme?

### <a name="payment-methods"></a>Betalingsmetoder

Når du tillader medarbejdere at pådrage dig udgifter på vegne af din virksomhed, skal du definere de betalingsmetoder, medarbejdere har tilladelse til at bruge. For eksempel kan du tillade medarbejdere at bruge penge eller firmaets kreditkort. Du kan også tillade medarbejdere at bruge personlige kreditkort og derefter refundere medarbejderne. Du skal træffe følgende beslutninger for hver betalingsmetode, du tillader.

**Beslutninger:**

- Hvile betalingsmetoder er tilladte?
- Hvem ejer udgifterne til betalingsmetoden?
- Er der en modkontotype? Hvis der findes en modkontotype, hvad er den?
- Hvis der findes en modkonto, hvad er kontoen?
- Hvis betalingsmetoden er et kreditkort, skal betalingsmetoden så kun bruges ved importerede transaktioner?

### <a name="expense-categories-and-shared-categories"></a>Udgiftskategorier og delte kategorier

Når medarbejderne opretter en udgiftsrapport, skal hver udgift, de registrerer, knyttes til en udgiftskategori. Udgiftskategorier stammer fra delte kategorier, der kan deles på tværs af de juridiske enheder i organisationen. Disse kategorier kan også deles i Projektstyring og regnskab, afhængigt af den måde organisationen er defineret på. Baseret på definitionen af organisationen og vejledning fra implementeringsgruppen skal du afgøre, om de kategorier, der bruges i udgiftsstyring, kun skal bruges i udgiftsstyring, eller om de skal deles mellem projektstyring og regnskab og udgiftsstyring. Bemærk, at disse kategorier kan deles mellem projekt og udgift eller projekt og produktion, men ikke mellem udgift og produktion. Du skal træffe følgende beslutninger for hver udgiftskategori.

**Beslutninger:**

- Hvad er udgiftskategorien? Eksemplerne omfatter kategorier for flyvninger, hotel eller kørsel.
- Kan udgiftskategorien også bruges i projektstyring og regnskab?
- Hvad er udgiftstypen?
- Hvad er standardbetalingsmetoden for udgiftskategorien?
- Skal udgifter i udgiftskategorien specificeres?
- Hvad er standardhovedkontoen for udgiftskategorien?
- Hvad er standardvaremomsgruppen for udgiftskategorien?
- Er yderligere betalingsmetoder tilladt for denne udgiftskategori? Hvis flere betalingsmetoder er tilladt, hvilke er der så tale om?
- Er der underkategorier i denne udgiftskategori? Hvis der er underkategorier, skal du også foretage følgende beslutninger:

    - Er der nogen af de underkategorier, der er udelukket fra momsopkrævning?
    - Hvad er varemomsgruppen for underkategorierne?

Hvis udgiftskategorien også anvendes i projektstyring og regnskab, skal du svare på de resterende spørgsmål. Ellers gå videre til næste afsnit.

- Hvilke omkostningskonti skal der bruges til følgende udgifter?

    - Kost
    - Lønfordeling
    - IGVF - kostværdi
    - Omkostning-vare
    - IGVF - kostværdi - vare
    - Periodiseret tab
    - IGVF - periodiseret tab

- Hvilke indtægtskonti skal der bruges til følgende?

    - Faktureret omsætning
    - Periodiseret omsætning – Salgsværdi
    - IGVF - salgsværdi
    - Periodiseret omsætning – produktion
    - IGVA – produktion
    - Periodiseret omsætning – profit
    - IGVA - profit
    - Periodiseret omsætning – abonnement
    - IGVF - Abonnement

### <a name="taxes"></a>Afgifter

For udgiftsrelateret moms skal du bestemme, hvad der er inkluderet eller aktiveret i udgiftsrapporter.

**Beslutninger:**

- Indgår der moms i udgiftsbeløbet?
- Skal momsopkrævning være aktiveret på udgifter?

    > [!NOTE]
    > Når du havde planlagt finans, kan du ikke aktivere momsopkrævning på udgifter, hvis du har besluttet at anvende amerikanske regler for moms og importmoms. (For at anvende regler for amerikansk moms og importmoms, skal du angive indstillingen **Anvend reglerne for moms** til **Ja**).

## <a name="policies"></a>Politikker

Når du oprettet udgiftsrapportpolitikker, kan din virksomhed spare tid og penge, når medarbejderne pådrager virksomheden udgifter på dens vegne. Politikker sikrer, at medarbejderne holder sig inden for budgettet, angiver alle nødvendige oplysninger og kun bruger penge, når der er behov for det. Du skal træffe følgende beslutninger for hver udgiftsrapportpolitik og hver udgiftsrapportgodkendelsespolitik, du opretter.

**Beslutninger:**

- Hvad er navnet på politikken?
- Hvad er udgiftspolitikken til?
- Hvis du tidligere har besluttet at aktivere interne udgifter, for hvilke virksomheder i organisationen skal denne politik anvendes?
- Hvornår vil politikken være gældende?
- Hvornår udløber politikken?
- Hvad er politikreglen?
- Hvad er resultatet af politikreglen?

