---
title: Reservationer kan ikke fjernes, når en ordre annulleres
description: Hvis arbejdet er knyttet til en salgsordre, kan du ikke annullere salgsordren, før arbejdet er annulleret og tilbageført. Hvis du vil gøre dette, skal du udføre disse tre trin.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a8d947e64568246dba5eff3c21fd3920b6494b73
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475915"
---
# <a name="reservations-cannot-be-removed-when-canceling-an-order"></a>Reservationer kan ikke fjernes, når en ordre annulleres

## <a name="symptoms"></a>Symptomer

Hvis der er knyttet arbejde til en salgsordre, og du forsøger at annullere den pågældende ordre, får du vist følgende fejlmeddelelse:

> Reservationer kan ikke fjernes, fordi der er oprettet arbejde, som er afhængigt af reservationerne.

Hvis arbejdet er knyttet til en salgsordre, kan du ikke annullere salgsordren, før arbejdet er annulleret og tilbageført. Dette krav gælder, selvom det arbejde, der er tilknyttet salgsordren, er lukket.

## <a name="resolution"></a>Løsning

Følg disse trin for at løse dette problem:

1. Annuller arbejdet, og læg lageret tilbage på den ønskede lokation. Gå til den relevante last af salgsordren, og vælg enten **Reducer plukket antal** på lastlinjen eller **Tilbagefør arbejde** i handlingsruden.

    Arbejdet har nu statussen *Annulleret*, og der oprettes og behandles automatisk nyt arbejde for lagerbevægelse for at bringe lagerbeholdningen tilbage til den lokation, der blev angivet, da den blev tilbageført.

2. Slet lasten. Forsendelsen slettes også.

3. Du skulle nu kunne gå til salgsordren og annullere den.
