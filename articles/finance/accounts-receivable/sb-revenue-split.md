---
title: Skabelonen til indtægtsopdeling i abonnementsfakturering
description: Denne artikel forklarer, hvordan du konfigurerer skabeloner til opdeling af omsætning for varer, der sælges som bundter.
author: JodiChristiansen
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 145ca6e6f0673a5a09fe9a23cf5e163421617fd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904753"
---
# <a name="revenue-split-templates-in-subscription-billing"></a>Skabelonen til indtægtsopdeling i abonnementsfakturering

Du kan bruge siden **Skabelon for opdeling af omsætning** til at oprette skabeloner til opdeling af omsætning. Indtægtssplit består af en overordnet vare, der har underordnede varer. Denne varetype sælges ofte til kunderne som en enkelt vare eller et bundt.

Et computerelement kan f.eks. oprettes på følgende måde:

- **Overordnet vare:** Abonnement Sølv
- **Linje (under) elementer:**

    - Support
    - Vedligeholdelse
    - Licens

Når du opretter en overordnet vare, skal du huske følgende begrænsninger:

- En vare kan kun angives som overordnet vare én gang.
- Den overordnede vare kan vælges som en underordnet vare i samme skabelon.
- En gyldig skabelon kræver mindst én underordnet vare.
- En vare kan angives som en underordnet vare til mere end én bundtvare.
- Hver overordnet-underordnet relation skal være entydig.

## <a name="create-a-parent-item-that-has-child-items"></a>Oprette en overordnet vare, der indeholder underordnede varer

Hvis du vil oprette en indkøbsordre, der indeholder betingelser for betal ved betaling, skal du følge disse trin.

1. Vælg **Ny** på siden **Indtægtsopdelt skabelon**.
1. Vælg en overordnet vare i feltet **Overordnet vare**. Feltet **Variantnummer** opdateres automatisk. Du kan ændre værdien efter behov.
1. Vælg en fordelingsmetode i feltet **Fordelingsmetode**.
1. Vælg **Tilføj** på listen **Komponentvarer** for at tilføje underordnede varer.
1. Hvis du har valgt **Procent** som **fordelingsmetode**, skal du angive fordelingsprocenten for hver linje i feltet **Procent**.

    - Hvis du har valgt **Lige beløb** i feltet **Fordelingsmetode**, opdateres feltet **procent** automatisk, så hver vare har en tilsvarende procent.
    - Hvis du valgte **Variabelt beløb**, **Nul-overordnet beløb** eller **Nul-beløb** i feltet **Fordelingsmetode**, forbliver værdien i feltet **Procent** **0** (nul) og kan ikke ændres.

1. Vælg **Gem**.

## <a name="fields"></a>Felter

Siden **Skabelon til indtægtsopdeling** indeholder følgende felter.

| Felt | Beskrivende tekst |
|-------|-------------|
| Overordnet vare | Vælg et varenummer. Denne vare bliver den overordnede vare til den bundtvare, du opretter. |
| Produktnavn | Produktnavnet. |
| Fordelingsmetode | <p>Vælg fordelingsmetoden:</p><ul><li>**Lige stort beløb** – Fordelingsprocenterne beregnes automatisk og fordeles ligeligt mellem alle varerne i skabelonen.</li><li>**Procent** – Der kan angives et procentbeløb til fordelingen. Summen af alle procenterne skal være 100.</li><li>**Variabelt beløb** – Underordnede varer, der tilføjes, har et nettobeløb på 0 (nul). Prisen på de underordnede varer skal angives på posteringsniveau.</li><li>**Nulbeløb** – Den overordnede vare bevarer enhedsprisen og nettobeløbet. Alle underordnede varer har et nettobeløb på 0 (nul).</li><li>**Nul som overordnet beløb** – Den overordnede vare har et fast nettobeløb på 0 (nul). Alle underordnede varer behandles som standardvarer. Der udføres ingen validering for at kontrollere, at summen af underordnede varebeløb er lig med det overordnede varebeløb.</li></ul> |
| **Komponentvarer** | |
| Komponentvare | Vælg et varenummer. Denne vare er en underordnet vare. |
| Variantnummer | Vælg variantnummeret for varen. |
| Produktnavn | Produktnavnet. |
| Procentdel | <p>Fordelingsprocenten for milestone.</p><ul><li>Hvis feltet **Fordelingsmetode** er angivet til **Procent**, kan du angive procenten for linjen.</li><li>Hvis feltet **Fordelingsmetode** er angivet til **Lige stort beløb**, deles procenten automatisk, så hver vare i skabelonen har lige store procentdele.</li><li>Hvis feltet **Fordelingsmetode** er angivet til **Variabelt beløb**, **Nul overordnet beløb** eller **Nulbeløb**, er procenten 0 (nul) og kan ikke redigeres.</li></ul><p>Værdien i dette felt kan være ethvert positivt tal mellem 0 (nul) og 100. Summen af alle procenterne skal være 100.</p> |
| Samlet procentdel | <p>Summen af værdier i kolonnen **Procent**.</p><ul><li>Hvis feltet **Fordelingstype** er angivet til **Lige beløb** eller **Procent**, skal de samlede procentsatser være lig med 100.</li><li>Hvis feltet **Fordelingsmetode** er angivet til **Variabelt beløb**, **Nul overordnet beløb** eller **Nulbeløb**, er den samlede procentsats 0 (nul).</li></ul> |

