---
title: "Få vist omkostningsværdier for disponibel lagerbeholdning"
description: "Brug formularen Regulering af disponibel lagerbeholdning til at regulere kostværdien af det disponible lagerantal, efter at der er gennemført en lagerlukning."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d1ef775c9783b975fd0f852dc7112506d3897605
ms.lasthandoff: 03/31/2017


---

# <a name="adjust-on-hand-inventory-cost-values"></a>Få vist omkostningsværdier for disponibel lagerbeholdning

Brug formularen Regulering af disponibel lagerbeholdning til at regulere kostværdien af det disponible lagerantal, efter at der er gennemført en lagerlukning.

Du kan bruge siden **Regulering af disponibel lagerbeholdning** til at regulere kostværdien af de disponible lagerantal, efter at der er gennemført en lagerlukning. **Bemærk:** at åbne den **regulering af disponibel lagerbeholdning** skal den **lukning og regulering** side, vælge en post for en fuldført lagerlukningsproces, og klik derefter på **justering af**&gt;**disponible**. **Eksempel:** Du har følgende posteringer i februar:

-   1. februar: en økonomisk lagertilgang for et antal på 2 til en kostpris af kr. 10,00
-   5. februar: en økonomisk lagertilgang for et antal på 1 til en kostpris af kr. 13,00
-   19. februar: en økonomisk lagerafgang for et antal på 1 til en løbende gennemsnitskostpris af kr. 11,00 pr. styk

Denne vare blev konfigureret med lagermodellen FIFO (First In, First Out), og lagerlukningen blev udført pr. 28. februar. Den økonomiske afgangspostering af USD 11.00 udlignes mod den økonomiske tilgang, der er dateret 1, og der foretages en regulering af USD 1.00. Følgende lagertilgange indeholder åbne lagerantal:

-   1. februar: en mængde på 1 til kr. 10,00
-   5. februar: en mængde på 1 til kr. 13,00

Hvis du vil angive kostprisen for disse to varer til kr. 15,00, skal du bruge indstillingen Regulering af disponibel lagerbeholdning til at regulere de åbne disponible lagerantal med virkning fra den sidste lagerlukningsperiode. **Bemærk!** Bogføringsdatoen for reguleringen af den disponible lagerbeholdning vil være datoen for den sidste lagerlukning. Denne dato kan ikke redigeres.

