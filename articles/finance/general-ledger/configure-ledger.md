---
title: Konfigurering af Finans
description: Dette emne indeholder oplysninger om konfiguration af Finans for hver juridisk enhed. Det indeholder oplysninger om, hvordan du vælger valutaer, regnskabskalendere, kontoplaner og de kontostrukturer, der skal bruges sammen med de enkelte juridiske enheder.
author: kweekley
ms.date: 09/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Ledger
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-09
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 38c4364c47915cc0019cb6b3d471d3e60d413bf0
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711542"
---
# <a name="configure-ledgers"></a>Konfigurering af Finans

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om konfiguration af Finans for hver juridisk enhed. Det indeholder oplysninger om, hvordan du vælger valutaer, regnskabskalendere, kontoplaner og de kontostrukturer, der skal bruges sammen med de enkelte juridiske enheder.

## <a name="selecting-the-chart-of-accounts"></a>Valg af kontoplan

For hver juridiske enhed i Microsoft Dynamics 365 Finance skal der konfigureres oplysninger om Finans. På siden **Finans** kan du vælge den kontoplan og de kontostrukturer, der skal bruges til den valgte juridiske enhed. Du kan dele din kontoplan og kontostrukturer ved at konfigurere siden **Finans** i hver juridisk enhed til at bruge den samme kontoplan og de samme kontostrukturer. Du kan også dele en del af konfigurationen i de enkelte juridiske enheder og angive specifikke konfigurationer i de enkelte juridiske enheder.

Hvis de juridiske enheder skal have forskellige kontoplaner eller forskellige regnskabsstrukturer, kan funktionen til tilsidesættelse af den juridiske enhed være nyttig. Ved at bruge samme kontoplan og kontostrukturer for flere juridiske enheder og derefter administrere eventuelle undtagelser ved tilsidesættelse af juridisk enheder, kan du forenkle vedligeholdelsen over tid.

Hvis du vil konfigurere kontoplanen for en juridisk enhed, skal du gå til **Finans \> Opsætning af Finans \> Finans**. På siden **Finans** skal du vælge **Kontoplan** og derefter vælge den kontoplan, du vil bruge, på listen. Bemærk, at kontoplanen ikke kan ændres, når du har valgt en værdi og bogført posteringer i den juridiske enhed.

Du kan finde flere oplysninger om, hvordan du planlægger og konfigurerer kontoplanen og hovedkonti, i [Planlægning af kontoplanen](plan-chart-of-accounts.md).

## <a name="selecting-account-structures"></a>Valg af kontostrukturer

Hver juridiske enhed i Dynamics 365 Finance kan konfigureres til at bruge en eller flere kontostrukturer. Hver kontostruktur definerer de økonomiske dimensioner og kombinationer af hovedkonti og økonomiske dimensioner, der tillades, når posteringerne bogføres. Du kan bruge de samme kontostrukturer i mere end én juridisk enhed.

Bemærk, at hvis du har flere kontostrukturer, kan du kun vælge kontostrukturer, der ikke har overlappende kombinationer af hovedkonti og økonomiske dimensioner. En af dine kontostrukturer er f. eks. konfigureret til at tilføje en afdeling for hovedkonti mellem 1000 og 1999. I en anden kontostruktur har du tilføjet en afdeling for økonomisk dimension for hovedkonti, der begynder med 1. I dette tilfælde er det kun en af kontostrukturerne, der kan tilføjes i den samme juridiske enhed.

Hvis du vil konfigurere kontostrukturer for Finans på siden **Finans**, skal du vælge oversigtspanelet **Kontostrukturer**, **Tilføj** og vælge en kontostruktur på listen. Angiv derefter **Vælg**. Det kan tage et par minutter, før kontostrukturer tilføjes og gemmes. Bemærk, at de kontostrukturer, du vælger, skal være aktive. Ellers vil oplysningerne om kontostrukturer ikke være gældende i de juridiske enheder, hvor de er knyttet til hinanden.

Hvis du vil fjerne en kontostruktur, skal du på siden **Finans** på oversigtspanelet **Kontostrukturer** vælge **Fjern**. Bemærk, at hvis du fjerner en kontostruktur fra Finans, fjerner du ikke de posteringer, der er bogført, ved hjælp af konfigurationen af den pågældende kontostruktur.

Du kan finde flere oplysninger om, hvordan du konfigurerer kontostrukturer, i [Konfigurere kontostrukturer](configure-account-structures.md).

## <a name="configuring-calendars-for-the-ledger"></a>Konfigurere kalendere til Finans

En anden del af Finans er regnskabskalenderen. Der skal vælges et regnskabsår for hver juridisk enhed. Du kan bruge de samme regnskabskalendere i mere end én juridisk enhed. Når du vælger en regnskabskalender til Finans, laves der en kopi. Denne kopi kaldes Finans-kalenderen. I Finans-kalenderen kan du vælge status for perioderne og modulerne i hver periode.

