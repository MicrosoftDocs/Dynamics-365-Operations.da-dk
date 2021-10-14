---
title: Omregning af intern valuta
description: Dette emne forklarer valutaomregninger for interne transaktioner
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 540849003d532ef2f0905c18332d9cb82a04cf7c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548180"
---
# <a name="intercompany-currency-conversions"></a>Omregning af intern valuta

[!include [banner](../../includes/banner.md)]

Når der er forskel på valutakoden på den oprindelige salgsordre og den interne indkøbsordre, valutaomregnes følgende felter, hvis synkronisering er aktiveret:

- **Enhedspris**
- **Salgsgebyrer** eller **gebyrer på indkøb**
- **Diskontering**
- **Samkøbsrabat**

Disse felter synkroniseres derefter med den interne salgsordrelinje.

Men da valutaen i den interne indkøbsordre og den interne salgsordre altid er synkroniseret, synkroniseres følgende felter uden omregning af valuta:

- **Enhedspris**
- **Salgsgebyrer** eller **gebyrer på indkøb**
- **Diskontering**
- **Rabatprocentdel**
- **Samkøbsrabat**
- **Samkøbsrabatprocent**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
