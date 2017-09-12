---
title: "Nulstil økonomirapporterings-datacenteret efter gendannelse af en database"
description: "Dette emne beskriver, hvordan du nulstiller økonomirapporterings-datacenteret efter gendannelse af en Microsoft Dynamics 365 for Finance and Operations-database."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: da-dk
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="65d8b-103">Nulstil økonomirapporterings-datacenteret efter gendannelse af en database</span><span class="sxs-lookup"><span data-stu-id="65d8b-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="65d8b-104">Dette emne beskriver, hvordan du nulstiller økonomirapporterings-datacenteret efter gendannelse af en Microsoft Dynamics 365 for Finance and Operations-database.</span><span class="sxs-lookup"><span data-stu-id="65d8b-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="65d8b-105">Hvis du på et tidspunkt vil gendanne din Finance and Operations-database fra en sikkerhedskopi eller kopiere databasen fra et andet miljø, skal du følge trinnene i dette emne for at sikre, at datacenteret for økonomirapportering bruger den gendannede Finance and Operations-database korrekt.</span><span class="sxs-lookup"><span data-stu-id="65d8b-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> <span data-ttu-id="65d8b-106">Trinene i processen understøttes for Dynamics 365 for Operations maj 2016 udgaven (App build 7.0.1265.23014 og økonomirapportering build 7.0.10000.4) og nyere versioner.</span><span class="sxs-lookup"><span data-stu-id="65d8b-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="65d8b-107">Hvis du har en tidligere udgave af Dynamics 365 for Finance and Operations, skal du kontakte vores supportteam for at få hjælp.</span><span class="sxs-lookup"><span data-stu-id="65d8b-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="65d8b-108">Eksporter rapportdefinitioner</span><span class="sxs-lookup"><span data-stu-id="65d8b-108">Export report definitions</span></span>
<span data-ttu-id="65d8b-109">Først skal du eksportere de rapportdesigns, der er placeret i Report Designer, ved hjælp af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="65d8b-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="65d8b-110">I Report Designer skal du gå til **Regnskab** &gt; **Komponentgruppe**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="65d8b-111">Vælg den komponentgruppe, der skal eksporterer, og klik på **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-111">Select the building block group to export, and click **Export**.</span></span> 
    > [!Note] 
    > <span data-ttu-id="65d8b-112">Bemærk: I Finance and Operations understøttes kun én komponentgruppe, **Standard**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
3.  <span data-ttu-id="65d8b-113">Vælg de rapportdefinitioner, der skal eksporteres:</span><span class="sxs-lookup"><span data-stu-id="65d8b-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="65d8b-114">Hvis du vil eksportere alle rapportdefinitioner og de tilhørende komponenter, skal du klikke på **Marker alt**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="65d8b-115">Hvis du vil eksportere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du klikke på den relevante fane og derefter vælge de elementer, der skal eksporteres.</span><span class="sxs-lookup"><span data-stu-id="65d8b-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="65d8b-116">Tryk på og hold Ctrl-tasten nede for at vælge flere elementer på en fane.</span><span class="sxs-lookup"><span data-stu-id="65d8b-116">Press and hold the Ctrl key to select multiple items in a tab.</span></span> <span data-ttu-id="65d8b-117">Når du vælger rapporter, der skal eksporteres, markeres de tilknyttede rækker, kolonner, træer og dimensionssæt.</span><span class="sxs-lookup"><span data-stu-id="65d8b-117">When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="65d8b-118">Klik på **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-118">Click **Export**.</span></span>
5.  <span data-ttu-id="65d8b-119">Angiv et filnavn, og vælg et sikkert sted, hvor du vil gemme de eksporterede rapportdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="65d8b-119">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="65d8b-120">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-120">Click **Save**.</span></span>

