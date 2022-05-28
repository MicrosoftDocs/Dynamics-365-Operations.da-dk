---
title: Forespørgsel på likviditet
description: Dette emne indeholder oplysninger om, hvordan du fastlægger den tilsvarende likviditet for økonomiske dimensionssæt, der indeholder selvafstemmende dimensioner.
author: velofog
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.search.industry: public sector
ms.author: twheeloc
ms.search.validFrom: 2019-10-24
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 521e8eefd29c312d4bfc8294508349ff507b0c98
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735596"
---
# <a name="cash-position-inquiry"></a>Forespørgsel på likviditet
[!include [banner](../includes/banner.md)]

Med forespørgslen **Likviditet** kan du fastlægge den tilsvarende likviditet for økonomiske dimensionssæt, der indeholder selvafstemmende dimensioner. I forespørgslen vises startkassesaldoen og resultatet af tilførte kasseboner, subtraktion af kontante udbetalinger og subtraktion af overførsler mellem fonde for at komme til en slutsaldo. Derefter trækkes de generelle budgetreservationer, behæftelser eller budgetreservationer fra slutsaldoen for at få en ikke-behæftet saldo.

Denne forespørgsel er entydig, da den giver brugerne mulighed for at tilpasse terminologien for kolonnenavne og de hovedkonti, der bruges til at aflede beløbene for kolonnerne. På siden **Likviditetsparametre** er de kolonner, der vises i forespørgslen, nummereret startende med kolonnen længst til venstre som kolonne ét.

## <a name="cash-position-inquiry-setup"></a>Opsætning af forespørgsel på likviditet

1. Gå til **Finans** > **Opsætning Finans** > **Likviditetsparametre**.
2. På siden **Likviditetsparametre** i sektionen **Kolonne ét**:

- I feltet **Kolonnenavn** skal du skrive en etiket, der skal bruges som overskrift til den første kolonne i forespørgslen (f.eks. "Startsaldo").
- I feltet **Startsaldo på hovedkonti** skal du vælge den eller de konti, du vil referere til i forbindelse med forespørgsler på startsaldoen.

3. I sektionen **Kolonne to**: 

- Angiv en etiket til den anden kolonne i forespørgslen (f.eks. "Indbetalinger").
- På listen **Debet- og kredit hovedkonti** skal du vælge de hovedkonti, hvorfra der kun skal bruges summen af alle debet- og kredittransaktioner for forespørgselsdataene. 

> [!NOTE]
> Forespørgslen tilføjer debet- og kreditkontiene nettobeløb plus debetbeløb og kreditbeløb fra hovedkontiene i de andre felter i gruppen.

- På listen **Kun debethovedkonti** skal du vælge de hovedkonti, hvorfra der kun skal bruges summen af alle debettransaktioner for forespørgselsdataene.
- På listen **Kun kredithovedkonti** skal du vælge de hovedkonti, hvorfra der kun skal bruges summen af alle kredittransaktioner for forespørgselsdataene.

4. I sektionerne **Kolonne tre** og **Kolonne fire**: 

- Angiv en etiket til den tredje kolonne (f.eks. "Kontante udbetalinger") og fjerde kolonne (f.eks. "Overførsler mellem fonde").
- I begge kolonner kan du angive kontonumre for debet- og kredithovedkonti, kun debethovedkonti og kun kredithovedkonti.

5. I gruppesektionen **Kolonne fem** skal du angive en etiket for den femte kolonne (f.eks. ""Slutsaldo""). 

> [!NOTE]
> Dynamics 365 Finance beregner automatisk en sum fra de konti, du har angivet, for de første fire kolonner: startsaldoen plus indbetalinger, minus kontante udbetalinger, minus overførsler mellem fonde.

6. I sektionerne **Kolonne seks** og **Kolonne syv**: 

- Angiv en etiket for kolonne seks (f.eks. Generelle budgetreservationer eller Behæftelser") og kolonne syv (f.eks. "Budgetreservationer").
- I begge kolonner kan du angive kontonumre for **Debet- og kredithovedkonti**, **Kun debethovedkonti** og **Kun kredithovedkonti**.

7. Angiv en kolonneetiket i sektionen **Kolonne otte** (f.eks. "Ikke-behæftet saldo"). 

> [!NOTE]
> Dynamics 365 Finance beregner automatisk et resultat fra de konti, du har angivet for kolonne fem til syv: slutsaldo minus behæftelser, minus budgetreservationer.

8. Klik på **Gem**.

## <a name="running-the-inquiry"></a>Kørsel af forespørgslen

1. Gå til **Finans** > **Forespørgsler og rapporter** > **Likviditet**.
2. I sektionen **Parametre**: 

- Vælg **Datointerval** som kode eller **Fra-dato** og **Til-dato**.
- Vælg **Økonomisk dimensionsopsætning**.
- Vælg **Beregn saldi** for at køre forespørgslen.

Valgfri: 

- Indstil **Undertryk konti med ene nuller** til **Ja** for at udelukke konti, der kun har nul saldi, fra forespørgslen.
- Indstil **Vis segmenter i separate kolonner** til **Ja** for at få vist kontonavnene for hver dimension som separate kolonner i gitteret.
- Hvis du vil filtrere værdierne for en bestemt dimension, skal du vælge de ønskede dimensioner i felterne under feltet **Økonomiske dimensionsopsætninger**. De valg, du skal foretage, afhænger af, hvilken økonomisk dimensionsopsætning du har valgt.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
