---
title: Opret et dataintegratorprojekt (prøveversion)
description: Dette emne forklarer, hvordan du opretter et dataintegratorprojekt.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 59f85c64ea7b1f539a245e08b76bd6a34797b0ca
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186462"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="cc000-103">Opret et dataintegratorprojekt (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="cc000-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="cc000-104">Dette emne forklarer, hvordan du opretter et dataintegratorprojekt.</span><span class="sxs-lookup"><span data-stu-id="cc000-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="cc000-105">Log på Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="cc000-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="cc000-106">Gå til **Arbejdsområder \> Datastyring**, og vælg **Dataenheder**.</span><span class="sxs-lookup"><span data-stu-id="cc000-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="cc000-107">Vent, indtil alle dataenheder er opdateret, før du går videre til næste trin.</span><span class="sxs-lookup"><span data-stu-id="cc000-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="cc000-108">Åbn [Power Apps-portalen](https://make.powerapps.com/), og udfør følgende trin:</span><span class="sxs-lookup"><span data-stu-id="cc000-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="cc000-109">Vælg det relevante miljø.</span><span class="sxs-lookup"><span data-stu-id="cc000-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="cc000-110">Vælg **Data \> Forbindelser** i den venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="cc000-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="cc000-111">Opret forbindelse til de relevante forekomster af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="cc000-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="cc000-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="cc000-112">Dynamics 365</span></span>
        - <span data-ttu-id="cc000-113">Fin og Ops til Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="cc000-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="cc000-114">Åbn [Power Apps-miljøer](https://admin.powerapps.com/environments), og udfør følgende trin:</span><span class="sxs-lookup"><span data-stu-id="cc000-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="cc000-115">Vælg **Dataintegrator**.</span><span class="sxs-lookup"><span data-stu-id="cc000-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="cc000-116">Vælg **Forbindelsessæt**.</span><span class="sxs-lookup"><span data-stu-id="cc000-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="cc000-117">Vælg **Nyt forbindelsessæt**.</span><span class="sxs-lookup"><span data-stu-id="cc000-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="cc000-118">Angiv et navn for forbindelsen.</span><span class="sxs-lookup"><span data-stu-id="cc000-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="cc000-119">Vælg de relevante forbindelser for følgende emner:</span><span class="sxs-lookup"><span data-stu-id="cc000-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="cc000-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="cc000-120">Dynamics 365</span></span>
        - <span data-ttu-id="cc000-121">Fin og Ops til Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="cc000-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="cc000-122">Vælg den relevante organisationstilknytning.</span><span class="sxs-lookup"><span data-stu-id="cc000-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="cc000-123">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="cc000-123">Select **Create**.</span></span>

5. <span data-ttu-id="cc000-124">Åbn [Power Apps-miljøer](https://admin.powerapps.com/environments), og udfør følgende trin:</span><span class="sxs-lookup"><span data-stu-id="cc000-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="cc000-125">Opret dataintegrationsprojekter til følgende skabeloner ved hjælp af det forbindelsessæt, du lige har oprettet:</span><span class="sxs-lookup"><span data-stu-id="cc000-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="cc000-126">Resultater af indsigt i kundebetaling (CDS til Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="cc000-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
            - <span data-ttu-id="cc000-127">Hvis du bruger version 10.0.17 eller senere, skal du bruge skabelonen med navnet Resultater af indsigt i kundebetaling (CDS til Fin og Ops 10.0.17+).</span><span class="sxs-lookup"><span data-stu-id="cc000-127">If you are using version 10.0.17 or later, you need to use the template named, Customer payment insights result (CDS to Fin and Ops 10.0.17+).</span></span>
        - <span data-ttu-id="cc000-128">Pengestrømsresultater for likviditetsserier (CDS Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="cc000-128">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="cc000-129">Budgetresultater for tidsserier (CDS Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="cc000-129">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="cc000-130">Angiv den relevante planlægning for hvert projekt.</span><span class="sxs-lookup"><span data-stu-id="cc000-130">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="cc000-131">Hvis du ikke kan se de påkrævede enheder i CDS, skal du gå til **Kredit og rykkere > Opsætning > Finance Insights > Finance Insights-parametre**, aktivere funktionen Debitorbetalingsforudsigelser og klikke på knappen **Opret forudsigelsesmodel**.</span><span class="sxs-lookup"><span data-stu-id="cc000-131">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="cc000-132">Når implementeringen af AI-modellen er fuldført (med eller uden succes), vil de CDS-enheder, der skal bruges til at oprette integrationen, blive installeret i CDS.</span><span class="sxs-lookup"><span data-stu-id="cc000-132">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
