---
title: Tilføjelsesprogrammet Lagersynlighed
description: Dette emne beskriver, hvordan du installerer og konfigurerer tilføjelsesprogrammet Lagersynlighed til Dynamics 365 Supply Chain Management.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114664"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="01020-103">Tilføjelsesprogrammet Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="01020-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="01020-104">Tilføjelsesprogrammet Lagersynlighed er en uafhængig og meget skalerbar mikrotjeneste, der gør det muligt at registrere disponibel lagerbeholdning i realtid, hvilket giver en global visning af lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="01020-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="01020-105">Alle oplysninger, der vedrører disponibel lagerbeholdning, eksporteres for tjenesten næsten i realtid via SQL-integration på lavt niveau.</span><span class="sxs-lookup"><span data-stu-id="01020-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="01020-106">Eksterne systemer får adgang til tjenesten via RESTful-API'er for at forespørge på disponible oplysninger om bestemte sæt dimensioner, så der hentes en liste over tilgængelige disponible positioner.</span><span class="sxs-lookup"><span data-stu-id="01020-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="01020-107">Lagersynlighed er en mikrotjeneste, der bygger på Microsoft Dataverse, hvilket betyder, at du kan udvide den ved at opbygge Power Apps og anvende Power BI for at levere brugerdefinerede funktioner, der opfylder virksomhedens behov.</span><span class="sxs-lookup"><span data-stu-id="01020-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="01020-108">Du kan også opgradere indekset for at foretage lagerforespørgsler.</span><span class="sxs-lookup"><span data-stu-id="01020-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="01020-109">Lagersynlighed angiver konfigurationsindstillinger, så den kan integreres med flere tredjepartssystemer.</span><span class="sxs-lookup"><span data-stu-id="01020-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="01020-110">Den understøtter den standardiserede lagerdimension, tilpassede udvidelsesmuligheder og standardiserede, beregnede antal, der kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="01020-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="01020-111">Dette emne beskriver, hvordan du installerer og konfigurerer tilføjelsesprogrammet Lagersynlighed til Dynamics 365 Supply Chain Management, og hvordan du bruger dets API (Application Programming Interface).</span><span class="sxs-lookup"><span data-stu-id="01020-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="01020-112">Installere tilføjelsesprogrammet Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="01020-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="01020-113">Du skal installere tilføjelsesprogrammet Lagersynlighed ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="01020-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="01020-114">LCS er en samarbejdsportal, der leverer et miljø og et sæt regelmæssigt opdaterede tjenester, der hjælper dig med at administrere programlivscyklussen for dine Dynamics 365 Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="01020-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="01020-115">Yderligere oplysninger finder du i [Ressourcer til Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="01020-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="01020-116">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="01020-116">Prerequisites</span></span>

<span data-ttu-id="01020-117">Før du installerer tilføjelsesprogrammet Lagersynlighed, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="01020-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="01020-118">Få et LCS-implementeringsprojekt med mindst ét miljø installeret.</span><span class="sxs-lookup"><span data-stu-id="01020-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="01020-119">Generér betanøglerne til dit tilbud i LCS.</span><span class="sxs-lookup"><span data-stu-id="01020-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="01020-120">Aktivér betanøglerne for dit tilbud til din bruger i LCS.</span><span class="sxs-lookup"><span data-stu-id="01020-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="01020-121">Kontakt Microsoft-produktteamet for Lagersynlighed, og levér et miljø-id, hvor du vil installere tilføjelsesprogrammet Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="01020-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="01020-122">Hvis du har spørgsmål om disse forudsætninger, skal du kontakte produktteamet for Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="01020-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="01020-123">Installer tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="01020-123">Install the add-in</span></span>

