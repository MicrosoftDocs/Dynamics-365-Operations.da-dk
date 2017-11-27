---
title: "Nulstil økonomirapporterings-datacenteret efter gendannelse af en database"
description: "Dette emne beskriver, hvordan du nulstiller økonomirapporterings-datacenteret efter gendannelse af en Microsoft Dynamics 365 for Finance and Operations-database."
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6e3f78fb2f6528449d2a411225cd0e14ca33443e
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="c4e7d-103">Nulstil økonomirapporterings-datacenteret efter gendannelse af en database</span><span class="sxs-lookup"><span data-stu-id="c4e7d-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c4e7d-104">Dette emne beskriver, hvordan du nulstiller økonomirapporterings-datacenteret efter gendannelse af en Microsoft Dynamics 365 for Finance and Operations-database.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="c4e7d-105">Hvis du på et tidspunkt vil gendanne din Finance and Operations-database fra en sikkerhedskopi eller kopiere databasen fra et andet miljø, skal du følge trinnene i dette emne for at sikre, at datacenteret for økonomirapportering bruger den gendannede Finance and Operations-database korrekt.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
> [!Note] 
> <span data-ttu-id="c4e7d-106">Trinene i processen understøttes for Dynamics 365 for Operations maj 2016 udgaven (App build 7.0.1265.23014 og økonomirapportering build 7.0.10000.4) og nyere versioner.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="c4e7d-107">Hvis du har en tidligere udgave af Dynamics 365 for Finance and Operations, skal du kontakte vores supportteam for at få hjælp.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="c4e7d-108">Eksporter rapportdefinitioner</span><span class="sxs-lookup"><span data-stu-id="c4e7d-108">Export report definitions</span></span>
<span data-ttu-id="c4e7d-109">Først skal du eksportere de rapportdesigns, der er placeret i Report Designer, ved hjælp af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="c4e7d-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="c4e7d-110">I Report Designer skal du gå til **Regnskab** &gt; **Komponentgruppe**.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="c4e7d-111">Vælg den komponentgruppe, der skal eksporterer, og klik på **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-111">Select the building block group to export, and click **Export**.</span></span> 

    > [!Note] 
    > <span data-ttu-id="c4e7d-112">Bemærk: I Finance and Operations understøttes kun én komponentgruppe, **Standard**.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="c4e7d-113">Vælg de rapportdefinitioner, der skal eksporteres:</span><span class="sxs-lookup"><span data-stu-id="c4e7d-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="c4e7d-114">Hvis du vil eksportere alle rapportdefinitioner og de tilhørende komponenter, skal du klikke på **Marker alt**.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="c4e7d-115">Hvis du vil eksportere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du klikke på den relevante fane og derefter vælge de elementer, der skal eksporteres.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="c4e7d-116">Tryk på og hold Ctrl-tasten nede for at vælge flere elementer på en fane. Når du vælger rapporter til eksport, vælges de tilknyttede rækker, kolonner, træer og dimensionsopsætninger.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-116">Press and hold the Ctrl key to select multiple items in a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="c4e7d-117">Klik på **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-117">Click **Export**.</span></span>
5.  <span data-ttu-id="c4e7d-118">Angiv et filnavn, og vælg et sikkert sted, hvor du vil gemme de eksporterede rapportdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-118">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="c4e7d-119">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-119">Click **Save**.</span></span>

