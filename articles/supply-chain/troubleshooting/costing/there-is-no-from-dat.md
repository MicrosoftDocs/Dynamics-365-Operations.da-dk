---
title: Der er ingen værdi for Fra-dato under fanen Aktive priser på siden Varepris
description: Der er ingen værdi for Fra-dato under fanen Aktive priser på siden Varepris.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026386"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>Der er ingen værdi for Fra-dato under fanen Aktive priser på siden Varepris

KB-nummer: 4613548

## <a name="symptoms"></a>Symptomer

Der er ingen værdi for **Fra-dato** under fanen **Aktive priser** på siden **Varepris**.

## <a name="resolution"></a>Løsning

Værdien for **Fra dato** (ikrafttrædelsesdato), der er angivet på den ventende pris, overføres ikke til den aktive pris.

Når en vares omkostningspost angives først, har den status *Venter* og en ønsket ikrafttrædelsesdato. Når du aktiverer omkostningsposten, opdateres statussen til *Aktiv*, og ikrafttrædelsesdatoen opdateres til aktiveringsdatoen. Aktiveringsdatoen for den aktive pris er derfor altid den faktiske dato for aktiveringen.

Du kan finde flere oplysninger i [Oversigt over efterkalkulationsversioner](../../cost-management/costing-versions.md).