## <a name="revenue-split-on-a-sales-order"></a>Gebyrfordeling på en salgsordre

Hvis du vil oprette en salgsordre, der indeholder en vare, der er konfigureret til opdeling af omsætning, skal du følge disse trin.

1. Opret en salgsordre på siden **Salgsordrer**.
2. Marker afkrydsningsfeltet **Indtægtssplit** på linjen for hver vare, der er konfigureret til indtægtssplitning. Den pågældende vare bliver den overordnede vare. Hvis skabelonen allerede er oprettet, vises de underordnede elementer automatisk på listen.
3. Hvis du vil tilføje flere underordnede varer, skal du vælge **Tilføj opdelt omsætning** og vælge det underordnede element, der skal tilføjes.
4. Gem ordren.

## <a name="revenue-split-with-billing-schedules"></a>Omsætningsopdelt med faktureringsplaner

Hvis du vil oprette en faktureringsplan, der indeholder en vare, der er konfigureret til opdeling af omsætning, skal du følge disse trin.

1. Opret en faktureringsplan på siden **Alle/aktive faktureringsplaner**
2. Marker afkrydsningsfeltet **Indtægtssplit** på linjen for hver vare, der er konfigureret til indtægtssplitning. Den pågældende vare bliver den overordnede vare. Hvis skabelonen allerede er oprettet, vises de underordnede elementer automatisk på listen.
3. Hvis du vil tilføje flere underordnede varer, skal du vælge **Tilføj opdelt omsætning** og vælge det underordnede element, der skal tilføjes.
4. Fortsæt med trinnene til arbejde med faktureringsplanen.

> [!NOTE]
> Hvis indstillingen **Opret automatisk opdeling af omsætning** er angivet til **Ja** på siden **Faktureringsparametre for tilbagevendende kontrakter**, udføres følgende handlinger:
>
> - Afkrydsningsfeltet **Splitning af omsætning** markeres automatisk på faktureringsplanlinjen, hvis varen er konfigureret som en opdelt omsætningsvare.
> - De underordnede varer angives automatisk på salgsordren eller faktureringsplanlinjen.
>
> Hvis indstillingen **Opret automatisk opdeling af omsætning** er angivet til **Nej**, er funktionaliteten som forklaret tidligere.

## <a name="additional-revenue-split-information"></a>Yderligere oplysninger om indtægtsopdeling

Når du tilføjer en vare, der er en del af en indtægtsopdeling, skal du notere følgende oplysninger: 

- Det overordnede beløb kan ikke udskydes.
- Værdierne for startdato, slutdato, antal, enhed, lokation og lagersted for underordnede varer er baseret på den overordnede vare. Disse værdier kan ikke ændres for de underordnede varer. Alle ændringer skal foretages af den overordnede vare. 
- Prissætningsmetoden er **Flad** og kan ikke ændres.
- Underordnede varer kan tilføjes eller fjernes.
- Overordnede og underordnede varer skal bruge samme varegruppe. 
- Underordnede varer kan have en af følgende opsætninger:

    - Felterne **Faktureringsfrekvens** og **Faktureringsintervaller** er angivet til samme værdi som den overordnede vare. 
    - Feltet **Faktureringsfrekvens** er angivet til **Én gang**. I dette tilfælde angives feltet **Faktureringsintervaller** automatisk til **1**. 

- Summen af nettobeløbene for de underordnede varer er lig med det overordnede beløb. Hvis fordelingsmetoden er **Nulbeløb**, er både summen af de underordnede varebeløb og det overordnede beløb 0 (nul). 

    > [!NOTE]
    > Hvis fordelingsmetoden er **Nul overordnet beløb** svarer summen (ikke-nul) af de underordnede varer ikke til det overordnede beløb, hvilket er 0 (nul). Denne fordelingsmetode bruges til interne formål, så medarbejderne kan se de underordnede varer. Men kunder kan kun se den overordnede vare.

