---
title: Omplacering af indtægtsføring - Scenarie 2
description: Dette emne behandler omplaceringsscenariet, hvor to salgsordrer angives, og kunden føjer en vare til kontrakten, efter at den første salgsordre er faktureret. Når en ny vare føjes til en kontrakt, kan den føjes til enten en ny salgsordre eller til en eksisterende salgsordre.
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
ms.openlocfilehash: 30b4c55a82237b5c8b6b41032243da337a5ec969
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003384"
---
# <a name="revenue-recognition-reallocation--scenario-2"></a>Omplacering af indtægtsføring - Scenarie 2

[!include [banner](../includes/banner.md)]

Dette emne behandler omplaceringsscenariet, hvor to salgsordrer angives, og kunden føjer en vare til kontrakten, efter at den første salgsordre er faktureret. Når en ny vare føjes til en kontrakt, kan den føjes til enten en ny salgsordre eller til en eksisterende salgsordre.

I dette scenarie er indstillingen **Bogfør fakturakorrektioner til debitor** angivet **Nej** på fanen **Indtægtsføring** på siden **Finansparametre** (**Indtægtsføring \> Opsætning \> Finansparametre**).

[![Bogfør fakturarettelser til indstillingen Debitor som Nej](./media/12_rev-rec-scenarios.png)](./media/12_rev-rec-scenarios.png)

Der oprettes en salgsordre for kunde US\_SI\_0003. Kunden køber installationstjenester (varenummer S0001) og en supportplan (varenummer S0008) til en bærbar computer, men de har endnu ikke valgt den bærbare computer. Indtægterne for installationstjenesten udskydes indtil den dato, hvor den bærbare computer købes. Omsætningen for støtteplanen udskydes og indregnes over 12 måneder som defineret af datointervallet i kontrakten.

[![Salgsordrelinjer til installationstjenester og supportplan](./media/13_rev-rec-scenarios.png)](./media/13_rev-rec-scenarios.png)

Salgsordren er bekræftet. Da begge varer er konfigureret til fordeling af omsætningsprisen, beregnes omsætningsprisen, når salgsordren bekræftes. Du kan få vist den omsætning, der skal registreres på siden **Fordeling af indtægtspris** (på siden **Salgsordre** i handlingsruden under fanen **Administrer** i gruppen **Indtægtsføring** skal du vælge **Fordeling af omsætningspris**). Indtægterne for installationstjenester vil blive bogført på Udskudt indtægtskonto med $250,00. Indtægterne for supportplanen vil også blive bogført på Udskudt indtægtskonto med $150,00. Summen af indtægtspriserne skal svare til summen af de linjer, der blev oprettet for at registrere fordeling af indtægtspriser ($400,00).

[![Fordeling af indtægtsprisside](./media/14_rev-rec-scenarios.png)](./media/14_rev-rec-scenarios.png)

Salgsordren er helt faktureret. I følgende illustration vises den regnskabspost, der er bogført på fakturaen.

[![Regnskabspost for den komplet fakturerede salgsordre](./media/15_rev-rec-scenarios.png)](./media/15_rev-rec-scenarios.png)

Tidsplanen for indtægtsføring oprettes også, men ingen af indtægterne registreres endnu.

[![Siden Tidsplan for indtægtsføring](./media/16_rev-rec-scenarios.png)](./media/16_rev-rec-scenarios.png)

Nogle dage senere vælger kunden en bærbar computer. Der angives endnu en salgsordre for debitoren.

[![Salgsordrelinje for den bærbare computer](./media/17_rev-rec-scenarios.png)](./media/17_rev-rec-scenarios.png)

Den anden salgsordre er bekræftet. Da denne salgsordre kun indeholder én linje, sker fordelingen af omsætningsprisen ikke, når salgsordren bekræftes. Fordeling af omsætningsprisen sker kun, hvis der er to eller flere entydige varer, og hvis disse varer er konfigureret til fordeling af omsætningsprisen.

Hvis denne nye salgsordre er den eneste ændring i kundens kontrakt, kan omfordelingsprocessen nu køres. I en af de to salgsordrer skal du vælge **Genalloker pris med nye ordrelinjer** for at åbne siden **Genallokering med nye ordrelinjer**. Du kan også gå til **Indtægtsføring \> Periodiske opgaver \> Genalloker prisen med nye ordrelinjer**. Vælg de to salgsordrer og de tilsvarende salgsordrelinjer, og vælg derefter **Opdater genallokering**. Kolonnen **Omfordelt beløb** viser den nye omsætningspris for hver salgsordrelinje.

[![Nye omsætningspriser på siden Genallokering med nye ordrelinjer](./media/18_rev-rec-scenarios.png)](./media/18_rev-rec-scenarios.png)

