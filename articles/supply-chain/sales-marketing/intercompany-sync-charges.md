---
title: Synkronisere interne gebyrer
description: Denne artikel forklarer synkronisering af interne gebyrer
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
ms.openlocfilehash: e7b3de3d7da7be6c1c8b5c3842862e7bccd78277
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857280"
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
