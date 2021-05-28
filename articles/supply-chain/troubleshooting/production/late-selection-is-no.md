---
title: Udskudt valg overholdes ikke, når produktionsordrer nulstilles via et batchjob
description: Når du bruger et tilbagevendende batchjob til at nulstille statussen for en produktionsordre, overholdes udskudte valg ikke.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e53198f427f4060421a4f0078277682c43db1320
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026365"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>Udskudt valg overholdes ikke, når produktionsordrer nulstilles via et batchjob

KB-nummer: 4614634

## <a name="symptoms"></a>Symptomer

Når du bruger et tilbagevendende batchjob til at nulstille statussen for en produktionsordre, overholdes udskudte valg ikke.

## <a name="resolution"></a>Løsning

Det aktuelle design understøtter ikke brugen af udskudte valg i processen *Nulstil status*.
