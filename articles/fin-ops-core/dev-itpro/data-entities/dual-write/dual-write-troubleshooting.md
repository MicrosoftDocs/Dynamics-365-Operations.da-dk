---
title: Generel fejlfinding
description: Dette emne indeholder generelle fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b01ef3da908739d17f2a03398ae56f35191e8db6
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744535"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="7c169-103">Generel fejlfinding</span><span class="sxs-lookup"><span data-stu-id="7c169-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="7c169-104">Dette emne indeholder generelle fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7c169-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c169-105">Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren.</span><span class="sxs-lookup"><span data-stu-id="7c169-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="7c169-106">I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="7c169-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="7c169-107">Når du forsøger at installere dobbeltskrivningspakken ved hjælp af værktøjet Package Deployer, vises der ingen tilgængelige løsninger</span><span class="sxs-lookup"><span data-stu-id="7c169-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="7c169-108">Nogle versioner af Package Deployer-værktøjet er inkompatible med pakken til dobbeltskrivningsløsninger.</span><span class="sxs-lookup"><span data-stu-id="7c169-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="7c169-109">For at installere pakken korrekt skal du sørge for at bruge [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) eller nyere af Package Deployer-værktøjet.</span><span class="sxs-lookup"><span data-stu-id="7c169-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="7c169-110">Når du har installeret Package Deployer-værktøjet, skal du installere løsningspakken ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="7c169-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="7c169-111">Hent den seneste fil med løsningspakken fra Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="7c169-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="7c169-112">Når zip-filen med pakken er hentet, skal du højreklikke på den og vælge **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="7c169-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="7c169-113">Markér afkrydsningsfeltet **Ophæv blokering**, og vælg derefter **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="7c169-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="7c169-114">Hvis du ikke kan se afkrydsningsfeltet **Ophæv blokering**, er blokeringen af zip-filen allerede fjernet, og du kan springe dette trin over.</span><span class="sxs-lookup"><span data-stu-id="7c169-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Dialogboksen Egenskaber](media/unblock_option.png)

