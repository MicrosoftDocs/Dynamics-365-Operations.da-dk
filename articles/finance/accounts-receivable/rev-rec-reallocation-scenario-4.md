---
title: Omplacering af indtægtsføring - Scenarie 4
description: Dette emne behandler omplacering af et scenarie, hvor der fjernes en linje fra en eksisterende, delvist faktureret salgsordre. Dette scenario giver det samme resultat, uanset om linjen fjernes fra salgsordren eller angives til en annulleret status.
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 500c7817795448d7d9759c4ad7a1842df0a9bdc5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003274"
---
# <a name="revenue-recognition-reallocation--scenario-4"></a>Omplacering af indtægtsføring - Scenarie 4

[!include [banner](../includes/banner.md)]

Dette emne behandler omplacering af et scenarie, hvor der fjernes en linje fra en eksisterende, delvist faktureret salgsordre. Dette scenario giver det samme resultat, uanset om linjen fjernes fra salgsordren eller angives til en annulleret status.

I dette scenarie er indstillingen **Bogfør fakturakorrektioner til debitor** angivet **Nej** på fanen **Indtægtsføring** på siden **Finansparametre** (**Indtægtsføring \> Opsætning \> Finansparametre**).

[![Bogfør fakturarettelser til indstillingen Debitor som Nej](./media/37_rev-rec-scenarios.png)](./media/37_rev-rec-scenarios.png)

Der oprettes en salgsordre for kunde US\_SI\_0003. Kunden køber en bærbar computer (varenummer S0012), installationsservices (varenummer S0001) og en supportplan til en bærbar computer (varenummer S0008, "Vedvarende teknisk service"). Indtægterne for den bærbare computer og installationstjenester er straks anerkendt. Omsætningen for støtteplanen udskydes og indregnes over 12 måneder som defineret af datointervallet i kontrakten.

[![Salgsordrelinjer til den bærbare computer, installationstjenester og supportplan](./media/38_rev-rec-scenarios.png)](./media/38_rev-rec-scenarios.png)

Salgsordren er bekræftet. Da alle tre varer er konfigureret til fordeling af omsætningsprisen, beregnes omsætningsprisen, når salgsordren bekræftes. Du kan få vist den omsætning, der skal registreres på siden **Fordeling af indtægtspris** (på siden **Salgsordre** i handlingsruden under fanen **Administrer** i gruppen **Indtægtsføring** skal du vælge **Fordeling af omsætningspris**). Indtægterne for den bærbare computer vil blive bogført på indtægtskontoen i mængden af $995,84. Indtægterne for installationsservices vil også blive bogført på indtægtskonto med $314,47. Indtægterne for supportplanen vil blive bogført på en Udskudt indtægtskonto med $188,69. Summen af indtægtspriserne skal svare til summen af de linjer, der blev oprettet for at registrere fordeling af indtægtspriser ($1.499,00).

[![Fordeling af indtægtsprisside](./media/39_rev-rec-scenarios.png)](./media/39_rev-rec-scenarios.png)

Kunden faktureres for den bærbare computer og supportplanen, men ikke for installationstjenesterne. I følgende illustration vises den regnskabspost, der er bogført på fakturaen.

[![Regnskabspost for den fakturerede salgsordre](./media/40_rev-rec-scenarios.png)](./media/40_rev-rec-scenarios.png)

Regnskabsposten bogfører $1.276,94 til Debitor. Men da denne faktura er en delvis faktura, er omsætningen eller den udskudte omsætning plus skatten ikke lig med debitorbeløbet. Forskellen på $-14,47 bogføres på en konto til modposteringer af delfakturaen.

Tidsplan for indtægtsføring oprettes også.

[![Plan for indtægtsføring for den delfaktura](./media/41_rev-rec-scenarios.png)](./media/41_rev-rec-scenarios.png)

Senere beslutter kunden ikke at købe installationstjenester. Derfor fjernes denne linje fra salgsordren. Bemærk, at salgsordren ikke kan bekræftes igen, da der kun er fakturerede linjer tilbage på salgsordren.

