---
title: Genopfyldningsstrategier
description: Dette emne indeholder oplysninger om genopfyldningsstrategier og forklarer, hvordan du kan bruge feltet Genopfyldningsstrategi på linjer til genopfyldningsskabeloner for bølgeefterspørgsel for at vælge, hvordan genopfyldning udføres.
author: mirzaab
manager: tfehr
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 9c23126c6ab15a1924b34f98d33a0661011ba8bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996092"
---
# <a name="replenishment-strategies"></a>Genopfyldningsstrategier

[!include [banner](../includes/banner.md)]

De skabeloner, der er defineret på siden **Genopfyldningsskabeloner**, omfatter skabelonlinjer til genopfyldning af bølgeefterspørgsel, hvor du kan vælge, hvordan genopfyldning udføres. Hver linje indeholder nu feltet **Genopfyldningsstrategi**.

Strategien *Bølgebehovsantal* er standardstrategien. Det er den genopfyldningsstrategi, der blev brugt før introduktionen af feltet **Genopfyldningsstrategi**. Den bruger lokationsvejledninger for genopfyldning til at finde lokationer, der kan genopfyldes. Disse lokationer genopfyldes derefter, indtil behovet er dækket.

Strategien *Maksimal lokationskapacitet* introducerer nogle nye funktioner. På samme måde som med strategien *Bølgebehovsantal* bruger denne strategi lokationsvejledninger for genopfyldning til at finde lokationer, der kan genopfyldes, og derefter genopfyldes disse lokationer, indtil behovet er dækket. Den adskiller sig fra strategien *Bølgebehovsantal* ved, at alle genopfyldningslokationer genopfyldes til den maksimale kapacitet, som defineres af grænser for lokationslager. Strategien *Maksimal lokationskapacitet* forsøger at oprette arbejde for at indhente det ønskede antal plus et ekstra antal til at fylde de lokationer, der genopfyldes. Men i nogle tilfælde vil det pågældende forsøg måske mislykkes. For eksempel har bulkvarelokationer muligvis ikke nok lagerbeholdning til at dække det ekstra antal. I disse tilfælde registrerer systemet fejlen og forsøger at genoprette.

Højsæson er et eksempel på en situation, hvor strategien *Maksimal lokationskapacitet* foretrækkes frem for strategien *Bølgebehovsantal*. I højsæsonen kan nogle varer blive solgt i store mængder. Derfor kan du proaktivt genopfylde de relevante plukpladser så meget som muligt for at reducere antallet af arbejds-id'er, der oprettes til genopfyldning.

> [!IMPORTANT]
> Hvis du vil kunne udnytte strategien *Maksimal lokationskapacitet* fuldt ud, skal du omdefinere lagergrænserne for de relevante lokationer. Ellers fungerer denne strategi på samme måde som strategien *Bølgebehovsantal*.

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a>Slå funktionen til genopfyldning til maksimum baseret på lagerbeholdningsgrænser

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Genopfyld til maksimum baseret på lagergrænser*

## <a name="set-up-replenishment-strategies"></a>Konfigurere genopfyldningsstrategier

Få adgang til skabelonerne ved at gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Genopfyldningsskabeloner**. I afsnittet **Oversigt** skal du vælge eller oprette en opfyldningsskabelon for bølgeefterspørgsel, hvor feltet **Genopfyldningstype** er angivet til *Bølgebehov*. Opret derefter genopfyldningsskabelonlinjerne i sektionen **Detaljer om genopfyldningsskabelon**. For hver linje i feltet **Genopfyldningsstrategi** skal du vælge den genopfyldningsstrategi, du vil bruge.

![Siden Genopfyldningsskabeloner](media/ReplenTempWaveDmdMaxLocCap.png "Siden Genopfyldningsskabeloner")

Hvis kolonnen **Genopfyldningsstrategi** ikke vises i gitteret i sektionen **Detaljer om genopfyldningsskabelon**, skal du kontrollere, at funktionen er slået til, og at den valgte genopfyldningsskabelon har genopfyldningstypen *Bølgebehov*.

> [!NOTE]
> Strategien *Bølgebehovsantal* er standardstrategien. Derfor skal du blot opdatere de linjer i genopfyldningsskabelonen, hvor du i stedet vil bruge strategien *Maksimal lokationskapacitet*.

## <a name="example-scenarios"></a>Eksempelscenarier

### <a name="example-1"></a>Eksempel 1

I dette eksempel er der kun én genopfyldningsskabelon, der kun har én genopfyldningsskabelonlinje.

