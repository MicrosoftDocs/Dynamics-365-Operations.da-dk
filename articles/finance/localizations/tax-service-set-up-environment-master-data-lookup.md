---
title: Konfigurere et miljø til opslag efter masterdata
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere dit miljø til at bruge funktionen til opslag af masterdata for momsberegning.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e4aa941c57e8c31793d6db8ae87140cd1bb1a82b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021338"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Konfigurere et miljø til opslag efter masterdata

[!include [banner](../includes/banner.md)]

Dette emne indeholder en forklaring på, hvordan du kan konfigurere dit miljø til at bruge funktionen til opslag af masterdata for momsberegning.

1. Konfigurer integration af Power Platform i Lifecycle Services (LCS). Du kan finde flere oplysninger under [Microsoft Power Platform integration - Oversigt over tilføjelsesprogrammer](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
2. Konfigurer Dynamics 365 Finance og Microsoft Dataverse. Du kan finde flere oplysninger under [Hente løsningen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) og [Godkendelse og autorisation](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
3. Konfigurer følgende enheder. Du kan finde flere oplysninger i [Aktivering af virtuelle enheder](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).
      - CompanyInfoEntity
      - CurrencyEntity
      - CustCustomerV3Entity
      - DeliveryTermsEntity
      - EcoResProductCategoryEntity
      - EcoResReleasedProductV2Entity
      - LogisticsAddressCityEntity
      - LogisticsAddressCountryRegionTranslationEntity
      - LogisticsAddressStateEntity
      - PurchProcurementChargeCDSEntity
      - SalesChargeCDSEntity
      - TaxGroupEntity
      - TaxItemGroupHeadingEntity
      - VendVendorV2Entity
4. Konfigurere Dynamics 365 Regulatory Configuration Service (RCS). 
5. Opret en serviceanmodning til Microsoft for at aktivere flighting for følgende funktioner:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. Gå til arbejdsområdet **Funktionsstyring**, og aktivér følgende funktioner:

      - (Forhåndsversion) Understøttelse af Dataverse-datakilder for elektronisk rapportering
      - (Prøveversion) Understøttelse af Dataverse-datakilder i momstjenesten
      - (Prøveversion) Globaliseringsfunktioner

5. Log på RCS ved hjælp af en administratorkonto for en lejer.
6. Gå til **Elektronisk rapportering** > **Tilsluttede programmer**. 
7. Vælg **Ny** for at tilføje en post, og angiv følgende feltoplysninger. 

   - Indtast et navn i feltet **Navn**.
   - Vælg **Dataverse** i feltet **Type**.
   - Angiv din Dataverse-URL-adresse i feltet **Program**.
   - Angiv lejeren i feltet **Lejer**.
   - I feltet **Brugerdefineret URL-adresse** skal du angive din Dataverse-URL-adresse og tilføje "/api/data/v9.1".

8. Vælg **Kontrollér forbindelsen**, og afslut forbindelsesprocessen. 

   [![Knappen Kontrollér forbindelsen](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. Gå til **Elektronisk rapportering** > **Momskonfigurationer**, og importér momskonfigurationer fra [Momskonfigurationer](https://go.microsoft.com/fwlink/?linkid=2158352).

   [![Siden Momskonfigurationer, træet med momsdatamodellen](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. Gå til **Tilknytning af den momspligtig dokumentmodel** eller **Dataverse-modeltilknytning**, hvis du bruger en Microsoft-konfiguration, og vælg den post, du oprettede i trin 7, i feltet **Tilknyttet program**.
11. Vælg **Ja** i indstillingen **Standard for modeltilknytning**.

   [![Siden Modeltilknytning](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
