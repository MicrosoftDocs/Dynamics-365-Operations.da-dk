---
title: Synkronisere interne gebyrer
description: Dette emne forklarer synkronisering af interne gebyrer
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
ms.openlocfilehash: 2c7f60786743cf750b2bb17ccc0dadf71d859766
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678569"
---
# <a name="synchronize-intercompany-charges"></a>Synkronisere interne gebyrer

[!include [banner](../../includes/banner.md)]

Gebyrer synkroniseres kun mellem den interne salgsordre og den interne indkøbsordre, og synkronisering finder altid sted.

Hvis afkrydsningsfeltet **Tillad prisredigering** er markeret på den interne indkøbsordre eller den interne salgsordre, kan du manuelt føje et gebyr til den interne salgsordre eller den interne indkøbsordre. Det kan du ikke, hvis de ikke er markeret.

Hvis feltet **Tillad prisredigering** ikke er valgt i den interne salgsordre, kan du ikke manuelt føje tillæg til en intern salgsordre.

Hvis feltet **Tillad prisredigering** ikke er markeret i den interne indkøbsordre, kan du ikke føje et gebyr til den interne indkøbsordre.

Hvis afkrydsningsfeltet **Tillad prisredigering** er markeret i både den interne indkøbsordre og den interne salgsordre, kan du manuelt føje gebyrer til begge ordrer. Dette kan dog medføre, at mange gebyrer tilføjes forkert.

Det er lettest at undgå konflikter af denne type ved at tillade, at gebyrer føjes til enten den interne salgsordre eller den interne indkøbsordre, men ikke til dem begge.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
