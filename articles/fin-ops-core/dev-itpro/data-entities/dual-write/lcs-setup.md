---
title: Konfiguration af dobbeltskrivning fra Lifecycle Services
description: Dette emne beskriver, hvordan du konfigurerer en forbindelse med dobbeltskrivning fra Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103563"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="f3833-103">Konfiguration af dobbeltskrivning fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="f3833-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f3833-104">Dette emne beskriver, hvordan du aktiverer dobbeltskrivning fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f3833-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f3833-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="f3833-105">Prerequisites</span></span>

<span data-ttu-id="f3833-106">Du skal fuldføre Power Platform-integrationen som beskrevet i følgende emner:</span><span class="sxs-lookup"><span data-stu-id="f3833-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="f3833-107">Power Platform-integration – Aktiveres under installation af miljøet</span><span class="sxs-lookup"><span data-stu-id="f3833-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="f3833-108">Power Platform-integration – Konfigureres efter installation af miljøet</span><span class="sxs-lookup"><span data-stu-id="f3833-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="f3833-109">Konfigurere dobbeltskrivning for nye Dataverse-miljøer</span><span class="sxs-lookup"><span data-stu-id="f3833-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="f3833-110">Følg disse trin for at konfigurere dobbeltskrivning fra LCS-siden **Miljøoplysninger**:</span><span class="sxs-lookup"><span data-stu-id="f3833-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="f3833-111">Udvid sektionen **Power Platform-integration** på siden **Miljøoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="f3833-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="f3833-112">Vælg knappen **Dobbeltskrivningsapplikation**.</span><span class="sxs-lookup"><span data-stu-id="f3833-112">Select the **Dual-write application** button.</span></span>

    ![Power Platform-integration](media/powerplat_integration_step2.png)

3. <span data-ttu-id="f3833-114">Gennemse vilkår og betingelser, og markér afkrydsningsfeltet **Konfigurer**.</span><span class="sxs-lookup"><span data-stu-id="f3833-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="f3833-115">Vælg **OK** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="f3833-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="f3833-116">Du kan overvåge status ved at opdatere siden med miljøoplysninger med jævne mellemrum.</span><span class="sxs-lookup"><span data-stu-id="f3833-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="f3833-117">Konfigurationen tager typisk 30 minutter eller mindre.</span><span class="sxs-lookup"><span data-stu-id="f3833-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="f3833-118">Når installationen er fuldført, vises der en meddelelse, som fortæller, om processen lykkedes, eller om der opstod en fejl.</span><span class="sxs-lookup"><span data-stu-id="f3833-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="f3833-119">Hvis installationen mislykkedes, vises der en relateret fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="f3833-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="f3833-120">Du skal rette eventuelle fejl, før du går videre til næste trin.</span><span class="sxs-lookup"><span data-stu-id="f3833-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="f3833-121">Vælg **Link til Power Platform-miljø** for at oprette en kæde mellem Dataverse og databaserne i det aktuelle miljø.</span><span class="sxs-lookup"><span data-stu-id="f3833-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="f3833-122">Det tager typisk mindre end 5 minutter.</span><span class="sxs-lookup"><span data-stu-id="f3833-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Link til Power Platform-miljø":::

8. <span data-ttu-id="f3833-124">Når sammenkædningen er fuldført, vises der et link.</span><span class="sxs-lookup"><span data-stu-id="f3833-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="f3833-125">Brug linket til at logge på administrationsområdet med dobbeltskrivning i Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="f3833-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="f3833-126">Herfra kan du oprette objekttilknytninger.</span><span class="sxs-lookup"><span data-stu-id="f3833-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="f3833-127">Konfigurere dobbeltskrivning for et eksisterende Dataverse-miljø</span><span class="sxs-lookup"><span data-stu-id="f3833-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="f3833-128">Hvis du vil konfigurere dobbeltskrivning for et eksisterende Dataverse-miljø, skal du oprette en Microsoft-[supportanmodning](../../lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="f3833-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="f3833-129">Anmodningen skal indeholde:</span><span class="sxs-lookup"><span data-stu-id="f3833-129">The ticket must include:</span></span>

+ <span data-ttu-id="f3833-130">Dit Finance and Operations-miljø-id.</span><span class="sxs-lookup"><span data-stu-id="f3833-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="f3833-131">Dit miljønavn fra Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="f3833-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="f3833-132">Dataverse-organisations-id'et eller Power Platform-miljø-id'et fra Power Platform Administration.</span><span class="sxs-lookup"><span data-stu-id="f3833-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="f3833-133">I din anmodning skal du anmode om, at id'et skal være den forekomst, der bruges til Power Platform-integration.</span><span class="sxs-lookup"><span data-stu-id="f3833-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="f3833-134">Du kan ikke fjerne sammenkædningen mellem miljøer ved hjælp af LCS.</span><span class="sxs-lookup"><span data-stu-id="f3833-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="f3833-135">Hvis du vil fjerne sammenkædningen mellem et miljø, skal du åbne arbejdsområdet **Dataintegration** i Finance and Operations-miljøet og derefter vælge **Fjern sammenkædning**.</span><span class="sxs-lookup"><span data-stu-id="f3833-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
