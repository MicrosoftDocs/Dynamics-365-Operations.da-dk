---
title: Omregning af intern valuta
description: Dette emne forklarer valutaomregninger for interne transaktioner
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f0af05c324bb67744ba6650e3d7a4ba8b958040e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671892"
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
