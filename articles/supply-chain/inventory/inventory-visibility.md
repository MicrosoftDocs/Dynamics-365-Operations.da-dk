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
ms.openlocfilehash: 4e588be2ac5aae395ca66e3c9a743a67d71db7c0
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574216"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="6d3cb-103">Tilføjelsesprogrammet Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="6d3cb-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="6d3cb-104">Tilføjelsesprogrammet Lagersynlighed er en uafhængig og meget skalerbar mikrotjeneste, der gør det muligt at registrere disponibel lagerbeholdning i realtid, hvilket giver en global visning af lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="6d3cb-105">Alle oplysninger, der vedrører disponibel lagerbeholdning, eksporteres for tjenesten næsten i realtid via SQL-integration på lavt niveau.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="6d3cb-106">Eksterne systemer får adgang til tjenesten via RESTful-API'er for at forespørge på disponible oplysninger om bestemte sæt dimensioner, så der hentes en liste over tilgængelige disponible positioner.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="6d3cb-107">Lagersynlighed er en mikrotjeneste, der bygger på Microsoft Dataverse, hvilket betyder, at du kan udvide den ved at opbygge Power Apps og anvende Power BI for at levere brugerdefinerede funktioner, der opfylder virksomhedens behov.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="6d3cb-108">Du kan også opgradere indekset for at foretage lagerforespørgsler.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="6d3cb-109">Lagersynlighed angiver konfigurationsindstillinger, så den kan integreres med flere tredjepartssystemer.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="6d3cb-110">Den understøtter den standardiserede lagerdimension, tilpassede udvidelsesmuligheder og standardiserede, beregnede antal, der kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="6d3cb-111">Dette emne beskriver, hvordan du installerer og konfigurerer tilføjelsesprogrammet Lagersynlighed til Dynamics 365 Supply Chain Management, og hvordan du bruger dets API (Application Programming Interface).</span><span class="sxs-lookup"><span data-stu-id="6d3cb-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="6d3cb-112">Installere tilføjelsesprogrammet Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="6d3cb-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="6d3cb-113">Du skal installere tilføjelsesprogrammet Lagersynlighed ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6d3cb-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="6d3cb-114">LCS er en samarbejdsportal, der leverer et miljø og et sæt regelmæssigt opdaterede tjenester, der hjælper dig med at administrere programlivscyklussen for dine Dynamics 365 Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="6d3cb-115">Yderligere oplysninger finder du i [Ressourcer til Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="6d3cb-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="6d3cb-116">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="6d3cb-116">Prerequisites</span></span>

