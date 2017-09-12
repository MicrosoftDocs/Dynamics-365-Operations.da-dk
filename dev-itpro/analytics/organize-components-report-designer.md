---
title: Organisere rapportkomponenter i Report Designer
description: "Når du har udviklet komponentdokumenter og oprettet rapporter, er det nyttigt at organisere disse objekter, så de er lettere for brugerne at finde. I denne artikel beskrives, hvordan du organiserer eksisterende rapporter, dokumentkomponenter og objekter i Report Designer."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: fade9e2acdb94daa6a908d949c578fd7ed439882
ms.contentlocale: da-dk
ms.lasthandoff: 07/18/2017

---

# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="249c4-104">Organisere rapportkomponenter i Report Designer</span><span class="sxs-lookup"><span data-stu-id="249c4-104">Organize report components in report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="249c4-105">Når du har udviklet komponentdokumenter og oprettet rapporter, er det nyttigt at organisere disse objekter, så de er lettere for brugerne at finde.</span><span class="sxs-lookup"><span data-stu-id="249c4-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="249c4-106">I denne artikel beskrives, hvordan du organiserer eksisterende rapporter, dokumentkomponenter og objekter i Report Designer.</span><span class="sxs-lookup"><span data-stu-id="249c4-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="249c4-107">Du kan omdøbe mapper, rapporter, dokumentkomponenter og andre objekter i Report Designer for at organisere dine filer.</span><span class="sxs-lookup"><span data-stu-id="249c4-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="249c4-108">Afhængigt af hvilken type objekt, du omdøber, skal du muligvis opdatere tilknytninger til det pågældende objekt.</span><span class="sxs-lookup"><span data-stu-id="249c4-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="249c4-109">Omdøbe en mappe eller en dokumentkomponent i Report Designer</span><span class="sxs-lookup"><span data-stu-id="249c4-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="249c4-110">Du kan omdøbe mapper, rapportdefinitioner, rækkedefinitioner, kolonnedefinitioner og rapporteringstrædefinitioner i Report Designer.</span><span class="sxs-lookup"><span data-stu-id="249c4-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span> <span data-ttu-id="249c4-111">**Bemærk:** Når du omdøber en dokumentkomponent, skal du opdatere alle rapportdefinitioner, der bruger dokumentkomponenten.</span><span class="sxs-lookup"><span data-stu-id="249c4-111">**Note:** When you rename a building block, you must update any reporting definitions that use the building block.</span></span> <span data-ttu-id="249c4-112">Ellers kan der ikke oprettes en ny rapport.</span><span class="sxs-lookup"><span data-stu-id="249c4-112">Otherwise, a new report can't be generated.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="249c4-113">Omdøbe en mappe eller en dokumentkomponent i Report Designer</span><span class="sxs-lookup"><span data-stu-id="249c4-113">Rename a folder or building block in Report Designer</span></span>

1.  <span data-ttu-id="249c4-114">I Report Designer kan du bruge navigationsruden til at finde den mappe eller det objekt, der skal omdøbes.</span><span class="sxs-lookup"><span data-stu-id="249c4-114">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2.  <span data-ttu-id="249c4-115">Højreklik på mappen eller objektet, og klik derefter på **Omdøb**.</span><span class="sxs-lookup"><span data-stu-id="249c4-115">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="249c4-116">Feltet **Navn** i navigationsruden bliver tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="249c4-116">The **Name** field in the navigation pane becomes available.</span></span>
3.  <span data-ttu-id="249c4-117">Skriv et nyt navn, og tryk derefter på Enter.</span><span class="sxs-lookup"><span data-stu-id="249c4-117">Type a new name, and then press Enter.</span></span>
4.  <span data-ttu-id="249c4-118">Hvis dokumentkomponenten er en rækkedefinition, kolonnedefinition eller rapporteringstrædefinition, skal du opdatere andre komponenter, der er knyttet til den.</span><span class="sxs-lookup"><span data-stu-id="249c4-118">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="249c4-119">Højreklik på den dokumentkomponent, du omdøbte i trin 3, vælg **Tilknytninger**, og vælg derefter et element på listen for at opdatere det.</span><span class="sxs-lookup"><span data-stu-id="249c4-119">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5.  <span data-ttu-id="249c4-120">Gentag trin 4, indtil alle tilknyttede elementer er opdateret.</span><span class="sxs-lookup"><span data-stu-id="249c4-120">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="249c4-121">Oprette og administrere rapportgrupper</span><span class="sxs-lookup"><span data-stu-id="249c4-121">Create and manage report groups</span></span>
<span data-ttu-id="249c4-122">Du kan gruppere rapportdefinitioner for at generere flere rapporter på samme tid.</span><span class="sxs-lookup"><span data-stu-id="249c4-122">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="249c4-123">Du skal have designer- eller administratorrollen for at oprette, redigere, slette og oprette rapportgrupper.</span><span class="sxs-lookup"><span data-stu-id="249c4-123">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="249c4-124">Brugere, der har generatorrollen, kan generere rapportgrupper og kan også ændre brugerindstillingen for rapportdefinitioner for rapportgrupper.</span><span class="sxs-lookup"><span data-stu-id="249c4-124">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="249c4-125">Oprette en rapportgruppe</span><span class="sxs-lookup"><span data-stu-id="249c4-125">Create a report group</span></span>

