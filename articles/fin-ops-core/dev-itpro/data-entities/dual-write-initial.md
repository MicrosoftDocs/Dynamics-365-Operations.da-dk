---
title: Udførelsesrækkefølge for indledende synkronisering af Finance and Operations-apps og Common Data Service
description: Dette emne angiver den synkroniseringsrækkefølge, du skal følge for at oprette de første data.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: cf444ef1192fed3a6a49282da37374dd8c443356
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769631"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a>Udførelsesrækkefølge for indledende synkronisering af Finance and Operations-apps og Common Data Service

[!include [banner](../includes/banner.md)]

Før du bruger dataintegration, skal du oprette de første data, der kræves til debitorer, kreditorer og kontakter. Du kan f.eks. oprette en ny **Leverandørgruppe** og angive dens **Betalingsbetingelser** til **Net30**. I dette tilfælde skal du sikre dig, at **Net30** findes i både programmet og Common Data Service, inden du forsøger at oprette elementet **Leverandørgruppe**. (I fremtiden vil Microsoft frigive en dobbeltskrivningsplatform med en funktionalitet kaldet Første synkronisering. Den vil udføre en engangsdatasynkronisering mellem programmet og Common Data Service som en del af dobbeltskrivningsopsætningen).

> [!TIP]
> Microsoft frigiver et kort med dobbeltskrivning for alle referencedata, herunder **Betalingsbetingelser** (betalingsvilkår). Hvis du allerede har de første data i ét system, kan en lille opdateringshandling på en post udløse dobbeltskrivning på den pågældende post.

Du skal følge nedenstående prioriteringsrækkefølge og sørge for, at de første data er tilgængelige i både programmet og Common Data Service.

## <a name="vendor"></a>Leverandør

Her er afviklingsrækkefølgen for objektet **Leverandør**:

1. Leverandørgruppe

    1. Betalingsbetingelse

        1. Betalingsdag og -linjer
        2. Betalingsplan

2. Kreditorbetalingsmetode

## <a name="customer-organization"></a>Kunde (organisation)

Her er afviklingsrækkefølgen for objektet **Kunde**:

1. Kundegruppe

    1. Betalingsbetingelse

        1. Betalingsdag og -linjer
        2. Betaling 

2. Debitorbetalingsmetode

## <a name="contact-person"></a>Kontakt (person)

Her er afviklingsrækkefølgen for objektet **Kontakt**:

1. Debitor 
2. Leverandør