- Hvis MEA-typen (aftale med flere varer) for salgsordren er **Enkelt**, oprettes den tilsvarende transaktionslinje for indtægtsfordeling af flere varer, når de overordnede og underordnede varer tilføjes. 
- Hvis fordelingsmetoden for en indtægtsfordeling er **Lige beløb**, og det overordnede beløb ændres, genberegnes beløbene for alle underordnede linjer. 
- I forbindelse med en indtægtsopdeling, hvor fordelingsmetoden er **Variabelt beløb**, forekommer følgende funktionsmåde:

    - Nettobeløbet af den overordnede vare vises i kolonnen **Overordnet beløb**. Denne værdi kan redigeres. Men enhedsprisen, nettobeløbet og rabatten er 0 (nul) og kan ikke redigeres.
    - Enhedsprisen for underordnede varer er 0 (nul). Du kan redigere enhedsprisen eller nettobeløbet. Når du redigerer én værdi, opdateres den anden værdi automatisk.

- I forbindelse med en indtægtsopdeling, hvor fordelingsmetoden er **Procent**, forekommer følgende funktionsmåde:

    - Nettobeløbet af den overordnede vare vises i kolonnen **Overordnet beløb**. Denne værdi kan redigeres. Men enhedsprisen, nettobeløbet og rabatten er 0 (nul) og kan ikke redigeres. 
    - Nettobeløbet for underordnede varer beregnes som *Procentbeløb* &times; *Procentbeløb*.

- I forbindelse med en indtægtsopdeling, hvor fordelingsmetoden er **Lige beløb**, forekommer følgende funktionsmåde:

    - Nettobeløbet af den overordnede vare vises i kolonnen **Overordnet beløb**. Denne værdi kan redigeres. Men enhedsprisen, nettobeløbet og rabatten er 0 (nul) og kan ikke redigeres. 
    - Nettobeløbet for underordnede varer beregnes ved at dividere det overordnede beløb ligeligt mellem alle underordnede varer. 
    - Hvis underordnede varer fjernes eller tilføjes, genberegnes nettobeløbet og enhedspriserne, så alle underordnede linjer har lige beløb. 
    - Hvis det overordnede beløb ikke kan deles ligeligt, kan nettobeløbet og enhedsprisen for den sidste underordnede vare være en smule større eller mindre end nettobeløbet og enhedsprisen for de andre underordnede varer. 

- I forbindelse med en indtægtsopdeling, hvor fordelingsmetoden er **Nulbeløb**, forekommer følgende funktionsmåde:

    - Enhedsprisen, nettobeløbet og rabatten kan redigeres. Det overordnede beløb er 0 (nul) og kan ikke redigeres. 
    - Værdierne for antal, enhed, lokation og lagersted for underordnede varer er baseret på den overordnede vare. Disse værdier kan ikke ændres for de underordnede varer. Alle ændringer skal foretages af den overordnede vare. 
    - Enhedsprisen og nettoprisen for underordnede varer er 0 (nul) og kan ikke redigeres. 

- I forbindelse med en indtægtsopdeling, hvor fordelingsmetoden er **Nul overordnet beløb**, forekommer følgende funktionsmåde:

    - Enhedsprisen, det overordnede beløb og og nettobeløbet for den overordnede vare er 0 (nul).
    - I en faktureringsplan vises de underordnede linjer, som om de er tilføjet manuelt, og alle værdier opdateres baseret på den valgte faktureringsplangruppe. Disse værdier kan redigeres. For underordnede varer kan du få adgang til indstillingerne **Eskalering og rabat** og **Avanceret prissætning** ved at bruge felterne **Antal angivet**, **Enhedspris**, **Rabat** og **Nettobeløb** i **Vis faktureringsoplysninger**. 
    - I en salgsordre har de underordnede linjer en rabat og rabatprocent på 0 (nul). 
    - Faktureringshyppigheden for de overordnede og underordnede varer kan ændres, og hver enkelt linje kan have en særskilt frekvens. Den overordnede vare opdateres dog automatisk, så den bruger den korteste frekvens blandt de underordnede linjer. En indtægtsopdeling har f.eks. to underordnede varer, hvoraf den ene bruger faktureringsfrekvensen **Månedlig**, og den anden bruger faktureringsfrekvensen **Årlig**. I dette tilfælde opdateres faktureringsfrekvensen for den overordnede vare til **Månedlig**.
