---
title: Kundeemne til kontanter
description: "Dette emne indeholder en oversigt over kundeemne til kontanter-løsningen mellem Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 02/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 025be8b44726194e6fc219816c40d2a15a7349df
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="36dae-103">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="36dae-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="36dae-104">Kundeemne til kontanter-løsningen giver direkte synkronisering på tværs af Dynamics 365 for Finance and Operations og Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="36dae-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="36dae-105">Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data til firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="36dae-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="36dae-106">Når data flyder mellem Finance and Operations og Sales, kan du udføre salgs- og marketingaktiviteter i Sales, og du kan håndtere ordreopfyldelsen ved at bruge lagerstyring i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36dae-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="36dae-107">Du kan finde yderligere oplysninger om kundeemne til kontant-integration i denne korte YouTube-video:</span><span class="sxs-lookup"><span data-stu-id="36dae-107">For more information about the Prospect to cash integration, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

<span data-ttu-id="36dae-108">I den aktuelle version indeholder Kundeemne til kontanter-løsning følgende typer direkte synkronisering:</span><span class="sxs-lookup"><span data-stu-id="36dae-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="36dae-109">Vedligehold konti i Sales, og synkroniser dem direkte fra Sales med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="36dae-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="36dae-110">Vedligeholde produkter i Finance and Operations, og synkronisere dem direkte med Sales</span><span class="sxs-lookup"><span data-stu-id="36dae-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="36dae-111">Vedligeholde kontakter i Sales og synkronisere dem direkte med kontakter eller debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="36dae-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="36dae-112">Synkronisere salgstilbud direkte fra Sales med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="36dae-112">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="36dae-113">Synkronisere salgsordrer direkte mellem Sales og Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="36dae-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="36dae-114">Synkronisere salgsfaktura direkte fra Finance and Operations med Sales</span><span class="sxs-lookup"><span data-stu-id="36dae-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="36dae-115">Systemkrav til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="36dae-115">System requirements for Finance and Operations</span></span>

