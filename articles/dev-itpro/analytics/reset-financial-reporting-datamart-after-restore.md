---
title: "Nulstille datacenteret Økonomirapportering"
description: "Dette emne beskriver, hvordan du nulstiller datacenteret Økonomirapportering."
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="3e546-103">Nulstille datacenteret Økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="3e546-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3e546-104">I dette emne forklares, hvordan du nulstiller datacenteret Økonomirapportering for følgende versioner:</span><span class="sxs-lookup"><span data-stu-id="3e546-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="3e546-105">Version 7.2.6.0 og nyere versioner af Økonomirapportering til Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3e546-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="3e546-106">Version 7.0.10000.4 og nyere versioner af Økonomirapportering til Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3e546-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="3e546-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (lokal installation)</span><span class="sxs-lookup"><span data-stu-id="3e546-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="3e546-108">Hvis du vil have Økonomirapportering version 7.2.6.0 til Finance and Operations, kan du hente KB 4052514 fra <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span><span class="sxs-lookup"><span data-stu-id="3e546-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="3e546-109">Nulstille datacenteret Økonomirapportering for version 7.2.6.0 og nyere versioner af Økonomirapportering til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3e546-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="3e546-110">Nulstille datacenteret Økonomirapportering fra Rapportdesigner</span><span class="sxs-lookup"><span data-stu-id="3e546-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="3e546-111">Trinnene i denne proces understøttes i version 7.2.6.0 og nyere versioner af Økonomirapportering til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3e546-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="3e546-112">Hvis du har en tidligere version, kan du kontakte supportteamet for at få hjælp.</span><span class="sxs-lookup"><span data-stu-id="3e546-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="3e546-113">Du skal muligvis nulstille datacenteret for økonomirapportering i bestemte scenarier.</span><span class="sxs-lookup"><span data-stu-id="3e546-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="3e546-114">Du kan udføre denne opgave i Rapportdesigner-klienten.</span><span class="sxs-lookup"><span data-stu-id="3e546-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="3e546-115">Her er nogle scenarier, hvor du muligvis skal nulstille datacenteret:</span><span class="sxs-lookup"><span data-stu-id="3e546-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="3e546-116">Finance and Operations-databasen blev gendannet, men databasen for datacenteret blev ikke gendannet.</span><span class="sxs-lookup"><span data-stu-id="3e546-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="3e546-117">Der vises forkerte data for en periode.</span><span class="sxs-lookup"><span data-stu-id="3e546-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="3e546-118">Support råder dig til at nulstille datacenteret som en del af et fejlfindingstrin.</span><span class="sxs-lookup"><span data-stu-id="3e546-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="3e546-119">Nulstillingen af datacenteret bør kun udføres på tidspunkter, hvor mængden af data, der behandles i databasen, er lille.</span><span class="sxs-lookup"><span data-stu-id="3e546-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="3e546-120">Økonomirapportering er ikke tilgængelig i forbindelse med nulstilling.</span><span class="sxs-lookup"><span data-stu-id="3e546-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="3e546-121">Nulstil datacenteret</span><span class="sxs-lookup"><span data-stu-id="3e546-121">Reset the data mart</span></span>

