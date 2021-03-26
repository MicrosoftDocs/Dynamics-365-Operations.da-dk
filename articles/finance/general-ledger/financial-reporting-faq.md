---
title: Ofte stillede spørgsmål vedrørende Økonomirapportering
description: Dette emne indeholder en oversigt over spørgsmål vedrørende økonomirapportering, som andre brugere har haft.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2d49213ea18e09f04b026559bdca49fee1de0ef7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249295"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="10703-103">Ofte stillede spørgsmål vedrørende Økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="10703-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="10703-104">Dette emne indeholder en oversigt over spørgsmål vedrørende økonomirapportering, som andre brugere har haft.</span><span class="sxs-lookup"><span data-stu-id="10703-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="10703-105">Hvordan begrænser jeg adgangen til en rapport ved hjælp af sikkerhedstræet?</span><span class="sxs-lookup"><span data-stu-id="10703-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="10703-106">Scenario: USMF-demofirmaet har en finansbalancerapport, som ikke ønsker, at alle brugere af økonomirapportering skal kunne se i D365.</span><span class="sxs-lookup"><span data-stu-id="10703-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="10703-107">Løsning: Du kan bruge sikkerhedstræet til at begrænse adgangen til en enkelt rapport, så kun bestemte brugere kan få adgang til rapporten.</span><span class="sxs-lookup"><span data-stu-id="10703-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="10703-108">Log på Rapportdesigner til økonomirapporter</span><span class="sxs-lookup"><span data-stu-id="10703-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="10703-109">Opret en ny trædiagramdefinition (Fil | Ny | Trædiagramdefinition) a.</span><span class="sxs-lookup"><span data-stu-id="10703-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="10703-110">Dobbeltklik på linjen **Oversigt** i kolonnen **Enhedssikkerhed**.</span><span class="sxs-lookup"><span data-stu-id="10703-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="10703-111">i.</span><span class="sxs-lookup"><span data-stu-id="10703-111">i.</span></span>    <span data-ttu-id="10703-112">Klik på Brugere og Grupper.</span><span class="sxs-lookup"><span data-stu-id="10703-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="10703-113">1. Vælg de brugere eller grupper, som skal have adgang til denne rapport.</span><span class="sxs-lookup"><span data-stu-id="10703-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="10703-114">[![brugerskærm](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="10703-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="10703-115">[![sikkerhedsskærm](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="10703-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="10703-116">b.</span><span class="sxs-lookup"><span data-stu-id="10703-116">b.</span></span>    <span data-ttu-id="10703-117">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="10703-117">Click **Save**.</span></span>
  
<span data-ttu-id="10703-118">[![knappen Gem](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="10703-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="10703-119">Tilføj den nye trædiagramdefinition i rapportdefinitionen</span><span class="sxs-lookup"><span data-stu-id="10703-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="10703-120">[![trædiagramdefinition, formular](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="10703-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="10703-121">A.</span><span class="sxs-lookup"><span data-stu-id="10703-121">A.</span></span>  <span data-ttu-id="10703-122">I trædiagramdefinitionen skal du klikke på Indstilling og under "Valg af rapporteringsenhed" og "Medtag alle enheder"</span><span class="sxs-lookup"><span data-stu-id="10703-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="10703-123">[![formular til valg af rapporteringsenhed](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="10703-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="10703-124">**Før:** [![før skærmbillede](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="10703-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="10703-125">**Efter:** [![efter skærmbillede](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="10703-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="10703-126">Bemærk: Årsagen til ovenstående meddelelse er, at min bruger ikke har adgang til rapporten, efter at der har anvendt enhedssikkerhed</span><span class="sxs-lookup"><span data-stu-id="10703-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="10703-127">Hvordan kan jeg bestemme, hvilke konti der ikke svarer til mine saldi i D365?</span><span class="sxs-lookup"><span data-stu-id="10703-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="10703-128">Når du har en rapport, der ikke svarer til det, du ville forvente i D365, kan du gøre følgende for at identificere disse konti og afvigelserne.</span><span class="sxs-lookup"><span data-stu-id="10703-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="10703-129">I Rapportdesigner til økonomirapporter</span><span class="sxs-lookup"><span data-stu-id="10703-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="10703-130">Opret en ny rækkedefinition a.</span><span class="sxs-lookup"><span data-stu-id="10703-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="10703-131">Klik på Rediger | Indsæt rækker fra dimensioner i.</span><span class="sxs-lookup"><span data-stu-id="10703-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="10703-132">Vælg MainAccount [![Vælg hovedkontoskærm](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="10703-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="10703-133">ii.</span><span class="sxs-lookup"><span data-stu-id="10703-133">ii.</span></span> <span data-ttu-id="10703-134">Klik på Ok b.</span><span class="sxs-lookup"><span data-stu-id="10703-134">Click Ok b.</span></span>    <span data-ttu-id="10703-135">Gem rækkedefinitionen</span><span class="sxs-lookup"><span data-stu-id="10703-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="10703-136">Opret en ny kolonnedefinition     [![Opret en ny kolonnedefinition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="10703-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="10703-137">Opret en ny rapportdefinition a.</span><span class="sxs-lookup"><span data-stu-id="10703-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="10703-138">Klik på Indstillinger, og fjern markeringen [![Indstillinger-formular](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span><span class="sxs-lookup"><span data-stu-id="10703-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="10703-139">Opret rapporten.</span><span class="sxs-lookup"><span data-stu-id="10703-139">Generate the Report.</span></span> 

5.  <span data-ttu-id="10703-140">Eksporter rapporten til Excel.</span><span class="sxs-lookup"><span data-stu-id="10703-140">Export the Report to Excel.</span></span>

### <a name="in-d365"></a><span data-ttu-id="10703-141">I D365:</span><span class="sxs-lookup"><span data-stu-id="10703-141">In D365:</span></span> 
1.  <span data-ttu-id="10703-142">Klik på Finans | Forespørgsler og rapporter | Råbalance a.</span><span class="sxs-lookup"><span data-stu-id="10703-142">Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id="10703-143">Parametre i.</span><span class="sxs-lookup"><span data-stu-id="10703-143">Parameters i.</span></span>  <span data-ttu-id="10703-144">Fra dato: Startdato for regnskabsåret ii.</span><span class="sxs-lookup"><span data-stu-id="10703-144">From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id="10703-145">Til dato: Den dato, hvor du genererede rapporten til iii.</span><span class="sxs-lookup"><span data-stu-id="10703-145">To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id="10703-146">Økonomiske dimensionsopsætninger "Hovedkontoopsætninger" [![Hovedkontoformular](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="10703-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="10703-147">b.</span><span class="sxs-lookup"><span data-stu-id="10703-147">b.</span></span>    <span data-ttu-id="10703-148">Klik på Beregn</span><span class="sxs-lookup"><span data-stu-id="10703-148">Click Calculate</span></span>

2.  <span data-ttu-id="10703-149">Eksporter rapporten til Excel</span><span class="sxs-lookup"><span data-stu-id="10703-149">Export the report to Excel</span></span>

<span data-ttu-id="10703-150">Du skal nu kunne kopiere data fra FR Excel-rapporten til rapporten D365 Råbalance og sammenligne kolonnerne med "Ultimosaldo".</span><span class="sxs-lookup"><span data-stu-id="10703-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]