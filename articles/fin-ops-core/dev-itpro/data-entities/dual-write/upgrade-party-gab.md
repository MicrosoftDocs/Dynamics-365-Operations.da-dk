---
title: Opgradere til modellen med part- og globalt adressekartotek
description: Dette emne indeholder en beskrivelse af, hvordan du opgraderer dobbeltskrivningsdata til modellen med part- og globalt adressekartotek.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112667"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="6a7b0-103">Opgradere til modellen med part- og globalt adressekartotek</span><span class="sxs-lookup"><span data-stu-id="6a7b0-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6a7b0-104">[Microsoft Azure Data Factory-skabelonen](https://aka.ms/dual-write-gab-adf) hjælper dig med at opgradere eksisterende tabeldata for **Konto**, **Kontakt** og **Leverandør** i dobbeltskrivning til part- og det globale adressekartoteks model.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="6a7b0-105">Skabelonen afstemmer dataene fra både Finance and Operations-apps og programmer til kundeengagement.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="6a7b0-106">I slutningen af processen oprettes der **Part**- og **Kontakt**-felter for **Part**-poster, som knyttes til posterne **Konto**, **Kontakt** og **Leverandør** i kundeengagementsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="6a7b0-107">Der genereres en .csv-fil (`FONewParty.csv`) for at oprette nye **Part**-poster i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="6a7b0-108">Dette emne indeholder instruktioner i, hvordan du bruger Data Factory-skabelonen og opgraderer dine data.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="6a7b0-109">Hvis du ikke har tilpasninger, kan du bruge skabelonen, som den er.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="6a7b0-110">Hvis du har tilpasninger af **Konto**, **Kontakt** og **Leverandør**, skal du redigere skabelonen ved hjælp af følgende vejledning.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="6a7b0-111">Skabelonen opgraderer kun **Part**-dataene.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="6a7b0-112">I en fremtidig version inkluderes post- og elektroniske adresser.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6a7b0-113">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="6a7b0-113">Prerequisites</span></span>

<span data-ttu-id="6a7b0-114">Der kræves følgende forudsætninger for at opgradere til partmodellen og modellen for det globale adressekartotek:</span><span class="sxs-lookup"><span data-stu-id="6a7b0-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="6a7b0-115">Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="6a7b0-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="6a7b0-116">Adgang til skabelonen</span><span class="sxs-lookup"><span data-stu-id="6a7b0-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="6a7b0-117">Du skal være eksisterende dobbeltskrivningskunde.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="6a7b0-118">Forberede opgraderingen</span><span class="sxs-lookup"><span data-stu-id="6a7b0-118">Prepare for the upgrade</span></span>
<span data-ttu-id="6a7b0-119">Følgende aktiviteter er nødvendige for at forberede opgraderingen:</span><span class="sxs-lookup"><span data-stu-id="6a7b0-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="6a7b0-120">**Fuldt synkroniseret**: Begge miljøer er synkroniseret fuldstændigt for **Konto (kunde)**, **Kontakt** og **Leverandør**.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="6a7b0-121">**Integrationsnøgler**: **Konto (kunde)**, **Kontakt** og **Leverandør** tabeller i kundeengagementapps bruger de integrationsnøgler, der leveres som standard.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="6a7b0-122">Hvis du har tilpasset integrationsnøglerne, skal du tilpasse skabelonen.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="6a7b0-123">**Partnummer**: Alle **Konto (kunde)**, **Kontakt** og **Leverandør** poster, der skal opgraderes, har et **Part**-nummer.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="6a7b0-124">Poster uden et **Part**-nummer ignoreres.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="6a7b0-125">Hvis du vil opgradere disse poster, skal du føje et **Part**-nummer til dem, før du starter opgraderingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="6a7b0-126">**Systemnedlukning**: Under opgraderingsprocessen skal både Finance and Operations-miljøet og kundeengagementsmiljøet være offline.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="6a7b0-127">**Øjebliksbillede**: Tag øjebliksbilleder af både Finance and Operations-apps og kundeengagementapps.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="6a7b0-128">Du kan bruge øjebliksbillederne til at gendanne den forrige tilstand, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="6a7b0-129">Installation</span><span class="sxs-lookup"><span data-stu-id="6a7b0-129">Deployment</span></span>

