---
title: Du kan ikke bekræfte en forsendelse, fordi antallet overstiger underleveringsprocenten
description: Du kan ikke bekræfte en forsendelse, fordi antallet overstiger underleveringsprocenten
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 625003731485329b93f5f9454ccece580c889613
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123813"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a>Du kan ikke bekræfte en forsendelse, fordi antallet overstiger underleveringsprocenten

Fejlkode: WAX1686

## <a name="symptoms"></a>Symptomer

Når du forsøger at bekræfte en forsendelse, vises følgende fejlmeddelelse:

> Forsendelsen for last %1 kunne ikke bekræftes, da antallet for varen %2 overstiger den procentdel, der er defineret for underlevering.

Du kan derfor ikke bekræfte forsendelsen for lasten.

## <a name="cause"></a>Årsag

Antallet for lasten eller forsendelsen er kun delvist plukket. Antallet er i øjeblikket mindre end det plukkede antal med en procentdel, der ligger uden for den tilladte underleveringsprocent.

## <a name="resolution"></a>Løsning

Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:

- Angiv antallet for lastlinjen.
- Angiv underleveringsprocenten.

### <a name="set-the-load-line-quantity"></a>Angive antallet for lastlinjen

Hvis du vil angive antallet for lastlinjen, skal du benytte følgende fremgangsmåde.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som forsendelsen ikke kan bekræftes for.
1. Vælg lastlinjen for den vare, der overstiger underleveringsprocenten, i oversigtspanelet **Lastlinjer**.
1. I oversigtspanelet **Linjedetaljer** skal du vælge **Ordre**.
1. I feltet **Antal** skal du angive værdien til det plukkede antal (dvs. værdien for **Antal oprettet under arbejde**), så der kan udstedes en forsendelsesbekræftelse.

### <a name="set-the-underdelivery-percentage"></a>Angive underleveringsprocenten

Hvis du vil angive overleveringsprocenten, skal du benytte følgende fremgangsmåde.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som forsendelsen ikke kan bekræftes for.
1. Vælg lastlinjen for den vare, der overstiger underleveringsprocenten, i oversigtspanelet **Lastlinjer**.
1. I oversigtspanelet **Linjedetaljer** skal du vælge **Generelt**.
1. I feltet **Underlevering** skal du angive værdien til en større procentdel, der tager højde for det antal, der er plukket i forhold til lastantallet, så der kan udstedes en forsendelsesbekræftelse.
