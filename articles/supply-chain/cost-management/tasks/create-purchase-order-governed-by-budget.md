---
title: Oprette en indkøbsordre, der er underlagt budgettet
description: Brug denne procedure, når du vil oprette en indkøbsordre, der skal kontrolleres for disponibelt budget.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e82e40d67547f5932a4805f2580e8c9f58def284
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569977"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Oprette en indkøbsordre, der er underlagt budgettet

[!include [task guide banner](../../includes/task-guide-banner.md)]

Brug denne procedure, når du vil oprette en indkøbsordre, der skal kontrolleres for disponibelt budget. Denne registrering bruger USMF-demodatafirmaet.


## <a name="review-the-budget-control-configuration"></a>Gennemse konfigurationen for budgetstyring
1. Gå til Budgettering > Opsætning > Budgetstyring > Konfiguration af budgetstyring.
2. Klik på fanen Tilgængelige budgetmidler.
3. Klik på fanen Dokumenter og journaler.
4. Klik på fanen Definer budgetstyringsregler.
5. Klik på fanen Definer budgetgrupper.
6. Luk siden.

## <a name="create-the-purchase-order-header"></a>Oprette indkøbsordrehovedet
1. Gå til Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Kreditorkonto.
4. Udvid afsnittet Generelt.
5. Konfigurer datoen '01-01-2016' i feltet Regnskabsdato.
6. Klik på OK.

## <a name="add-a-purchase-order-line"></a>Tilføje en indkøbsordrelinje
1. Indtast eller vælg en værdi i feltet Indkøbskategori.
2. Indstil Antal til '2'.
3. Indtast eller vælg en værdi i feltet Enhed.
4. Angiv Enhedspris til "10000".
5. Klik på Finans.
6. Klik på Fordel beløb.
7. I feltet Finanskonto skal du angive værdien '601300-001-023--'.
8. Luk siden.

## <a name="perform-budget-checking"></a>Udfør budgetkontrol
1. Klik på Finans.
2. Klik på Udfør budgetkontrol.
3. Klik på Finans.
4. Klik på Fejl eller advarsler i forbindelse med budgetkontrol.
5. Klik på Luk.