[![Salgsordre, efter at linjen til installationstjenester er fjernet](./media/42_rev-rec-scenarios.png)](./media/42_rev-rec-scenarios.png)

Selvom salgsordren ikke kan bekræftes, kan den omfordeles. I salgsordren skal du vælge **Genalloker pris med nye ordrelinjer** for at åbne siden **Genallokering med nye ordrelinjer**. Vælg de to resterende salgsordrelinjer til denne salgsordre, og vælg derefter **Opdater genallokering**. Kolonnen **Omfordelt beløb** viser den nye omsætningspris for hver resterende salgsordrelinje.

[![Nye omsætningspriser på siden Genallokering med nye ordrelinjer](./media/43_rev-rec-scenarios.png)](./media/43_rev-rec-scenarios.png)

Vælg derefter **Forventet bilag** for at få vist regnskabsposterne.

[![Regnskabsposter på siden Forventet bilag](./media/44_rev-rec-scenarios.png)](./media/44_rev-rec-scenarios.png)

På siden **Forventet bilag** tilbageføres de sidste fem linjer i den oprindelige regnskabspost fra den bogførte faktura. De første fire linjer udgør de nye regnskabsposter, der bogføres for fakturaen. Det er vigtigt, at du forstår, at en ny faktura ikke præsenteres for kunden. Efter omfordelingen skylder debitoren stadig $1.276,94, hvilket er det beløb, der skal bogføres på Debitor i den nye regnskabspost. Den nye indtægt eller udskudt omsætning plus skat er lig $1.276,94. Du behøver derfor ikke at bogføre på kontoen til modpostering af delfakturaomsætning.

Hvis du vil fuldføre omfordelingen, skal du vælge **Proces**. Der er angivet en bogføringsdato. Når omplaceringen er fuldført, viser siden **Fordeling af omsætningspris** tildelingen af prisen for de resterende to varer.

[![Prisomfordeling for de resterende varer på siden Indtægtspristildeling](./media/45_rev-rec-scenarios.png)](./media/45_rev-rec-scenarios.png)

Planen for indtægtsføring blev også opdateret på baggrund af den nye indtægt til genallokationspris. Åbn siden **Indtægtsføringsplan** fra denne salgsordre. Tidligere var der 13 linjer for vare S0008 (der blev tildelt en plan på 12 måneder til denne vare). Der er nu 39 linjer: De 13 oprindelige planlægningslinjer, 13 linjer i tilbageførselsplanen og 13 linjer, der er baseret på den nye omsætningspris.

[![Siden Opdateret plan for indtægtsføring med 39 linjer for varen S0008](./media/46_rev-rec-scenarios.png)](./media/46_rev-rec-scenarios.png)

Når du vælger **Bilag**, viser fakturakladden den oprindelige regnskabspost. Hvis du vil have vist tilbageførselsposten og den nye regnskabspost fra salgsordren, skal du vælge **Indtægtsreguleringer** i handlingsruden og derefter vælge **Bilag**.

Åbn derefter siden **Alle debitorer** (**Debitorer \> Kunder \> alle kunder**), vælg kunde **US\_SI\_0003**, og vælg derefter **Transaktioner**. Siden **Debitorposteringer** viser kun den oprindelige faktura (000008) sammen med den oprindelige regnskabspost. Da indstillingen **Bogfør fakturakorrektioner i Debitor** er angivet til **Nej** på siden **Finansparametre**, opdateres kun Finans. Derfor vises tilbageførsels- og opdaterede regnskabsposter ikke. Bemærk, at de omsætningsreguleringsposteringer, der blev oprettet i [senarie 3](rev-rec-reallocation-scenario-3.md), vises.

[![Den oprindelige regnskabspost på siden Debitorposteringer](./media/47_rev-rec-scenarios.png)](./media/47_rev-rec-scenarios.png)
