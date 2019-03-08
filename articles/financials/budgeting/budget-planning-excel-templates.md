---
title: Budgetplanlægningsskabeloner til Excel
description: I dette emne beskrives, hvordan du kan oprette Microsoft Excel-skabeloner, der kan bruges sammen med budgetplaner.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 079aa6bb4be020fc050b81c400050ed23d48f6ca
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "337043"
---
# <a name="budget-planning-templates-for-excel"></a><span data-ttu-id="4466e-103">Budgetplanlægningsskabeloner til Excel</span><span class="sxs-lookup"><span data-stu-id="4466e-103">Budget planning templates for Excel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4466e-104">I dette emne beskrives, hvordan du kan oprette Microsoft Excel-skabeloner, der kan bruges sammen med budgetplaner.</span><span class="sxs-lookup"><span data-stu-id="4466e-104">This topic describes how to create Microsoft Excel templates that can be used with budget plans.</span></span>

<span data-ttu-id="4466e-105">I dette emne kan du se, hvordan du opretter Excel-skabeloner, der skal bruges med budgetplaner ved hjælp af standarddemodatasæt og logon som administratorbruger.</span><span class="sxs-lookup"><span data-stu-id="4466e-105">This topic shows how to create Excel templates that will be used with budget plans using the standard demo data set and the Admin user login.</span></span> <span data-ttu-id="4466e-106">Du kan finde flere oplysninger om budgetplanlægning under [Budgetplanlægningsoversigt.](budget-planning-overview-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="4466e-106">For more information about budget planning, see [Budget planning overview.](budget-planning-overview-configuration.md)</span></span> <span data-ttu-id="4466e-107">Du kan også følge selvstudiet [Budgetplanlægning 101](budget-plan.md) for at lære grundlæggende principper for modulkonfiguration og -brug.</span><span class="sxs-lookup"><span data-stu-id="4466e-107">You can also follow the [Budget planning 101](budget-plan.md) tutorial to learn basic module configuration and usage principles.</span></span>

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a><span data-ttu-id="4466e-108">Automatisk generere et regneark ved hjælp af dokumentlayout til budgetplan</span><span class="sxs-lookup"><span data-stu-id="4466e-108">Generate a worksheet using budget plan document layout</span></span>

<span data-ttu-id="4466e-109">Budgetplandokumenter kan ses og redigeres ved hjælp af et eller flere layout.</span><span class="sxs-lookup"><span data-stu-id="4466e-109">Budget plan documents can be viewed and edited using one or more layouts.</span></span> <span data-ttu-id="4466e-110">Hvert layout kan have en tilknyttet skabelon til et budgetplandokument for at få vist og redigere budgetplandata i et Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="4466e-110">Each layout can have an associated budget plan document template to view and edit the budget plan data in an Excel worksheet.</span></span> <span data-ttu-id="4466e-111">I dette emne vil der blive genereret en skabelon til et budgetplandokument ved hjælp af en eksisterende layoutkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4466e-111">In this topic, a budget plan document template will be generated using an existing layout configuration.</span></span> 

1. <span data-ttu-id="4466e-112">Åbn **listen over budgetplaner** (**Budgettering** &gt; **Budgetplaner**).</span><span class="sxs-lookup"><span data-stu-id="4466e-112">Open the **Budget plans list** (**Budgeting** &gt; **Budget plans**).</span></span> 
2. <span data-ttu-id="4466e-113">Klik på **Ny** for at oprette et nyt budgetplandokument.</span><span class="sxs-lookup"><span data-stu-id="4466e-113">Click **New** to create a new budget plan document.</span></span> 

   <span data-ttu-id="4466e-114">[![Budgetplanliste](./media/bpt11-1024x552.png)](./media/bpt11.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-114">[![Budget plans list](./media/bpt11-1024x552.png)](./media/bpt11.png)</span></span> 

3. <span data-ttu-id="4466e-115">Brug indstillingen på linjen **Tilføj** for at tilføje linjer.</span><span class="sxs-lookup"><span data-stu-id="4466e-115">Use the **Add** line option to add lines.</span></span> <span data-ttu-id="4466e-116">Klik på **Layout** for at få vist konfigurationen af dokumentlayout til budgetplan.</span><span class="sxs-lookup"><span data-stu-id="4466e-116">Click **Layouts** to view the budget plan document layout configuration.</span></span> 

   <span data-ttu-id="4466e-117">[![Budgetplantilføjelse](./media/bpt2-1024x274.png)](./media/bpt2.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-117">[![Budget plans add](./media/bpt2-1024x274.png)](./media/bpt2.png)</span></span> 

<span data-ttu-id="4466e-118">Du kan gennemgå layoutkonfigurationen og justere den efter behov.</span><span class="sxs-lookup"><span data-stu-id="4466e-118">You can review the layout configuration and adjust it as needed.</span></span> 
1. <span data-ttu-id="4466e-119">Gå til **Skabelon** &gt; **Generer** for at oprette en Excel-fil for dette layout.</span><span class="sxs-lookup"><span data-stu-id="4466e-119">Go to **Template** &gt; **Generate** to create an Excel file for this layout.</span></span> 
2. <span data-ttu-id="4466e-120">Når skabelonen er oprettet, kan du gå til **Skabelon** &gt; **Vis** for at åbne og gennemse skabelonen til budgetplandokumentet.</span><span class="sxs-lookup"><span data-stu-id="4466e-120">After the template is generated, go to **Template** &gt; **View** to open and review the budget plan document template.</span></span> <span data-ttu-id="4466e-121">Du kan gemme Excel-filen til den lokale harddisk.</span><span class="sxs-lookup"><span data-stu-id="4466e-121">You can save the Excel file to your local drive.</span></span> 

<span data-ttu-id="4466e-122">[![Gem som](./media/bpt3-1024x545.png)](./media/bpt3.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-122">[![Save as](./media/bpt3-1024x545.png)](./media/bpt3.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="4466e-123">Dokumentlayout til budgetplaner kan ikke redigeres, når der er knyttet en Excel-skabelon til det.</span><span class="sxs-lookup"><span data-stu-id="4466e-123">The Budget plan document layout cannot be edited after an Excel template is associated with it.</span></span> <span data-ttu-id="4466e-124">Hvis du vil ændre layoutet, skal du slette den tilknyttede Excel-skabelonfil og oprette den igen.</span><span class="sxs-lookup"><span data-stu-id="4466e-124">To modify the layout, delete the associated Excel template file and regenerate it.</span></span> <span data-ttu-id="4466e-125">Dette er påkrævet for at holde felterne i layoutet og regnearket synkroniseret.</span><span class="sxs-lookup"><span data-stu-id="4466e-125">This is required to keep the fields in the layout and the worksheet synchronized.</span></span> 

<span data-ttu-id="4466e-126">Excel-skabelonen indeholder alle elementerne fra dokumentlayoutet til budgetplanen, hvor kolonnen **Tilgængelig i regneark** er indstillet til Sand.</span><span class="sxs-lookup"><span data-stu-id="4466e-126">The Excel template will contain all of the elements from the budget plan document layout, where the **Available in Worksheet** column is set to True.</span></span> <span data-ttu-id="4466e-127">Overlappende elementer er ikke tilladt i Excel-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="4466e-127">Overlapping elements are not allowed in the Excel template.</span></span> <span data-ttu-id="4466e-128">For eksempel hvis layoutet indeholder kolonner med anmodningen Første kvartal, anmodningen Andet kvartal, anmodningen Tredje kvartal og anmodningen Fjerde kvartal, og en kolonne med alle anmodninger, der repræsenterer summen af alle 4 kvartalsvise kolonner, er kun de kvartalsvise kolonner eller kolonnen med alle anmodninger tilgængelig og kan bruges i Excel-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="4466e-128">For example, if the layout contains Request Q1, Request Q2, Request Q3, and Request Q4 columns, and a total request column that represents a sum of all 4 quarterly columns, only the quarterly columns or total column is available to be used in the Excel template.</span></span> <span data-ttu-id="4466e-129">Excel-filen kan ikke opdatere overlappende kolonner under opdateringen, fordi dataene i tabellen bliver forældede og upræcise.</span><span class="sxs-lookup"><span data-stu-id="4466e-129">The Excel file cannot update overlapping columns during the update because data in the table could become out of date and inaccurate.</span></span>

<span data-ttu-id="4466e-130">[![Eksempel](./media/bpt4-1024x615.png)](./media/bpt4.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-130">[![Example](./media/bpt4-1024x615.png)](./media/bpt4.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="4466e-131">For at undgå potentielle problemer med visning og redigering af budgetplandata ved hjælp af Excel skal den samme bruger være logget på både Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics Office-tilføjelsesprogrammet Dataconnector.</span><span class="sxs-lookup"><span data-stu-id="4466e-131">To avoid potential issues with viewing and editing budget plan data using Excel, the same user should be logged into both Microsoft Dynamics 365 for Finance and Operations and the Microsoft Dynamics Office Add-in Data Connector.</span></span>

## <a name="add-a-header-to-budget-plan-document-template"></a><span data-ttu-id="4466e-132">Tilføje et sidehoved til skabelon til budgetplandokument</span><span class="sxs-lookup"><span data-stu-id="4466e-132">Add a header to budget plan document template</span></span>
<span data-ttu-id="4466e-133">Hvis du vil tilføje sidehovedoplysninger, skal du vælge den øverste række i Excel-filen og indsætte tomme rækker.</span><span class="sxs-lookup"><span data-stu-id="4466e-133">To add header information, select the top row in the Excel file and insert empty rows.</span></span> <span data-ttu-id="4466e-134">Klik på **Design** i **Dataconnector** for at tilføje sidehovedfelter i Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="4466e-134">Click **Design** in the **Data Connector** to add header fields to the Excel file.</span></span>

<span data-ttu-id="4466e-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span></span> 

<span data-ttu-id="4466e-136">Under fanen **Design** skal du klikke på **Tilføj** felter og derefter vælge **BudgetPlanHeader** som enhedsdatakilden.</span><span class="sxs-lookup"><span data-stu-id="4466e-136">In the **Design** tab, click **Add** fields, and then select **BudgetPlanHeader** as the entity data source.</span></span>

<span data-ttu-id="4466e-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span></span>

<span data-ttu-id="4466e-138">Peg med markøren på den ønskede placering i Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="4466e-138">Point the cursor to the desired location in the Excel file.</span></span> <span data-ttu-id="4466e-139">Klik på **Tilføj etiket** for at føje feltetiketten til den valgte placering.</span><span class="sxs-lookup"><span data-stu-id="4466e-139">Click **Add label** to add the field label to the selected location.</span></span> <span data-ttu-id="4466e-140">Vælg **Tilføj værdi** for at føje værdifeltet til det valgte sted.</span><span class="sxs-lookup"><span data-stu-id="4466e-140">Select **Add Value** to add the value field to the selected place.</span></span> <span data-ttu-id="4466e-141">Klik på **Udført** for at lukke designeren.</span><span class="sxs-lookup"><span data-stu-id="4466e-141">Click **Done** to close the designer.</span></span>

## <a name="bpt7mediabpt7pngmediabpt7png"></a><span data-ttu-id="4466e-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span></span>

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a><span data-ttu-id="4466e-143">Tilføje en beregnet kolonne i skabelontabel til budgetplandokument</span><span class="sxs-lookup"><span data-stu-id="4466e-143">Add a calculated column to budget plan document template table</span></span>
--------------------------------------------------------------

<span data-ttu-id="4466e-144">Derefter føjes beregnede kolonner til den genererede dokumentskabelon til budgetplanen.</span><span class="sxs-lookup"><span data-stu-id="4466e-144">Next, calculated columns will be added to generated budget plan document template.</span></span> <span data-ttu-id="4466e-145">En **Anmodet i alt**-kolonne, som opsummerer kolonner med anmodningen Første kvartal til anmodningen Fjerde kvartal, og en **Regulering**-kolonne, der genberegner **Anmodet i alt**-kolonnen med en foruddefineret faktor.</span><span class="sxs-lookup"><span data-stu-id="4466e-145">A **Total request** column, which summarizes Request Q1: Request Q4 columns, and an **Adjustment** column, which recalculates the **Total Request** column by a predefined factor.</span></span>

<span data-ttu-id="4466e-146">Klik på **Design** i **Dataconnector** for at tilføje kolonner i tabellen.</span><span class="sxs-lookup"><span data-stu-id="4466e-146">Click **Design** in the **Data connector** to add columns to the table.</span></span> <span data-ttu-id="4466e-147">Klik på **Rediger** ud for **BudgetPlanWorksheet**-datakilden for at begynde at tilføje kolonner.</span><span class="sxs-lookup"><span data-stu-id="4466e-147">Click **Edit** next to **BudgetPlanWorksheet** data source to start adding columns.</span></span>

<span data-ttu-id="4466e-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span></span> 

<span data-ttu-id="4466e-149">Den markerede feltgruppe viser de kolonner, der er tilgængelige i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="4466e-149">The selected field group displays the columns that are available in the template.</span></span> <span data-ttu-id="4466e-150">Klik på **Formel** for at tilføje en ny kolonne.</span><span class="sxs-lookup"><span data-stu-id="4466e-150">Click **Formula** to add a new column.</span></span> <span data-ttu-id="4466e-151">Navngiv den nye kolonne, og indsæt derefter formlen i feltet **Formel**.</span><span class="sxs-lookup"><span data-stu-id="4466e-151">Name the new column and then paste the formula into the **Formula** field.</span></span> <span data-ttu-id="4466e-152">Klik på **Opdater** for at indsætte kolonnen.</span><span class="sxs-lookup"><span data-stu-id="4466e-152">Click **Update** to insert the column.</span></span>

<span data-ttu-id="4466e-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="4466e-154">For at definere formlen skal du oprette formlen i regnearket og derefter kopiere det til **Design** vinduet.</span><span class="sxs-lookup"><span data-stu-id="4466e-154">To define the formula, create the formula in the spreadsheet, and then copy it to the **Design** window.</span></span> <span data-ttu-id="4466e-155">En tabel, der er bundet til Finance and Operations, får typisk navnet "AXTable1".</span><span class="sxs-lookup"><span data-stu-id="4466e-155">A Finance and Operations bound table will typically be named "AXTable1".</span></span> <span data-ttu-id="4466e-156">For at opsummere kolonnerne for anmodningen Første kvartal til anmodningen Fjerde kvartal i regnearket bruges formlen = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span><span class="sxs-lookup"><span data-stu-id="4466e-156">For example, to summarize Request Q1 : Request Q4 columns in the spreadsheet, the formula = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span></span>

<span data-ttu-id="4466e-157">Gentag disse trin for at indsætte kolonnen **Regulering**.</span><span class="sxs-lookup"><span data-stu-id="4466e-157">Repeat these steps to insert the **Adjustment** column.</span></span> <span data-ttu-id="4466e-158">Brug formlen = AxTable1\[Total request\]\*$I$ 1 for denne kolonne.</span><span class="sxs-lookup"><span data-stu-id="4466e-158">Use formula = AxTable1\[Total request\]\*$I$1 for this column.</span></span> <span data-ttu-id="4466e-159">Dette vil tage værdien i celle I1 og multiplicere værdierne i kolonnen **Anmodet i alt** for at beregne reguleringsbeløb.</span><span class="sxs-lookup"><span data-stu-id="4466e-159">This will take the value in cell I1 and multiply the values in the **Total request** column to calculate adjustment amounts.</span></span>

<span data-ttu-id="4466e-160">Gem og luk Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="4466e-160">Save and close the Excel file.</span></span> <span data-ttu-id="4466e-161">Gå tilbage til Finance and Operations og klik i **Layout** på **Skabelon &gt; Overfør** for at overføre den gemte Excel-skabelon, der skal bruges til budgetplanen.</span><span class="sxs-lookup"><span data-stu-id="4466e-161">Return to Finance and Operations, and in **Layouts**, click **Template &gt; Upload** to upload the saved Excel template to be used for the budget plan.</span></span> 

<span data-ttu-id="4466e-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span></span> 

<span data-ttu-id="4466e-163">Luk **Layout** skyderen.</span><span class="sxs-lookup"><span data-stu-id="4466e-163">Close the **Layouts** slider.</span></span> <span data-ttu-id="4466e-164">Klik i dokumentet **Budgetplan** på **Regneark** for at få vist og redigere dokument i Excel.</span><span class="sxs-lookup"><span data-stu-id="4466e-164">In **Budget plan** document, click **Worksheet** to view and edit the document in Excel.</span></span> <span data-ttu-id="4466e-165">Bemærk, at den justerede Excel-skabelon, der blev brugt til at oprette dette budgetplansregneark og beregnede kolonner, opdateres ved hjælp af formler, der blev defineret i de forrige trin.</span><span class="sxs-lookup"><span data-stu-id="4466e-165">Note that the adjusted Excel template was used to create this budget plan worksheet and calculated columns are updated using the formulas that were defined in the previous steps.</span></span> 

<span data-ttu-id="4466e-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span></span>

## <a name="tips--tricks-for-creating-budget-plan-templates"></a><span data-ttu-id="4466e-167">Tips og tricks til oprettelse af skabeloner for budgetplan</span><span class="sxs-lookup"><span data-stu-id="4466e-167">Tips & tricks for creating budget plan templates</span></span>
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a><span data-ttu-id="4466e-168">Kan jeg tilføje og bruge flere datakilder til en budgetplansskabelon?</span><span class="sxs-lookup"><span data-stu-id="4466e-168">Can I add and use additional data sources to a budget plan template?</span></span>

<span data-ttu-id="4466e-169">Ja, du kan bruge menuen **Design** til at føje flere enheder til det samme eller andre regneark i Excel-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="4466e-169">Yes, you can use the **Design** menu to add additional entities to the same or other sheets in the Excel template.</span></span> <span data-ttu-id="4466e-170">For eksempel kan du tilføje **BudgetPlanProposedProject**-datakilden for at oprette og vedligeholde en liste over foreslåede projekter på samme tid, når du arbejder med budgetplandata i Excel.</span><span class="sxs-lookup"><span data-stu-id="4466e-170">For example, you can add the **BudgetPlanProposedProject** data source to create and maintain a list of proposed projects at the same time when working with budget plan data in Excel.</span></span> <span data-ttu-id="4466e-171">Bemærk, at hvis du inkluderer store datakilder, kan det påvirke ydeevnen af Excel-projektmappen.</span><span class="sxs-lookup"><span data-stu-id="4466e-171">Note that including high-volume data sources might impact performance of the Excel workbook.</span></span> 

<span data-ttu-id="4466e-172">Du kan bruge indstillingen **Filter** i **Dataconnector** til at føje ønskede filtre til flere datakilder.</span><span class="sxs-lookup"><span data-stu-id="4466e-172">You can use the **Filter** option in the **Data Connector** to add desired filters to additional data sources.</span></span>

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a><span data-ttu-id="4466e-173">Kan jeg skjule designindstillinger i Dataconnector for andre brugere?</span><span class="sxs-lookup"><span data-stu-id="4466e-173">Can I hide the Design option in the Data connector for other users?</span></span>

<span data-ttu-id="4466e-174">Ja, åbn **Dataconnector**-indstillingerne for at skjule **Design**-indstillingen fra andre brugere.</span><span class="sxs-lookup"><span data-stu-id="4466e-174">Yes, open the **Data Connector** options to hide the **Design** option from other users.</span></span>

<span data-ttu-id="4466e-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span></span>

<span data-ttu-id="4466e-176">Udvid **Indstillinger for Dataconnector**, og fjern markeringen i afkrydsningsfeltet **Aktivér design**.</span><span class="sxs-lookup"><span data-stu-id="4466e-176">Expand **Data connector options** and clear the **Enable design** check box.</span></span> <span data-ttu-id="4466e-177">Derved skjules **Design** indstilling fra **Dataconnector**.</span><span class="sxs-lookup"><span data-stu-id="4466e-177">This will hide the **Design** option from the **Data connector**.</span></span>

<span data-ttu-id="4466e-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span></span>

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a><span data-ttu-id="4466e-179">Er det muligt at forhindre brugere i ved et uheld at lukke Dataconnector, mens de arbejder med data?</span><span class="sxs-lookup"><span data-stu-id="4466e-179">Can I prevent users from accidently closing the Data connector while working with data?</span></span>

<span data-ttu-id="4466e-180">Vi anbefaler at låse skabelonen for at forhindre brugere i at lukke den.</span><span class="sxs-lookup"><span data-stu-id="4466e-180">We recommend locking the template to prevent users from closing it.</span></span> <span data-ttu-id="4466e-181">Hvis du vil aktivere låsen, skal du klikke på **Dataconnector**. Der vises en pil i øverste højre hjørne.</span><span class="sxs-lookup"><span data-stu-id="4466e-181">To turn on the lock, click the **Data connector**, in the top right corner an arrow appears.</span></span> 

<span data-ttu-id="4466e-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span></span> 

<span data-ttu-id="4466e-183">Klik på pilen for at åbne en ekstra menu.</span><span class="sxs-lookup"><span data-stu-id="4466e-183">Click the arrow for an additional menu.</span></span> <span data-ttu-id="4466e-184">Vælg **Lås**.</span><span class="sxs-lookup"><span data-stu-id="4466e-184">Select **Lock**.</span></span>

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a><span data-ttu-id="4466e-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span></span>

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a><span data-ttu-id="4466e-186">Er det muligt at bruge andre Excel-funktioner, som celleformatering, farver, betinget formatering og diagrammer med mine budgetplanskabeloner?</span><span class="sxs-lookup"><span data-stu-id="4466e-186">Can I use other Excel features, like cell formatting, colors, conditional formatting, and charts with my budget plan templates?</span></span>

<span data-ttu-id="4466e-187">Ja, de fleste af de almindelige Excel-funktioner fungerer i budgetplanskabeloner.</span><span class="sxs-lookup"><span data-stu-id="4466e-187">Yes, most of the standard Excel capabilities will work in budget plan templates.</span></span> <span data-ttu-id="4466e-188">Det anbefales at bruge farvekodning, så brugerne kan skelne mellem skrivebeskyttede og redigerbare kolonner.</span><span class="sxs-lookup"><span data-stu-id="4466e-188">We recommend using color-coding for users to distinguish between read-only and editable columns.</span></span> <span data-ttu-id="4466e-189">Betinget formatering kan bruges til at fremhæve problematiske områder af budgettet.</span><span class="sxs-lookup"><span data-stu-id="4466e-189">Conditional formatting can be used to highlight problematic areas of the budget.</span></span> <span data-ttu-id="4466e-190">Kolonnetotaler kan let vises ved hjælp af standard Excel-formler oven over tabellen.</span><span class="sxs-lookup"><span data-stu-id="4466e-190">Column totals can easily be presented by using standard Excel formulas above the table.</span></span>

<span data-ttu-id="4466e-191">Du kan også oprette og bruge pivottabeller og -diagrammer til supplerende grupperinger og visualiseringer af budgetdata.</span><span class="sxs-lookup"><span data-stu-id="4466e-191">You can also create and use pivot tables and charts for additional groupings and visualizations of budget data.</span></span> <span data-ttu-id="4466e-192">Under fanen **Data** i gruppen **Forbindelser** skal du klikke på **Opdater alle** og derefter klikke på **Forbindelsesegenskaber**.</span><span class="sxs-lookup"><span data-stu-id="4466e-192">On the **Data** tab, in the **Connections** group, click **Refresh All**, and then click **Connection Properties**.</span></span> <span data-ttu-id="4466e-193">Klik på fanen **Anvendelse**. Under **Opdater** skal du markere afkrydsningsfeltet **Opdater data, når filen åbnes**.</span><span class="sxs-lookup"><span data-stu-id="4466e-193">Click the **Usage** tab. Under **Refresh**, select the **Refresh data when opening the file** check box.</span></span> 

<span data-ttu-id="4466e-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span><span class="sxs-lookup"><span data-stu-id="4466e-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span></span>



