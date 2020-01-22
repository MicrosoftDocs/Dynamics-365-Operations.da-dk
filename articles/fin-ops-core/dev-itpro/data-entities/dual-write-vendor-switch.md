---
title: Skifte mellem kreditordesign
description: I dette emne beskrives det, hvordan du kan skifte mellem integrationen af leverandørdata mellem Finance and Operations-programmer og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
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
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902719"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="92e62-103">Skifte mellem kreditordesign</span><span class="sxs-lookup"><span data-stu-id="92e62-103">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="92e62-104">Kreditordataflow</span><span class="sxs-lookup"><span data-stu-id="92e62-104">Vendor data flow</span></span> 

<span data-ttu-id="92e62-105">Hvis du bruger andre Dynamics 365-apps til leverandørhåndtering, og du vil adskille leverandøroplysningerne fra kundernes, kan du bruge dette grundlæggende leverandørdesign.</span><span class="sxs-lookup"><span data-stu-id="92e62-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Grundlæggende leverandørflow](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="92e62-107">Hvis du bruger andre Dynamics 365-apps til leverandørhåndtering, og du fortsat vil bruge enheden **Konto** til at gemme leverandøroplysninger, kan du bruge dette udvidede leverandørdesign.</span><span class="sxs-lookup"><span data-stu-id="92e62-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="92e62-108">I dette design gemmes udvidede leverandøroplysninger som f.eks. leverandørers på hold-status og leverandørprofil i enheden **leverandører** i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="92e62-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Udvidet leverandørflow](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="92e62-110">Følg nedenstående fremgangsmåde for at bruge det udvidede leverandør design:</span><span class="sxs-lookup"><span data-stu-id="92e62-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="92e62-111">Løsningspakken **SupplyChainCommon** indeholder skabeloner for arbejdsgangsproces som vist i følgende billede.</span><span class="sxs-lookup"><span data-stu-id="92e62-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="92e62-112">![Skabeloner for arbejdsgangsprocesser](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="92e62-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="92e62-113">Opret nye arbejdsgangsprocesser ved hjælp af arbejdsgangsprocesskabeloner:</span><span class="sxs-lookup"><span data-stu-id="92e62-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="92e62-114">Opret en ny arbejdsgangsproces for enheden **Leverandør** ved hjælp af skabelonen for arbejdsgangsprocessen **Opret leverandører i Kontoenheden**, og tryk dernæst på **OK**.</span><span class="sxs-lookup"><span data-stu-id="92e62-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="92e62-115">Denne arbejdsgang håndterer leverandøroprettelsesscenariet for enheden **Konto**.</span><span class="sxs-lookup"><span data-stu-id="92e62-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="92e62-116">![Opret Leverandører i Kontoenhed](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="92e62-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="92e62-117">Opret en ny arbejdsgangsproces for enheden **Leverandør** ved hjælp af skabelonen for arbejdsgangsprocessen **Opdater Kontoenheder**, og tryk dernæst på **OK**.</span><span class="sxs-lookup"><span data-stu-id="92e62-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="92e62-118">Denne arbejdsgang håndterer opdateringsscenariet for leverandører for enheden **Konto**.</span><span class="sxs-lookup"><span data-stu-id="92e62-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="92e62-119">![Opdater Kontoenheder](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="92e62-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="92e62-120">Opret nye arbejdsgangsprocesser ud fra de skabeloner, der blev oprettet på enheden **Konti**.</span><span class="sxs-lookup"><span data-stu-id="92e62-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="92e62-121">![Opret leverandører i leverandørenheder](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="92e62-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="92e62-122">![Opdater leverandørenheder](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="92e62-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="92e62-123">Du kan konfigurere arbejdsprocesser som realtids- eller baggrundsarbejdsgange, der er baseret på dine krav.</span><span class="sxs-lookup"><span data-stu-id="92e62-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="92e62-124">![Konverter til en baggrundsarbejdsgang](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="92e62-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="92e62-125">Aktiver de arbejdsgange, du har oprettet på enhederne **Konto** og **Leverandør** for at påbegynde anvendelsen af enheden **Konto** til lagring af leverandøroplysninger.</span><span class="sxs-lookup"><span data-stu-id="92e62-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 
