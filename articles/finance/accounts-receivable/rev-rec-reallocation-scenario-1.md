---
title: Omplacering af indtægtsføring - Scenarie 1
description: Dette emne behandler en omplacering, hvor to salgsordrer er angivet, men de er kun bekræftet. Det samme scenario giver lignende resultater, hvis mere end to salgsordrer er i bekræftet tilstand.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f94b054d213dc2b347f4e5a7b2f4c2a51d519f57
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823998"
---
# <a name="revenue-recognition-reallocation--scenario-1"></a>Omplacering af indtægtsføring - Scenarie 1

[!include [banner](../includes/banner.md)]

Dette emne behandler en omplacering, hvor to salgsordrer er angivet, men de er kun bekræftet. Det samme scenario giver lignende resultater, hvis mere end to salgsordrer er i bekræftet tilstand.

I dette scenarie er indstillingen **Bogfør fakturakorrektioner til debitor** angivet **Nej** på fanen **Indtægtsføring** på siden **Finansparametre** (**Indtægtsføring \> Opsætning \> Finansparametre**).

[![Bogfør fakturarettelser til indstillingen Debitor som Nej](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)

Der oprettes en salgsordre for kunde US\_SI\_0003. Kunden køber en bærbar computer (varenummer S0012) og en supportplan for den (varenummer S0008, "Vedvarende teknisk service"). Indtægterne for den bærbare computer er straks anerkendt (der er ingen indtægtsføringplan). Omsætningen for støtteplanen udskydes og indregnes over 12 måneder som defineret af datointervallet i kontrakten.

[![Salgsordrelinjer til den bærbare computer og supportplan](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)

Salgsordren er bekræftet. Da begge varer er konfigureret til fordeling af omsætningsprisen, beregnes omsætningsprisen, når salgsordren bekræftes. Du kan få vist den omsætning, der skal registreres på siden **Fordeling af indtægtspris** (på siden **Salgsordre** i handlingsruden under fanen **Administrer** i gruppen **Indtægtsføring** skal du vælge **Fordeling af omsætningspris**). Indtægterne for den bærbare computer vil blive bogført på indtægtskontoen i mængden af $1.008,01. Indtægterne for supportplanen vil blive bogført på Udskudt indtægtskonto med $190,99. Summen af indtægtspriserne skal svare til summen af de linjer, der blev oprettet for at registrere fordeling af indtægtspriser ($1.199,00).

[![Fordeling af indtægtsprisside](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)

Kunden valgte ikke at købe installationsydelser (varenummer S0001) på salgstidspunktet, men skiftede senere mening. Der angives derfor endnu en salgsordre for den samme kunde.

[![Salgsordrelinje for installationstjenester](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)

Den anden salgsordre er bekræftet. Da denne salgsordre kun indeholder én linje, sker fordelingen af omsætningsprisen ikke, når salgsordren bekræftes. Fordeling af omsætningsprisen sker kun, hvis der er to eller flere entydige varer, og hvis disse varer er konfigureret til fordeling af omsætningsprisen.

Hvis denne nye salgsordre er den eneste ændring i kundens kontrakt, kan omfordelingsprocessen nu køres. I en af de to salgsordrer skal du vælge **Genalloker pris med nye ordrelinjer** for at åbne siden **Genallokering med nye ordrelinjer**. Du kan også gå til **Indtægtsføring \> Periodiske opgaver \> Genalloker prisen med nye ordrelinjer**. Vælg de to salgsordrer og de tilsvarende salgsordrelinjer, og vælg derefter **Opdater genallokering**. Kolonnen **Omfordelt beløb** viser den nye omsætningspris for hver salgsordrelinje.

[![Nye omsætningspriser på siden Genallokering med nye ordrelinjer](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)

Hvis du vælger **Forventet bilag**, vises der intet, fordi der ikke er bogført fakturaer.

Hvis du vil fuldføre omfordelingen, skal du vælge **Proces**. Du bliver bedt om en bogføringsdato, selvom der ikke er bogført noget. Når omfordelingen er fuldført, viser siden **Indtægtsprisfordeling** for hver salgsordre prisfordelingen for alle varer på tværs af begge salgsordrer. Med andre ord vil siden **Fordeling af omsætningspris** indeholde en vare, der ikke findes på salgsordren, fordi den er en del af den samme kontrakt, men på en anden salgsordre.

> [!TIP]
> Hvis du vil give kontekst om, hvorfor disse yderligere elementer vises, kan du føje andre kolonner til gitteret, f.eks. **Genplacerings-id** og **Salgsordre**.
> 
> [![Yderligere kolonner på siden Indtægtsprisfordelinger](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]