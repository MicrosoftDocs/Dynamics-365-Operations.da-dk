---
title: Du kan ikke fakturere en kundehenvendt salgsordre
description: Du kan ikke længere fakturere den oprindelige salgsordre og den oprindelige indkøbsordre for direkte levering, når du har aktiveret indstillingen Bogfør faktura automatisk.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026367"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Du kan ikke fakturere en kundehenvendt salgsordre

KB-nummer: 4611793

## <a name="symptoms"></a>Symptomer

Du kan ikke længere fakturere den oprindelige salgsordre og den oprindelige indkøbsordre for direkte levering, når du har aktiveret indstillingen **Bogfør faktura automatisk** på siden **Intern** for en leverandør.

## <a name="resolution"></a>Løsning

Synkroniseringsfunktionsmåden for interne og direkte leveringsordrefakturaer styres og gennemtvinges af de parametre, der er beskrevet i [Definere parametre for bogføring af en intern ordre](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

Når du har angivet disse parametre, skal du fakturere den interne salgsordre først. De oprindelige salgsordrer og indkøbsordrer synkroniseres derefter.
