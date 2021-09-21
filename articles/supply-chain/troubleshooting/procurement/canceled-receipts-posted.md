---
title: Posteringer kan bogføres på en suspenderet finanskonto
description: Hvis en produktkvittering annulleres, tillader systemet, at der bogføres transaktioner på suspenderede finanskonti, selvom hovedkontiene er suspenderet
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
ms.openlocfilehash: 20df0ee4107ad62bec0dd9a683660fe2375a3dd1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475952"
---
# <a name="transactions-can-be-posted-to-a-suspended-ledger-account"></a>Posteringer kan bogføres på en suspenderet finanskonto

## <a name="symptoms"></a>Symptomer

Hvis en produktkvittering annulleres, tillader systemet, at der bogføres transaktioner på suspenderede finanskonti, selvom hovedkontiene er suspenderet.

## <a name="reproduce-the-issue"></a>Genskabe problemet

Følgende procedurer viser en måde at genskabe problemet på.

1. På siden **Kreditorparametre** skal du under fanen **Generelt** kontrollere, at indstillingen **Bogfør produktkvittering i finans** er angivet til *Ja*.
1. Opret en indkøbsordre, og tilføj en ordrelinje, der har et antal på *1.000* for et produkt.
1. Bekræft indkøbsordren.
1. Bogfør produktkvitteringen, og kontrollér bilagene.
1. Suspender de relevante hovedkonti, *200140* og *140200*.
1. Annuller den bogførte produktkvittering.
1. Bemærk, at transaktioner kan bogføres på de suspenderede finanskonti.

## <a name="resolution"></a>Løsning

Transaktioner kan bogføres på de suspenderede finanskonti, når produktkvitteringer annulleres, da denne funktionsmåde giver mulighed for korrekte bogføringer.
