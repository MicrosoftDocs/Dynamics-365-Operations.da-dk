---
title: Understøttede scenarier til installation med to skrivninger
description: I dette emne beskrives de scenarier, der understøttes til installation med to skrivninger.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1319f1228b635e207754f7c2516cb2b5353a9edd
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112409"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="14332-103">Understøttede scenarier til installation med to skrivninger</span><span class="sxs-lookup"><span data-stu-id="14332-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="14332-104">Du kan oprette en forbindelse med to skrivninger mellem et Finance and Operations-miljø og et Common Data Service-miljø.</span><span class="sxs-lookup"><span data-stu-id="14332-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="14332-105">Et **Finance and Operations-miljø** leverer den underliggende platform for **Finance and Operations-apps** (f.eks Microsoft Dynamics 365 Finance. Dynamics 365 Supply Chain Management, Dynamics 365 Retail og Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="14332-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="14332-106">Et **Common Data Service-miljø** giver den underliggende platform for **modelstyrede apps i Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="14332-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

<span data-ttu-id="14332-107">Konfigurationsmekanismen varierer, afhængigt af dit abonnement og miljøet.</span><span class="sxs-lookup"><span data-stu-id="14332-107">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="14332-108">Ved nye forekomster af Finance and Operations-apps begynder opsætningen af en forbindelse med to skrivninger i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="14332-108">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="14332-109">Hvis du har en licens til Microsoft Power Platform, vil du få et nyt Common Data Service-miljø, hvis din lejer ikke har en.</span><span class="sxs-lookup"><span data-stu-id="14332-109">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="14332-110">For eksisterende forekomster af Finance and Operations-apps begynder opsætningen af en forbindelse med to skrivninger i Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="14332-110">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="14332-111">Følgende konfigurationsscenarier understøttes:</span><span class="sxs-lookup"><span data-stu-id="14332-111">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="14332-112">En ny Finance and Operations-app-forekomst og en ny modeldrevet app-forekomst</span><span class="sxs-lookup"><span data-stu-id="14332-112">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="14332-113">En ny Finance and Operations-app-forekomst og en eksisterende modeldrevet app-forekomst</span><span class="sxs-lookup"><span data-stu-id="14332-113">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="14332-114">En ny Finance and Operations-app-forekomst, som har demodata og en ny modeldrevet app-forekomst</span><span class="sxs-lookup"><span data-stu-id="14332-114">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="14332-115">En ny Finance and Operations-app-forekomst, som har demodata og en eksisterende modeldrevet app-forekomst</span><span class="sxs-lookup"><span data-stu-id="14332-115">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="14332-116">En eksisterende Finance and Operations-app-forekomst og en ny modeldrevet app-forekomst</span><span class="sxs-lookup"><span data-stu-id="14332-116">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="14332-117">En ny Finance and Operations-app-forekomst og en ny modeldrevet app-forekomst</span><span class="sxs-lookup"><span data-stu-id="14332-117">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="14332-118">Hvis du vil oprette en forbindelse med to skrivninger mellem en ny forekomst af en Finance and Operations-app, der ikke har data, og en ny forekomst af en modeldrevet app i Dynamics 365, skal du følge trinnene i [Opsætning af en forbindelse med to skrivninger fra Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="14332-118">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="14332-119">Når opsætningen af forbindelsen er fuldført, sker følgende handlinger automatisk:</span><span class="sxs-lookup"><span data-stu-id="14332-119">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="14332-120">Der klargøres et nyt tomt Finance and Operations-miljø.</span><span class="sxs-lookup"><span data-stu-id="14332-120">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="14332-121">Der klargøres en ny tom forekomst af en modeldrevet app, hvor CRM standardløsningen installeres.</span><span class="sxs-lookup"><span data-stu-id="14332-121">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="14332-122">Der oprettes en forbindelse med to skrivninger for DAT-virksomhedsdata.</span><span class="sxs-lookup"><span data-stu-id="14332-122">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="14332-123">Enhedstilknytninger er aktiveret til direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="14332-123">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="14332-124">Begge miljøer er derefter klar til dynamisk datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="14332-124">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="14332-125">En ny Finance and Operations-app-forekomst og en eksisterende modeldrevet app-forekomst</span><span class="sxs-lookup"><span data-stu-id="14332-125">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="14332-126">Hvis du vil oprette en forbindelse med to skrivninger mellem en ny forekomst af en Finance and Operations-app, der ikke har data, og en eksisterende forekomst af en modeldrevet app i Dynamics 365, skal du følge trinnene i [Opsætning af en forbindelse med to skrivninger fra Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="14332-126">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="14332-127">Når opsætningen af forbindelsen er fuldført, sker følgende handlinger automatisk:</span><span class="sxs-lookup"><span data-stu-id="14332-127">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="14332-128">Der klargøres et nyt tomt Finance and Operations-miljø.</span><span class="sxs-lookup"><span data-stu-id="14332-128">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="14332-129">Der oprettes en forbindelse med to skrivninger for DAT-virksomhedsdata.</span><span class="sxs-lookup"><span data-stu-id="14332-129">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="14332-130">Enhedstilknytninger er aktiveret til direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="14332-130">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="14332-131">Begge miljøer er derefter klar til dynamisk datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="14332-131">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="14332-132">Udfør følgende trin for at synkronisere Common Data Service-data til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="14332-132">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="14332-133">Opret et nyt regnskab i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="14332-133">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="14332-134">Føj firmaet til opsætningen af forbindelsen med to skrivninger.</span><span class="sxs-lookup"><span data-stu-id="14332-134">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="14332-135">[Bootstrap](bootstrap-company-data.md) Common Data Service-dataene ved hjælp af en ISO-virksomhedskode (International Organization for Standardization) på tre bogstaver.</span><span class="sxs-lookup"><span data-stu-id="14332-135">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="14332-136">Da to skrivninger er i direkte synkroniseringstilstand, starter dataene fra Common Data Service automatisk med at strømme til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="14332-136">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="14332-137">En ny Finance and Operations-app-forekomst, som har demodata og en ny modeldrevet app-forekomst</span><span class="sxs-lookup"><span data-stu-id="14332-137">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="14332-138">Hvis du vil oprette en forbindelse med to skrivninger mellem en ny forekomst af en Finance and Operations-app, der har demonstrationsdata og en ny forekomst af en modeldrevet app i Dynamics 365, skal du følge trinnene i afsnittet [En ny Finance and Operations-app-forekomst og en ny modeldrevet app-forekomst](#new-new) tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="14332-138">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="14332-139">Når opsætningen af forbindelsen er fuldført, skal du udføre følgende trin, hvis du vil synkronisere demodataene til den modelbaserede app.</span><span class="sxs-lookup"><span data-stu-id="14332-139">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="14332-140">Åbn Finance and Operations-appen fra siden LCS, log på, og gå derefter til **Datastyring \> To skrivninger**.</span><span class="sxs-lookup"><span data-stu-id="14332-140">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="14332-141">Kør den **første synkroniseringsfunktion** for de enheder, du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="14332-141">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="14332-142">En ny Finance and Operations-app-forekomst, som har demodata og en eksisterende modeldrevet app-forekomst</span><span class="sxs-lookup"><span data-stu-id="14332-142">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="14332-143">Hvis du vil oprette en forbindelse med to skrivninger mellem en ny forekomst af en Finance and Operations-app, der har demonstrationsdata og en eksisterende forekomst af en modeldrevet app i Dynamics 365, skal du følge trinnene i afsnittet [En ny Finance and Operations-app-forekomst og en eksisterende modeldrevet app-forekomst](#new-existing) tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="14332-143">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="14332-144">Når opsætningen af forbindelsen er fuldført, skal du udføre følgende trin, hvis du vil synkronisere demodataene til den modelbaserede app.</span><span class="sxs-lookup"><span data-stu-id="14332-144">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="14332-145">Åbn Finance and Operations-appen fra siden LCS, log på, og gå derefter til **Datastyring \> To skrivninger**.</span><span class="sxs-lookup"><span data-stu-id="14332-145">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="14332-146">Kør den **første synkroniseringsfunktion** for de enheder, du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="14332-146">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="14332-147">Udfør følgende trin for at synkronisere Common Data Service-data til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="14332-147">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="14332-148">Opret et nyt regnskab i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="14332-148">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="14332-149">Føj firmaet til opsætningen af forbindelsen med to skrivninger.</span><span class="sxs-lookup"><span data-stu-id="14332-149">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="14332-150">[Bootstrap](bootstrap-company-data.md) Common Data Service-dataene ved hjælp af en ISO-virksomhedskode på tre bogstaver.</span><span class="sxs-lookup"><span data-stu-id="14332-150">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="14332-151">Da to skrivninger er i direkte synkroniseringstilstand, starter dataene fra Common Data Service automatisk med at strømme til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="14332-151">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="14332-152">En eksisterende Finance and Operations-app-forekomst og en ny modeldrevet app-forekomst</span><span class="sxs-lookup"><span data-stu-id="14332-152">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="14332-153">Opsætningen af en forbindelse med tom skrivninger mellem en eksisterende forekomst af en Finance and Operations-app og en ny eller eksisterende forekomst af en modelbaseret app i Dynamics 365 forekommer i økonomi- og handlingsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="14332-153">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="14332-154">Konfigurer forbindelsen fra Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="14332-154">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="14332-155">Hvis du vil synkronisere eksisterende Common Data Service-data med Finance and Operations-appen, skal du udføre en [bootstrap](bootstrap-company-data.md) på Common Data Service-dataene ved hjælp af en ISO-virksomhedskode på tre bogstaver.</span><span class="sxs-lookup"><span data-stu-id="14332-155">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="14332-156">Da to skrivninger er i direkte synkroniseringstilstand, starter dataene fra Common Data Service automatisk med at strømme til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="14332-156">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
