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
ms.openlocfilehash: 32128d48bfac195530d70b60e67cfd4921fc001e
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941077"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="6bc25-103">Opgradere til modellen med part- og globalt adressekartotek</span><span class="sxs-lookup"><span data-stu-id="6bc25-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6bc25-104">[Azure Data Factory-skabelonen](https://aka.ms/dual-write-gab-adf) hjælper dig med at opgradere eksisterende tabeldata for **Konto**, **Kontakt** og **Leverandør** i dobbeltskrivning til part- og det globale adressekartoteks model.</span><span class="sxs-lookup"><span data-stu-id="6bc25-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="6bc25-105">Skabelonen afstemmer dataene fra både Finance and Operations-apps og programmer til kundeengagement.</span><span class="sxs-lookup"><span data-stu-id="6bc25-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="6bc25-106">I slutningen af processen oprettes der **Part**- og **Kontakt**-felter for **Part**-poster, som knyttes til posterne **Konto**, **Kontakt** og **Leverandør** i kundeengagementsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="6bc25-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="6bc25-107">Der genereres en .csv-fil (`FONewParty.csv`) for at oprette nye **Part**-poster i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="6bc25-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="6bc25-108">Dette emne indeholder instruktioner til brug af Data Factory-skabelonen og opgradering af dine data.</span><span class="sxs-lookup"><span data-stu-id="6bc25-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="6bc25-109">Hvis du ikke har tilpasninger, kan du bruge skabelonen, som den er.</span><span class="sxs-lookup"><span data-stu-id="6bc25-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="6bc25-110">Hvis du har tilpasninger af **Konto**, **Kontakt** og **Leverandør**, skal du redigere skabelonen ved hjælp af følgende vejledning.</span><span class="sxs-lookup"><span data-stu-id="6bc25-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="6bc25-111">Skabelonen hjælper kun med at opgradere **Part**-dataene.</span><span class="sxs-lookup"><span data-stu-id="6bc25-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="6bc25-112">I en fremtidig version inkluderes post- og elektroniske adresser.</span><span class="sxs-lookup"><span data-stu-id="6bc25-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6bc25-113">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="6bc25-113">Prerequisites</span></span>

<span data-ttu-id="6bc25-114">Disse forudsætninger er obligatoriske:</span><span class="sxs-lookup"><span data-stu-id="6bc25-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="6bc25-115">Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="6bc25-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="6bc25-116">Adgang til skabelonen</span><span class="sxs-lookup"><span data-stu-id="6bc25-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="6bc25-117">Du er eksisterende dobbeltskrivningskunde.</span><span class="sxs-lookup"><span data-stu-id="6bc25-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="6bc25-118">Forberede opgraderingen</span><span class="sxs-lookup"><span data-stu-id="6bc25-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="6bc25-119">**Fuldt synkroniseret**: Begge miljøer er synkroniseret fuldstændigt for **Konto (kunde)**, **Kontakt** og **Leverandør**.</span><span class="sxs-lookup"><span data-stu-id="6bc25-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="6bc25-120">**Integrationsnøgler**: **Konto (kunde)**, **Kontakt** og **Leverandør** tabeller i kundeengagementapps bruger de integrationsnøgler, der leveres som standard.</span><span class="sxs-lookup"><span data-stu-id="6bc25-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="6bc25-121">Hvis du har tilpasset integrationsnøglerne, skal du tilpasse skabelonen.</span><span class="sxs-lookup"><span data-stu-id="6bc25-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="6bc25-122">**Partnummer**: Alle **Konto (kunde)**, **Kontakt** og **Leverandør** poster, der skal opgraderes, har et **Part**-nummer.</span><span class="sxs-lookup"><span data-stu-id="6bc25-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="6bc25-123">Poster uden et **Part**-nummer ignoreres.</span><span class="sxs-lookup"><span data-stu-id="6bc25-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="6bc25-124">Hvis du vil opgradere disse poster, skal du føje et **Part**-nummer til dem, før du starter opgraderingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="6bc25-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="6bc25-125">**Systemnedlukning**: Under opgraderingsprocessen skal både Finance and Operations og kundeengagementsmiljøer være offline.</span><span class="sxs-lookup"><span data-stu-id="6bc25-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="6bc25-126">**Øjebliksbillede**: Tag øjebliksbilleder af både Finance and Operations og kundeengagementapps.</span><span class="sxs-lookup"><span data-stu-id="6bc25-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="6bc25-127">Du kan bruge øjebliksbillederne til at gendanne den forrige tilstand, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="6bc25-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="6bc25-128">Installation</span><span class="sxs-lookup"><span data-stu-id="6bc25-128">Deployment</span></span>