<span data-ttu-id="3e546-122">Når du vil nulstille datacenteret, skal du i menuen **Værktøjer** i Rapportdesigner vælge **Nulstil datacenter**.</span><span class="sxs-lookup"><span data-stu-id="3e546-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="3e546-123">Den viste dialogboks har to sektioner: **Statistik** og **Nulstil**.</span><span class="sxs-lookup"><span data-stu-id="3e546-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="3e546-124">[![Dialogboksen Nulstil datacenter](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="3e546-124">[![Reset Data Mart dialog box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="3e546-125">Integrationsforsøg</span><span class="sxs-lookup"><span data-stu-id="3e546-125">Integration attempts</span></span>

<span data-ttu-id="3e546-126">Gitteret **Integrationsforsøg** viser, hvor mange gange systemet har forsøgt at integrere posteringer.</span><span class="sxs-lookup"><span data-stu-id="3e546-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="3e546-127">Systemet fortsætter med at forsøge at integrere data i en periode på flere dage, hvis de første forsøg ikke lykkes.</span><span class="sxs-lookup"><span data-stu-id="3e546-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="3e546-128">Du ved, at datacenteret skal nulstilles, hvis antallet af forsøg er 8 eller derover, og hvis der er mange dimensionskombinations- eller transaktionsposter.</span><span class="sxs-lookup"><span data-stu-id="3e546-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="3e546-129">I så fald skal der ikke rapporteres om dataene.</span><span class="sxs-lookup"><span data-stu-id="3e546-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="3e546-130">Datastatus</span><span class="sxs-lookup"><span data-stu-id="3e546-130">Data status</span></span>

<span data-ttu-id="3e546-131">Gitteret **Datastatus** indeholder et øjebliksbillede af transaktionerne, kurserne og dimensionsværdierne i datacenteret.</span><span class="sxs-lookup"><span data-stu-id="3e546-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="3e546-132">Et stort antal forældede poster angiver, at der er foretaget mange opdateringer af posterne.</span><span class="sxs-lookup"><span data-stu-id="3e546-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="3e546-133">Det kan medføre længere rapportgenereringstider.</span><span class="sxs-lookup"><span data-stu-id="3e546-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="3e546-134">Hovedkontokategorier, der ikke er justeret korrekt</span><span class="sxs-lookup"><span data-stu-id="3e546-134">Misaligned main account categories</span></span>

<span data-ttu-id="3e546-135">Hvis du bruger en version, der er ældre end Økonomirapportering version 7.2.1 til Microsoft Dynamics 365 for Finance and Operations, kan du muligvis nulstille datacenteret, hvis du omdøber konti og flytter konti fra en kontokategori til en anden.</span><span class="sxs-lookup"><span data-stu-id="3e546-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="3e546-136">Disse handlinger kan medføre, at hovedkontokategorier bliver justeret forkert.</span><span class="sxs-lookup"><span data-stu-id="3e546-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="3e546-137">Feltet **Hovedkontokategorier, der ikke er justeret korrekt** viser, om du oplever dette problem.</span><span class="sxs-lookup"><span data-stu-id="3e546-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="3e546-138">Nulstille datacenteret i Økonomirapportering version 7.2.6.0 til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3e546-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="3e546-139">Hvis du vil nulstille datacenteret i version 7.2.6.0 og tidligere versioner af Økonomirapportering til Finance and Operations, skal du i dialogboksen **Nulstil datacenter** markere afkrydsningsfeltet **Nulstil datacenter** og derefter vælger **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e546-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="3e546-140">Nulstil kun datacenteret under planlagt nedetid.</span><span class="sxs-lookup"><span data-stu-id="3e546-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="3e546-141">[![Afkrydsningsfeltet Nulstil datacenter](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="3e546-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="3e546-142">Nulstil datacenteret, og vælg en årsag i Økonomirapportering version 7.3.0 til Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3e546-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="3e546-143">Hvis du konstaterer, at der kræves en nulstilling af datacenteret, kan du markere afkrydsningsfeltet **Nulstil datacenter** og derefter vælge en årsag i feltet **Årsag**.</span><span class="sxs-lookup"><span data-stu-id="3e546-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="3e546-144">Følgende valgmuligheder er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="3e546-144">The following options are available:</span></span>

- <span data-ttu-id="3e546-145">**Manglende eller forkerte data** – Baseret på statistikken, har du konstateret, at der sandsynligvis mangler data.</span><span class="sxs-lookup"><span data-stu-id="3e546-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="3e546-146">Før du fortsætter, anbefaler vi, at du samarbejder med Support om at bestemme den egentlige årsag.</span><span class="sxs-lookup"><span data-stu-id="3e546-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="3e546-147">**Gendan database** – Finance and Operations-databasen blev gendannet, men databasen for datacenteret Økonomirapportering blev ikke gendannet.</span><span class="sxs-lookup"><span data-stu-id="3e546-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="3e546-148">**Andet** – Du er ved at nulstille datacenteret af anden årsag.</span><span class="sxs-lookup"><span data-stu-id="3e546-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="3e546-149">Hvis du mener, at der er et problem, kan du kontakte Support for at identificere det.</span><span class="sxs-lookup"><span data-stu-id="3e546-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

<span data-ttu-id="3e546-150">[![Nulstil datacenter](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="3e546-150">[![Reset data mart](./media/Integration.png)](./media/Integration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="3e546-151">Kontroller, at alle opgaver i datacenteret har fuldført en oprindelige belastning, før du starter en nulstilling.</span><span class="sxs-lookup"><span data-stu-id="3e546-151">Verify that all data mart reset tasks have completed an initial load before you begin a reset.</span></span> <span data-ttu-id="3e546-152">Du kan kontrollere dette ved at søge efter en værdi i kolonnen Tidspunkt for seneste kørsel ved at vælge **Værktøjer** &gt; **Integrationsstatus**.</span><span class="sxs-lookup"><span data-stu-id="3e546-152">You can confirm this by looking for a value in the Last Runtime column by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="3e546-153">Ryd brugere og firmaer</span><span class="sxs-lookup"><span data-stu-id="3e546-153">Clear users and companies</span></span>

<span data-ttu-id="3e546-154">Marker afkrydsningsfeltet **Ryd brugere og firmaer**, hvis du har gendannet databasen, men derefter har foretaget ændringer af brugere eller virksomheder.</span><span class="sxs-lookup"><span data-stu-id="3e546-154">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="3e546-155">Det skulle ikke være nødvendigt at markere dette afkrydsningsfelt ofte.</span><span class="sxs-lookup"><span data-stu-id="3e546-155">You should rarely have to select this check box.</span></span>

<span data-ttu-id="3e546-156">Når du er klar til at starte nulstillingsprocessen, skal du vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e546-156">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="3e546-157">Du bliver bedt om at bekræfte, at du er klar til at starte processen.</span><span class="sxs-lookup"><span data-stu-id="3e546-157">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="3e546-158">Bemærk, at Økonomirapportering ikke er tilgængelig under nulstillingen og den indledende dataintegration, der foretages bagefter.</span><span class="sxs-lookup"><span data-stu-id="3e546-158">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="3e546-159">Hvis du vil kontrollere status for integrationen, skal du vælge **Værktøjer** &gt; **Integrationsstatus** at se sidst integrationen blev kørt og status.</span><span class="sxs-lookup"><span data-stu-id="3e546-159">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="3e546-160">[![Få vist status for integrationen](./media/New-integration.PNG)](./media/New-integration.PNG)</span><span class="sxs-lookup"><span data-stu-id="3e546-160">[![View the status of the integration](./media/New-integration.PNG)](./media/New-integration.PNG)</span></span>

> [!NOTE]
> <span data-ttu-id="3e546-161">Nulstillingen er afsluttet, når alle tilknytninger viser status for RanToCompletion, og der i vinduet Integrationsstatus står "Integration fuldført" i nederste venstre hjørne.</span><span class="sxs-lookup"><span data-stu-id="3e546-161">The reset is finished when all mappings show the status of RanToCompletion and the Integration Status window says “Integration complete” in the bottom-left corner.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="3e546-162">Nulstille datacenteret Økonomirapportering version 7.0.10000.4 og nyere versioner af Økonomirapportering til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3e546-162">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="3e546-163">Hvis du på et tidspunkt vil gendanne din Finance and Operations-database fra en sikkerhedskopi eller kopiere databasen fra et andet miljø, skal du følge trinnene i dette afsnit for at prøve at sikre, at datacenteret Økonomirapportering bruger den gendannede Finance and Operations-database korrekt.</span><span class="sxs-lookup"><span data-stu-id="3e546-163">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="3e546-164">Trinene i processen understøttes for Microsoft Dynamics AX-programversion 7.0.1 (maj 2016) (programbuild 7.0.1265.23014 og Økonomirapportering build 7.0.10000.4) og nyere versioner.</span><span class="sxs-lookup"><span data-stu-id="3e546-164">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="3e546-165">Hvis du har en tidligere version af Finance and Operations, skal du kontakte vores Support for at få hjælp.</span><span class="sxs-lookup"><span data-stu-id="3e546-165">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="3e546-166">Eksporter rapportdefinitioner</span><span class="sxs-lookup"><span data-stu-id="3e546-166">Export report definitions</span></span>

<span data-ttu-id="3e546-167">Følg først disse trin for at eksportere dine rapportdesign fra Rapportdesigneren.</span><span class="sxs-lookup"><span data-stu-id="3e546-167">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="3e546-168">I Reportdesigner skal du vælge **Regnskab** &gt; **Rapportkomponentgrupper**.</span><span class="sxs-lookup"><span data-stu-id="3e546-168">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="3e546-169">Vælg den rapportkomponentgruppe, der skal eksporteres, og vælg derefter **Eksportér**.</span><span class="sxs-lookup"><span data-stu-id="3e546-169">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3e546-170">Bemærk: I Finance and Operations understøttes kun én komponentgruppe, **Standard**.</span><span class="sxs-lookup"><span data-stu-id="3e546-170">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="3e546-171">Vælg de rapportdefinitioner, der skal eksporteres:</span><span class="sxs-lookup"><span data-stu-id="3e546-171">Select the report definitions to export:</span></span>

    - <span data-ttu-id="3e546-172">Hvis du vil eksportere alle dine rapportdefinitioner og de tilknyttede rapportkomponenter, skal du vælge **Markér alt**.</span><span class="sxs-lookup"><span data-stu-id="3e546-172">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="3e546-173">Hvis du vil eksportere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du vælge den relevante fane og derefter vælge de elementer, der skal eksporteres.</span><span class="sxs-lookup"><span data-stu-id="3e546-173">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="3e546-174">Tryk på og hold Ctrl-tasten nede for at vælge flere elementer under en fane. Når du vælger rapporter til eksport, vælges de tilknyttede rækker, kolonner, træer og dimensionsopsætninger.</span><span class="sxs-lookup"><span data-stu-id="3e546-174">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="3e546-175">Vælg **Eksportér**.</span><span class="sxs-lookup"><span data-stu-id="3e546-175">Select **Export**.</span></span>
5. <span data-ttu-id="3e546-176">Angiv et filnavn, og vælg et sikkert sted, hvor du vil gemme de eksporterede rapportdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="3e546-176">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="3e546-177">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="3e546-177">Select **Save**.</span></span>

<span data-ttu-id="3e546-178">Du kan kopiere eller overføre filen til et sikkert sted.</span><span class="sxs-lookup"><span data-stu-id="3e546-178">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="3e546-179">På denne måde kan filen importeres til et andet miljø senere.</span><span class="sxs-lookup"><span data-stu-id="3e546-179">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="3e546-180">Du kan finde oplysninger om, hvordan du bruger en Microsoft Azure-lagerkonto, i [Overfør data med AzCopy-kommandolinjeværktøjet](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="3e546-180">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="3e546-181">Microsoft leverer ikke en lagerkonto som en del af din Finance and Operations-aftale.</span><span class="sxs-lookup"><span data-stu-id="3e546-181">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="3e546-182">Du skal købe en lagerkonto eller bruge en lagerkonto fra et separat Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="3e546-182">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="3e546-183">Vær opmærksom på funktionen af D-drevet på virtuelle Azure-maskiner (VM'er).</span><span class="sxs-lookup"><span data-stu-id="3e546-183">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="3e546-184">Gem ikke permanent dine eksporterede rapportkomponentgrupper på drev D. Du kan finde flere oplysninger om midlertidige drev i [Om de midlertidige drev på virtuelle Windows Azure-maskiner](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="3e546-184">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="3e546-185">Stop tjenester</span><span class="sxs-lookup"><span data-stu-id="3e546-185">Stop services</span></span>

<span data-ttu-id="3e546-186">Følgende Microsoft Windows-tjenester har åbne forbindelser til Finance and Operations-databasen.</span><span class="sxs-lookup"><span data-stu-id="3e546-186">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="3e546-187">Derfor skal du bruge Microsoft Fjernskrivebord til at oprette forbindelse til alle computere i miljøet og derefter bruge services.msc til at stoppe disse tjenester.</span><span class="sxs-lookup"><span data-stu-id="3e546-187">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="3e546-188">Tjenesten World Wide Web Publishing (på alle AOS-computere [Applikationsobjektservere])</span><span class="sxs-lookup"><span data-stu-id="3e546-188">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="3e546-189">Tjenesten Microsoft Dynamics 365 for Finance and Operations Batch Management (kun på ikke-private AOS-computere)</span><span class="sxs-lookup"><span data-stu-id="3e546-189">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="3e546-190">Tjenesten Management Reporter 2012 Process (kun på Business Intelligence-computere [BI])</span><span class="sxs-lookup"><span data-stu-id="3e546-190">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="3e546-191">Nulstil</span><span class="sxs-lookup"><span data-stu-id="3e546-191">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="3e546-192">Download den nyeste MinorVersionDataUpgrade.zip-pakke</span><span class="sxs-lookup"><span data-stu-id="3e546-192">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="3e546-193">Download den nyeste MinorVersionDataUpgrade.zip-pakke.</span><span class="sxs-lookup"><span data-stu-id="3e546-193">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="3e546-194">Du kan finde oplysninger om, hvordan du finder og henter den korrekte version af dataopgraderingspakken, under [Hent den nyeste installerbare dataopgraderingspakke](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="3e546-194">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> 

<span data-ttu-id="3e546-195">Der kræves ikke en opgradering for at hente pakken MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="3e546-195">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="3e546-196">Derfor skal du bare følge trinnene i afsnittet "Hent den nyeste installerbare dataopgraderingspakke" i det pågældende emne.</span><span class="sxs-lookup"><span data-stu-id="3e546-196">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="3e546-197">Du kan springe alle de andre trin i emnet over.</span><span class="sxs-lookup"><span data-stu-id="3e546-197">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="3e546-198">Køre scripts mod Finance and Operations-databasen</span><span class="sxs-lookup"><span data-stu-id="3e546-198">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="3e546-199">Kør følgende scripts mod Finance and Operations-databasen (ikke mod Økonomirapportering-databasen):</span><span class="sxs-lookup"><span data-stu-id="3e546-199">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="3e546-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="3e546-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="3e546-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="3e546-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="3e546-202">Disse scripts er med til at sikre, at brugerne, rollerne og indstillingerne for sporing af ændringer er korrekte.</span><span class="sxs-lookup"><span data-stu-id="3e546-202">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="3e546-203">Køre en Windows PowerShell-kommando for at nulstille databasen</span><span class="sxs-lookup"><span data-stu-id="3e546-203">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="3e546-204">På AOS-computeren skal du starte Microsoft Windows PowerShell som administrator og udføre følgende kommandoer for at nulstille integrationen mellem Finance and Operations og Økonomirapportering.</span><span class="sxs-lookup"><span data-stu-id="3e546-204">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="3e546-205">Her er en forklaring på parametrene i kommandoen **Reset-DatamartIntegration**:</span><span class="sxs-lookup"><span data-stu-id="3e546-205">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="3e546-206">De gyldige værdier for **-Reason** er: **SERVICING**, **BADDATA** og **OTHER**.</span><span class="sxs-lookup"><span data-stu-id="3e546-206">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="3e546-207">Parameteren **-ReasonDetail** er fri tekst.</span><span class="sxs-lookup"><span data-stu-id="3e546-207">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="3e546-208">Årsagen og detaljer om årsagen registreres i telemetri/miljøovervågningen.</span><span class="sxs-lookup"><span data-stu-id="3e546-208">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="3e546-209">Når du har kørt kommandoerne, bliver du bedt om at angive **Y** for at bekræfte, at du vil nulstille databasen.</span><span class="sxs-lookup"><span data-stu-id="3e546-209">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="3e546-210">Genstart tjenester</span><span class="sxs-lookup"><span data-stu-id="3e546-210">Restart services</span></span>

<span data-ttu-id="3e546-211">Brug services.msc til at genstarte de tjenester, som du tidligere har stoppet:</span><span class="sxs-lookup"><span data-stu-id="3e546-211">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="3e546-212">Tjenesten World Wide Web Publishing (på alle AOS-computere)</span><span class="sxs-lookup"><span data-stu-id="3e546-212">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="3e546-213">Tjenesten Microsoft Dynamics 365 for Finance and Operations Batch Management (kun på ikke-private AOS-computere)</span><span class="sxs-lookup"><span data-stu-id="3e546-213">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="3e546-214">Tjenesten Management Reporter 2012 Process (kun på BI-computere)</span><span class="sxs-lookup"><span data-stu-id="3e546-214">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="3e546-215">Importer rapportdefinitioner</span><span class="sxs-lookup"><span data-stu-id="3e546-215">Import report definitions</span></span>

<span data-ttu-id="3e546-216">Importer dine rapportdesigns fra Reportdesigner ved hjælp af den fil, der blev oprettet under eksporten.</span><span class="sxs-lookup"><span data-stu-id="3e546-216">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="3e546-217">I Reportdesigner skal du vælge **Regnskab** &gt; **Rapportkomponentgrupper**.</span><span class="sxs-lookup"><span data-stu-id="3e546-217">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="3e546-218">Vælg den rapportkomponentgruppe, der skal eksporteres, og vælg derefter **Eksportér**.</span><span class="sxs-lookup"><span data-stu-id="3e546-218">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3e546-219">Bemærk: I Finance and Operations understøttes kun én komponentgruppe, **Standard**.</span><span class="sxs-lookup"><span data-stu-id="3e546-219">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="3e546-220">Vælg komponenten **Standard**, og vælg derefter **Importer**.</span><span class="sxs-lookup"><span data-stu-id="3e546-220">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="3e546-221">Vælg den fil, der indeholder de eksporterede rapportdefinitioner, og vælg derefter **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="3e546-221">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="3e546-222">Vælg de rapportdefinitioner, der skal importeres, i dialogboksen **Importér**:</span><span class="sxs-lookup"><span data-stu-id="3e546-222">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="3e546-223">Hvis du vil importere alle rapportdefinitionerne og de tilknyttede rapportkomponenter, skal du vælge **Markér alt**.</span><span class="sxs-lookup"><span data-stu-id="3e546-223">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="3e546-224">Hvis du vil importere bestemte rapporter, rækker, kolonner, træer eller dimensionsgrupper, skal du markere de rapporter, rækker, kolonner, træer eller dimensionsgrupper, der skal importeres.</span><span class="sxs-lookup"><span data-stu-id="3e546-224">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="3e546-225">Vælg **Importér**.</span><span class="sxs-lookup"><span data-stu-id="3e546-225">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="3e546-226">Nulstille datacenteret Økonomirapportering til Finance and Operations (til det lokale miljø)</span><span class="sxs-lookup"><span data-stu-id="3e546-226">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="3e546-227">Bed alle brugere om at afslutte Reportdesigner og området Økonomirapportering i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3e546-227">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="3e546-228">Kør følgende script mod Økonomirapportering-databasen (MRDB).</span><span class="sxs-lookup"><span data-stu-id="3e546-228">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. <span data-ttu-id="3e546-229">Afkort eller slet alle poster fra tabellen FINANCIALREPORTS i Finance and Operations-databasen (AXDB).</span><span class="sxs-lookup"><span data-stu-id="3e546-229">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="3e546-230">Afkort eller slet alle poster fra tabellen FINANCIALREPORTVERSION, hvis denne tabel finde i Finance and Operations-databasen.</span><span class="sxs-lookup"><span data-stu-id="3e546-230">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="3e546-231">Hvis tabellen ikke findes i Finance and Operations-databasen, kan du springe dette trin over.</span><span class="sxs-lookup"><span data-stu-id="3e546-231">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="3e546-232">Kør scriptet **ResetDatamart.sql** mod Økonomirapportering-databasen.</span><span class="sxs-lookup"><span data-stu-id="3e546-232">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="3e546-233">Dette script deaktiverer datacenterintegrationen, sletter alle data i datacenteret og genaktiverer derefter datacenterets dataintegration.</span><span class="sxs-lookup"><span data-stu-id="3e546-233">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. <span data-ttu-id="3e546-234">Efter nulstillingen kan du manuelt kontrollere genindlæsningen af dataene ved at køre følgende forespørgsel mod Økonomirapportering-databasen.</span><span class="sxs-lookup"><span data-stu-id="3e546-234">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="3e546-235">Bekræft, at alle rækker har en **LastRunTime**-værdi, og at **StateType** er indstillet til **5**.</span><span class="sxs-lookup"><span data-stu-id="3e546-235">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="3e546-236">En **StateType**-værdi på **5** angiver, at dataene blev genindlæst korrekt.</span><span class="sxs-lookup"><span data-stu-id="3e546-236">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="3e546-237">En værdi på **7** angiver en fejltilstand.</span><span class="sxs-lookup"><span data-stu-id="3e546-237">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="3e546-238">Nogle gange har tilknytningen af organisationshierarkiet denne tilstand ved første kørsel.</span><span class="sxs-lookup"><span data-stu-id="3e546-238">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="3e546-239">Dog skulle fejltilstanden blive afhjulpet automatisk.</span><span class="sxs-lookup"><span data-stu-id="3e546-239">However, the faulted state but should be automatically resolved.</span></span>