<span data-ttu-id="6d3cb-117">Før du installerer tilføjelsesprogrammet Lagersynlighed, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="6d3cb-118">Få et LCS-implementeringsprojekt med mindst ét miljø installeret.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="6d3cb-119">Kontrollér, at forudsætningerne for opsætning af tilføjelsesprogrammer, der er angivet i [oversigten over tilføjelsesprogrammer](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md), er fuldført.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="6d3cb-120">Lagersynlighed kræver ikke sammenkædning af dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="6d3cb-121">Kontakt teamet for lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for at få følgende tre krævede filer:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="6d3cb-122">`Inventory Visibility Integration.zip` (hvis den version af Supply Chain Management, du kører, er tidligere end version 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="6d3cb-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>

> [!NOTE]
> <span data-ttu-id="6d3cb-123">De lande og områder, der i øjeblikket understøttes, omfatter Canada, USA og EU.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-123">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="6d3cb-124">Hvis du har spørgsmål om disse forudsætninger, skal du kontakte produktteamet for Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-124">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="6d3cb-125">Konfigurere Dataverse</span><span class="sxs-lookup"><span data-stu-id="6d3cb-125">Set up Dataverse</span></span>

<span data-ttu-id="6d3cb-126">Gør følgende for at konfigurere Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-126">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="6d3cb-127">Føj et serviceprincip til lejeren:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-127">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="6d3cb-128">Installer Azure AD PowerShell-modul v2 som beskrevet i [Installere Azure Active Directory PowerShell til Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="6d3cb-128">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="6d3cb-129">Kør følgende PowerShell-kommando.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-129">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="6d3cb-130">Opret en programbruger til lagersynlighed i Dataverse:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-130">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="6d3cb-131">Åbn URL-adressen til dit Dataverse-miljø.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-131">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="6d3cb-132">Gå til **Avancerede indstillinger \> System \> Sikkerhed \> Brugere**, og opret en programbruger.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-132">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="6d3cb-133">Brug menuen Vis til at ændre sidevisningen til **Applikationsbrugere**.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-133">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="6d3cb-134">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-134">Select **New**.</span></span> <span data-ttu-id="6d3cb-135">Indstil program-id til *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-135">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="6d3cb-136">(Objekt-id'et indlæses automatisk, når du gemmer ændringerne). Du kan tilpasse navnet.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-136">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="6d3cb-137">Du kan f.eks. ændre det til *Lagsynlighed*.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-137">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="6d3cb-138">Vælg **Gem**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-138">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="6d3cb-139">Vælg **Tildel rolle**, og vælg derefter **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-139">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="6d3cb-140">Hvis der er en rolle med navnet **Common Data Service Bruger**, skal du også vælge den.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-140">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="6d3cb-141">Du kan finde flere oplysninger under [Oprette en programbruger](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="6d3cb-141">For more information, see [Create an application user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="6d3cb-142">Importér `Inventory Visibility Dataverse Solution.zip`-filen, der indeholder Dataverse-konfigurationsrelaterede enheder, og Power Apps:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-142">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="6d3cb-143">Gå til siden **Løsninger**.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-143">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="6d3cb-144">Vælg **Importér**.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-144">Select **Import**.</span></span>

1. <span data-ttu-id="6d3cb-145">Importér udløserflowet for konfigurationsopgradering:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-145">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="6d3cb-146">Gå til siden Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-146">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="6d3cb-147">Kontrollér, at forbindelsen med navnet *Dataverse (ældre)* findes.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-147">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="6d3cb-148">(Hvis den ikke findes, skal du oprette den).</span><span class="sxs-lookup"><span data-stu-id="6d3cb-148">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="6d3cb-149">Importér filen `Inventory Visibility Configuration Trigger.zip`.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-149">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="6d3cb-150">Når den er importeret, vises udløseren under **Mine flow**.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-150">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="6d3cb-151">Start følgende fire variabler på basis af miljøoplysningerne:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-151">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="6d3cb-152">Azure-lejer-id</span><span class="sxs-lookup"><span data-stu-id="6d3cb-152">Azure Tenant ID</span></span>
        - <span data-ttu-id="6d3cb-153">Azure-programklient-id</span><span class="sxs-lookup"><span data-stu-id="6d3cb-153">Azure Application Client ID</span></span>
        - <span data-ttu-id="6d3cb-154">Azure-programklienthemmelighed</span><span class="sxs-lookup"><span data-stu-id="6d3cb-154">Azure Application Client Secret</span></span>
        - <span data-ttu-id="6d3cb-155">Slutpunkt for lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="6d3cb-155">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="6d3cb-156">Du kan finde flere oplysninger om denne variabel under [Konfigurere integration af lagersynlighed](#setup-inventory-visibility-integration) senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-156">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="6d3cb-157">![Konfigurationsudløser](media/configuration-trigger.png "Konfigurationsudløser")</span><span class="sxs-lookup"><span data-stu-id="6d3cb-157">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="6d3cb-158">Vælg **Slå til**.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-158">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="6d3cb-159">Installer tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="6d3cb-159">Install the add-in</span></span>

<span data-ttu-id="6d3cb-160">For at installere tilføjelsesprogrammet Lagersynlighed skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-160">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="6d3cb-161">Log på portalen [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="6d3cb-161">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="6d3cb-162">Vælg det projekt, dit miljø skal implementeres i, på startsiden.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-162">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="6d3cb-163">Vælg det miljø, som tilføjelsesprogrammet skal installeres i, på projektsiden.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-163">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="6d3cb-164">Rul ned på miljøsiden, indtil du ser afsnittet **Miljøtilføjelsesprogrammer** i sektionen **Power Platform-integration**, hvor du kan finde Dataverse-miljønavnet.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-164">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="6d3cb-165">Vælg **Installér et nyt tilføjelsesprogram** i afsnittet **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-165">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="6d3cb-166">![Miljøsiden i LCS](media/inventory-visibility-environment.png "Miljøsiden i LCS")</span><span class="sxs-lookup"><span data-stu-id="6d3cb-166">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="6d3cb-167">Vælg linket **Installer et nyt tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-167">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="6d3cb-168">Der åbnes en liste over tilgængelige tilføjelsesprogrammer.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-168">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="6d3cb-169">Vælg **Lagersynlighed** på listen.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-169">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="6d3cb-170">Angiv værdier for følgende felter til dit miljø:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-170">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="6d3cb-171">**AAD-program-id (klient)**</span><span class="sxs-lookup"><span data-stu-id="6d3cb-171">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="6d3cb-172">**AAD-lejer-id**</span><span class="sxs-lookup"><span data-stu-id="6d3cb-172">**AAD tenant ID**</span></span>

    <span data-ttu-id="6d3cb-173">![Konfigurationsside for tilføjelsesprogram](media/inventory-visibility-setup.png "Konfigurationsside for tilføjelsesprogram")</span><span class="sxs-lookup"><span data-stu-id="6d3cb-173">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="6d3cb-174">Acceptér vilkårene og betingelsen ved at markere afkrydsningsfeltet **Vilkår og betingelser**.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-174">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="6d3cb-175">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-175">Select **Install**.</span></span> <span data-ttu-id="6d3cb-176">Status for tilføjelsesprogrammet vil blive vist som **installerer**.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-176">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="6d3cb-177">Når det er gjort, skal du opdatere siden for at se statusændringen til **Installeret**.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-177">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="6d3cb-178">Fjern tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="6d3cb-178">Uninstall the add-in</span></span>

<span data-ttu-id="6d3cb-179">Hvis du vil fjerne tilføjelsesprogrammet, skal du vælge **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-179">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="6d3cb-180">Når du opdaterer LCS, fjernes tilføjelsesprogrammet Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-180">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="6d3cb-181">Fjernelsesprocessen fjerner registreringen af tilføjelsesprogrammet og starter også et job for at rydde op i alle de forretningsdata, der er gemt i tjenesten.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-181">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="6d3cb-182">Forbruge data i den tilgængelige lagerbeholdning fra Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6d3cb-182">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="6d3cb-183">Implementere integrationspakken Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="6d3cb-183">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="6d3cb-184">Hvis du kører Supply Chain Management version 10.0.17 eller tidligere, skal du kontakte supportteamet for onboarding af lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for at hente pakkefilen.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-184">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="6d3cb-185">Implementer derefter pakken i LCS.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-185">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="6d3cb-186">Hvis der opstår uoverensstemmelse mellem versioner under installationen, skal du importere projektet X++ manuelt til udviklingsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-186">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="6d3cb-187">Opret derefter implementeringspakken i udviklingsmiljøet, og implementer den i produktionsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-187">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="6d3cb-188">Koden er inkluderet i Supply Chain Management version 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-188">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="6d3cb-189">Hvis du kører denne version eller en senere, er det ikke påkrævet.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-189">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="6d3cb-190">Sørg for, at følgende funktioner er aktiveret i dit Supply Chain Management-miljø.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-190">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="6d3cb-191">(Som standard er de aktiveret).</span><span class="sxs-lookup"><span data-stu-id="6d3cb-191">(By default, they are turned on.)</span></span>

| <span data-ttu-id="6d3cb-192">Funktionsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="6d3cb-192">Feature description</span></span> | <span data-ttu-id="6d3cb-193">Kodeversion</span><span class="sxs-lookup"><span data-stu-id="6d3cb-193">Code version</span></span> | <span data-ttu-id="6d3cb-194">Skifte klasse</span><span class="sxs-lookup"><span data-stu-id="6d3cb-194">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="6d3cb-195">Aktivere eller deaktivere ved hjælp af lagerdimensioner i tabellen InventSum</span><span class="sxs-lookup"><span data-stu-id="6d3cb-195">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="6d3cb-196">10.0.11</span><span class="sxs-lookup"><span data-stu-id="6d3cb-196">10.0.11</span></span> | <span data-ttu-id="6d3cb-197">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="6d3cb-197">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="6d3cb-198">Aktivere eller deaktivere ved hjælp af lagerdimensioner i tabellen InventSumDelta</span><span class="sxs-lookup"><span data-stu-id="6d3cb-198">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="6d3cb-199">10.0.12</span><span class="sxs-lookup"><span data-stu-id="6d3cb-199">10.0.12</span></span> | <span data-ttu-id="6d3cb-200">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="6d3cb-200">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="6d3cb-201">Konfigurer integration af lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="6d3cb-201">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="6d3cb-202">I Supply Chain Management skal du åbne arbejdsområdet **[Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og aktivere funktionen **Integration af lagersynlighed**.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-202">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="6d3cb-203">Gå til **Lagerstyring \> Konfiguration \> Parametre for integration af lagersynlighed**, og angiv URL-adressen for det miljø, hvor du kører lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-203">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="6d3cb-204">Find LCS-miljøets Azure-område, og angiv derefter URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-204">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="6d3cb-205">URL-adressen har følgende format:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-205">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="6d3cb-206">Hvis du f.eks. er i Europa, har dit miljø en af følgende URL-adresser:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-206">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="6d3cb-207">Følgende områder er tilgængelige i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-207">The following regions are currently available.</span></span>

    | <span data-ttu-id="6d3cb-208">Azure-region</span><span class="sxs-lookup"><span data-stu-id="6d3cb-208">Azure region</span></span> | <span data-ttu-id="6d3cb-209">Områdets korte navn</span><span class="sxs-lookup"><span data-stu-id="6d3cb-209">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="6d3cb-210">Det østlige Australien</span><span class="sxs-lookup"><span data-stu-id="6d3cb-210">Australia east</span></span> | <span data-ttu-id="6d3cb-211">eau</span><span class="sxs-lookup"><span data-stu-id="6d3cb-211">eau</span></span> |
    | <span data-ttu-id="6d3cb-212">Det sydøstlige Australien</span><span class="sxs-lookup"><span data-stu-id="6d3cb-212">Australia southeast</span></span> | <span data-ttu-id="6d3cb-213">seau</span><span class="sxs-lookup"><span data-stu-id="6d3cb-213">seau</span></span> |
    | <span data-ttu-id="6d3cb-214">Det centrale Canada</span><span class="sxs-lookup"><span data-stu-id="6d3cb-214">Canada central</span></span> | <span data-ttu-id="6d3cb-215">cca</span><span class="sxs-lookup"><span data-stu-id="6d3cb-215">cca</span></span> |
    | <span data-ttu-id="6d3cb-216">Det østlige Canada</span><span class="sxs-lookup"><span data-stu-id="6d3cb-216">Canada east</span></span> | <span data-ttu-id="6d3cb-217">eca</span><span class="sxs-lookup"><span data-stu-id="6d3cb-217">eca</span></span> |
    | <span data-ttu-id="6d3cb-218">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="6d3cb-218">North Europe</span></span> | <span data-ttu-id="6d3cb-219">neu</span><span class="sxs-lookup"><span data-stu-id="6d3cb-219">neu</span></span> |
    | <span data-ttu-id="6d3cb-220">Vesteuropa</span><span class="sxs-lookup"><span data-stu-id="6d3cb-220">West Europe</span></span> | <span data-ttu-id="6d3cb-221">weu</span><span class="sxs-lookup"><span data-stu-id="6d3cb-221">weu</span></span> |
    | <span data-ttu-id="6d3cb-222">Det østlige USA</span><span class="sxs-lookup"><span data-stu-id="6d3cb-222">East US</span></span> | <span data-ttu-id="6d3cb-223">eus</span><span class="sxs-lookup"><span data-stu-id="6d3cb-223">eus</span></span> |
    | <span data-ttu-id="6d3cb-224">Det vestlige USA</span><span class="sxs-lookup"><span data-stu-id="6d3cb-224">West US</span></span> | <span data-ttu-id="6d3cb-225">wus</span><span class="sxs-lookup"><span data-stu-id="6d3cb-225">wus</span></span> |

1. <span data-ttu-id="6d3cb-226">Gå til **Lagerstyring \> Periodisk \> Integration af lagersynlighed**, og aktivér jobbet.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-226">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="6d3cb-227">Alle hændelser med lagerændringer fra Supply Chain Management vil nu blive bogført i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-227">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="6d3cb-228">Den offentlige API for tilføjelsesprogrammet Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="6d3cb-228">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="6d3cb-229">Den offentlige REST-API til tilføjelsesprogrammet Lagersynlighed viser flere specifikke slutpunkter for integration.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-229">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="6d3cb-230">Det understøtter tre overordnede interaktionstyper:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-230">It supports three main interaction types:</span></span>

- <span data-ttu-id="6d3cb-231">Bogføring af ændret lagerbeholdning i tilføjelsesprogrammet fra et eksternt system</span><span class="sxs-lookup"><span data-stu-id="6d3cb-231">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="6d3cb-232">Forespørgsel om aktuelle disponible lagerantal fra et eksternt system</span><span class="sxs-lookup"><span data-stu-id="6d3cb-232">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="6d3cb-233">Automatisk synkronisering med lagerbeholdning i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6d3cb-233">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="6d3cb-234">Automatisk synkronisering er ikke en del af den offentlige API.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-234">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="6d3cb-235">Den håndteres i stedet i baggrunden for miljøer, hvor tilføjelsesprogrammet Lagersynlighed er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-235">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="6d3cb-236">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="6d3cb-236">Authentication</span></span>

<span data-ttu-id="6d3cb-237">Sikkerhedstoken til platformen bruges til at kalde tilføjelsesprogrammet Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-237">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="6d3cb-238">Du skal derfor generere et *Azure Active Directory-token (Azure AD)* ved hjælp af Azure AD-programmet.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-238">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="6d3cb-239">Du skal derefter bruge Azure AD-tokenet til at hente *adgangstoken* fra sikkerhedstjenesten.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-239">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="6d3cb-240">Få et token til sikkerhedsservice ved at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-240">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="6d3cb-241">Log på Azure-portalen, og brug den til at finde `clientId` og `clientSecret` til din Supply Chain Management-applikation.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-241">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="6d3cb-242">Hent et Azure Active Directory-token (`aadToken`) ved at sende en HTTP-anmodning med følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-242">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="6d3cb-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="6d3cb-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="6d3cb-244">**metode** - `GET`</span><span class="sxs-lookup"><span data-stu-id="6d3cb-244">**Method** - `GET`</span></span>
    - <span data-ttu-id="6d3cb-245">**Brødtekst (formulardata)**:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-245">**Body content (form data)**:</span></span>

        | <span data-ttu-id="6d3cb-246">nøgle</span><span class="sxs-lookup"><span data-stu-id="6d3cb-246">key</span></span> | <span data-ttu-id="6d3cb-247">værdi</span><span class="sxs-lookup"><span data-stu-id="6d3cb-247">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="6d3cb-248">client_id</span><span class="sxs-lookup"><span data-stu-id="6d3cb-248">client_id</span></span> | <span data-ttu-id="6d3cb-249">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="6d3cb-249">${aadAppId}</span></span> |
        | <span data-ttu-id="6d3cb-250">client_secret</span><span class="sxs-lookup"><span data-stu-id="6d3cb-250">client_secret</span></span> | <span data-ttu-id="6d3cb-251">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="6d3cb-251">${aadAppSecret}</span></span> |
        | <span data-ttu-id="6d3cb-252">grant_type</span><span class="sxs-lookup"><span data-stu-id="6d3cb-252">grant_type</span></span> | <span data-ttu-id="6d3cb-253">client_credentials</span><span class="sxs-lookup"><span data-stu-id="6d3cb-253">client_credentials</span></span> |
        | <span data-ttu-id="6d3cb-254">ressource</span><span class="sxs-lookup"><span data-stu-id="6d3cb-254">resource</span></span> | <span data-ttu-id="6d3cb-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="6d3cb-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="6d3cb-256">Du modtager et `aadToken` i svaret, der ligner følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-256">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="6d3cb-257">Formuler en JSON-anmodning, der ligner følgende:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-257">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="6d3cb-258">Placering:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-258">Where:</span></span>
    - <span data-ttu-id="6d3cb-259">Værdien `client_assertion` skal være det `aadToken`, du har modtaget i det forrige trin.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-259">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="6d3cb-260">Værdien `context` skal være det miljø-id, hvor du vil implementere tilføjelsesprogrammet.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-260">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="6d3cb-261">Angiv alle andre værdier som vist i eksemplet.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-261">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="6d3cb-262">Send en HTTP-anmodning med følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-262">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="6d3cb-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="6d3cb-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="6d3cb-264">**metode** - `POST`</span><span class="sxs-lookup"><span data-stu-id="6d3cb-264">**Method** - `POST`</span></span>
    - <span data-ttu-id="6d3cb-265">**HTTP-overskrift** – Medtag API-versionen (nøglen er `Api-Version`, og værdien er `1.0`)</span><span class="sxs-lookup"><span data-stu-id="6d3cb-265">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="6d3cb-266">**Brødtekst** – Medtag den JSON-anmodning, du oprettede i det forrige trin.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-266">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="6d3cb-267">Du vil få et `access_token` i svaret.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-267">You will get an `access_token` in response.</span></span> <span data-ttu-id="6d3cb-268">Det skal du bruge som ihændehavertoken for at kalde Lagersynlighed-API'et.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-268">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="6d3cb-269">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-269">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="6d3cb-270">Konfigurere API'et til Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="6d3cb-270">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="6d3cb-271">Før du bruger tjenesten, skal du udføre de konfigurationer, der er beskrevet i følgende underafsnit.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-271">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="6d3cb-272">Konfigurationen kan variere afhængigt af detaljerne i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-272">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="6d3cb-273">Den består primært af fire dele:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-273">It primarily includes four parts:</span></span>

- [<span data-ttu-id="6d3cb-274">Partitionering</span><span class="sxs-lookup"><span data-stu-id="6d3cb-274">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="6d3cb-275">Dimensionskonfigurationer</span><span class="sxs-lookup"><span data-stu-id="6d3cb-275">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="6d3cb-276">Indeksering</span><span class="sxs-lookup"><span data-stu-id="6d3cb-276">Indexing</span></span>](#indexing)
- [<span data-ttu-id="6d3cb-277">Brugerdefineret måling</span><span class="sxs-lookup"><span data-stu-id="6d3cb-277">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="6d3cb-278">Partitionering</span><span class="sxs-lookup"><span data-stu-id="6d3cb-278">Partitioning</span></span>

<span data-ttu-id="6d3cb-279">Partitionering kan have stor indflydelse på ydeevnen af Lagersynlighed-API'et.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-279">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="6d3cb-280">Det er en god ide at definere et skema, der giver mulighed for mindre gruppering af data, mens det stadig er muligt at give meningsfulde dataforespørgsler.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-280">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="6d3cb-281">Elementet `organizationId` (`dataAreaId` i Supply Chain Management) vil altid være en del af partitionen, og Lagersynlighede er som standard angivet til at partitionere efter dimensioner som *Sted + lokation*.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-281">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="6d3cb-282">Det betyder, at der altid skal sendes forespørgsler til tjenesten med de dimensioner, der er defineret på filtrene.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-282">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="6d3cb-283">*Sted* og *Lokation* er to generelle standarddimensioner i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-283">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="6d3cb-284">I Supply Chain Management kaldes disse dimensioner *Sted* (`InventSiteId`) og *Lagersted* (`InventLocationId`).</span><span class="sxs-lookup"><span data-stu-id="6d3cb-284">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="6d3cb-285">Dimensionskonfigurationer</span><span class="sxs-lookup"><span data-stu-id="6d3cb-285">Dimension configurations</span></span>

<span data-ttu-id="6d3cb-286">Lagersynlighed vil indeholde en liste over generelle standarddimensioner, der gør det muligt at integrere flere kildesystemer.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-286">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="6d3cb-287">I følgende tabel vises de lagerdimensioner, der vil være standarddimensionsnavne i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-287">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="6d3cb-288">Dimensionstype</span><span class="sxs-lookup"><span data-stu-id="6d3cb-288">Dimension type</span></span> | <span data-ttu-id="6d3cb-289">Dimensionens navn</span><span class="sxs-lookup"><span data-stu-id="6d3cb-289">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="6d3cb-290">Produkt</span><span class="sxs-lookup"><span data-stu-id="6d3cb-290">Product</span></span> | `ColorId` |
| <span data-ttu-id="6d3cb-291">Produkt</span><span class="sxs-lookup"><span data-stu-id="6d3cb-291">Product</span></span> | `SizeId` |
| <span data-ttu-id="6d3cb-292">Produkt</span><span class="sxs-lookup"><span data-stu-id="6d3cb-292">Product</span></span> | `StyleId` |
| <span data-ttu-id="6d3cb-293">Produkt</span><span class="sxs-lookup"><span data-stu-id="6d3cb-293">Product</span></span> | `ConfigId` |
| <span data-ttu-id="6d3cb-294">Sporing</span><span class="sxs-lookup"><span data-stu-id="6d3cb-294">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="6d3cb-295">Sporing</span><span class="sxs-lookup"><span data-stu-id="6d3cb-295">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="6d3cb-296">Adresse</span><span class="sxs-lookup"><span data-stu-id="6d3cb-296">Location</span></span> | `LocationId` |
| <span data-ttu-id="6d3cb-297">Adresse</span><span class="sxs-lookup"><span data-stu-id="6d3cb-297">Location</span></span> | `SiteId` |
| <span data-ttu-id="6d3cb-298">Lagerstatus</span><span class="sxs-lookup"><span data-stu-id="6d3cb-298">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="6d3cb-299">Lagerstedsspecifik</span><span class="sxs-lookup"><span data-stu-id="6d3cb-299">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="6d3cb-300">Lagerstedsspecifik</span><span class="sxs-lookup"><span data-stu-id="6d3cb-300">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="6d3cb-301">Lagerstedsspecifik</span><span class="sxs-lookup"><span data-stu-id="6d3cb-301">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="6d3cb-302">Den dimensionstype, der er angivet i forrige tabel, er kun til reference.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-302">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="6d3cb-303">Du behøver ikke definere dimensionstypen i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-303">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="6d3cb-304">Hvis der findes en brugerdefineret dimension, som skal overføres til en standardværdi, når den forbruges af Lagersynlighed, kan du konfigurere navnet **Brugerdefineret dimension** i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-304">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="6d3cb-305">Eksterne systemer får adgang til Lagersynlighed gennem RESTful API'er, der muliggør disponible oplysninger om bestemte sæt dimensioner, der skal forespørges.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-305">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="6d3cb-306">I forbindelse med integrationen giver Lagersynlighed dig mulighed for at konfigurere den *eksterne kanals datakilde* og kildedimensionen til *måldimensionerne* i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-306">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="6d3cb-307">Måldimensionerne skal være en af følgende:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-307">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="6d3cb-308">Standarddimensioner i Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="6d3cb-308">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="6d3cb-309">Brugerdefinerede dimensioner</span><span class="sxs-lookup"><span data-stu-id="6d3cb-309">Custom dimensions</span></span>

<span data-ttu-id="6d3cb-310">Formålet med dimensionskonfiguration er at standardisere integrationen af flere systemer til forespørgslen på dimensioner og bogføringshændelsen med dimensioner.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-310">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="6d3cb-311">Indeksering</span><span class="sxs-lookup"><span data-stu-id="6d3cb-311">Indexing</span></span>

<span data-ttu-id="6d3cb-312">I de fleste tilfælde vil lagerbeholdningsforespørgslen ikke kun være på det højeste "totale" niveau, men du ønsker måske at se de samlede resultater på baggrund af lagerdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-312">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="6d3cb-313">Lagersynlighed giver fleksibilitet, fordi du kan konfigurere de indekser, der er baseret på dimensionen eller kombinationen af dimensionerne.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-313">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="6d3cb-314">I øjeblikket kan du kun konfigurere indekser til maksimalt fem.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-314">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="6d3cb-315">Du skal nøje overveje, hvilken dimension eller dimensionskombination du vil bruge før implementeringen for at sikre, at den opfylder dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-315">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="6d3cb-316">Hvis du f.eks. vil forespørge på produkter på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-316">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="6d3cb-317">Forespørg på den samlede disponible beholdning via *Farve*- og *Størrelse*-dimensionerne.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-317">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="6d3cb-318">I nogle tilfælde vil du kun forespørge på produktet i alt.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-318">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="6d3cb-319">Du skal have defineret to indekser som følgende:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-319">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="6d3cb-320">Den tomme kantede parentes samles på basis af produkt-id'et i partitionen.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-320">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="6d3cb-321">Indekseringen definerer, hvordan du kan gruppere resultaterne baseret på `groupBy`-forespørgselsindstillingen.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-321">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="6d3cb-322">Hvis du ikke definerer `groupBy`-værdier, får du totaler med `productid`.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-322">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="6d3cb-323">Hvis du definerer `groupBy` som `groupBy=ColorId&groupBy=SizeId`, får du ellers flere linjer baseret på de forskellige kombinationer af farve og størrelse i systemet.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-323">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="6d3cb-324">Du kan sætte dine forespørgselskriterier i anmodningsteksten.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-324">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="6d3cb-325">Her er et eksempel på en forespørgsel på produktet med en kombination af farve og størrelse.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-325">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="6d3cb-326">Brugerdefineret måling</span><span class="sxs-lookup"><span data-stu-id="6d3cb-326">Custom measurement</span></span>

<span data-ttu-id="6d3cb-327">Standardmåleantallet er kædet sammen med Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-327">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="6d3cb-328">Det kan dog være en god ide at have et antal, der består af en kombination af standardmålene.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-328">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="6d3cb-329">Hvis du vil gøre dette, kan du have en konfiguration af brugerdefinerede antal, der føjes til outputtet af forespørgsler på den disponible lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-329">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="6d3cb-330">Denne funktion giver dig mulighed for at definere et sæt målinger, der skal tilføjes, og/eller et sæt målinger, der skal trækkes fra, så de danner den brugerdefinerede måling.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-330">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="6d3cb-331">I følgende forespørgselsbetingelse skal du f.eks. konfigurere det brugerdefinerede måleanta som `MyCustomAvailableforReservation`, der skal forbruges af forbrugssystemet.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-331">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="6d3cb-332">Forbrugssystem</span><span class="sxs-lookup"><span data-stu-id="6d3cb-332">Consumption system</span></span> | <span data-ttu-id="6d3cb-333">Beregnede målinger</span><span class="sxs-lookup"><span data-stu-id="6d3cb-333">Calculated measurers</span></span> | <span data-ttu-id="6d3cb-334">Datakilde</span><span class="sxs-lookup"><span data-stu-id="6d3cb-334">Data source</span></span> | <span data-ttu-id="6d3cb-335">Modifikator</span><span class="sxs-lookup"><span data-stu-id="6d3cb-335">Modifier</span></span> | <span data-ttu-id="6d3cb-336">Modifikator som beregningstype</span><span class="sxs-lookup"><span data-stu-id="6d3cb-336">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="6d3cb-337">Addition</span><span class="sxs-lookup"><span data-stu-id="6d3cb-337">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="6d3cb-338">Addition</span><span class="sxs-lookup"><span data-stu-id="6d3cb-338">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="6d3cb-339">Subtraktion</span><span class="sxs-lookup"><span data-stu-id="6d3cb-339">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="6d3cb-340">Addition</span><span class="sxs-lookup"><span data-stu-id="6d3cb-340">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="6d3cb-341">Subtraktion</span><span class="sxs-lookup"><span data-stu-id="6d3cb-341">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="6d3cb-342">Addition</span><span class="sxs-lookup"><span data-stu-id="6d3cb-342">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="6d3cb-343">Addition</span><span class="sxs-lookup"><span data-stu-id="6d3cb-343">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="6d3cb-344">Subtraktion</span><span class="sxs-lookup"><span data-stu-id="6d3cb-344">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="6d3cb-345">Subtraktion</span><span class="sxs-lookup"><span data-stu-id="6d3cb-345">Subtraction</span></span> |

<span data-ttu-id="6d3cb-346">Med denne fremgangsmåde vil forespørgslen på det brugerdefinerede måleantal returnere følgende output.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-346">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="6d3cb-347">Outputtet `MyCustomAvailableforReservation` er baseret på beregningsindstillingen i de brugerdefinerede målinger som:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-347">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="6d3cb-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="6d3cb-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="6d3cb-349">Bogføring af ændret lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="6d3cb-349">Posting on-hand changes</span></span>

<span data-ttu-id="6d3cb-350">Den præcise URL-adresse, som hændelsen vil blive bogført til, afhænger af dit geografiske område.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-350">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="6d3cb-351">Den har formatet:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-351">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="6d3cb-352">Når denne URL-adresse er godkendt, kan den bruges sammen med HTTP-`POST`-metoden til at sende hændelser for beholdningsændring til tjenesten.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-352">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="6d3cb-353">En speciel header bruges til kommunikation med Dynamics 365-tjenester via HTTP-anmodninger, der angiver miljø-id'et for Supply Chain Management-forekomst, som dataene er kædet sammen med.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-353">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="6d3cb-354">F.eks.:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-354">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="6d3cb-355">Bogføring af forespørgsel på lagerbeholdningsændringer, eksempel 1</span><span class="sxs-lookup"><span data-stu-id="6d3cb-355">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="6d3cb-356">I dette eksempel vises et scenario, hvor du konfigurerer dimensionskonfigurationen i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-356">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="6d3cb-357">Brug følgende forespørgsel til at konfigurere dimensionstilknytningen i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-357">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="6d3cb-358">Nu kan du angive `dimensionDataSource` og bruge brugerdefinerede dimensioner i forespørgslerne.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-358">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="6d3cb-359">Systemet vil automatisk konvertere brugerdefinerede dimensioner til basisdimensioner.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-359">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="6d3cb-360">Bogføring af forespørgsel på lagerbeholdningsændringer, eksempel 2</span><span class="sxs-lookup"><span data-stu-id="6d3cb-360">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="6d3cb-361">I dette eksempel vises et scenario, hvor der ikke er konfigureret tilknytninger for dimensionskonfigurationen i Power Apps, så bogføringen skal også bruge basisdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-361">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="6d3cb-362">Alle dimensioner skal være basisdimensioner, når `dimensionDataSource`-feltet er null, tomt eller blanktegn.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-362">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="6d3cb-363">JSON-dokumentfeltegenskaber</span><span class="sxs-lookup"><span data-stu-id="6d3cb-363">JSON document field properties</span></span>

<span data-ttu-id="6d3cb-364">Felterne fra de JSON-forespørgselseksempler, der tidligere blev vist, har de egenskaber, der er angivet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-364">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="6d3cb-365">Felt-id</span><span class="sxs-lookup"><span data-stu-id="6d3cb-365">Field ID</span></span> | <span data-ttu-id="6d3cb-366">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6d3cb-366">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="6d3cb-367">Et entydigt id for den specifikke ændringshændelse.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-367">A unique ID for the specific change event.</span></span> <span data-ttu-id="6d3cb-368">Dette id bruges til at sikre, at hvis kommunikationen med tjenesten mislykkes under bogføring, vil genafsendelse af hændelsen ikke resultere i, at den samme hændelse tælles to gange i systemet.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-368">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="6d3cb-369">Identifikatoren for den organisation, der er knyttet til hændelsen.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-369">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="6d3cb-370">Dette knytter data til Supply Chain Management-organisationer eller dataområde-id'er.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-370">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="6d3cb-371">Produktets identifikator.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-371">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="6d3cb-372">Det antal, som lagerbeholdningen skal ændres med.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-372">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="6d3cb-373">Hvis der f.eks. er føjet 10 nye bagels til en hylde, vil denne værdi være 10.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-373">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="6d3cb-374">Hvis 3 bagels blev fjernet fra hylden eller solgt, vil denne værdi være -3.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-374">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="6d3cb-375">Datakilden til de dimensioner, der bruges i bogføring af ændringshændelsen og forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-375">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="6d3cb-376">Hvis du angiver datakilden, kan du bruge de brugerdefinerede dimensioner fra den angivne datakilde.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-376">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="6d3cb-377">Med dimensionskonfigurationen kan Lagersynlighed knytte de tilpassede dimensioner til de generelle standarddimensioner.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-377">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="6d3cb-378">Hvis `dimensionDataSource` ikke er angivet, kan du kun bruge de generelle standarddimensioner i forespørgslerne.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-378">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="6d3cb-379">En dynamisk pose med nøgle/værdi-par.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-379">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="6d3cb-380">De vil blive knyttet til nogle af dimensionerne i Supply Chain Management, men du kan også tilføje brugerdefinerede dimensioner (som f.eks. *Kilde*), der kan angive, om hændelsen kommer fra Supply Chain Management eller et eksternt system.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-380">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="6d3cb-381">Forespørgsel på aktuel disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="6d3cb-381">Querying current on-hand</span></span>

<span data-ttu-id="6d3cb-382">Slutpunktet for forespørgsel på den aktuelle disponible lagerbeholdning vil have en lignende URL-adresse:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-382">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="6d3cb-383">Den vil blive forespurgt efter HTTP-`POST`-metoden.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-383">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="6d3cb-384">Forespørgsel på aktuel disponibel lagerbeholdning, eksempel 1</span><span class="sxs-lookup"><span data-stu-id="6d3cb-384">Current on-hand query example 1</span></span>

<span data-ttu-id="6d3cb-385">I dette eksempel vises et scenario, hvor du allerede har fuldført dimensionskonfigurationen i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-385">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="6d3cb-386">Brug følgende forespørgsel til at konfigurere dimensionstilknytningen i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="6d3cb-386">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="6d3cb-387">Nu kan du angive `dimensionDataSource` og bruge brugerdefinerede dimensioner i forespørgslerne.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-387">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="6d3cb-388">Systemet vil automatisk konvertere brugerdefinerede dimensioner til basisdimensioner.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-388">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="6d3cb-389">Du kan angive `DimensionDataSource` i `filters` og angive brugerdefinerede dimensioner i både `filters` og `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-389">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="6d3cb-390">Systemet vil automatisk konvertere brugerdefinerede dimensioner til basisdimensioner.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-390">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="6d3cb-391">Forespørgsel på aktuel disponibel lagerbeholdning, eksempel 2</span><span class="sxs-lookup"><span data-stu-id="6d3cb-391">Current on-hand query example 2</span></span>

<span data-ttu-id="6d3cb-392">I dette eksempel vises et scenario, hvor der ikke er konfigureret tilknytninger for dimensionskonfigurationen i Power Apps, så bogføringen skal også bruge basisdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-392">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="6d3cb-393">Alle dimensioner skal være basisdimensioner, når `dimensionDataSource`-feltet under `filters` er null, tomt eller blanktegn.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-393">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="6d3cb-394">Eksempel på returnering af resultat</span><span class="sxs-lookup"><span data-stu-id="6d3cb-394">Example return result</span></span>

<span data-ttu-id="6d3cb-395">De forespørgsler, der vises i de foregående eksempler, kunne returnere et resultat som dette.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-395">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="6d3cb-396">Bemærk, at antalsfelterne er struktureret som en ordbog med målinger og deres tilknyttede værdier.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-396">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