<span data-ttu-id="01020-124">For at installere tilføjelsesprogrammet Lagersynlighed skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="01020-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="01020-125">Log på portalen [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="01020-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="01020-126">Vælg det projekt, dit miljø skal implementeres i, på startsiden.</span><span class="sxs-lookup"><span data-stu-id="01020-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="01020-127">Vælg det miljø, som tilføjelsesprogrammet skal installeres i, på projektsiden.</span><span class="sxs-lookup"><span data-stu-id="01020-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="01020-128">Rul ned på miljøsiden, indtil du ser afsnittet **Miljøtilføjelsesprogrammer**.</span><span class="sxs-lookup"><span data-stu-id="01020-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="01020-129">Hvis sektionen ikke vises, skal du kontrollere, at de nødvendige betanøgler er blevet behandlet fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="01020-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="01020-130">Vælg **Installér et nyt tilføjelsesprogram** i afsnittet **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="01020-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="01020-131">![Miljøsiden i LCS](media/inventory-visibility-environment.png "Miljøsiden i LCS")</span><span class="sxs-lookup"><span data-stu-id="01020-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="01020-132">Vælg linket **Installer et nyt tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="01020-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="01020-133">Der åbnes en liste over tilgængelige tilføjelsesprogrammer.</span><span class="sxs-lookup"><span data-stu-id="01020-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="01020-134">Vælg **Lagerservice** på listen.</span><span class="sxs-lookup"><span data-stu-id="01020-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="01020-135">(Bemærk, at den nu kan være angivet som **Tilføjelsesprogrammet Lagersynlighed til Dynamics 365 Supply Chain Management**).</span><span class="sxs-lookup"><span data-stu-id="01020-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="01020-136">Angiv værdier for følgende felter til dit miljø:</span><span class="sxs-lookup"><span data-stu-id="01020-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="01020-137">**AAD-program-id**</span><span class="sxs-lookup"><span data-stu-id="01020-137">**AAD application ID**</span></span>
    - <span data-ttu-id="01020-138">**AAD-lejer-id**</span><span class="sxs-lookup"><span data-stu-id="01020-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="01020-139">![Konfigurationsside for tilføjelsesprogram](media/inventory-visibility-setup.png "Konfigurationsside for tilføjelsesprogram")</span><span class="sxs-lookup"><span data-stu-id="01020-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="01020-140">Acceptér vilkårene og betingelsen ved at markere afkrydsningsfeltet **Vilkår og betingelser**.</span><span class="sxs-lookup"><span data-stu-id="01020-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="01020-141">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="01020-141">Select **Install**.</span></span> <span data-ttu-id="01020-142">Status for tilføjelsesprogrammet vil blive vist som **installerer**.</span><span class="sxs-lookup"><span data-stu-id="01020-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="01020-143">Når det er gjort, skal du opdatere siden for at se statusændringen til **Installeret**.</span><span class="sxs-lookup"><span data-stu-id="01020-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="01020-144">Få et token til sikkerhedsservice</span><span class="sxs-lookup"><span data-stu-id="01020-144">Get a security service token</span></span>

