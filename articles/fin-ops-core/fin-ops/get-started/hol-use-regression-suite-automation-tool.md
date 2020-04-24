---
title: Bruge Regression Suite Automation Tool
description: I dette emne vises, hvordan du kan bruge værktøjet RSAT (Regression Suite Automation Tool). Det beskriver forskellige funktioner og indeholder eksempler, der bruger avanceret scripting.
author: robinarh
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 2d3dde69b102ce161e5c1f1dd393ffceca608bcb
ms.sourcegitcommit: 4fdee254649a751d46632fb4d0d48698e112fa72
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248730"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="f737d-104">Brug Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="f737d-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="f737d-105">Brug dine internetbrowserværktøjer til at downloade og gemme denne side i PDF-format.</span><span class="sxs-lookup"><span data-stu-id="f737d-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="f737d-106">Dette selvstudium gennemgår nogle af de avancerede funktioner i RSAT (Regression suite automation tool), herunder en demoopgave og beskriver strategi og centrale undervisningspunkter.</span><span class="sxs-lookup"><span data-stu-id="f737d-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span> 

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="f737d-107">Vigtige funktioner i RSAT og Arbejdsrutineoptager</span><span class="sxs-lookup"><span data-stu-id="f737d-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="f737d-108">Valider en feltværdi</span><span class="sxs-lookup"><span data-stu-id="f737d-108">Validate a field value</span></span>

<span data-ttu-id="f737d-109">RSAT giver dig mulighed for at medtage valideringstrin i din test case for at validere forventede værdier.</span><span class="sxs-lookup"><span data-stu-id="f737d-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="f737d-110">Du kan få flere oplysninger om denne funktion i artiklen [Validere forventede værdier](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).</span><span class="sxs-lookup"><span data-stu-id="f737d-110">For information about this feature, see the article [Validate expected values](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).</span></span>