1.  <span data-ttu-id="249c4-126">Klik på **Rapportgrupper** i navigationsruden i Report Designer.</span><span class="sxs-lookup"><span data-stu-id="249c4-126">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="249c4-127">I menuen **Filer** skal du klikke på **Ny** &gt; **Rapportgruppedefinition** for at åbne en ny rapportgruppe i fremviservinduet.</span><span class="sxs-lookup"><span data-stu-id="249c4-127">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="249c4-128">Du kan også klikke på knappen **Rapportgruppe** ![Rapportgruppe](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Rapportgruppe") på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="249c4-128">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3.  <span data-ttu-id="249c4-129">Klik på fanen **Rapportgruppe**.</span><span class="sxs-lookup"><span data-stu-id="249c4-129">Click the **Report Group** tab.</span></span> <span data-ttu-id="249c4-130">Hvis du vil tilsidesætte oplysningerne om de enkelte rapportdefinitioner til generering af denne rapport, skal du markere afkrydsningsfeltet **Tilsidesæt regnskab, detaljer og datoindstillinger fra individuelle rapportdefinitioner**.</span><span class="sxs-lookup"><span data-stu-id="249c4-130">To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="249c4-131">Firmanavnet, detaljeringsniveauet, foreløbig-indstillingen og datooplysninger angives automatisk, men du kan stadig foretage opdateringer.</span><span class="sxs-lookup"><span data-stu-id="249c4-131">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4.  <span data-ttu-id="249c4-132">Hvis du vil have genereret flere rapporter, der viser rapporteringsvalutaerne, skal du markere afkrydsningsfeltet **Medtag alle rapporteringsvalutaer**.</span><span class="sxs-lookup"><span data-stu-id="249c4-132">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="249c4-133">Derefter kan du åbne flere visninger ved at klikke på knappen **Valuta** i webfremviseren, når du får vist rapporten.</span><span class="sxs-lookup"><span data-stu-id="249c4-133">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5.  <span data-ttu-id="249c4-134">I feltet **Rapporter i gruppe** skal du klikke på **Tilføj** for at vælge de rapporter, der skal medtages i rapportgruppen.</span><span class="sxs-lookup"><span data-stu-id="249c4-134">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="249c4-135">Hvis du vil vælge flere rapporter i dialogboksen **Tilføj**, skal du holde tasten Ctrl nede, mens du markerer rapporter.</span><span class="sxs-lookup"><span data-stu-id="249c4-135">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="249c4-136">Når du er færdig med at vælge rapporter, skal du klikke på **OK**.</span><span class="sxs-lookup"><span data-stu-id="249c4-136">When you've finished selecting reports, click **OK**.</span></span>
6.  <span data-ttu-id="249c4-137">Klik på **Filer** &gt; **Gem** for at gemme den nye rapportgruppe.</span><span class="sxs-lookup"><span data-stu-id="249c4-137">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="249c4-138">Redigere en rapportgruppe</span><span class="sxs-lookup"><span data-stu-id="249c4-138">Modify a report group</span></span>

1.  <span data-ttu-id="249c4-139">Klik på **Rapportgrupper** i navigationsruden i Report Designer.</span><span class="sxs-lookup"><span data-stu-id="249c4-139">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="249c4-140">Dobbeltklik på den rapportgruppe, der skal redigeres.</span><span class="sxs-lookup"><span data-stu-id="249c4-140">Double-click the report group to modify.</span></span>
3.  <span data-ttu-id="249c4-141">Under fanen **Rapportgruppe** kan du foretage de ønskede ændringer.</span><span class="sxs-lookup"><span data-stu-id="249c4-141">On the **Report Group** tab, make the changes that you want.</span></span>
4.  <span data-ttu-id="249c4-142">I menuen **Filer** skal du klikke på **Gem** for at gemme den ændrede rapportgruppe, eller du kan klikke på knappen **Gem** ![Gem](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Gem") på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="249c4-142">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

<span data-ttu-id="249c4-143">**Bemærk:** Hvis du har planlagt, at rapporter skal genereres med faste intervaller, kan du tilsidesætte disse indstillinger og generere en rapport med det samme.</span><span class="sxs-lookup"><span data-stu-id="249c4-143">**Note:** If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="249c4-144">Generere en rapportgrupperapport</span><span class="sxs-lookup"><span data-stu-id="249c4-144">Generate a report group report</span></span>

1.  <span data-ttu-id="249c4-145">Klik på **Rapportgrupper** i navigationsruden i Report Designer.</span><span class="sxs-lookup"><span data-stu-id="249c4-145">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="249c4-146">Åbn den rapportgruppe, der skal genereres.</span><span class="sxs-lookup"><span data-stu-id="249c4-146">Open the report group to generate.</span></span>
3.  <span data-ttu-id="249c4-147">Klik på knappen **Opret rapport** ![Opret rapport](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Opret rapport") for at oprette rapporter.</span><span class="sxs-lookup"><span data-stu-id="249c4-147">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="249c4-148">Slette en rapportgruppe</span><span class="sxs-lookup"><span data-stu-id="249c4-148">Delete a report group</span></span>

1.  <span data-ttu-id="249c4-149">Klik på **Rapportgrupper** i navigationsruden i Report Designer.</span><span class="sxs-lookup"><span data-stu-id="249c4-149">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="249c4-150">Højreklik på rapportgruppen, og vælg derefter **Slet**.</span><span class="sxs-lookup"><span data-stu-id="249c4-150">Right-click the report group to delete, and then select **Delete**.</span></span>
3.  <span data-ttu-id="249c4-151">Klik på **Ja**, når der vises en bekræftelsesmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="249c4-151">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="249c4-152">Fanebladskontrolelementer til Rapportgruppe</span><span class="sxs-lookup"><span data-stu-id="249c4-152">Report Group tab controls</span></span>
<span data-ttu-id="249c4-153">Følgende tabel indeholder beskrivelser af kontrolelementerne under fanen **Rapportgruppe**.</span><span class="sxs-lookup"><span data-stu-id="249c4-153">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="249c4-154">Styring</span><span class="sxs-lookup"><span data-stu-id="249c4-154">Control</span></span></th>
<th><span data-ttu-id="249c4-155">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="249c4-155">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="249c4-156">Tilsidesætte regnskab, detaljer og datoindstillinger fra individuelle rapportdefinitioner</span><span class="sxs-lookup"><span data-stu-id="249c4-156">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="249c4-157">Markér dette afkrydsningsfelt for at tilsidesætte individuelle rapportdefinitioner af rapporterne i denne rapportgruppe udelukkende i forbindelse med oprettelse af disse rapporter.</span><span class="sxs-lookup"><span data-stu-id="249c4-157">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="249c4-158">Firmanavn</span><span class="sxs-lookup"><span data-stu-id="249c4-158">Company name</span></span></td>
<td><span data-ttu-id="249c4-159">Vælg det regnskab, der skal bruges til rapporterne.</span><span class="sxs-lookup"><span data-stu-id="249c4-159">Select the company to use for the reports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="249c4-160">Detaljeringsniveau</span><span class="sxs-lookup"><span data-stu-id="249c4-160">Detail level</span></span></td>
<td><span data-ttu-id="249c4-161">Angiv det detaljeringsniveau, som rapporterne indeholder.</span><span class="sxs-lookup"><span data-stu-id="249c4-161">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="249c4-162"><strong>Finansiel</strong>– en oversigtsrapport på højt niveau.</span><span class="sxs-lookup"><span data-stu-id="249c4-162"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="249c4-163">Du kan ikke rulle ned til konti og dimensioner, med undtagelse af de konti og dimensioner, der er tilføjet via et rapporteringstræ.</span><span class="sxs-lookup"><span data-stu-id="249c4-163">You can't drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="249c4-164"><strong>Finans og konto</strong> – en rapport, der indeholder en oversigt på højt niveau og kontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="249c4-164"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="249c4-165"><strong>Finans, Konto og Transaktion</strong> – en rapport, der indeholder en oversigt på højt niveau og transaktionsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="249c4-165"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="249c4-166">Midlertidig</span><span class="sxs-lookup"><span data-stu-id="249c4-166">Provisional</span></span></td>
<td><span data-ttu-id="249c4-167">Angiv de aktivitetstyper, som rapporterne indeholder.</span><span class="sxs-lookup"><span data-stu-id="249c4-167">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="249c4-168"><strong>Kun bogført aktivitet</strong> − Omfatter kun de transaktioner og saldi, der er bogført i dine finansielle data.</span><span class="sxs-lookup"><span data-stu-id="249c4-168"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="249c4-169"><strong>Bogført og ikke-bogført aktivitet</strong> − Omfatter alle de transaktioner og saldi, der er indtastet og bogført i dine finansielle data.</span><span class="sxs-lookup"><span data-stu-id="249c4-169"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="249c4-170"><strong>Kun ikke-bogført aktivitet</strong> − Omfatter kun de transaktioner, der er indtastet men ikke bogført i dine finansielle data.</span><span class="sxs-lookup"><span data-stu-id="249c4-170"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="249c4-171">Medtag alle rapporteringsvalutaer</span><span class="sxs-lookup"><span data-stu-id="249c4-171">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="249c4-172">Hvis der konfigureres yderligere rapporteringsvalutaer i Microsoft Dynamics ERP-systemet, vises de her.</span><span class="sxs-lookup"><span data-stu-id="249c4-172">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="249c4-173">Markér dette afkrydsningsfelt for at få genereret flere rapporter i de angivne valutaer.</span><span class="sxs-lookup"><span data-stu-id="249c4-173">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="249c4-174">Du kan få vist disse rapporter i webfremviseren ved at klikke på knappen <strong>Valuta</strong> og derefter vælge en valuta.</span><span class="sxs-lookup"><span data-stu-id="249c4-174">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="249c4-175">Datooplysninger gemmes ikke sammen med rapportdefinitionen</span><span class="sxs-lookup"><span data-stu-id="249c4-175">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="249c4-176">Basisperiode</span><span class="sxs-lookup"><span data-stu-id="249c4-176">Base period</span></span></li>
<li><span data-ttu-id="249c4-177">Basisår</span><span class="sxs-lookup"><span data-stu-id="249c4-177">Base year</span></span></li>
<li><span data-ttu-id="249c4-178">Periode, der er omfattet</span><span class="sxs-lookup"><span data-stu-id="249c4-178">Period covered</span></span></li>
</ul>
<span data-ttu-id="249c4-179">Kun indstillinger for standardbasisperiode gemmes sammen med rapportdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="249c4-179">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="249c4-180">Datooplysninger, der er gemt sammen med rapportdefinitionen</span><span class="sxs-lookup"><span data-stu-id="249c4-180">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="249c4-181">Rapportdato</span><span class="sxs-lookup"><span data-stu-id="249c4-181">Report date</span></span></li>
<li><span data-ttu-id="249c4-182">Standardbasisperiode</span><span class="sxs-lookup"><span data-stu-id="249c4-182">Default base period</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="249c4-183">Rapporter i gruppe</span><span class="sxs-lookup"><span data-stu-id="249c4-183">Reports in group</span></span></td>
<td><span data-ttu-id="249c4-184">Tilføje, fjerne og ændre rækkefølgen af rapporter i rapportgruppen.</span><span class="sxs-lookup"><span data-stu-id="249c4-184">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="249c4-185">Hvis du vil tilføje rapportdefinitioner til rapportgruppen, skal du dobbeltklikke på rapportgruppen for at åbne den og derefter klikke på <strong>Tilføj</strong>.</span><span class="sxs-lookup"><span data-stu-id="249c4-185">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="249c4-186">Markér de rapporter, der skal medtages i rapportgruppen, og klik derefter på <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="249c4-186">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="249c4-187">Hvis du vil fjerne en rapport fra rapportgruppen, skal du markere den og derefter klikke på <strong>Fjern</strong>.</span><span class="sxs-lookup"><span data-stu-id="249c4-187">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="249c4-188">Hvis du vil ændre den rækkefølge, rapporterne genereres i, skal du vælge en rapport på listen og derefter klikke på <strong>Flyt op</strong> eller <strong>Flyt ned</strong>.</span><span class="sxs-lookup"><span data-stu-id="249c4-188">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="249c4-189">Se også</span><span class="sxs-lookup"><span data-stu-id="249c4-189">See also</span></span>
--------

[<span data-ttu-id="249c4-190">Økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="249c4-190">Financial reporting</span></span>](financial-reporting-intro.md)