<span data-ttu-id="01020-145">Få et token til sikkerhedsservice ved at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="01020-145">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="01020-146">Log på Azure-portalen, og brug den til at finde `clientId` og `clientSecret` til din Supply Chain Management-applikation.</span><span class="sxs-lookup"><span data-stu-id="01020-146">Sign in to Azure Portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="01020-147">Hent et Azure Active Directory-token (`aadToken`) ved at sende en HTTP-anmodning med følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="01020-147">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="01020-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="01020-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="01020-149">**metode** - `GET`</span><span class="sxs-lookup"><span data-stu-id="01020-149">**Method** - `GET`</span></span>
    - <span data-ttu-id="01020-150">**Brødtekst (formulardata)**:</span><span class="sxs-lookup"><span data-stu-id="01020-150">**Body content (form data)**:</span></span>

        | <span data-ttu-id="01020-151">nøgle</span><span class="sxs-lookup"><span data-stu-id="01020-151">key</span></span> | <span data-ttu-id="01020-152">værdi</span><span class="sxs-lookup"><span data-stu-id="01020-152">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="01020-153">client_id</span><span class="sxs-lookup"><span data-stu-id="01020-153">client_id</span></span> | <span data-ttu-id="01020-154">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="01020-154">${aadAppId}</span></span> |
        | <span data-ttu-id="01020-155">client_secret</span><span class="sxs-lookup"><span data-stu-id="01020-155">client_secret</span></span> | <span data-ttu-id="01020-156">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="01020-156">${aadAppSecret}</span></span> |
        | <span data-ttu-id="01020-157">grant_type</span><span class="sxs-lookup"><span data-stu-id="01020-157">grant_type</span></span> | <span data-ttu-id="01020-158">client_credentials</span><span class="sxs-lookup"><span data-stu-id="01020-158">client_credentials</span></span> |
        | <span data-ttu-id="01020-159">ressource</span><span class="sxs-lookup"><span data-stu-id="01020-159">resource</span></span> | <span data-ttu-id="01020-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="01020-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="01020-161">Du modtager et `aadToken` i svaret, der ligner følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="01020-161">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="01020-162">Formuler en JSON-anmodning, der ligner følgende:</span><span class="sxs-lookup"><span data-stu-id="01020-162">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="01020-163">Placering:</span><span class="sxs-lookup"><span data-stu-id="01020-163">Where:</span></span>
    - <span data-ttu-id="01020-164">Værdien `client_assertion` skal være det `aadToken`, du har modtaget i det forrige trin.</span><span class="sxs-lookup"><span data-stu-id="01020-164">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="01020-165">Værdien `context` skal være det miljø-id, hvor du vil implementere tilføjelsesprogrammet.</span><span class="sxs-lookup"><span data-stu-id="01020-165">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="01020-166">Angiv alle andre værdier som vist i eksemplet.</span><span class="sxs-lookup"><span data-stu-id="01020-166">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="01020-167">Send en HTTP-anmodning med følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="01020-167">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="01020-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="01020-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="01020-169">**metode** - `POST`</span><span class="sxs-lookup"><span data-stu-id="01020-169">**Method** - `POST`</span></span>
    - <span data-ttu-id="01020-170">**HTTP-overskrift** – Medtag API-versionen (nøglen er `Api-Version`, og værdien er `1.0`)</span><span class="sxs-lookup"><span data-stu-id="01020-170">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="01020-171">**Brødtekst** – Medtag den JSON-anmodning, du oprettede i det forrige trin.</span><span class="sxs-lookup"><span data-stu-id="01020-171">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="01020-172">Du vil få et `access_token` i svaret.</span><span class="sxs-lookup"><span data-stu-id="01020-172">You will get an `access_token` in response.</span></span> <span data-ttu-id="01020-173">Det skal du bruge som ihændehavertoken for at kalde Lagersynlighed-API'et.</span><span class="sxs-lookup"><span data-stu-id="01020-173">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="01020-174">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="01020-174">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="01020-175">Fjern tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="01020-175">Uninstall the add-in</span></span>

<span data-ttu-id="01020-176">Hvis du vil fjerne tilføjelsesprogrammet, skal du vælge **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="01020-176">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="01020-177">Opdater LCS, så tilføjelsesprogrammet Lagersynlighed fjernes.</span><span class="sxs-lookup"><span data-stu-id="01020-177">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="01020-178">Fjernelsesprocessen fjerner registreringen af tilføjelsesprogrammet og starter et job for at rydde op i alle de forretningsdata, der er gemt i tjenesten.</span><span class="sxs-lookup"><span data-stu-id="01020-178">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="01020-179">Offentlig API for tilføjelsesprogrammet Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="01020-179">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="01020-180">Den offentlige REST-API til tilføjelsesprogrammet Lagersynlighed viser flere specifikke integrationsslutpunkter.</span><span class="sxs-lookup"><span data-stu-id="01020-180">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="01020-181">Det understøtter tre overordnede interaktionstyper:</span><span class="sxs-lookup"><span data-stu-id="01020-181">It supports three main interaction types:</span></span>

- <span data-ttu-id="01020-182">Bogføring af ændret lagerbeholdning i tilføjelsesprogrammet fra et eksternt system.</span><span class="sxs-lookup"><span data-stu-id="01020-182">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="01020-183">Forespørgsel om aktuelle disponible lagerantal fra et eksternt system.</span><span class="sxs-lookup"><span data-stu-id="01020-183">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="01020-184">Automatisk synkronisering med lagerbeholdning i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="01020-184">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="01020-185">Den automatiske synkronisering er ikke en del af det offentlige API, men bliver i stedet håndteret i baggrunden for miljøer, der har aktiveret tilføjelsesprogrammet Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="01020-185">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="01020-186">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="01020-186">Authentication</span></span>

