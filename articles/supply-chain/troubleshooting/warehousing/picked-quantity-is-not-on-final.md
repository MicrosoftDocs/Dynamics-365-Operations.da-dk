---
title: Du kan ikke bekræfte en forsendelse, fordi der ikke er plukket varer
description: Du kan ikke bekræfte en forsendelse, fordi der ikke er plukket varer
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938441"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Du kan ikke bekræfte en forsendelse, fordi der ikke er plukket varer

Fejlkode: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Symptomer

Når du forsøger at bekræfte en forsendelse, vises følgende fejlmeddelelse:

> Nogle af varerne, der skal bruges til lasten %1, er endnu ikke plukket og flyttet til den endelige afsendelseslokation.

Du kan derfor ikke bekræfte forsendelsen for lasten.

## <a name="cause"></a>Årsag

Lasten eller forsendelsen kan ikke bekræftes i dens aktuelle tilstand, da en af følgende betingelser kan være til stede:

- Det relaterede arbejde er endnu ikke plukket og flyttet til det endelige afsendelsessted.
- Det plukkede arbejdsantal svarer ikke til det oprettede arbejdsantal på linjen for lasten.

## <a name="resolution"></a>Løsning

Kontrollér de relaterede salgsordrer eller flytteordrer for lasten eller forsendelsen. Kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som forsendelsen ikke kan bekræftes for.
1. Vælg linjen for lasten i oversigtspanelet **Lastlinjer**.
1. Notér værdien for feltet **Antal oprettet under arbejde**.
1. under fanen **Laster** i gruppen **Relaterede oplysninger** i handlingsruden skal du vælge **Arbejde**.
1. Kontrollér, at arbejdet er udført på den endelige forsendelseslokation, og at det plukkede arbejdsantal svarer til det oprettede arbejdsantal på lastlinjen.
1. Gentag denne procedure for alle lastlinjer for at sikre, at alle kriterier er opfyldt.
