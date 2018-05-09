---
title: Konfigurere SQL Server Reporting Services for en lokal installation
description: Dette emne indeholder oplysninger om konfiguration af SQL Server Reporting Services (SSRS) for en lokal installation.
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 86aa52a4d75ca358355ab6bb85dbacefd21e4509
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a><span data-ttu-id="6ed25-103">Konfigurere SQL Server Reporting Services for en lokal installation</span><span class="sxs-lookup"><span data-stu-id="6ed25-103">Configure SQL Server Reporting Services for an on-premises deployment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ed25-104">Brug trinnene i dette emne til at konfigurere SQL Server Reporting Services (SSRS) til din installation af Microsoft Dynamics 365 for Finance and Operations (on-premises).</span><span class="sxs-lookup"><span data-stu-id="6ed25-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 for Finance and Operations (on-premises) deployment.</span></span>

1. <span data-ttu-id="6ed25-105">Åbn programmet Konfigurationsstyring til Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="6ed25-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="6ed25-106">Lad standard **Servernavn** stå, som bør være navnet på den aktuelle computer, og **Rapportserverforekomst**, **MSSQLSERVER**.</span><span class="sxs-lookup"><span data-stu-id="6ed25-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span> 
3. <span data-ttu-id="6ed25-107">Klik på **Tilknyt**.</span><span class="sxs-lookup"><span data-stu-id="6ed25-107">Click **Connect**.</span></span>
   
   <span data-ttu-id="6ed25-108">[![Reporting Services-konfigurationsforbindelse](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="6ed25-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>
   
4. <span data-ttu-id="6ed25-109">Klik på fanen **Tjenestekonto**, og kontroller, at indstillingerne svarer til følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="6ed25-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="6ed25-110">[![Fanen Tjenestekonto](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="6ed25-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>
    
5. <span data-ttu-id="6ed25-111">Klik på fanen **URL-adresse til webtjeneste**, og kontroller, at indstillingerne svarer til følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="6ed25-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span> 

    <span data-ttu-id="6ed25-112">[![Fanen URL-nøgle til webtjeneste](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="6ed25-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span> 
    
6. <span data-ttu-id="6ed25-113">Klik på fanen **Database**, og kontroller, at den **Databasenavn** og **Indstillinger for legitimationsoplysninger** svarer til følgende grafik.</span><span class="sxs-lookup"><span data-stu-id="6ed25-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span> <span data-ttu-id="6ed25-114">**Bemærk!** Du skal oprette en ny database.</span><span class="sxs-lookup"><span data-stu-id="6ed25-114">**Note:** You will need to create a new database.</span></span> <span data-ttu-id="6ed25-115">Det gør du ved at klikke på **Skift database** og derefter kontrollere, at det nye databasenavn er: **DynamicsAxReportServer**.</span><span class="sxs-lookup"><span data-stu-id="6ed25-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="6ed25-116">[![fanen database](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="6ed25-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>
    
7. <span data-ttu-id="6ed25-117">Klik på fanen **URL-adresse til webportal**, og kontroller, at indstillingerne svarer til følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="6ed25-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span> <span data-ttu-id="6ed25-118">**Bemærk!** Du skal klikke på **Anvend** for at oprette og konfigurere portalen korrekt.</span><span class="sxs-lookup"><span data-stu-id="6ed25-118">**Note:** You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="6ed25-119">[![fanen URL-adresse til webportal](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="6ed25-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>
    
   <span data-ttu-id="6ed25-120">Når portalen er konfigureret, svarer fanen **Webportal** til følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="6ed25-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>
    <span data-ttu-id="6ed25-121">[![fanen webportal](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="6ed25-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>
    
8. <span data-ttu-id="6ed25-122">Klik på URL-adressen til rapporter for at se SQL Server Reporting Services-webportalen.</span><span class="sxs-lookup"><span data-stu-id="6ed25-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span> 
9. <span data-ttu-id="6ed25-123">Når du er på portalen, kan du oprette en ny mappe med navnet **Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="6ed25-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

   <span data-ttu-id="6ed25-124">[![dynamics-mappe](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="6ed25-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>
    
10. <span data-ttu-id="6ed25-125">I **Konfigurationsstyring til Reporting Services** skal du klikke på fanen **Mailindstillinger** og kontrollere, at indstillingerne svarer til følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="6ed25-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="6ed25-126">[![fanen mailindstillinger](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="6ed25-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>
    
11. <span data-ttu-id="6ed25-127">Klik på fanen **Udførelseskonto**, og kontroller, at indstillingerne svarer til følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="6ed25-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="6ed25-128">[![fanen udførelseskonto](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="6ed25-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>
    
    <span data-ttu-id="6ed25-129">Du skal ikke ændre standardindstillingerne under fanen **Krypteringsnøgler**. [![fanen krypteringsnøgler](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="6ed25-129">Don’t change the default settings on the **Encryption Keys** tab. [![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>
    
12. <span data-ttu-id="6ed25-130">Klik på fanen **Abonnementsindstillinger**, og kontroller, at indstillingerne svarer til følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="6ed25-130">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="6ed25-131">[![fanen abonnementsindstillinger](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="6ed25-131">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>
    
    <span data-ttu-id="6ed25-132">Du skal ikke ændre standardindstillingerne under fanen **Udvidet installation**. [![fanen udvidet installation](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="6ed25-132">Don’t change the default settings on the **Scale-out Deployment** tab. [![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>
    
    <span data-ttu-id="6ed25-133">Du skal ikke ændre standardindstillingerne under fanen **Power BI-integration**. [![fanen power bi-integration](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="6ed25-133">Don’t change the default settings on the **Power BI Integration** tab. [![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span> 
    
13. <span data-ttu-id="6ed25-134">Klik på **Afslut** for at lukke **Konfigurationsstyring til Reporting Services**.</span><span class="sxs-lookup"><span data-stu-id="6ed25-134">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="6ed25-135">[![konfigurationsstyring til reporting services](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="6ed25-135">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
    


