---
title: Konfigurere et eksperiment
description: Dette emne beskriver, hvordan du konfigurerer et eksperiment i en tredjepartstjeneste.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 29c21ceb4c259f463f4a039942e51141201a9809
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097041"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="dfe2d-103">Konfigurere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="dfe2d-103">Set up an experiment</span></span>

<span data-ttu-id="dfe2d-104">Når du [definerer en hypotese og bestemmer, hvilke succesmålepunkter du vil bruge](experimentation-identify.md), skal du konfigurere dit eksperiment i tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="dfe2d-105">I følgende diagram vises alle de trin, der er nødvendige for at konfigurere og køre et eksperiment på et e-handelswebsted i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="dfe2d-106">Yderligere trin behandles i separate emner.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="dfe2d-107">[ ![Eksperimenteringens brugerrejse - konfiguration](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="dfe2d-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="dfe2d-108">Konfigurere dit eksperiment i tredjepartstjenesten</span><span class="sxs-lookup"><span data-stu-id="dfe2d-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="dfe2d-109">Nu skulle du have valgt en tredjepartstjeneste til at køre og overvåge dit eksperiment, så du kan konfigurere eksperimenteren-connectoren.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="dfe2d-110">Disse forudsætninger er angivet i [Eksperimenteren i Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dfe2d-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="dfe2d-111">Følg de trin, der er nødvendige for at oprette dit eksperiment i tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="dfe2d-112">Hvis connectoren er konfigureret korrekt, vil den fuldstændige liste over de eksperimenter, du konfigurerer i tredjepartstjenesten, blive synlig i Commerce-webstedsgeneratoren inden for 5 minutter.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will appear in Commerce site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="dfe2d-113">Konfigurere succesmålepunkter</span><span class="sxs-lookup"><span data-stu-id="dfe2d-113">Set up your success metrics</span></span>
<span data-ttu-id="dfe2d-114">Alle eksperimenter skal bruge målepunkter til måling af variationernes effekt og for at validere hypotesen.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="dfe2d-115">Benyt følgende fremgangsmåde for at aktivere beregning af målepunkter i tredjepartstjenesten ved hjælp af hændelser med live telemetri fra Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="dfe2d-116">Benyt følgende fremgangsmåde for at konfigurere succesmålepunkter.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-116">To set up your success metrics, follow these steps.</span></span>

1. <span data-ttu-id="dfe2d-117">I Commerce-webstedsgeneratoren skal du vælge **Sider** i venstre navigationsrude og derefter vælge den side, du vil indsamle målepunkter for.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-117">In Commerce site builder, select **Pages** in the left navigation pane, and then select the page that you want to collect metrics for.</span></span> 
1. <span data-ttu-id="dfe2d-118">Gå til sektionen **Hændelses-id'er, der skal spores** i egenskabsruden til højre for den side eller det modul, du vil spore.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-118">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="dfe2d-119">Vælg **Vis**.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-119">Select **View**.</span></span> <span data-ttu-id="dfe2d-120">Der vises en liste over alle hændelses-id'er.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-120">A list of all event IDs is displayed.</span></span> <span data-ttu-id="dfe2d-121">Kopiér den hændelse, du vil spore, og Indsæt hændelsesnøglen på den angivne placering i tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-121">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="dfe2d-122">Hvis du skal bruge mere end én hændelse, skal du kopiere nøglerne én ad gangen.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-122">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="dfe2d-123">Du kan få mere at vide om, hvordan du kan få vist alle tilgængelige hændelser og attributter, herunder sidevisninger og sporing af omsætning, under [Commerce-komponenthændelser for diagnosticering og fejlfinding](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="dfe2d-123">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="dfe2d-124">Udfør andre trin for at spore de påkrævede målepunkter i tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-124">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="dfe2d-125">Forrige trin</span><span class="sxs-lookup"><span data-stu-id="dfe2d-125">Previous step</span></span>
[<span data-ttu-id="dfe2d-126">Identificere en hypotese og fastslå målepunkter for et eksperiment</span><span class="sxs-lookup"><span data-stu-id="dfe2d-126">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="dfe2d-127">Næste trin</span><span class="sxs-lookup"><span data-stu-id="dfe2d-127">Next step</span></span>
[<span data-ttu-id="dfe2d-128">Tilslutte og redigere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="dfe2d-128">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)
