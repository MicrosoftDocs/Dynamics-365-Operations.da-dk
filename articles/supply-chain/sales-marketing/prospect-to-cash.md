---
title: Kundeemne til kontanter
description: "Emnet indeholder en oversigt over kundeemne til kontanter-løsningen mellem Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="e9c2a-103">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="e9c2a-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e9c2a-104">Kundeemne til kontanter-løsningen bruger [Dataintegration](/common-data-service/entity-reference/dynamics-365-integration) til at synkronisere data på tværs af Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales-forekomster via Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="e9c2a-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="e9c2a-105">Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="e9c2a-106">Når dataene flyder mellem Finance and Operations og Sales, kan du udføre salgs- og marketingaktiviteter i Sales og håndtere ordreopfyldelsen med lagerstyring i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="e9c2a-107">Denne løsning giver integration på følgende områder:</span><span class="sxs-lookup"><span data-stu-id="e9c2a-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="e9c2a-108">Vedligehold konti i Sales, og synkroniser dem med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e9c2a-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="e9c2a-109">Vedligehold kontakter i Sales, og synkroniser dem med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e9c2a-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="e9c2a-110">Vedligehold produkter kontakter i Finance and Operations, og synkroniser dem med Sales</span><span class="sxs-lookup"><span data-stu-id="e9c2a-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="e9c2a-111">Opret salgstilbud i Sales, og synkroniser dem med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e9c2a-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="e9c2a-112">Opret salgsordrer i Finance and Operations, og synkroniser dem med Sales</span><span class="sxs-lookup"><span data-stu-id="e9c2a-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="e9c2a-113">Opret salgsfakturaer i Finance and Operations, og synkroniser dem med Sales</span><span class="sxs-lookup"><span data-stu-id="e9c2a-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="e9c2a-114">Systemkrav til Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="e9c2a-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="e9c2a-115">Hvis du vil bruge løsningen Kundeemne til kontanter, skal du installere følgende:</span><span class="sxs-lookup"><span data-stu-id="e9c2a-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="e9c2a-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) med platformsopdatering 8 (App 7.2.11792.56024 med Platform 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="e9c2a-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="e9c2a-117">To hotfixes til Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017).</span><span class="sxs-lookup"><span data-stu-id="e9c2a-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="e9c2a-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - dette hotfix muliggør salgsordrelinjesynkronisering med funktionen Dataintegration fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="e9c2a-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - dette hotfix muliggør salgsordresynkronisering med funktionen Dataintegration fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="e9c2a-120">**Bemærk**: Du skal kun installere KB4036524, fordi installationen omfatter ændringerne fra KB4036461.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="e9c2a-121">Systemkravene til Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="e9c2a-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="e9c2a-122">Hvis du vil bruge løsningen Kundeemne til kontanter, skal du installere følgende:</span><span class="sxs-lookup"><span data-stu-id="e9c2a-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="e9c2a-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online eller senere.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="e9c2a-124">Løsningen Kundeemne til kontanter til Dynamics 365 for Sales, version 1.14.0.0 (v14) eller nyere.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e9c2a-125">Installer løsningen Kundeemne til kontanter til Sales</span><span class="sxs-lookup"><span data-stu-id="e9c2a-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="e9c2a-126">Hent [zip-filen med løsningspakken Kundeemne til kontanter til Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) på CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="e9c2a-127">Sørg for, at blokeringen af zip-filen ophæves, så du ikke får fejlmeddelelsen "Der blev ikke fundet nogen importpakker", når du installerer løsningspakken.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="e9c2a-128">Du ophæver blokeringen af filen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="e9c2a-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="e9c2a-129">Højreklik på zip-filen.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="e9c2a-130">Vælg **Egenskaber** og derefter vælge **Ophæv blokering**.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="e9c2a-131">Pak filen ud, og kør PackageDeployer.exe.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="e9c2a-132">Installer løsningen Kundeemne til kontanter i din Sales-forekomst.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="e9c2a-133">Vælg installationstypen **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="e9c2a-134">Vælg **Vis avancerede**.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="e9c2a-135">For en hurtig installation, skal du vælge et **område**.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="e9c2a-136">Hvis du vælger **Ved ikke**, vil systemet søge efter alle områder, og det tager længere tid at installere.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="e9c2a-137">Angiv **Brugernavn** og **Adgangskode** for en administrator, der har de nødvendige rettigheder til at installere.</span><span class="sxs-lookup"><span data-stu-id="e9c2a-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

