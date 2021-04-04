---
title: Konfigurere virtuelle Dataverse-tabeller
description: I dette emne vises, hvordan du konfigurerer virtuelle tabeller til Dynamics 365 Human Resources. Opret og opdater eksisterende virtuelle tabeller, og analysér oprettede og tilgængelige tabeller.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: d8780be777c9a204fcb95950f5679a5711aee298
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465816"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="00963-104">Konfigurere virtuelle Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="00963-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="00963-105">Dynamics 365 Human Resources er en virtuel datakilde i Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="00963-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="00963-106">Den giver fuld adgang til at oprette, læse, opdatere og slette data fra Dataverse og Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="00963-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="00963-107">Dataene for de virtuelle tabeller gemmes ikke i Dataverse, men i programdatabasen.</span><span class="sxs-lookup"><span data-stu-id="00963-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="00963-108">Hvis du vil aktivere disse handlinger på Human Resources-enheder fra Dataverse, skal du gøre enhederne tilgængelige som virtuelle tabeller i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="00963-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="00963-109">På denne måde kan du udføre disse handlinger fra Dataverse og Microsoft Power Platform på data i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="00963-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="00963-110">Handlingerne understøtter også fulde valideringer af forretningslogik i Human Resources for at sikre dataintegritet, når der skrives data til enhederne.</span><span class="sxs-lookup"><span data-stu-id="00963-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="00963-111">Enheder under Human Resources svarer til Dataverse-tabeller.</span><span class="sxs-lookup"><span data-stu-id="00963-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="00963-112">Yderligere oplysninger om Dataverse (tidligere Common Data Service) og terminologiopdateringer finder du i [Hvad er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="00963-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="00963-113">Tilgængelige virtuelle tabeller for Human Resources</span><span class="sxs-lookup"><span data-stu-id="00963-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="00963-114">Alle OData-enheder (Open data Protocol) under Human Resources er tilgængelige som virtuelle tabeller i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="00963-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="00963-115">De er også tilgængelige i Power Platform.</span><span class="sxs-lookup"><span data-stu-id="00963-115">They're also available in Power Platform.</span></span> <span data-ttu-id="00963-116">Nu kan du opbygge apps og oplevelser med data direkte fra Human Resources med fulde handlingsmuligheder uden at kopiere eller synkronisere data til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="00963-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="00963-117">Du kan bruge Power Apps-portaler til at opbygge eksterne websteder, der giver mulighed for samarbejdsscenarier til forretningsprocesser i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="00963-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="00963-118">Du kan få vist listen over de virtuelle tabeller, der er aktiveret i miljøet, og starte med at arbejde med tabellerne i [Power Apps](https://make.powerapps.com), i løsningen **Dynamics 365 HR Virtual Tables**.</span><span class="sxs-lookup"><span data-stu-id="00963-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Dynamics 365 HR Virtual Tables i Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="00963-120">Virtuelle tabeller vs. oprindelige tabeller</span><span class="sxs-lookup"><span data-stu-id="00963-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="00963-121">Virtuelle tabeller til Human Resources er ikke de samme som de oprindelige Dataverse-tabeller, der er oprettet til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="00963-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="00963-122">De oprindelige tabeller til Human Resources genereres separat og vedligeholdes i HCM Common-løsningen i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="00963-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="00963-123">Med de oprindelige tabeller gemmes dataene i Dataverse og kræver synkronisering med programdatabasen til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="00963-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="00963-124">Du kan se en liste over de oprindelige Dataverse-tabeller til Human Resources i [Dataverse-tabeller](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="00963-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="00963-125">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="00963-125">Setup</span></span>

