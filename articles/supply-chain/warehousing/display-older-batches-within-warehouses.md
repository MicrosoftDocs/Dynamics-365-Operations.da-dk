---
title: Konfigurere visning af ældre batches på lagerstedet på en mobilenhed
description: Denne artikel beskriver, hvordan du konfigurerer en mobilenhed til at vise en liste over lokaliteter med navne, der er ældre end den aktuelle lokalitet af en arbejdslinje.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5788b42483f2c3046b0d20f45115b98d62cce213
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900529"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>Konfigurere visning af ældre batches på lagerstedet på en mobilenhed

[!include [banner](../includes/banner.md)]

Med konfigurationen **Visning af ældre batches på lagersted** kan du få vist en liste over lokaliteter med batches, der er ældre end den aktuelle lokalitet af arbejdslinjen. Listen over de lokaliteter, der vises, indeholder oplysninger om de ældre batches på lokaliteten med udløbsdatoen og det fysiske lager for hvert batch. Du kan vælge at plukke fra en ny lokalitet eller fortsætte med at plukke fra den aktuelle lokalitet. 
- Pluk fra en ny lokalitet - Hvis du vælger en ny lokalitet, der skal plukkes fra, opdateres den aktuelle arbejdslinje og bruger den nye lokalitet, og arbejde fortsætter som normalt med den nye lokalitet. Den nye lokalitet skal have tilstrækkeligt stort disponibelt antal for hele arbejdslinjen for at være gyldig. Hvis behovsantallet ikke er tilgængeligt, bliver arbejdslinjen ikke opdateret, og listen vises. 
- Fortsætte med pluk fra den aktuelle lokalitet – Hvis du fortsætter med den aktuelle arbejdslinjelokalitet, bliver antal for arbejdslinjen fortsat plukket fra den oprindelige lokalitet.

## <a name="where-it-applies"></a>Hvor det er relevant
Visning af ældre batches på lagerstedet konfigureres i menupunkter på en mobilenhed og påvirker pluk for-batchet under varer.

## <a name="set-up-display-older-batches-within-warehouse"></a>Konfigurere Visning af ældre batches på lagerstedet
Konfigurationen **Visning af ældre batches på lagerstedet** er tilgængelig i menupunkter på en mobilenhed, når indstillingen **Pluk den ældste batch** er sat til **Advar**.

- Under **Lokationsstyring** > **Konfiguration** > **Mobilenhed** > **Menupunkter i mobilenhed** skal du indstille **Brug eksisterende arbejde** til **Ja** for menupunktet og vælge **Advar** i feltet **Pluk den ældste batch**. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]