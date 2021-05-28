---
title: Tilføjelsesprogrammet Lagersynlighed
description: Dette emne beskriver, hvordan du installerer og konfigurerer tilføjelsesprogrammet Lagersynlighed til Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 84f5e949f0c81f840c8a9086d05bbcfc576e42aa
ms.sourcegitcommit: b67665ed689c55df1a67d1a7840947c3977d600c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6017000"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="3b370-103">Tilføjelsesprogrammet Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="3b370-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="3b370-104">Tilføjelsesprogrammet Lagersynlighed er en uafhængig og meget skalerbar mikrotjeneste, der gør det muligt at registrere disponibel lagerbeholdning i realtid, hvilket giver en global visning af lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="3b370-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="3b370-105">Alle oplysninger, der vedrører disponibel lagerbeholdning, eksporteres for tjenesten næsten i realtid via SQL-integration på lavt niveau.</span><span class="sxs-lookup"><span data-stu-id="3b370-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="3b370-106">Eksterne systemer får adgang til tjenesten via RESTful-API'er for at forespørge på disponible oplysninger om bestemte sæt dimensioner, så der hentes en liste over tilgængelige disponible positioner.</span><span class="sxs-lookup"><span data-stu-id="3b370-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="3b370-107">Lagersynlighed er en mikrotjeneste, der bygger på Microsoft Dataverse, hvilket betyder, at du kan udvide den ved at opbygge Power Apps og anvende Power BI for at levere brugerdefinerede funktioner, der opfylder virksomhedens behov.</span><span class="sxs-lookup"><span data-stu-id="3b370-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="3b370-108">Du kan også opgradere indekset for at foretage lagerforespørgsler.</span><span class="sxs-lookup"><span data-stu-id="3b370-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="3b370-109">Lagersynlighed angiver konfigurationsindstillinger, så den kan integreres med flere tredjepartssystemer.</span><span class="sxs-lookup"><span data-stu-id="3b370-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="3b370-110">Den understøtter den standardiserede lagerdimension, tilpassede udvidelsesmuligheder og standardiserede, beregnede antal, der kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="3b370-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="3b370-111">Dette emne beskriver, hvordan du installerer og konfigurerer tilføjelsesprogrammet Lagersynlighed til Dynamics 365 Supply Chain Management, og hvordan du bruger dets API (Application Programming Interface).</span><span class="sxs-lookup"><span data-stu-id="3b370-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="3b370-112">Installere tilføjelsesprogrammet Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="3b370-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="3b370-113">Du skal installere tilføjelsesprogrammet Lagersynlighed ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3b370-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="3b370-114">LCS er en samarbejdsportal, der leverer et miljø og et sæt regelmæssigt opdaterede tjenester, der hjælper dig med at administrere programlivscyklussen for dine Dynamics 365 Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="3b370-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="3b370-115">Yderligere oplysninger finder du i [Ressourcer til Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="3b370-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="inventory-visibility-add-in-prerequisites"></a><span data-ttu-id="3b370-116">Forudsætninger for tilføjelsesprogrammet Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="3b370-116">Inventory Visibility Add-in prerequisites</span></span>

<span data-ttu-id="3b370-117">Før du installerer tilføjelsesprogrammet Lagersynlighed, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="3b370-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="3b370-118">Få et LCS-implementeringsprojekt med mindst ét miljø installeret.</span><span class="sxs-lookup"><span data-stu-id="3b370-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="3b370-119">Kontrollér, at forudsætningerne for opsætning af tilføjelsesprogrammer, der er angivet i [oversigten over tilføjelsesprogrammer](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md), er fuldført.</span><span class="sxs-lookup"><span data-stu-id="3b370-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="3b370-120">Lagersynlighed kræver ikke sammenkædning af dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="3b370-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="3b370-121">Kontakt teamet for lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for at få følgende tre krævede filer:</span><span class="sxs-lookup"><span data-stu-id="3b370-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - <span data-ttu-id="3b370-122">`Inventory Visibility Integration.zip` (hvis den version af Supply Chain Management, du kører, er tidligere end version 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="3b370-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="3b370-123">Du kan også kontakte teamet for lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for at få Package Deployer-pakkerne.</span><span class="sxs-lookup"><span data-stu-id="3b370-123">Alternatively, contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package deployer packages.</span></span> <span data-ttu-id="3b370-124">Disse pakker kan bruges af et officielt Package Deployer-værktøj.</span><span class="sxs-lookup"><span data-stu-id="3b370-124">These packages can be used by an official package deployer tool.</span></span>
  - `InventoryServiceBase.PackageDeployer.zip`
  - <span data-ttu-id="3b370-125">`InventoryServiceApplication.PackageDeployer.zip` (denne pakke indeholder alle ændringerne i `InventoryServiceBase`-pakken samt yderligere komponenter til brugergrænsefladen)</span><span class="sxs-lookup"><span data-stu-id="3b370-125">`InventoryServiceApplication.PackageDeployer.zip` (this package contains all of the changes in the `InventoryServiceBase` package, plus additional UI application components)</span></span>
