---
title: Project Service Automation
description: "Denne løsning bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation via Common Data Service (CDS)."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: da-dk
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="8a6dd-103">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8a6dd-103">Project Service Automation</span></span>

<span data-ttu-id="8a6dd-104">Løsningen integration af Project Service Automation med Finance and Operations bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation via Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="8a6dd-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="8a6dd-105">Integrationsskabelonerne, der er tilgængelige med dataintegrationsfunktionen, muliggør strømmen af projekter, projektkontrakter, projektkontraktlinjer, milepæle i projektkontraktlinjer, projektopgaver, udgiftstransaktionskategorier, timeestimater og udgiftsestimater fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="8a6dd-106">Hvis du bruger Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, skal du installere KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="8a6dd-107">Dette gør det muligt for dig at integrere fastprisprojekter.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="8a6dd-108">Hvis du bruger Dynamics 365 for Finance and Operations version 8.0, kan du bruge projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="8a6dd-109">Hvis du bruger Dynamics 365 for Finance and Operations version 8.0.1, kan du synkronisere faktiske oplysninger.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="8a6dd-110">Hvis du bruger Dynamics 365 for Finance and Operations, Enterprise edition, 7.3.0, når du har installeret KB 4132657 og KB 4132660, kan du bruge skabelonerne til at integrere projektopgaver, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og faktiske oplysninger og konfigurere låsning af funktionalitet.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="8a6dd-111">Hvis du skal nulstille regnskabsfordelingerne, anbefaler vi, at du også installerer KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="8a6dd-112">Før du kan integrere Project Service Automation med Finance and Operations, skal du konfigurere integrationsparametrene for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="8a6dd-113">Du kan finde flere oplysninger under integrationsparametre for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="8a6dd-114">Denne integrationsløsning muliggør direkte synkronisering i følgende situationer:</span><span class="sxs-lookup"><span data-stu-id="8a6dd-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="8a6dd-115">Vedligeholde projektkontrakter i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="8a6dd-116">Oprette projekter i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="8a6dd-117">Vedligeholde projektkontraktlinjer i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="8a6dd-118">Vedligeholde milepæle i projektkontraktlinjer i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="8a6dd-119">Vedligeholde projektopgaver i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="8a6dd-120">Vedligeholde udgiftstransaktionskategorier i Finance and Operations og synkronisere dem direkte fra Finance and Operations til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="8a6dd-121">Oprette projekttimeestimater i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="8a6dd-122">Oprette projektudgiftsestimater i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="8a6dd-123">Datasynkronisering</span><span class="sxs-lookup"><span data-stu-id="8a6dd-123">Data synchronization</span></span>
<span data-ttu-id="8a6dd-124">I følgende illustration vises, hvordan data synkroniseres som et led i integrationen mellem Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="8a6dd-125">Ikke alle skabeloner er tilgængelige for øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-125">Not all templates are currently available.</span></span> <span data-ttu-id="8a6dd-126">Skabeloner udgives, efterhånden som de fuldføres.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="8a6dd-127">[![Project Service Automation-integration med Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="8a6dd-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="8a6dd-128">Systemkrav til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8a6dd-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="8a6dd-129">Når du vil bruge løsningen til integration af Project Service Automation med Finance and Operations, skal du installere Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 med platformsopdatering 12 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="8a6dd-130">Systemkravene til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8a6dd-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="8a6dd-131">Når du vil bruge løsningen til integration af Project Service Automation med Finance and Operations, skal du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="8a6dd-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="8a6dd-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="8a6dd-133">Løsningen Kundeemne til kontanter til Dynamics 365 for Sales, version 1.14.0.0 (v14) eller nyere.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="8a6dd-134">Project Service Automation til Operations-løsningen for Dynamics 365 for Project Service Automation version 1.0.0.0 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="8a6dd-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="8a6dd-135">Installer løsningen til integration af Project Service Automation med Finance and Operations i din Project Service Automation-forekomst</span><span class="sxs-lookup"><span data-stu-id="8a6dd-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



