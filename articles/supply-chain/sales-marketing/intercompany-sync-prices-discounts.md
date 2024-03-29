---
title: Synkronisere interne priser og rabatter
description: Denne artikel forklarer synkronisering af priser og rabatter for interne salgsordrer og indkøbsordrer
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
ms.openlocfilehash: 64130c400212a819f931cc36459667e4d7c83f32
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905683"
---
# <a name="synchronize-intercompany-prices-and-discounts"></a>Synkronisere interne priser og rabatter

[!include [banner](../../includes/banner.md)]

Rabatter og priser synkroniseres altid mellem den interne salgsordre og den interne indkøbsordre. Du kan også vælge at synkronisere prisen og rabatter til og fra den oprindelige salgsordre, så ordrerne har samme priser og rabatter. Det kan du gøre fra siden **Intern handel**, som du får adgang til fra fanen **Generelt** på listesiden **Alle kunder** - enten fra **Salg og marketing** eller fra **Indkøb og forsyning**.

Feltet **Pris og rabat** synkroniseres til den interne salgsordrelinje. Det betyder, at du ved at markere afkrydsningsfelterne **Tillad prisredigering** og **Tillad rabatredigering** tillader en ændring i den interne salgsordre og den interne indkøbsordre. En ændring i enhedsprisen, prisenheden eller salgsgebyret på den interne salgsordre bestemmer prisen på den interne indkøbsordrelinje.

Hvis afkrydsningsfelterne **Tillad prisredigering** og **Tillad rabatredigering** er markeret på den interne salgsordre eller den interne indkøbsordre, kan du ændre prisen eller rabatten manuelt på ordren. Det kan du ikke, hvis de ikke er markeret.

Hvis afkrydsningsfelterne **Tillad prisredigering** og **Tillad rabatredigering** ikke er markeret på den interne salgsordre eller den interne indkøbsordre, kan du ikke ændre prisen (eller gebyrer) eller rabatten manuelt på en intern handelsordre.

Hvis afkrydsningsfelterne **Tillad prisredigering** og **Tillad rabatredigering** ikke er markeret på den interne købsordre, kan du ikke ændre prisen (eller gebyrer) eller rabatten manuelt på en intern købsordre.

Hvis afkrydsningsfelterne **Tillad prisredigering** og **Tillad rabatredigering** er markeret på både den interne indkøbsordre og den interne salgsordre, kan du ændre manuelt ændre begge ordrer. Men det kan medføre en situation, hvor opdateringer, der udføres af én person, tilsidesættes af opdateringer, der udføres af en anden i et andet firma på samme ordre.

> [!NOTE]
> Hvis du har markeret afkrydsningsfeltet **Pris og rabat** både på den interne indkøbsordre og den interne salgsordre, kan du ikke bestemme over prisfastsættelsen.

Hvis du vil undgå denne type konflikter, er det bedst at tillade ændringen af priser og rabatter på den interne salgsordre eller interne indkøbsordre. Dette gør du ved at aktivere felterne **Tillad prisredigering** og **Tillad rabatredigering** i en af disse ordrer.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
