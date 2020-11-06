---
title: Konfigurere virtuelle enheder i Common Data Service
description: I dette emne vises, hvordan du konfigurerer virtuelle enheder til Dynamics 365 Human Resources. Opret og opdater eksisterende virtuelle enheder, og analysér oprettede og tilgængelige enheder.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0d6f79ea569a7a9b0d25e73e8666bf9ba19095d0
ms.sourcegitcommit: a8665c47696028d371cdc4671db1fd8fcf9e1088
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/21/2020
ms.locfileid: "4058148"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="b7447-104">Konfigurere virtuelle enheder i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="b7447-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="b7447-105">Dynamics 365 Human Resources er en virtuel datakilde i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b7447-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="b7447-106">Den giver fuld adgang til at oprette, læse, opdatere og slette data fra Common Data Service og Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="b7447-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="b7447-107">Dataene for de virtuelle enheder gemmes ikke i Common Data Service, men i programdatabasen.</span><span class="sxs-lookup"><span data-stu-id="b7447-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="b7447-108">Hvis du vil aktivere disse handlinger på Human Resources-enheder fra Common Data Service, skal du gøre enhederne tilgængelige som virtuelle enheder i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b7447-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="b7447-109">På denne måde kan du udføre disse handlinger fra Common Data Service og Microsoft Power Platform på data i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b7447-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="b7447-110">Handlingerne understøtter også fulde valideringer af forretningslogik i Human Resources for at sikre dataintegritet, når der skrives data til enhederne.</span><span class="sxs-lookup"><span data-stu-id="b7447-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="b7447-111">Tilgængelige virtuelle enheder for Human Resources</span><span class="sxs-lookup"><span data-stu-id="b7447-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="b7447-112">Alle OData-enheder (Open data Protocol) under Human Resources er tilgængelige som virtuelle enheder i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b7447-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="b7447-113">De er også tilgængelige i Power Platform.</span><span class="sxs-lookup"><span data-stu-id="b7447-113">They're also available in Power Platform.</span></span> <span data-ttu-id="b7447-114">Nu kan du opbygge apps og oplevelser med data direkte fra Human Resources med fulde handlingsmuligheder uden at kopiere eller synkronisere data til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b7447-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="b7447-115">Du kan bruge Power Apps-portaler til at opbygge eksterne websteder, der giver mulighed for samarbejdsscenarier til forretningsprocesser i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b7447-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="b7447-116">Du kan få vist listen over de virtuelle enheder, der er aktiveret i miljøet, og starte med at arbejde med enhederne i [Power Apps](https://make.powerapps.com), i løsningen **Dynamics 365 HR Virtual Entities**.</span><span class="sxs-lookup"><span data-stu-id="b7447-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Dynamics 365 HR Virtual Entities i Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="b7447-118">Virtuelle enheder i forhold til fysiske enheder</span><span class="sxs-lookup"><span data-stu-id="b7447-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="b7447-119">Virtuelle enheder til Human Resources er ikke de samme som de fysiske Common Data Service-enheder, der er oprettet for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b7447-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="b7447-120">De fysiske enheder for Human Resources genereres separat og vedligeholdes i HCM Common-løsningen i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b7447-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="b7447-121">Med fysiske enheder gemmes dataene i Common Data Service og kræver synkronisering med programdatabasen til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b7447-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="b7447-122">Du kan se en liste over de fysiske Common Data Service-enheder for Human Resources i [Common Data Service-enheder](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="b7447-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="b7447-123">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="b7447-123">Setup</span></span>