1. <span data-ttu-id="6bc25-129">Hent skabelonen fra [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="6bc25-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="6bc25-130">Log på [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="6bc25-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="6bc25-131">Opret en [ressourcegruppe](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="6bc25-131">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="6bc25-132">Opret en [lagerkonto](/azure/storage/common/storage-account-create?tabs=azure-portal) i den ressourcegruppe, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="6bc25-132">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="6bc25-133">Opret en [datafabrik](/azure/data-factory/quickstart-create-data-factory-portal) i den ressourcegruppe, du har oprettet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="6bc25-133">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="6bc25-134">Åbn datafabrikken, og vælg feltet **Forfatter og overvåger**.</span><span class="sxs-lookup"><span data-stu-id="6bc25-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="6bc25-135">Vælg **ARM-skabelon** under fanen **Administrer**.</span><span class="sxs-lookup"><span data-stu-id="6bc25-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="6bc25-136">Vælg **Importér ARM-skabelon** for at importere **Part**-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="6bc25-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="6bc25-137">Importér skabelonen til datafabrikken.</span><span class="sxs-lookup"><span data-stu-id="6bc25-137">Import the template into the data factory.</span></span> <span data-ttu-id="6bc25-138">Angiv følgende værdier for **Projektdetaljer** og **Forekomstdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="6bc25-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="6bc25-139">Felt</span><span class="sxs-lookup"><span data-stu-id="6bc25-139">Field</span></span> | <span data-ttu-id="6bc25-140">Værdi</span><span class="sxs-lookup"><span data-stu-id="6bc25-140">Value</span></span>
    ---|---
    <span data-ttu-id="6bc25-141">Abonnement</span><span class="sxs-lookup"><span data-stu-id="6bc25-141">Subscription</span></span> | <span data-ttu-id="6bc25-142">Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="6bc25-142">Azure subscription</span></span>
    <span data-ttu-id="6bc25-143">Ressourcegruppe</span><span class="sxs-lookup"><span data-stu-id="6bc25-143">Resource group</span></span> | <span data-ttu-id="6bc25-144">Angiv den samme ressource, som lagerkontoen oprettes under.</span><span class="sxs-lookup"><span data-stu-id="6bc25-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="6bc25-145">Land/område</span><span class="sxs-lookup"><span data-stu-id="6bc25-145">Region</span></span> | <span data-ttu-id="6bc25-146">Angiv område.</span><span class="sxs-lookup"><span data-stu-id="6bc25-146">Specify region.</span></span>
    <span data-ttu-id="6bc25-147">Navn på fabrik</span><span class="sxs-lookup"><span data-stu-id="6bc25-147">Factory Name</span></span> | <span data-ttu-id="6bc25-148">Angiv fabriksnavnet.</span><span class="sxs-lookup"><span data-stu-id="6bc25-148">Specify factory name.</span></span>
    <span data-ttu-id="6bc25-149">Hovednøgle til sammenkædet service</span><span class="sxs-lookup"><span data-stu-id="6bc25-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="6bc25-150">Angiv programnøglen.</span><span class="sxs-lookup"><span data-stu-id="6bc25-150">Specify the application's key.</span></span>
    <span data-ttu-id="6bc25-151">Forbindelsesstreng til Azure Blob Storage</span><span class="sxs-lookup"><span data-stu-id="6bc25-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="6bc25-152">Forbindelsesstrengen til Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="6bc25-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="6bc25-153">Dynamics CRM-sammenkædet serviceadgangskode</span><span class="sxs-lookup"><span data-stu-id="6bc25-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="6bc25-154">Adgangskoden for den brugerkonto, du har angivet som brugernavn.</span><span class="sxs-lookup"><span data-stu-id="6bc25-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="6bc25-155">FO-sammenkædet Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="6bc25-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="6bc25-156">FO-sammenkædet Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="6bc25-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="6bc25-157">Angiv de lejeroplysninger (domænenavn eller lejer-id), hvor dit program er placeret.</span><span class="sxs-lookup"><span data-stu-id="6bc25-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="6bc25-158">FO-sammenkædet Service_properties_type Properties_aad ressource-id</span><span class="sxs-lookup"><span data-stu-id="6bc25-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="6bc25-159">FO-sammenkædet Service_properties_type Properties_service hoved-id</span><span class="sxs-lookup"><span data-stu-id="6bc25-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="6bc25-160">Angiv programmets klient-id.</span><span class="sxs-lookup"><span data-stu-id="6bc25-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="6bc25-161">Dynamics CRM-sammenkædet Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="6bc25-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="6bc25-162">Det brugernavn, der skal forbindes med Dynamics.</span><span class="sxs-lookup"><span data-stu-id="6bc25-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="6bc25-163">Du kan finde flere oplysninger i [Manuelt promovere en Resource Manager-skabelon for hvert miljø](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Sammenkædede tjenesteegenskaber](/azure/data-factory/connector-dynamics-ax#linked-service-properties) og [Kopiere data vha. Azure Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="6bc25-163">For more information, see [Manually promote a Resource Manager template for each environment](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="6bc25-164">Efter installationen skal du validere datasæt, dataflow og tilknyttet tjeneste for datafabrikken.</span><span class="sxs-lookup"><span data-stu-id="6bc25-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Datasæt, dataflow og tilknyttet tjeneste](media/data-factory-validate.png)

11. <span data-ttu-id="6bc25-166">Naviger til **Administrer**.</span><span class="sxs-lookup"><span data-stu-id="6bc25-166">Navigate to **Manage**.</span></span> <span data-ttu-id="6bc25-167">Vælg **Sammenkædet tjeneste** under **Forbindelser**.</span><span class="sxs-lookup"><span data-stu-id="6bc25-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="6bc25-168">Vælg **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="6bc25-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="6bc25-169">Angiv følgende værdier i formularen **Rediger sammenkædet tjeneste (Dynamics CRM)**:</span><span class="sxs-lookup"><span data-stu-id="6bc25-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="6bc25-170">Felt</span><span class="sxs-lookup"><span data-stu-id="6bc25-170">Field</span></span> | <span data-ttu-id="6bc25-171">Værdi</span><span class="sxs-lookup"><span data-stu-id="6bc25-171">Value</span></span>
    ---|---
    <span data-ttu-id="6bc25-172">Navn</span><span class="sxs-lookup"><span data-stu-id="6bc25-172">Name</span></span> | <span data-ttu-id="6bc25-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="6bc25-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="6bc25-174">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="6bc25-174">Description</span></span> | <span data-ttu-id="6bc25-175">Sammenkædede tjenester, der bruges til at oprette forbindelse til CRM-forekomst for at hente data til enheder</span><span class="sxs-lookup"><span data-stu-id="6bc25-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="6bc25-176">Oprette forbindelse via integrationskørsel</span><span class="sxs-lookup"><span data-stu-id="6bc25-176">Connect via integration runtime</span></span> | <span data-ttu-id="6bc25-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6bc25-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="6bc25-178">Installationstype</span><span class="sxs-lookup"><span data-stu-id="6bc25-178">Deployment type</span></span> | <span data-ttu-id="6bc25-179">Online</span><span class="sxs-lookup"><span data-stu-id="6bc25-179">Online</span></span>
    <span data-ttu-id="6bc25-180">Tjeneste-URI</span><span class="sxs-lookup"><span data-stu-id="6bc25-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="6bc25-181">Godkendelsestype</span><span class="sxs-lookup"><span data-stu-id="6bc25-181">Authentication type</span></span> | <span data-ttu-id="6bc25-182">Office365</span><span class="sxs-lookup"><span data-stu-id="6bc25-182">Office365</span></span>
    <span data-ttu-id="6bc25-183">Brugernavn</span><span class="sxs-lookup"><span data-stu-id="6bc25-183">User name</span></span> |
    <span data-ttu-id="6bc25-184">Adgangskode eller Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="6bc25-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="6bc25-185">Adgangskode</span><span class="sxs-lookup"><span data-stu-id="6bc25-185">Password</span></span>
    <span data-ttu-id="6bc25-186">Adgangskode</span><span class="sxs-lookup"><span data-stu-id="6bc25-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="6bc25-187">Køre skabelonen</span><span class="sxs-lookup"><span data-stu-id="6bc25-187">Run the template</span></span>

1. <span data-ttu-id="6bc25-188">Stop følgende dobbeltskrivning af **Konto**, **Kontakt** og **Leverandør** ved hjælp af appen Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6bc25-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="6bc25-189">Debitorer V3 (konti)</span><span class="sxs-lookup"><span data-stu-id="6bc25-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="6bc25-190">Debitorer V3 (kontakter)</span><span class="sxs-lookup"><span data-stu-id="6bc25-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="6bc25-191">CDS-kontakter V2 (kontakter)</span><span class="sxs-lookup"><span data-stu-id="6bc25-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="6bc25-192">CDS-kontakter V2 (kontakter)</span><span class="sxs-lookup"><span data-stu-id="6bc25-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="6bc25-193">Kreditor V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="6bc25-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="6bc25-194">Kontrollér, at tilknytningerne er fjernet fra `msdy_dualwriteruntimeconfig`-tabellen i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6bc25-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="6bc25-195">Installer [Løsninger til part og globalt adressekartotek for dobbeltskrivning](https://aka.ms/dual-write-gab) fra AppSource.</span><span class="sxs-lookup"><span data-stu-id="6bc25-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="6bc25-196">Hvis følgende tabeller indeholder data i appen Finance and Operations, skal du køre **Første synkronisering** for dem.</span><span class="sxs-lookup"><span data-stu-id="6bc25-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="6bc25-197">Tiltaleformer</span><span class="sxs-lookup"><span data-stu-id="6bc25-197">Salutations</span></span>
    + <span data-ttu-id="6bc25-198">Personlige tegntyper</span><span class="sxs-lookup"><span data-stu-id="6bc25-198">Personal character types</span></span>
    + <span data-ttu-id="6bc25-199">Afsluttende hilsner</span><span class="sxs-lookup"><span data-stu-id="6bc25-199">Complimentary closing</span></span>
    + <span data-ttu-id="6bc25-200">Titler på kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="6bc25-200">Contact person titles</span></span>
    + <span data-ttu-id="6bc25-201">Beslutningstagerrolle</span><span class="sxs-lookup"><span data-stu-id="6bc25-201">Decision making roles</span></span>
    + <span data-ttu-id="6bc25-202">Loyalitetsniveauer</span><span class="sxs-lookup"><span data-stu-id="6bc25-202">Loyalty levels</span></span>

5. <span data-ttu-id="6bc25-203">Deaktiver følgende plugin-trin i kundeengagementsappen.</span><span class="sxs-lookup"><span data-stu-id="6bc25-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="6bc25-204">Opdater konto</span><span class="sxs-lookup"><span data-stu-id="6bc25-204">Account Update</span></span>
         + <span data-ttu-id="6bc25-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Opdatering af konto</span><span class="sxs-lookup"><span data-stu-id="6bc25-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="6bc25-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Opdatering af konto</span><span class="sxs-lookup"><span data-stu-id="6bc25-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="6bc25-207">Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="6bc25-207">Contact Update</span></span>
         + <span data-ttu-id="6bc25-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="6bc25-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="6bc25-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="6bc25-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="6bc25-210">Opdatering af msdyn_party</span><span class="sxs-lookup"><span data-stu-id="6bc25-210">msdyn_party Update</span></span>
         + <span data-ttu-id="6bc25-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Opdatering af msdyn_party</span><span class="sxs-lookup"><span data-stu-id="6bc25-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="6bc25-212">Opdatering af msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="6bc25-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="6bc25-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Opdatering af msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="6bc25-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="6bc25-214">Deaktiver følgende arbejdsflows i kundeengagementsappen:</span><span class="sxs-lookup"><span data-stu-id="6bc25-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="6bc25-215">Opret kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="6bc25-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="6bc25-216">Opret kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="6bc25-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="6bc25-217">Opret kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="6bc25-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="6bc25-218">Opret kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="6bc25-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="6bc25-219">Opdater kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="6bc25-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="6bc25-220">Opdater kreditorer i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="6bc25-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="6bc25-221">Opdater kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="6bc25-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="6bc25-222">Opdater kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="6bc25-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="6bc25-223">På datafabrikken skal du køre skabelonen ved at vælge **Udløs nu** som vist på følgende billede.</span><span class="sxs-lookup"><span data-stu-id="6bc25-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="6bc25-224">Det kan tage et par timer, før denne proces er fuldført, afhængigt af datavolumen.</span><span class="sxs-lookup"><span data-stu-id="6bc25-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![Udløserkørsel](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="6bc25-226">Hvis du har tilpasninger af **Konto**, **Kontakt** og **Leverandør**, skal du redigere skabelonen.</span><span class="sxs-lookup"><span data-stu-id="6bc25-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="6bc25-227">Importér de nye **Part**-poster i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="6bc25-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="6bc25-228">Download filen `FONewParty.csv` fra Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="6bc25-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="6bc25-229">Stien er `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="6bc25-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="6bc25-230">Konverter filen `FONewParty.csv` til en Excel-fil, og importér Excel-filen til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="6bc25-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="6bc25-231">Hvis csv-importen fungerer for dig, kan du importere csv-filen direkte.</span><span class="sxs-lookup"><span data-stu-id="6bc25-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="6bc25-232">Det kan tage et par timer at importere, afhængigt af datavolumen.</span><span class="sxs-lookup"><span data-stu-id="6bc25-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="6bc25-233">Du kan finde flere oplysninger i [Oversigt over dataimport og eksportjob](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="6bc25-233">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Importere Dataverse-partposterne](media/data-factory-import-party.png)

9. <span data-ttu-id="6bc25-235">Aktivér følgende plugin-trin i kundeengagementsapps:</span><span class="sxs-lookup"><span data-stu-id="6bc25-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="6bc25-236">Opdater konto</span><span class="sxs-lookup"><span data-stu-id="6bc25-236">Account Update</span></span>
         + <span data-ttu-id="6bc25-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Opdatering af konto</span><span class="sxs-lookup"><span data-stu-id="6bc25-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="6bc25-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Opdatering af konto</span><span class="sxs-lookup"><span data-stu-id="6bc25-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="6bc25-239">Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="6bc25-239">Contact Update</span></span>
         + <span data-ttu-id="6bc25-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="6bc25-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="6bc25-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Opdatering af kontakt</span><span class="sxs-lookup"><span data-stu-id="6bc25-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="6bc25-242">Opdatering af msdyn_party</span><span class="sxs-lookup"><span data-stu-id="6bc25-242">msdyn_party Update</span></span>
         + <span data-ttu-id="6bc25-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Opdatering af msdyn_party</span><span class="sxs-lookup"><span data-stu-id="6bc25-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="6bc25-244">Opdatering af msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="6bc25-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="6bc25-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Opdatering af msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="6bc25-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="6bc25-246">I apps til kundeengagement skal du aktivere følgende arbejdsgange, hvis du deaktiverede dem i forrige trin:</span><span class="sxs-lookup"><span data-stu-id="6bc25-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="6bc25-247">Opret kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="6bc25-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="6bc25-248">Opret kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="6bc25-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="6bc25-249">Opret kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="6bc25-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="6bc25-250">Opret kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="6bc25-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="6bc25-251">Opdater kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="6bc25-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="6bc25-252">Opdater kreditorer i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="6bc25-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="6bc25-253">Opdater kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="6bc25-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="6bc25-254">Opdater kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="6bc25-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="6bc25-255">Kør de **Part**-relaterede kort som beskrevet i [Part- og globalt adressekartotek](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="6bc25-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="6bc25-256">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="6bc25-256">Troubleshooting</span></span>

1. <span data-ttu-id="6bc25-257">Hvis processen mislykkes, skal du køre datafabrikken igen med start fra den mislykkede aktivitet.</span><span class="sxs-lookup"><span data-stu-id="6bc25-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="6bc25-258">Nogle filer genereres af datafabrikken, som du kan bruge til datavalideringsformål.</span><span class="sxs-lookup"><span data-stu-id="6bc25-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="6bc25-259">Datafabrikken kører på basis af csv-filer, der er kommaseparerede.</span><span class="sxs-lookup"><span data-stu-id="6bc25-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="6bc25-260">Hvis der er en feltværdi med komma, kan den forstyrre resultaterne.</span><span class="sxs-lookup"><span data-stu-id="6bc25-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="6bc25-261">Du skal fjerne kommaerne.</span><span class="sxs-lookup"><span data-stu-id="6bc25-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="6bc25-262">Fanen **Overvågning** indeholder oplysninger om alle trin og data, der er behandlet.</span><span class="sxs-lookup"><span data-stu-id="6bc25-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="6bc25-263">Vælg et bestemt trin for at fejlfinde det.</span><span class="sxs-lookup"><span data-stu-id="6bc25-263">Select a specific step to debug it.</span></span>

    ![Fanen Overvågning](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="6bc25-265">Få mere at vide om skabelonen</span><span class="sxs-lookup"><span data-stu-id="6bc25-265">Learn more about the template</span></span>

<span data-ttu-id="6bc25-266">Du kan finde kommentarer til skabelonen i filen [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="6bc25-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>