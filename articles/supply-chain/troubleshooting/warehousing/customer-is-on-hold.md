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
ms.openlocfilehash: 801778fc8f04b106bf168a3dcd5a89767a837740
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344258"
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
