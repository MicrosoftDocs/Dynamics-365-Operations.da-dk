---
title: Opret et dataintegratorprojekt (prøveversion)
description: Dette emne forklarer, hvordan du opretter et dataintegratorprojekt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 0029e093f524c61ff17a480ee3b881b3994ba95a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009437"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="a6b00-103">Opret et dataintegratorprojekt (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="a6b00-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a6b00-104">Dette emne forklarer, hvordan du opretter et dataintegratorprojekt.</span><span class="sxs-lookup"><span data-stu-id="a6b00-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="a6b00-105">Log på Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="a6b00-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="a6b00-106">Gå til **Arbejdsområder \> Datastyring**, og vælg **Dataenheder**.</span><span class="sxs-lookup"><span data-stu-id="a6b00-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="a6b00-107">Vent, indtil alle dataenheder er opdateret, før du går videre til næste trin.</span><span class="sxs-lookup"><span data-stu-id="a6b00-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="a6b00-108">Åbn [Power Apps-portalen](https://make.powerapps.com/), og udfør følgende trin:</span><span class="sxs-lookup"><span data-stu-id="a6b00-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="a6b00-109">Vælg det relevante miljø.</span><span class="sxs-lookup"><span data-stu-id="a6b00-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="a6b00-110">Vælg **Data \> Forbindelser** i den venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="a6b00-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="a6b00-111">Opret forbindelse til de relevante forekomster af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="a6b00-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="a6b00-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a6b00-112">Dynamics 365</span></span>
        - <span data-ttu-id="a6b00-113">Fin og Ops til Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a6b00-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="a6b00-114">Åbn [Power Apps-miljøer](https://admin.powerapps.com/environments), og udfør følgende trin:</span><span class="sxs-lookup"><span data-stu-id="a6b00-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="a6b00-115">Vælg **Dataintegrator**.</span><span class="sxs-lookup"><span data-stu-id="a6b00-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="a6b00-116">Vælg **Forbindelsessæt**.</span><span class="sxs-lookup"><span data-stu-id="a6b00-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="a6b00-117">Vælg **Nyt forbindelsessæt**.</span><span class="sxs-lookup"><span data-stu-id="a6b00-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="a6b00-118">Angiv et navn for forbindelsen.</span><span class="sxs-lookup"><span data-stu-id="a6b00-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="a6b00-119">Vælg de relevante forbindelser for følgende emner:</span><span class="sxs-lookup"><span data-stu-id="a6b00-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="a6b00-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a6b00-120">Dynamics 365</span></span>
        - <span data-ttu-id="a6b00-121">Fin og Ops til Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a6b00-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="a6b00-122">Vælg den relevante organisationstilknytning.</span><span class="sxs-lookup"><span data-stu-id="a6b00-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="a6b00-123">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="a6b00-123">Select **Create**.</span></span>

5. <span data-ttu-id="a6b00-124">Åbn [Power Apps-miljøer](https://admin.powerapps.com/environments), og udfør følgende trin:</span><span class="sxs-lookup"><span data-stu-id="a6b00-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="a6b00-125">Opret dataintegrationsprojekter til følgende skabeloner ved hjælp af det forbindelsessæt, du lige har oprettet:</span><span class="sxs-lookup"><span data-stu-id="a6b00-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="a6b00-126">Resultater af indsigt i kundebetaling (CDS til Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="a6b00-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="a6b00-127">Pengestrømsresultater for likviditetsserier (CDS Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="a6b00-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="a6b00-128">Budgetresultater for tidsserier (CDS Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="a6b00-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="a6b00-129">Angiv den relevante planlægning for hvert projekt.</span><span class="sxs-lookup"><span data-stu-id="a6b00-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="a6b00-130">Hvis du ikke kan se de påkrævede enheder i CDS, skal du gå til **Kredit og rykkere > Opsætning > Finance Insights > Finance Insights-parametre**, aktivere funktionen Debitorbetalingsforudsigelser og klikke på knappen **Opret forudsigelsesmodel**.</span><span class="sxs-lookup"><span data-stu-id="a6b00-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="a6b00-131">Når implementeringen af AI-modellen er fuldført (med eller uden succes), vil de CDS-enheder, der skal bruges til at oprette integrationen, blive installeret i CDS.</span><span class="sxs-lookup"><span data-stu-id="a6b00-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="a6b00-132">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="a6b00-132">Privacy notice</span></span>

<span data-ttu-id="a6b00-133">Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.</span><span class="sxs-lookup"><span data-stu-id="a6b00-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
