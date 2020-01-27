---
title: Konfigurer og køre forespørgslen Likviditet
description: Dette emne indeholder oplysninger om forespørgslen Likviditet. Dette forespørgslen gør det muligt for dig at fastlægge den tilsvarende likviditet for økonomiske dimensionssæt, der indeholder selvafstemmende dimensioner.
author: velofog
manager: AnnBe
ms.date: 10/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.search.industry: public sector
ms.author: v-alpavk
ms.search.validFrom: 2019-10-07
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 28d295db574080735173bed0f40037fb7d66ecad
ms.sourcegitcommit: 34395464ec80cea800b953eae49af579d436fc1b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935479"
---
# <a name="set-up-and-run-the-cash-position-inquiry"></a>Konfigurer og køre forespørgslen Likviditet
[!include [banner](../includes/banner.md)]


Dette emne indeholder oplysninger om forespørgslen Likviditet. Dette forespørgslen gør det muligt for dig at fastlægge den tilsvarende likviditet for økonomiske dimensionssæt, der indeholder selvafstemmende dimensioner. Det viser følgende elementer:

- Startsaldoen for kontantbeholdningen
- Virkningen af tilførelsen af kasseboner
- Subtraktion af kontante udbetalinger
- Subtraktion af overførsler mellem fonde for at komme til en slutsaldo
- Subtraktion af generelle budgetreservationer, behæftelser eller budgetreservationer fra slutsaldoen for at få en ikke-behæftet saldo

Denne forespørgsel adskiller sig fra andre forespørgsler, fordi du kan tilpasse terminologien for kolonnenavne og de hovedkonti, der bruges til at aflede de beløb, der fremgår af kolonnerne. På siden **Likviditetsparametre** nummereres de kolonner, der vises i forespørgslen, fortløbende fra venstre mod højre. Kolonnen yderst til venstre er **Kolonne et**.

## <a name="set-up-the-cash-position-inquiry"></a>Konfigurer forespørgslen Likviditet

1. Gå til **Finans \> Opsætning af finans \> Likviditetsparametre**.
2. På siden **Likviditetsparametre** i gruppen **Kolonne ét** skal du gøre følgende:

    - I feltet **Kolonnenavn** skal du angive en etiket for overskriften på den første kolonne i forespørgslen (f.eks. **Startsaldo**).
    - I feltet **Startsaldo på hovedkonti** skal du vælge de konti, du vil referere til i forbindelse med forespørgsler om startsaldoen.

3. Benyt følgende fremgangsmåde i gruppen **Kolonne to**:

    - Indtast en etiket for overskriften på den anden kolonne (f.eks. **Indbetalinger**).
    - På listen **Debet- og kredit hovedkonti** skal du vælge hovedkontiene, for kun at anvende summen af alle debet- og kredittransaktioner for forespørgselsdataene.
    
        Forespørgslen tilføjer nettobeløbet for debet- og kreditkontiene plus debetbeløb og kreditbeløb fra de hovedkonti, der er specificeret i de andre felter i gruppen.

    - For kun at bruge summen af alle debettransaktioner for forespørgselsdataene skal du vælge hovedkontiene på listen **Kun debethovedkonti**.
    - For kun at bruge summen af alle kredittransaktioner for forespørgselsdataene skal du vælge hovedkontiene på listen **Kun kredithovedkonti**.

4. Følg disse trin for **Kolonne tre**- og **Kolonne fire**-grupper:

    - Indtast en etiket for overskriften til den tredje kolonne (f.eks. **Kontante udbetalinger**) og den fjerde kolonne (f.eks. **Overførsler mellem fonde**).
    - For begge kolonner skal du angive de hovedkonti, du vil distribuere debet- og kreditposter til. Du skal også angive "kun debet"- og "kun kredit"-hovedkontiene.

5. I gruppen **Kolonne fem** skal du angive en etiket for overskriften for den femte kolonne (f.eks. **Slutsaldo**).

    Et resultat beregnes automatisk ud fra de konti, du har angivet i de første fire kolonner. I dette eksempel er beregningen Åbningssaldo + Kontantindbetalinger - Kontante udbetalinger - Overførsler mellem fonde.

6. Følg disse trin for **Kolonne seks**- og **Kolonne syv**-grupper:

    - Indtast en etiket for overskriften for den sjette kolonne seks (f.eks. **Generelle budgetreservationer** eller **Behæftelser**) og den syvende kolonne (f.eks. **Budgetreservationer**).
    - I begge kolonner kan du angive kontonumre for debet- og kredithovedkonti, og for kun debethovedkontiene samt kun kredithovedkontiene.

7. I gruppen **Kolonne otte** skal du angive en etiket for overskriften for den ottende kolonne (f.eks. **Ikke-behæftet saldo**).

    Et resultat beregnes automatisk ud fra de konti, du har angivet i femte til syvende kolonne. I dette eksempel er beregningen Slutsaldo - Behæftelser - Budgetreservationer.

8. Vælg **Gem**.

## <a name="run-the-cash-position-inquiry"></a>Kør forespørgslen Likviditet

1. Gå til **Finans \> Forespørgsler og rapporter \> Likviditet**.
2. Benyt følgende fremgangsmåde i afsnittet **Parametre**:

    - Vælg koden for datointervallet i feltet **Datointerval**. Alternativt kan du i felterne **Fra dato** og **Til dato** definere datointervallet.
    - Vælg det økonomiske dimensionssæt i feltet **Økonomisk dimensionssæt**.
    - Valgmulighed: Indstil **Undertryk konti med ene nuller** til **Ja** for at udelukke konti, der kun har 0 (nul) saldi, fra forespørgslen.
    - Valgmulighed: Indstil **Vis segmenter i separate kolonner** til **Ja** for at få vist kontonavnene for hver dimension som separate kolonner i gitteret.
    - Valgmulighed: For at filtrere værdierne for en bestemt dimension, skal du i felterne under feltet **Økonomiske dimensionssæt** vælge, hvilke dimensioner der skal medtages. De tilgængelige valgmuligheder varierer afhængigt af det økonomiske dimensionssæt, du har valgt.

3. Vælg **Beregn saldi** for at køre forespørgslen.