2. <span data-ttu-id="7c169-116">Udpak zip-filen med pakken, og kopier alle filerne i mappen **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.</span><span class="sxs-lookup"><span data-stu-id="7c169-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Indhold af mappen Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. <span data-ttu-id="7c169-118">Indsæt alle de kopierede filer i mappen **Tools** i Package Deployer-værktøjet.</span><span class="sxs-lookup"><span data-stu-id="7c169-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="7c169-119">Kør **PackageDeployer.exe** for at vælge Dataverse-miljøet og installere løsningerne.</span><span class="sxs-lookup"><span data-stu-id="7c169-119">Run **PackageDeployer.exe** to select the Dataverse environment and install the solutions.</span></span>

    ![Indhold af mappen Tools](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a><span data-ttu-id="7c169-121">Aktivere og åbne plug-in-sporingslogge i Dataverse for at få vist oplysninger om fejl</span><span class="sxs-lookup"><span data-stu-id="7c169-121">Enable and view the plug-in trace log in Dataverse to view error details</span></span>

<span data-ttu-id="7c169-122">**Følgende rolle er påkrævet for at kunne aktivere sporingsloggen og få vist fejl:** systemadministrator</span><span class="sxs-lookup"><span data-stu-id="7c169-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="7c169-123">Udfør følgende trin for at aktivere sporingsloggen.</span><span class="sxs-lookup"><span data-stu-id="7c169-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="7c169-124">Log på den modeldrevede app i Dynamics 365, åbn siden **Indstillinger**, og vælg derefter **Administration** under **System**.</span><span class="sxs-lookup"><span data-stu-id="7c169-124">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="7c169-125">På siden **Administration** skal du vælge **Systemindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="7c169-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="7c169-126">Under fanen **Tilpasning** i kolonnen **Plug-in og brugerdefineret sporing af arbejdsgangsaktivitet** skal du vælge **Alle** for at aktivere sporingslogfilen for plug-in'en.</span><span class="sxs-lookup"><span data-stu-id="7c169-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** column, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="7c169-127">Hvis du kun vil logføre sporingslogge, når der opstår undtagelser, kan du vælge **Undtagelse** i stedet.</span><span class="sxs-lookup"><span data-stu-id="7c169-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="7c169-128">Udfør følgende trin for at få vist sporingsloggen.</span><span class="sxs-lookup"><span data-stu-id="7c169-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="7c169-129">Log på den modeldrevede app i Dynamics 365, åbn siden **Indstillinger**, og vælg derefter **Plug-in-sporingslogfil** under **Tilpasning**.</span><span class="sxs-lookup"><span data-stu-id="7c169-129">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="7c169-130">Find sporingslogfilerne, hvor kolonnen **Typenavn** er indstillet til **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span><span class="sxs-lookup"><span data-stu-id="7c169-130">Find the trace logs where the **Type Name** column is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="7c169-131">Dobbeltklik på et element for at få vist hele loggen, og gennemse derefter **Message Block**-teksten i oversigtspanelet **Udførelse**.</span><span class="sxs-lookup"><span data-stu-id="7c169-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="7c169-132">Aktivere fejlfindingstilstand for at foretage fejlfinding af problemer med direkte synkronisering i Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="7c169-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="7c169-133">**Påkrævet rolle for at få vist fejl**: Dobbeltskrivningsfejl i systemadministrationen, der stammer fra Dataverse, kan vises i appen Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7c169-133">**Required role to view the errors:** System admin Dual-write errors that originate in Dataverse can appear in the Finance and Operations app.</span></span> <span data-ttu-id="7c169-134">I nogle tilfælde er den fulde tekst i fejlmeddelelsen ikke tilgængelig, fordi meddelelsen er for lang eller indeholder personligt identificerbare oplysninger (PII).</span><span class="sxs-lookup"><span data-stu-id="7c169-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="7c169-135">Du kan aktivere detaljeret logføring for fejl ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="7c169-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="7c169-136">Alle projektkonfigurationer i Finance and Operations-apps har egenskaben **IsDebugMode** i tabellen **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="7c169-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** table.</span></span> <span data-ttu-id="7c169-137">Åbn tabellen **DualWriteProjectConfiguration** ved hjælp af tilføjelsesprogrammet til Excel.</span><span class="sxs-lookup"><span data-stu-id="7c169-137">Open the **DualWriteProjectConfiguration** table by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="7c169-138">Du kan nemt åbne tabellen ved at slå **Design**-tilstand til i Excel-tilføjelsesprogrammet og derefter tilføje **DualWriteProjectConfigurationEntity** i regnearket.</span><span class="sxs-lookup"><span data-stu-id="7c169-138">An easy way to open the table is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="7c169-139">Du kan finde flere oplysninger under [Åbne tabeldata i Excel og opdatere dem ved hjælp af tilføjelsesprogrammet til Excel](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="7c169-139">For more information, see [Open table data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="7c169-140">Indstil egenskaben **IsDebugMode** til **Ja** for projektet.</span><span class="sxs-lookup"><span data-stu-id="7c169-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="7c169-141">Kør det scenario, der genererer fejl.</span><span class="sxs-lookup"><span data-stu-id="7c169-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="7c169-142">De detaljerede logfiler er tilgængelige i tabellen DualWriteErrorLog.</span><span class="sxs-lookup"><span data-stu-id="7c169-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="7c169-143">Hvis du vil slå data op i tabelbrowseren, skal du bruge følgende URL-adresse (Erstat **XXX** efter behov):</span><span class="sxs-lookup"><span data-stu-id="7c169-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="7c169-144">Kontrollere synkroniseringsfejl på den virtuelle maskine for Finance and Operations-appen</span><span class="sxs-lookup"><span data-stu-id="7c169-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="7c169-145">**Påkrævet rolle for at få vist fejl:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="7c169-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="7c169-146">Log på Microsoft Dynamics LifeCycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="7c169-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="7c169-147">Åbn det LCS-projekt, du har valgt til at udføre dobbeltskrivningstesten for.</span><span class="sxs-lookup"><span data-stu-id="7c169-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="7c169-148">Vælg titlen **Skybaserede miljøer**.</span><span class="sxs-lookup"><span data-stu-id="7c169-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="7c169-149">Brug Fjernskrivebord til at logge på den virtuelle maskine (VM) for Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="7c169-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="7c169-150">Brug den lokale konto, der vises i LCS.</span><span class="sxs-lookup"><span data-stu-id="7c169-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="7c169-151">Åbn Logbog.</span><span class="sxs-lookup"><span data-stu-id="7c169-151">Open Event viewer.</span></span>
6. <span data-ttu-id="7c169-152">Vælg **Logfiler for programmer og tjenester \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operationel**.</span><span class="sxs-lookup"><span data-stu-id="7c169-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="7c169-153">Gennemse listen over seneste fejl.</span><span class="sxs-lookup"><span data-stu-id="7c169-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="7c169-154">Fjerne sammenkædning og sammenkæde med et andet Dataverse-miljø fra en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="7c169-154">Unlink and link another Dataverse environment from a Finance and Operations app</span></span>

<span data-ttu-id="7c169-155">**Påkrævet rolle for at fjerne miljøtilknytningen:** Systemadministrator for enten Finance and Operations-app eller Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7c169-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Dataverse.</span></span>

1. <span data-ttu-id="7c169-156">Log på Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="7c169-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="7c169-157">Gå til **Arbejdsområder \> Datastyring**, og vælg feltet **Dobbeltskrivning**.</span><span class="sxs-lookup"><span data-stu-id="7c169-157">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="7c169-158">Vælg alle kørende tilknytninger, og vælg derefter **Stop**.</span><span class="sxs-lookup"><span data-stu-id="7c169-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="7c169-159">Vælg **Ophæv sammenkædning af miljø**.</span><span class="sxs-lookup"><span data-stu-id="7c169-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="7c169-160">Vælg **Ja** for at bekræfte operationen.</span><span class="sxs-lookup"><span data-stu-id="7c169-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="7c169-161">Nu kan du sammenkæde et nyt miljø.</span><span class="sxs-lookup"><span data-stu-id="7c169-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="7c169-162">Kan ikke se linjeoplysningsformularen for salgsordren</span><span class="sxs-lookup"><span data-stu-id="7c169-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="7c169-163">Når du opretter en salgsordre i Dynamics 365 Sales, kan klik på **+ Tilføj produkter** omdirigere dig til ordrelinjeformen i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7c169-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="7c169-164">Du kan ikke få vist formularen for salgsordrelinjens **Oplysninger** på denne måde.</span><span class="sxs-lookup"><span data-stu-id="7c169-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="7c169-165">Indstillingen for **Oplysninger** vises ikke på rullelisten under **Ny ordrelinje**.</span><span class="sxs-lookup"><span data-stu-id="7c169-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="7c169-166">Dette sker, fordi Project Operations er installeret i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="7c169-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="7c169-167">Hvis du vil aktivere formularindstillingen **Oplysninger** igen, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="7c169-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="7c169-168">Naviger til tabellen **Ordrelinje**.</span><span class="sxs-lookup"><span data-stu-id="7c169-168">Navigate to the **Order Line** table.</span></span>
2. <span data-ttu-id="7c169-169">Find formularen **Oplysninger** under formularernoden.</span><span class="sxs-lookup"><span data-stu-id="7c169-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="7c169-170">Vælg formularen **Oplysninger**, og klik på **Aktivér sikkerhedsroller**.</span><span class="sxs-lookup"><span data-stu-id="7c169-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="7c169-171">Ret sikkerhedsindstillingen til **Vis for alle**.</span><span class="sxs-lookup"><span data-stu-id="7c169-171">Change the security setting to **Display to everyone**.</span></span>
