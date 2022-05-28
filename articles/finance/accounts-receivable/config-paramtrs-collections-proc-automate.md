---
title: Konfigurere parametre for automatisk rykkerproces
description: Dette emne indeholder en beskrivelse af de parametre, der påvirker automatiserede rykkerprocesser, og vejledning i, hvordan du kan indstille dem, så den automatiserede proces afspejler dine hensigter og forventninger.
author: JodiChristiansen
ms.date: 08/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: e7a7e048a371fc90456368206b91c29c4b1264d5
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734390"
---
# <a name="configure-parameters-for-collection-process-automation"></a>Konfigurere parametre for automatisk rykkerproces

[!include [banner](../includes/banner.md)]

Dette emne indeholder en beskrivelse af de parametre, der påvirker automatiserede rykkerprocesser, og vejledning i, hvordan du kan indstille dem, så den automatiserede proces afspejler dine hensigter og forventninger. Yderligere oplysninger om, hvordan du automatiserer rykkerprocesser, finder du i [Automatiseret opkrævningsproces](collections-process-automate.md).

## <a name="general"></a>Almindelig
Angiv et antal i **Procentvis af kunder pr. batchopgave** for at bestemme antallet af batchopgaver pr. automatiseringsproces. Indstil **Bogfør rykkerbreve automatisk** til **Ja**, så rykkerhandlingstypen bogfører rykkeren under automatisering. Angiv **Opret aktiviteter for automatisering** til **Ja**, hvis du vil oprette og lukke aktiviteter for handlingstyper, der ikke er aktivitet, for at få vist alle automatiske trin, der er foretaget for en konto. Definer det antal dage, rykkerhistorikken skal gemmes, i **Opbevaringsdage for automatiseret rykkerproces**. Når en faktura når sidste trin i rykkerprocessen, bruges den ikke til at oprette handlingstyper for fremtidig procesautomatisering, hvis **Udelad faktura, når det sidste procestrin er aktiveret** er angivet til **Ja**. Den næstældste faktura er bestemmende for næste trin i proces-automatiseringen for at sikre, at automatiseringshandlingerne for rykkerprocessen fortsætter. 

## <a name="payment-predictions"></a>Betalingsforudsigelser
Fra og med version 10.0.21, forudsiger debitorbetalingen i Økonomisk indsigt, om en faktura betales til tiden, for sent eller meget sent. Du kan konfigurere hver af disse kategorier i Økonomisk indsigt. Hvis det forventes, at fakturaerne betales for sent, er det vigtigt at starte rykkerprocessen, før fakturaen forfalder. Disse forudsigelser kan bruges til at oprette rykkeraktiviteter, når automatisering af rykkerprocessen køres. Angiv **Aktivér forudsigelser om betalinger** til **Ja**, hvis du vil bruge forudsigelser ved debitorbetaling til at oprette rykkeraktiviteter baseret på sandsynligheden for, at fakturaen betales for sent. 

Du kan finde flere oplysninger om forudsigelser af debitorbetaling og Økonomisk indsigt under [Forudsigelser om debitorbetalinger](payment-insights-overview.md).

Når modellen til forudsigelser om debitorbetaling køres, tildeles en procentdel til forudsigelsen af, at fakturaen betales til tiden, for sent eller meget sent. Du kan bruge disse oplysninger til automatisk at starte rykkeraktiviteter ved hjælp af automatisering af rykkerprocessen i tilfælde, hvor forsinket betaling forventes. Du kan få vist disse procentsatser på siderne **Betalingsforudsigelser pr. debitor** eller **Betalingsforudsigelser pr. transaktion** under **Kredit og rykkere > Rykkere**. 

Hvis den gennemsnitlige betalingsforudsigelse for en debitorfaktura er mindre end benchmark-procenten, oprettes der ingen aktivitet. Hvis fakturaforudsigelsen er større end eller lig med benchmark-procenten, oprettes der én aktivitet pr. debitor. Ved **Forudsigelse: Forsinket** skal du angive **Benchmark-procent** for, hvornår automatisering af rykkerproces skal oprette rykkeraktiviteter. Dette er en samlet værdi af både forsinket og meget forsinket. Vælg en **Forretningsdokumentskabelon**, der skal bruges til den oprettede aktivitet, eller opret en ny. Denne identificerer **Type**, **Formål** og **Dage indtil aktiviteten er lukket**. Angiv eventuelle **Noter**, der vil være standardbeskrivelsen, når aktiviteten oprettes. Ved **Forudsigelse: Meget forsinket** skal du angive **Benchmark-procent** for, hvornår automatisering af rykkerproces skal oprette rykkeraktiviteter for en debitor, der forventes at betale meget forsinket. Vælg en **Forretningsdokumentskabelon**, der skal bruges til den oprettede aktivitet. Denne identificerer **Type**, **Formål** og **Dage indtil aktiviteten er lukket**. Angiv eventuelle **Noter**, der vil være standardbeskrivelsen, når aktiviteten oprettes. 

### <a name="example"></a>Eksempel
Hvis den forsinkede benchmark-procent angives til 60 %. Når forudsigelser om debitorbetaling køres for hver faktura, tildeles en procentdel til forudsigelsen af, at fakturaen betales til tiden, forsinket eller meget forsinket. Hvis betalingen forudsiger, at fakturaen betales for sent, er 59 % eller mindre, oprettes der ingen rykkeraktivitet for fakturaen af den automatiserede rykkerproces. Hvis forudsigelsen af debitorbetalingen for en faktura er større end eller lig med 60 %, oprettes der en rykkeraktivitet under automatisering af rykkerprocessen. 

> [!NOTE]
> Den meget forsinkede forudsigelse evalueres før den forsinkede forudsigelse, fordi meget forsinket inkluderer fakturaer, der forventes at blive betalt for sent. Rykkerprocessen genererer kun én aktivitet, hvis fakturaen både falder for sent og meget sent. I dette tilfælde bruger systemet meget forsinket-aktiviteten og forretningsdokumentet, fordi meget forsinket prioriteres højere. Eventuelle andre handlinger, der allerede er genereret, genereres ikke en gang til.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
