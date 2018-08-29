---
title: Project Service Automation
description: "Dette emne indeholder oplysninger om Project Service Automation til integrationsløsningen til Finance and Operations. Denne integrationsløsning bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation via Common Data Service."
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="930b8-104">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="930b8-104">Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="930b8-105">Løsningen integration af Project Service Automation med Finance and Operations bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="930b8-105">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="930b8-106">Integrationsskabelonerne, der er tilgængelige med dataintegrationsfunktionen, muliggør strømmen af projekter, projektkontrakter, projektkontraktlinjer, milepæle i projektkontraktlinjer, projektopgaver, udgiftstransaktionskategorier, timeestimater og udgiftsestimater fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="930b8-106">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="930b8-107">Hvis du bruger Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, 7.3.0, når du har installeret KB 4132657 og KB 4132660, kan du bruge skabelonerne til at integrere projektopgaver, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og faktiske oplysninger og konfigurere låsning af funktionalitet.</span><span class="sxs-lookup"><span data-stu-id="930b8-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="930b8-108">Hvis du skal nulstille regnskabsfordelingerne, anbefaler vi, at du også installerer KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="930b8-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="930b8-109">Hvis du bruger Finance and Operations 7.3.0, skal du installere KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="930b8-109">If you're using Finance and Operations 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="930b8-110">Du vil så være i stand til at integrere fastprisprojekter.</span><span class="sxs-lookup"><span data-stu-id="930b8-110">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="930b8-111">Hvis du bruger Finance and Operations 7.3.0, og du bringer gebyrtransaktioner fra Project Service Automation, skal du installere KB 4345320 for at medtage disse gebyrer i projektfakturaen.</span><span class="sxs-lookup"><span data-stu-id="930b8-111">If you're using Finance and Operations 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="930b8-112">Hvis du bruger Microsoft Dynamics 365 for Finance and Operations version 8.0, kan du bruge projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner.</span><span class="sxs-lookup"><span data-stu-id="930b8-112">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="930b8-113">Hvis du bruger Microsoft Dynamics 365 for Finance and Operations version 8.0.1 eller nyere, kan du synkronisere faktiske oplysninger.</span><span class="sxs-lookup"><span data-stu-id="930b8-113">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0.1, or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="930b8-114">Før du kan integrere Project Service Automation med Finance and Operations, skal du konfigurere integrationsparametrene for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="930b8-114">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="930b8-115">Du kan finde flere oplysninger under [Integrationsparametre for Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="930b8-115">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="930b8-116">Denne integrationsløsning muliggør direkte synkronisering i følgende situationer:</span><span class="sxs-lookup"><span data-stu-id="930b8-116">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="930b8-117">Vedligeholde projektkontrakter i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="930b8-117">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="930b8-118">Oprette projekter i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="930b8-118">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="930b8-119">Vedligeholde projektkontraktlinjer i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="930b8-119">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="930b8-120">Vedligeholde milepæle i projektkontraktlinjer i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="930b8-120">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="930b8-121">Vedligeholde projektopgaver i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="930b8-121">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="930b8-122">Vedligeholde udgiftstransaktionskategorier i Finance and Operations og synkronisere dem direkte fra Finance and Operations til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="930b8-122">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="930b8-123">Oprette projekttimeestimater i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="930b8-123">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="930b8-124">Oprette projektudgiftsestimater i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="930b8-124">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="930b8-125">Oprette faktiske tal for projekttid, udgifter og gebyr i Project Service Automation og oprette projektposteringer i Project Service Automation-integrationskladden, så de kan bogføres i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="930b8-125">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="930b8-126">Datasynkronisering</span><span class="sxs-lookup"><span data-stu-id="930b8-126">Data synchronization</span></span>

<span data-ttu-id="930b8-127">I følgende illustration vises, hvordan data synkroniseres som et led i integrationen mellem Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="930b8-127">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="930b8-128">Ikke alle skabeloner er tilgængelige for øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="930b8-128">Not all templates are currently available.</span></span> <span data-ttu-id="930b8-129">Skabeloner udgives, efterhånden som de fuldføres.</span><span class="sxs-lookup"><span data-stu-id="930b8-129">Templates will be released as they are completed.</span></span>

<span data-ttu-id="930b8-130">[![Project Service Automation-integration med Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="930b8-130">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="930b8-131">Systemkrav til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="930b8-131">System requirements for Finance and Operations</span></span>

<span data-ttu-id="930b8-132">Når du vil bruge løsningen til integration af Project Service Automation med Finance and Operations, skal du installere Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 med platformsopdatering 12 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="930b8-132">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="930b8-133">Systemkravene til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="930b8-133">System requirements for Project Service Automation</span></span>

<span data-ttu-id="930b8-134">Når du vil bruge løsningen til integration af Project Service Automation med Finance and Operations, skal du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="930b8-134">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="930b8-135">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="930b8-135">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="930b8-136">Løsningen Kundeemne til kontanter til Microsoft Dynamics 365 for Sales, version 1.14.0.0 (v14) eller nyere.</span><span class="sxs-lookup"><span data-stu-id="930b8-136">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="930b8-137">Project Service Automation til Finance and Operations-løsningen til Microsoft Dynamics 365 for Project Service Automation version 1.0.0.0 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="930b8-137">Project Service Automation to Finance and Operations solution for Microsoft Dynamics 365 for Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="930b8-138">Installer løsningen til integration af Project Service Automation med Finance and Operations i din Project Service Automation-forekomst</span><span class="sxs-lookup"><span data-stu-id="930b8-138">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="930b8-139">Hente Project Service Automation til Finance and Operations-integrationsløsning fra [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=57016), og følg vejledningen, der er inkluderet i løsningen.</span><span class="sxs-lookup"><span data-stu-id="930b8-139">Download the Project Service Automation to Finance and Operations integration solution from [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>

