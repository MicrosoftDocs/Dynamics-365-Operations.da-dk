---
title: Udførelsesrækkefølge for indledende synkronisering af Finance and Operations og Common Data Service
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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797292"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a>Udførelsesrækkefølge for indledende synkronisering af Finance and Operations og Common Data Service

Før du bruger dataintegration, skal du oprette de oprindelige data, der kræves til debitorer, kreditorer og kontakter. Hvis du for eksempel vil oprette et nyt **Leverandørgruppe**-element og angive **Betalingsbetingelser** som **Net30**, skal du, før du forsøger at oprette **Leverandørgruppe**-elementet, sikre dig, at **Net30** findes i både Finance and Operations og Common Data Service. (I fremtiden vil vi frigive en dobbeltskrivningsplatform med en funktionalitet kaldet **Første synkronisering**. Den vil udføre en engangsdatasynkronisering mellem Finance and Operations og Common Data Service som en del af dobbeltskrivningsopsætningen).

Tips: Vi udgiver et kort med dobbeltskrivning for alle referencedata, herunder **Betalingsbetingelser** (betalingsvilkår). Hvis du allerede har de første data i ét system, kan en lille opdateringshandling på en post udløse dobbeltskrivning på den pågældende post. 

Du skal følge følgende prioriteringsrækkefølge og sørge for, at de første data er tilgængelige på både Finance and Operations og Common Data Service.   

## <a name="vendor"></a>Leverandør

Udførelsesrækkefølgen for leverandøren er:

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a>Kunde (organisation)

Udførelsesrækkefølgen for kunden er:

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a>Kontakt (person)

Udførelsesrækkefølgen for kontakten er:

```
Customer
Vendor               
```
