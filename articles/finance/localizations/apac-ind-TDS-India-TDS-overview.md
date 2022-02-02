---
title: Oversigt over indisk kildeskat (TDS – Tax Deducted at Source)
description: Dette emne indeholder detaljerede oplysninger om indisk kildeskat (TDS – Tax Deducted at Source) . Skattedokumentationen dækker denne funktion.
author: kailiang
ms.date: 03/19/2021
ms.topic: overview
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d33faaff8be4821005b8772875eb91f0afe26cb0
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983897"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a>Oversigt over indisk kildeskat (TDS – Tax Deducted at Source)

[!include [banner](../includes/banner.md)]

Dette emne indeholder detaljerede oplysninger om indisk kildeskat (TDS – Tax Deducted at Source) .

Skattedokumentationen dækker denne funktion. Den forklarer også, hvordan du foretager den grundlæggende opsætning af kildeskat, beregner kildeskat for transaktioner, fuldfører skatteudligningsprocessen, registrerer skattecertifikatnumre og genererer skatteforespørgsler, skatteopgørelser og skattecertifikater. Dokumentet dækker følgende emner:

- [Grundlæggende opsætning for kildeskat](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [Funktioner i formeldesigneren og for grænseværdi, som bruges til skatteberegning](apac-ind-TDS-Formula-designer.md)
- [Beregning af kildeskat for fakturaer, betalinger, egenveksler og interne transaktioner](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [Periodisk skatteudligningsproces og udligning af skattebeløb til kreditorer hos skattemyndigheder](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [Registrere og opdatere skattecertifikatnumre og -datoer](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a>Introduktion til kildeskat

I henhold til Skatteloven 1961 fratrækkes indkomstskatten ved kilden af modtageren af tjenesten på tidspunktet for forudbetaling eller bogføring af kreditten, alt efter hvad der indtræffer først. Den person, der foretager betalingen, skal trække skattebeløbet fra og kun betale nettosaldoen til udbyderen af tjenesten. Kildeskat beregnes af tjenester, som myndighederne har specificeret, og skatten fratrækkes ud fra de satser, som myndighederne har specificeret for en periode. Fradragssatsen er baseret på status for den enhed, der modtager betalingen eller leverer tjenesten. Statusserne inkluderer **Individuelt**, **Indisk uopdelt familie** (**HUF**), **Virksomhed**, **Firma**, **Tilknytning af personer** (**AOP**), **Gruppe af enkeltpersoner** (**BOI**) og **Lokal myndighed**.

I følgende afsnit vises de tjenester, som kildeskat gælder for som angivet af den indiske regering.

**Hjemmehørende**

- Lønindtægter (under afsnit 192)
- Renteindtægter på værdipapirer (under afsnit 193)
- Indtægter fra udbytte (under afsnit 194)
- Renteindtægter (under afsnit 194A)
- Indtægter fra lotterier eller konkurrencer (under afsnit 194B)
- Gevinster fra hestevæddeløb (under afsnit 194BB)
- Kontrahenter og underleverandører (under afsnit 194C)
- Forsikringserstatning (under afsnit 194D)
- Indtægter fra indbetalinger til national opsparingsordning (under afsnit 194EE)
- Indtægter fra fælles fond eller UTI (under afsnit 194F)
- Provision, vederlag, præmie osv ved salg eller handel (under afsnit 194G)
- Betaling af provision eller kurtage (under afsnit 194H)
- Leje (under afsnit 194I)
- Professionel tjeneste (under afsnit 194J)
- Indtægter fra enheder (under afsnit 194K)
- Betaling af kompensation ved anskaffelse af bestemte former for immateriel ejendom (under afsnit 194LA)

**Ikke-hjemmehørende**

- Betalinger til ikke-hjemmehørende sportsmænd eller dennes sportsorganisation (under afsnit 194E)
- Øvrige beløb (under afsnit 195)
- Indtægter i forbindelse med enheder for ikke-hjemmehørende (under afsnit 196A)

    - Indtægter fra obligationer og aktier i udenlandsk valuta for indisk virksomhed (under afsnit 196C)
    - Indtægter fra værdipapirer for udenlandske investorer (under afsnit 196D)
    - Løn og alle andre positive indtægter under enhver type indtægt (afsnit 192)
    - Rente på værdipapirer (afsnit 193)
    - Anden rente end rente på værdipapirer (afsnit 194A)
    - Betalinger til kontrahenter og underleverandører (afsnit 194C)
    - Gevinster fra lotteri eller krydsord (afsnit 194B)
    - Gevinster fra hestevæddeløb (afsnit 194BB)
    - Forsikringsudbetaling, der dækker alle betalinger til anskaffelse af forsikring (afsnit 194D)
    - Enhver rente, der ikke er rente på værdipapirer, der tilfalder ikke-hjemmehørende, som ikke er en virksomhed eller en udenlandsk virksomhed (afsnit 195)
    - Betaling til ikke-hjemmehørende sportsmand, herunder atletik- eller sportsforeninger eller -institutioner. I tilfælde af en ikke-hjemmehørende sportsmand, betalinger for annoncer samt artikler om spil/sport i indien i aviser, magasiner osv. er inkluderet (afsnit 194E)
    - Betaling i forbindelse med indbetalinger under NSS \[National Savings Scheme\] (afsnit 194EE)
    - Betaling på grund af tilbagekøb af enheder af fælles fond eller UTI (Section 194F)
    - Betaling for provision eller kurtage (afsnit 194H)
    - Betaling af leje (afsnit 194I)
    - Betaling af gebyrer for professionelle eller tekniske tjenester (afsnit 194J)
    - Provision til lagerførere, distributører, indkøbere og sælgere af lotteribilletter, herunder vederlag eller præmie for sådanne kuponer (afsnit 194G)
    - Indtægt fra enheder, der er købt i fremmed valuta eller langsigtet kapitalgevinst som følge af overførsel af sådanne enheder, der er købt i fremmed valuta (afsnit 196B)
    - Betaling af indtægt til ikke-hjemmehørende i forbindelse med renter eller udbytte på obligationer og aktier (afsnit 196C)

Kildeskatten beregnes på indkøb, salg, salgsreturneringer, kreditnotaer, anskaffelse af anlægsaktiver, forudbetalinger, forudbetalinger, egenveksler, arbejde og interne transaktioner.

> [!NOTE]
> I det aktuelle indiske skattescenarie beregner kildeskat ikke for salgstransaktioner. Systemet inkluderer mulighed for at beregne skatterefusion for salgstransaktioner, især for interne transaktioner.

Beregningen af kildeskat tager altid højde for den grænseværdi og tærskel for fritagelse, der er defineret for skattekomponenten.

Den periodiske skatteudligningsproces skal køres, og skattebetalingerne skal udlignes med skattemyndighedskreditorer.

Certifikatnumrene og -datoerne for skattecertifikater, der modtages fra kreditorer eller debitorer, kan registreres og opdateres. Desuden kan kvartalsopgørelser for Formular 26Q og Formular 27Q samt Formular 16A-certifikatet for kildeskat genereres i Finans.

## <a name="setting-up-and-working-with-tds"></a>Opsætte og arbejde med kildeskat

Her er en oversigt over processen for opsætning af og arbejde med kildeskat:

1. **Opsætning af kildeskat:**

    - Opsætning af parametre:

        - I Finansparametre skal du aktivere de parametre, der er relateret til kildeskat.
        - Angiv nummerserien for betalinger af A-skat i Finansparametre.
        - Angiv parametre i Kreditor og Debitor.

    - Grundlæggende opsætning:

        - Angiv skatteregistreringsnumre for en virksomhed, debitorer og kreditorer.
        - Konfigurer skattekomponentgrupper.
        - Konfigurer skattekomponenter, knyt skattekomponentgrupper til dem, og definer grænseværdien og tærsklen for fritagelse for dem.
        - Angiv skattemyndigheder.
        - Angiv skatteudligningsperioder.
        - Angiv kildeskattekoder, og knyt skattekomponenter til dem.
        - Angiv kildeskattegrupper, og knyt kildeskattekoder til dem.
        - I formeldesigneren skal du definere en formel for at beregne kildeskat for en kildeskattegruppe.
        - Registrer certifikatnumre for skattekoncession.

    - Opsætning af finanskonti og virksomheder:

        - Konfigurere finanskonti for kildeskat i forhold til kreditorer og debitorer.
        - Angiv et kontonummer for skattefradrag og -opkrævning (ITRA) og en fradragskategori for virksomheden.

    - Anden opsætning:

        - Konfigurer en betalingsplan, der omfatter skattefordeling.
        - Angiv en betalingsgebyrtype for betalinger til skattemyndighed.
        - Konfigurer oplysninger om kildeskattegrupper, permanente kontonumre (PAN – Permanent Account Number) og skattekontonumre for kreditorer og debitorer.

2. **Beregning af kildeskat i transaktioner:**

    - Fakturaer og betalinger
    - Egenveksler
    - Forudbetalinger
    - Forudbetalinger

3. **Skatteudligning:**

    - Periodisk skatteudligningsproces
    - Udligning af skattebetalinger til skattemyndighedskreditorer og generering af skatteopgørelse

4. **Skatteforespørgsler, -opgørelser og -certifikat:**

    - Registrer og opdater skattecertifikatnumre og -datoer.
    - Generer en skatteforespørgsel og en bogført skatteforespørgsel.
    - Generer Formular 27A, Formular 26Q og Formular 27Q for kildeskat og elektroniske kvartalsopgørelser af kildeskat.
    - Generer et skattecerfikat for Formular 16A.
