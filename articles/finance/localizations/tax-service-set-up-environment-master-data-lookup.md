---
title: Konfigurere et miljø til opslag efter masterdata
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere dit miljø til at bruge funktionen til opslag af masterdata for momsberegning.
author: kai-cloud
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: eda093a75898bace2f3c7968933b83ccafa7fabb
ms.sourcegitcommit: 66095f1b7e0fd2756aa29fd7deb9ce5392b7e0b2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/08/2021
ms.locfileid: "5869052"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="62c5f-103">Konfigurere et miljø til opslag efter masterdata</span><span class="sxs-lookup"><span data-stu-id="62c5f-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="62c5f-104">Dette emne indeholder en forklaring på, hvordan du kan konfigurere dit miljø til at bruge funktionen til opslag af masterdata for momsberegning.</span><span class="sxs-lookup"><span data-stu-id="62c5f-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="62c5f-105">Konfigurer integration af Power Platform i Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="62c5f-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="62c5f-106">Du kan finde flere oplysninger under [Microsoft Power Platform integration - Oversigt over tilføjelsesprogrammer](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="62c5f-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="62c5f-107">Konfigurer Dynamics 365 Finance og Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="62c5f-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="62c5f-108">Du kan finde flere oplysninger under [Hente løsningen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) og [Godkendelse og autorisation](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="62c5f-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="62c5f-109">Importér den *forudsættende løsning med den virtuelle enhed for momstjeneste* fra den [virtuelle enhed for momstjenesten](https://go.microsoft.com/fwlink/?linkid=2158160).</span><span class="sxs-lookup"><span data-stu-id="62c5f-109">Import the *Prerequisite tax service virtual entity solution* from the [Tax service virtual entity](https://go.microsoft.com/fwlink/?linkid=2158160).</span></span>
4. <span data-ttu-id="62c5f-110">Konfigurere Dynamics 365 Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="62c5f-110">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="62c5f-111">Opret en serviceanmodning til Microsoft for at aktivere flighting for følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="62c5f-111">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="62c5f-112">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="62c5f-112">ERCdsFeature</span></span>
      - <span data-ttu-id="62c5f-113">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="62c5f-113">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="62c5f-114">I arbejdsområdet **Funktionsstyring** i Finance skal du aktivere følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="62c5f-114">In Finance, go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="62c5f-115">(Forhåndsversion) Understøttelse af Dataverse-datakilder for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="62c5f-115">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="62c5f-116">(Prøveversion) Understøttelse af Dataverse-datakilder i momstjenesten</span><span class="sxs-lookup"><span data-stu-id="62c5f-116">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="62c5f-117">(Prøveversion) Globaliseringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="62c5f-117">(Preview) Globalization features</span></span>

5. <span data-ttu-id="62c5f-118">Log på RCS ved hjælp af en administratorkonto for en lejer.</span><span class="sxs-lookup"><span data-stu-id="62c5f-118">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="62c5f-119">Gå til **Elektronisk rapportering** > **Tilsluttede programmer**.</span><span class="sxs-lookup"><span data-stu-id="62c5f-119">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="62c5f-120">Vælg **Ny** for at tilføje en post, og angiv følgende feltoplysninger.</span><span class="sxs-lookup"><span data-stu-id="62c5f-120">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="62c5f-121">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="62c5f-121">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="62c5f-122">Vælg **Dataverse** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="62c5f-122">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="62c5f-123">Angiv din Dataverse-URL-adresse i feltet **Program**.</span><span class="sxs-lookup"><span data-stu-id="62c5f-123">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="62c5f-124">Angiv lejeren i feltet **Lejer**.</span><span class="sxs-lookup"><span data-stu-id="62c5f-124">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="62c5f-125">I feltet **Brugerdefineret URL-adresse** skal du angive din Dataverse-URL-adresse og tilføje "/api/data/v9.1".</span><span class="sxs-lookup"><span data-stu-id="62c5f-125">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="62c5f-126">Vælg **Kontrollér forbindelsen**, og afslut forbindelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="62c5f-126">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="62c5f-127">[![Knappen Kontrollér forbindelsen](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="62c5f-127">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="62c5f-128">Gå til **Elektronisk rapportering** > **Momskonfigurationer**, og importér momskonfigurationer fra [Momskonfigurationer](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="62c5f-128">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="62c5f-129">[![Siden Momskonfigurationer, træet med momsdatamodellen](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="62c5f-129">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="62c5f-130">Gå til **Tilknytning af den momspligtig dokumentmodel** eller **Dataverse-modeltilknytning**, hvis du bruger en Microsoft-konfiguration, og vælg den post, du oprettede i trin 7, i feltet **Tilknyttet program**.</span><span class="sxs-lookup"><span data-stu-id="62c5f-130">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="62c5f-131">Vælg **Ja** i indstillingen **Standard for modeltilknytning**.</span><span class="sxs-lookup"><span data-stu-id="62c5f-131">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="62c5f-132">[![Siden Modeltilknytning](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="62c5f-132">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
