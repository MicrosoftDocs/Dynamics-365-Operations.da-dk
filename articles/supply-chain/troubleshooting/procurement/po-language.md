---
title: Indkøbsordrer afspejler ikke den juridiske enheds sprogindstillinger
description: Produktnavnet på en indkøbsordre vises på systemsproget i stedet for det sprog, der er angivet for den juridiske enhed, hvor indkøbsordren er oprettet
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4deec493b5480dc570ac82876243bc31a2ae87aa
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475893"
---
# <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Indkøbsordrer afspejler ikke den juridiske enheds sprogindstillinger


## <a name="symptoms"></a>Symptomer

Produktnavnet på en indkøbsordre vises på systemsproget i stedet for det sprog, der er angivet for den juridiske enhed, hvor indkøbsordren er oprettet.

## <a name="reproduce-the-issue"></a>Genskabe problemet

Følgende procedurer viser en måde at genskabe problemet på.

1. Indstil systemsproget til *EN-US* (amerikansk engelsk).
1. Sørg for, at der findes et produkt, hvor sprogene *EN-US* og *DK* (dansk) bruges til oversættelser af produktnavnet.
1. Skift sproget for en juridisk enhed til *DK*.
1. Opret en indkøbsordre, der indeholder produktet, i den juridiske enhed, hvor *DK* er angivet som sprog.
1. Bemærk, at produktnavnet stadig vises på amerikansk engelsk (systemsproget).

## <a name="resolution"></a>Løsning

Denne funktionsmåde er tilsigtet. På indkøbsordrer vises produktet altid på systemsproget. Indkøbsordresproget bruges, når der oprettes en bekræftelsesjournal.
