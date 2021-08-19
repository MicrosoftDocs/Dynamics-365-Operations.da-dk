---
title: Du kan ikke bekræfte en forsendelse, fordi antallet er nul
description: Du kan ikke bekræfte en forsendelse, fordi antallet er nul
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
ms.openlocfilehash: b2f9f8deaca30e318d0393fb1d7911eebf63060ccca83dc6f1de9b04b9e30e11
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712880"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>Du kan ikke bekræfte en forsendelse, fordi antallet er nul

Fejlkode: LoadLineWarningUpdatedToZero

## <a name="symptoms"></a>Symptomer

Når du forsøger at bekræfte en forsendelse, vises følgende fejlmeddelelse:

> Lastlinje for varen %1 og forsendelsen %2 er blevet opdateret til at have et antal på nul på grund af konfiguration af underlevering, som ikke tillader, at der sendes nogen mængder af denne vare.

Du kan derfor ikke bekræfte forsendelsen for lasten.

## <a name="cause"></a>Årsag

Systemet evaluerer, om det plukkede antal ligger inden for de forventede grænser baseret på plukket antal, lastlinjeantal og underleveringsprocent. Hvis det plukkede antal på lastlinjen er 0 (nul), kan du ikke bekræfte forsendelsen. Dette problem kan f.eks. forekomme, hvis arbejdet er blevet annulleret, og underleveringsprocenten på lastlinjen er 100 procent.

## <a name="resolution"></a>Løsning

Kontrollér lastlinjerne for at sikre, at underleveringsprocenten og -mængderne er tilpasset det plukkede arbejde.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som forsendelsen ikke kan bekræftes for.
1. Vælg lastlinjen for den vare, der overstiger underleveringsprocenten, i oversigtspanelet **Lastlinjer**.
1. Juster værdien i feltet **Underlevering** eller feltet **Antal** efter behov.

> [!TIP]
> Hvis problemet stadig ikke er løst, skal du muligvis udføre mere plukarbejde for de relaterede salgsordrer eller flytteordrer, indtil det tilgængelige antal stemmer med lasten eller forsendelsen.
