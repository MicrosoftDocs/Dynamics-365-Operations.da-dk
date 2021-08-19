---
title: Du kan ikke bekræfte en forsendelse, fordi kunden er på hold
description: Du kan ikke bekræfte en forsendelse, fordi kunden er på hold.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 82b28e7cfd8c88e453cdd09398f5a92f605eab15a17d33defa0b9729a53c05b6
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012149"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>Du kan ikke bekræfte en forsendelse, fordi kunden er på hold

Fejlkode: WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>Symptomer

Når du forsøger at bekræfte en forsendelse, vises følgende fejlmeddelelse:

> Forsendelsen %1 kan ikke bekræftes, fordi kunden er på hold til %2.

Du kan derfor ikke bekræfte forsendelsen for lasten.

## <a name="cause"></a>Årsag

Debitorkontoen for lasten eller forsendelsen er på hold. Kundens status forhindrer derfor forsendelsesbekræftelse.

## <a name="resolution"></a>Løsning

Du kan bruge følgende procedure til at fjerne spærringen af debitorkontoen.

1. Gå til **Debitorer \> Kunder \> Alle kunder**.
1. Åbn den debitorkonto, som forsendelsen ikke kan bekræftes for.
1. Angiv feltet **Fakturering og levering er sat på hold** til **Nej** i oversigtspanelet *Kredit og rykkere*.
1. Gentag denne procedure for alle spærrede kunder for lasten.
