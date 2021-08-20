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
ms.openlocfilehash: 8800ec411ddd7ae73c5ac159592620a07b50c1e87938f823274ec24062c9a71a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741950"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>Udskudt valg overholdes ikke, når produktionsordrer nulstilles via et batchjob

KB-nummer: 4614634

## <a name="symptoms"></a>Symptomer

Når du bruger et tilbagevendende batchjob til at nulstille statussen for en produktionsordre, overholdes udskudte valg ikke.

## <a name="resolution"></a>Løsning

Det aktuelle design understøtter ikke brugen af udskudte valg i processen *Nulstil status*.