<span data-ttu-id="c4e7d-120">Filen kan kopieres eller overføres til et sikkert sted, så den kan importeres til et andet miljø på et senere tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-120">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="c4e7d-121">Du kan finde oplysninger om brug af en Microsoft Azure-lagerkonto i [Overfør data med AzCopy-kommandolinjeværktøjet](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="c4e7d-121">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="c4e7d-122">Microsoft leverer ikke en lagerkonto som en del af din Finance and Operations-aftale.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-122">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="c4e7d-123">Du skal købe en lagerkonto eller bruge en lagerkonto fra et separat Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-123">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="c4e7d-124">Vær opmærksom på funktionen af D-drevet på virtuelle Azure-maskiner.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-124">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="c4e7d-125">Opbevar ikke dine eksporterede komponentgrupper her permanent.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-125">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="c4e7d-126">Du kan finde flere oplysninger om midlertidige drev i [Om de midlertidige drev på virtuelle Windows Azure-maskiner](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="c4e7d-126">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="c4e7d-127">Stop tjenester</span><span class="sxs-lookup"><span data-stu-id="c4e7d-127">Stop services</span></span>
<span data-ttu-id="c4e7d-128">Brug Fjernskrivebord til at oprette forbindelse til alle computere i miljøet, og stop følgende tjenester i Windows ved hjælp af services.msc:</span><span class="sxs-lookup"><span data-stu-id="c4e7d-128">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="c4e7d-129">Tjenesten World Wide Web Publishing (på alle AOS-computere)</span><span class="sxs-lookup"><span data-stu-id="c4e7d-129">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="c4e7d-130">Tjenesten Microsoft Dynamics 365 for Finance and Operations Batch Management (kun på ikke-private AOS-computere)</span><span class="sxs-lookup"><span data-stu-id="c4e7d-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="c4e7d-131">Tjenesten Management Reporter 2012 Process (kun på BI-computere)</span><span class="sxs-lookup"><span data-stu-id="c4e7d-131">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="c4e7d-132">Disse tjenester har åbne forbindelser til Dynamics 365 for Finance and Operations-databasen.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-132">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="c4e7d-133">Nulstil</span><span class="sxs-lookup"><span data-stu-id="c4e7d-133">Reset</span></span>
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="c4e7d-134">Find og hent den nyeste MinorVersionDataUpgrade.zip-pakke</span><span class="sxs-lookup"><span data-stu-id="c4e7d-134">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="c4e7d-135">Find den nyeste MinorVersionDataUpgrade.zip-pakke ved hjælp af vejledningen i [Hent den nyeste installerbare dataopgraderingspakke](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span><span class="sxs-lookup"><span data-stu-id="c4e7d-135">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="c4e7d-136">Vejledningen beskriver, hvordan du finder og henter den korrekte version af dataopgraderingspakken.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-136">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="c4e7d-137">Der kræves ikke en opgradering for at hent pakken MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-137">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="c4e7d-138">Du behøver kun at udføre trinnene i afsnittet "Hent den nyeste installerbare dataopgraderingspakke" uden at udføre nogen af de øvrige trin i artiklen for at hente en kopi af MinorVersionDataUpgrade.zip-pakken.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-138">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="c4e7d-139">Udfør scripts mod Finance and Operations-databasen</span><span class="sxs-lookup"><span data-stu-id="c4e7d-139">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="c4e7d-140">Kør følgende scripts mod Finance and Operations-databasen (ikke mod økonomirapporteringsdatabasen).</span><span class="sxs-lookup"><span data-stu-id="c4e7d-140">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="c4e7d-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="c4e7d-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="c4e7d-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="c4e7d-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="c4e7d-143">Disse scripts sikrer, at brugerne, rollerne og indstillingerne for sporing af ændringer er korrekte.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-143">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="c4e7d-144">Udfør PowerShell-kommando for at nulstille databasen</span><span class="sxs-lookup"><span data-stu-id="c4e7d-144">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="c4e7d-145">På AOS-computeren skal du udføre følgende kommandoer i PowerShell som administrator for at nulstille integrationen mellem Finance and Operations og økonomirapporteringen:</span><span class="sxs-lookup"><span data-stu-id="c4e7d-145">On the AOS computer, execute the following commands in PowerShell as an Administrator to reset the integration between Finance and Operations and financial reporting:</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> <span data-ttu-id="c4e7d-146">Når du har udført kommandoerne, bliver du bedt om at indtaste "Y" for at bekræfte.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-146">After executing the commands, you will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="c4e7d-147">Forklaring af parametrene:</span><span class="sxs-lookup"><span data-stu-id="c4e7d-147">Explanation of parameters:</span></span>

-   <span data-ttu-id="c4e7d-148">De gyldige værdier for -Reason er: SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-148">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="c4e7d-149">Parameteren -ReasonDetail er fri tekst.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-149">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="c4e7d-150">Årsag og reasonDetail registreres i telemetri/miljø overvågningen.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-150">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="c4e7d-151">Start tjenester</span><span class="sxs-lookup"><span data-stu-id="c4e7d-151">Start services</span></span>
<span data-ttu-id="c4e7d-152">Brug services.msc til at genstarte de tjenester, som du tidligere har stoppet:</span><span class="sxs-lookup"><span data-stu-id="c4e7d-152">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="c4e7d-153">Tjenesten World Wide Web Publishing (på alle AOS-computere)</span><span class="sxs-lookup"><span data-stu-id="c4e7d-153">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="c4e7d-154">Tjenesten Microsoft Dynamics 365 for Finance and Operations Batch Management (kun på ikke-private AOS-computere)</span><span class="sxs-lookup"><span data-stu-id="c4e7d-154">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="c4e7d-155">Tjenesten Management Reporter 2012 Process (kun på BI-computere)</span><span class="sxs-lookup"><span data-stu-id="c4e7d-155">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="c4e7d-156">Importer rapportdefinitioner</span><span class="sxs-lookup"><span data-stu-id="c4e7d-156">Import report definitions</span></span>
<span data-ttu-id="c4e7d-157">Importer dine rapportdesigns fra Report Designer ved hjælp af den fil, der oprettes under eksporten:</span><span class="sxs-lookup"><span data-stu-id="c4e7d-157">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="c4e7d-158">I Report Designer skal du gå til **Regnskab** &gt; **Komponentgruppe**.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-158">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="c4e7d-159">Vælg den komponentgruppe, der skal eksporterer, og klik på **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-159">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="c4e7d-160">Bemærk: I Finance and Operations understøttes kun én komponentgruppe, **Standard**.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-160">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="c4e7d-161">Vælg komponenten **Standard**, og klik på **Importer**.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-161">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="c4e7d-162">Vælg den fil, der indeholder de eksporterede rapportdefinitioner, og klik på **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-162">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="c4e7d-163">I dialogboksen Importér skal du vælge de rapportdefinitioner, der skal importeres:</span><span class="sxs-lookup"><span data-stu-id="c4e7d-163">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="c4e7d-164">Hvis du vil importere alle rapportdefinitioner og de understøttende komponenter, skal du klikke på **Marker alt**.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-164">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="c4e7d-165">Hvis du vil importere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du markere de rapporter, rækker, kolonner, træer eller dimensionsopsætninger, der skal importeres.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-165">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="c4e7d-166">Klik på **Importer**.</span><span class="sxs-lookup"><span data-stu-id="c4e7d-166">Click **Import**.</span></span>