<span data-ttu-id="65d8b-121">Filen kan kopieres eller overføres til et sikkert sted, så den kan importeres til et andet miljø på et senere tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="65d8b-121">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="65d8b-122">Du kan finde oplysninger om brug af en Microsoft Azure-lagerkonto i [Overfør data med AzCopy-kommandolinjeværktøjet](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="65d8b-122">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="65d8b-123">Microsoft leverer ikke en lagerkonto som en del af din Finance and Operations-aftale.</span><span class="sxs-lookup"><span data-stu-id="65d8b-123">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="65d8b-124">Du skal købe en lagerkonto eller bruge en lagerkonto fra et separat Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="65d8b-124">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="65d8b-125">Vær opmærksom på funktionen af D-drevet på virtuelle Azure-maskiner.</span><span class="sxs-lookup"><span data-stu-id="65d8b-125">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="65d8b-126">Opbevar ikke dine eksporterede komponentgrupper her permanent.</span><span class="sxs-lookup"><span data-stu-id="65d8b-126">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="65d8b-127">Du kan finde flere oplysninger om midlertidige drev i [Om de midlertidige drev på virtuelle Windows Azure-maskiner](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="65d8b-127">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="65d8b-128">Stop tjenester</span><span class="sxs-lookup"><span data-stu-id="65d8b-128">Stop services</span></span>
<span data-ttu-id="65d8b-129">Brug Fjernskrivebord til at oprette forbindelse til alle computere i miljøet, og stop følgende tjenester i Windows ved hjælp af services.msc:</span><span class="sxs-lookup"><span data-stu-id="65d8b-129">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="65d8b-130">Tjenesten World Wide Web Publishing (på alle AOS-computere)</span><span class="sxs-lookup"><span data-stu-id="65d8b-130">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="65d8b-131">Tjenesten Microsoft Dynamics 365 for Finance and Operations Batch Management (kun på ikke-private AOS-computere)</span><span class="sxs-lookup"><span data-stu-id="65d8b-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="65d8b-132">Tjenesten Management Reporter 2012 Process (kun på BI-computere)</span><span class="sxs-lookup"><span data-stu-id="65d8b-132">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="65d8b-133">Disse tjenester har åbne forbindelser til Dynamics 365 for Finance and Operations-databasen.</span><span class="sxs-lookup"><span data-stu-id="65d8b-133">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="65d8b-134">Nulstil</span><span class="sxs-lookup"><span data-stu-id="65d8b-134">Reset</span></span>
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="65d8b-135">Find og hent den nyeste MinorVersionDataUpgrade.zip-pakke</span><span class="sxs-lookup"><span data-stu-id="65d8b-135">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="65d8b-136">Find den nyeste MinorVersionDataUpgrade.zip-pakke ved hjælp af vejledningen i [Hent den nyeste installerbare dataopgraderingspakke](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="65d8b-136">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> <span data-ttu-id="65d8b-137">Vejledningen beskriver, hvordan du finder og henter den korrekte version af dataopgraderingspakken.</span><span class="sxs-lookup"><span data-stu-id="65d8b-137">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="65d8b-138">Der kræves ikke en opgradering for at hent pakken MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="65d8b-138">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="65d8b-139">Du behøver kun at udføre trinnene i afsnittet "Hent den nyeste installerbare dataopgraderingspakke" uden at udføre nogen af de øvrige trin i artiklen for at hente en kopi af MinorVersionDataUpgrade.zip-pakken.</span><span class="sxs-lookup"><span data-stu-id="65d8b-139">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

#### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="65d8b-140">Udfør scripts mod Finance and Operations-databasen</span><span class="sxs-lookup"><span data-stu-id="65d8b-140">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="65d8b-141">Kør følgende scripts mod Finance and Operations-databasen (ikke mod økonomirapporteringsdatabasen).</span><span class="sxs-lookup"><span data-stu-id="65d8b-141">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="65d8b-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="65d8b-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="65d8b-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="65d8b-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="65d8b-144">Disse scripts sikrer, at brugerne, rollerne og indstillingerne for sporing af ændringer er korrekte.</span><span class="sxs-lookup"><span data-stu-id="65d8b-144">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="65d8b-145">Udfør PowerShell-kommando for at nulstille databasen</span><span class="sxs-lookup"><span data-stu-id="65d8b-145">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="65d8b-146">Følgende kommando skal udføres direkte på AOS-computeren for at nulstille integrationen mellem Finance and Operations og økonomirapporteringen:</span><span class="sxs-lookup"><span data-stu-id="65d8b-146">Execute the following command, directly on the AOS computer, to reset the integration between Finance and Operations and financial reporting:</span></span>

1.  <span data-ttu-id="65d8b-147">Åbn Windows PowerShell som administrator.</span><span class="sxs-lookup"><span data-stu-id="65d8b-147">Open Windows PowerShell as Administrator.</span></span>
2.  <span data-ttu-id="65d8b-148">Udfør: F:</span><span class="sxs-lookup"><span data-stu-id="65d8b-148">Execute: F:</span></span>
3.  <span data-ttu-id="65d8b-149">Udfør: cd F:\\MRApplicationService\\MRInstallDirectory</span><span class="sxs-lookup"><span data-stu-id="65d8b-149">Execute: cd F:\\MRApplicationService\\MRInstallDirectory</span></span>
4.  <span data-ttu-id="65d8b-150">Udfør: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span><span class="sxs-lookup"><span data-stu-id="65d8b-150">Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span></span>
5.  <span data-ttu-id="65d8b-151">Udfør: Reset-DatamartIntegration -Reason OTHER -ReasonDetail "&lt;min årsag til nulstilling&gt;"</span><span class="sxs-lookup"><span data-stu-id="65d8b-151">Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span></span>
    -   <span data-ttu-id="65d8b-152">Du bliver bedt om at indtaste "Y" for at bekræfte.</span><span class="sxs-lookup"><span data-stu-id="65d8b-152">You will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="65d8b-153">Forklaring af parametrene:</span><span class="sxs-lookup"><span data-stu-id="65d8b-153">Explanation of parameters:</span></span>

-   <span data-ttu-id="65d8b-154">De gyldige værdier for -Reason er: SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="65d8b-154">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="65d8b-155">Parameteren -ReasonDetail er fri tekst.</span><span class="sxs-lookup"><span data-stu-id="65d8b-155">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="65d8b-156">Årsag og reasonDetail registreres i telemetri/miljø overvågningen.</span><span class="sxs-lookup"><span data-stu-id="65d8b-156">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="65d8b-157">Start tjenester</span><span class="sxs-lookup"><span data-stu-id="65d8b-157">Start services</span></span>
<span data-ttu-id="65d8b-158">Brug services.msc til at genstarte de tjenester, som du tidligere har stoppet:</span><span class="sxs-lookup"><span data-stu-id="65d8b-158">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="65d8b-159">Tjenesten World Wide Web Publishing (på alle AOS-computere)</span><span class="sxs-lookup"><span data-stu-id="65d8b-159">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="65d8b-160">Tjenesten Microsoft Dynamics 365 for Finance and Operations Batch Management (kun på ikke-private AOS-computere)</span><span class="sxs-lookup"><span data-stu-id="65d8b-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="65d8b-161">Tjenesten Management Reporter 2012 Process (kun på BI-computere)</span><span class="sxs-lookup"><span data-stu-id="65d8b-161">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="65d8b-162">Importer rapportdefinitioner</span><span class="sxs-lookup"><span data-stu-id="65d8b-162">Import report definitions</span></span>
<span data-ttu-id="65d8b-163">Importer dine rapportdesigns fra Report Designer ved hjælp af den fil, der oprettes under eksporten:</span><span class="sxs-lookup"><span data-stu-id="65d8b-163">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="65d8b-164">I Report Designer skal du gå til **Regnskab** &gt; **Komponentgruppe**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-164">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="65d8b-165">Vælg den komponentgruppe, der skal eksporterer, og klik på **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-165">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="65d8b-166">Bemærk: I Finance and Operations understøttes kun én komponentgruppe, **Standard**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-166">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="65d8b-167">Vælg komponenten **Standard**, og klik på **Importer**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-167">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="65d8b-168">Vælg den fil, der indeholder de eksporterede rapportdefinitioner, og klik på **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-168">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="65d8b-169">I dialogboksen Importér skal du vælge de rapportdefinitioner, der skal importeres:</span><span class="sxs-lookup"><span data-stu-id="65d8b-169">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="65d8b-170">Hvis du vil importere alle rapportdefinitioner og de understøttende komponenter, skal du klikke på **Marker alt**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-170">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="65d8b-171">Hvis du vil importere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du markere de rapporter, rækker, kolonner, træer eller dimensionsopsætninger, der skal importeres.</span><span class="sxs-lookup"><span data-stu-id="65d8b-171">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="65d8b-172">Klik på **Importer**.</span><span class="sxs-lookup"><span data-stu-id="65d8b-172">Click **Import**.</span></span>





