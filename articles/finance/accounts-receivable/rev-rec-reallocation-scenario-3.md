---
title: Omplacering af indtægtsføring - Scenarie 3
description: Denne artikel behandler omplacering af et scenarie, hvor der føjes en ny linje til en eksisterende faktureret salgsordre. Når en ny vare føjes til en kontrakt, kan den føjes til enten en ny salgsordre eller til en eksisterende salgsordre.
author: bking
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: bking
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e76c077aa24813c9b6ac8c72db06b38cedaafd18
ms.sourcegitcommit: 1909d18a74cef85aad020a6a7473281e451f58c7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348177"
---
# <a name="revenue-recognition-reallocation--scenario-3"></a>Omplacering af indtægtsføring - Scenarie 3

[!include [banner](../includes/banner.md)]

Denne artikel behandler omplacering af et scenarie, hvor der føjes en ny linje til en eksisterende faktureret salgsordre. Når en ny vare føjes til en kontrakt, kan den føjes til enten en ny salgsordre eller til en eksisterende salgsordre. Dette scenario viser også, hvad der sker, når Debitor opdateres på grund af omplaceringen.

I dette scenarie er indstillingen **Bogfør fakturakorrektioner til debitor** angivet **Ja** på fanen **Indtægtsføring** på siden **Finansparametre** (**Indtægtsføring \> Opsætning \> Finansparametre**).

[![Bogfør fakturarettelser til indstillingen Debitor som Ja.](./media/25_rev-rec-scenarios.png)](./media/25_rev-rec-scenarios.png)

Der oprettes en salgsordre for kunde US\_SI\_0003. Kunden køber en bærbar computer (varenummer S0012) og en supportplan for den (varenummer S0008, "Vedvarende teknisk service"). Indtægten for den bærbare computer registreres med det samme. Omsætningen for støtteplanen udskydes og indregnes over 12 måneder som defineret af datointervallet i kontrakten.

[![Salgsordrelinjer til den bærbare computer og supportplan.](./media/26_rev-rec-scenarios.png)](./media/26_rev-rec-scenarios.png)

Salgsordren er bekræftet. Da begge varer er konfigureret til fordeling af omsætningsprisen, beregnes omsætningsprisen, når salgsordren bekræftes. Du kan få vist den omsætning, der skal registreres på siden **Fordeling af indtægtspris** (på siden **Salgsordre** i handlingsruden under fanen **Administrer** i gruppen **Indtægtsføring** skal du vælge **Fordeling af omsætningspris**). Indtægterne for den bærbare computer vil blive bogført på indtægtskontoen med $1.008,01. Indtægterne for supportplanen vil blive bogført på Udskudt indtægtskonto med $190,99. Summen af indtægtspriserne skal svare til summen af de linjer, der blev oprettet for at registrere fordeling af indtægtspriser (DKK 1.199,00).

[![Fordeling af indtægtsprisside.](./media/27_rev-rec-scenarios.png)](./media/27_rev-rec-scenarios.png)

Salgsordren er helt faktureret. I følgende illustration vises den regnskabspost, der er bogført på fakturaen.

[![Regnskabspost for den komplet fakturerede salgsordre.](./media/28_rev-rec-scenarios.png)](./media/28_rev-rec-scenarios.png)

Tidsplan for indtægtsføring oprettes også. Når der er gå lang tid, har to af månederne registreret indtægt for supportplanen.

[![Siden Indtægtsføringsplan, når der er gået to måneder.](./media/29_rev-rec-scenarios.png)](./media/29_rev-rec-scenarios.png)

På dette tidspunkt beslutter kunden sig for at tilføje installationstjenester (varenummer S0001). Denne vare føjes til den eksisterende salgsordre. Kunden bliver bedt om at bekræfte, at de vil redigere den komplet fakturerede salgsordre, og de vælger **Ja**.

[![Salgsordre, efter at linjen til installationstjenester er tilføjet.](./media/30_rev-rec-scenarios.png)](./media/30_rev-rec-scenarios.png)

Hvis dette nye element er den eneste ændring i kundens kontrakt, kan omfordelingsprocessen køres nu. I salgsordren skal du vælge **Genalloker pris med nye ordrelinjer** for at åbne siden **Genallokering med nye ordrelinjer**. Vælg alle salgsordrelinjer til denne salgsordre, og vælg derefter **Opdater genallokering**. Kolonnen **Omfordelt beløb** viser den nye omsætningspris for hver salgsordrelinje.

