---
title: Omregning af intern valuta
description: Denne artikel forklarer valutaomregninger for interne transaktioner
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
ms.openlocfilehash: 41bfafc0dcb3bd356931b67dc63b717c0d098116
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851472"
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
