---
title: Integration næsten i realtid med Common Data Service
description: Dette emne indeholder en oversigt over integrationen mellem Finance and Operations-apps og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.openlocfilehash: 11a5792c9c039eb76337309ef2fdb2b994ce191a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772381"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Integration næsten i realtid med Common Data Service

[!include [banner](../includes/banner.md)]

I den nuværende digitale verden bruger professionelle økosystemer Microsoft Dynamics 365-programmer som en helhed. Da data fra personer, kunder, drift og Tingenes internet flyder ind i én kilde, er der mulighed for digitale feedbackløkker. For at opnå denne oplevelse er integration mellem Finance and Operations-apps og Dynamics 365-programmer afgørende. Nogle programmer er bygget oven på Common Data Service. Integration mellem Finance and Operations-appdata og Common Data Service giver andre programmer mulighed for at kommunikere sammenhængende og flydende med Finance and Operations.

Finance and Operations-apps og Common Data Service leverer datasynkronisering tæt på realtid mellem Finance and Operations-apps og andre Dynamics 365-programmer via en dobbeltskrivningsstruktur. Dækningen er bred og spænder over 28 overfladeområder i programmet. Målet er at skabe én "One Dynamics 365"-brugeroplevelse gennem problemfri datastrømme, der forbinder forretningsprocesser på tværs af applikationer.

![Diagram over arkitekturoversigt](media/dual-write-overview.jpg)

Følgende værdiforslag er tilgængelige:

+ [Organisationshierarki i Common Data Service](dual-write-organization.md)
+ [Firmakoncept i Common Data Service](dual-write-company.md)
+ [Integreret debitormaster](dual-write-customer.md)
+ [Integreret finans](dual-write-ledger.md)
+ [Samlet produktoplevelse](dual-write-product.md)
+ [Integreret kreditormaster](dual-write-vendor.md)
+ [Integrerede lokationer og lagersteder](dual-write-sites-and-warehouses.md)
+ [Integreret momsmaster](dual-write-tax.md)

## <a name="system-requirements"></a>Systemkrav

Synkrone, tovejs datastrømme næsten i realtid kræver følgende versioner:

+ Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (juli 2019) med Platform update 28 eller nyere
+ Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) eller nyere

## <a name="setup-instructions"></a>Installationsvejledning

Følg disse trin for at konfigurere integrationen mellem Finance and Operations-apps og Common Data Service.
    
1. For opsætningen af dobbeltskrivningssystemet skal du se [trinvis vejledning](https://aka.ms/dualwrite-docs) til annoncering af prøveversion af dobbeltskrivning.
2. Download og installer løsningen fra [Finance and Operations, Common Data Service og Customer Engagement-integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer-gruppen. Pakken indeholder fem løsninger:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Følg udførelsesrækkefølgen for [synkronisering af indledende referencedata](dual-write-initial.md).
4. Hvis du støder på problemer med dobbeltskrivningssynkronisering, skal du se [Fejlfindingsvejledning til dataintegration](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Du kan ikke køre dobbeltskrivning og [Kundeemne til kontanter](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side om side. Hvis du kører løsningen Kundeemne til kontanter, skal du afinstallere den. Du skal også deaktivere de skabeloner til dobbeltskrivning af debitorer og kreditorer, der er en del af løsningen Kundeemne til kontanter.
