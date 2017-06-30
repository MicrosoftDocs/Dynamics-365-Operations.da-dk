---
title: "Få vist omkostningsværdier for disponibel lagerbeholdning"
description: "Brug formularen Regulering af disponibel lagerbeholdning til at regulere kostværdien af det disponible lagerantal, efter at der er gennemført en lagerlukning."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7f7c1008eea83bbda96ace92cd4aedf09c8febdc
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="adjust-on-hand-inventory-cost-values"></a>Få vist omkostningsværdier for disponibel lagerbeholdning

[!include[banner](../includes/banner.md)]


Brug formularen Regulering af disponibel lagerbeholdning til at regulere kostværdien af det disponible lagerantal, efter at der er gennemført en lagerlukning.

Du kan bruge siden **Regulering af disponibel lagerbeholdning** til at regulere kostværdien af de disponible lagerantal, efter at der er gennemført en lagerlukning. **Bemærk!** Hvis du vil åbne siden **Regulering af disponibel lagerbeholdning** på siden **Lukning og regulering**, skal du vælge posten for en fuldført lagerlukningsproces og derefter klikke på **Regulering** &gt; **Disponibel**. **Eksempel:** Du har følgende posteringer i februar:

-   1. februar: en økonomisk lagertilgang for et antal på 2 til en kostpris af kr. 10,00
-   5. februar: en økonomisk lagertilgang for et antal på 1 til en kostpris af kr. 13,00
-   19. februar: en økonomisk lagerafgang for et antal på 1 til en løbende gennemsnitskostpris af kr. 11,00 pr. styk

Denne vare blev konfigureret med lagermodellen FIFO (First In, First Out), og lagerlukningen blev udført pr. 28. februar. Den økonomiske afgangspostering på kr. 11,00 udlignes mod den økonomiske tilgang, der er dateret 1. februar, og der udføres en regulering på kr. 1,00. Følgende lagertilgange indeholder åbne lagerantal:

-   1. februar: en mængde på 1 til kr. 10,00
-   5. februar: en mængde på 1 til kr. 13,00

Hvis du vil angive kostprisen for disse to varer til kr. 15,00, skal du bruge indstillingen Regulering af disponibel lagerbeholdning til at regulere de åbne disponible lagerantal med virkning fra den sidste lagerlukningsperiode. **Bemærk!** Bogføringsdatoen for reguleringen af den disponible lagerbeholdning vil være datoen for den sidste lagerlukning. Denne dato kan ikke redigeres.




