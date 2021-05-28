---
title: Du kan ikke fjerne behovsprognosedimensionen for et lagersted fra budgetlinjer
description: Du kan ikke fjerne behovsprognosedimensionen for et lagersted fra budgetlinjer.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026374"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>Du kan ikke fjerne behovsprognosedimensionen for et lagersted fra budgetlinjer

KB-nummer: 4614408

## <a name="symptoms"></a>Symptomer

Dette problem opstår, når dimensionen **Lagersted** ikke er tildelt under fanen **Budgetdimensioner** på siden **Parametre til behovsprognoser**. Kolonnen **Lagersted** vises dog på siden **Behovsprognose** (**Varedisponering \> Budgettering \> Manuel budgetenhed \> Behovsprognoselinjer**).

## <a name="resolution"></a>Løsning

Indstillingerne under fanen **Budgetdimensioner** på siden **Parametre til behovsprognoser** har ingen indflydelse på siden **Behovsprognose**. De styrer det oprindelige budget, der oprettes og vises i den regulerede behovsprognose. De styrer dog ikke de dimensioner, der kræves til den "reelle" behovsprognose. Når du autoriserer de poster, der vises på siden **Justeret behovsprognose**, kan du konvertere dem til "reelle" budgetposteringer for en prognosemodel. Denne model kan derefter bruges til behovsplanlægning.

På siden **Behovsprognose** indgår dimensionerne for det "reelle" budget, der vises på linjerne i efterspørgselsprognosen, i lagerdimensionerne. (Denne funktionsmåde minder om funktionsmåden for salgsordrelinjer). Hvis systemet ikke er konfigureret til at bruge **Lagersted** som en obligatorisk lagerdimension, kan du tilpasse siden, så kolonnen skjules.