1. <span data-ttu-id="6a7b0-130">Hent skabelonen fra [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="6a7b0-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="6a7b0-131">Log på [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="6a7b0-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="6a7b0-132">Opret en [ressourcegruppe](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="6a7b0-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="6a7b0-133">Opret en [lagerkonto](/azure/storage/common/storage-account-create?tabs=azure-portal) i den ressourcegruppe, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="6a7b0-134">Opret en [datafabrik](/azure/data-factory/quickstart-create-data-factory-portal) i den ressourcegruppe, du har oprettet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="6a7b0-135">Åbn datafabrikken, og vælg feltet **Forfatter og overvåger**.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="6a7b0-136">Vælg **ARM-skabelon** under fanen **Administrer**.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="6a7b0-137">Vælg **Importér ARM-skabelon** for at importere **Part**-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="6a7b0-138">Importér skabelonen til datafabrikken.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-138">Import the template into the data factory.</span></span> <span data-ttu-id="6a7b0-139">Angiv følgende værdier for **Projektdetaljer** og **Forekomstdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="6a7b0-140">Felt</span><span class="sxs-lookup"><span data-stu-id="6a7b0-140">Field</span></span> | <span data-ttu-id="6a7b0-141">Værdi</span><span class="sxs-lookup"><span data-stu-id="6a7b0-141">Value</span></span>
    ---|---
    <span data-ttu-id="6a7b0-142">Abonnement</span><span class="sxs-lookup"><span data-stu-id="6a7b0-142">Subscription</span></span> | <span data-ttu-id="6a7b0-143">Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="6a7b0-143">Azure subscription</span></span>
    <span data-ttu-id="6a7b0-144">Ressourcegruppe</span><span class="sxs-lookup"><span data-stu-id="6a7b0-144">Resource group</span></span> | <span data-ttu-id="6a7b0-145">Angiv den samme ressource, som lagerkontoen oprettes under.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="6a7b0-146">Land/område</span><span class="sxs-lookup"><span data-stu-id="6a7b0-146">Region</span></span> | <span data-ttu-id="6a7b0-147">Angiv område.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-147">Specify region.</span></span>
    <span data-ttu-id="6a7b0-148">Navn på fabrik</span><span class="sxs-lookup"><span data-stu-id="6a7b0-148">Factory Name</span></span> | <span data-ttu-id="6a7b0-149">Angiv fabriksnavnet.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-149">Specify factory name.</span></span>
    <span data-ttu-id="6a7b0-150">Hovednøgle til sammenkædet service</span><span class="sxs-lookup"><span data-stu-id="6a7b0-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="6a7b0-151">Angiv programnøglen.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-151">Specify the application's key.</span></span>
    <span data-ttu-id="6a7b0-152">Forbindelsesstreng til Azure Blob Storage</span><span class="sxs-lookup"><span data-stu-id="6a7b0-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="6a7b0-153">Forbindelsesstrengen til Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="6a7b0-154">Dynamics CRM-sammenkædet serviceadgangskode</span><span class="sxs-lookup"><span data-stu-id="6a7b0-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="6a7b0-155">Adgangskoden for den brugerkonto, du har angivet som brugernavn.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="6a7b0-156">FO-sammenkædet Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="6a7b0-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="6a7b0-157">FO-sammenkædet Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="6a7b0-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="6a7b0-158">Angiv de lejeroplysninger (domænenavn eller lejer-id), hvor dit program er placeret.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="6a7b0-159">FO-sammenkædet Service_properties_type Properties_aad ressource-id</span><span class="sxs-lookup"><span data-stu-id="6a7b0-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="6a7b0-160">FO-sammenkædet Service_properties_type Properties_service hoved-id</span><span class="sxs-lookup"><span data-stu-id="6a7b0-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="6a7b0-161">Angiv programmets klient-id.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="6a7b0-162">Dynamics CRM-sammenkædet Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="6a7b0-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="6a7b0-163">Det brugernavn, der skal forbindes med Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="6a7b0-164">Yderligere oplysninger finder du i følgende emner:</span><span class="sxs-lookup"><span data-stu-id="6a7b0-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="6a7b0-165">Opgradere en Resource Manager-skabelon manuelt for hvert miljø</span><span class="sxs-lookup"><span data-stu-id="6a7b0-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="6a7b0-166">Egenskaber for sammenkædet tjeneste</span><span class="sxs-lookup"><span data-stu-id="6a7b0-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="6a7b0-167">Kopiere data ved hjælp af Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="6a7b0-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="6a7b0-168">Efter installationen skal du validere datasæt, dataflow og tilknyttet tjeneste for datafabrikken.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Datasæt, dataflow og tilknyttet tjeneste](media/data-factory-validate.png)

11. <span data-ttu-id="6a7b0-170">Naviger til **Administrer**.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-170">Navigate to **Manage**.</span></span> <span data-ttu-id="6a7b0-171">Vælg **Sammenkædet tjeneste** under **Forbindelser**.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="6a7b0-172">Vælg **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="6a7b0-173">Angiv følgende værdier i formularen **Rediger sammenkædet tjeneste (Dynamics CRM)**.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="6a7b0-174">Felt</span><span class="sxs-lookup"><span data-stu-id="6a7b0-174">Field</span></span> | <span data-ttu-id="6a7b0-175">Værdi</span><span class="sxs-lookup"><span data-stu-id="6a7b0-175">Value</span></span>
    ---|---
    <span data-ttu-id="6a7b0-176">Navn</span><span class="sxs-lookup"><span data-stu-id="6a7b0-176">Name</span></span> | <span data-ttu-id="6a7b0-177">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="6a7b0-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="6a7b0-178">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="6a7b0-178">Description</span></span> | <span data-ttu-id="6a7b0-179">Sammenkædede tjenester, der bruges til at oprette forbindelse til CRM-forekomst for at hente data til enheder</span><span class="sxs-lookup"><span data-stu-id="6a7b0-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="6a7b0-180">Oprette forbindelse via integrationskørsel</span><span class="sxs-lookup"><span data-stu-id="6a7b0-180">Connect via integration runtime</span></span> | <span data-ttu-id="6a7b0-181">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6a7b0-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="6a7b0-182">Installationstype</span><span class="sxs-lookup"><span data-stu-id="6a7b0-182">Deployment type</span></span> | <span data-ttu-id="6a7b0-183">Online</span><span class="sxs-lookup"><span data-stu-id="6a7b0-183">Online</span></span>
    <span data-ttu-id="6a7b0-184">Tjeneste-URI</span><span class="sxs-lookup"><span data-stu-id="6a7b0-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="6a7b0-185">Godkendelsestype</span><span class="sxs-lookup"><span data-stu-id="6a7b0-185">Authentication type</span></span> | <span data-ttu-id="6a7b0-186">Office365</span><span class="sxs-lookup"><span data-stu-id="6a7b0-186">Office365</span></span>
    <span data-ttu-id="6a7b0-187">Brugernavn</span><span class="sxs-lookup"><span data-stu-id="6a7b0-187">User name</span></span> |
    <span data-ttu-id="6a7b0-188">Adgangskode eller Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="6a7b0-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="6a7b0-189">Adgangskode</span><span class="sxs-lookup"><span data-stu-id="6a7b0-189">Password</span></span>
    <span data-ttu-id="6a7b0-190">Adgangskode</span><span class="sxs-lookup"><span data-stu-id="6a7b0-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="6a7b0-191">Køre skabelonen</span><span class="sxs-lookup"><span data-stu-id="6a7b0-191">Run the template</span></span>

1. <span data-ttu-id="6a7b0-192">Stop følgende dobbeltskrivningstilknytninger af **Konto**, **Kontakt** og **Leverandør** ved hjælp af appen Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="6a7b0-193">Debitorer V3 (konti)</span><span class="sxs-lookup"><span data-stu-id="6a7b0-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="6a7b0-194">Debitorer V3 (kontakter)</span><span class="sxs-lookup"><span data-stu-id="6a7b0-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="6a7b0-195">CDS-kontakter V2 (kontakter)</span><span class="sxs-lookup"><span data-stu-id="6a7b0-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="6a7b0-196">CDS-kontakter V2 (kontakter)</span><span class="sxs-lookup"><span data-stu-id="6a7b0-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="6a7b0-197">Kreditor V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="6a7b0-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="6a7b0-198">Kontrollér, at tilknytningerne er fjernet fra `msdy_dualwriteruntimeconfig`-tabellen i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="6a7b0-199">Installer [Løsninger til part og globalt adressekartotek for dobbeltskrivning](https://aka.ms/dual-write-gab) fra AppSource.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="6a7b0-200">Hvis følgende tabeller indeholder data i Finance and Operations-appen, skal du køre **Første synkronisering** for dem.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="6a7b0-201">Tiltaleformer</span><span class="sxs-lookup"><span data-stu-id="6a7b0-201">Salutations</span></span>
    + <span data-ttu-id="6a7b0-202">Personlige tegntyper</span><span class="sxs-lookup"><span data-stu-id="6a7b0-202">Personal character types</span></span>
    + <span data-ttu-id="6a7b0-203">Afsluttende hilsner</span><span class="sxs-lookup"><span data-stu-id="6a7b0-203">Complimentary closing</span></span>
    + <span data-ttu-id="6a7b0-204">Titler på kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="6a7b0-204">Contact person titles</span></span>
    + <span data-ttu-id="6a7b0-205">Beslutningstagerrolle</span><span class="sxs-lookup"><span data-stu-id="6a7b0-205">Decision making roles</span></span>
    + <span data-ttu-id="6a7b0-206">Loyalitetsniveauer</span><span class="sxs-lookup"><span data-stu-id="6a7b0-206">Loyalty levels</span></span>

5. <span data-ttu-id="6a7b0-207">Deaktiver følgende plugin-trin i kundeengagementsappen.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="6a7b0-208">Kontoopdatering</span><span class="sxs-lookup"><span data-stu-id="6a7b0-208">Account Update</span></span>
         + <span data-ttu-id="6a7b0-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Opdatering af konto</span><span class="sxs-lookup"><span data-stu-id="6a7b0-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="6a7b0-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Opdatering af konto</span><span class="sxs-lookup"><span data-stu-id="6a7b0-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="6a7b0-211">Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="6a7b0-211">Contact Update</span></span>
         + <span data-ttu-id="6a7b0-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="6a7b0-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="6a7b0-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="6a7b0-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="6a7b0-214">Opdatering af msdyn_party</span><span class="sxs-lookup"><span data-stu-id="6a7b0-214">msdyn_party Update</span></span>
         + <span data-ttu-id="6a7b0-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Opdatering af msdyn_party</span><span class="sxs-lookup"><span data-stu-id="6a7b0-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="6a7b0-216">Opdatering af msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="6a7b0-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="6a7b0-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Opdatering af msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="6a7b0-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="6a7b0-218">Deaktiver følgende arbejdsflows i kundeengagementsappen:</span><span class="sxs-lookup"><span data-stu-id="6a7b0-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="6a7b0-219">Opret kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="6a7b0-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="6a7b0-220">Opret kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="6a7b0-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="6a7b0-221">Opret kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="6a7b0-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="6a7b0-222">Opret kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="6a7b0-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="6a7b0-223">Opdater kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="6a7b0-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="6a7b0-224">Opdater kreditorer i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="6a7b0-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="6a7b0-225">Opdater kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="6a7b0-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="6a7b0-226">Opdater kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="6a7b0-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="6a7b0-227">På datafabrikken skal du køre skabelonen ved at vælge **Udløs nu** som vist på følgende billede.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="6a7b0-228">Det kan tage et par timer, før denne proces er fuldført, afhængigt af datavolumen.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![Udløserkørsel](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="6a7b0-230">Hvis du har tilpasninger af **Konto**, **Kontakt** og **Leverandør**, skal du redigere skabelonen.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="6a7b0-231">Importér de nye **Part**-poster i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="6a7b0-232">Download filen `FONewParty.csv` fra Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="6a7b0-233">Stien er `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="6a7b0-234">Konverter `FONewParty.csv`-filen til en Excel-fil, og importér Excel-filen til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="6a7b0-235">Hvis csv-importen fungerer for dig, kan du importere csv-filen direkte.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="6a7b0-236">Det kan tage et par timer at importere, afhængigt af datavolumen.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="6a7b0-237">Du kan finde flere oplysninger i [Oversigt over dataimport og eksportjob](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="6a7b0-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Importere Dataverse-partposterne](media/data-factory-import-party.png)

9. <span data-ttu-id="6a7b0-239">Aktivér følgende plugin-trin i kundeengagementsapps:</span><span class="sxs-lookup"><span data-stu-id="6a7b0-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="6a7b0-240">Kontoopdatering</span><span class="sxs-lookup"><span data-stu-id="6a7b0-240">Account Update</span></span>
         + <span data-ttu-id="6a7b0-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Opdatering af konto</span><span class="sxs-lookup"><span data-stu-id="6a7b0-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="6a7b0-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Opdatering af konto</span><span class="sxs-lookup"><span data-stu-id="6a7b0-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="6a7b0-243">Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="6a7b0-243">Contact Update</span></span>
         + <span data-ttu-id="6a7b0-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="6a7b0-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="6a7b0-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="6a7b0-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="6a7b0-246">Opdatering af msdyn_party</span><span class="sxs-lookup"><span data-stu-id="6a7b0-246">msdyn_party Update</span></span>
         + <span data-ttu-id="6a7b0-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Opdatering af msdyn_party</span><span class="sxs-lookup"><span data-stu-id="6a7b0-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="6a7b0-248">Opdatering af msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="6a7b0-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="6a7b0-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Opdatering af msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="6a7b0-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="6a7b0-250">I apps til kundeengagement skal du aktivere følgende arbejdsgange, hvis du deaktiverede dem i forrige trin:</span><span class="sxs-lookup"><span data-stu-id="6a7b0-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="6a7b0-251">Opret kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="6a7b0-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="6a7b0-252">Opret kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="6a7b0-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="6a7b0-253">Opret kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="6a7b0-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="6a7b0-254">Opret kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="6a7b0-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="6a7b0-255">Opdater kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="6a7b0-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="6a7b0-256">Opdater kreditorer i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="6a7b0-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="6a7b0-257">Opdater kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="6a7b0-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="6a7b0-258">Opdater kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="6a7b0-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="6a7b0-259">Kør de **Part**-relaterede kort som beskrevet i [Part- og globalt adressekartotek](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="6a7b0-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="6a7b0-260">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="6a7b0-260">Troubleshooting</span></span>

1. <span data-ttu-id="6a7b0-261">Hvis processen mislykkes, skal du køre datafabrikken igen med start fra den mislykkede aktivitet.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="6a7b0-262">Nogle filer genereres af datafabrikken, som du kan bruge til datavalideringsformål.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="6a7b0-263">Datafabrikken kører på basis af csv-filer, der er kommaseparerede.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="6a7b0-264">Hvis der er en feltværdi med komma, kan den forstyrre resultaterne.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="6a7b0-265">Du skal fjerne kommaerne.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="6a7b0-266">Fanen **Overvågning** indeholder oplysninger om alle trin og data, der er behandlet.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="6a7b0-267">Vælg et bestemt trin for at fejlfinde det.</span><span class="sxs-lookup"><span data-stu-id="6a7b0-267">Select a specific step to debug it.</span></span>

    ![Fanen Overvågning](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="6a7b0-269">Få mere at vide om skabelonen</span><span class="sxs-lookup"><span data-stu-id="6a7b0-269">Learn more about the template</span></span>

<span data-ttu-id="6a7b0-270">Du kan finde flere oplysninger om skabelonen i [Kommentarer til filen vigtige oplysninger til Azure Data Factory](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="6a7b0-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>
