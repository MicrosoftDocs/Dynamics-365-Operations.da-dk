---
title: Opgradere til modellen med part- og globalt adressekartotek
description: Dette emne indeholder en beskrivelse af, hvordan du opgraderer dobbeltskrivningsdata til modellen med part- og globalt adressekartotek.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 76e64d483e833782733277a64d8dc37cbeba6130
ms.sourcegitcommit: 011468a6cffea8641bebc2922e0676d9f44b36fc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857364"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="1e6ac-103">Opgradere til modellen med part- og globalt adressekartotek</span><span class="sxs-lookup"><span data-stu-id="1e6ac-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1e6ac-104">[Azure Data Factory-skabelonen](https://aka.ms/dual-write-gab-adf) hjælper dig med at opgradere eksisterende tabeldata for **Konto**, **Kontakt** og **Leverandør** i dobbeltskrivning til part- og det globale adressekartoteks model.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="1e6ac-105">Skabelonen afstemmer dataene fra både Finance and Operations-apps og programmer til kundeengagement.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="1e6ac-106">I slutningen af processen oprettes der **Part**- og **Kontakt**-felter for **Part**-poster, som knyttes til posterne **Konto**, **Kontakt** og **Leverandør** i kundeengagementsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="1e6ac-107">Der genereres en .csv-fil (`FONewParty.csv`) for at oprette nye **Part**-poster i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="1e6ac-108">Dette emne indeholder instruktioner til brug af Data Factory-skabelonen og opgradering af dine data.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="1e6ac-109">Hvis du ikke har tilpasninger, kan du bruge skabelonen, som den er.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="1e6ac-110">Hvis du har tilpasninger af **Konto**, **Kontakt** og **Leverandør**, skal du redigere skabelonen ved hjælp af følgende vejledning.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="1e6ac-111">Skabelonen hjælper kun med at opgradere **Part**-dataene.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="1e6ac-112">I en fremtidig version inkluderes post- og elektroniske adresser.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1e6ac-113">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="1e6ac-113">Prerequisites</span></span>

<span data-ttu-id="1e6ac-114">Disse forudsætninger er obligatoriske:</span><span class="sxs-lookup"><span data-stu-id="1e6ac-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="1e6ac-115">Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="1e6ac-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="1e6ac-116">Adgang til skabelonen</span><span class="sxs-lookup"><span data-stu-id="1e6ac-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="1e6ac-117">Du er eksisterende dobbeltskrivningskunde.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="1e6ac-118">Forberede opgraderingen</span><span class="sxs-lookup"><span data-stu-id="1e6ac-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="1e6ac-119">**Fuldt synkroniseret**: Begge miljøer er synkroniseret fuldstændigt for **Konto (kunde)**, **Kontakt** og **Leverandør**.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="1e6ac-120">**Integrationsnøgler**: **Konto (kunde)**, **Kontakt** og **Leverandør** tabeller i kundeengagementapps bruger de integrationsnøgler, der leveres som standard.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="1e6ac-121">Hvis du har tilpasset integrationsnøglerne, skal du tilpasse skabelonen.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="1e6ac-122">**Partnummer**: Alle **Konto (kunde)**, **Kontakt** og **Leverandør** poster, der skal opgraderes, har et **Part**-nummer.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="1e6ac-123">Poster uden et **Part**-nummer ignoreres.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="1e6ac-124">Hvis du vil opgradere disse poster, skal du føje et **Part**-nummer til dem, før du starter opgraderingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="1e6ac-125">**Systemnedlukning**: Under opgraderingsprocessen skal både Finance and Operations og kundeengagementsmiljøer være offline.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="1e6ac-126">**Øjebliksbillede**: Tag øjebliksbilleder af både Finance and Operations og kundeengagementapps.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="1e6ac-127">Du kan bruge øjebliksbillederne til at gendanne den forrige tilstand, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="1e6ac-128">Installation</span><span class="sxs-lookup"><span data-stu-id="1e6ac-128">Deployment</span></span>

