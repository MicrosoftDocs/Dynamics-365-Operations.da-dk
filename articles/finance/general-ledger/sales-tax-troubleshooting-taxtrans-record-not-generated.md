---
title: TaxTrans-post er ikke genereret
description: Dette emne indeholder fejlfindingsoplysninger, som kan hjælpe, når der ikke er genereret en TaxTrans-post.
author: qire
ms.date: 04/13/2021
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
ms.openlocfilehash: 284fd4047347386b3893684f077a5980f98a6788
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349994"
---
# <a name="taxtrans-record-isnt-generated"></a>TaxTrans-post er ikke genereret

[!include [banner](../includes/banner.md)]

Hvis du vælger **Bogført moms** for en transaktion, men siden **Bogført moms** enten ikke viser nogen momslinjer eller mangler en momslinje, er **TaxTrans**-posten muligvis ikke blevet genereret.

[![Siden Bogført moms, der ikke indeholder linjeelementer.](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

Du kan udføre fejlfinding af dette problem ved at følge trinnene i følgende afsnit efter behov.

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>Kontrollere momsen, før du bogfører transaktionen

1. Før du bogfører transaktionen, skal du vælge **Moms** på siden **Bogføring af faktura** for at kontrollere beregningen.

    [![Knappen Moms på siden Bogføring af faktura.](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. Gennemse resultatet af beregningen på siden **Midlertidige posteringer af moms**. Hvis der ikke er beregnet moms, skal du se i [Moms er ikke beregnet, eller momsbeløb er nul](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>Find TaxTrans-posten i al bogført moms

1. Gå til **Moms** \> **Forespørgsler og rapporter** \> **Momsforespørgsler** > **Bogført moms**.
2. Vælg filtersymbolet i kolonneoverskriften **Bilag** for at finde posten **TaxTrans**.
3. Hvis du finder de momsposter, du søger efter, skal du kontrollere datoen. Hvis datoen afviger fra datoen i kladdehovedet, skal du oprette en Microsoft-serviceanmodning for at få yderligere support.

    [![Siden Bogført moms.](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>Løse fejl for at kontrollere oplysninger

1. Yderligere oplysninger om, hvordan du kan løse fejl og finde ud af, om **TmpTaxWorkTrans** og **TaxUncommitted** er korrekt genereret, finder du i [Feltværdi i TaxTrans er forkert](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).
2. Hvis **TaxTmpWorkTrans** eller **TaxUncommitted** er genereret korrekt, skal du tilføje et pausepunkt ved **TaxPost::SaveAndPost()** og **Tax::SaveAndPost** for at finde årsagen til, at **TaxTrans** ikke er indsat.

    [![Pausepunkter tilføjet i kode.](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![Resultater af tilføjede pausepunkter.](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>Afgøre, om der findes tilpasninger

Hvis du har udført trinnene i de forrige afsnit, men ikke har fundet nogen problemer, skal du afgøre, om der er foretaget tilpasninger. Hvis der ikke er foretaget tilpasninger, skal du oprette en Microsoft-serviceanmodning for at få yderligere support.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
