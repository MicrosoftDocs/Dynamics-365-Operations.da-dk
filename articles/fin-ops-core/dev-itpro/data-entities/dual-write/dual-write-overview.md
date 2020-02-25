---
title: Integration næsten i realtid med Common Data Service
description: Dette emne indeholder en oversigt over integrationen mellem Finance and Operations og Common Data Service.
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
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019702"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Integration næsten i realtid med Common Data Service

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

I den nuværende digitale verden bruger professionelle økosystemer Microsoft Dynamics 365-programmer som en helhed. Da data fra personer, kunder, drift og Tingenes internet flyder ind i én kilde, er der mulighed for digitale feedbackløkker. For at opnå denne oplevelse er integration mellem Finance and Operations-apps og Dynamics 365-programmer afgørende. Nogle programmer er bygget oven på Common Data Service. Integration mellem Finance and Operations-appsdata og Common Data Service giver andre programmer muligheder for at kommunikere sammenhængende og flydende med Finance and Operations.

Finance and Operations-apps og Common Data Service leverer datasynkronisering tæt på realtid mellem Finance and Operations-apps og andre Dynamics 365-programmer via en dobbeltskrivningsstruktur. Dækningen er bred og spænder over 28 overfladeområder i programmet. Målet er at skabe én "One Dynamics 365"-brugeroplevelse gennem problemfri datastrømme, der forbinder forretningsprocesser på tværs af applikationer.

![Diagram over arkitekturoversigt](media/dual-write-overview.jpg)

Følgende værdiforslag er tilgængelige:

+ [Organisationshierarki i Common Data Service](organization-mapping.md)
+ [Firmakoncept i Common Data Service](company-data.md)
+ [Integreret debitormaster](customer-mapping.md)
+ [Integreret finans](ledger-mapping.md)
+ [Samlet produktoplevelse](product-mapping.md)
+ [Integreret kreditormaster](vendor-mapping.md)
+ [Integrerede lokationer og lagersteder](sites-warehouses-mapping.md)
+ [Integreret momsmaster](tax-mapping.md)

## <a name="system-requirements"></a>Systemkrav

Synkrone, tovejs datastrømme næsten i realtid kræver følgende versioner:

+ Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (juli 2019) med Platform update 28 eller nyere
+ Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) eller nyere

## <a name="setup-instructions"></a>Installationsvejledning

Benyt følgende fremgangsmåde for at konfigurere mellem Finance and Operations-apps og Common Data Service.
    
1. For opsætningen af dobbeltskrivningssystemet skal du se [trinvis vejledning](https://aka.ms/dualwrite-docs) til annoncering af prøveversion af dobbeltskrivning.
2. Download og Installer løsningen fra gruppen [Fin Ops og CDS-/CE-integration via dobbeltskrivning](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer. Pakken indeholder fem løsninger:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Følg udførelsesrækkefølgen for [synkronisering af indledende referencedata](initial-sync.md).
4. Hvis du støder på problemer med dobbeltskrivningssynkronisering, skal du se [Fejlfindingsvejledning til dataintegration](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Du kan ikke køre dobbeltskrivning og [Kundeemne til kontanter](../../../../supply-chain/sales-marketing/prospect-to-cash.md) side om side. Hvis du kører løsningen Kundeemne til kontanter, skal du afinstallere den. Du skal også deaktivere de skabeloner til dobbeltskrivning af debitorer og kreditorer, der er en del af løsningen Kundeemne til kontanter.
