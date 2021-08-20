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
ms.openlocfilehash: 96af593d2e8a738258fe614f0f252620cb48c5f19eeb4425c9659ee6f9cd8c0c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741207"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>Du kan ikke fjerne behovsprognosedimensionen for et lagersted fra budgetlinjer

KB-nummer: 4614408

## <a name="symptoms"></a>Symptomer

Dette problem opstår, når dimensionen **Lagersted** ikke er tildelt under fanen **Budgetdimensioner** på siden **Parametre til behovsprognoser**. Kolonnen **Lagersted** vises dog på siden **Behovsprognose** (**Varedisponering \> Budgettering \> Manuel budgetenhed \> Behovsprognoselinjer**).

## <a name="resolution"></a>Løsning

Indstillingerne under fanen **Budgetdimensioner** på siden **Parametre til behovsprognoser** har ingen indflydelse på siden **Behovsprognose**. De styrer det oprindelige budget, der oprettes og vises i den regulerede behovsprognose. De styrer dog ikke de dimensioner, der kræves til den "reelle" behovsprognose. Når du autoriserer de poster, der vises på siden **Justeret behovsprognose**, kan du konvertere dem til "reelle" budgetposteringer for en prognosemodel. Denne model kan derefter bruges til behovsplanlægning.

På siden **Behovsprognose** indgår dimensionerne for det "reelle" budget, der vises på linjerne i efterspørgselsprognosen, i lagerdimensionerne. (Denne funktionsmåde minder om funktionsmåden for salgsordrelinjer). Hvis systemet ikke er konfigureret til at bruge **Lagersted** som en obligatorisk lagerdimension, kan du tilpasse siden, så kolonnen skjules.
