---
title: En købsordrekvittering omfatter ikke alle gebyrer
description: En købsordrekvittering omfatter ikke alle gebyrer
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475862"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>En købsordrekvittering omfatter ikke alle gebyrer

## <a name="symptoms"></a>Symptomer

Når du modtager en indkøbsordre, er det ikke alle gebyrer, der medtages i tilgangen.

### <a name="reproduce-the-issue"></a>Genskabe problemet

Følgende procedurer viser en måde at genskabe problemet på.

1. På siden **Indkøbs- og forsyningsparametre** skal du under fanen **Levering** kontrollere, at indstillingen **Generér gebyrer på produktkvittering** er angivet til *Ja*.
1. Opret en indkøbsordre, der inkluderer gebyrer.
1. Bekræft indkøbsordren.
1. Modtag indkøbsordren.
1. Kig på den kvitteringstotalen, og sammenlign den med den forventede total.
1. Bemærk, at ikke alle gebyrer er medtaget i købsordrekvitteringen.

## <a name="resolution"></a>Løsning

Løsningen afhænger af den måde, som de forskellige gebyrer er konfigureret på. Du kan finde oplysninger om, hvordan du konfigurerer gebyrer, så de opfylder dine behov, i følgende blogindlæg: [Bogføre diverse gebyrer på tidspunktet for produktmodtagelse](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
