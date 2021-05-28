---
title: Momsen beregnes ikke, eller momsbeløbet er nul
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig, når momsbeløbet er 0 (nul) eller ikke er beregnet.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: c398579a0a408e7f5625a3e801a967955c4b1e5b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020109"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a>Momsen beregnes ikke, eller momsbeløbet er nul

[!include [banner](../includes/banner.md)]

En transaktion kan have et linjebeløb, der ikke er 0 (nul), men enten er momsbeløbet ikke beregnet, eller det beregnede momsbeløb er 0. Du kan udføre fejlfinding af dette problem ved at følge trinnene i følgende afsnit efter behov.

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a>Kontrollér, at momskoderne er valgt korrekt af transaktionen

Hvis transaktionen ikke vælger de rette momskoder, eller hvis den ikke vælger nogen momskoder, beregnes der ikke moms af den. Benyt denne fremgangsmåde for at kontrollere, at momskoderne er valgt korrekt af transaktionen. 

1. På posteringslinjen i oversigtspanelet **Linjedetaljer** under fanen **Opsætning** i sektionen **Moms** skal du kontrollere, at de korrekte momsgrupper er valgt i felterne **Varemomsgruppe** og **Momsgruppe**. Hvis de korrekte momsgrupper ikke er valgt, skal du vælge dem.

    [![Felterne Varemomsgruppe og Momsgruppe](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)

2. Gå til **Moms** \> **Indirekte skatter** \> **Moms** \> **Momsgrupper**.
3. Vælg den relevante momsgruppe, og noter derefter momskoden i feltet **Momskode** i oversigtspanelet **Opsætning**.

    [![Siden Momsgrupper](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)

4. Gå til **Moms** \> **Indirekte skatter** \> **Moms** \> **Varemomsgrupper**.
5. Vælg den relevante varemomsgruppe, og kontroller derefter, at momskoden i feltet **Momskode** svarer til momsgruppens momskode i oversigtspanelet **Opsætning**.

    [![Siden Varemomsgrupper](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)

6. Hvis momskoderne ikke stemmer overens, skal du opdatere momskoden for en af grupperne.

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a>Kontrollér, at de valgte momskoder ikke er fritaget for moms, og at de har den rette momssatsværdi

Hvis momskoderne er fritaget for moms, eller hvis momssatsen er 0 (nul), vil resultatet af momsberegningen være 0. Benyt følgende fremgangsmåde for at finde ud af, om de valgte momskoder er fritaget for moms, og for at kontrollere, at den rette momssats er anvendt til dem.

1. Gå til **Moms** \> **Indirekte skatter** \> **Moms** \> **Momsgrupper**.
2. Vælg den relevante momsgruppe, og kontroller derefter, at afkrydsningsfeltet **Momsfritagelse** ikke er markeret, i oversigtspanelet **Opsætning**. Hvis feltet er markeret, skal du fjerne markeringen.

    [![Afkrydsningsfeltet Momsfritagelse på siden Momsgrupper](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)

3. Gå til **Moms** \> **Indirekte skatter** \> **Moms** \> **Momskoder**.
4. Vælg den relevante momskode, og kontroller derefter, at momssatsværdien i **feltet Værdi** ikke er 0 (nul). Hvis værdien er 0, skal du opdatere feltet, så det er indstillet til den rette momssats.

    [![Feltet Værdi på siden Momskodeværdier](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a>Afgøre, om nul er det korrekte momsbeløb

I nogle tilfælde er et momsbeløb på 0 (nul) korrekt. Benyt denne fremgangsmåde for at finde ud af, om 0 er det korrekte momsbeløb for transaktionen.

1. Gå til **Finans** \> **Opsætning Finans** \> **Finansparametre**.
2. Kontrollér, at **Total** er valgt i feltet **Beregningsmetode** under fanen **Moms**.

    [![Feltet Beregningsmetode på siden Finansparametre](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)

3. Gå til **Moms** \> **Indirekte skatter** \> **Moms** \> **Momskoder**.
4. Vælg den relevante momskode, vælg **Beregning** \> **Beregningsgrundlag**, og kontrollér, at beregningsgrundlaget er angivet til **Nettobeløb for fakturasaldo** eller **Fakturatotal inkl. andre momsbeløb**. Yderligere oplysninger finder du i [Fakturatotal inkl. andre momsbeløb](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).
5. Hvis de korrekte værdier er angivet i trin 2 og 4, skal du afgøre, om det samlede beløb for transaktionen er 0 (nul). Hvis totalbeløbet er 0, er et momsbeløb på 0 det forventede resultat. Da momsberegningen er baseret på fakturasaldoens totalbeløb, og ikke beløbet linje for linje, fordeles momsbeløbet på 0 til hver linje efter momsberegningen.

## <a name="determine-whether-customization-exists"></a>Afgøre, om der findes tilpasninger

Hvis du har udført trinnene i de forrige afsnit, men ikke har fundet nogen problemer, skal du afgøre, om der er foretaget tilpasninger. Hvis der ikke er foretaget tilpasninger, skal du oprette en Microsoft-serviceanmodning for at få yderligere support.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