<span data-ttu-id="00963-126">Følg disse installationstrin for at aktivere virtuelle tabeller i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="00963-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="00963-127">Aktivere virtuelle tabeller i Human Resources</span><span class="sxs-lookup"><span data-stu-id="00963-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="00963-128">Først skal du aktivere virtuelle tabeller i arbejdsområdet **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="00963-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="00963-129">I Human Resources skal du vælge **Systemadministration**.</span><span class="sxs-lookup"><span data-stu-id="00963-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="00963-130">Vælg felter **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="00963-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="00963-131">Vælg **Virtuel tabelunderstøttelse til HR i Dataverse**, og vælg derefter **Aktivere**.</span><span class="sxs-lookup"><span data-stu-id="00963-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="00963-132">Du kan finde flere oplysninger om aktivering og deaktivering af funktioner i [Administrere funktioner](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="00963-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="00963-133">Registrere appen i Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="00963-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="00963-134">Du skal registrere dine forekomst af Human Resources i Azure-portalen, så Microsoft-identitetsplatformen kan levere godkendelse og autorisationstjenester til appen og brugerne.</span><span class="sxs-lookup"><span data-stu-id="00963-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="00963-135">Du kan finde flere oplysninger om registrering af apps i Azure under [Hurtig start: Registrere et program med platformen Microsoft-identitet](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="00963-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="00963-136">Åbn [Microsoft Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="00963-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="00963-137">Vælg **Appregistreringer** på listen Azure-tjenester.</span><span class="sxs-lookup"><span data-stu-id="00963-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="00963-138">Vælg **Ny registrering**.</span><span class="sxs-lookup"><span data-stu-id="00963-138">Select **New registration**.</span></span>

4. <span data-ttu-id="00963-139">Angiv et sigende navn for appen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="00963-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="00963-140">F.eks. **Dynamics 365 Human Resources-virtuelle tabeller**.</span><span class="sxs-lookup"><span data-stu-id="00963-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="00963-141">Angiv URL-adressen til navneområdet for din forekomst af Human Resources i feltet **Omdirigerings-URI**.</span><span class="sxs-lookup"><span data-stu-id="00963-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="00963-142">Vælg **Registrer**.</span><span class="sxs-lookup"><span data-stu-id="00963-142">Select **Register**.</span></span>

7. <span data-ttu-id="00963-143">Når registreringen er fuldført, viser Azure-portalen appregistreringens **Oversigt**-rude, som indeholder **Program-id (klient)**.</span><span class="sxs-lookup"><span data-stu-id="00963-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="00963-144">Notér dig **Program-id (klient)** nu.</span><span class="sxs-lookup"><span data-stu-id="00963-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="00963-145">Du skal angive disse oplysninger, når du vil [Konfigurere datakilden til den virtuelle tabel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="00963-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="00963-146">Vælg **Certifikater og hemmeligheder** i venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="00963-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="00963-147">Vælg **Ny klienthemmelighed** i afsnittet **Klienthemmeligheder** på siden.</span><span class="sxs-lookup"><span data-stu-id="00963-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="00963-148">Indtast en beskrivelse, vælg en varighed, og vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="00963-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="00963-149">Registrere værdien af hemmeligheden.</span><span class="sxs-lookup"><span data-stu-id="00963-149">Record the secret's value.</span></span> <span data-ttu-id="00963-150">Du skal angive disse oplysninger, når du vil [Konfigurere datakilden til den virtuelle tabel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="00963-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="00963-151">Husk at notere dig hemmelighedens værdi på dette tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="00963-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="00963-152">Hemmeligheden vises aldrig igen, når du forlader denne side.</span><span class="sxs-lookup"><span data-stu-id="00963-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="00963-153">Installere appen Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="00963-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="00963-154">Installer appen Dynamics 365 HR Virtual Table i dit Power Apps-miljø for at udrulle den virtuelle tabelløsningspakke til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="00963-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="00963-155">Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="00963-155">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="00963-156">Vælg det Power Apps-miljø, der er knyttet til din forekomst af Human Resources, på listen over **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="00963-156">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="00963-157">Vælg **Dynamics 365-apps** i sektionen **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="00963-157">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="00963-158">Vælg handlingen **Installer app**.</span><span class="sxs-lookup"><span data-stu-id="00963-158">Select the **Install app** action.</span></span>

5. <span data-ttu-id="00963-159">Vælg **Dynamics 365 HR Virtual Table**, og vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="00963-159">Select **Dynamics 365 HR Virtual Table**, and select **Next**.</span></span>

6. <span data-ttu-id="00963-160">Gennemgå og markér, at du accepterer servicebetingelserne.</span><span class="sxs-lookup"><span data-stu-id="00963-160">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="00963-161">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="00963-161">Select **Install**.</span></span>

<span data-ttu-id="00963-162">Installationen tager et par minutter.</span><span class="sxs-lookup"><span data-stu-id="00963-162">The install takes a few minutes.</span></span> <span data-ttu-id="00963-163">Når den er fuldført, skal du fortsætte til de næste trin.</span><span class="sxs-lookup"><span data-stu-id="00963-163">When it completes, continue to the next steps.</span></span>

![Installer appen Dynamics 365 HR Virtual Table fra Power Platform Administration](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="00963-165">Konfigurere datakilden til den virtuelle tabel</span><span class="sxs-lookup"><span data-stu-id="00963-165">Configure the virtual table data source</span></span> 

<span data-ttu-id="00963-166">Det næste trin er at konfigurere datakilden til den virtuelle tabel i Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="00963-166">The next step is to configure the virtual table data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="00963-167">Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="00963-167">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="00963-168">Vælg det Power Apps-miljø, der er knyttet til din forekomst af Human Resources, på listen over **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="00963-168">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="00963-169">Vælg **URL-adressen til miljøet** i afsnittet **Detaljer** på siden.</span><span class="sxs-lookup"><span data-stu-id="00963-169">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="00963-170">I **Løsningstilstandshub** skal du vælge ikonet **Avanceret søgning** øverst til højre på programsiden.</span><span class="sxs-lookup"><span data-stu-id="00963-170">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="00963-171">Vælg **Finance and Operations-konfigurationer af virtuel datakilde** r på rullelisten **Søg efter** på siden **Avanceret søgning**.</span><span class="sxs-lookup"><span data-stu-id="00963-171">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="00963-172">Vælg **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="00963-172">Select **Results**.</span></span>

7. <span data-ttu-id="00963-173">Vælg posten **Microsoft HR-datakilde**.</span><span class="sxs-lookup"><span data-stu-id="00963-173">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="00963-174">Angiv de nødvendige oplysninger til datakildens konfiguration:</span><span class="sxs-lookup"><span data-stu-id="00963-174">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="00963-175">**Mål-URL-adresse** URL-adressen til dit Human Resources-navneområde.</span><span class="sxs-lookup"><span data-stu-id="00963-175">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="00963-176">Formatet for mål-URL-adressen er:</span><span class="sxs-lookup"><span data-stu-id="00963-176">The format of the target URL is:</span></span>
     
     <span data-ttu-id="00963-177">https://\<hostname\>.hr.talent.dynamics.com/navneområder/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="00963-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="00963-178">F.eks.:</span><span class="sxs-lookup"><span data-stu-id="00963-178">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="00963-179">Husk at medtage "**/**"-tegnet i slutningen af URL-adressen for at undgå at modtage en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="00963-179">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="00963-180">**Lejer-id**: Azure Active Directory-lejer-id (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="00963-180">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="00963-181">**AAD-program-id**: Det program-id (klient), der er oprettet for det program, der er registreret i Microsoft Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="00963-181">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="00963-182">Du har modtaget disse oplysninger tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="00963-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="00963-183">**AAD-programhemmelighed**: Den programklienthemmelighed, der er oprettet for det program, der er registreret i Microsoft Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="00963-183">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="00963-184">Du har modtaget disse oplysninger tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="00963-184">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR-datakilde](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="00963-186">Vælg **Gem og luk**.</span><span class="sxs-lookup"><span data-stu-id="00963-186">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="00963-187">Give app-tilladelser i Human Resources</span><span class="sxs-lookup"><span data-stu-id="00963-187">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="00963-188">Give tilladelser til de to Azure AD-programmer i Human Resources:</span><span class="sxs-lookup"><span data-stu-id="00963-188">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="00963-189">Appen, der er oprettet til din lejer i Microsoft Azure-portalen</span><span class="sxs-lookup"><span data-stu-id="00963-189">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="00963-190">Appen Dynamics 365 HR Virtual Table, der er installeret i Power Apps-miljøet</span><span class="sxs-lookup"><span data-stu-id="00963-190">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="00963-191">I Human Resources skal du åbne siden **Azure Active Directory-programmer**.</span><span class="sxs-lookup"><span data-stu-id="00963-191">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="00963-192">Vælg **Ny** for at oprette en ny programpost:</span><span class="sxs-lookup"><span data-stu-id="00963-192">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="00963-193">Angiv klient-id'et for den app, du har registreret i Microsoft Azure-portalen, i feltet **Klient-id**.</span><span class="sxs-lookup"><span data-stu-id="00963-193">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="00963-194">Angiv navnet på den app, du har registreret i Microsoft Azure-portalen, i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="00963-194">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="00963-195">I feltet **Bruger-id** skal du vælge bruger-id'et for en bruger med administratorrettigheder i Human Resources og Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="00963-195">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="00963-196">Vælg **Ny** for at oprette endnu en programpost:</span><span class="sxs-lookup"><span data-stu-id="00963-196">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="00963-197">**Klient-id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="00963-197">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="00963-198">**Navn**: Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="00963-198">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="00963-199">I feltet **Bruger-id** skal du vælge bruger-id'et for en bruger med administratorrettigheder i Human Resources og Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="00963-199">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="00963-200">Generere virtuelle tabeller</span><span class="sxs-lookup"><span data-stu-id="00963-200">Generate virtual tables</span></span>

<span data-ttu-id="00963-201">Når installationen er fuldført, kan du vælge de virtuelle tabeller, du vil generere og aktivere i din Dataverse-forekomst.</span><span class="sxs-lookup"><span data-stu-id="00963-201">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="00963-202">I Human Resources skal du åbne siden **Dataverse-integration**.</span><span class="sxs-lookup"><span data-stu-id="00963-202">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="00963-203">Vælg fanen **Virtuelle tabeller**.</span><span class="sxs-lookup"><span data-stu-id="00963-203">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="00963-204">Til/fra-knappen **Aktivér den virtuelle tabel** indstilles til **Ja** automatisk, når alle nødvendige konfigurationer er fuldført.</span><span class="sxs-lookup"><span data-stu-id="00963-204">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="00963-205">Hvis knappen er indstillet til **Nej**, skal du gennemgå trinnene i tidligere afsnit af dette dokument for at sikre, at alle forudsætninger for installationen er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="00963-205">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="00963-206">Vælg den tabel eller de tabeller, du vil oprette i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="00963-206">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="00963-207">Vælg **Generer/Opdater**.</span><span class="sxs-lookup"><span data-stu-id="00963-207">Select **Generate/refresh**.</span></span>

![Dataverse-integration](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-table-generation-status"></a><span data-ttu-id="00963-209">Kontrollere status for oprettelse af tabel</span><span class="sxs-lookup"><span data-stu-id="00963-209">Check table generation status</span></span>

<span data-ttu-id="00963-210">Virtuelle tabeller genereres i Dataverse via en asynkron baggrundsproces.</span><span class="sxs-lookup"><span data-stu-id="00963-210">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="00963-211">Opdateringer af processen vises i handlingscenteret.</span><span class="sxs-lookup"><span data-stu-id="00963-211">Updates on the process display in the action center.</span></span> <span data-ttu-id="00963-212">Oplysninger om processen, herunder fejllogfiler, vises på siden **Procesautomatiseringer**.</span><span class="sxs-lookup"><span data-stu-id="00963-212">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="00963-213">Åbn listesiden **Procesautomatiseringer** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="00963-213">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="00963-214">Vælg fanen **Baggrundsprocesser**.</span><span class="sxs-lookup"><span data-stu-id="00963-214">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="00963-215">Vælg **Baggrundsproces i asynkron handling for virtuel tabelforespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="00963-215">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="00963-216">Vælg **Vis seneste resultater**.</span><span class="sxs-lookup"><span data-stu-id="00963-216">Select **View most recent results**.</span></span>

<span data-ttu-id="00963-217">I slide-out-ruden vises de seneste udførelsesresultater for processen.</span><span class="sxs-lookup"><span data-stu-id="00963-217">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="00963-218">Du kan se logfilen for processen, herunder eventuelle fejl, der returneres fra Dataverse.</span><span class="sxs-lookup"><span data-stu-id="00963-218">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="00963-219">Se også</span><span class="sxs-lookup"><span data-stu-id="00963-219">See also</span></span>

[<span data-ttu-id="00963-220">Hvad er Dataverse?</span><span class="sxs-lookup"><span data-stu-id="00963-220">What is Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="00963-221">Tabeller i Dataverse</span><span class="sxs-lookup"><span data-stu-id="00963-221">Tables in Dataverse</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="00963-222">Oversigt over tabelrelationer</span><span class="sxs-lookup"><span data-stu-id="00963-222">Table relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="00963-223">Oprette og redigere virtuelle tabeller, der indeholder data fra en ekstern datakilde</span><span class="sxs-lookup"><span data-stu-id="00963-223">Create and edit virtual tables that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="00963-224">Hvad er Power Apps-portaler?</span><span class="sxs-lookup"><span data-stu-id="00963-224">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="00963-225">Oversigt over oprettelse af apps i Power Apps</span><span class="sxs-lookup"><span data-stu-id="00963-225">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]