<span data-ttu-id="36dae-116">Kundeemne til kontant-integration understøttes iå følgende versioner:</span><span class="sxs-lookup"><span data-stu-id="36dae-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="36dae-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (December 2017)</span><span class="sxs-lookup"><span data-stu-id="36dae-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="36dae-118">Dynamics 365 for Finance and Operations, Enterprise Edition (december 2017) - programbuild 7.3.11971.56116 med platformopdatering 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="36dae-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="36dae-119">Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017)</span><span class="sxs-lookup"><span data-stu-id="36dae-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="36dae-120">Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) - med platformsopdatering 8 (programbuild 7.2.11792.56024 med platformbuild 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="36dae-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="36dae-121">De følgende hotfixes er obligatoriske:</span><span class="sxs-lookup"><span data-stu-id="36dae-121">The following hotfixes are required:</span></span>

    - <span data-ttu-id="36dae-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – Dette hotfix muliggør salgsordresynkronisering fra Sales til Finance and Operations via funktionen Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="36dae-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="36dae-123">Det indeholder også flere andre forbedringer.</span><span class="sxs-lookup"><span data-stu-id="36dae-123">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="36dae-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Dette hotfix muliggør salgsordrelinjesynkronisering fra Sales til Finance and Operations til Sales via funktionen Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="36dae-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="36dae-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Dette hotfix muliggør salgsordresynkronisering fra Sales til Finance and Operations til Sales via funktionen Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="36dae-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="36dae-126">Du behøver kun at installere KB4045570, fordi installationen omfatter ændringerne fra andre hotfixes.</span><span class="sxs-lookup"><span data-stu-id="36dae-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="36dae-127">Dynamics 365 for Finance and Operations version 1611 (november 2016)</span><span class="sxs-lookup"><span data-stu-id="36dae-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="36dae-128">Dynamics 365 for Finance and Operations version 1611 (november 2016) med platformsopdatering 8 eller derover</span><span class="sxs-lookup"><span data-stu-id="36dae-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="36dae-129">De følgende hotfixes er obligatoriske:</span><span class="sxs-lookup"><span data-stu-id="36dae-129">The following hotfixes are required:</span></span>

    - <span data-ttu-id="36dae-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – Aktiver synkronisering af salgsordre med Dataintegrator fra Finance and Operations for Sales.</span><span class="sxs-lookup"><span data-stu-id="36dae-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
    - <span data-ttu-id="36dae-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – Aktiver synkronisering af salgsordrehoved og -linjer med Dataintegrator fra Finance and Operations for Sales.</span><span class="sxs-lookup"><span data-stu-id="36dae-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
    - <span data-ttu-id="36dae-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Understøttelse af Kundeemne til kontanter-integration via dataenheder er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="36dae-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="36dae-133">Du skal udløse følgende batchjob fra formularen **SalesPopulateProspectToCash** efter installation af hotfixes.</span><span class="sxs-lookup"><span data-stu-id="36dae-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="36dae-134">Denne formular er skjult, fordi du kun skal bruge den én gang.</span><span class="sxs-lookup"><span data-stu-id="36dae-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="36dae-135">For at få adgang til formen skal du logge på miljøet og føje følgende til URL-adressen i din browseradresse: &mi=action:SalesPopulateProspectToCash, f.eks. `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="36dae-135">To access the form, log in to the environment and add the following to the URL in your browser address: &mi=action:SalesPopulateProspectToCash, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="36dae-136">Når formularen åbnes, skal du klikke på OK.</span><span class="sxs-lookup"><span data-stu-id="36dae-136">When the form opens, click OK.</span></span> <span data-ttu-id="36dae-137">Dette udfylder et nyt **LineCreationSequnceNumber**-felt i tabellerne **SalesLine**, **SalesQuotationLine** og **CustInvoiceTrans** med entydige værdier og opdaterer produktlisten.</span><span class="sxs-lookup"><span data-stu-id="36dae-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="36dae-138">Dette er nødvendigt, for at integration af Kundeemne til kontanter kan fungere.</span><span class="sxs-lookup"><span data-stu-id="36dae-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="36dae-139">Systemkrav til Sales</span><span class="sxs-lookup"><span data-stu-id="36dae-139">System requirements for Sales</span></span>

<span data-ttu-id="36dae-140">Hvis du vil bruge løsningen Kundeemne til kontanter, skal du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="36dae-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="36dae-141">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online eller en nyere version.</span><span class="sxs-lookup"><span data-stu-id="36dae-141">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="36dae-142">Løsningen Kundeemne til kontanter til Dynamics 365 for Sales, version 1.15.0.0 (v15)</span><span class="sxs-lookup"><span data-stu-id="36dae-142">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="36dae-143">Installer løsningen Kundeemne til kontanter til Sales</span><span class="sxs-lookup"><span data-stu-id="36dae-143">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="36dae-144">Hent [zip-filen med løsningspakken Kundeemne til kontanter til Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) fra CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="36dae-144">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="36dae-145">Kontroller, at zip-filen ikke er blokeret.</span><span class="sxs-lookup"><span data-stu-id="36dae-145">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="36dae-146">Ellers, når du forsøger at installere løsningspakken, kan du modtage følgende fejlmeddelelse: "Der blev ikke fundet nogen importpakker".</span><span class="sxs-lookup"><span data-stu-id="36dae-146">Otherwise, when you try to install the solution package, you may receive the following error message, "No import packages were found."</span></span> <span data-ttu-id="36dae-147">For at fjerne blokeringen af zip-filen skal du højreklikke på filen og vælge **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="36dae-147">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="36dae-148">Vælg **Ophæv blokering**.</span><span class="sxs-lookup"><span data-stu-id="36dae-148">Select **Unblock**.</span></span>
3. <span data-ttu-id="36dae-149">Pak filen ud, og kør **PackageDeployer.exe**.</span><span class="sxs-lookup"><span data-stu-id="36dae-149">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="36dae-150">Installer løsningen Kundeemne til kontanter i din Sales-forekomst:</span><span class="sxs-lookup"><span data-stu-id="36dae-150">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="36dae-151">Vælg installationstypen **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="36dae-151">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="36dae-152">Vælg **Vis avancerede**.</span><span class="sxs-lookup"><span data-stu-id="36dae-152">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="36dae-153">For en hurtig installation skal du vælge et område.</span><span class="sxs-lookup"><span data-stu-id="36dae-153">For a quick installation, select a region.</span></span> <span data-ttu-id="36dae-154">Hvis du vælger **Ved ikke**, vil systemet søge efter alle områder, og installationen vil tage længere tid.</span><span class="sxs-lookup"><span data-stu-id="36dae-154">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="36dae-155">Angiv brugernavnet og adgangskoden for en administrator, der har installationsrettigheder.</span><span class="sxs-lookup"><span data-stu-id="36dae-155">Enter the user name and password of an admin user who has installation rights.</span></span>



