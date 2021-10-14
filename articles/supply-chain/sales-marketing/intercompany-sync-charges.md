---
title: Synkronisere interne gebyrer
description: Dette emne forklarer synkronisering af interne gebyrer
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c4854b698c8046fc603454c4d9d7059c938c70b3
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548174"
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