<span data-ttu-id="f737d-111">I følgende eksempel vises, hvordan du kan bruge denne funktion til at validere, om den disponible lagerbeholdning er større end 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="f737d-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="f737d-112">I demodataene i **USMF**-firmaet skal du oprette en opgaveregistrering, der indeholder følgende trin:</span><span class="sxs-lookup"><span data-stu-id="f737d-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="f737d-113">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="f737d-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="f737d-114">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="f737d-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f737d-115">Filtrer f.eks. efter en værdi på **1000** for feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="f737d-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="f737d-116">Vælg **Disponibel lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="f737d-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="f737d-117">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="f737d-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f737d-118">Du kan f.eks. filtrere efter værdien **1** for feltet **Lokation**.</span><span class="sxs-lookup"><span data-stu-id="f737d-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="f737d-119">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f737d-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="f737d-120">Kontroller, at værdien af feltet **I alt disponibelt** er **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="f737d-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="f737d-121">Gem opgaveregistreringen, og knyt den til test casen i Azure Devops.</span><span class="sxs-lookup"><span data-stu-id="f737d-121">Save the task recording and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="f737d-122">Føj testsagen til testplanen, og Indlæs testsagen i RSAT.</span><span class="sxs-lookup"><span data-stu-id="f737d-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="f737d-123">Åbn Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="f737d-123">Open the Excel parameter file.</span></span> <span data-ttu-id="f737d-124">Under fanen **InventOnhandItem** kan du se afsnittet **Valider InventOnhandItem**, der indeholder feltet **operator**.</span><span class="sxs-lookup"><span data-stu-id="f737d-124">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Feltet Operator](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="f737d-126">Hvis du vil validere, om den disponible lagerbeholdning altid vil være mere end 0, skal du ændre værdien af feltet **Værdi** fra **411** til **0** og værdien af feltet **Operator** fra et lighedstegn (**=**) til et større end tegn (**\>**).</span><span class="sxs-lookup"><span data-stu-id="f737d-126">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Værdierne i felterne Værdi og Operator ændres](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="f737d-128">Gem og luk Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="f737d-128">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="f737d-129">Vælg **Overfør** for at gemme de ændringer, du har foretaget, i Excel-parameterfilen Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f737d-129">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="f737d-130">Hvis værdien af feltet **I alt disponibelt** for den angivne vare på lageret er større end 0 (nul), vil testene bestå, uanset den faktiske værdi for disponibel lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="f737d-130">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="f737d-131">Gemte variabler og sammenkædning af test cases</span><span class="sxs-lookup"><span data-stu-id="f737d-131">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="f737d-132">En af nøglefunktionerne i RSAT er sammenkædning af test cases, dvs. en test kan overføre værdier til andre test.</span><span class="sxs-lookup"><span data-stu-id="f737d-132">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="f737d-133">Du kan få flere oplysninger i artiklen [Kopiere variabler til sammenkædede test cases](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="f737d-133">For more information, see the article [Copy variables to chain test cases](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="f737d-134">Afledt testsag</span><span class="sxs-lookup"><span data-stu-id="f737d-134">Derived test case</span></span>

<span data-ttu-id="f737d-135">RSAT giver dig mulighed for at bruge den samme opgaveregistrering i flere test cases, hvilket gør det muligt at køre en opgave med forskellige datakonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="f737d-135">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="f737d-136">Du kan finde flere oplysninger i artiklen [Afledte test cases](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="f737d-136">See the article [Derived test cases](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="f737d-137">Validere beskeder og meddelelser</span><span class="sxs-lookup"><span data-stu-id="f737d-137">Validate notifications and messages</span></span>

<span data-ttu-id="f737d-138">Denne funktion kan bruges til at validere, om der opstod en handling.</span><span class="sxs-lookup"><span data-stu-id="f737d-138">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="f737d-139">Når der f.eks. oprettes, estimeres og derefter startes en produktionsordre, viser appen meddelelsen "Produktion – start" for at give dig besked om, at produktionsordren er startet.</span><span class="sxs-lookup"><span data-stu-id="f737d-139">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Beskeden Produktion – start](./media/use_rsa_tool_05.png)

<span data-ttu-id="f737d-141">Du kan validere denne meddelelse via RSAT ved at angive meddelelsesteksten under fanen **Meddelelsesvalidering** i Excel-parameterfilen for den relevante registrering.</span><span class="sxs-lookup"><span data-stu-id="f737d-141">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Fanen Meddelelsesvalidering](./media/use_rsa_tool_06.png)

<span data-ttu-id="f737d-143">Når testsagen er kørt, sammenlignes meddelelsen i Excel-parameterfilen med den viste meddelelse.</span><span class="sxs-lookup"><span data-stu-id="f737d-143">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="f737d-144">Hvis meddelelserne ikke stemmer overens, vil testsagen mislykkes.</span><span class="sxs-lookup"><span data-stu-id="f737d-144">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="f737d-145">Du kan angive mere end én meddelelse under fanen **Meddelelsesvalidering** i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="f737d-145">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="f737d-146">Meddelelserne kan også være fejl- eller advarselsmeddelelser i stedet for orienterende meddelelser.</span><span class="sxs-lookup"><span data-stu-id="f737d-146">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="f737d-147">Øjebliksbillede</span><span class="sxs-lookup"><span data-stu-id="f737d-147">Snapshot</span></span>

<span data-ttu-id="f737d-148">Denne funktion bruger skærmbilleder af de trin, der blev udført under opgaveregistreringen.</span><span class="sxs-lookup"><span data-stu-id="f737d-148">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="f737d-149">Det er nyttigt i forbindelse med overvågning eller fejlfinding.</span><span class="sxs-lookup"><span data-stu-id="f737d-149">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="f737d-150">Hvis du vil bruge denne funktion, skal du åbne filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installationsmappen (f.eks. **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og ændre værdien af det følgende element fra **falsk** til **sand**.</span><span class="sxs-lookup"><span data-stu-id="f737d-150">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="f737d-151">Når du kører test casen, vil RSAT generere snapshots (billeder) af trinnene i afspilningsmappen i test cases i arbejdsbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="f737d-151">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="f737d-152">Hvis du bruger en ældre version af RSAT, gemmes billederne i **C:\\Brugere\\\<Brugernavn\>\\AppData\\Roaming\\regressionTool\\afspilning**, og der oprettes en separat mappe for hver test case, der køres.</span><span class="sxs-lookup"><span data-stu-id="f737d-152">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="f737d-153">Tilknytning</span><span class="sxs-lookup"><span data-stu-id="f737d-153">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="f737d-154">Scenario</span><span class="sxs-lookup"><span data-stu-id="f737d-154">Scenario</span></span>

1. <span data-ttu-id="f737d-155">Produktdesigneren opretter et nyt, frigivet produkt.</span><span class="sxs-lookup"><span data-stu-id="f737d-155">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="f737d-156">Produktionschefen starter en produktionsordre for at bringe lagerniveauet op til to styk.</span><span class="sxs-lookup"><span data-stu-id="f737d-156">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="f737d-157">Produktionen starter og afslutter produktionsordren og kontrollerer, at det disponible antal er to styk.</span><span class="sxs-lookup"><span data-stu-id="f737d-157">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="f737d-158">Salgsteamet modtager en ordre på fire stykker af det nye produkt.</span><span class="sxs-lookup"><span data-stu-id="f737d-158">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="f737d-159">Salgsgruppen opdaterer derfor nettokravene via den dynamiske plan.</span><span class="sxs-lookup"><span data-stu-id="f737d-159">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="f737d-160">Da der ikke er mere tilgængelig kapacitet, er standardordrepolitikken indstillet til "køb i stedet for at fremstille".</span><span class="sxs-lookup"><span data-stu-id="f737d-160">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="f737d-161">Derfor oprettes der et salgsforslag.</span><span class="sxs-lookup"><span data-stu-id="f737d-161">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="f737d-162">Køberen tilføjer en kreditor, autoriserer indkøbsordreforslaget og bekræfter derefter indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="f737d-162">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="f737d-163">Når de købte varer ankommer til butikken, søger butiksoperatøren efter den relaterede indkøbsordre og modtager varerne.</span><span class="sxs-lookup"><span data-stu-id="f737d-163">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="f737d-164">Da ordren nu er fuldført, kan varer plukkes og pakkes i forhold til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="f737d-164">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="f737d-165">Finans bogfører købsfakturaen og salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="f737d-165">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="f737d-166">I følgende illustration vises flowet i dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="f737d-166">The following illustration shows the flow for this scenario.</span></span>

![Flow for demoscenariet](./media/use_rsa_tool_14.png)

<span data-ttu-id="f737d-168">I følgende illustration vises hierarkiet af forretningsprocesserne for dette scenario i LCS Forretningsmodeldesigner.</span><span class="sxs-lookup"><span data-stu-id="f737d-168">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![Forretningsprocesser til demoscenariet](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="f737d-170">Strategi – vigtig læring</span><span class="sxs-lookup"><span data-stu-id="f737d-170">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="f737d-171">Data</span><span class="sxs-lookup"><span data-stu-id="f737d-171">Data</span></span>

- <span data-ttu-id="f737d-172">Sørg for, at du har repræsentative datamængder (en kopi af produktion/gyldne konfigurationsdata plus overførte data).</span><span class="sxs-lookup"><span data-stu-id="f737d-172">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="f737d-173">Når du genererer nye data via en opgaveregistrering, skal du oprette testnavne, der ikke er i konflikt med eksisterende navne (brug f.eks. et præfisk såsom **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="f737d-173">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="f737d-174">Brug Azures funktion til genoprettelse af et bestemt tidspunkt for at køre test i miljøjer, der ikke er niveau 1, igen.</span><span class="sxs-lookup"><span data-stu-id="f737d-174">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="f737d-175">Selvom du kan bruge Excel-funktionerne **VILKÅRLIG** og **NU** til at generere en entydig kombination, kræver det ret meget arbejde.</span><span class="sxs-lookup"><span data-stu-id="f737d-175">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="f737d-176">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="f737d-176">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="f737d-177">Arbejdsrutineoptager</span><span class="sxs-lookup"><span data-stu-id="f737d-177">Task recorder</span></span>

- <span data-ttu-id="f737d-178">Definer scenarierne, før du går i gang med at registrere.</span><span class="sxs-lookup"><span data-stu-id="f737d-178">Define scenarios before you start recording.</span></span> <span data-ttu-id="f737d-179">Et godt styret projekt har foruddefinerede testscenarier.</span><span class="sxs-lookup"><span data-stu-id="f737d-179">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="f737d-180">Hvis du vil oprette en testsag, skal du overveje, hvor forudsigelige udfaldet af disse testsituationer er.</span><span class="sxs-lookup"><span data-stu-id="f737d-180">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="f737d-181">Opdel registreringer, hvis de udføres af forskellige roller, eller hvis der er ventetiden eller en ekstern hændelse før næste trin.</span><span class="sxs-lookup"><span data-stu-id="f737d-181">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="f737d-182">Undgå at vælge værdier på lister.</span><span class="sxs-lookup"><span data-stu-id="f737d-182">Avoid selecting values in lists.</span></span> <span data-ttu-id="f737d-183">Brug i stedet tekstformater som f.eks **FIFO**, **AudioRM** og **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="f737d-183">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="f737d-184">Når du vælger på en liste, registreres placeringen af værdien på listen, ikke selve værdien.</span><span class="sxs-lookup"><span data-stu-id="f737d-184">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="f737d-185">Hvis der føjes varer til listen, kan placeringen af værdien ændres.</span><span class="sxs-lookup"><span data-stu-id="f737d-185">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="f737d-186">Derfor vil din registrering bruge en anden parameter, og resten af scenariet kan blive påvirket.</span><span class="sxs-lookup"><span data-stu-id="f737d-186">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="f737d-187">Tænk over funktionsmåde for flere brugere.</span><span class="sxs-lookup"><span data-stu-id="f737d-187">Think about multi-user behavior.</span></span> <span data-ttu-id="f737d-188">Antag f. eks. ikke, at din nyoprettede salgsordre altid skal vælges automatisk.</span><span class="sxs-lookup"><span data-stu-id="f737d-188">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="f737d-189">Brug i stedet for altid filteret til at finde den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="f737d-189">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="f737d-190">Brug funktionen Kopier i Opgaveregistrering til at gemme navnet på et nyoprettet produkt, så det kan bruges i sammenkædede testsager.</span><span class="sxs-lookup"><span data-stu-id="f737d-190">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="f737d-191">Brug funktionen Valider i Opgaveregistrering til at angive kontrolpunkter, der bekræftet, at trinnene er blevet kørt korrekt.</span><span class="sxs-lookup"><span data-stu-id="f737d-191">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="f737d-192">RSAT</span><span class="sxs-lookup"><span data-stu-id="f737d-192">RSAT</span></span>

- <span data-ttu-id="f737d-193">Hvis du vil køre testen i et andet firma, kan du ændre firmaet under fanen **Generelt** i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="f737d-193">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="f737d-194">Sørg for, at indstillinger og data er tilgængelige i netop det valgte firma.</span><span class="sxs-lookup"><span data-stu-id="f737d-194">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="f737d-195">Du kan ændre testbrugeren under fanen **Generelt** i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="f737d-195">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="f737d-196">Angiv e-mail-id'et for den bruger, der skal køre testsagen.</span><span class="sxs-lookup"><span data-stu-id="f737d-196">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="f737d-197">På denne måde kan testsagen køres ved hjælp af sikkerhedstilladelserne for den angivne bruger.</span><span class="sxs-lookup"><span data-stu-id="f737d-197">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="f737d-198">Hvis du vil vente, før testen startes, kan du definere en pause under fanen **Generelt** i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="f737d-198">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="f737d-199">Denne pause kan bruges i et batchjob (f. eks. hvis en arbejdsgang skal køres, før næste trin kan udføres).</span><span class="sxs-lookup"><span data-stu-id="f737d-199">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="f737d-200">Avanceret scripting</span><span class="sxs-lookup"><span data-stu-id="f737d-200">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="f737d-201">CLI</span><span class="sxs-lookup"><span data-stu-id="f737d-201">CLI</span></span>

<span data-ttu-id="f737d-202">RSAT kan kaldes fra et **Kommandoprompt**- eller **PowerShell**-vindue.</span><span class="sxs-lookup"><span data-stu-id="f737d-202">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="f737d-203">Kontroller, at **TestRoot**-miljøvariablen er indstillet til RSAT-installationsstien.</span><span class="sxs-lookup"><span data-stu-id="f737d-203">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="f737d-204">(Gå til Microsoft Windows, åbn **Kontrolpanel**, vælg **System og sikkerhed \> System \> Avancerede systemindstillinger**, og vælg derefter **Miljøvariabler**.)</span><span class="sxs-lookup"><span data-stu-id="f737d-204">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="f737d-205">Åbn et **Kommandoprompt**- eller **PowerShell**-vindue som administrator.</span><span class="sxs-lookup"><span data-stu-id="f737d-205">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="f737d-206">Naviger til RSAT-installationsmappen.</span><span class="sxs-lookup"><span data-stu-id="f737d-206">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="f737d-207">Vis alle kommandoer.</span><span class="sxs-lookup"><span data-stu-id="f737d-207">List all commands.</span></span>

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a><span data-ttu-id="f737d-208">?</span><span class="sxs-lookup"><span data-stu-id="f737d-208">?</span></span> 
<span data-ttu-id="f737d-209">Viser hjælp om alle tilgængelige kommandoer og deres parametre.</span><span class="sxs-lookup"><span data-stu-id="f737d-209">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="f737d-210">Valgfrie parametre</span><span class="sxs-lookup"><span data-stu-id="f737d-210">Optional parameters</span></span>

**``command``**


<span data-ttu-id="f737d-211">Hvor ``[command]`` er en af de kommandoer, der er angivet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="f737d-211">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="f737d-212">om</span><span class="sxs-lookup"><span data-stu-id="f737d-212">about</span></span>
<span data-ttu-id="f737d-213">Viser den aktuelle version.</span><span class="sxs-lookup"><span data-stu-id="f737d-213">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="f737d-214">cls</span><span class="sxs-lookup"><span data-stu-id="f737d-214">cls</span></span>
<span data-ttu-id="f737d-215">Rydder skærmen.</span><span class="sxs-lookup"><span data-stu-id="f737d-215">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="f737d-216">hent</span><span class="sxs-lookup"><span data-stu-id="f737d-216">download</span></span>
<span data-ttu-id="f737d-217">Downloader vedhæftede filer for den angivne testcase til outputmappen.</span><span class="sxs-lookup"><span data-stu-id="f737d-217">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="f737d-218">Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases.</span><span class="sxs-lookup"><span data-stu-id="f737d-218">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="f737d-219">Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="f737d-219">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="f737d-220">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="f737d-220">Required parameters</span></span>
<span data-ttu-id="f737d-221">**``test_case_id``** Repræsenterer testcase-id'et.</span><span class="sxs-lookup"><span data-stu-id="f737d-221">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="f737d-222">**``output_dir``** Repræsenterer outputmappen.</span><span class="sxs-lookup"><span data-stu-id="f737d-222">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="f737d-223">Biblioteket skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="f737d-223">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="f737d-224">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f737d-224">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="f737d-225">rediger</span><span class="sxs-lookup"><span data-stu-id="f737d-225">edit</span></span>
<span data-ttu-id="f737d-226">Giver dig mulighed for at åbne parameterfilen i Excel-programmet og redigere den.</span><span class="sxs-lookup"><span data-stu-id="f737d-226">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="f737d-227">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="f737d-227">Required parameters</span></span>
<span data-ttu-id="f737d-228">**``excel_file``** Skal indeholde en fuldstændig sti til en eksisterende Excel-fil.</span><span class="sxs-lookup"><span data-stu-id="f737d-228">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="f737d-229">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f737d-229">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="f737d-230">generate</span><span class="sxs-lookup"><span data-stu-id="f737d-230">generate</span></span>
<span data-ttu-id="f737d-231">Opretter testkørsels- og -parameterfiler for det angivne testcase i outputmappen.</span><span class="sxs-lookup"><span data-stu-id="f737d-231">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="f737d-232">Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases.</span><span class="sxs-lookup"><span data-stu-id="f737d-232">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="f737d-233">Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="f737d-233">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="f737d-234">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="f737d-234">Required parameters</span></span>
<span data-ttu-id="f737d-235">**``test_case_id``** Repræsenterer testcase-id'et.</span><span class="sxs-lookup"><span data-stu-id="f737d-235">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="f737d-236">**``output_dir``** Repræsenterer outputmappen.</span><span class="sxs-lookup"><span data-stu-id="f737d-236">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="f737d-237">Biblioteket skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="f737d-237">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="f737d-238">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f737d-238">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="f737d-239">generatederived</span><span class="sxs-lookup"><span data-stu-id="f737d-239">generatederived</span></span>
<span data-ttu-id="f737d-240">Genererer en ny testcase, der er afledt fra den leverede testcase.</span><span class="sxs-lookup"><span data-stu-id="f737d-240">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="f737d-241">Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases.</span><span class="sxs-lookup"><span data-stu-id="f737d-241">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="f737d-242">Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="f737d-242">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="f737d-243">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="f737d-243">Required parameters</span></span>
<span data-ttu-id="f737d-244">**``parent_test_case_id``** Repræsenterer det overordnede testcase-id.</span><span class="sxs-lookup"><span data-stu-id="f737d-244">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="f737d-245">**``test_plan_id``** Repræsenterer testplan-id'et.</span><span class="sxs-lookup"><span data-stu-id="f737d-245">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="f737d-246">**``test_suite_id``** Repræsenterer testpakke-id'et.</span><span class="sxs-lookup"><span data-stu-id="f737d-246">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="f737d-247">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f737d-247">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="f737d-248">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="f737d-248">generatetestonly</span></span>
<span data-ttu-id="f737d-249">Opretter kun testkørselsfilen for det angivne testcase i outputmappen.</span><span class="sxs-lookup"><span data-stu-id="f737d-249">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="f737d-250">Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases.</span><span class="sxs-lookup"><span data-stu-id="f737d-250">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="f737d-251">Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="f737d-251">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="f737d-252">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="f737d-252">Required parameters</span></span>
<span data-ttu-id="f737d-253">**``test_case_id``** Repræsenterer testcase-id'et.</span><span class="sxs-lookup"><span data-stu-id="f737d-253">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="f737d-254">**``output_dir``** Repræsenterer outputmappen.</span><span class="sxs-lookup"><span data-stu-id="f737d-254">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="f737d-255">Biblioteket skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="f737d-255">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="f737d-256">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f737d-256">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="f737d-257">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="f737d-257">generatetestsuite</span></span>
<span data-ttu-id="f737d-258">Opretter alle testcases for den angivne pakke i outputmappen.</span><span class="sxs-lookup"><span data-stu-id="f737d-258">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="f737d-259">Du kan bruge kommandoen ``listtestsuitenames`` til at få vist alle tilgængelige testpakker.</span><span class="sxs-lookup"><span data-stu-id="f737d-259">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="f737d-260">Brug en vilkårlig værdi fra første kolonne som en **test_suite_name**-parameter.</span><span class="sxs-lookup"><span data-stu-id="f737d-260">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="f737d-261">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="f737d-261">Required parameters</span></span>
<span data-ttu-id="f737d-262">**``test_suite_name``** Repræsenterer testpakkenavnet.</span><span class="sxs-lookup"><span data-stu-id="f737d-262">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="f737d-263">**``output_dir``** Repræsenterer outputmappen.</span><span class="sxs-lookup"><span data-stu-id="f737d-263">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="f737d-264">Biblioteket skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="f737d-264">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="f737d-265">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f737d-265">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="f737d-266">help</span><span class="sxs-lookup"><span data-stu-id="f737d-266">help</span></span>
<span data-ttu-id="f737d-267">Identisk med [?](#section)</span><span class="sxs-lookup"><span data-stu-id="f737d-267">Identical to the [?](#section)</span></span> <span data-ttu-id="f737d-268">command</span><span class="sxs-lookup"><span data-stu-id="f737d-268">command</span></span>


#### <a name="list"></a><span data-ttu-id="f737d-269">listen</span><span class="sxs-lookup"><span data-stu-id="f737d-269">list</span></span>
<span data-ttu-id="f737d-270">Viser alle tilgængelige testcases.</span><span class="sxs-lookup"><span data-stu-id="f737d-270">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="f737d-271">listtestplans</span><span class="sxs-lookup"><span data-stu-id="f737d-271">listtestplans</span></span>
<span data-ttu-id="f737d-272">Viser alle tilgængelige testplaner.</span><span class="sxs-lookup"><span data-stu-id="f737d-272">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="f737d-273">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="f737d-273">listtestsuite</span></span>
<span data-ttu-id="f737d-274">Viser testcases for den angivne testpakke.</span><span class="sxs-lookup"><span data-stu-id="f737d-274">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="f737d-275">Du kan bruge kommandoen ``listtestsuitenames`` til at få vist alle tilgængelige pakker.</span><span class="sxs-lookup"><span data-stu-id="f737d-275">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="f737d-276">Brug en vilkårlig værdi fra første kolonne som **suite_name**-parameter.</span><span class="sxs-lookup"><span data-stu-id="f737d-276">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="f737d-277">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="f737d-277">Required parameters</span></span>
<span data-ttu-id="f737d-278">**``suite_name``** Navnet på den ønskede pakke.</span><span class="sxs-lookup"><span data-stu-id="f737d-278">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="f737d-279">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f737d-279">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="f737d-280">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="f737d-280">listtestsuitenames</span></span>
<span data-ttu-id="f737d-281">Viser alle tilgængelige testpakker.</span><span class="sxs-lookup"><span data-stu-id="f737d-281">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="f737d-282">playback</span><span class="sxs-lookup"><span data-stu-id="f737d-282">playback</span></span>
<span data-ttu-id="f737d-283">Afspiller en testcase ved hjælp af en Excel-fil.</span><span class="sxs-lookup"><span data-stu-id="f737d-283">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="f737d-284">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="f737d-284">Required parameters</span></span>
<span data-ttu-id="f737d-285">**``excel_file``** En fuld sti til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="f737d-285">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="f737d-286">Filen skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="f737d-286">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="f737d-287">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f737d-287">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="f737d-288">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="f737d-288">playbackbyid</span></span>
<span data-ttu-id="f737d-289">Afspiller flere testcases på én gang.</span><span class="sxs-lookup"><span data-stu-id="f737d-289">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="f737d-290">Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases.</span><span class="sxs-lookup"><span data-stu-id="f737d-290">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="f737d-291">Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="f737d-291">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="f737d-292">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="f737d-292">Required parameters</span></span>
<span data-ttu-id="f737d-293">**``test_case_id1``** Id for eksisterende testcase.</span><span class="sxs-lookup"><span data-stu-id="f737d-293">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="f737d-294">**``test_case_id2``** Id for eksisterende testcase.</span><span class="sxs-lookup"><span data-stu-id="f737d-294">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="f737d-295">**``test_case_idN``** Id for eksisterende testcase.</span><span class="sxs-lookup"><span data-stu-id="f737d-295">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="f737d-296">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f737d-296">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="f737d-297">playbackmany</span><span class="sxs-lookup"><span data-stu-id="f737d-297">playbackmany</span></span>
<span data-ttu-id="f737d-298">Afspiller mange testcases på én gang ved hjælp af Excel-filer.</span><span class="sxs-lookup"><span data-stu-id="f737d-298">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="f737d-299">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="f737d-299">Required parameters</span></span>
<span data-ttu-id="f737d-300">**``excel_file1``** Fuld sti til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="f737d-300">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="f737d-301">Filen skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="f737d-301">File must exist.</span></span>  
<span data-ttu-id="f737d-302">**``excel_file2``** Fuld sti til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="f737d-302">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="f737d-303">Filen skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="f737d-303">File must exist.</span></span>  
<span data-ttu-id="f737d-304">**``excel_fileN``** Fuld sti til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="f737d-304">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="f737d-305">Filen skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="f737d-305">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="f737d-306">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f737d-306">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="f737d-307">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="f737d-307">playbacksuite</span></span>
<span data-ttu-id="f737d-308">Afspiller alle testcases fra den angivne testpakke.</span><span class="sxs-lookup"><span data-stu-id="f737d-308">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="f737d-309">Du kan bruge kommandoen ``listtestsuitenames`` til at få vist alle tilgængelige pakker.</span><span class="sxs-lookup"><span data-stu-id="f737d-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="f737d-310">Brug en vilkårlig værdi fra første kolonne som **suite_name**-parameter.</span><span class="sxs-lookup"><span data-stu-id="f737d-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="f737d-311">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="f737d-311">Required parameters</span></span>
<span data-ttu-id="f737d-312">**``suite_name``** Navnet på den ønskede pakke.</span><span class="sxs-lookup"><span data-stu-id="f737d-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="f737d-313">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f737d-313">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="f737d-314">quit</span><span class="sxs-lookup"><span data-stu-id="f737d-314">quit</span></span>
<span data-ttu-id="f737d-315">Lukker programmet.</span><span class="sxs-lookup"><span data-stu-id="f737d-315">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="f737d-316">upload</span><span class="sxs-lookup"><span data-stu-id="f737d-316">upload</span></span>
<span data-ttu-id="f737d-317">Uploader alle de filer, der hører til den angivne testpakke eller de angivne testcases.</span><span class="sxs-lookup"><span data-stu-id="f737d-317">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="f737d-318">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="f737d-318">Required parameters</span></span>
<span data-ttu-id="f737d-319">**``suite_name``** Alle de filer, der hører til den angivne testpakke, bliver uploadet.</span><span class="sxs-lookup"><span data-stu-id="f737d-319">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="f737d-320">**``testcase_id``** Alle de filer, der hører til den eller de angivne testcases, bliver uploadet.</span><span class="sxs-lookup"><span data-stu-id="f737d-320">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="f737d-321">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f737d-321">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="f737d-322">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="f737d-322">uploadrecording</span></span>
<span data-ttu-id="f737d-323">Uploader kun den optagne fil, der hører til de angivne testcases.</span><span class="sxs-lookup"><span data-stu-id="f737d-323">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="f737d-324">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="f737d-324">Required parameters</span></span>
<span data-ttu-id="f737d-325">**``testcase_id``** Den optagne fil, der hører til de angivne testcases, bliver uploadet.</span><span class="sxs-lookup"><span data-stu-id="f737d-325">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="f737d-326">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f737d-326">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="f737d-327">usage</span><span class="sxs-lookup"><span data-stu-id="f737d-327">usage</span></span>
<span data-ttu-id="f737d-328">Viser to måder at aktivere dette program på: en, der bruger en fil med standardindstillinger, en anden, der angiver en fil med indstillinger.</span><span class="sxs-lookup"><span data-stu-id="f737d-328">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="f737d-329">Windows PowerShell-eksempler</span><span class="sxs-lookup"><span data-stu-id="f737d-329">Windows PowerShell examples</span></span>

[!IMPORTANT] <span data-ttu-id="f737d-330">Nedenstående eksempelscripts leveres, som DE ER, og er beregnet til illustrationsformål og understøttes ikke af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f737d-330">The example scripts below are provided AS IS for illustration purposes and are not supported by Microsoft.</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="f737d-331">Køre en testsag i en løkke</span><span class="sxs-lookup"><span data-stu-id="f737d-331">Run a test case in a loop</span></span>

<span data-ttu-id="f737d-332">Du har et testscript, der opretter en ny kunde.</span><span class="sxs-lookup"><span data-stu-id="f737d-332">You have a test script that creates a new customer.</span></span> <span data-ttu-id="f737d-333">Ved hjælp af scripting kan denne testsag køres i en løkke ved at gøre følgende data tilfældige, før hver enkelt gentagelse køres:</span><span class="sxs-lookup"><span data-stu-id="f737d-333">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="f737d-334">Debitor-id</span><span class="sxs-lookup"><span data-stu-id="f737d-334">Customer ID</span></span>
- <span data-ttu-id="f737d-335">Navn på debitor</span><span class="sxs-lookup"><span data-stu-id="f737d-335">Customer name</span></span>
- <span data-ttu-id="f737d-336">Debitors adresse</span><span class="sxs-lookup"><span data-stu-id="f737d-336">Customer address</span></span>

<span data-ttu-id="f737d-337">Kunde-id'et har formatet *ATCUS\<tal\>*, hvor \<tal\> er en værdi mellem **000000001** og **999999999**.</span><span class="sxs-lookup"><span data-stu-id="f737d-337">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="f737d-338">I følgende eksempel bruges en parameter, **start**, til at definere det første tal, der bruges.</span><span class="sxs-lookup"><span data-stu-id="f737d-338">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="f737d-339">Er bruger en anden parameter, **nr**, til at det definere det antal kunder, der skal oprettes.</span><span class="sxs-lookup"><span data-stu-id="f737d-339">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="f737d-340">For hver gentagelse ændres parametrene i Excel-parameterfilen ved hjælp af en UpdateCustomer-funktion.</span><span class="sxs-lookup"><span data-stu-id="f737d-340">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="f737d-341">Derefter kaldes RSAT-kommandolinjen i en RunTestCase-funktion.</span><span class="sxs-lookup"><span data-stu-id="f737d-341">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="f737d-342">Åbn Microsoft Windows PowerShell Integrated Scripting Environment (ISE) i admininistratortilstand, og indsæt følgende kode i det vindue, der hedder **Uden titel.ps1**.</span><span class="sxs-lookup"><span data-stu-id="f737d-342">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="f737d-343">Køre et script, der afhænger af data i Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f737d-343">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="f737d-344">I følgende eksempel bruges et OData-kald (Open data Protocol) til at finde ordrestatussen for en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="f737d-344">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="f737d-345">Hvis status ikke er **faktureret**, kan du f.eks. kalde en RSAT-testsag, der bogfører fakturaen.</span><span class="sxs-lookup"><span data-stu-id="f737d-345">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```