[![Nye omsætningspriser på siden Genallokering med nye ordrelinjer.](./media/31_rev-rec-scenarios.png)](./media/31_rev-rec-scenarios.png)

Vælg derefter **Forventet bilag** for at få vist regnskabsposterne. Da indstillingen **Bogfør fakturakorrektioner i Debitor** er angivet til **Ja** på siden **Finansparametre**, bogføres disse regnskabsposter i Finans via kreditdokumentet, og der oprettes en ny faktura i Debitor.

[![Regnskabsposter på siden Forventet bilag.](./media/32_rev-rec-scenarios.png)](./media/32_rev-rec-scenarios.png)

På siden **Forventet bilag** tilbageføres de sidste fire linjer i den oprindelige regnskabspost fra den bogførte faktura. De første fem linjer udgør de nye regnskabsposter, der bogføres for fakturaen. Det er vigtigt, at du forstår, at en ny faktura ikke præsenteres for kunden. Efter omfordelingen skylder debitoren stadig $1.276,94, hvilket er det beløb, der skal bogføres på Debitor i den nye regnskabspost. Modregningsskat og omsætning eller udskudt omsætning er lig med $995,83 + $188,69 + $77,94 = $1.262,46. Indtægten eller det udskudte omsætningsbeløb er ændret på grund af omfordelingen. Forskellen på $-14,48 bogføres på en konto til modposteringer af delfakturaer. Denne saldo ryddes, når fakturaen bogføres for den nye vare, der blev medtaget i salgsordren.

Hvis du vil fuldføre omfordelingen, skal du vælge **Proces**. Der er angivet en bogføringsdato. Når omplaceringen er fuldført, viser siden **Fordeling af omsætningspris** tildelingen af prisen for alle tre varer.

[![Prisomfordeling for alle tre varer på siden Indtægtspristildeling.](./media/33_rev-rec-scenarios.png)](./media/33_rev-rec-scenarios.png)

Planen for indtægtsføring blev også opdateret på baggrund af den nye indtægt til genallokationspris. Åbn siden **Indtægtsføringsplan** fra denne salgsordre. Tidligere var der 13 linjer for vare S0008 (der blev tildelt en plan på 12 måneder til denne vare). Der er nu 39 linjer: De 13 oprindelige planlægningslinjer, 13 linjer i tilbageførselsplanen og 13 linjer, der er baseret på den nye omsætningspris.

[![Siden Opdateret plan for indtægtsføring med 39 linjer for varen S0008.](./media/34_rev-rec-scenarios.png)](./media/34_rev-rec-scenarios.png)

Når du vælger **Bilag**, viser fakturakladden den oprindelige regnskabspost. Hvis du vil have vist tilbageførselsposten og den nye regnskabspost fra salgsordren, skal du vælge **Indtægtsreguleringer** i handlingsruden og derefter vælge **Bilag**.

Åbn derefter siden **Alle debitorer** (**Debitorer \> Kunder \> alle kunder**), vælg kunde **US\_SI\_0003**, og vælg derefter **Transaktioner**. Siden **Debitorposteringer** viser den oprindelige faktura (000006), tilbageførselsdokumentet (000006-1) og den nye faktura (000006-2). Den oprindelige faktura og tilbageførselsdokumentet udlignes mod hinanden og har en saldo på 0 (nul). Få vist bilaget for de enkelte dokumenter for at se virkningen i Finans.

[![Oprindelig faktura, tilbageført dokument og den nye faktura på siden Debitortransaktioner.](./media/35_rev-rec-scenarios.png)](./media/35_rev-rec-scenarios.png)

Salgsordren faktureres igen for den vare, der er tilføjet. Den samlede faktura, der vises til kunden, er for $300,00 + $19,50 moms = $319,50. I følgende illustration vises den regnskabspost, der er bogført.

[![Siden Posteringer på bilag med den regnskabspost, der er bogført.](./media/36_rev-rec-scenarios.png)](./media/36_rev-rec-scenarios.png)

Da summen af omsætningen og salget er større end DKK 319,50, bogføres differencen på DKK 14,48. Dette beløb rydder saldoen fra kontoen til clearing for delfakturaomsætning. Den pågældende saldo blev opdateret bogføres i den nye regnskabspost, der blev bogført efter omfordelingen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
