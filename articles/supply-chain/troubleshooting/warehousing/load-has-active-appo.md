---
title: Du kan ikke bekræfte en forsendelse på grund af problemer med kalenderen
description: Du kan ikke bekræfte en forsendelse på grund af problemer med kalenderen
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
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938443"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>Du kan ikke bekræfte en forsendelse på grund af problemer med kalenderen

Fejlkode: TRX2716

## <a name="symptoms"></a>Symptomer

Når du forsøger at bekræfte en forsendelse, vises følgende fejlmeddelelse:

> Kalendertypen %1 kræver, at aftalen %2 tjekkes ind og ud.

Du kan derfor ikke bekræfte forsendelsen for lasten.

## <a name="cause"></a>Årsag

Der findes aktive aftaler i indlæsningen. Der findes f.eks. en regel, der kræver, at chaufføren tjekker ind. Belastningen befinder sig derfor i øjeblikket i en tilstand, hvor forsendelsesbekræftelsen mislykkes.

## <a name="resolution"></a>Løsning

Du skal undersøge sagen og løse eventuelle problemer med de aktive aftaler, der er tilknyttet belastningen.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som forsendelsen ikke kan bekræftes for.
1. I handlingsruden under fanen **Transport** i gruppen **Aftaler** skal du vælge **Planlægning af aftale**.
1. Udfør ét af følgende trin:

    - Kontrollér, at chaufførens indtjekning/udtjekning er fuldført for aftalen.
    - Fuldfør eller annuller aftalen.
    - Deaktiver indstillingen **Chaufførs indtjekning er er påkrævet** for den relaterede aftaleregel.