<span data-ttu-id="b7447-124">Følg disse installationstrin for at aktivere virtuelle enheder i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="b7447-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="b7447-125">Registrere appen i Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="b7447-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="b7447-126">Først skal du registrere appen i Azure-portalen, så Microsoft-identitetsplatformen kan levere godkendelse og autorisationstjenester til appen og brugerne.</span><span class="sxs-lookup"><span data-stu-id="b7447-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="b7447-127">Du kan finde flere oplysninger om registrering af apps i Azure under [Hurtig start: Registrere et program med platformen Microsoft-identitet](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="b7447-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="b7447-128">Åbn [Microsoft Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="b7447-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="b7447-129">Vælg **Appregistreringer** på listen Azure-tjenester.</span><span class="sxs-lookup"><span data-stu-id="b7447-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="b7447-130">Vælg **Ny registrering**.</span><span class="sxs-lookup"><span data-stu-id="b7447-130">Select **New registration**.</span></span>

4. <span data-ttu-id="b7447-131">Angiv et sigende navn for appen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="b7447-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="b7447-132">F.eks. **Dynamics 365 Human Resources-virtuelle enheder**.</span><span class="sxs-lookup"><span data-stu-id="b7447-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="b7447-133">Angiv URL-adressen til navneområdet for din forekomst af Human Resources i feltet **Omdirigerings-URI**.</span><span class="sxs-lookup"><span data-stu-id="b7447-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="b7447-134">Vælg **Registrer**.</span><span class="sxs-lookup"><span data-stu-id="b7447-134">Select **Register**.</span></span>

7. <span data-ttu-id="b7447-135">Når registreringen er fuldført, viser Azure-portalen appregistreringens **Oversigt** -rude, som indeholder **Program-id (klient)**.</span><span class="sxs-lookup"><span data-stu-id="b7447-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="b7447-136">Notér dig **Program-id (klient)** nu.</span><span class="sxs-lookup"><span data-stu-id="b7447-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="b7447-137">Du skal angive disse oplysninger, når du [konfigurerer datakilden til den virtuelle enhed](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="b7447-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="b7447-138">Vælg **Certifikater og hemmeligheder** i venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="b7447-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="b7447-139">Vælg **Ny klienthemmelighed** i afsnittet **Klienthemmeligheder** på siden.</span><span class="sxs-lookup"><span data-stu-id="b7447-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="b7447-140">Indtast en beskrivelse, vælg en varighed, og vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="b7447-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="b7447-141">Registrere værdien af hemmeligheden.</span><span class="sxs-lookup"><span data-stu-id="b7447-141">Record the secret's value.</span></span> <span data-ttu-id="b7447-142">Du skal angive disse oplysninger, når du [konfigurerer datakilden til den virtuelle enhed](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="b7447-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b7447-143">Husk at notere dig hemmelighedens værdi på dette tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="b7447-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="b7447-144">Hemmeligheden vises aldrig igen, når du forlader denne side.</span><span class="sxs-lookup"><span data-stu-id="b7447-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="b7447-145">Installere appen Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="b7447-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="b7447-146">Installer appen Dynamics 365 HR Virtual Entity i dit Power Apps-miljø for at udrulle den virtuelle enhedsløsningspakke til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b7447-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="b7447-147">Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="b7447-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="b7447-148">Vælg det Power Apps-miljø, der er knyttet til din forekomst af Human Resources, på listen over **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="b7447-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="b7447-149">Vælg **Dynamics 365-apps** i sektionen **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="b7447-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="b7447-150">Vælg handlingen **Installer app**.</span><span class="sxs-lookup"><span data-stu-id="b7447-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="b7447-151">Vælg **Dynamics 365 HR Virtual Entity** , og vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="b7447-151">Select **Dynamics 365 HR Virtual Entity** , and select **Next**.</span></span>

6. <span data-ttu-id="b7447-152">Gennemgå og markér, at du accepterer servicebetingelserne.</span><span class="sxs-lookup"><span data-stu-id="b7447-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="b7447-153">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="b7447-153">Select **Install**.</span></span>

<span data-ttu-id="b7447-154">Installationen tager et par minutter.</span><span class="sxs-lookup"><span data-stu-id="b7447-154">The install takes a few minutes.</span></span> <span data-ttu-id="b7447-155">Når den er fuldført, skal du fortsætte til de næste trin.</span><span class="sxs-lookup"><span data-stu-id="b7447-155">When it completes, continue to the next steps.</span></span>

![Installer appen Dynamics 365 HR Virtual Entity fra Power Platform Administration](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="b7447-157">Konfigurere datakilden til den virtuelle enhed</span><span class="sxs-lookup"><span data-stu-id="b7447-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="b7447-158">Det næste trin er at konfigurere datakilden til den virtuelle enhed i Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="b7447-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="b7447-159">Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="b7447-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="b7447-160">Vælg det Power Apps-miljø, der er knyttet til din forekomst af Human Resources, på listen over **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="b7447-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="b7447-161">Vælg **URL-adressen til miljøet** i afsnittet **Detaljer** på siden.</span><span class="sxs-lookup"><span data-stu-id="b7447-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="b7447-162">I **Løsningstilstandshub** skal du vælge ikonet **Avanceret søgning** øverst til højre på programsiden.</span><span class="sxs-lookup"><span data-stu-id="b7447-162">In the **Solution Health Hub** , select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="b7447-163">Vælg **Finance and Operations-konfigurationer af virtuel datakilde** r på rullelisten **Søg efter** på siden **Avanceret søgning**.</span><span class="sxs-lookup"><span data-stu-id="b7447-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="b7447-164">Vælg **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="b7447-164">Select **Results**.</span></span>

7. <span data-ttu-id="b7447-165">Vælg posten **Microsoft HR-datakilde**.</span><span class="sxs-lookup"><span data-stu-id="b7447-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="b7447-166">Angiv de nødvendige oplysninger til datakildens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b7447-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="b7447-167">**Mål-URL-adresse** URL-adressen til dit Human Resources-navneområde.</span><span class="sxs-lookup"><span data-stu-id="b7447-167">**Target URL** : The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="b7447-168">**Lejer-id** : Azure Active Directory-lejer-id (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="b7447-168">**Tenant ID** : The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="b7447-169">**AAD-program-id** : Det program-id (klient), der er oprettet for det program, der er registreret i Microsoft Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="b7447-169">**AAD Application ID** : The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="b7447-170">Du har modtaget disse oplysninger tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="b7447-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="b7447-171">**AAD-programhemmelighed** : Den programklienthemmelighed, der er oprettet for det program, der er registreret i Microsoft Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="b7447-171">**AAD Application Secret** : The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="b7447-172">Du har modtaget disse oplysninger tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="b7447-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="b7447-173">Vælg **Gem og luk**.</span><span class="sxs-lookup"><span data-stu-id="b7447-173">Select **Save & Close**.</span></span>

   ![Microsoft HR-datakilde](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="b7447-175">Give app-tilladelser i Human Resources</span><span class="sxs-lookup"><span data-stu-id="b7447-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="b7447-176">Give tilladelser til de to Azure AD-programmer i Human Resources:</span><span class="sxs-lookup"><span data-stu-id="b7447-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="b7447-177">Appen, der er oprettet til din lejer i Microsoft Azure-portalen</span><span class="sxs-lookup"><span data-stu-id="b7447-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="b7447-178">Appen Dynamics 365 HR Virtual Entity, der er installeret i Power Apps-miljøet</span><span class="sxs-lookup"><span data-stu-id="b7447-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="b7447-179">I Human Resources skal du åbne siden **Azure Active Directory-programmer**.</span><span class="sxs-lookup"><span data-stu-id="b7447-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="b7447-180">Vælg **Ny** for at oprette en ny programpost:</span><span class="sxs-lookup"><span data-stu-id="b7447-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="b7447-181">Angiv klient-id'et for den app, du har registreret i Microsoft Azure-portalen, i feltet **Klient-id**.</span><span class="sxs-lookup"><span data-stu-id="b7447-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="b7447-182">Angiv navnet på den app, du har registreret i Microsoft Azure-portalen, i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="b7447-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="b7447-183">I feltet **Bruger-id** skal du vælge bruger-id'et for en bruger med administratorrettigheder i Human Resources og Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="b7447-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="b7447-184">Vælg **Ny** for at oprette endnu en programpost:</span><span class="sxs-lookup"><span data-stu-id="b7447-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="b7447-185">**Klient-id** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="b7447-185">**Client Id** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="b7447-186">**Navn** : Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="b7447-186">**Name** : Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="b7447-187">I feltet **Bruger-id** skal du vælge bruger-id'et for en bruger med administratorrettigheder i Human Resources og Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="b7447-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="b7447-188">Generere virtuelle enheder</span><span class="sxs-lookup"><span data-stu-id="b7447-188">Generate virtual entities</span></span>

<span data-ttu-id="b7447-189">Når installationen er fuldført, kan du vælge de virtuelle enheder, du vil generere og aktivere i din Common Data Service-forekomst.</span><span class="sxs-lookup"><span data-stu-id="b7447-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="b7447-190">I Human Resources skal du åbne siden **Common Data Service (CDS)-integration**.</span><span class="sxs-lookup"><span data-stu-id="b7447-190">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="b7447-191">Vælg fanen **Virtuelle enheder**.</span><span class="sxs-lookup"><span data-stu-id="b7447-191">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="b7447-192">Til/fra-knappen **Aktivér den virtuelle enhed** indstilles til **Ja** automatisk, når alle nødvendige konfigurationer er fuldført.</span><span class="sxs-lookup"><span data-stu-id="b7447-192">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="b7447-193">Hvis knappen er indstillet til **Nej** , skal du gennemgå trinnene i tidligere afsnit af dette dokument for at sikre, at alle forudsætninger for installationen er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="b7447-193">If the toggle is set to **No** , review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="b7447-194">Vælg den enhed eller de enheder, du vil oprette i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b7447-194">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="b7447-195">Vælg **Generer/Opdater**.</span><span class="sxs-lookup"><span data-stu-id="b7447-195">Select **Generate/refresh**.</span></span>

![Common Data Service-integration](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="b7447-197">Kontrollere status for oprettelse af enhed</span><span class="sxs-lookup"><span data-stu-id="b7447-197">Check entity generation status</span></span>

<span data-ttu-id="b7447-198">Virtuelle enheder genereres i Common Data Service via en asynkron baggrundsproces.</span><span class="sxs-lookup"><span data-stu-id="b7447-198">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="b7447-199">Opdateringer af processen vises i handlingscenteret.</span><span class="sxs-lookup"><span data-stu-id="b7447-199">Updates on the process display in the action center.</span></span> <span data-ttu-id="b7447-200">Oplysninger om processen, herunder fejllogfiler, vises på siden **Procesautomatiseringer**.</span><span class="sxs-lookup"><span data-stu-id="b7447-200">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="b7447-201">Åbn listesiden **Procesautomatiseringer** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b7447-201">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="b7447-202">Vælg fanen **Baggrundsprocesser**.</span><span class="sxs-lookup"><span data-stu-id="b7447-202">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="b7447-203">Vælg **Baggrundsproces i asynkron handling for virtuel enhedsforespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="b7447-203">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="b7447-204">Vælg **Vis seneste resultater**.</span><span class="sxs-lookup"><span data-stu-id="b7447-204">Select **View most recent results**.</span></span>

<span data-ttu-id="b7447-205">I slide-out-ruden vises de seneste udførelsesresultater for processen.</span><span class="sxs-lookup"><span data-stu-id="b7447-205">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="b7447-206">Du kan se logfilen for processen, herunder eventuelle fejl, der returneres fra Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b7447-206">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7447-207">Se også</span><span class="sxs-lookup"><span data-stu-id="b7447-207">See also</span></span>

[<span data-ttu-id="b7447-208">Hvad er Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="b7447-208">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="b7447-209">Oversigt over enheder</span><span class="sxs-lookup"><span data-stu-id="b7447-209">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="b7447-210">Oversigt over enhedsrelationer</span><span class="sxs-lookup"><span data-stu-id="b7447-210">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="b7447-211">Oprette og redigere virtuelle enheder, der indeholder data fra en ekstern datakilde</span><span class="sxs-lookup"><span data-stu-id="b7447-211">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="b7447-212">Hvad er Power Apps-portaler?</span><span class="sxs-lookup"><span data-stu-id="b7447-212">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="b7447-213">Oversigt over oprettelse af apps i Power Apps</span><span class="sxs-lookup"><span data-stu-id="b7447-213">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
