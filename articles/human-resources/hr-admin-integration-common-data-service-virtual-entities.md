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
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959569"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="4a5c9-104">Konfigurere virtuelle enheder i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4a5c9-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="4a5c9-105">Dynamics 365 Human Resources er en virtuel datakilde i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="4a5c9-106">Den giver fuld adgang til at oprette, læse, opdatere og slette data fra Common Data Service og Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="4a5c9-107">Dataene for de virtuelle enheder gemmes ikke i Common Data Service, men i programdatabasen.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="4a5c9-108">Hvis du vil aktivere disse handlinger på Human Resources-enheder fra Common Data Service, skal du gøre enhederne tilgængelige som virtuelle enheder i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="4a5c9-109">På denne måde kan du udføre disse handlinger fra Common Data Service og Microsoft Power Platform på data i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="4a5c9-110">Handlingerne understøtter også fulde valideringer af forretningslogik i Human Resources for at sikre dataintegritet, når der skrives data til enhederne.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="4a5c9-111">Tilgængelige virtuelle enheder for Human Resources</span><span class="sxs-lookup"><span data-stu-id="4a5c9-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="4a5c9-112">Alle OData-enheder (Open data Protocol) under Human Resources er tilgængelige som virtuelle enheder i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="4a5c9-113">De er også tilgængelige i Power Platform.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-113">They're also available in Power Platform.</span></span> <span data-ttu-id="4a5c9-114">Nu kan du opbygge apps og oplevelser med data direkte fra Human Resources med fulde handlingsmuligheder uden at kopiere eller synkronisere data til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="4a5c9-115">Du kan bruge Power Apps-portaler til at opbygge eksterne websteder, der giver mulighed for samarbejdsscenarier til forretningsprocesser i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="4a5c9-116">Du kan få vist listen over de virtuelle enheder, der er aktiveret i miljøet, og starte med at arbejde med enhederne i [Power Apps](https://make.powerapps.com), i løsningen **Dynamics 365 HR Virtual Entities**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Dynamics 365 HR Virtual Entities i Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="4a5c9-118">Virtuelle enheder i forhold til fysiske enheder</span><span class="sxs-lookup"><span data-stu-id="4a5c9-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="4a5c9-119">Virtuelle enheder til Human Resources er ikke de samme som de fysiske Common Data Service-enheder, der er oprettet for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="4a5c9-120">De fysiske enheder for Human Resources genereres separat og vedligeholdes i HCM Common-løsningen i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="4a5c9-121">Med fysiske enheder gemmes dataene i Common Data Service og kræver synkronisering med programdatabasen til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="4a5c9-122">Du kan se en liste over de fysiske Common Data Service-enheder for Human Resources i [Common Data Service-enheder](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="4a5c9-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="4a5c9-123">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="4a5c9-123">Setup</span></span>

<span data-ttu-id="4a5c9-124">Følg disse installationstrin for at aktivere virtuelle enheder i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="4a5c9-125">Registrere appen i Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="4a5c9-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="4a5c9-126">Først skal du registrere appen i Azure-portalen, så Microsoft-identitetsplatformen kan levere godkendelse og autorisationstjenester til appen og brugerne.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="4a5c9-127">Du kan finde flere oplysninger om registrering af apps i Azure under [Hurtig start: Registrere et program med platformen Microsoft-identitet](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="4a5c9-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="4a5c9-128">Åbn [Microsoft Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="4a5c9-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="4a5c9-129">Vælg **Appregistreringer** på listen Azure-tjenester.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="4a5c9-130">Vælg **Ny registrering**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-130">Select **New registration**.</span></span>

4. <span data-ttu-id="4a5c9-131">Angiv et sigende navn for appen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="4a5c9-132">F.eks. **Dynamics 365 Human Resources-virtuelle enheder**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="4a5c9-133">Angiv URL-adressen til navneområdet for din forekomst af Human Resources i feltet **Omdirigerings-URI**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="4a5c9-134">Vælg **Registrer**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-134">Select **Register**.</span></span>

7. <span data-ttu-id="4a5c9-135">Når registreringen er fuldført, viser Azure-portalen appregistreringens **Oversigt**-rude, som indeholder **Program-id (klient)**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="4a5c9-136">Notér dig **Program-id (klient)** nu.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="4a5c9-137">Du skal angive disse oplysninger, når du [konfigurerer datakilden til den virtuelle enhed](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="4a5c9-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="4a5c9-138">Vælg **Certifikater og hemmeligheder** i venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="4a5c9-139">Vælg **Ny klienthemmelighed** i afsnittet **Klienthemmeligheder** på siden.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="4a5c9-140">Indtast en beskrivelse, vælg en varighed, og vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="4a5c9-141">Registrere værdien af hemmeligheden.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-141">Record the secret's value.</span></span> <span data-ttu-id="4a5c9-142">Du skal angive disse oplysninger, når du [konfigurerer datakilden til den virtuelle enhed](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="4a5c9-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="4a5c9-143">Husk at notere dig hemmelighedens værdi på dette tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="4a5c9-144">Hemmeligheden vises aldrig igen, når du forlader denne side.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="4a5c9-145">Installere appen Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="4a5c9-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="4a5c9-146">Installer appen Dynamics 365 HR Virtual Entity i dit Power Apps-miljø for at udrulle den virtuelle enhedsløsningspakke til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="4a5c9-147">Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="4a5c9-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="4a5c9-148">Vælg det Power Apps-miljø, der er knyttet til din forekomst af Human Resources, på listen over **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="4a5c9-149">Vælg **Dynamics 365-apps** i sektionen **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="4a5c9-150">Vælg handlingen **Installer app**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="4a5c9-151">Vælg **Dynamics 365 HR Virtual Entity**, og vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-151">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="4a5c9-152">Gennemgå og markér, at du accepterer servicebetingelserne.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="4a5c9-153">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-153">Select **Install**.</span></span>

<span data-ttu-id="4a5c9-154">Installationen tager et par minutter.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-154">The install takes a few minutes.</span></span> <span data-ttu-id="4a5c9-155">Når den er fuldført, skal du fortsætte til de næste trin.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-155">When it completes, continue to the next steps.</span></span>

![Installer appen Dynamics 365 HR Virtual Entity fra Power Platform Administration](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="4a5c9-157">Konfigurere datakilden til den virtuelle enhed</span><span class="sxs-lookup"><span data-stu-id="4a5c9-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="4a5c9-158">Det næste trin er at konfigurere datakilden til den virtuelle enhed i Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="4a5c9-159">Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="4a5c9-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="4a5c9-160">Vælg det Power Apps-miljø, der er knyttet til din forekomst af Human Resources, på listen over **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="4a5c9-161">Vælg **URL-adressen til miljøet** i afsnittet **Detaljer** på siden.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="4a5c9-162">I **Løsningstilstandshub** skal du vælge ikonet **Avanceret søgning** øverst til højre på programsiden.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-162">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="4a5c9-163">Vælg **Finance and Operations-konfigurationer af virtuel datakilde** r på rullelisten **Søg efter** på siden **Avanceret søgning**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="4a5c9-164">Vælg **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-164">Select **Results**.</span></span>

7. <span data-ttu-id="4a5c9-165">Vælg posten **Microsoft HR-datakilde**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="4a5c9-166">Angiv de nødvendige oplysninger til datakildens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="4a5c9-167">**Mål-URL-adresse** URL-adressen til dit Human Resources-navneområde.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-167">**Target URL**: The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="4a5c9-168">**Lejer-id**: Azure Active Directory-lejer-id (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="4a5c9-168">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="4a5c9-169">**AAD-program-id**: Det program-id (klient), der er oprettet for det program, der er registreret i Microsoft Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-169">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="4a5c9-170">Du har modtaget disse oplysninger tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="4a5c9-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="4a5c9-171">**AAD-programhemmelighed**: Den programklienthemmelighed, der er oprettet for det program, der er registreret i Microsoft Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-171">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="4a5c9-172">Du har modtaget disse oplysninger tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="4a5c9-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="4a5c9-173">Vælg **Gem og luk**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-173">Select **Save & Close**.</span></span>

   ![Microsoft HR-datakilde](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="4a5c9-175">Give app-tilladelser i Human Resources</span><span class="sxs-lookup"><span data-stu-id="4a5c9-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="4a5c9-176">Give tilladelser til de to Azure AD-programmer i Human Resources:</span><span class="sxs-lookup"><span data-stu-id="4a5c9-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="4a5c9-177">Appen, der er oprettet til din lejer i Microsoft Azure-portalen</span><span class="sxs-lookup"><span data-stu-id="4a5c9-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="4a5c9-178">Appen Dynamics 365 HR Virtual Entity, der er installeret i Power Apps-miljøet</span><span class="sxs-lookup"><span data-stu-id="4a5c9-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="4a5c9-179">I Human Resources skal du åbne siden **Azure Active Directory-programmer**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="4a5c9-180">Vælg **Ny** for at oprette en ny programpost:</span><span class="sxs-lookup"><span data-stu-id="4a5c9-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="4a5c9-181">Angiv klient-id'et for den app, du har registreret i Microsoft Azure-portalen, i feltet **Klient-id**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="4a5c9-182">Angiv navnet på den app, du har registreret i Microsoft Azure-portalen, i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="4a5c9-183">I feltet **Bruger-id** skal du vælge bruger-id'et for en bruger med administratorrettigheder i Human Resources og Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="4a5c9-184">Vælg **Ny** for at oprette endnu en programpost:</span><span class="sxs-lookup"><span data-stu-id="4a5c9-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="4a5c9-185">**Klient-id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="4a5c9-185">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="4a5c9-186">**Navn**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="4a5c9-186">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="4a5c9-187">I feltet **Bruger-id** skal du vælge bruger-id'et for en bruger med administratorrettigheder i Human Resources og Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="4a5c9-188">Generere virtuelle enheder</span><span class="sxs-lookup"><span data-stu-id="4a5c9-188">Generate virtual entities</span></span>

<span data-ttu-id="4a5c9-189">Når installationen er fuldført, kan du vælge de virtuelle enheder, du vil generere og aktivere i din Common Data Service-forekomst.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="4a5c9-190">Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="4a5c9-190">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="4a5c9-191">Vælg det Power Apps-miljø, der er knyttet til din forekomst af Human Resources, på listen over **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-191">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="4a5c9-192">Vælg **URL-adressen til miljøet** i afsnittet **Detaljer** på siden.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-192">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="4a5c9-193">I **Løsningstilstandshub** skal du vælge ikonet **Avanceret søgning** øverst til højre på siden.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-193">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the page.</span></span>

5. <span data-ttu-id="4a5c9-194">Vælg **Tilgængelige HR-enheder** på rullelisten **Søg efter** på siden **Avanceret søgning**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-194">On the **Advanced Find** page, in the **Look for** dropdown list, select **Available HR Entities**.</span></span>

6. <span data-ttu-id="4a5c9-195">Brug filterindstillingerne til at finde det eller de enheder, du vil aktivere.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-195">Use the filter options to find the entity or entities you want to enable.</span></span>

7. <span data-ttu-id="4a5c9-196">Vælg en enhed på listen.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-196">Select an entity from the list.</span></span>

8. <span data-ttu-id="4a5c9-197">På enhedssiden skal du ændre egenskaben **Er genereret** til **Ja** for objektet.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-197">On the entity page, change the **Has Been Generated** property to **Yes** for the entity.</span></span>

9. <span data-ttu-id="4a5c9-198">Gem og luk enhedssiden.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-198">Save and close the entity page.</span></span>

> [!NOTE]
> <span data-ttu-id="4a5c9-199">Du kan oprette flere virtuelle enheder på én gang ved at bruge siden **Rediger flere poster**.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-199">You can generate multiple virtual entities at once by using the **Change Multiple Records** page.</span></span> <span data-ttu-id="4a5c9-200">Vælg flere poster på siden, og vælg **Rediger** på båndet.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-200">Select multiple records on the page, and select **Edit** on the ribbon.</span></span> <span data-ttu-id="4a5c9-201">Du kan derefter ændre egenskaben **Er genereret** for alle valgte poster.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-201">You can then change the **Has Been Generated** property for all selected records.</span></span>

![Tilgængelige HR-enheder](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> <span data-ttu-id="4a5c9-203">For at strømline processen til generering af virtuelle enheder i fremtidige versioner vil processen finde sted på en side i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4a5c9-203">To streamline the process of generating virtual entities in future releases, the process will occur in a page in Human Resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a5c9-204">Se også</span><span class="sxs-lookup"><span data-stu-id="4a5c9-204">See also</span></span>

[<span data-ttu-id="4a5c9-205">Hvad er Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="4a5c9-205">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="4a5c9-206">Oversigt over enheder</span><span class="sxs-lookup"><span data-stu-id="4a5c9-206">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="4a5c9-207">Oversigt over enhedsrelationer</span><span class="sxs-lookup"><span data-stu-id="4a5c9-207">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="4a5c9-208">Oprette og redigere virtuelle enheder, der indeholder data fra en ekstern datakilde</span><span class="sxs-lookup"><span data-stu-id="4a5c9-208">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="4a5c9-209">Hvad er Power Apps-portaler?</span><span class="sxs-lookup"><span data-stu-id="4a5c9-209">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="4a5c9-210">Oversigt over oprettelse af apps i Power Apps</span><span class="sxs-lookup"><span data-stu-id="4a5c9-210">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
