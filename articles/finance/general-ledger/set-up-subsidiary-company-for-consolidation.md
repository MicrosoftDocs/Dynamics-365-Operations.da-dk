---
title: Konfigurere en juridisk datterselskabsenhed til konsolidering
description: Dette emne indeholder en forklaring på, hvordan du kan arbejde med kontoplaner for konsoliderede regnskaber.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: bfa913ca1778391ce0f5a1b2fdf6e5828b30cb66
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724467"
---
# <a name="set-up-a-subsidiary-legal-entity-for-consolidation"></a>Konfigurere en juridisk datterselskabsenhed til konsolidering

[!include [banner](../includes/banner.md)]

Den metode, du bruger til at forberede et datterselskabs konti til konsolidering, afhænger delvist af det omfang, som strukturen i kontoplanen i datterselskabets juridiske enhed afspejler kontoplanen i den konsoliderede juridiske enhed.

Før du starter en konsolidering som en del af slutningen af en periode, skal du fuldføre de forberedende aktiviteter for lukningen af perioden, men du skal ikke lukke datterselskabets konti, før konsolideringen er gennemført. Du kan finde flere oplysninger om lukningen af perioden i [Lukke Finans ved periodeafslutning](close-general-ledger-at-period-end.md) og [Lukke regnskabsåret](tasks/close-fiscal-year.md).

> [!NOTE]
>  Det anbefales, at du bruger Management Reporter til Microsoft Dynamics 365 Finance til at kombinere de økonomiske resultater for flere juridiske enheder i et konsolideret format. Du kan bruge Management Reporter til at oprette konsoliderede regnskabsrapporter på tværs af juridiske enheder, bruge Excel til at importere konsolideringsdata fra andre kilder og oversætte beløb til et vilkårligt antal rapporteringsvalutaer uden at skulle køre konsolideringsprocessen i Dynamics 365 Finance.

## <a name="map-subsidiary-main-accounts-to-consolidated-main-accounts"></a>Knytte hovedkonti i datterselskaber til konsoliderede hovedkonti

Hvis kontoplanen i datterselskabets juridiske enhed ikke følger af kontoplanen i den konsoliderede juridiske enhed, kan du knytte de hovedkontiene i datterselskabet til hovedkontiene i den konsoliderede juridiske enhed.

1. I *datterselskabets juridiske enhed* skal du gå til **Finans \> Opsætning** \> **Kontoplan \> Finansopsætning**.
2. Vælg en kontoplan. Vælg en hovedkonto i oversigtspanelet **Hovedkonti**, og vælg derefter **Rediger**.
3. Vælg hver hovedkonto i datterselskabet, der skal knyttes til en konsolideret hovedkonto. I oversigtspanelet **Generelt** i feltet **Konsolideret konto** skal du angive den konto, hvor saldoen eller transaktionerne fra den valgte hovedkonto i datterselskabet skal overføres til i den konsoliderede juridiske enhed. Du kan angive samme konsoliderede hovedkonto til flere konti i datterselskabet.

    > [!NOTE]
    > Hvis de vigtigste hovedkonti i datterselskabet, der er tilknyttet, afviger fra de vigtigste hovedkontotyper i den konsoliderede juridiske enhed, overskrives værdierne af konti, der har hovedkontotypen **Total**, under konsolidering.

4. Forbered rapporter og regnskaber til den konsoliderede juridiske enhed, der er baseret på økonomiske dimensioner. Benyt følgende fremgangsmåde for at knytte de økonomiske dimensioner, der bruges i datterselskabskontiene, til de økonomiske dimensioner i den konsoliderede juridiske enhed:

    1. I *datterselskabets juridiske enhed* skal du gå til **Finans \> Opsætning \> Økonomiske dimensioner \> Økonomiske dimensioner**, vælge en økonomisk dimension og derefter **Økonomiske dimensionsværdier**.
    2. Vælg den finansielle dimensionsværdi, der skal knyttes til finansiel dimensionsværdi i den konsoliderede juridiske enhed.
    3. I oversigtspanelet **Generelt** i feltet **Gruppedimension** skal du angive den finansielle dimension i den konsoliderede juridiske enhed. Under konsolidering tildeles denne økonomiske dimension til transaktioner og saldi, der bruger den valgte finansielle dimension i datterselskabets juridiske enhed. De økonomiske dimensioner, du angiver her, skal bruges i den konsoliderede juridiske enhed. Du kan tildele den økonomiske dimension, der bruges som gruppen af økonomiske dimensioner, til flere datterselskabers økonomiske dimensioner.