Du opretter en salgsordre på 130 stk. af vare A0001. Før du frigiver ordren til lagerstedet, konfigureres lagerstedet på følgende måde:

- Der er kun én bulkvarelokation, og den har 500 stk. af den tilgængelige disponible lagerbeholdning.
- Der er tre plukpladser, der hver har en lagergrænse på 100 stk. (Husk, at der kræves lagergrænser for strategien *Maksimal lokationskapacitet*).
- Plukpladserne til genopfyldning er de samme som ved salg.
- Genopfyldningsenheden er en kasse (1 kasse = 20 stk).

På tidspunktet for ordren er den følgende disponible lagerbeholdning på salgsplukstederne:

- **Pluk-001:** 20 stk (1 kasse)
- **Pluk-002:** 0 stk
- **Pluk-003:** 0 stk

Genopfyldningsstrategien er først angivet til *Bølgebehovsantal*.

Når du har frigivet salgsordren til lagerstedet, og bølgebehandling kører for bølgen, får du følgende genopfyldningsarbejde:

- **Genopfyldningsarbejde 1:** Pluk 4 kasser fra bulkvarelokation, og placer dem i lokationspluk-001.
- **Genopfyldningsarbejde 2:** Pluk 2 kasser fra bulkvarelokation, og placer dem i lokationspluk-002.

Du får to genopfyldningsarbejds-id'er, fordi du skal genopfylde to lokationer, og læg-flere-varer-på-lager understøttes ikke.

Hvis genopfyldningsstrategien indstilles til *Maksimal lokationskapacitet*, får du følgende genopfyldningsarbejde:

- **Genopfyldningsarbejde 1:** Pluk 4 kasser fra bulkvarelokation, og placer dem i lokationspluk-001.
- **Genopfyldningsarbejde 2:** Pluk 5 kasser fra bulkvarelokation, og placer dem i lokationspluk-002.

[![Eksempel 1](media/ReplenTemp_example_1.png "Eksempel 1")](media/ReplenTemp_example_1_large.png)

### <a name="example-2"></a>Eksempel 2

Dette eksempel viser, hvad der sker, når der ikke er nok lagerbeholdning på bulkvarelokationen til at dække det ekstra antal. Det bruger samme scenario som eksempel 1, men bulkvarelokationen har 160 stk. (8 kasser).

Strategien *Bølgebehovsantal* opretter det samme arbejde, som den gjorde i eksempel 1.

Men da strategien for *Maksimal lokationskapacitet* forsøger at oprette arbejds-id'erne som i eksempel 1, kan den mislykkes. På dette tidspunkt forsøger systemet at genoprette.

Afhængigt af indstillingen af **Tillad opdeling** i lokationsvejledningen for genopfyldningspluk er der to mulige udfald:

- Hvis indstillingen **Tillad opdeling** er angivet til *Ja*, oprettes følgende genopfyldningsarbejde:

    - **Genopfyldningsarbejde 1:** Pluk 4 kasser fra bulkvarelokation, og placer dem i lokationspluk-001.
    - **Genopfyldningsarbejde 2:** Pluk 4 kasser fra bulkvarelokation, og placer dem i lokationspluk-002.

- Hvis indstillingen **Tillad opdeling** er angivet til *Nej*, oprettes følgende genopfyldningsarbejde:

    - **Genopfyldningsarbejde 1:** Pluk 4 kasser fra bulkvarelokation, og placer dem i lokationspluk-001.
    - **Genopfyldningsarbejde 2:** Pluk 2 kasser fra bulkvarelokation, og placer dem i lokationspluk-002.

Resultaterne er forskellige på grund af de oplysninger, der er tilgængelige, når du opretter arbejdet. Når **Tillad opdeling** er angivet til *Ja* i lokationsvejledningerne for genopfyldningspluk, er du sikker på, at du kan finde 160 stk. Derfor kan du oprette arbejde for det pågældende antal. Men når indstillingen **Tillad opdeling** er angivet til *Nej*, ved du ikke, at der findes 160 stk. Da det ekstra antal, du har besluttet at genopfylde, var 3 kasser, dropper du det ekstra antal og afprøver det oprindelige antal igen.

[![Eksempel 2](media/ReplenTemp_example_2.png "Eksempel 2")](media/ReplenTemp_example_2_large.png)

Hvis du vil hente maksimumantallet til genopfyldningslokationer, skal du derfor angive indstillingen **Tillad opdeling** til *Ja* i lokationsvejledningerne for genopfyldningspluk.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]