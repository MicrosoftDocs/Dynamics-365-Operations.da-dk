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
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="c231b-103">Konfigurere et miljø til opslag efter masterdata</span><span class="sxs-lookup"><span data-stu-id="c231b-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c231b-104">Dette emne indeholder en forklaring på, hvordan du kan konfigurere dit miljø til at bruge funktionen til opslag af masterdata for momsberegning.</span><span class="sxs-lookup"><span data-stu-id="c231b-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="c231b-105">Konfigurer integration af Power Platform i Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c231b-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="c231b-106">Du kan finde flere oplysninger under [Microsoft Power Platform integration - Oversigt over tilføjelsesprogrammer](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c231b-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="c231b-107">Konfigurer Dynamics 365 Finance og Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c231b-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="c231b-108">Du kan finde flere oplysninger under [Hente løsningen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) og [Godkendelse og autorisation](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="c231b-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="c231b-109">Konfigurer følgende enheder.</span><span class="sxs-lookup"><span data-stu-id="c231b-109">Set up the following entities.</span></span> <span data-ttu-id="c231b-110">Du kan finde flere oplysninger i [Aktivering af virtuelle enheder](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="c231b-110">For more information, see [Enabling virtual entities](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span></span>
      - <span data-ttu-id="c231b-111">CompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="c231b-111">CompanyInfoEntity</span></span>
      - <span data-ttu-id="c231b-112">CurrencyEntity</span><span class="sxs-lookup"><span data-stu-id="c231b-112">CurrencyEntity</span></span>
      - <span data-ttu-id="c231b-113">CustCustomerV3Entity</span><span class="sxs-lookup"><span data-stu-id="c231b-113">CustCustomerV3Entity</span></span>
      - <span data-ttu-id="c231b-114">DeliveryTermsEntity</span><span class="sxs-lookup"><span data-stu-id="c231b-114">DeliveryTermsEntity</span></span>
      - <span data-ttu-id="c231b-115">EcoResProductCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="c231b-115">EcoResProductCategoryEntity</span></span>
      - <span data-ttu-id="c231b-116">EcoResReleasedProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="c231b-116">EcoResReleasedProductV2Entity</span></span>
      - <span data-ttu-id="c231b-117">LogisticsAddressCityEntity</span><span class="sxs-lookup"><span data-stu-id="c231b-117">LogisticsAddressCityEntity</span></span>
      - <span data-ttu-id="c231b-118">LogisticsAddressCountryRegionTranslationEntity</span><span class="sxs-lookup"><span data-stu-id="c231b-118">LogisticsAddressCountryRegionTranslationEntity</span></span>
      - <span data-ttu-id="c231b-119">LogisticsAddressStateEntity</span><span class="sxs-lookup"><span data-stu-id="c231b-119">LogisticsAddressStateEntity</span></span>
      - <span data-ttu-id="c231b-120">PurchProcurementChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="c231b-120">PurchProcurementChargeCDSEntity</span></span>
      - <span data-ttu-id="c231b-121">SalesChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="c231b-121">SalesChargeCDSEntity</span></span>
      - <span data-ttu-id="c231b-122">TaxGroupEntity</span><span class="sxs-lookup"><span data-stu-id="c231b-122">TaxGroupEntity</span></span>
      - <span data-ttu-id="c231b-123">TaxItemGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="c231b-123">TaxItemGroupHeadingEntity</span></span>
      - <span data-ttu-id="c231b-124">VendVendorV2Entity</span><span class="sxs-lookup"><span data-stu-id="c231b-124">VendVendorV2Entity</span></span>
4. <span data-ttu-id="c231b-125">Konfigurere Dynamics 365 Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="c231b-125">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="c231b-126">Opret en serviceanmodning til Microsoft for at aktivere flighting for følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="c231b-126">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="c231b-127">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="c231b-127">ERCdsFeature</span></span>
      - <span data-ttu-id="c231b-128">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="c231b-128">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="c231b-129">Gå til arbejdsområdet **Funktionsstyring**, og aktivér følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="c231b-129">Go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="c231b-130">(Forhåndsversion) Understøttelse af Dataverse-datakilder for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="c231b-130">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="c231b-131">(Prøveversion) Understøttelse af Dataverse-datakilder i momstjenesten</span><span class="sxs-lookup"><span data-stu-id="c231b-131">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="c231b-132">(Prøveversion) Globaliseringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="c231b-132">(Preview) Globalization features</span></span>

5. <span data-ttu-id="c231b-133">Log på RCS ved hjælp af en administratorkonto for en lejer.</span><span class="sxs-lookup"><span data-stu-id="c231b-133">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="c231b-134">Gå til **Elektronisk rapportering** > **Tilsluttede programmer**.</span><span class="sxs-lookup"><span data-stu-id="c231b-134">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="c231b-135">Vælg **Ny** for at tilføje en post, og angiv følgende feltoplysninger.</span><span class="sxs-lookup"><span data-stu-id="c231b-135">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="c231b-136">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="c231b-136">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="c231b-137">Vælg **Dataverse** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="c231b-137">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="c231b-138">Angiv din Dataverse-URL-adresse i feltet **Program**.</span><span class="sxs-lookup"><span data-stu-id="c231b-138">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="c231b-139">Angiv lejeren i feltet **Lejer**.</span><span class="sxs-lookup"><span data-stu-id="c231b-139">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="c231b-140">I feltet **Brugerdefineret URL-adresse** skal du angive din Dataverse-URL-adresse og tilføje "/api/data/v9.1".</span><span class="sxs-lookup"><span data-stu-id="c231b-140">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="c231b-141">Vælg **Kontrollér forbindelsen**, og afslut forbindelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="c231b-141">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="c231b-142">[![Knappen Kontrollér forbindelsen](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="c231b-142">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="c231b-143">Gå til **Elektronisk rapportering** > **Momskonfigurationer**, og importér momskonfigurationer fra [Momskonfigurationer](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="c231b-143">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="c231b-144">[![Siden Momskonfigurationer, træet med momsdatamodellen](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="c231b-144">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="c231b-145">Gå til **Tilknytning af den momspligtig dokumentmodel** eller **Dataverse-modeltilknytning**, hvis du bruger en Microsoft-konfiguration, og vælg den post, du oprettede i trin 7, i feltet **Tilknyttet program**.</span><span class="sxs-lookup"><span data-stu-id="c231b-145">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="c231b-146">Vælg **Ja** i indstillingen **Standard for modeltilknytning**.</span><span class="sxs-lookup"><span data-stu-id="c231b-146">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="c231b-147">[![Siden Modeltilknytning](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="c231b-147">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