Derefter skal du vælge **Forventet bilag** for at få vist de regnskabsposter, der kun skal bogføres i Finans. Da indstillingen **Bogfør fakturakorrektioner i Debitor** er angivet til **Nej** på siden **Finansparametre**, ændres intet i Debitor, når genplaceringen behandles.

[![Regnskabsposter på siden Forventet bilag](./media/19_rev-rec-scenarios.png)](./media/19_rev-rec-scenarios.png)

På siden **Forventet bilag** tilbageføres de sidste tre linjer i den oprindelige regnskabspost fra den bogførte faktura. De første fire linjer udgør den nye regnskabspost, der bogføres for fakturaen. Det er vigtigt, at du forstår, at en ny faktura ikke præsenteres for kunden. Efter omfordelingen skylder debitoren stadig $426,00, hvilket er det beløb, der skal bogføres på Debitor i den nye regnskabspost. Modregningsskat og udskudt omsætning er lig med $188,69 + $314,48 + $26,00 = $529,17. Det udskudte omsætningsbeløb er ændret på grund af omfordelingen. Forskellen på $103,17 bogføres på en konto til modposteringer af delfakturaer. Denne saldo ryddes, når fakturaen bogføres for den anden salgsordre, der blev medtaget i omplaceringen.

Hvis du vil fuldføre omfordelingen, skal du vælge **Proces**. Du bliver bedt om en bogføringsdato, selvom der ikke er bogført noget. Når omfordelingen er fuldført, viser siden **Indtægtsprisfordeling** for hver salgsordre prisfordelingen for alle varer på tværs af begge salgsordrer. Med andre ord vil siden **Fordeling af omsætningspris** indeholde en vare, der ikke findes på salgsordren, fordi den er en del af den samme kontrakt, men på en anden salgsordre.

> [!TIP]
> Hvis du vil give kontekst om, hvorfor disse yderligere elementer vises, kan du føje andre kolonner til gitteret, f.eks. **Genplacerings-id** og **Salgsordre**.
> 
> [![Yderligere kolonner på siden Indtægtsprisfordelinger](./media/20_rev-rec-scenarios.png)](./media/20_rev-rec-scenarios.png)

I salgsordre 00036 blev planen for indtægtsføring også opdateret på baggrund af den nye indtægt til genallokationspris. Åbn siden **Indtægtsføringsplan** fra denne salgsordre. Tidligere var der 13 linjer for vare S0008 (der blev tildelt en plan på 12 måneder til denne vare). Der er nu 39 linjer: De 13 oprindelige planlægningslinjer, 13 linjer i tilbageførselsplanen og 13 linjer, der er baseret på den nye omsætningspris.

[![Siden Opdateret plan for indtægtsføring med 39 linjer for varen S0008](./media/21_rev-rec-scenarios.png)](./media/21_rev-rec-scenarios.png)

På samme måde har der tidligere været to linjer for vare S0001, men nu er der seks.

[![Siden Opdateret plan for indtægtsføring med seks linjer for varen S0001](./media/22_rev-rec-scenarios.png)](./media/22_rev-rec-scenarios.png)

Når du vælger **Bilag** i salgsordre 000036, viser fakturakladden den oprindelige regnskabspost. Hvis du vil have vist tilbageførselsposten og den nye regnskabspost fra salgsordren, skal du vælge **Indtægtsreguleringer** i handlingsruden og derefter vælge **Bilag**.

[![Salgsordre 000036](./media/23_rev-rec-scenarios.png)](./media/23_rev-rec-scenarios.png)

Åbn derefter siden **Alle debitorer** (**Debitorer \> Kunder \> alle kunder**), vælg kunde **US\_SI\_0003**, og vælg derefter **Transaktioner**. Den åbne faktura fra salgsordre 000036 vises. Hvis du vælger bilaget, får du vist den oprindelige regnskabspost, ikke den nye regnskabspost fra omfordelingen. Tilbageførselsposten og den nye regnskabspost kan ikke ses fra Debitor.

Den anden salgsordre er nu faktureret. Den samlede faktura, der vises til kunden, er for $1.099,00 + $71,44 moms = $1.170,44. I følgende illustration vises den regnskabspost, der er bogført.

[![Siden Posteringer på bilag med den regnskabspost, der er bogført](./media/24_rev-rec-scenarios.png)](./media/24_rev-rec-scenarios.png)

Da summen af omsætningen og salget er større end $1.170,44, bogføres differencen på $-130,17. Dette beløb rydder saldoen fra kontoen til clearing for delfakturaomsætning. Den pågældende saldo bogføres i den nye regnskabspost efter omfordelingen.
