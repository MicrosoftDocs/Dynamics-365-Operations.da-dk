---
title: Oprette en indkøbsordre, der er underlagt budgettet
description: Brug denne procedure, når du vil oprette en indkøbsordre, der skal kontrolleres for disponibelt budget.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 319eb0070a3677035e2a5d89744e80cd38c08d8e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980501"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Oprette en indkøbsordre, der er underlagt budgettet

[!include [banner](../../includes/banner.md)]

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