<span data-ttu-id="01020-187">Platformens sikkerhedstoken bruges til at kalde tilføjelsesprogrammet Lagersynlighed, så du skal generere et Azure Active Directory-token ved hjælp af dit Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="01020-187">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="01020-188">Du kan finde flere oplysninger om, hvordan du får fat i sikkerhedstoken, i [Installere tilføjelsesprogrammet Lagersynlighed](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="01020-188">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="01020-189">Konfigurere API'et til Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="01020-189">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="01020-190">Før du bruger tjenesten, skal du udføre de konfigurationer, der er beskrevet i følgende underafsnit.</span><span class="sxs-lookup"><span data-stu-id="01020-190">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="01020-191">Konfigurationen kan variere afhængigt af detaljerne i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="01020-191">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="01020-192">Den består primært af fire dele:</span><span class="sxs-lookup"><span data-stu-id="01020-192">It primarily includes four parts:</span></span>

- [<span data-ttu-id="01020-193">Partitionering</span><span class="sxs-lookup"><span data-stu-id="01020-193">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="01020-194">Dimensionskonfigurationer</span><span class="sxs-lookup"><span data-stu-id="01020-194">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="01020-195">Indeksering</span><span class="sxs-lookup"><span data-stu-id="01020-195">Indexing</span></span>](#indexing)
- [<span data-ttu-id="01020-196">Brugerdefineret måling</span><span class="sxs-lookup"><span data-stu-id="01020-196">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="01020-197">Partitionering</span><span class="sxs-lookup"><span data-stu-id="01020-197">Partitioning</span></span>

<span data-ttu-id="01020-198">Partitionering kan have stor indflydelse på ydeevnen af Lagersynlighed-API'et.</span><span class="sxs-lookup"><span data-stu-id="01020-198">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="01020-199">Det er en god ide at definere et skema, der giver mulighed for mindre gruppering af data, mens det stadig er muligt at give meningsfulde dataforespørgsler.</span><span class="sxs-lookup"><span data-stu-id="01020-199">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="01020-200">Elementet `organizationId` (`dataAreaId` i Supply Chain Management) vil altid være en del af partitionen, og Lagersynlighede er som standard angivet til at partitionere efter dimensioner som *Sted + lokation*.</span><span class="sxs-lookup"><span data-stu-id="01020-200">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="01020-201">Det betyder, at der altid skal sendes forespørgsler til tjenesten med de dimensioner, der er defineret på filtrene.</span><span class="sxs-lookup"><span data-stu-id="01020-201">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="01020-202">*Sted* og *Lokation* er to generelle standarddimensioner i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="01020-202">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="01020-203">I Supply Chain Management kaldes disse dimensioner *Sted* (`InventSiteId`) og *Lagersted* (`InventLocationId`).</span><span class="sxs-lookup"><span data-stu-id="01020-203">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="01020-204">Dimensionskonfigurationer</span><span class="sxs-lookup"><span data-stu-id="01020-204">Dimension configurations</span></span>

<span data-ttu-id="01020-205">Lagersynlighed vil indeholde en liste over generelle standarddimensioner, der gør det muligt at integrere flere kildesystemer.</span><span class="sxs-lookup"><span data-stu-id="01020-205">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="01020-206">I følgende tabel vises de lagerdimensioner, der vil være standarddimensionsnavne i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="01020-206">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="01020-207">Dimensionstype</span><span class="sxs-lookup"><span data-stu-id="01020-207">Dimension type</span></span> | <span data-ttu-id="01020-208">Dimensionens navn</span><span class="sxs-lookup"><span data-stu-id="01020-208">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="01020-209">Produkt</span><span class="sxs-lookup"><span data-stu-id="01020-209">Product</span></span> | `ColorId` |
| <span data-ttu-id="01020-210">Produkt</span><span class="sxs-lookup"><span data-stu-id="01020-210">Product</span></span> | `SizeId` |
| <span data-ttu-id="01020-211">Produkt</span><span class="sxs-lookup"><span data-stu-id="01020-211">Product</span></span> | `StyleId` |
| <span data-ttu-id="01020-212">Produkt</span><span class="sxs-lookup"><span data-stu-id="01020-212">Product</span></span> | `ConfigId` |
| <span data-ttu-id="01020-213">Sporing</span><span class="sxs-lookup"><span data-stu-id="01020-213">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="01020-214">Sporing</span><span class="sxs-lookup"><span data-stu-id="01020-214">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="01020-215">Adresse</span><span class="sxs-lookup"><span data-stu-id="01020-215">Location</span></span> | `LocationId` |
| <span data-ttu-id="01020-216">Adresse</span><span class="sxs-lookup"><span data-stu-id="01020-216">Location</span></span> | `SiteId` |
| <span data-ttu-id="01020-217">Lagerstatus</span><span class="sxs-lookup"><span data-stu-id="01020-217">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="01020-218">Lagerstedsspecifik</span><span class="sxs-lookup"><span data-stu-id="01020-218">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="01020-219">Lagerstedsspecifik</span><span class="sxs-lookup"><span data-stu-id="01020-219">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="01020-220">Lagerstedsspecifik</span><span class="sxs-lookup"><span data-stu-id="01020-220">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="01020-221">Den dimensionstype, der er angivet i forrige tabel, er kun til reference.</span><span class="sxs-lookup"><span data-stu-id="01020-221">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="01020-222">Du behøver ikke definere dimensionstypen i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="01020-222">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="01020-223">Hvis der findes en brugerdefineret dimension, som skal overføres til en standardværdi, når den forbruges af Lagersynlighed, kan du konfigurere navnet **Brugerdefineret dimension** i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="01020-223">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="01020-224">Eksterne systemer får adgang til Lagersynlighed gennem RESTful API'er, der muliggør disponible oplysninger om bestemte sæt dimensioner, der skal forespørges.</span><span class="sxs-lookup"><span data-stu-id="01020-224">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="01020-225">I forbindelse med integrationen giver Lagersynlighed dig mulighed for at konfigurere den *eksterne kanals datakilde* og kildedimensionen til *måldimensionerne* i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="01020-225">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="01020-226">Måldimensionerne skal være en af følgende:</span><span class="sxs-lookup"><span data-stu-id="01020-226">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="01020-227">Standarddimensioner i Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="01020-227">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="01020-228">Brugerdefinerede dimensioner</span><span class="sxs-lookup"><span data-stu-id="01020-228">Custom dimensions</span></span>

<span data-ttu-id="01020-229">Formålet med dimensionskonfiguration er at standardisere integrationen af flere systemer til forespørgslen på dimensioner og bogføringshændelsen med dimensioner.</span><span class="sxs-lookup"><span data-stu-id="01020-229">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="01020-230">Indeksering</span><span class="sxs-lookup"><span data-stu-id="01020-230">Indexing</span></span>

<span data-ttu-id="01020-231">I de fleste tilfælde vil lagerbeholdningsforespørgslen ikke kun være på det højeste "totale" niveau, men du ønsker måske at se de samlede resultater på baggrund af lagerdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="01020-231">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="01020-232">Lagersynlighed giver fleksibilitet, fordi du kan konfigurere de indekser, der er baseret på dimensionen eller kombinationen af dimensionerne.</span><span class="sxs-lookup"><span data-stu-id="01020-232">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="01020-233">I øjeblikket kan du kun konfigurere indekser til maksimalt fem.</span><span class="sxs-lookup"><span data-stu-id="01020-233">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="01020-234">Du skal nøje overveje, hvilken dimension eller dimensionskombination du vil bruge før implementeringen for at sikre, at den opfylder dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="01020-234">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="01020-235">Hvis du f.eks. vil forespørge på produkter på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="01020-235">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="01020-236">Forespørg på den samlede disponible beholdning via *Farve*- og *Størrelse*-dimensionerne.</span><span class="sxs-lookup"><span data-stu-id="01020-236">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="01020-237">I nogle tilfælde vil du kun forespørge på produktet i alt.</span><span class="sxs-lookup"><span data-stu-id="01020-237">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="01020-238">Du skal have defineret to indekser som følgende:</span><span class="sxs-lookup"><span data-stu-id="01020-238">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="01020-239">Den tomme kantede parentes samles på basis af produkt-id'et i partitionen.</span><span class="sxs-lookup"><span data-stu-id="01020-239">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="01020-240">Indekseringen definerer, hvordan du kan gruppere resultaterne baseret på `groupBy`-forespørgselsindstillingen.</span><span class="sxs-lookup"><span data-stu-id="01020-240">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="01020-241">Hvis du ikke definerer `groupBy`-værdier, får du totaler med `productid`.</span><span class="sxs-lookup"><span data-stu-id="01020-241">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="01020-242">Hvis du definerer `groupBy` som `groupBy=ColorId&groupBy=SizeId`, får du flere linjer baseret på de forskellige kombinationer af farve og størrelse i systemet.</span><span class="sxs-lookup"><span data-stu-id="01020-242">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="01020-243">Du kan sætte dine forespørgselskriterier i anmodningsteksten.</span><span class="sxs-lookup"><span data-stu-id="01020-243">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="01020-244">Her er et eksempel på en forespørgsel på produktet med en kombination af farve og størrelse.</span><span class="sxs-lookup"><span data-stu-id="01020-244">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="01020-245">Brugerdefineret måling</span><span class="sxs-lookup"><span data-stu-id="01020-245">Custom measurement</span></span>

<span data-ttu-id="01020-246">Standardmålingen af antal er knyttet til Supply Chain Management, men det kan være en god ide at have et antal, der består af en kombination af standardmålingerne.</span><span class="sxs-lookup"><span data-stu-id="01020-246">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="01020-247">Hvis du vil gøre dette, kan du have en konfiguration af brugerdefinerede antal, der føjes til outputtet af forespørgsler på den disponible lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="01020-247">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="01020-248">Denne funktion giver dig mulighed for at definere et sæt målinger, der skal tilføjes, og/eller et sæt målinger, der skal trækkes fra, så de danner den brugerdefinerede måling.</span><span class="sxs-lookup"><span data-stu-id="01020-248">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="01020-249">I følgende forespørgselsbetingelse skal du f.eks. konfigurere det brugerdefinerede måleanta som `MyCustomAvailableforReservation`, der skal forbruges af forbrugssystemet.</span><span class="sxs-lookup"><span data-stu-id="01020-249">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="01020-250">Forbrugssystem</span><span class="sxs-lookup"><span data-stu-id="01020-250">Consumption system</span></span> | <span data-ttu-id="01020-251">Beregnede målinger</span><span class="sxs-lookup"><span data-stu-id="01020-251">Calculated measurers</span></span> | <span data-ttu-id="01020-252">Datakilde</span><span class="sxs-lookup"><span data-stu-id="01020-252">Data source</span></span> | <span data-ttu-id="01020-253">Modifikator</span><span class="sxs-lookup"><span data-stu-id="01020-253">Modifier</span></span> | <span data-ttu-id="01020-254">Modifikator som beregningstype</span><span class="sxs-lookup"><span data-stu-id="01020-254">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="01020-255">Addition</span><span class="sxs-lookup"><span data-stu-id="01020-255">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="01020-256">Addition</span><span class="sxs-lookup"><span data-stu-id="01020-256">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="01020-257">Subtraktion</span><span class="sxs-lookup"><span data-stu-id="01020-257">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="01020-258">Addition</span><span class="sxs-lookup"><span data-stu-id="01020-258">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="01020-259">Subtraktion</span><span class="sxs-lookup"><span data-stu-id="01020-259">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="01020-260">Addition</span><span class="sxs-lookup"><span data-stu-id="01020-260">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="01020-261">Addition</span><span class="sxs-lookup"><span data-stu-id="01020-261">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="01020-262">Subtraktion</span><span class="sxs-lookup"><span data-stu-id="01020-262">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="01020-263">Subtraktion</span><span class="sxs-lookup"><span data-stu-id="01020-263">Subtraction</span></span> |

<span data-ttu-id="01020-264">Med denne fremgangsmåde vil forespørgslen på det brugerdefinerede måleantal returnere følgende output.</span><span class="sxs-lookup"><span data-stu-id="01020-264">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="01020-265">Outputtet `MyCustomAvailableforReservation` er baseret på beregningsindstillingen i de brugerdefinerede målinger som:</span><span class="sxs-lookup"><span data-stu-id="01020-265">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="01020-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="01020-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="01020-267">Bogføring af ændret lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="01020-267">Posting on-hand changes</span></span>

<span data-ttu-id="01020-268">Den præcise URL-adresse, som hændelsen vil blive bogført til, afhænger af dit geografiske område.</span><span class="sxs-lookup"><span data-stu-id="01020-268">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="01020-269">Den har formatet:</span><span class="sxs-lookup"><span data-stu-id="01020-269">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="01020-270">Når denne URL-adresse er godkendt, kan den bruges sammen med HTTP-`POST`-metoden til at sende hændelser for beholdningsændring til tjenesten.</span><span class="sxs-lookup"><span data-stu-id="01020-270">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="01020-271">En speciel header bruges til kommunikation med Dynamics 365-tjenester via HTTP-anmodninger, der angiver miljø-id'et for Supply Chain Management-forekomst, som dataene er kædet sammen med.</span><span class="sxs-lookup"><span data-stu-id="01020-271">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="01020-272">F.eks.:</span><span class="sxs-lookup"><span data-stu-id="01020-272">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="01020-273">Bogføring af forespørgsel på lagerbeholdningsændringer, eksempel 1</span><span class="sxs-lookup"><span data-stu-id="01020-273">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="01020-274">I dette eksempel vises et scenario, hvor du konfigurerer dimensionskonfigurationen i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="01020-274">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="01020-275">Brug følgende forespørgsel til at konfigurere dimensionstilknytningen i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="01020-275">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="01020-276">Nu kan du angive `dimensionDataSource` og bruge brugerdefinerede dimensioner i forespørgslerne.</span><span class="sxs-lookup"><span data-stu-id="01020-276">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="01020-277">Systemet vil automatisk konvertere brugerdefinerede dimensioner til basisdimensioner.</span><span class="sxs-lookup"><span data-stu-id="01020-277">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="01020-278">Bogføring af forespørgsel på lagerbeholdningsændringer, eksempel 2</span><span class="sxs-lookup"><span data-stu-id="01020-278">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="01020-279">I dette eksempel vises et scenario, hvor der ikke er konfigureret tilknytninger for dimensionskonfigurationen i Power Apps, så bogføringen skal også bruge basisdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="01020-279">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="01020-280">Alle dimensioner skal være basisdimensioner, når `dimensionDataSource`-feltet er null, tomt eller blanktegn.</span><span class="sxs-lookup"><span data-stu-id="01020-280">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="01020-281">JSON-dokumentfeltegenskaber</span><span class="sxs-lookup"><span data-stu-id="01020-281">JSON document field properties</span></span>

<span data-ttu-id="01020-282">Felterne fra de JSON-forespørgselseksempler, der tidligere blev vist, har de egenskaber, der er angivet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="01020-282">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="01020-283">Felt-id</span><span class="sxs-lookup"><span data-stu-id="01020-283">Field ID</span></span> | <span data-ttu-id="01020-284">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="01020-284">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="01020-285">Et entydigt id for den specifikke ændringshændelse.</span><span class="sxs-lookup"><span data-stu-id="01020-285">A unique ID for the specific change event.</span></span> <span data-ttu-id="01020-286">Dette id bruges til at sikre, at hvis kommunikationen med tjenesten mislykkes under bogføring, vil genafsendelse af hændelsen ikke resultere i, at den samme hændelse tælles to gange i systemet.</span><span class="sxs-lookup"><span data-stu-id="01020-286">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="01020-287">Identifikatoren for den organisation, der er knyttet til hændelsen.</span><span class="sxs-lookup"><span data-stu-id="01020-287">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="01020-288">Dette knytter data til Supply Chain Management-organisationer eller dataområde-id'er.</span><span class="sxs-lookup"><span data-stu-id="01020-288">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="01020-289">Produktets identifikator.</span><span class="sxs-lookup"><span data-stu-id="01020-289">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="01020-290">Det antal, som lagerbeholdningen skal ændres med.</span><span class="sxs-lookup"><span data-stu-id="01020-290">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="01020-291">Hvis der f.eks. er føjet 10 nye bagels til en hylde, vil denne værdi være 10.</span><span class="sxs-lookup"><span data-stu-id="01020-291">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="01020-292">Hvis 3 bagels blev fjernet fra hylden eller solgt, vil denne værdi være -3.</span><span class="sxs-lookup"><span data-stu-id="01020-292">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="01020-293">Datakilden til de dimensioner, der bruges i bogføring af ændringshændelsen og forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="01020-293">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="01020-294">Hvis du angiver datakilden, kan du bruge de brugerdefinerede dimensioner fra den angivne datakilde.</span><span class="sxs-lookup"><span data-stu-id="01020-294">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="01020-295">Med dimensionskonfigurationen kan Lagersynlighed knytte de tilpassede dimensioner til de generelle standarddimensioner.</span><span class="sxs-lookup"><span data-stu-id="01020-295">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="01020-296">Hvis `dimensionDataSource` ikke er angivet, kan du kun bruge de generelle standarddimensioner i forespørgslerne.</span><span class="sxs-lookup"><span data-stu-id="01020-296">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="01020-297">En dynamisk pose med nøgle/værdi-par.</span><span class="sxs-lookup"><span data-stu-id="01020-297">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="01020-298">De vil blive knyttet til nogle af dimensionerne i Supply Chain Management, men du kan også tilføje brugerdefinerede dimensioner (som f.eks. *Kilde*), der kan angive, om hændelsen kommer fra Supply Chain Management eller et eksternt system.</span><span class="sxs-lookup"><span data-stu-id="01020-298">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="01020-299">Forespørgsel på aktuel disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="01020-299">Querying current on-hand</span></span>

<span data-ttu-id="01020-300">Slutpunktet for forespørgsel på den aktuelle disponible lagerbeholdning vil have en lignende URL-adresse:</span><span class="sxs-lookup"><span data-stu-id="01020-300">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="01020-301">Den vil blive forespurgt efter HTTP-`POST`-metoden.</span><span class="sxs-lookup"><span data-stu-id="01020-301">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="01020-302">Forespørgsel på aktuel disponibel lagerbeholdning, eksempel 1</span><span class="sxs-lookup"><span data-stu-id="01020-302">Current on-hand query example 1</span></span>

<span data-ttu-id="01020-303">I dette eksempel vises et scenario, hvor du allerede har fuldført dimensionskonfigurationen i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="01020-303">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="01020-304">Brug følgende forespørgsel til at konfigurere dimensionstilknytningen i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="01020-304">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="01020-305">Nu kan du angive `dimensionDataSource` og bruge brugerdefinerede dimensioner i forespørgslerne.</span><span class="sxs-lookup"><span data-stu-id="01020-305">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="01020-306">Systemet vil automatisk konvertere brugerdefinerede dimensioner til basisdimensioner.</span><span class="sxs-lookup"><span data-stu-id="01020-306">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="01020-307">Du kan angive `DimensionDataSource` i `filters` og angive brugerdefinerede dimensioner i både `filters` og `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="01020-307">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="01020-308">Systemet vil automatisk konvertere brugerdefinerede dimensioner til basisdimensioner.</span><span class="sxs-lookup"><span data-stu-id="01020-308">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="01020-309">Forespørgsel på aktuel disponibel lagerbeholdning, eksempel 2</span><span class="sxs-lookup"><span data-stu-id="01020-309">Current on-hand query example 2</span></span>

<span data-ttu-id="01020-310">I dette eksempel vises et scenario, hvor der ikke er konfigureret tilknytninger for dimensionskonfigurationen i Power Apps, så bogføringen skal også bruge basisdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="01020-310">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="01020-311">Alle dimensioner skal være basisdimensioner, når `dimensionDataSource`-feltet under `filters` er null, tomt eller blanktegn.</span><span class="sxs-lookup"><span data-stu-id="01020-311">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="01020-312">Eksempel på returnering af resultat</span><span class="sxs-lookup"><span data-stu-id="01020-312">Example return result</span></span>

<span data-ttu-id="01020-313">De forespørgsler, der vises i de foregående eksempler, kunne returnere et resultat som dette.</span><span class="sxs-lookup"><span data-stu-id="01020-313">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="01020-314">Bemærk, at antalsfelterne er struktureret som en ordbog med målinger og deres tilknyttede værdier.</span><span class="sxs-lookup"><span data-stu-id="01020-314">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