1. <span data-ttu-id="1e6ac-129">Hent skabelonen fra [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="1e6ac-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="1e6ac-130">Log på [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="1e6ac-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="1e6ac-131">Opret en [ressourcegruppe](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="1e6ac-131">Create a [resource group](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="1e6ac-132">Opret en [lagerkonto](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) i den ressourcegruppe, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-132">Create a [storage account](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="1e6ac-133">Opret en [datafabrik](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) i den ressourcegruppe, du har oprettet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-133">Create a [data factory](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="1e6ac-134">Åbn datafabrikken, og vælg feltet **Forfatter og overvåger**.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="1e6ac-135">Vælg **ARM-skabelon** under fanen **Administrer**.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="1e6ac-136">Vælg **Importér ARM-skabelon** for at importere **Part**-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="1e6ac-137">Importér skabelonen til datafabrikken.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-137">Import the template into the data factory.</span></span> <span data-ttu-id="1e6ac-138">Angiv følgende værdier for **Projektdetaljer** og **Forekomstdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="1e6ac-139">Felt</span><span class="sxs-lookup"><span data-stu-id="1e6ac-139">Field</span></span> | <span data-ttu-id="1e6ac-140">Værdi</span><span class="sxs-lookup"><span data-stu-id="1e6ac-140">Value</span></span>
    ---|---
    <span data-ttu-id="1e6ac-141">Abonnement</span><span class="sxs-lookup"><span data-stu-id="1e6ac-141">Subscription</span></span> | <span data-ttu-id="1e6ac-142">Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="1e6ac-142">Azure subscription</span></span>
    <span data-ttu-id="1e6ac-143">Ressourcegruppe</span><span class="sxs-lookup"><span data-stu-id="1e6ac-143">Resource group</span></span> | <span data-ttu-id="1e6ac-144">Angiv den samme ressource, som lagerkontoen oprettes under.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="1e6ac-145">Land/område</span><span class="sxs-lookup"><span data-stu-id="1e6ac-145">Region</span></span> | <span data-ttu-id="1e6ac-146">Angiv område.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-146">Specify region.</span></span>
    <span data-ttu-id="1e6ac-147">Navn på fabrik</span><span class="sxs-lookup"><span data-stu-id="1e6ac-147">Factory Name</span></span> | <span data-ttu-id="1e6ac-148">Angiv fabriksnavnet.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-148">Specify factory name.</span></span>
    <span data-ttu-id="1e6ac-149">Hovednøgle til sammenkædet service</span><span class="sxs-lookup"><span data-stu-id="1e6ac-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="1e6ac-150">Angiv programnøglen.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-150">Specify the application's key.</span></span>
    <span data-ttu-id="1e6ac-151">Forbindelsesstreng til Azure Blob Storage</span><span class="sxs-lookup"><span data-stu-id="1e6ac-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="1e6ac-152">Forbindelsesstrengen til Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="1e6ac-153">Dynamics CRM-sammenkædet serviceadgangskode</span><span class="sxs-lookup"><span data-stu-id="1e6ac-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="1e6ac-154">Adgangskoden for den brugerkonto, du har angivet som brugernavn.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="1e6ac-155">FO-sammenkædet Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="1e6ac-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="1e6ac-156">FO-sammenkædet Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="1e6ac-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="1e6ac-157">Angiv de lejeroplysninger (domænenavn eller lejer-id), hvor dit program er placeret.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="1e6ac-158">FO-sammenkædet Service_properties_type Properties_aad ressource-id</span><span class="sxs-lookup"><span data-stu-id="1e6ac-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="1e6ac-159">FO-sammenkædet Service_properties_type Properties_service hoved-id</span><span class="sxs-lookup"><span data-stu-id="1e6ac-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="1e6ac-160">Angiv programmets klient-id.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="1e6ac-161">Dynamics CRM-sammenkædet Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="1e6ac-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="1e6ac-162">Det brugernavn, der skal forbindes med Dynamics.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="1e6ac-163">Du kan finde flere oplysninger i [Manuelt promovere en Resource Manager-skabelon for hvert miljø](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Sammenkædede tjenesteegenskaber](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties) og [Kopiere data vha. Azure Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="1e6ac-163">For more information, see [Manually promote a Resource Manager template for each environment](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="1e6ac-164">Efter installationen skal du validere datasæt, dataflow og tilknyttet tjeneste for datafabrikken.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Datasæt, dataflow og tilknyttet tjeneste](media/data-factory-validate.png)

11. <span data-ttu-id="1e6ac-166">Naviger til **Administrer**.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-166">Navigate to **Manage**.</span></span> <span data-ttu-id="1e6ac-167">Vælg **Sammenkædet tjeneste** under **Forbindelser**.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="1e6ac-168">Vælg **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="1e6ac-169">Angiv følgende værdier i formularen **Rediger sammenkædet tjeneste (Dynamics CRM)**:</span><span class="sxs-lookup"><span data-stu-id="1e6ac-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="1e6ac-170">Felt</span><span class="sxs-lookup"><span data-stu-id="1e6ac-170">Field</span></span> | <span data-ttu-id="1e6ac-171">Værdi</span><span class="sxs-lookup"><span data-stu-id="1e6ac-171">Value</span></span>
    ---|---
    <span data-ttu-id="1e6ac-172">Navn</span><span class="sxs-lookup"><span data-stu-id="1e6ac-172">Name</span></span> | <span data-ttu-id="1e6ac-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="1e6ac-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="1e6ac-174">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="1e6ac-174">Description</span></span> | <span data-ttu-id="1e6ac-175">Sammenkædede tjenester, der bruges til at oprette forbindelse til CRM-forekomst for at hente data til enheder</span><span class="sxs-lookup"><span data-stu-id="1e6ac-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="1e6ac-176">Oprette forbindelse via integrationskørsel</span><span class="sxs-lookup"><span data-stu-id="1e6ac-176">Connect via integration runtime</span></span> | <span data-ttu-id="1e6ac-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1e6ac-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="1e6ac-178">Installationstype</span><span class="sxs-lookup"><span data-stu-id="1e6ac-178">Deployment type</span></span> | <span data-ttu-id="1e6ac-179">Online</span><span class="sxs-lookup"><span data-stu-id="1e6ac-179">Online</span></span>
    <span data-ttu-id="1e6ac-180">Tjeneste-URI</span><span class="sxs-lookup"><span data-stu-id="1e6ac-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="1e6ac-181">Godkendelsestype</span><span class="sxs-lookup"><span data-stu-id="1e6ac-181">Authentication type</span></span> | <span data-ttu-id="1e6ac-182">Office365</span><span class="sxs-lookup"><span data-stu-id="1e6ac-182">Office365</span></span>
    <span data-ttu-id="1e6ac-183">Brugernavn</span><span class="sxs-lookup"><span data-stu-id="1e6ac-183">User name</span></span> |
    <span data-ttu-id="1e6ac-184">Adgangskode eller Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="1e6ac-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="1e6ac-185">Adgangskode</span><span class="sxs-lookup"><span data-stu-id="1e6ac-185">Password</span></span>
    <span data-ttu-id="1e6ac-186">Adgangskode</span><span class="sxs-lookup"><span data-stu-id="1e6ac-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="1e6ac-187">Køre skabelonen</span><span class="sxs-lookup"><span data-stu-id="1e6ac-187">Run the template</span></span>

1. <span data-ttu-id="1e6ac-188">Stop følgende dobbeltskrivning af **Konto**, **Kontakt** og **Leverandør** ved hjælp af appen Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="1e6ac-189">Debitorer V3 (konti)</span><span class="sxs-lookup"><span data-stu-id="1e6ac-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="1e6ac-190">Debitorer V3 (kontakter)</span><span class="sxs-lookup"><span data-stu-id="1e6ac-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="1e6ac-191">CDS-kontakter V2 (kontakter)</span><span class="sxs-lookup"><span data-stu-id="1e6ac-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="1e6ac-192">CDS-kontakter V2 (kontakter)</span><span class="sxs-lookup"><span data-stu-id="1e6ac-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="1e6ac-193">Kreditor V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="1e6ac-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="1e6ac-194">Kontrollér, at tilknytningerne er fjernet fra `msdy_dualwriteruntimeconfig`-tabellen i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="1e6ac-195">Installer [Løsninger til part og globalt adressekartotek for dobbeltskrivning](https://aka.ms/dual-write-gab) fra AppSource.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="1e6ac-196">Hvis følgende tabeller indeholder data i appen Finance and Operations, skal du køre **Første synkronisering** for dem.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="1e6ac-197">Tiltaleformer</span><span class="sxs-lookup"><span data-stu-id="1e6ac-197">Salutations</span></span>
    + <span data-ttu-id="1e6ac-198">Personlige tegntyper</span><span class="sxs-lookup"><span data-stu-id="1e6ac-198">Personal character types</span></span>
    + <span data-ttu-id="1e6ac-199">Afsluttende hilsner</span><span class="sxs-lookup"><span data-stu-id="1e6ac-199">Complimentary closing</span></span>
    + <span data-ttu-id="1e6ac-200">Titler på kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="1e6ac-200">Contact person titles</span></span>
    + <span data-ttu-id="1e6ac-201">Beslutningstagerrolle</span><span class="sxs-lookup"><span data-stu-id="1e6ac-201">Decision making roles</span></span>
    + <span data-ttu-id="1e6ac-202">Loyalitetsniveauer</span><span class="sxs-lookup"><span data-stu-id="1e6ac-202">Loyalty levels</span></span>

5. <span data-ttu-id="1e6ac-203">Deaktiver følgende plugin-trin i kundeengagementsappen.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="1e6ac-204">Opdater konto</span><span class="sxs-lookup"><span data-stu-id="1e6ac-204">Account Update</span></span>
         + <span data-ttu-id="1e6ac-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Opdatering af konto</span><span class="sxs-lookup"><span data-stu-id="1e6ac-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="1e6ac-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Opdatering af konto</span><span class="sxs-lookup"><span data-stu-id="1e6ac-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="1e6ac-207">Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="1e6ac-207">Contact Update</span></span>
         + <span data-ttu-id="1e6ac-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="1e6ac-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="1e6ac-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="1e6ac-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="1e6ac-210">Opdatering af msdyn_party</span><span class="sxs-lookup"><span data-stu-id="1e6ac-210">msdyn_party Update</span></span>
         + <span data-ttu-id="1e6ac-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Opdatering af msdyn_party</span><span class="sxs-lookup"><span data-stu-id="1e6ac-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="1e6ac-212">Opdatering af msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="1e6ac-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="1e6ac-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Opdatering af msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="1e6ac-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="1e6ac-214">Deaktiver følgende arbejdsflows i kundeengagementsappen:</span><span class="sxs-lookup"><span data-stu-id="1e6ac-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="1e6ac-215">Opret kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="1e6ac-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="1e6ac-216">Opret kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="1e6ac-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="1e6ac-217">Opret kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="1e6ac-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="1e6ac-218">Opret kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="1e6ac-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="1e6ac-219">Opdater kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="1e6ac-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="1e6ac-220">Opdater kreditorer i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="1e6ac-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="1e6ac-221">Opdater kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="1e6ac-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="1e6ac-222">Opdater kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="1e6ac-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="1e6ac-223">På datafabrikken skal du køre skabelonen ved at vælge **Udløs nu** som vist på følgende billede.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="1e6ac-224">Det kan tage et par timer, før denne proces er fuldført, afhængigt af datavolumen.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![Udløserkørsel](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="1e6ac-226">Hvis du har tilpasninger af **Konto**, **Kontakt** og **Leverandør**, skal du redigere skabelonen.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="1e6ac-227">Importér de nye **Part**-poster i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="1e6ac-228">Download filen `FONewParty.csv` fra Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="1e6ac-229">Stien er `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="1e6ac-230">Konverter filen `FONewParty.csv` til en Excel-fil, og importér Excel-filen til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="1e6ac-231">Hvis csv-importen fungerer for dig, kan du importere csv-filen direkte.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="1e6ac-232">Det kan tage et par timer at importere, afhængigt af datavolumen.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="1e6ac-233">Du kan finde flere oplysninger i [Oversigt over dataimport og eksportjob](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).</span><span class="sxs-lookup"><span data-stu-id="1e6ac-233">For more information, see [Data import and export jobs overview](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).</span></span>

    ![Importere Dataverse-partposterne](media/data-factory-import-party.png)

9. <span data-ttu-id="1e6ac-235">Aktivér følgende plugin-trin i kundeengagementsapps:</span><span class="sxs-lookup"><span data-stu-id="1e6ac-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="1e6ac-236">Opdater konto</span><span class="sxs-lookup"><span data-stu-id="1e6ac-236">Account Update</span></span>
         + <span data-ttu-id="1e6ac-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Opdatering af konto</span><span class="sxs-lookup"><span data-stu-id="1e6ac-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="1e6ac-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Opdatering af konto</span><span class="sxs-lookup"><span data-stu-id="1e6ac-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="1e6ac-239">Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="1e6ac-239">Contact Update</span></span>
         + <span data-ttu-id="1e6ac-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="1e6ac-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="1e6ac-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="1e6ac-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="1e6ac-242">Opdatering af msdyn_party</span><span class="sxs-lookup"><span data-stu-id="1e6ac-242">msdyn_party Update</span></span>
         + <span data-ttu-id="1e6ac-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Opdatering af msdyn_party</span><span class="sxs-lookup"><span data-stu-id="1e6ac-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="1e6ac-244">Opdatering af msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="1e6ac-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="1e6ac-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Opdatering af msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="1e6ac-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="1e6ac-246">I apps til kundeengagement skal du aktivere følgende arbejdsgange, hvis du deaktiverede dem i forrige trin:</span><span class="sxs-lookup"><span data-stu-id="1e6ac-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="1e6ac-247">Opret kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="1e6ac-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="1e6ac-248">Opret kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="1e6ac-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="1e6ac-249">Opret kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="1e6ac-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="1e6ac-250">Opret kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="1e6ac-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="1e6ac-251">Opdater kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="1e6ac-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="1e6ac-252">Opdater kreditorer i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="1e6ac-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="1e6ac-253">Opdater kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="1e6ac-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="1e6ac-254">Opdater kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="1e6ac-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="1e6ac-255">Kør de **Part**-relaterede kort som beskrevet i [Part- og globalt adressekartotek](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="1e6ac-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="1e6ac-256">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="1e6ac-256">Troubleshooting</span></span>

1. <span data-ttu-id="1e6ac-257">Hvis processen mislykkes, skal du køre datafabrikken igen med start fra den mislykkede aktivitet.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="1e6ac-258">Nogle filer genereres af datafabrikken, som du kan bruge til datavalideringsformål.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="1e6ac-259">Datafabrikken kører på basis af csv-filer, der er kommaseparerede.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="1e6ac-260">Hvis der er en feltværdi med komma, kan den forstyrre resultaterne.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="1e6ac-261">Du skal fjerne kommaerne.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="1e6ac-262">Fanen **Overvågning** indeholder oplysninger om alle trin og data, der er behandlet.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="1e6ac-263">Vælg et bestemt trin for at fejlfinde det.</span><span class="sxs-lookup"><span data-stu-id="1e6ac-263">Select a specific step to debug it.</span></span>

    ![Fanen Overvågning](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="1e6ac-265">Få mere at vide om skabelonen</span><span class="sxs-lookup"><span data-stu-id="1e6ac-265">Learn more about the template</span></span>

<span data-ttu-id="1e6ac-266">Du kan finde kommentarer til skabelonen i filen [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="1e6ac-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>
