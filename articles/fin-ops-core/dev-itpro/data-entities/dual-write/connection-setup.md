---
title: Vejledning i opsætning af dobbeltskrivning
description: I dette emne beskrives de scenarier, der understøttes til installation med to skrivninger.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 78a7cdc18476a1c523c83c92ca6f354c3ba806dc
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744847"
---
# <a name="guidance-for-dual-write-setup"></a><span data-ttu-id="940b9-103">Vejledning i opsætning af dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="940b9-103">Guidance for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="940b9-104">Du kan oprette en forbindelse med to skrivninger mellem et Finance and Operations-miljø og et Dataverse-miljø.</span><span class="sxs-lookup"><span data-stu-id="940b9-104">You can set up a dual-write connection between a Finance and Operations environment and a Dataverse environment.</span></span>

+ <span data-ttu-id="940b9-105">Et **Finance and Operations-miljø** leverer den underliggende platform for **Finance and Operations-apps** (f.eks Microsoft Dynamics 365 Finance. Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="940b9-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="940b9-106">Et **Dataverse-miljø** giver den underliggende platform for **modelbaserede apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="940b9-106">A **Dataverse environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="940b9-107">Modulet Human Resources i Dynamics 365 Finance understøtter dobbeltskrivningsforbindelser, men Dynamics 365 Human Resources-appen gør ikke.</span><span class="sxs-lookup"><span data-stu-id="940b9-107">The Human Resources module in Dynamics 365 Finance supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="940b9-108">Konfigurationsmekanismen varierer, afhængigt af dit abonnement og miljøet:</span><span class="sxs-lookup"><span data-stu-id="940b9-108">The setup mechanism varies, depending on your subscription and the environment:</span></span>

+ <span data-ttu-id="940b9-109">Ved nye forekomster af Finance and Operations-apps begynder opsætningen af en forbindelse med to skrivninger i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="940b9-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="940b9-110">Hvis du har en licens til Microsoft Power Platform, vil du få et nyt Dataverse-miljø, hvis din lejer ikke har en.</span><span class="sxs-lookup"><span data-stu-id="940b9-110">If you have a license for Microsoft Power Platform, you will get a new Dataverse environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="940b9-111">For eksisterende forekomster af Finance and Operations-apps begynder opsætningen af en forbindelse med to skrivninger i Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="940b9-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="940b9-112">Før du starter dobbeltskrivning på en enhed, kan du køre en indledende synkronisering for at håndtere eksisterende data på begge sider: Finance and Operations-apps og kundeengagementapps.</span><span class="sxs-lookup"><span data-stu-id="940b9-112">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="940b9-113">Du kan springe den første synkronisering over, hvis du ikke har brug for at synkronisere data mellem de to miljøer.</span><span class="sxs-lookup"><span data-stu-id="940b9-113">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="940b9-114">Ved hjælp af en første synkronisering kan du kopiere eksisterende data fra én app til en anden tovejs.</span><span class="sxs-lookup"><span data-stu-id="940b9-114">An initial synchronization lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="940b9-115">Der er flere forskellige opsætningsscenarier, afhængigt af hvilke miljøer du allerede har, og hvilken type data der er i dem.</span><span class="sxs-lookup"><span data-stu-id="940b9-115">There are several setup scenarios, depending on the environments that you already have and the type of data in them.</span></span>

<span data-ttu-id="940b9-116">Følgende konfigurationsscenarier understøttes:</span><span class="sxs-lookup"><span data-stu-id="940b9-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="940b9-117">En ny Finance and Operations-app-forekomst og en ny forekomst af en kundeengagementapp</span><span class="sxs-lookup"><span data-stu-id="940b9-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="940b9-118">En ny Finance and Operations-app-forekomst og en eksisterende forekomst af en kundeengagementapp</span><span class="sxs-lookup"><span data-stu-id="940b9-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="940b9-119">En ny Finance and Operations-app-forekomst, som har data, og en ny forekomst af kundeengagementapp</span><span class="sxs-lookup"><span data-stu-id="940b9-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="940b9-120">En ny Finance and Operations-app-forekomst, som har data, og en eksisterende forekomst af kundeengagementapp</span><span class="sxs-lookup"><span data-stu-id="940b9-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="940b9-121">En eksisterende Finance and Operations-app-forekomst og en ny forekomst af en kundeengagementapp</span><span class="sxs-lookup"><span data-stu-id="940b9-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="940b9-122">En eksisterende Finance and Operations-app-forekomst og en eksisterende forekomst af en kundeengagementapp</span><span class="sxs-lookup"><span data-stu-id="940b9-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="940b9-123">En ny Finance and Operations-app-forekomst og en ny forekomst af en kundeengagementapp</span><span class="sxs-lookup"><span data-stu-id="940b9-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="940b9-124">Hvis du vil oprette en forbindelse med dobbeltskrivning mellem en ny forekomst af en Finance and Operations-app, der ikke har data, og en ny forekomst af en kundeengagementapp, skal du følge trinnene i [Konfiguration af dobbeltskrivning fra Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="940b9-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="940b9-125">Når opsætningen af forbindelsen er fuldført, sker følgende handlinger automatisk:</span><span class="sxs-lookup"><span data-stu-id="940b9-125">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="940b9-126">Der klargøres et nyt tomt Finance and Operations-miljø.</span><span class="sxs-lookup"><span data-stu-id="940b9-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="940b9-127">Der klargøres en ny tom forekomst af en kundeengagementapp, hvor den primære CRM-løsning er installeret.</span><span class="sxs-lookup"><span data-stu-id="940b9-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="940b9-128">Der oprettes en forbindelse med to skrivninger for DAT-virksomhedsdata.</span><span class="sxs-lookup"><span data-stu-id="940b9-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="940b9-129">Tabeltilknytninger er aktiveret til direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="940b9-129">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="940b9-130">Begge miljøer er derefter klar til dynamisk datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="940b9-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="940b9-131">En ny Finance and Operations-app-forekomst og en eksisterende forekomst af en kundeengagementapp</span><span class="sxs-lookup"><span data-stu-id="940b9-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="940b9-132">Hvis du vil oprette en forbindelse med dobbeltskrivning mellem en ny forekomst af en Finance and Operations-app, der ikke har data, og en eksisterende forekomst af en kundeengagementapp, skal du følge trinnene i [Konfiguration af dobbeltskrivning fra Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="940b9-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="940b9-133">Når opsætningen af forbindelsen er fuldført, sker følgende handlinger automatisk:</span><span class="sxs-lookup"><span data-stu-id="940b9-133">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="940b9-134">Der klargøres et nyt tomt Finance and Operations-miljø.</span><span class="sxs-lookup"><span data-stu-id="940b9-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="940b9-135">Der oprettes en forbindelse med to skrivninger for DAT-virksomhedsdata.</span><span class="sxs-lookup"><span data-stu-id="940b9-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="940b9-136">Tabeltilknytninger er aktiveret til direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="940b9-136">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="940b9-137">Begge miljøer er derefter klar til dynamisk datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="940b9-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="940b9-138">Udfør følgende trin for at synkronisere Dataverse-data til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="940b9-138">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="940b9-139">Opret et nyt regnskab i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="940b9-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="940b9-140">Føj firmaet til opsætningen af forbindelsen med to skrivninger.</span><span class="sxs-lookup"><span data-stu-id="940b9-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="940b9-141">[Bootstrap](bootstrap-company-data.md) Dataverse-dataene ved hjælp af en ISO-virksomhedskode (International Organization for Standardization) på tre bogstaver.</span><span class="sxs-lookup"><span data-stu-id="940b9-141">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="940b9-142">Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="940b9-142">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="940b9-143">Du kan finde links til et eksempel og en alternativ fremgangsmåde i afsnittet [Eksempel](#example) senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="940b9-143">For links to an example and an alternative approach, see the [Example](#example) section later in this topic.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="940b9-144">En ny Finance and Operations-app-forekomst, som har data, og en ny forekomst af kundeengagementapp</span><span class="sxs-lookup"><span data-stu-id="940b9-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="940b9-145">Hvis du vil oprette en forbindelse med dobbeltskrivning mellem en ny forekomst af en Finance and Operations-app, der har data, og en ny forekomst af en kundeengagementapp, skal du følge trinnene i afsnittet [En ny Finance and Operations-app-forekomst og en ny forekomst af kundeengagementapp](#new-new) tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="940b9-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="940b9-146">Når opsætningen af forbindelsen er fuldført, skal du udføre følgende trin, hvis du vil synkronisere dataene til kundeengagementappen.</span><span class="sxs-lookup"><span data-stu-id="940b9-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="940b9-147">Åbn Finance and Operations-appen fra siden LCS, log på, og gå derefter til **Datastyring \> To skrivninger**.</span><span class="sxs-lookup"><span data-stu-id="940b9-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="940b9-148">Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="940b9-148">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="940b9-149">Du kan finde links til et eksempel og en alternativ fremgangsmåde i afsnittet [Eksempel](#example).</span><span class="sxs-lookup"><span data-stu-id="940b9-149">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="940b9-150">En ny Finance and Operations-app-forekomst, som har data, og en eksisterende forekomst af kundeengagementapp</span><span class="sxs-lookup"><span data-stu-id="940b9-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="940b9-151">Hvis du vil oprette en forbindelse med dobbeltskrivning mellem en ny forekomst af en Finance and Operations-app, der har data, og en eksisterende forekomst af en kundeengagementapp, skal du følge trinnene i afsnittet [En ny Finance and Operations-app-forekomst og en eksisterende forekomst af kundeengagementapp](#new-existing) tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="940b9-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="940b9-152">Når opsætningen af forbindelsen er fuldført, skal du udføre følgende trin, hvis du vil synkronisere dataene til kundeengagementappen.</span><span class="sxs-lookup"><span data-stu-id="940b9-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="940b9-153">Åbn Finance and Operations-appen fra siden LCS, log på, og gå derefter til **Datastyring \> To skrivninger**.</span><span class="sxs-lookup"><span data-stu-id="940b9-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="940b9-154">Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="940b9-154">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="940b9-155">Udfør følgende trin for at synkronisere Dataverse-data til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="940b9-155">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="940b9-156">Opret et nyt regnskab i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="940b9-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="940b9-157">Føj firmaet til opsætningen af forbindelsen med to skrivninger.</span><span class="sxs-lookup"><span data-stu-id="940b9-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="940b9-158">[Bootstrap](bootstrap-company-data.md) Dataverse-dataene ved hjælp af en ISO-virksomhedskode på tre bogstaver.</span><span class="sxs-lookup"><span data-stu-id="940b9-158">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="940b9-159">Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="940b9-159">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="940b9-160">Du kan finde links til et eksempel og en alternativ fremgangsmåde i afsnittet [Eksempel](#example).</span><span class="sxs-lookup"><span data-stu-id="940b9-160">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="940b9-161">En eksisterende Finance and Operations-app-forekomst og en ny forekomst af en kundeengagementapp</span><span class="sxs-lookup"><span data-stu-id="940b9-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="940b9-162">Opsætningen af en forbindelse med dobbeltskrivning mellem en eksisterende forekomst af en Finance and Operations-app og en ny forekomst af en kundeengagementapp forekommer i Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="940b9-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="940b9-163">[Konfigurer forbindelsen fra Finance and Operations-appen](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="940b9-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="940b9-164">Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="940b9-164">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="940b9-165">Du kan finde links til et eksempel og en alternativ fremgangsmåde i afsnittet [Eksempel](#example).</span><span class="sxs-lookup"><span data-stu-id="940b9-165">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="940b9-166">En eksisterende Finance and Operations-app-forekomst og en eksisterende forekomst af en kundeengagementapp</span><span class="sxs-lookup"><span data-stu-id="940b9-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="940b9-167">Opsætningen af en forbindelse med dobbeltskrivning mellem en eksisterende forekomst af en Finance and Operations-app og en eksisterende forekomst af en kundeengagementapp forekommer i Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="940b9-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="940b9-168">[Konfigurer forbindelsen fra Finance and Operations-appen](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="940b9-168">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="940b9-169">Hvis du vil synkronisere eksisterende Dataverse-data med Finance and Operations-appen, skal du udføre en [bootstrap](bootstrap-company-data.md) på Dataverse-dataene ved hjælp af en ISO-virksomhedskode på tre bogstaver.</span><span class="sxs-lookup"><span data-stu-id="940b9-169">To sync the existing Dataverse data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="940b9-170">Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="940b9-170">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="940b9-171">Du kan finde links til et eksempel og en alternativ fremgangsmåde i afsnittet [Eksempel](#example).</span><span class="sxs-lookup"><span data-stu-id="940b9-171">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="example"></a><span data-ttu-id="940b9-172">Eksempel</span><span class="sxs-lookup"><span data-stu-id="940b9-172">Example</span></span>

<span data-ttu-id="940b9-173">Du kan finde et eksempel under [Aktivering af Debitorer V3 – tabeltilknytningen Kontakter](enable-entity-map.md#enable-table-map)</span><span class="sxs-lookup"><span data-stu-id="940b9-173">For an example, see [Enabling the Customers V3—Contacts table map](enable-entity-map.md#enable-table-map)</span></span>

<span data-ttu-id="940b9-174">Du kan finde en alternativ fremgangsmåde, der er baseret på datamængder i de enkelte enheder, der skal køre den første synkronisering, under [Overvejelser ved første synkronisering](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="940b9-174">For an alternative approach that is based on data volumes in each entity that must run an initial synchronization, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
