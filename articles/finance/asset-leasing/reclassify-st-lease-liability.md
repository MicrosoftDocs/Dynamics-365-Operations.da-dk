---
title: Genklassificere den kortfristede del af leasingforpligtelse
description: I dette emne forklares det, hvordan du opretter en måneds kladdepost, så en del af leasingforpligtelsen klassificeres som kortfristet.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ae5aebab507479775626579e8b08d68001326a06
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881560"
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
5. Vælg **OK**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