Hvis du vil have adgang til og opdatere kalenderen for den valgte juridiske enhed, skal du siden **Finans** vælge **Finans-kalender** i handlingsruden.

Hvis du vil angive kalenderen, skal du vælge **Regnskabskalendere** og derefter vælge kalenderen på listen. Hvis du ændrer regnskabskalenderen, efter at posteringerne er bogført i den juridiske enhed, skal du vælge **Genberegning af Finans-perioder**. Du kan derefter opdatere Finans-saldi for perioderne i kalenderen i den dialogboks, der vises. Det anbefales, at du kører processen **Genberegning af finansperioder** i tilstanden **Batch**, og at du kører den, når der håndteres processer, der ikke er kritiske, i systemet. Afhængigt af antallet af posteringer og kombinationer af økonomiske dimensioner, kan denne proces tage noget tid.

Hvis der ikke er valgt en regnskabskalender for en juridisk enhed, modtager du en fejlmeddelelse, når du forsøger at bogføre en transaktion i den pågældende juridiske enhed.

Yderligere oplysninger finder du under [Regnskabskalendere, regnskabsår og perioder](../budgeting/fiscal-calendars-fiscal-years-periods.md).

## <a name="using-a-balancing-financial-dimension"></a>Brug af økonomisk udligningsdimension

Når du har valgt kontoplanen og tilføjet en eller flere kontostrukturer, kan du vælge at bruge en enkelt økonomisk dimension som økonomisk udligningsdimension. Den dimension, du vælger, skal findes i alle kontostrukturer. Den skal også afstemmes i alle regnskabsposter. Debet- og kreditbeløb skal med andre ord være ens for hovedkontoen og den økonomiske udligningsdimension. Systemet opretter automatisk posteringer for at afstemme posterne på baggrund af de hovedkonti, der er angivet i felterne **Internt mellem enheder - kredit** og **Internt mellem enheder - debet** på siden **Konti til automatisk postering**.

Yderligere oplysninger om modpostering finder du i [Afstemte kladder til internt regnskab mellem enheder](example-balanced-journals-interunit-accounting.md).

## <a name="configuring-currencies-for-the-ledger"></a>Konfigurering af valutaer til Finans

Siden **Finans** bruges også til at kontrollere og definere de valutaer, der skal bruges, når posteringerne bogføres i Finans. Du skal angive regnskabsvalutaen, som er den valuta, der skal bruges i kolonnen **Regnskabsvaluta** i Finans på alle bilag. Derudover kan du vælge en anden valuta i kolonne **Rapporteringsvaluta**. Hvis du vælger en rapporteringsvaluta, vil alle posteringer blive registreret i den pågældende valuta i kolonnen **Rapporteringsvaluta** i Finans på alle bilag.

Hvis posteringer bogføres i en anden valuta, konverterer systemet automatisk transaktionsbeløbet fra transaktionsvalutaen til regnskabsvalutaen og rapporteringsvalutaen i bilaget. På siden **Finans** i feltet **Regnskabsvaluta - valutakurstype** skal du vælge den type valuta, der er konfigureret for de valutakurser, der skal bruges til at konvertere værdier fra transaktionsvalutaen til regnskabsvalutaen på et bilag. Hvis du har valgt en rapporteringsvaluta, skal du også angive feltet **Regnskabsvaluta - valutakurstype** for at angive den valutakurs, der skal bruges til omregning af værdier fra transaktionsvalutaen til rapporteringsvalutaen på et bilag.

Hvis du bruger budgetteringsfunktionalitet, kan du også angive feltet **Budgetvalutakurstype** til at angive den valutakurs, der skal bruges til konvertering af budgettransaktioner fra én valuta til en anden.

Hvis du bruger to valutaer, eller hvis du bruger en enkelt valuta, men posteringer bogføres i en anden valuta, skal du konfigurere oversigtpanelet **Konti til valutaregulering** på siden **Finans**. I dette oversigtspanel kan du definere standardrealiserede og ikke-realiserede gevinst- og tabskonti, der skal bruges som standard, når der bogføres posteringer, hvis der ikke er angivet en konto på siden **Valutaværdireguleringskonti**. (Siden **Valutaværdireguleringskonti** bruges til at konfigurere forskellige konti til realiserede og ikke-realiserede gevinster og tab for hver valuta.)

Realiserede gevinster og tab er fortjeneste og tab, der er foretaget fra afsluttede transaktioner. De registreres i driftsregnskabet. Ikke-realiserede gevinster og tab er fortjeneste og tab, der har materialiseret sig, men posteringen er ikke fuldført. Du har med andre ord f.eks. bogført en faktura, men fakturaen er endnu ikke udlignet og betalt. Ikke-realiserede gevinster og tab registreres i balancen.

Yderligere oplysninger om hvordan du bruger to valutaer, finder du under [To valutaer](dual-currency.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
