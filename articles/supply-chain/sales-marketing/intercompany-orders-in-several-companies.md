---
title: Oprettelse af interne indkøbsordrer og salgsordrer i flere firmaer
description: Denne artikel forklarer oprettelse af interne indkøbsordrer eller salgsordrer i flere firmaer
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 6dce419126d60199bc11d4bd3209185ad779e979
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873544"
---
# <a name="creating-intercompany-purchase-and-sales-orders-in-several-companies"></a>Oprettelse af interne indkøbsordrer og salgsordrer i flere firmaer

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management er ikke begrænset til kun at håndtere ét produktionsfirma og flere salgsfirmaer. Alle firmaer, der er oprettet til intern handel, kan både være samhandelsfirmaer og produktionsfirmaer.

Hvis der er flere firmaer, der kan levere den samme vare, kan du frit vælge, hvem du vil købe fra, og opdateringerne behandles, også selvom én salgsordre bliver til flere indkøbsordrer.

På samme måde som du automatisk kan oprette en intern indkøbsordre, kan du oprette en oprindelig salgsordre i dit firma og derefter få flere interne leverandørfirmaer til at opfylde ordren ved at oprette mere end én intern indkøbsordre. Microsoft Dynamics 365 Supply Chain Management opretter automatisk interne salgsordrer i leverandørfirmaerne.

Inden det kan lade sig gøre, skal alle firmaerne være oprettet som samhandelsforhold. Kreditorfirmaerne skal oprettes i Microsoft Dynamics 365 Supply Chain Management som interne kreditorer, og de skal være den primære leverandør for den pågældende vare. I **overskriften** til salgsordren skal du markere feltet **Opret interne ordre automatisk** og feltet **Direkte levering** i oversigtspanelet **Interne indstillinger**. Dette er standardindstillingen.

Du opretter salgslinjerne på den sædvanlige måde. Når du afslutter posten, vises en meddelelse med oplysninger om, at der er oprettet interne indkøbsordrer og interne salgsordrer. Meddelelsen indeholder links til de nye ordrer. Hvis du vil se de interne salgsordrer, der er oprettet i dine leverandørfirmaer, skal du åbne de oprindelige salgsordrer og vælge under fanen **Generelt** i gruppen **Relaterede oplysninger** **Referencer**.

Hvis du åbner de interne købsordrer for leverandørerne, kan du ligeledes se, at Microsoft Dynamics 365 Supply Chain Management automatisk indsætter nummeret på den oprindelige salgsordre og den interne salgsordre for hver leverandør.

Ligeledes, hvis du åbner de interne salgsordrer for leverandørerne, kan du ligeledes se, at Microsoft Dynamics 365 Supply Chain Management automatisk indsætter nummeret på den oprindelige salgsordre og den interne købsordre for hver leverandør.

> [!NOTE]
> Hvis de bestilte varer findes i et af de interne leverandørfirmaer, men ikke i et andet, opretter Microsoft Dynamics 365 Supply Chain Management de interne ordrer for det interne leverandørfirma, hvor varerne findes og stopper ordreoprettelsen for det andet firma. Hvis det sker, vises der en notifikationsmeddelelse.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
