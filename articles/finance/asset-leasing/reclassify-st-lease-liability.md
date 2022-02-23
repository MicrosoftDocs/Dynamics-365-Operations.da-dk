---
title: Genklassificere den kortfristede del af leasingforpligtelse
description: I dette emne forklares det, hvordan du opretter en måneds kladdepost, så en del af leasingforpligtelsen klassificeres som kortfristet.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 46bcd396c93bc1d2944241165d438f8ccc013e20
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441753"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Genklassificere den kortfristede del af leasingforpligtelsen

[!include [banner](../includes/banner.md)]

I dette emne forklares det, hvordan du opretter en måneds kladdepost, så en del af leasingforpligtelsen klassificeres som kortfristet. Når den plan, der er valgt i batchprocessen, er **Kortsigtet omposteringsleasingforpligtelse**, oprettes der en kladdepost. Denne post bruges til bogføring af den aktuelle del af en leasingforpligtelse på den sidste dag i måneden. På samme tid, bogføres en post for tilbageførsel pr. den første dag i den næste måned.

Den kortfristede del af leasingforpligtelsen vises i planen for leasingamortisering. Når kladdeposten er bogført, bliver kolonnen **Kladde, der er oprettet for passiv** tilgængelig, og kladde-id'et angives også i tidsplanen.

Udfør følgende trin for at oprette og bogføre den kortfristede passiv-omposteringskladde.

1. Gå til det **Aktivleasing \> Periodisk \> Oprettelse af batchkladde**.
2. I dialogboksen **Oprettelse af batchkladde** i feltet **Vælg tidsplan** kan du vælge **Kortfristet leasingforpligtelse**.
3. Vælg en leasinggruppe i feltet **Leasinggruppe**. Alternativt kan du vælge Kartotek-id i feltet **Kartotek-id**.
4. Aktiver parameteren **Bogfør**. Alternativt, hvis posten skal oprettes men ikke bogføres, skal denne parameter være deaktiveret.
5. Aktiver parameteren **Vis udskrift før bogføring** for at få vist posten, før den bogføres.
6. Vælg **OK**.
