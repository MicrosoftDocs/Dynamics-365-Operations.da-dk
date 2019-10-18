---
title: Oversigt over Project Service Automation
description: Dette emne indeholder oplysninger om Dynamics 365 Project Service Automation til Dynamics 365 Finance-integrationsløsningen.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250547"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="bcb42-103">Oversigt over Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="bcb42-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bcb42-104">Project Service Automation til Finance-integrationsløsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Dynamics 365 Finance og Dynamics 365 Project Service Automation via Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="bcb42-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="bcb42-105">Integrationsskabelonerne, der er tilgængelige med dataintegrationsfunktionen, muliggør strømmen af projekter, projektkontrakter, projektkontraktlinjer, milepæle i projektkontraktlinjer, projektopgaver, udgiftstransaktionskategorier, timeestimater og udgiftsestimater fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="bcb42-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="bcb42-106">Hvis du bruger version 7.3.0, skal du installere KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="bcb42-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="bcb42-107">Du vil så være i stand til at integrere fastprisprojekter.</span><span class="sxs-lookup"><span data-stu-id="bcb42-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="bcb42-108">Hvis du bruger version 7.3.0, og du bringer gebyrtransaktioner fra Project Service Automation, skal du installere KB 4345320 for at medtage disse gebyrer i projektfakturaen.</span><span class="sxs-lookup"><span data-stu-id="bcb42-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="bcb42-109">Hvis du bruger version 8.0, kan du bruge projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner.</span><span class="sxs-lookup"><span data-stu-id="bcb42-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="bcb42-110">Hvis du bruger version 8.0.1 eller nyere, kan du synkronisere faktiske oplysninger.</span><span class="sxs-lookup"><span data-stu-id="bcb42-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="bcb42-111">Før du kan integrere Project Service Automation med Finance, skal du konfigurere integrationsparametrene for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bcb42-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="bcb42-112">Du kan finde flere oplysninger under [Integrationsparametre for Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bcb42-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="bcb42-113">Denne integrationsløsning muliggør direkte synkronisering i følgende situationer:</span><span class="sxs-lookup"><span data-stu-id="bcb42-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="bcb42-114">Vedligeholde projektkontrakter i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="bcb42-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="bcb42-115">Oprette projekter i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="bcb42-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="bcb42-116">Vedligeholde projektkontraktlinjer i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="bcb42-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="bcb42-117">Vedligeholde milepæle for projektkontraktlinjer i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="bcb42-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="bcb42-118">Vedligeholde projektopgaver i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="bcb42-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="bcb42-119">Vedligeholde udgiftstransaktionskategorier i Finance og synkronisere dem direkte fra Finance til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bcb42-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="bcb42-120">Oprette projekttimeestimater i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="bcb42-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="bcb42-121">Oprette projektudgiftsestimater i Project Service Automation og synkronisere dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="bcb42-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="bcb42-122">Oprette faktiske tal for projekttid, udgifter og gebyr i Project Service Automation og oprette projektposteringer i Project Service Automation-integrationskladden, så de kan bogføres i Finance.</span><span class="sxs-lookup"><span data-stu-id="bcb42-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="bcb42-123">Datasynkronisering</span><span class="sxs-lookup"><span data-stu-id="bcb42-123">Data synchronization</span></span>

<span data-ttu-id="bcb42-124">I følgende illustration vises, hvordan data synkroniseres som et led i integrationen mellem Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="bcb42-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="bcb42-125">Ikke alle skabeloner er tilgængelige for øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="bcb42-125">Not all templates are currently available.</span></span> <span data-ttu-id="bcb42-126">Skabeloner udgives, efterhånden som de fuldføres.</span><span class="sxs-lookup"><span data-stu-id="bcb42-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="bcb42-127">[![Project Service Automation-integration med Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="bcb42-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="bcb42-128">Systemkrav til Finance</span><span class="sxs-lookup"><span data-stu-id="bcb42-128">System requirements for Finance</span></span>

<span data-ttu-id="bcb42-129">Når du vil bruge løsningen til integration af Project Service Automation med Finance, skal du installere Enterprise edition 7.3 med Platform update 12 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="bcb42-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="bcb42-130">Systemkravene til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="bcb42-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="bcb42-131">Når du vil bruge løsningen til integration af Project Service Automation med Finance, skal du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="bcb42-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="bcb42-132">Dynamics 365 Project Service Automation version 9.0.0.0 eller nyere</span><span class="sxs-lookup"><span data-stu-id="bcb42-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="bcb42-133">Løsningen Kundeemne til kontanter til Dynamics 365 Sales, version 1.14.0.0 (v14) eller nyere.</span><span class="sxs-lookup"><span data-stu-id="bcb42-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="bcb42-134">Løsning til integration af Project Service Automation med Finance til Dynamics 365 Project Service Automation version 1.0.0.0 eller nyere</span><span class="sxs-lookup"><span data-stu-id="bcb42-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="bcb42-135">Installer løsningen til integration af Project Service Automation med Finance i din Project Service Automation-forekomst.</span><span class="sxs-lookup"><span data-stu-id="bcb42-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="bcb42-136">Download Project Service Automation til Finance-integrationsløsning fra [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), og følg vejledningen, der er inkluderet i løsningen.</span><span class="sxs-lookup"><span data-stu-id="bcb42-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