5. Hvis du udfører en onlinekonsolidering, skal du udføre følgende trin for at sikre, at overførslerne finder sted som planlagt:

    1. I den *konsoliderede juriske enhed* skal du gå til **Finans \> Periodisk \> Konsolider \> Konsolider \[Eksporter til\]** for at åbne siden **Konsolider \[Online\]**.
    2. Markér afkrydsningsfeltet **Brug konsolideringskonto** på fanen **Kriterie**.
    3. Vælg de relevante økonomiske dimensioner under fanen **Økonomiske dimensioner**.
    4. For hver økonomisk dimension, du vælger, skal du skrive et tal i feltet **Rækkefølge for segmenter** for at angive den rækkefølge, dimensionerne vises i.

## <a name="maintain-the-same-chart-of-accounts-in-the-subsidiary-and-consolidated-legal-entities"></a>Opretholde samme kontoplan i datterselskabet og konsoliderede juridiske enheder

Hovedkontiene i datterselskabets juridiske enhed kan have de samme kontonumre og den samme struktur i kontoplanen som hovedkontiene i den konsoliderede juridiske enhed. I dette tilfælde kan du ikke tilknytte hovedkontiene i datterselskabet manuelt til hovedkontiene i den konsoliderede juridiske enhed.

Før du starter konsolideringen, skal du benytte følgende fremgangsmåde.

1. I den *konsoliderede juriske enhed* skal du gå til **Finans \> Periodisk \> Konsolider \> Konsolider \[Eksporter til\]** for at åbne siden **Konsolider \[Online\]**.
2. Markér afkrydsningsfeltet **Brug konsolideringskonto**. Under konsolidering overføres transaktioner og saldi automatisk til den korrekte konto.

> [!NOTE]
> Hvis kontonumrene ikke stemmer overens, standses konsolideringen, og du får vist en meddelelse.

## <a name="create-a-chart-of-accounts-for-the-consolidated-legal-entity-based-on-an-existing-chart-of-accounts"></a>Oprette en kontoplan for den konsoliderede juridiske enhed, baseret på en eksisterende kontoplan

Du kan udføre konsolideringen, selvom en kontoplan ikke allerede er oprettet i den konsoliderede juridiske enhed.

- Hvis du har planlagt en kontostruktur til brug i den konsoliderede juridiske enhed, kan du knytte kontiene i datterselskabet til denne struktur.
- Hvis du ikke knytter datterselskabets konti, oprettes kontiene i den konsoliderede juridiske enhed automatisk, når datterselskabets data overføres til den konsoliderede juridiske enhed. Disse konti er baseret på hovedkontoen. Efterfølgende data er akkumuleret i konti i den konsoliderede juridiske enhed, der har det samme kontonummer som datterselskabets konti.

Uanset om du har tilknyttet konti, skal du fjerne markeringen i afkrydsningsfeltet **Brug konsolideringskonto** på siden **Konsolider**, før du kører denne type konsolidering.

> [!NOTE]
> Du kan anvende denne metode til at oprette en kontoplan i den konsoliderede juridiske enhed fra kontoplanen i en af datterselskabernes juridiske enheder. (Du kan finde flere oplysninger i [Konsolideringskontogrupper og yderligere](../budgeting/consolidation-account-groups-consolidation-accounts.md)konsolideringskonti.) Tildel derefter et relevant princip for konsolideringsomregning til hver konsolideret hovedkonto, og kør konsolideringen for alle juridiske enheder for datterselskabet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