- <span data-ttu-id="3b370-126">Følg instruktionerne i [Hurtig start: Registrer et program med platformen Microsoft-identitet](/azure/active-directory/develop/quickstart-register-app) for at registrere et program og føje en klient til AAD under dit Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b370-126">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
  - [<span data-ttu-id="3b370-127">Registrere en applikation</span><span class="sxs-lookup"><span data-stu-id="3b370-127">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
  - [<span data-ttu-id="3b370-128">Tilføje en klienthemmelighed</span><span class="sxs-lookup"><span data-stu-id="3b370-128">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - <span data-ttu-id="3b370-129">**Program-id (klient)**, **Klienthemmelighed** og **Lejer-id** bruges i følgende trin.</span><span class="sxs-lookup"><span data-stu-id="3b370-129">The **Application(Client) Id**, **Client Secret**, and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="3b370-130">De lande og områder, der i øjeblikket understøttes, omfatter Canada, USA og EU.</span><span class="sxs-lookup"><span data-stu-id="3b370-130">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="3b370-131">Hvis du har spørgsmål om disse forudsætninger, skal du kontakte produktteamet for Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="3b370-131">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="3b370-132">Konfigurere Dataverse</span><span class="sxs-lookup"><span data-stu-id="3b370-132">Set up Dataverse</span></span>

<span data-ttu-id="3b370-133">Hvis du vil konfigurere Dataverse til brug med Lagersynlighed, skal du først forberede forudsætningerne og derefter beslutte, om du vil konfigurere Dataverse med Package Deployer-værktøjet eller ved manuelt at importere løsningerne (du behøver ikke at gøre begge dele).</span><span class="sxs-lookup"><span data-stu-id="3b370-133">To set up Dataverse for use with Inventory Visibility, you must first prepare the prerequisites and then decide whether to set up Dataverse using either the package deployer tool or by manually importing the solutions (you don't have to do both).</span></span> <span data-ttu-id="3b370-134">Installer derefter tilføjelsesprogrammet Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="3b370-134">Then install the Inventory Visibility Add-in.</span></span> <span data-ttu-id="3b370-135">I følgende underafsnit beskrives, hvordan du udfører hver af disse opgaver.</span><span class="sxs-lookup"><span data-stu-id="3b370-135">The following subsections describe how to complete each of these tasks.</span></span>

#### <a name="prepare-dataverse-prerequisites"></a><span data-ttu-id="3b370-136">Forberede Dataverse-forudsætninger</span><span class="sxs-lookup"><span data-stu-id="3b370-136">Prepare Dataverse prerequisites</span></span>

<span data-ttu-id="3b370-137">Før du begynder at konfigurere Dataverse, kan du føje et serviceprincip til din lejer på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="3b370-137">Before you start to set up Dataverse, add a service principle to your tenant by doing the following:</span></span>

1. <span data-ttu-id="3b370-138">Installer Azure AD PowerShell-modul v2 som beskrevet i [Installere Azure Active Directory PowerShell til Graph](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="3b370-138">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>

1. <span data-ttu-id="3b370-139">Kør følgende PowerShell-kommando:</span><span class="sxs-lookup"><span data-stu-id="3b370-139">Run the following PowerShell command:</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a><span data-ttu-id="3b370-140">Konfigurere Dataverse ved hjælp af Package Deployer-værktøjet</span><span class="sxs-lookup"><span data-stu-id="3b370-140">Set up Dataverse using the package deployer tool</span></span>

<span data-ttu-id="3b370-141">Når du har forudsætningerne på plads, skal du benytte følgende fremgangsmåde, hvis du foretrækker at konfigurere Dataverse ved hjælp af Package Deployer-værktøjet.</span><span class="sxs-lookup"><span data-stu-id="3b370-141">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse using the package deployer tool.</span></span> <span data-ttu-id="3b370-142">Se næste afsnit for at få oplysninger om, hvordan du importerer løsningerne manuelt i stedet (du skal ikke gøre begge dele).</span><span class="sxs-lookup"><span data-stu-id="3b370-142">See the next section for details about how to import the solutions manually instead (don't do both).</span></span>

1. <span data-ttu-id="3b370-143">Installer udviklerværktøjer som beskrevet i [Hent værktøjer fra NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).</span><span class="sxs-lookup"><span data-stu-id="3b370-143">Install developer tools as described in [Download tools from NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).</span></span>

1. <span data-ttu-id="3b370-144">Vælg `InventoryServiceBase`- eller `InventoryServiceApplication`-pakken ud fra dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="3b370-144">Based on your business requirements, choose the `InventoryServiceBase` or `InventoryServiceApplication` package.</span></span>

1. <span data-ttu-id="3b370-145">Importer løsningerne:</span><span class="sxs-lookup"><span data-stu-id="3b370-145">Import the solutions:</span></span>
    1. <span data-ttu-id="3b370-146">For `InventoryServiceBase`-pakken:</span><span class="sxs-lookup"><span data-stu-id="3b370-146">For the `InventoryServiceBase` package:</span></span>
        - <span data-ttu-id="3b370-147">Pak `InventoryServiceBase.PackageDeployer.zip` ud</span><span class="sxs-lookup"><span data-stu-id="3b370-147">Unzip `InventoryServiceBase.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="3b370-148">Find `InventoryServiceBase`-mappen, filen `[Content_Types].xml`, filen `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, filen `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` og filen `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`.</span><span class="sxs-lookup"><span data-stu-id="3b370-148">Find folder `InventoryServiceBase`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`.</span></span> 
        - <span data-ttu-id="3b370-149">Kopier hver af disse mapper og filer til den `.\Tools\PackageDeployment`-mappe, der blev oprettet, da du installerede udviklerværktøjerne.</span><span class="sxs-lookup"><span data-stu-id="3b370-149">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="3b370-150">For `InventoryServiceApplication`-pakken:</span><span class="sxs-lookup"><span data-stu-id="3b370-150">For the `InventoryServiceApplication` package:</span></span>
        - <span data-ttu-id="3b370-151">Pak `InventoryServiceApplication.PackageDeployer.zip` ud</span><span class="sxs-lookup"><span data-stu-id="3b370-151">Unzip `InventoryServiceApplication.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="3b370-152">Find `InventoryServiceApplication`-mappen, filen `[Content_Types].xml`, filen `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, filen `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` og filen `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.</span><span class="sxs-lookup"><span data-stu-id="3b370-152">Find folder `InventoryServiceApplication`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.</span></span>
        - <span data-ttu-id="3b370-153">Kopier hver af disse mapper og filer til den `.\Tools\PackageDeployment`-mappe, der blev oprettet, da du installerede udviklerværktøjerne.</span><span class="sxs-lookup"><span data-stu-id="3b370-153">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="3b370-154">Udfør `.\Tools\PackageDeployment\PackageDeployer.exe`.</span><span class="sxs-lookup"><span data-stu-id="3b370-154">Execute `.\Tools\PackageDeployment\PackageDeployer.exe`.</span></span> <span data-ttu-id="3b370-155">Følg instruktionerne på skærmen for at importere løsningerne.</span><span class="sxs-lookup"><span data-stu-id="3b370-155">Follow the instructions on your screen to import the solutions.</span></span>

1. <span data-ttu-id="3b370-156">Tildel sikkerhedsroller til programbrugeren.</span><span class="sxs-lookup"><span data-stu-id="3b370-156">Assign security roles to the application user.</span></span>
    1. <span data-ttu-id="3b370-157">Åbn URL-adressen til dit Dataverse-miljø.</span><span class="sxs-lookup"><span data-stu-id="3b370-157">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="3b370-158">Gå til **Avancerede indstillinger \> System \> Sikkerhed \> Brugere**, og find brugeren med navnet **# InventoryVisibility**.</span><span class="sxs-lookup"><span data-stu-id="3b370-158">Go to **Advanced Setting \> System \> Security \> Users**, and find user the named **# InventoryVisibility**.</span></span>
    1. <span data-ttu-id="3b370-159">Vælg **Tildel rolle**, og vælg derefter **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="3b370-159">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="3b370-160">Hvis der er en rolle med navnet **Common Data Service Bruger**, skal du også vælge den.</span><span class="sxs-lookup"><span data-stu-id="3b370-160">If there is a role that is named **Common Data Service User**, select it as well.</span></span>

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a><span data-ttu-id="3b370-161">Oprette Dataverse manuelt ved at importere løsninger</span><span class="sxs-lookup"><span data-stu-id="3b370-161">Set up Dataverse manually by importing solutions</span></span>

<span data-ttu-id="3b370-162">Når du har forudsætningerne på plads, skal du benytte følgende fremgangsmåde, hvis du foretrækker at konfigurere Dataverse ved at importere løsninger manuelt.</span><span class="sxs-lookup"><span data-stu-id="3b370-162">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse by manually importing solutions.</span></span> <span data-ttu-id="3b370-163">Se forrige afsnit for at få oplysninger om, hvordan du bruger Package Deployer-værktøjet i stedet (du skal ikke gøre begge dele).</span><span class="sxs-lookup"><span data-stu-id="3b370-163">See the previous section for details about how to use the package deployer tool instead (don't do both).</span></span>

1. <span data-ttu-id="3b370-164">Opret en programbruger til lagersynlighed i Dataverse:</span><span class="sxs-lookup"><span data-stu-id="3b370-164">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="3b370-165">Åbn URL-adressen til dit Dataverse-miljø.</span><span class="sxs-lookup"><span data-stu-id="3b370-165">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="3b370-166">Gå til **Avancerede indstillinger \> System \> Sikkerhed \> Brugere**, og opret en programbruger.</span><span class="sxs-lookup"><span data-stu-id="3b370-166">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="3b370-167">Brug menuen Vis til at ændre sidevisningen til **Applikationsbrugere**.</span><span class="sxs-lookup"><span data-stu-id="3b370-167">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="3b370-168">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3b370-168">Select **New**.</span></span> <span data-ttu-id="3b370-169">Indstil program-id til *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="3b370-169">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="3b370-170">(Objekt-id'et indlæses automatisk, når du gemmer ændringerne). Du kan tilpasse navnet.</span><span class="sxs-lookup"><span data-stu-id="3b370-170">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="3b370-171">Du kan f.eks. ændre det til *Lagsynlighed*.</span><span class="sxs-lookup"><span data-stu-id="3b370-171">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="3b370-172">Vælg **Gem**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="3b370-172">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="3b370-173">Vælg **Tildel rolle**, og vælg derefter **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="3b370-173">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="3b370-174">Hvis der er en rolle med navnet **Common Data Service Bruger**, skal du også vælge den.</span><span class="sxs-lookup"><span data-stu-id="3b370-174">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="3b370-175">Du kan finde flere oplysninger under [Oprette en programbruger](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="3b370-175">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="3b370-176">Hvis dit standardsprog for Dataverse ikke er **engelsk**:</span><span class="sxs-lookup"><span data-stu-id="3b370-176">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="3b370-177">Gå til **Avancerede indstillinger \> Administration \> Sprog**.</span><span class="sxs-lookup"><span data-stu-id="3b370-177">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="3b370-178">Vælg **Engelsk (LanguageCode=1033)**, og vælg **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="3b370-178">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="3b370-179">Importér `Inventory Visibility Dataverse Solution.zip`-filen, der indeholder Dataverse-konfigurationsrelaterede enheder, og Power Apps:</span><span class="sxs-lookup"><span data-stu-id="3b370-179">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="3b370-180">Gå til siden **Løsninger**.</span><span class="sxs-lookup"><span data-stu-id="3b370-180">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="3b370-181">Vælg **Importér**.</span><span class="sxs-lookup"><span data-stu-id="3b370-181">Select **Import**.</span></span>

1. <span data-ttu-id="3b370-182">Importér udløserflowet for konfigurationsopgradering:</span><span class="sxs-lookup"><span data-stu-id="3b370-182">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="3b370-183">Gå til siden Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="3b370-183">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="3b370-184">Kontrollér, at forbindelsen med navnet *Dataverse (ældre)* findes.</span><span class="sxs-lookup"><span data-stu-id="3b370-184">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="3b370-185">(Hvis den ikke findes, skal du oprette den).</span><span class="sxs-lookup"><span data-stu-id="3b370-185">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="3b370-186">Importér filen `Inventory Visibility Configuration Trigger.zip`.</span><span class="sxs-lookup"><span data-stu-id="3b370-186">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="3b370-187">Når den er importeret, vises udløseren under **Mine flow**.</span><span class="sxs-lookup"><span data-stu-id="3b370-187">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="3b370-188">Start følgende fire variabler på basis af miljøoplysningerne:</span><span class="sxs-lookup"><span data-stu-id="3b370-188">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="3b370-189">Azure-lejer-id</span><span class="sxs-lookup"><span data-stu-id="3b370-189">Azure Tenant ID</span></span>
        - <span data-ttu-id="3b370-190">Azure-programklient-id</span><span class="sxs-lookup"><span data-stu-id="3b370-190">Azure Application Client ID</span></span>
        - <span data-ttu-id="3b370-191">Azure-programklienthemmelighed</span><span class="sxs-lookup"><span data-stu-id="3b370-191">Azure Application Client Secret</span></span>
        - <span data-ttu-id="3b370-192">Slutpunkt for lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="3b370-192">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="3b370-193">Du kan finde flere oplysninger om denne variabel under [Konfigurere integration af lagersynlighed](#setup-inventory-visibility-integration) senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="3b370-193">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="3b370-194">![Konfigurationsudløser](media/configuration-trigger.png "Konfigurationsudløser")</span><span class="sxs-lookup"><span data-stu-id="3b370-194">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="3b370-195">Vælg **Slå til**.</span><span class="sxs-lookup"><span data-stu-id="3b370-195">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="3b370-196">Installer tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="3b370-196">Install the add-in</span></span>

<span data-ttu-id="3b370-197">For at installere tilføjelsesprogrammet Lagersynlighed skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="3b370-197">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="3b370-198">Log på portalen [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="3b370-198">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="3b370-199">Vælg det projekt, dit miljø skal implementeres i, på startsiden.</span><span class="sxs-lookup"><span data-stu-id="3b370-199">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="3b370-200">Vælg det miljø, som tilføjelsesprogrammet skal installeres i, på projektsiden.</span><span class="sxs-lookup"><span data-stu-id="3b370-200">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="3b370-201">Rul ned på miljøsiden, indtil du ser afsnittet **Miljøtilføjelsesprogrammer** i sektionen **Power Platform-integration**, hvor du kan finde Dataverse-miljønavnet.</span><span class="sxs-lookup"><span data-stu-id="3b370-201">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="3b370-202">Vælg **Installér et nyt tilføjelsesprogram** i afsnittet **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="3b370-202">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="3b370-203">![Miljøsiden i LCS](media/inventory-visibility-environment.png "Miljøsiden i LCS")</span><span class="sxs-lookup"><span data-stu-id="3b370-203">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="3b370-204">Vælg linket **Installer et nyt tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="3b370-204">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="3b370-205">Der åbnes en liste over tilgængelige tilføjelsesprogrammer.</span><span class="sxs-lookup"><span data-stu-id="3b370-205">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="3b370-206">Vælg **Lagersynlighed** på listen.</span><span class="sxs-lookup"><span data-stu-id="3b370-206">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="3b370-207">Angiv værdier for følgende felter til dit miljø:</span><span class="sxs-lookup"><span data-stu-id="3b370-207">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="3b370-208">**AAD-program-id (klient)**</span><span class="sxs-lookup"><span data-stu-id="3b370-208">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="3b370-209">**AAD-lejer-id**</span><span class="sxs-lookup"><span data-stu-id="3b370-209">**AAD tenant ID**</span></span>

    <span data-ttu-id="3b370-210">![Konfigurationsside for tilføjelsesprogram](media/inventory-visibility-setup.png "Konfigurationsside for tilføjelsesprogram")</span><span class="sxs-lookup"><span data-stu-id="3b370-210">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="3b370-211">Acceptér vilkårene og betingelsen ved at markere afkrydsningsfeltet **Vilkår og betingelser**.</span><span class="sxs-lookup"><span data-stu-id="3b370-211">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="3b370-212">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="3b370-212">Select **Install**.</span></span> <span data-ttu-id="3b370-213">Status for tilføjelsesprogrammet vil blive vist som **installerer**.</span><span class="sxs-lookup"><span data-stu-id="3b370-213">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="3b370-214">Når det er gjort, skal du opdatere siden for at se statusændringen til **Installeret**.</span><span class="sxs-lookup"><span data-stu-id="3b370-214">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="3b370-215">Fjern tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="3b370-215">Uninstall the add-in</span></span>

<span data-ttu-id="3b370-216">Hvis du vil fjerne tilføjelsesprogrammet, skal du vælge **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="3b370-216">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="3b370-217">Når du opdaterer LCS, fjernes tilføjelsesprogrammet Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="3b370-217">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="3b370-218">Fjernelsesprocessen fjerner registreringen af tilføjelsesprogrammet og starter også et job for at rydde op i alle de forretningsdata, der er gemt i tjenesten.</span><span class="sxs-lookup"><span data-stu-id="3b370-218">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="3b370-219">Forbruge data i den tilgængelige lagerbeholdning fra Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3b370-219">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="3b370-220">Implementere integrationspakken Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="3b370-220">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="3b370-221">Hvis du kører Supply Chain Management version 10.0.17 eller tidligere, skal du kontakte supportteamet for onboarding af lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for at hente pakkefilen.</span><span class="sxs-lookup"><span data-stu-id="3b370-221">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="3b370-222">Implementer derefter pakken i LCS.</span><span class="sxs-lookup"><span data-stu-id="3b370-222">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="3b370-223">Hvis der opstår uoverensstemmelse mellem versioner under installationen, skal du importere projektet X++ manuelt til udviklingsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="3b370-223">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="3b370-224">Opret derefter implementeringspakken i udviklingsmiljøet, og implementer den i produktionsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="3b370-224">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="3b370-225">Koden er inkluderet i Supply Chain Management version 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="3b370-225">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="3b370-226">Hvis du kører denne version eller en senere, er det ikke påkrævet.</span><span class="sxs-lookup"><span data-stu-id="3b370-226">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="3b370-227">Sørg for, at følgende funktioner er aktiveret i dit Supply Chain Management-miljø.</span><span class="sxs-lookup"><span data-stu-id="3b370-227">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="3b370-228">(Som standard er de aktiveret).</span><span class="sxs-lookup"><span data-stu-id="3b370-228">(By default, they are turned on.)</span></span>

| <span data-ttu-id="3b370-229">Funktionsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="3b370-229">Feature description</span></span> | <span data-ttu-id="3b370-230">Kodeversion</span><span class="sxs-lookup"><span data-stu-id="3b370-230">Code version</span></span> | <span data-ttu-id="3b370-231">Skifte klasse</span><span class="sxs-lookup"><span data-stu-id="3b370-231">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="3b370-232">Aktivere eller deaktivere ved hjælp af lagerdimensioner i tabellen InventSum</span><span class="sxs-lookup"><span data-stu-id="3b370-232">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="3b370-233">10.0.11</span><span class="sxs-lookup"><span data-stu-id="3b370-233">10.0.11</span></span> | <span data-ttu-id="3b370-234">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="3b370-234">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="3b370-235">Aktivere eller deaktivere ved hjælp af lagerdimensioner i tabellen InventSumDelta</span><span class="sxs-lookup"><span data-stu-id="3b370-235">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="3b370-236">10.0.12</span><span class="sxs-lookup"><span data-stu-id="3b370-236">10.0.12</span></span> | <span data-ttu-id="3b370-237">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="3b370-237">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="3b370-238">Konfigurer integration af lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="3b370-238">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="3b370-239">I Supply Chain Management skal du åbne arbejdsområdet **[Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og aktivere funktionen **Integration af lagersynlighed**.</span><span class="sxs-lookup"><span data-stu-id="3b370-239">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="3b370-240">Gå til **Lagerstyring \> Konfiguration \> Parametre for integration af lagersynlighed**, og angiv URL-adressen for det miljø, hvor du kører lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="3b370-240">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="3b370-241">Find LCS-miljøets Azure-område, og angiv derefter URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="3b370-241">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="3b370-242">URL-adressen har følgende format:</span><span class="sxs-lookup"><span data-stu-id="3b370-242">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="3b370-243">Hvis du f.eks. er i Europa, har dit miljø en af følgende URL-adresser:</span><span class="sxs-lookup"><span data-stu-id="3b370-243">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="3b370-244">Følgende områder er tilgængelige i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="3b370-244">The following regions are currently available.</span></span>

    | <span data-ttu-id="3b370-245">Azure-region</span><span class="sxs-lookup"><span data-stu-id="3b370-245">Azure region</span></span> | <span data-ttu-id="3b370-246">Områdets korte navn</span><span class="sxs-lookup"><span data-stu-id="3b370-246">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="3b370-247">Det østlige Australien</span><span class="sxs-lookup"><span data-stu-id="3b370-247">Australia east</span></span> | <span data-ttu-id="3b370-248">eau</span><span class="sxs-lookup"><span data-stu-id="3b370-248">eau</span></span> |
    | <span data-ttu-id="3b370-249">Det sydøstlige Australien</span><span class="sxs-lookup"><span data-stu-id="3b370-249">Australia southeast</span></span> | <span data-ttu-id="3b370-250">seau</span><span class="sxs-lookup"><span data-stu-id="3b370-250">seau</span></span> |
    | <span data-ttu-id="3b370-251">Det centrale Canada</span><span class="sxs-lookup"><span data-stu-id="3b370-251">Canada central</span></span> | <span data-ttu-id="3b370-252">cca</span><span class="sxs-lookup"><span data-stu-id="3b370-252">cca</span></span> |
    | <span data-ttu-id="3b370-253">Det østlige Canada</span><span class="sxs-lookup"><span data-stu-id="3b370-253">Canada east</span></span> | <span data-ttu-id="3b370-254">eca</span><span class="sxs-lookup"><span data-stu-id="3b370-254">eca</span></span> |
    | <span data-ttu-id="3b370-255">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="3b370-255">North Europe</span></span> | <span data-ttu-id="3b370-256">neu</span><span class="sxs-lookup"><span data-stu-id="3b370-256">neu</span></span> |
    | <span data-ttu-id="3b370-257">Vesteuropa</span><span class="sxs-lookup"><span data-stu-id="3b370-257">West Europe</span></span> | <span data-ttu-id="3b370-258">weu</span><span class="sxs-lookup"><span data-stu-id="3b370-258">weu</span></span> |
    | <span data-ttu-id="3b370-259">Det østlige USA</span><span class="sxs-lookup"><span data-stu-id="3b370-259">East US</span></span> | <span data-ttu-id="3b370-260">eus</span><span class="sxs-lookup"><span data-stu-id="3b370-260">eus</span></span> |
    | <span data-ttu-id="3b370-261">Det vestlige USA</span><span class="sxs-lookup"><span data-stu-id="3b370-261">West US</span></span> | <span data-ttu-id="3b370-262">wus</span><span class="sxs-lookup"><span data-stu-id="3b370-262">wus</span></span> |

1. <span data-ttu-id="3b370-263">Gå til **Lagerstyring \> Periodisk \> Integration af lagersynlighed**, og aktivér jobbet.</span><span class="sxs-lookup"><span data-stu-id="3b370-263">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="3b370-264">Alle hændelser med lagerændringer fra Supply Chain Management vil nu blive bogført i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="3b370-264">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="3b370-265">Den offentlige API for tilføjelsesprogrammet Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="3b370-265">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="3b370-266">Den offentlige REST-API til tilføjelsesprogrammet Lagersynlighed viser flere specifikke slutpunkter for integration.</span><span class="sxs-lookup"><span data-stu-id="3b370-266">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="3b370-267">Det understøtter tre overordnede interaktionstyper:</span><span class="sxs-lookup"><span data-stu-id="3b370-267">It supports three main interaction types:</span></span>

- <span data-ttu-id="3b370-268">Bogføring af ændret lagerbeholdning i tilføjelsesprogrammet fra et eksternt system</span><span class="sxs-lookup"><span data-stu-id="3b370-268">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="3b370-269">Forespørgsel om aktuelle disponible lagerantal fra et eksternt system</span><span class="sxs-lookup"><span data-stu-id="3b370-269">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="3b370-270">Automatisk synkronisering med lagerbeholdning i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3b370-270">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="3b370-271">Automatisk synkronisering er ikke en del af den offentlige API.</span><span class="sxs-lookup"><span data-stu-id="3b370-271">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="3b370-272">Den håndteres i stedet i baggrunden for miljøer, hvor tilføjelsesprogrammet Lagersynlighed er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="3b370-272">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="3b370-273">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="3b370-273">Authentication</span></span>

<span data-ttu-id="3b370-274">Sikkerhedstoken til platformen bruges til at kalde tilføjelsesprogrammet Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="3b370-274">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="3b370-275">Du skal derfor generere et *Azure Active Directory-token (Azure AD)* ved hjælp af Azure AD-programmet.</span><span class="sxs-lookup"><span data-stu-id="3b370-275">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="3b370-276">Du skal derefter bruge Azure AD-tokenet til at hente *adgangstoken* fra sikkerhedstjenesten.</span><span class="sxs-lookup"><span data-stu-id="3b370-276">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="3b370-277">Få et token til sikkerhedsservice ved at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="3b370-277">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="3b370-278">Log på Azure-portalen, og brug den til at finde `clientId` og `clientSecret` til din Supply Chain Management-applikation.</span><span class="sxs-lookup"><span data-stu-id="3b370-278">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="3b370-279">Hent et Azure Active Directory-token (`aadToken`) ved at sende en HTTP-anmodning med følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="3b370-279">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="3b370-280">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="3b370-280">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="3b370-281">**metode** - `GET`</span><span class="sxs-lookup"><span data-stu-id="3b370-281">**Method** - `GET`</span></span>
    - <span data-ttu-id="3b370-282">**Brødtekst (formulardata)**:</span><span class="sxs-lookup"><span data-stu-id="3b370-282">**Body content (form data)**:</span></span>

        | <span data-ttu-id="3b370-283">nøgle</span><span class="sxs-lookup"><span data-stu-id="3b370-283">key</span></span> | <span data-ttu-id="3b370-284">værdi</span><span class="sxs-lookup"><span data-stu-id="3b370-284">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="3b370-285">client_id</span><span class="sxs-lookup"><span data-stu-id="3b370-285">client_id</span></span> | <span data-ttu-id="3b370-286">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="3b370-286">${aadAppId}</span></span> |
        | <span data-ttu-id="3b370-287">client_secret</span><span class="sxs-lookup"><span data-stu-id="3b370-287">client_secret</span></span> | <span data-ttu-id="3b370-288">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="3b370-288">${aadAppSecret}</span></span> |
        | <span data-ttu-id="3b370-289">grant_type</span><span class="sxs-lookup"><span data-stu-id="3b370-289">grant_type</span></span> | <span data-ttu-id="3b370-290">client_credentials</span><span class="sxs-lookup"><span data-stu-id="3b370-290">client_credentials</span></span> |
        | <span data-ttu-id="3b370-291">ressource</span><span class="sxs-lookup"><span data-stu-id="3b370-291">resource</span></span> | <span data-ttu-id="3b370-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="3b370-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="3b370-293">Du modtager et `aadToken` i svaret, der ligner følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="3b370-293">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="3b370-294">Formuler en JSON-anmodning, der ligner følgende:</span><span class="sxs-lookup"><span data-stu-id="3b370-294">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="3b370-295">Placering:</span><span class="sxs-lookup"><span data-stu-id="3b370-295">Where:</span></span>
    - <span data-ttu-id="3b370-296">Værdien `client_assertion` skal være det `aadToken`, du har modtaget i det forrige trin.</span><span class="sxs-lookup"><span data-stu-id="3b370-296">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="3b370-297">Værdien `context` skal være det miljø-id, hvor du vil implementere tilføjelsesprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3b370-297">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="3b370-298">Angiv alle andre værdier som vist i eksemplet.</span><span class="sxs-lookup"><span data-stu-id="3b370-298">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="3b370-299">Send en HTTP-anmodning med følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="3b370-299">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="3b370-300">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="3b370-300">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="3b370-301">**metode** - `POST`</span><span class="sxs-lookup"><span data-stu-id="3b370-301">**Method** - `POST`</span></span>
    - <span data-ttu-id="3b370-302">**HTTP-overskrift** – Medtag API-versionen (nøglen er `Api-Version`, og værdien er `1.0`)</span><span class="sxs-lookup"><span data-stu-id="3b370-302">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="3b370-303">**Brødtekst** – Medtag den JSON-anmodning, du oprettede i det forrige trin.</span><span class="sxs-lookup"><span data-stu-id="3b370-303">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="3b370-304">Du vil få et `access_token` i svaret.</span><span class="sxs-lookup"><span data-stu-id="3b370-304">You will get an `access_token` in response.</span></span> <span data-ttu-id="3b370-305">Det skal du bruge som ihændehavertoken for at kalde Lagersynlighed-API'et.</span><span class="sxs-lookup"><span data-stu-id="3b370-305">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="3b370-306">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="3b370-306">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="3b370-307">Eksempelanmodning</span><span class="sxs-lookup"><span data-stu-id="3b370-307">Sample Request</span></span>

<span data-ttu-id="3b370-308">Til reference er der en eksempel http-anmodning, og du kan bruge værktøjer eller kodningssprog til at sende denne anmodning, f.eks. ``Postman``.</span><span class="sxs-lookup"><span data-stu-id="3b370-308">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="3b370-309">Konfigurere API'et til Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="3b370-309">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="3b370-310">Før du bruger tjenesten, skal du udføre de konfigurationer, der er beskrevet i følgende underafsnit.</span><span class="sxs-lookup"><span data-stu-id="3b370-310">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="3b370-311">Konfigurationen kan variere afhængigt af detaljerne i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="3b370-311">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="3b370-312">Den består primært af fire dele:</span><span class="sxs-lookup"><span data-stu-id="3b370-312">It primarily includes four parts:</span></span>

- [<span data-ttu-id="3b370-313">Partitionering</span><span class="sxs-lookup"><span data-stu-id="3b370-313">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="3b370-314">Dimensionskonfigurationer</span><span class="sxs-lookup"><span data-stu-id="3b370-314">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="3b370-315">Indeksering</span><span class="sxs-lookup"><span data-stu-id="3b370-315">Indexing</span></span>](#indexing)
- [<span data-ttu-id="3b370-316">Brugerdefineret måling</span><span class="sxs-lookup"><span data-stu-id="3b370-316">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="3b370-317">Partitionering</span><span class="sxs-lookup"><span data-stu-id="3b370-317">Partitioning</span></span>

<span data-ttu-id="3b370-318">Partitionering kan have stor indflydelse på ydeevnen af Lagersynlighed-API'et.</span><span class="sxs-lookup"><span data-stu-id="3b370-318">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="3b370-319">Det er en god ide at definere et skema, der giver mulighed for mindre gruppering af data, mens det stadig er muligt at give meningsfulde dataforespørgsler.</span><span class="sxs-lookup"><span data-stu-id="3b370-319">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="3b370-320">Elementet `organizationId` (`dataAreaId` i Supply Chain Management) vil altid være en del af partitionen, og Lagersynlighede er som standard angivet til at partitionere efter dimensioner som *Sted + lokation*.</span><span class="sxs-lookup"><span data-stu-id="3b370-320">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="3b370-321">Det betyder, at der altid skal sendes forespørgsler til tjenesten med de dimensioner, der er defineret på filtrene.</span><span class="sxs-lookup"><span data-stu-id="3b370-321">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="3b370-322">*Sted* og *Lokation* er to generelle standarddimensioner i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="3b370-322">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="3b370-323">I Supply Chain Management kaldes disse dimensioner *Sted* (`InventSiteId`) og *Lagersted* (`InventLocationId`).</span><span class="sxs-lookup"><span data-stu-id="3b370-323">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="3b370-324">Dimensionskonfigurationer</span><span class="sxs-lookup"><span data-stu-id="3b370-324">Dimension configurations</span></span>

<span data-ttu-id="3b370-325">Lagersynlighed vil indeholde en liste over generelle standarddimensioner, der gør det muligt at integrere flere kildesystemer.</span><span class="sxs-lookup"><span data-stu-id="3b370-325">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="3b370-326">I følgende tabel vises de lagerdimensioner, der vil være standarddimensionsnavne i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="3b370-326">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="3b370-327">Dimensionstype</span><span class="sxs-lookup"><span data-stu-id="3b370-327">Dimension type</span></span> | <span data-ttu-id="3b370-328">Dimensionens navn</span><span class="sxs-lookup"><span data-stu-id="3b370-328">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="3b370-329">Produkt</span><span class="sxs-lookup"><span data-stu-id="3b370-329">Product</span></span> | `ColorId` |
| <span data-ttu-id="3b370-330">Produkt</span><span class="sxs-lookup"><span data-stu-id="3b370-330">Product</span></span> | `SizeId` |
| <span data-ttu-id="3b370-331">Produkt</span><span class="sxs-lookup"><span data-stu-id="3b370-331">Product</span></span> | `StyleId` |
| <span data-ttu-id="3b370-332">Produkt</span><span class="sxs-lookup"><span data-stu-id="3b370-332">Product</span></span> | `ConfigId` |
| <span data-ttu-id="3b370-333">Sporing</span><span class="sxs-lookup"><span data-stu-id="3b370-333">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="3b370-334">Sporing</span><span class="sxs-lookup"><span data-stu-id="3b370-334">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="3b370-335">Adresse</span><span class="sxs-lookup"><span data-stu-id="3b370-335">Location</span></span> | `LocationId` |
| <span data-ttu-id="3b370-336">Adresse</span><span class="sxs-lookup"><span data-stu-id="3b370-336">Location</span></span> | `SiteId` |
| <span data-ttu-id="3b370-337">Lagerstatus</span><span class="sxs-lookup"><span data-stu-id="3b370-337">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="3b370-338">Lagerstedsspecifik</span><span class="sxs-lookup"><span data-stu-id="3b370-338">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="3b370-339">Lagerstedsspecifik</span><span class="sxs-lookup"><span data-stu-id="3b370-339">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="3b370-340">Lagerstedsspecifik</span><span class="sxs-lookup"><span data-stu-id="3b370-340">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="3b370-341">Den dimensionstype, der er angivet i forrige tabel, er kun til reference.</span><span class="sxs-lookup"><span data-stu-id="3b370-341">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="3b370-342">Du behøver ikke definere dimensionstypen i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="3b370-342">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="3b370-343">Hvis der findes en brugerdefineret dimension, som skal overføres til en standardværdi, når den forbruges af Lagersynlighed, kan du konfigurere navnet **Brugerdefineret dimension** i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="3b370-343">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="3b370-344">Eksterne systemer får adgang til Lagersynlighed gennem RESTful API'er, der muliggør disponible oplysninger om bestemte sæt dimensioner, der skal forespørges.</span><span class="sxs-lookup"><span data-stu-id="3b370-344">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="3b370-345">I forbindelse med integrationen giver Lagersynlighed dig mulighed for at konfigurere den *eksterne kanals datakilde* og kildedimensionen til *måldimensionerne* i Lagersynlighed.</span><span class="sxs-lookup"><span data-stu-id="3b370-345">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="3b370-346">Måldimensionerne skal være en af følgende:</span><span class="sxs-lookup"><span data-stu-id="3b370-346">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="3b370-347">Standarddimensioner i Lagersynlighed</span><span class="sxs-lookup"><span data-stu-id="3b370-347">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="3b370-348">Brugerdefinerede dimensioner</span><span class="sxs-lookup"><span data-stu-id="3b370-348">Custom dimensions</span></span>

<span data-ttu-id="3b370-349">Formålet med dimensionskonfiguration er at standardisere integrationen af flere systemer til forespørgslen på dimensioner og bogføringshændelsen med dimensioner.</span><span class="sxs-lookup"><span data-stu-id="3b370-349">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="3b370-350">Indeksering</span><span class="sxs-lookup"><span data-stu-id="3b370-350">Indexing</span></span>

<span data-ttu-id="3b370-351">I de fleste tilfælde vil lagerbeholdningsforespørgslen ikke kun være på det højeste "totale" niveau, men du ønsker måske at se de samlede resultater på baggrund af lagerdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="3b370-351">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="3b370-352">Lagersynlighed giver fleksibilitet, fordi du kan konfigurere de indekser, der er baseret på dimensionen eller kombinationen af dimensionerne.</span><span class="sxs-lookup"><span data-stu-id="3b370-352">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="3b370-353">I øjeblikket kan du kun konfigurere indekser til maksimalt fem.</span><span class="sxs-lookup"><span data-stu-id="3b370-353">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="3b370-354">Du skal nøje overveje, hvilken dimension eller dimensionskombination du vil bruge før implementeringen for at sikre, at den opfylder dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="3b370-354">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="3b370-355">Hvis du f.eks. vil forespørge på produkter på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="3b370-355">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="3b370-356">Forespørg på den samlede disponible beholdning via *Farve*- og *Størrelse*-dimensionerne.</span><span class="sxs-lookup"><span data-stu-id="3b370-356">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="3b370-357">I nogle tilfælde vil du kun forespørge på produktet i alt.</span><span class="sxs-lookup"><span data-stu-id="3b370-357">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="3b370-358">Du skal have defineret to indekser som følgende:</span><span class="sxs-lookup"><span data-stu-id="3b370-358">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="3b370-359">Den tomme kantede parentes samles på basis af produkt-id'et i partitionen.</span><span class="sxs-lookup"><span data-stu-id="3b370-359">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="3b370-360">Indekseringen definerer, hvordan du kan gruppere resultaterne baseret på `groupBy`-forespørgselsindstillingen.</span><span class="sxs-lookup"><span data-stu-id="3b370-360">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="3b370-361">Hvis du ikke definerer `groupBy`-værdier, får du totaler med `productid`.</span><span class="sxs-lookup"><span data-stu-id="3b370-361">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="3b370-362">Hvis du definerer `groupBy` som `groupBy=ColorId&groupBy=SizeId`, får du ellers flere linjer baseret på de forskellige kombinationer af farve og størrelse i systemet.</span><span class="sxs-lookup"><span data-stu-id="3b370-362">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="3b370-363">Du kan sætte dine forespørgselskriterier i anmodningsteksten.</span><span class="sxs-lookup"><span data-stu-id="3b370-363">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="3b370-364">Her er et eksempel på en forespørgsel på produktet med en kombination af farve og størrelse.</span><span class="sxs-lookup"><span data-stu-id="3b370-364">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
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

<span data-ttu-id="3b370-365">For feltet `filters` understøtter kun `ProductId` i øjeblikket flere værdier.</span><span class="sxs-lookup"><span data-stu-id="3b370-365">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="3b370-366">Hvis `ProductId` er en tom matrix, forespørges på alle produkter.</span><span class="sxs-lookup"><span data-stu-id="3b370-366">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="3b370-367">Brugerdefineret måling</span><span class="sxs-lookup"><span data-stu-id="3b370-367">Custom measurement</span></span>

<span data-ttu-id="3b370-368">Standardmåleantallet er kædet sammen med Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3b370-368">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="3b370-369">Det kan dog være en god ide at have et antal, der består af en kombination af standardmålene.</span><span class="sxs-lookup"><span data-stu-id="3b370-369">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="3b370-370">Hvis du vil gøre dette, kan du have en konfiguration af brugerdefinerede antal, der føjes til outputtet af forespørgsler på den disponible lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="3b370-370">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="3b370-371">Denne funktion giver dig mulighed for at definere et sæt målinger, der skal tilføjes, og/eller et sæt målinger, der skal trækkes fra, så de danner den brugerdefinerede måling.</span><span class="sxs-lookup"><span data-stu-id="3b370-371">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="3b370-372">I følgende forespørgselsbetingelse skal du f.eks. konfigurere det brugerdefinerede måleanta som `MyCustomAvailableforReservation`, der skal forbruges af forbrugssystemet.</span><span class="sxs-lookup"><span data-stu-id="3b370-372">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="3b370-373">Forbrugssystem</span><span class="sxs-lookup"><span data-stu-id="3b370-373">Consumption system</span></span> | <span data-ttu-id="3b370-374">Beregnede målinger</span><span class="sxs-lookup"><span data-stu-id="3b370-374">Calculated measurers</span></span> | <span data-ttu-id="3b370-375">Datakilde</span><span class="sxs-lookup"><span data-stu-id="3b370-375">Data source</span></span> | <span data-ttu-id="3b370-376">Modifikator</span><span class="sxs-lookup"><span data-stu-id="3b370-376">Modifier</span></span> | <span data-ttu-id="3b370-377">Modifikator som beregningstype</span><span class="sxs-lookup"><span data-stu-id="3b370-377">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="3b370-378">Addition</span><span class="sxs-lookup"><span data-stu-id="3b370-378">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="3b370-379">Addition</span><span class="sxs-lookup"><span data-stu-id="3b370-379">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="3b370-380">Subtraktion</span><span class="sxs-lookup"><span data-stu-id="3b370-380">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="3b370-381">Addition</span><span class="sxs-lookup"><span data-stu-id="3b370-381">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="3b370-382">Subtraktion</span><span class="sxs-lookup"><span data-stu-id="3b370-382">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="3b370-383">Addition</span><span class="sxs-lookup"><span data-stu-id="3b370-383">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="3b370-384">Addition</span><span class="sxs-lookup"><span data-stu-id="3b370-384">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="3b370-385">Subtraktion</span><span class="sxs-lookup"><span data-stu-id="3b370-385">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="3b370-386">Subtraktion</span><span class="sxs-lookup"><span data-stu-id="3b370-386">Subtraction</span></span> |

<span data-ttu-id="3b370-387">Med denne fremgangsmåde vil forespørgslen på det brugerdefinerede måleantal returnere følgende output.</span><span class="sxs-lookup"><span data-stu-id="3b370-387">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="3b370-388">Outputtet `MyCustomAvailableforReservation` er baseret på beregningsindstillingen i de brugerdefinerede målinger som:</span><span class="sxs-lookup"><span data-stu-id="3b370-388">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="3b370-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="3b370-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="3b370-390">Bogføring af ændret lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="3b370-390">Posting on-hand changes</span></span>

<span data-ttu-id="3b370-391">Den præcise URL-adresse, som hændelsen vil blive bogført til, afhænger af dit geografiske område.</span><span class="sxs-lookup"><span data-stu-id="3b370-391">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="3b370-392">Den har formatet:</span><span class="sxs-lookup"><span data-stu-id="3b370-392">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="3b370-393">Når denne URL-adresse er godkendt, kan den bruges sammen med HTTP-`POST`-metoden til at sende hændelser for beholdningsændring til tjenesten.</span><span class="sxs-lookup"><span data-stu-id="3b370-393">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="3b370-394">En speciel header bruges til kommunikation med Dynamics 365-tjenester via HTTP-anmodninger, der angiver miljø-id'et for Supply Chain Management-forekomst, som dataene er kædet sammen med.</span><span class="sxs-lookup"><span data-stu-id="3b370-394">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="3b370-395">F.eks.:</span><span class="sxs-lookup"><span data-stu-id="3b370-395">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="3b370-396">Bogføring af forespørgsel på lagerbeholdningsændringer, eksempel 1</span><span class="sxs-lookup"><span data-stu-id="3b370-396">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="3b370-397">I dette eksempel vises et scenario, hvor du konfigurerer dimensionskonfigurationen i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3b370-397">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="3b370-398">Brug følgende forespørgsel til at konfigurere dimensionstilknytningen i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="3b370-398">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="3b370-399">Nu kan du angive `dimensionDataSource` og bruge brugerdefinerede dimensioner i forespørgslerne.</span><span class="sxs-lookup"><span data-stu-id="3b370-399">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="3b370-400">Systemet vil automatisk konvertere brugerdefinerede dimensioner til basisdimensioner.</span><span class="sxs-lookup"><span data-stu-id="3b370-400">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="3b370-401">Bogføring af forespørgsel på lagerbeholdningsændringer, eksempel 2</span><span class="sxs-lookup"><span data-stu-id="3b370-401">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="3b370-402">I dette eksempel vises et scenario, hvor der ikke er konfigureret tilknytninger for dimensionskonfigurationen i Power Apps, så bogføringen skal også bruge basisdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="3b370-402">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="3b370-403">Alle dimensioner skal være basisdimensioner, når `dimensionDataSource`-feltet er null, tomt eller blanktegn.</span><span class="sxs-lookup"><span data-stu-id="3b370-403">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="3b370-404">JSON-dokumentfeltegenskaber</span><span class="sxs-lookup"><span data-stu-id="3b370-404">JSON document field properties</span></span>

<span data-ttu-id="3b370-405">Felterne fra de JSON-forespørgselseksempler, der tidligere blev vist, har de egenskaber, der er angivet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="3b370-405">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="3b370-406">Felt-id</span><span class="sxs-lookup"><span data-stu-id="3b370-406">Field ID</span></span> | <span data-ttu-id="3b370-407">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="3b370-407">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="3b370-408">Et entydigt id for den specifikke ændringshændelse.</span><span class="sxs-lookup"><span data-stu-id="3b370-408">A unique ID for the specific change event.</span></span> <span data-ttu-id="3b370-409">Dette id bruges til at sikre, at hvis kommunikationen med tjenesten mislykkes under bogføring, vil genafsendelse af hændelsen ikke resultere i, at den samme hændelse tælles to gange i systemet.</span><span class="sxs-lookup"><span data-stu-id="3b370-409">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="3b370-410">Identifikatoren for den organisation, der er knyttet til hændelsen.</span><span class="sxs-lookup"><span data-stu-id="3b370-410">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="3b370-411">Dette knytter data til Supply Chain Management-organisationer eller dataområde-id'er.</span><span class="sxs-lookup"><span data-stu-id="3b370-411">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="3b370-412">Produktets identifikator.</span><span class="sxs-lookup"><span data-stu-id="3b370-412">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="3b370-413">Det antal, som lagerbeholdningen skal ændres med.</span><span class="sxs-lookup"><span data-stu-id="3b370-413">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="3b370-414">Hvis der f.eks. er føjet 10 nye bagels til en hylde, vil denne værdi være 10.</span><span class="sxs-lookup"><span data-stu-id="3b370-414">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="3b370-415">Hvis 3 bagels blev fjernet fra hylden eller solgt, vil denne værdi være -3.</span><span class="sxs-lookup"><span data-stu-id="3b370-415">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="3b370-416">Datakilden til de dimensioner, der bruges i bogføring af ændringshændelsen og forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="3b370-416">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="3b370-417">Hvis du angiver datakilden, kan du bruge de brugerdefinerede dimensioner fra den angivne datakilde.</span><span class="sxs-lookup"><span data-stu-id="3b370-417">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="3b370-418">Med dimensionskonfigurationen kan Lagersynlighed knytte de tilpassede dimensioner til de generelle standarddimensioner.</span><span class="sxs-lookup"><span data-stu-id="3b370-418">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="3b370-419">Hvis `dimensionDataSource` ikke er angivet, kan du kun bruge de generelle standarddimensioner i forespørgslerne.</span><span class="sxs-lookup"><span data-stu-id="3b370-419">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="3b370-420">En dynamisk pose med nøgle/værdi-par.</span><span class="sxs-lookup"><span data-stu-id="3b370-420">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="3b370-421">De vil blive knyttet til nogle af dimensionerne i Supply Chain Management, men du kan også tilføje brugerdefinerede dimensioner (som f.eks. *Kilde*), der kan angive, om hændelsen kommer fra Supply Chain Management eller et eksternt system.</span><span class="sxs-lookup"><span data-stu-id="3b370-421">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="3b370-422">Forespørgsel på aktuel disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="3b370-422">Querying current on-hand</span></span>

<span data-ttu-id="3b370-423">Slutpunktet for forespørgsel på den aktuelle disponible lagerbeholdning vil have en lignende URL-adresse:</span><span class="sxs-lookup"><span data-stu-id="3b370-423">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="3b370-424">Den vil blive forespurgt efter HTTP-`POST`-metoden.</span><span class="sxs-lookup"><span data-stu-id="3b370-424">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="3b370-425">Forespørgsel på aktuel disponibel lagerbeholdning, eksempel 1</span><span class="sxs-lookup"><span data-stu-id="3b370-425">Current on-hand query example 1</span></span>

<span data-ttu-id="3b370-426">I dette eksempel vises et scenario, hvor du allerede har fuldført dimensionskonfigurationen i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3b370-426">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="3b370-427">Brug følgende forespørgsel til at konfigurere dimensionstilknytningen i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="3b370-427">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="3b370-428">Nu kan du angive `dimensionDataSource` og bruge brugerdefinerede dimensioner i forespørgslerne.</span><span class="sxs-lookup"><span data-stu-id="3b370-428">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="3b370-429">Systemet vil automatisk konvertere brugerdefinerede dimensioner til basisdimensioner.</span><span class="sxs-lookup"><span data-stu-id="3b370-429">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="3b370-430">Du kan angive `DimensionDataSource` i `filters` og angive brugerdefinerede dimensioner i både `filters` og `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="3b370-430">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="3b370-431">Systemet vil automatisk konvertere brugerdefinerede dimensioner til basisdimensioner.</span><span class="sxs-lookup"><span data-stu-id="3b370-431">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="3b370-432">Forespørgsel på aktuel disponibel lagerbeholdning, eksempel 2</span><span class="sxs-lookup"><span data-stu-id="3b370-432">Current on-hand query example 2</span></span>

<span data-ttu-id="3b370-433">I dette eksempel vises et scenario, hvor der ikke er konfigureret tilknytninger for dimensionskonfigurationen i Power Apps, så bogføringen skal også bruge basisdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="3b370-433">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="3b370-434">Alle dimensioner skal være basisdimensioner, når `dimensionDataSource`-feltet under `filters` er null, tomt eller blanktegn.</span><span class="sxs-lookup"><span data-stu-id="3b370-434">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="3b370-435">Eksempel på returnering af resultat</span><span class="sxs-lookup"><span data-stu-id="3b370-435">Example return result</span></span>

<span data-ttu-id="3b370-436">De forespørgsler, der vises i de foregående eksempler, kunne returnere et resultat som dette.</span><span class="sxs-lookup"><span data-stu-id="3b370-436">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="3b370-437">Bemærk, at antalsfelterne er struktureret som en ordbog med målinger og deres tilknyttede værdier.</span><span class="sxs-lookup"><span data-stu-id="3b370-437">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
