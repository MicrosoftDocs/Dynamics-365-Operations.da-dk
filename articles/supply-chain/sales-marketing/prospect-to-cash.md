---
title: Kundeemne til kontanter
description: "Emnet indeholder en oversigt over kundeemne til kontanter-løsningen mellem Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: da-dk
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="60449-103">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="60449-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="60449-104">Kundeemne til kontanter-løsningen bruger [Dataintegration](/common-data-service/entity-reference/dynamics-365-integration) til at synkronisere data på tværs af Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales-forekomster via Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="60449-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="60449-105">Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="60449-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="60449-106">Når dataene flyder mellem Finance and Operations og Sales, kan du udføre salgs- og marketingaktiviteter i Sales og håndtere ordreopfyldelsen med lagerstyring i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="60449-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="60449-107">Denne løsning giver integration på følgende områder:</span><span class="sxs-lookup"><span data-stu-id="60449-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="60449-108">Vedligehold konti i Sales, og synkroniser dem med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="60449-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="60449-109">Vedligehold kontakter i Sales, og synkroniser dem med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="60449-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="60449-110">Vedligehold produkter kontakter i Finance and Operations, og synkroniser dem med Sales</span><span class="sxs-lookup"><span data-stu-id="60449-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="60449-111">Opret salgstilbud i Sales, og synkroniser dem med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="60449-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="60449-112">Opret salgsordrer i Finance and Operations, og synkroniser dem med Sales</span><span class="sxs-lookup"><span data-stu-id="60449-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="60449-113">Opret salgsfakturaer i Finance and Operations, og synkroniser dem med Sales</span><span class="sxs-lookup"><span data-stu-id="60449-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

<span data-ttu-id="60449-114">Denne løsning giver direkte synkronisering på følgende områder:</span><span class="sxs-lookup"><span data-stu-id="60449-114">This solution provides direct synchronization in the following areas:</span></span>

-   [<span data-ttu-id="60449-115">Vedligehold konti i Sales, og synkroniser dem direkte fra Sales med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="60449-115">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
-   [<span data-ttu-id="60449-116">Vedligehold produkter i Finance and Operations, og synkroniser dem direkte med Sales</span><span class="sxs-lookup"><span data-stu-id="60449-116">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
-   [<span data-ttu-id="60449-117">Vedligehold kontakter i Sales, og synkroniser dem direkte med kontakter eller debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="60449-117">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
-   [<span data-ttu-id="60449-118">Synkroniser hoveder og linjer i salgstilbud direkte fra Sales med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="60449-118">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
-   [<span data-ttu-id="60449-119">Opret salgsordrer i Finance and Operations, og synkroniser dem direkte med Sales</span><span class="sxs-lookup"><span data-stu-id="60449-119">Create sales orders in Finance and Operations and sync them directly to Sales</span></span>](sales-order-template-mapping-direct.md)
-  [<span data-ttu-id="60449-120">Synkroniser hoveder og linjer i salgsordrer direkte mellem Sales og Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="60449-120">Synchronize sales order headers and lines directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-between-sales-fin.md)
-   [<span data-ttu-id="60449-121">Synkroniser salgsordrer direkte mellem Sales og Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="60449-121">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
-   [<span data-ttu-id="60449-122">Opret salgsfakturaer i Finance and Operations, og synkroniser dem direkte med Sales</span><span class="sxs-lookup"><span data-stu-id="60449-122">Create sales invoices in Finance and Operations and sync them directly to Sales</span></span>](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="60449-123">Systemkrav til Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="60449-123">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="60449-124">Hvis du vil bruge løsningen Kundeemne til kontanter, skal du installere følgende:</span><span class="sxs-lookup"><span data-stu-id="60449-124">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="60449-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) med platformsopdatering 8 (App 7.2.11792.56024 med Platform 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="60449-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="60449-126">Hotfixes til Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017).</span><span class="sxs-lookup"><span data-stu-id="60449-126">Hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>
        
    -  <span data-ttu-id="60449-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) – Dette hotfix aktiverer understøttelse af synkronisering af salgsordrer med funktionen Dataintegration fra Sales til Finance and Operations, sammen med en række andre forbedringer.</span><span class="sxs-lookup"><span data-stu-id="60449-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - This hotfix enabels support for sales order synchronization with the Data Integration feature from Sales to Finance and Operations, along with a number of other enhancements.</span></span>

    -  <span data-ttu-id="60449-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - dette hotfix muliggør salgsordrelinjesynkronisering med funktionen Dataintegration fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="60449-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="60449-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - dette hotfix muliggør salgsordresynkronisering med funktionen Dataintegration fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="60449-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>

<span data-ttu-id="60449-130">**Bemærk**: Du behøver kun at installere KB4045570, fordi installationen omfatter ændringerne fra andre KB'er.</span><span class="sxs-lookup"><span data-stu-id="60449-130">**Note**: You only need to install KB4045570 because the installation includes the changes from the other KB's.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="60449-131">Systemkravene til Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="60449-131">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="60449-132">Hvis du vil bruge løsningen Kundeemne til kontanter, skal du installere følgende:</span><span class="sxs-lookup"><span data-stu-id="60449-132">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="60449-133">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online.</span><span class="sxs-lookup"><span data-stu-id="60449-133">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online.</span></span>
- <span data-ttu-id="60449-134">Løsningen Kundeemne til kontanter til Dynamics 365 for Sales, version 1.14.0.0 (v14) eller nyere.</span><span class="sxs-lookup"><span data-stu-id="60449-134">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="60449-135">Installer løsningen Kundeemne til kontanter til Sales</span><span class="sxs-lookup"><span data-stu-id="60449-135">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="60449-136">Hent [zip-filen med løsningspakken Kundeemne til kontanter til Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) på CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="60449-136">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="60449-137">Sørg for, at blokeringen af zip-filen ophæves, så du ikke får fejlmeddelelsen "Der blev ikke fundet nogen importpakker", når du installerer løsningspakken.</span><span class="sxs-lookup"><span data-stu-id="60449-137">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="60449-138">Du ophæver blokeringen af filen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="60449-138">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="60449-139">Højreklik på zip-filen.</span><span class="sxs-lookup"><span data-stu-id="60449-139">Right-click the zip file.</span></span>
    -  <span data-ttu-id="60449-140">Vælg **Egenskaber** og derefter vælge **Ophæv blokering**.</span><span class="sxs-lookup"><span data-stu-id="60449-140">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="60449-141">Pak filen ud, og kør PackageDeployer.exe.</span><span class="sxs-lookup"><span data-stu-id="60449-141">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="60449-142">Installer løsningen Kundeemne til kontanter i din Sales-forekomst.</span><span class="sxs-lookup"><span data-stu-id="60449-142">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="60449-143">Vælg installationstypen **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="60449-143">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="60449-144">Vælg **Vis avancerede**.</span><span class="sxs-lookup"><span data-stu-id="60449-144">Select **Show advanced**.</span></span>
    - <span data-ttu-id="60449-145">For en hurtig installation, skal du vælge et **område**.</span><span class="sxs-lookup"><span data-stu-id="60449-145">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="60449-146">Hvis du vælger **Ved ikke**, vil systemet søge efter alle områder, og det tager længere tid at installere.</span><span class="sxs-lookup"><span data-stu-id="60449-146">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="60449-147">Angiv **Brugernavn** og **Adgangskode** for en administrator, der har de nødvendige rettigheder til at installere.</span><span class="sxs-lookup"><span data-stu-id="60449-147">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

