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
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a><span data-ttu-id="f0092-103">Udskudt valg overholdes ikke, når produktionsordrer nulstilles via et batchjob</span><span class="sxs-lookup"><span data-stu-id="f0092-103">Late selection isn't respected when production orders are reset via a batch job</span></span>

<span data-ttu-id="f0092-104">KB-nummer: 4614634</span><span class="sxs-lookup"><span data-stu-id="f0092-104">KB number: 4614634</span></span>

## <a name="symptoms"></a><span data-ttu-id="f0092-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="f0092-105">Symptoms</span></span>

<span data-ttu-id="f0092-106">Når du bruger et tilbagevendende batchjob til at nulstille statussen for en produktionsordre, overholdes udskudte valg ikke.</span><span class="sxs-lookup"><span data-stu-id="f0092-106">When you use a recurring batch job to reset the status of a production order, late selections aren't respected.</span></span>

## <a name="resolution"></a><span data-ttu-id="f0092-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="f0092-107">Resolution</span></span>

<span data-ttu-id="f0092-108">Det aktuelle design understøtter ikke brugen af udskudte valg i processen *Nulstil status*.</span><span class="sxs-lookup"><span data-stu-id="f0092-108">The current design doesn't support the use of late selections for the *Reset status* process.</span></span>
