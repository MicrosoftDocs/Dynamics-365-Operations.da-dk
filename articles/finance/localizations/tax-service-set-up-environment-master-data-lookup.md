---
title: Aktivere masterdataopslag til konfiguration af momsberegning
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere og aktivere funktionen til opslag af masterdata for momsberegning.
author: kai-cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7640144b1687fc64e55f659d49cdb0817c17294a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686705"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Aktivere masterdataopslag til konfiguration af momsberegning 

[!include [banner](../includes/banner.md)]

Dette emne indeholder en forklaring på, hvordan du kan konfigurere og aktivere funktionen til opslag af masterdata for momsberegning. Der findes en rullemenu til valg af værdier i momsberegningskonfigurationen for felter som **Juridisk enhed**, **Kreditorkonto**, **Varekode** og **Leveringsbetingelse**. Disse værdier kommer fra det tilsluttede Microsoft Dynamics 365 Finance-miljø via Microsoft Dataverse-datakilden.

> [!NOTE] 
> Funktionaliteten for opslag efter stamdata for momsberegning er valgfri. Du kan springe følgende trin over, hvis du deaktiverer funktionen **Understøttelse af Dataverse-datakilder i momstjenesten** i RCS (Regulatory Configuration Service). Men i dette tilfælde er rullelisten ikke tilgængelig i konfigurationen af momsberegningen.

1. Konfigurer integration af Microsoft Power Platform i Microsoft Dynamics Lifecycle Services (LCS). Du kan finde flere oplysninger under [Microsoft Power Platform integration - Oversigt over tilføjelsesprogrammer](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Når du har fuldført trinnet, vises navnet på et Microsoft Power Platform-miljø i sektionen **Power Platform-integration**.
2. Gå til [Microsoft Power Platform administration](https://admin.powerplatform.microsoft.com/environments), og vælg miljønavnet. URL-adressen til miljøet er angivet.
3. Konfigurer Dynamics 365 Finance og Dataverse. Du kan finde flere oplysninger under [Hente løsningen for den virtuelle enhed](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) og [Godkendelse og autorisation](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
4. Konfigurer følgende enheder. Du kan finde flere oplysninger i [Aktivere virtuelle Microsoft Dataverse-enheder](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

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

5. Konfigurer Regulatory Configuration Service (RCS). Åbn arbejdsområdet **Funktionsstyring**, og aktivér følgende funktioner:

    - Understøttelse af Dataverse-datakilder for elektronisk rapportering
    - Understøttelse af Dataverse-datakilder i momstjenesten
    - Globaliseringsfunktioner

6. Log på RCS ved hjælp af en administratorkonto for en lejer.
7. Gå til **Elektronisk rapportering** > **Tilsluttede programmer**. 
8. Vælg **Ny** for at tilføje en post, og angiv følgende feltoplysninger. 

    - Indtast et navn i feltet **Navn**.
    - Vælg **Dataverse** i feltet **Type**.
    - Angiv din Dataverse-URL-adresse i feltet **Program**.
    - Angiv lejeren i feltet **Lejer**.
    - I feltet **Brugerdefineret URL-adresse** skal du angive din Dataverse-URL-adresse og tilføje "/api/data/v9.1".

9. Vælg **Kontrollér forbindelsen**, og afslut forbindelsesprocessen. 

    [![Knappen Kontrollér forbindelsen.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. Gå til **Elektronisk rapportering** > **Momskonfigurationer**, og importér momskonfigurationer fra [Momskonfigurationer](https://go.microsoft.com/fwlink/?linkid=2158352).

    [![Siden Momskonfigurationer, træet med momsdatamodellen.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. Gå til **Tilknytning af den momspligtig dokumentmodel** eller **Dataverse-modeltilknytning**, hvis du bruger en Microsoft-konfiguration, og vælg den post, du oprettede i trin 7, i feltet **Tilknyttet program**.
12. Vælg **Ja** i indstillingen **Standard for modeltilknytning**.

    [![Siden Modeltilknytning.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
