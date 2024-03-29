---
title: Genklassificere den kortfristede del af leasingforpligtelse
description: Denne artikel forklarer, hvordan du opretter en måneds kladdepost, så en del af leasingforpligtelsen klassificeres som kortfristet.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7c7c3f86aa5d24e9aeed89526a4b7317699e9a78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886336"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Genklassificere den kortfristede del af leasingforpligtelsen

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du opretter en måneds kladdepost, så en del af leasingforpligtelsen klassificeres som kortfristet. Når den plan, der er valgt i batchprocessen, er **Kortsigtet omposteringsleasingforpligtelse**, oprettes der en kladdepost. Denne post bruges til bogføring af den aktuelle del af en leasingforpligtelse på den sidste dag i måneden. På samme tid, bogføres en post for tilbageførsel pr. den første dag i den næste måned.

Den kortfristede del af leasingforpligtelsen vises i planen for leasingamortisering. Når kladdeposten er bogført, bliver kolonnen **Kladde, der er oprettet for passiv** tilgængelig, og kladde-id'et angives også i tidsplanen.

Udfør følgende trin for at oprette og bogføre den kortfristede passiv-omposteringskladde.

1. Gå til det **Aktivleasing \> Periodisk \> Oprettelse af batchkladde**.
2. I dialogboksen **Oprettelse af batchkladde** i feltet **Vælg tidsplan** kan du vælge **Kortfristet leasingforpligtelse**.
3. Vælg en leasinggruppe i feltet **Leasinggruppe**. Alternativt kan du vælge Kartotek-id i feltet **Kartotek-id**.
4. Aktiver parameteren **Bogfør**. Alternativt, hvis posten skal oprettes men ikke bogføres, skal denne parameter være deaktiveret.
5. Vælg **OK**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
