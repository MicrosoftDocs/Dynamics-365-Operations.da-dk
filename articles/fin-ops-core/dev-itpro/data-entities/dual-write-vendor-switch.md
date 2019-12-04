---
title: Skift mellem leverandørdesign
description: ''
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
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772358"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="94aea-102">Skift mellem leverandørdesign</span><span class="sxs-lookup"><span data-stu-id="94aea-102">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="94aea-103">Kreditordataflow</span><span class="sxs-lookup"><span data-stu-id="94aea-103">Vendor data flow</span></span> 

<span data-ttu-id="94aea-104">Hvis du bruger andre Dynamics 365-apps til leverandørhåndtering, og du vil adskille leverandøroplysningerne fra kundernes, kan du bruge dette grundlæggende leverandørdesign.</span><span class="sxs-lookup"><span data-stu-id="94aea-104">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Grundlæggende leverandørflow](media/dual-write-switch-1.png)
 
<span data-ttu-id="94aea-106">Hvis du bruger andre Dynamics 365-apps til leverandørhåndtering, og du fortsat vil bruge enheden **Konto** til at gemme leverandøroplysninger, kan du bruge dette udvidede leverandørdesign.</span><span class="sxs-lookup"><span data-stu-id="94aea-106">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="94aea-107">I dette design gemmes udvidede leverandøroplysninger som f.eks. leverandørers på hold-status og leverandørprofil i enheden **leverandører** i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="94aea-107">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Udvidet leverandørflow](media/dual-write-switch-2.png)
 
<span data-ttu-id="94aea-109">Følg nedenstående fremgangsmåde for at bruge det udvidede leverandør design:</span><span class="sxs-lookup"><span data-stu-id="94aea-109">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="94aea-110">Løsningspakken **SupplyChainCommon** indeholder skabeloner for arbejdsgangsproces som vist i følgende billede.</span><span class="sxs-lookup"><span data-stu-id="94aea-110">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="94aea-111">![Skabeloner for arbejdsgangsprocesser](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="94aea-111">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="94aea-112">Opret nye arbejdsgangsprocesser ved hjælp af arbejdsgangsprocesskabeloner:</span><span class="sxs-lookup"><span data-stu-id="94aea-112">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="94aea-113">Opret en ny arbejdsgangsproces for enheden **Leverandør** ved hjælp af skabelonen for arbejdsgangsprocessen **Opret leverandører i Kontoenheden**, og tryk dernæst på **OK**.</span><span class="sxs-lookup"><span data-stu-id="94aea-113">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="94aea-114">Denne arbejdsgang håndterer leverandøroprettelsesscenariet for enheden **Konto**.</span><span class="sxs-lookup"><span data-stu-id="94aea-114">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="94aea-115">![Opret Leverandører i Kontoenhed](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="94aea-115">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="94aea-116">Opret en ny arbejdsgangsproces for enheden **Leverandør** ved hjælp af skabelonen for arbejdsgangsprocessen **Opdater Kontoenheder**, og tryk dernæst på **OK**.</span><span class="sxs-lookup"><span data-stu-id="94aea-116">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="94aea-117">Denne arbejdsgang håndterer opdateringsscenariet for leverandører for enheden **Konto**.</span><span class="sxs-lookup"><span data-stu-id="94aea-117">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="94aea-118">![Opdater Kontoenheder](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="94aea-118">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="94aea-119">Opret nye arbejdsgangsprocesser ud fra de skabeloner, der blev oprettet på enheden **Konti**.</span><span class="sxs-lookup"><span data-stu-id="94aea-119">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="94aea-120">![Opret leverandører i leverandørenheder](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="94aea-120">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="94aea-121">![Opdater leverandørenheder](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="94aea-121">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="94aea-122">Du kan konfigurere arbejdsprocesser som realtids- eller baggrundsarbejdsgange, der er baseret på dine krav.</span><span class="sxs-lookup"><span data-stu-id="94aea-122">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="94aea-123">![Konverter til en baggrundsarbejdsgang](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="94aea-123">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="94aea-124">Aktiver de arbejdsgange, du har oprettet på enhederne **Konto** og **Leverandør** for at påbegynde anvendelsen af Customer Engagement-enheden **Konto** til lagring af leverandøroplysninger.</span><span class="sxs-lookup"><span data-stu-id="94aea-124">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the Customer Engagement **Account** entity for storing vendor information.</span></span> 
 
