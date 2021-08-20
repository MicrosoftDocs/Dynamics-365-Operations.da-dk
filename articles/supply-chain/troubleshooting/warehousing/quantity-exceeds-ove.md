---
title: Du kan ikke bekræfte en forsendelse, fordi antallet overstiger overleveringsprocenten
description: Du kan ikke bekræfte en forsendelse, fordi antallet overstiger overleveringsprocenten
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b25050572662afebbeaa39fa5a96e70cef618ac671dceba189fab1315480ede2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755149"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a>Du kan ikke bekræfte en forsendelse, fordi antallet overstiger overleveringsprocenten

Fejlkode: WAX1687

## <a name="symptoms"></a>Symptomer

Når du forsøger at bekræfte en forsendelse, vises følgende fejlmeddelelse:

> Forsendelsen for last %1 kunne ikke bekræftes, da antallet for varen %2 overstiger den procentdel, der er defineret for overlevering.

Du kan derfor ikke bekræfte forsendelsen for lasten.

## <a name="cause"></a>Årsag

Antallet for lasten eller forsendelsen er kun delvist plukket. Antallet er i øjeblikket større end det plukkede antal med en procentdel, der ligger uden for den tilladte overleveringsprocent.

## <a name="resolution"></a>Løsning

Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:

- Angiv antallet for lastlinjen.
- Angiv overleveringsprocenten.

### <a name="set-the-load-line-quantity"></a>Angive antallet for lastlinjen

Hvis du vil angive antallet for lastlinjen, skal du benytte følgende fremgangsmåde.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som forsendelsen ikke kan bekræftes for.
1. Vælg lastlinjen for den vare, der overstiger overleveringsprocenten, i oversigtspanelet **Lastlinjer**.
1. I oversigtspanelet **Linjedetaljer** skal du vælge **Ordre**.
1. I feltet **Antal** skal du angive værdien til det plukkede antal (dvs. værdien for **Antal oprettet under arbejde**), så der kan udstedes en forsendelsesbekræftelse.

### <a name="set-the-overdelivery-percentage"></a>Angive overleveringsprocenten

Hvis du vil angive overleveringsprocenten, skal du benytte følgende fremgangsmåde.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som forsendelsen ikke kan bekræftes for.
1. Vælg lastlinjen for den vare, der overstiger overleveringsprocenten, i oversigtspanelet **Lastlinjer**.
1. I oversigtspanelet **Linjedetaljer** skal du vælge **Generelt**.
1. I feltet **Overlevering** skal du angive værdien til en større procentdel, der tager højde for det antal, der er plukket i forhold til lastantallet, så der kan udstedes en forsendelsesbekræftelse.
