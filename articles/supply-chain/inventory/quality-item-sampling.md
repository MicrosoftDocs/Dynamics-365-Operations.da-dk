---
title: Varestikprøve for kvalitetsstyring
description: Dette emne beskriver, hvordan du konfigurerer varestikprøver.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea749c470ab1d80f1f3974596a2cd4a1f5b7b32d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578482"
---
# <a name="quality-management-item-sampling"></a>Varestikprøve for kvalitetsstyring

[!include [banner](../includes/banner.md)]

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
