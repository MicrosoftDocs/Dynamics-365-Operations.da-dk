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
ms.openlocfilehash: 30c485be79be5ebbec8b51272b8bbe6e0c7df9d81bbaaaef316dbfede03abf68
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756745"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Du kan ikke fakturere en kundehenvendt salgsordre

KB-nummer: 4611793

## <a name="symptoms"></a>Symptomer

Du kan ikke længere fakturere den oprindelige salgsordre og den oprindelige indkøbsordre for direkte levering, når du har aktiveret indstillingen **Bogfør faktura automatisk** på siden **Intern** for en leverandør.

## <a name="resolution"></a>Løsning

Synkroniseringsfunktionsmåden for interne og direkte leveringsordrefakturaer styres og gennemtvinges af de parametre, der er beskrevet i [Definere parametre for bogføring af en intern ordre](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

Når du har angivet disse parametre, skal du fakturere den interne salgsordre først. De oprindelige salgsordrer og indkøbsordrer synkroniseres derefter.
