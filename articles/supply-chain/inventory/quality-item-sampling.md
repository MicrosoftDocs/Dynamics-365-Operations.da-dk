---
title: Varestikprøve for kvalitetsstyring
description: Dette emne beskriver, hvordan du konfigurerer varestikprøver.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956587"
---
# <a name="quality-management-item-sampling"></a>Varestikprøve for kvalitetsstyring

Varestikprøver bruges som del af kvalitetssikringen. Den definerer mængden af det aktuelle fysiske lager, som skal inspiceres. Varestikprøver kan baseres på faste antal, en procentdel eller hele varenummeret.

## <a name="set-up-item-sampling"></a>Konfigurer vareprøve

Benyt følgende fremgangsmåde for at konfigurere varestikprøve.

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Vareprøve**.
1. Vælg **Ny**.
1. Indtast en værdi i feltet **Varestikprøve**.
1. Indtast en værdi i feltet **Beskrivelse**.
1. Angiv et tal i feltet **Værdi**. Denne værdi er relateret til den angivne værdi for det antal, der er valgt i det tilstødende felt.
1. Markér afkrydsningsfeltet **Fuld blokering** i sektionen **Proces**, hvis hele parti- eller ordrelinjeantallet skal blokeres, når en test er mislykket. Hvis dette afkrydsningsfelt ikke er markeret, blokeres kun varerne i kvalitetsordren, når en test mislykkes.
1. Vælg **Gem**.
1. Luk siden.

> [!NOTE]
> Funktionen *Kvalitetsstyring for lagerstedsprocesser* indeholder yderligere vareprøveegenskaber. Den tilføjer et begreb for *varestikprøves omfang* og gør det muligt at definere et helt varenummer som specifikation af antallet. Hvis du har aktiveret denne funktion, skal du se [Kvalitetsstyring for lagerstedsprocesser](quality-management-for-warehouses-processes.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
