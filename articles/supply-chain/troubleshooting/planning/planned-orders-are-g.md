---
title: Ved varedisponering oprettes der ordreforslag til fantomprodukter
description: Der oprettes ordreforslag til fantomprodukter, når varedisponeringskørslen har fundet sted.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f3170bcb723e2d7483258bb0ecf786e62f2aa3d196745074c2ac554bc212ec55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741998"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Ved varedisponering oprettes der ordreforslag til fantomprodukter

KB-nummer: 4614729

## <a name="symptoms"></a>Symptomer

Der oprettes ordreforslag til fantomprodukter, når varedisponeringskørslen har fundet sted.

## <a name="resolution"></a>Løsning

Valg for **Fantom**-indstillingen for frigivne produkter bestemmer standardlinjetypen på styklisten. Når indstillingen **Fantom** er angivet til *Ja*, opretter systemet stadig ordreforslag for varen, men indstillingen **Direkte afledt behov** for hvert ordreforslag angives til *Ja*. Produktionsordreforslaget kan derfor ikke autoriseres alene. Det medtages i stedet altid automatisk, når den overordnede produktionsordre autoriseres automatisk. Styklistelinjerne i fantomordreforslaget medtages desuden i styklisten for den overordnede produktionsordre.
