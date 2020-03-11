---
title: Bruge Regression Suite Automation Tool
description: I dette emne vises, hvordan du kan bruge værktøjet RSAT (Regression Suite Automation Tool). Det beskriver forskellige funktioner og indeholder eksempler, der bruger avanceret scripting.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 6cdaa89fb6d50ebaaaefe7f92d7224a1567d17d1
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070814"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="6af6b-104">Brug Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="6af6b-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="6af6b-105">Brug dine internetbrowserværktøjer til at downloade og gemme denne side i PDF-format.</span><span class="sxs-lookup"><span data-stu-id="6af6b-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="6af6b-106">Dette selvstudium gennemgår nogle af de avancerede funktioner i RSAT (Regression suite automation tool), herunder en demoopgave og beskriver strategi og centrale undervisningspunkter.</span><span class="sxs-lookup"><span data-stu-id="6af6b-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="6af6b-107">Funktioner i RSAT/Arbejdsrutineoptager</span><span class="sxs-lookup"><span data-stu-id="6af6b-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="6af6b-108">Valider en feltværdi</span><span class="sxs-lookup"><span data-stu-id="6af6b-108">Validate a field value</span></span>

<span data-ttu-id="6af6b-109">Du kan finde flere oplysninger om denne funktion under [Oprette en ny opgaveregistrering, der har en valideringsfunktion](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="6af6b-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="6af6b-110">Gemt variabel</span><span class="sxs-lookup"><span data-stu-id="6af6b-110">Saved variable</span></span>

<span data-ttu-id="6af6b-111">Du kan finde flere oplysninger om denne funktion under [Redigere en eksisterende opgaveregistrering for at oprette en gemt variabel](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="6af6b-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="6af6b-112">Afledt testsag</span><span class="sxs-lookup"><span data-stu-id="6af6b-112">Derived test case</span></span>

1. <span data-ttu-id="6af6b-113">Åbn Regression suite automation tool (RSAT), og vælg begge testsager, du har oprettet i [Konfigurere og installere selvstudium til Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="6af6b-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool tutorial](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="6af6b-114">Vælg **Ny \> Opret afledt testsag**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-114">Select **New \> Create derived test case**.</span></span>

    ![Kommandoen Opret afledt testsag i menuen Ny](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="6af6b-116">Du får vist en meddelelse, hvor det angives, at der oprettes en afledt test sag for hver valgt testsag i den aktuelle testpakke, og at hver afledt testsag vil have sin egen kopi af Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="6af6b-117">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6af6b-118">Når du kører en afledt testsag, bruger den en opgaveregistrering af den overordnede test og dens egen kopi af Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="6af6b-119">På denne måde kan du køre den samme test med forskellige parametre uden at skulle vedligeholde mere end én opgaveregistrering.</span><span class="sxs-lookup"><span data-stu-id="6af6b-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="6af6b-120">En afledt testsag behøver ikke at være en del af samme testpakke som dens overordnede testsag.</span><span class="sxs-lookup"><span data-stu-id="6af6b-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Meddelelsesboks](./media/use_rsa_tool_02.png)

    <span data-ttu-id="6af6b-122">Der oprettes to ekstra afledte testsager, og afkrydsningsfeltet **Afledt?** er markeret for dem.</span><span class="sxs-lookup"><span data-stu-id="6af6b-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Afledte testsager oprettet](./media/use_rsa_tool_03.png)

    <span data-ttu-id="6af6b-124">Der oprettes automatisk en afledt testsag i Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6af6b-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="6af6b-125">Det er et underordnet element til testsagen **Opret et nyt produkt** og mærkes med et særligt nøgleord: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="6af6b-126">Disse testsager føjes også automatisk til testplanen i Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6af6b-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![Nøgleordet RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="6af6b-128">Hvis de afledte testsager, der oprettes, af en eller anden årsag ikke har den rigtige ordre, skal du gå til Azure DevOps og omarrangere testsagerne i testpakken, så RSAT kan køre dem i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="6af6b-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="6af6b-129">Vælg de afledte testsager, og vælg derefter **Rediger** for at åbne de tilhørende Excel-parameterfiler.</span><span class="sxs-lookup"><span data-stu-id="6af6b-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="6af6b-130">Rediger disse Excel-parameter filer på samme måde, som du redigerede de overordnede filer.</span><span class="sxs-lookup"><span data-stu-id="6af6b-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="6af6b-131">Med andre ord skal du sikre dig, at produkt-id'et er angivet, så det genereres automatisk.</span><span class="sxs-lookup"><span data-stu-id="6af6b-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="6af6b-132">Kontroller også, at den gemte variabel kopieres til de relevante felter.</span><span class="sxs-lookup"><span data-stu-id="6af6b-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="6af6b-133">Gå til fanen **Generelt** i begge Excel-parameterfiler, opdater værdien af feltet **Firma** til **USSI**, så de afledte testsager køres mod en anden juridisk enhed end den overordnede testsag.</span><span class="sxs-lookup"><span data-stu-id="6af6b-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="6af6b-134">Hvis du vil køre testsagerne mod en bestemt bruger (eller den rolle, der er knyttet til en bestemt bruger), kan du opdatere værdien i feltet **Testbruger**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="6af6b-135">Vælg **Kør**, og kontroller, at produktet er oprettet i både den juridiske enhed, USMF, og den juridiske enhed, USSI.</span><span class="sxs-lookup"><span data-stu-id="6af6b-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="6af6b-136">Valider beskeder</span><span class="sxs-lookup"><span data-stu-id="6af6b-136">Validate notifications</span></span>

<span data-ttu-id="6af6b-137">Denne funktion kan bruges til at validere, om der opstod en handling.</span><span class="sxs-lookup"><span data-stu-id="6af6b-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="6af6b-138">Når der f.eks. oprettes, estimeres og derefter startes en produktionsordre, viser appen meddelelsen "Produktion – start" for at give dig besked om, at produktionsordren er startet.</span><span class="sxs-lookup"><span data-stu-id="6af6b-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Beskeden Produktion – start](./media/use_rsa_tool_05.png)

<span data-ttu-id="6af6b-140">Du kan validere denne meddelelse via RSAT ved at angive meddelelsesteksten under fanen **Meddelelsesvalidering** i Excel-parameterfilen for den relevante registrering.</span><span class="sxs-lookup"><span data-stu-id="6af6b-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Fanen Meddelelsesvalidering](./media/use_rsa_tool_06.png)

<span data-ttu-id="6af6b-142">Når testsagen er kørt, sammenlignes meddelelsen i Excel-parameterfilen med den viste meddelelse.</span><span class="sxs-lookup"><span data-stu-id="6af6b-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="6af6b-143">Hvis meddelelserne ikke stemmer overens, vil testsagen mislykkes.</span><span class="sxs-lookup"><span data-stu-id="6af6b-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="6af6b-144">Du kan angive mere end én meddelelse under fanen **Meddelelsesvalidering** i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="6af6b-145">Meddelelserne kan også være fejl- eller advarselsmeddelelser i stedet for orienterende meddelelser.</span><span class="sxs-lookup"><span data-stu-id="6af6b-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="6af6b-146">Valider værdier ved hjælp af operatorer</span><span class="sxs-lookup"><span data-stu-id="6af6b-146">Validate values by using operators</span></span>

<span data-ttu-id="6af6b-147">I tidligere versioner af RSAT kunne du kun validere værdier, hvis en kontrolværdi var lig med en forventet værdi.</span><span class="sxs-lookup"><span data-stu-id="6af6b-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="6af6b-148">Den nye funktion giver dig mulighed for at validere, at en variabel ikke er lig med, er mindre end eller mere end en angivet værdi.</span><span class="sxs-lookup"><span data-stu-id="6af6b-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="6af6b-149">Hvis du vil bruge denne funktion, skal du åbne filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installationsmappen (f.eks. **C:\\Program Files (x86)\\Regression Suite Automation Tool**), og ændre værdien i det følgende element fra **falsk** til **sand**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="6af6b-150">I Excel-parameterfilen vises et nyt felt **Operator**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6af6b-151">Hvis du har brugt en ældre version af RSAT, skal du oprette nye Excel-parameterfiler.</span><span class="sxs-lookup"><span data-stu-id="6af6b-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Feltet Operator](./media/use_rsa_tool_07.png)

<span data-ttu-id="6af6b-153">I følgende eksempel vises, hvordan du kan bruge denne funktion til at validere, om den disponible lagerbeholdning er større end 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="6af6b-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="6af6b-154">I demodataene i **USMF**-firmaet skal du oprette en opgaveregistrering, der indeholder følgende trin:</span><span class="sxs-lookup"><span data-stu-id="6af6b-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="6af6b-155">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="6af6b-156">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="6af6b-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6af6b-157">Filtrer f.eks. efter en værdi på **1000** for feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="6af6b-158">Vælg **Disponibel lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="6af6b-159">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="6af6b-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6af6b-160">Du kan f.eks. filtrere efter værdien **1** for feltet **Lokation**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="6af6b-161">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="6af6b-162">Kontroller, at værdien af feltet **I alt disponibelt** er **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="6af6b-163">Gem opgaveregistreringen i BPM-biblioteket i LCS, og synkroniser den med Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6af6b-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="6af6b-164">Føj testsagen til testplanen, og Indlæs testsagen i RSAT.</span><span class="sxs-lookup"><span data-stu-id="6af6b-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="6af6b-165">Åbn Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-165">Open the Excel parameter file.</span></span> <span data-ttu-id="6af6b-166">Under fanen **InventOnhandItem** kan du se afsnittet **Valider InventOnhandItem**, der indeholder feltet **operator**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Feltet Operator](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="6af6b-168">Hvis du vil validere, om den disponible lagerbeholdning altid vil være mere end 0, skal du ændre værdien af feltet **Værdi** fra **411** til **0** og værdien af feltet **Operator** fra et lighedstegn (**=**) til et større end tegn (**\>**).</span><span class="sxs-lookup"><span data-stu-id="6af6b-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Værdierne i felterne Værdi og Operator ændres](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="6af6b-170">Gem og luk Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="6af6b-171">Vælg **Overfør** for at gemme de ændringer, du har foretaget, i Excel-parameterfilen Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6af6b-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="6af6b-172">Hvis værdien af feltet **I alt disponibelt** for den angivne vare på lageret er større end 0 (nul), vil testene bestå, uanset den faktiske værdi for disponibel lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="6af6b-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="6af6b-173">Generatorlogfiler</span><span class="sxs-lookup"><span data-stu-id="6af6b-173">Generator logs</span></span>

<span data-ttu-id="6af6b-174">Denne funktion opretter en mappe, der indeholder logfilerne for de testsager, der er blevet kørt.</span><span class="sxs-lookup"><span data-stu-id="6af6b-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="6af6b-175">Hvis du vil bruge denne funktion, skal du åbne filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installationsmappen (f.eks. **C:\\Program Files (x86)\\Regression Suite Automation Tool**), og ændre værdien i det følgende element fra **falsk** til **sand**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="6af6b-176">Når testsagerne er kørt, kan du finde logfilerne under **C:\\Brugere\\\<Brugernavn\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![Mappen GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="6af6b-178">Hvis der var eksisterende testsager, før du ændrede værdien i. config-filen, oprettes der ikke logfiler for disse testsager, før du opretter nye testkørselsfiler.</span><span class="sxs-lookup"><span data-stu-id="6af6b-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Kommandoen Generér kun testkørselsfiler i menuen Ny](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="6af6b-180">Øjebliksbillede</span><span class="sxs-lookup"><span data-stu-id="6af6b-180">Snapshot</span></span>

<span data-ttu-id="6af6b-181">Denne funktion bruger skærmbilleder af de trin, der blev udført under opgaveregistreringen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="6af6b-182">Hvis du vil bruge denne funktion, skal du åbne filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installationsmappen (f.eks. **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og ændre værdien af det følgende element fra **falsk** til **sand**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="6af6b-183">Under **C:\\Brugere\\\<Brugernavn\>\\AppData\\Roaming\\regressionTool\\playback** oprettes der en separat mappe for hver testsag, der køres.</span><span class="sxs-lookup"><span data-stu-id="6af6b-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Mappen til øjebliksbiller for en testsag](./media/use_rsa_tool_12.png)

<span data-ttu-id="6af6b-185">I hver af disse mapper kan du finde øjebliksbilleder af de trin, der blev udført, mens testsagerne blev kørt.</span><span class="sxs-lookup"><span data-stu-id="6af6b-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Øjebliksfiler](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="6af6b-187">Tilknytning</span><span class="sxs-lookup"><span data-stu-id="6af6b-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="6af6b-188">Scenarie</span><span class="sxs-lookup"><span data-stu-id="6af6b-188">Scenario</span></span>

1. <span data-ttu-id="6af6b-189">Produktdesigneren opretter et nyt, frigivet produkt.</span><span class="sxs-lookup"><span data-stu-id="6af6b-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="6af6b-190">Produktionschefen starter en produktionsordre for at bringe lagerniveauet op til to styk.</span><span class="sxs-lookup"><span data-stu-id="6af6b-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="6af6b-191">Produktionen starter og afslutter produktionsordren og kontrollerer, at det disponible antal er to styk.</span><span class="sxs-lookup"><span data-stu-id="6af6b-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="6af6b-192">Salgsteamet modtager en ordre på fire stykker af det nye produkt.</span><span class="sxs-lookup"><span data-stu-id="6af6b-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="6af6b-193">Salgsgruppen opdaterer derfor nettokravene via den dynamiske plan.</span><span class="sxs-lookup"><span data-stu-id="6af6b-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="6af6b-194">Da der ikke er mere tilgængelig kapacitet, er standardordrepolitikken indstillet til "køb i stedet for at fremstille".</span><span class="sxs-lookup"><span data-stu-id="6af6b-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="6af6b-195">Derfor oprettes der et salgsforslag.</span><span class="sxs-lookup"><span data-stu-id="6af6b-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="6af6b-196">Køberen tilføjer en kreditor, autoriserer indkøbsordreforslaget og bekræfter derefter indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="6af6b-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="6af6b-197">Når de købte varer ankommer til butikken, søger butiksoperatøren efter den relaterede indkøbsordre og modtager varerne.</span><span class="sxs-lookup"><span data-stu-id="6af6b-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="6af6b-198">Da ordren nu er fuldført, kan varer plukkes og pakkes i forhold til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="6af6b-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="6af6b-199">Finans bogfører købsfakturaen og salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="6af6b-200">I følgende illustration vises flowet i dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="6af6b-200">The following illustration shows the flow for this scenario.</span></span>

![Flow for demoscenariet](./media/use_rsa_tool_14.png)

<span data-ttu-id="6af6b-202">I følgende illustration vises forretningsprocesserne for dette scenario i RSAT.</span><span class="sxs-lookup"><span data-stu-id="6af6b-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Forretningsprocesser til demoscenariet](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="6af6b-204">Strategi – vigtig læring</span><span class="sxs-lookup"><span data-stu-id="6af6b-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="6af6b-205">Data</span><span class="sxs-lookup"><span data-stu-id="6af6b-205">Data</span></span>

- <span data-ttu-id="6af6b-206">Sørg for, at du har repræsentative datamængder (en kopi af produktion/gyldne konfigurationsdata plus overførte data).</span><span class="sxs-lookup"><span data-stu-id="6af6b-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="6af6b-207">Når du genererer nye data via en opgaveregistrering, skal du oprette testnavne, der ikke er i konflikt med eksisterende navne (brug f.eks. et præfisk såsom **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="6af6b-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="6af6b-208">Brug Azures funktion til genoprettelse af et bestemt tidspunkt for at køre test i miljøjer, der ikke er niveau 1, igen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="6af6b-209">Selvom du kan bruge Excel-funktionerne **VILKÅRLIG** og **NU** til at generere en entydig kombination, kræver det ret meget arbejde.</span><span class="sxs-lookup"><span data-stu-id="6af6b-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="6af6b-210">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="6af6b-210">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="6af6b-211">Arbejdsrutineoptager</span><span class="sxs-lookup"><span data-stu-id="6af6b-211">Task recorder</span></span>

- <span data-ttu-id="6af6b-212">Definer scenarierne, før du går i gang med at registrere.</span><span class="sxs-lookup"><span data-stu-id="6af6b-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="6af6b-213">Et godt styret projekt har foruddefinerede testscenarier.</span><span class="sxs-lookup"><span data-stu-id="6af6b-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="6af6b-214">Hvis du vil oprette en testsag, skal du overveje, hvor forudsigelige udfaldet af disse testsituationer er.</span><span class="sxs-lookup"><span data-stu-id="6af6b-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="6af6b-215">Opdel registreringer, hvis de udføres af forskellige roller, eller hvis der er ventetiden eller en ekstern hændelse før næste trin.</span><span class="sxs-lookup"><span data-stu-id="6af6b-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="6af6b-216">Undgå at vælge værdier på lister.</span><span class="sxs-lookup"><span data-stu-id="6af6b-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="6af6b-217">Brug i stedet tekstformater som f.eks **FIFO**, **AudioRM** og **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="6af6b-218">Når du vælger på en liste, registreres placeringen af værdien på listen, ikke selve værdien.</span><span class="sxs-lookup"><span data-stu-id="6af6b-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="6af6b-219">Hvis der føjes varer til listen, kan placeringen af værdien ændres.</span><span class="sxs-lookup"><span data-stu-id="6af6b-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="6af6b-220">Derfor vil din registrering bruge en anden parameter, og resten af scenariet kan blive påvirket.</span><span class="sxs-lookup"><span data-stu-id="6af6b-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="6af6b-221">Tænk over funktionsmåde for flere brugere.</span><span class="sxs-lookup"><span data-stu-id="6af6b-221">Think about multi-user behavior.</span></span> <span data-ttu-id="6af6b-222">Antag f. eks. ikke, at din nyoprettede salgsordre altid skal vælges automatisk.</span><span class="sxs-lookup"><span data-stu-id="6af6b-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="6af6b-223">Brug i stedet for altid filteret til at finde den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="6af6b-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="6af6b-224">Brug funktionen Kopier i Opgaveregistrering til at gemme navnet på et nyoprettet produkt, så det kan bruges i sammenkædede testsager.</span><span class="sxs-lookup"><span data-stu-id="6af6b-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="6af6b-225">Brug funktionen Valider i Opgaveregistrering til at angive kontrolpunkter, der bekræftet, at trinnene er blevet kørt korrekt.</span><span class="sxs-lookup"><span data-stu-id="6af6b-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="6af6b-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="6af6b-226">RSAT</span></span>

- <span data-ttu-id="6af6b-227">Hvis du vil køre testen i et andet firma, kan du ændre firmaet under fanen **Generelt** i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="6af6b-228">Sørg for, at indstillinger og data er tilgængelige i netop det valgte firma.</span><span class="sxs-lookup"><span data-stu-id="6af6b-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="6af6b-229">Du kan ændre testbrugeren under fanen **Generelt** i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="6af6b-230">Angiv e-mail-id'et for den bruger, der skal køre testsagen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="6af6b-231">På denne måde kan testsagen køres ved hjælp af sikkerhedstilladelserne for den angivne bruger.</span><span class="sxs-lookup"><span data-stu-id="6af6b-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="6af6b-232">Hvis du vil vente, før testen startes, kan du definere en pause under fanen **Generelt** i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="6af6b-233">Denne pause kan bruges i et batchjob (f. eks. hvis en arbejdsgang skal køres, før næste trin kan udføres).</span><span class="sxs-lookup"><span data-stu-id="6af6b-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="6af6b-234">Avanceret scripting</span><span class="sxs-lookup"><span data-stu-id="6af6b-234">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="6af6b-235">CLI</span><span class="sxs-lookup"><span data-stu-id="6af6b-235">CLI</span></span>

<span data-ttu-id="6af6b-236">RSAT kan kaldes fra et **Kommandoprompt**- eller **PowerShell**-vindue.</span><span class="sxs-lookup"><span data-stu-id="6af6b-236">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="6af6b-237">Kontroller, at **TestRoot**-miljøvariablen er indstillet til RSAT-installationsstien.</span><span class="sxs-lookup"><span data-stu-id="6af6b-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="6af6b-238">(Gå til Microsoft Windows, åbn **Kontrolpanel**, vælg **System og sikkerhed \> System \> Avancerede systemindstillinger**, og vælg derefter **Miljøvariabler**.)</span><span class="sxs-lookup"><span data-stu-id="6af6b-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="6af6b-239">Åbn et **Kommandoprompt**- eller **PowerShell**-vindue som administrator.</span><span class="sxs-lookup"><span data-stu-id="6af6b-239">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="6af6b-240">Naviger til RSAT-installationsmappen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-240">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="6af6b-241">Vis alle kommandoer.</span><span class="sxs-lookup"><span data-stu-id="6af6b-241">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="6af6b-242">?</span><span class="sxs-lookup"><span data-stu-id="6af6b-242">?</span></span> 
<span data-ttu-id="6af6b-243">Viser hjælp om alle tilgængelige kommandoer og deres parametre.</span><span class="sxs-lookup"><span data-stu-id="6af6b-243">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="6af6b-244">Valgfrie parametre</span><span class="sxs-lookup"><span data-stu-id="6af6b-244">Optional parameters</span></span>

**``command``**


<span data-ttu-id="6af6b-245">Hvor ``[command]`` er en af de kommandoer, der er angivet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="6af6b-245">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="6af6b-246">om</span><span class="sxs-lookup"><span data-stu-id="6af6b-246">about</span></span>
<span data-ttu-id="6af6b-247">Viser den aktuelle version.</span><span class="sxs-lookup"><span data-stu-id="6af6b-247">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="6af6b-248">cls</span><span class="sxs-lookup"><span data-stu-id="6af6b-248">cls</span></span>
<span data-ttu-id="6af6b-249">Rydder skærmen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-249">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="6af6b-250">hent</span><span class="sxs-lookup"><span data-stu-id="6af6b-250">download</span></span>
<span data-ttu-id="6af6b-251">Downloader vedhæftede filer for den angivne testcase til outputmappen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-251">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="6af6b-252">Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases.</span><span class="sxs-lookup"><span data-stu-id="6af6b-252">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="6af6b-253">Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="6af6b-253">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="6af6b-254">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="6af6b-254">Required parameters</span></span>
<span data-ttu-id="6af6b-255">**``test_case_id``** Repræsenterer testcase-id'et.</span><span class="sxs-lookup"><span data-stu-id="6af6b-255">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="6af6b-256">**``output_dir``** Repræsenterer outputmappen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-256">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="6af6b-257">Biblioteket skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="6af6b-257">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="6af6b-258">Eksempler</span><span class="sxs-lookup"><span data-stu-id="6af6b-258">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="6af6b-259">rediger</span><span class="sxs-lookup"><span data-stu-id="6af6b-259">edit</span></span>
<span data-ttu-id="6af6b-260">Giver dig mulighed for at åbne parameterfilen i Excel-programmet og redigere den.</span><span class="sxs-lookup"><span data-stu-id="6af6b-260">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="6af6b-261">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="6af6b-261">Required parameters</span></span>
<span data-ttu-id="6af6b-262">**``excel_file``** Skal indeholde en fuldstændig sti til en eksisterende Excel-fil.</span><span class="sxs-lookup"><span data-stu-id="6af6b-262">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="6af6b-263">Eksempler</span><span class="sxs-lookup"><span data-stu-id="6af6b-263">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="6af6b-264">generate</span><span class="sxs-lookup"><span data-stu-id="6af6b-264">generate</span></span>
<span data-ttu-id="6af6b-265">Opretter testkørsels- og -parameterfiler for det angivne testcase i outputmappen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-265">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="6af6b-266">Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases.</span><span class="sxs-lookup"><span data-stu-id="6af6b-266">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="6af6b-267">Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="6af6b-267">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="6af6b-268">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="6af6b-268">Required parameters</span></span>
<span data-ttu-id="6af6b-269">**``test_case_id``** Repræsenterer testcase-id'et.</span><span class="sxs-lookup"><span data-stu-id="6af6b-269">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="6af6b-270">**``output_dir``** Repræsenterer outputmappen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-270">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="6af6b-271">Biblioteket skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="6af6b-271">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="6af6b-272">Eksempler</span><span class="sxs-lookup"><span data-stu-id="6af6b-272">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="6af6b-273">generatederived</span><span class="sxs-lookup"><span data-stu-id="6af6b-273">generatederived</span></span>
<span data-ttu-id="6af6b-274">Genererer en ny testcase, der er afledt fra den leverede testcase.</span><span class="sxs-lookup"><span data-stu-id="6af6b-274">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="6af6b-275">Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases.</span><span class="sxs-lookup"><span data-stu-id="6af6b-275">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="6af6b-276">Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="6af6b-276">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="6af6b-277">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="6af6b-277">Required parameters</span></span>
<span data-ttu-id="6af6b-278">**``parent_test_case_id``** Repræsenterer det overordnede testcase-id.</span><span class="sxs-lookup"><span data-stu-id="6af6b-278">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="6af6b-279">**``test_plan_id``** Repræsenterer testplan-id'et.</span><span class="sxs-lookup"><span data-stu-id="6af6b-279">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="6af6b-280">**``test_suite_id``** Repræsenterer testpakke-id'et.</span><span class="sxs-lookup"><span data-stu-id="6af6b-280">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="6af6b-281">Eksempler</span><span class="sxs-lookup"><span data-stu-id="6af6b-281">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="6af6b-282">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="6af6b-282">generatetestonly</span></span>
<span data-ttu-id="6af6b-283">Opretter kun testkørselsfilen for det angivne testcase i outputmappen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-283">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="6af6b-284">Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases.</span><span class="sxs-lookup"><span data-stu-id="6af6b-284">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="6af6b-285">Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="6af6b-285">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="6af6b-286">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="6af6b-286">Required parameters</span></span>
<span data-ttu-id="6af6b-287">**``test_case_id``** Repræsenterer testcase-id'et.</span><span class="sxs-lookup"><span data-stu-id="6af6b-287">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="6af6b-288">**``output_dir``** Repræsenterer outputmappen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-288">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="6af6b-289">Biblioteket skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="6af6b-289">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="6af6b-290">Eksempler</span><span class="sxs-lookup"><span data-stu-id="6af6b-290">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="6af6b-291">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="6af6b-291">generatetestsuite</span></span>
<span data-ttu-id="6af6b-292">Opretter alle testcases for den angivne pakke i outputmappen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-292">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="6af6b-293">Du kan bruge kommandoen ``listtestsuitenames`` til at få vist alle tilgængelige testpakker.</span><span class="sxs-lookup"><span data-stu-id="6af6b-293">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="6af6b-294">Brug en vilkårlig værdi fra første kolonne som en **test_suite_name**-parameter.</span><span class="sxs-lookup"><span data-stu-id="6af6b-294">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="6af6b-295">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="6af6b-295">Required parameters</span></span>
<span data-ttu-id="6af6b-296">**``test_suite_name``** Repræsenterer testpakkenavnet.</span><span class="sxs-lookup"><span data-stu-id="6af6b-296">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="6af6b-297">**``output_dir``** Repræsenterer outputmappen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-297">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="6af6b-298">Biblioteket skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="6af6b-298">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="6af6b-299">Eksempler</span><span class="sxs-lookup"><span data-stu-id="6af6b-299">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="6af6b-300">help</span><span class="sxs-lookup"><span data-stu-id="6af6b-300">help</span></span>
<span data-ttu-id="6af6b-301">Identisk med [?](####?)</span><span class="sxs-lookup"><span data-stu-id="6af6b-301">Identical to the [?](####?)</span></span> <span data-ttu-id="6af6b-302">command</span><span class="sxs-lookup"><span data-stu-id="6af6b-302">command</span></span>


#### <a name="list"></a><span data-ttu-id="6af6b-303">listen</span><span class="sxs-lookup"><span data-stu-id="6af6b-303">list</span></span>
<span data-ttu-id="6af6b-304">Viser alle tilgængelige testcases.</span><span class="sxs-lookup"><span data-stu-id="6af6b-304">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="6af6b-305">listtestplans</span><span class="sxs-lookup"><span data-stu-id="6af6b-305">listtestplans</span></span>
<span data-ttu-id="6af6b-306">Viser alle tilgængelige testplaner.</span><span class="sxs-lookup"><span data-stu-id="6af6b-306">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="6af6b-307">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="6af6b-307">listtestsuite</span></span>
<span data-ttu-id="6af6b-308">Viser testcases for den angivne testpakke.</span><span class="sxs-lookup"><span data-stu-id="6af6b-308">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="6af6b-309">Du kan bruge kommandoen ``listtestsuitenames`` til at få vist alle tilgængelige pakker.</span><span class="sxs-lookup"><span data-stu-id="6af6b-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="6af6b-310">Brug en vilkårlig værdi fra første kolonne som **suite_name**-parameter.</span><span class="sxs-lookup"><span data-stu-id="6af6b-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="6af6b-311">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="6af6b-311">Required parameters</span></span>
<span data-ttu-id="6af6b-312">**``suite_name``** Navnet på den ønskede pakke.</span><span class="sxs-lookup"><span data-stu-id="6af6b-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="6af6b-313">Eksempler</span><span class="sxs-lookup"><span data-stu-id="6af6b-313">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="6af6b-314">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="6af6b-314">listtestsuitenames</span></span>
<span data-ttu-id="6af6b-315">Viser alle tilgængelige testpakker.</span><span class="sxs-lookup"><span data-stu-id="6af6b-315">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="6af6b-316">playback</span><span class="sxs-lookup"><span data-stu-id="6af6b-316">playback</span></span>
<span data-ttu-id="6af6b-317">Afspiller en testcase ved hjælp af en Excel-fil.</span><span class="sxs-lookup"><span data-stu-id="6af6b-317">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="6af6b-318">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="6af6b-318">Required parameters</span></span>
<span data-ttu-id="6af6b-319">**``excel_file``** En fuld sti til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-319">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="6af6b-320">Filen skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="6af6b-320">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="6af6b-321">Eksempler</span><span class="sxs-lookup"><span data-stu-id="6af6b-321">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="6af6b-322">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="6af6b-322">playbackbyid</span></span>
<span data-ttu-id="6af6b-323">Afspiller flere testcases på én gang.</span><span class="sxs-lookup"><span data-stu-id="6af6b-323">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="6af6b-324">Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases.</span><span class="sxs-lookup"><span data-stu-id="6af6b-324">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="6af6b-325">Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="6af6b-325">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="6af6b-326">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="6af6b-326">Required parameters</span></span>
<span data-ttu-id="6af6b-327">**``test_case_id1``** Id for eksisterende testcase.</span><span class="sxs-lookup"><span data-stu-id="6af6b-327">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="6af6b-328">**``test_case_id2``** Id for eksisterende testcase.</span><span class="sxs-lookup"><span data-stu-id="6af6b-328">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="6af6b-329">**``test_case_idN``** Id for eksisterende testcase.</span><span class="sxs-lookup"><span data-stu-id="6af6b-329">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="6af6b-330">Eksempler</span><span class="sxs-lookup"><span data-stu-id="6af6b-330">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="6af6b-331">playbackmany</span><span class="sxs-lookup"><span data-stu-id="6af6b-331">playbackmany</span></span>
<span data-ttu-id="6af6b-332">Afspiller mange testcases på én gang ved hjælp af Excel-filer.</span><span class="sxs-lookup"><span data-stu-id="6af6b-332">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="6af6b-333">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="6af6b-333">Required parameters</span></span>
<span data-ttu-id="6af6b-334">**``excel_file1``** Fuld sti til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-334">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="6af6b-335">Filen skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="6af6b-335">File must exist.</span></span>  
<span data-ttu-id="6af6b-336">**``excel_file2``** Fuld sti til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-336">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="6af6b-337">Filen skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="6af6b-337">File must exist.</span></span>  
<span data-ttu-id="6af6b-338">**``excel_fileN``** Fuld sti til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-338">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="6af6b-339">Filen skal eksistere.</span><span class="sxs-lookup"><span data-stu-id="6af6b-339">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="6af6b-340">Eksempler</span><span class="sxs-lookup"><span data-stu-id="6af6b-340">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="6af6b-341">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="6af6b-341">playbacksuite</span></span>
<span data-ttu-id="6af6b-342">Afspiller alle testcases fra den angivne testpakke.</span><span class="sxs-lookup"><span data-stu-id="6af6b-342">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="6af6b-343">Du kan bruge kommandoen ``listtestsuitenames`` til at få vist alle tilgængelige pakker.</span><span class="sxs-lookup"><span data-stu-id="6af6b-343">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="6af6b-344">Brug en vilkårlig værdi fra første kolonne som **suite_name**-parameter.</span><span class="sxs-lookup"><span data-stu-id="6af6b-344">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="6af6b-345">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="6af6b-345">Required parameters</span></span>
<span data-ttu-id="6af6b-346">**``suite_name``** Navnet på den ønskede pakke.</span><span class="sxs-lookup"><span data-stu-id="6af6b-346">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="6af6b-347">Eksempler</span><span class="sxs-lookup"><span data-stu-id="6af6b-347">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="6af6b-348">quit</span><span class="sxs-lookup"><span data-stu-id="6af6b-348">quit</span></span>
<span data-ttu-id="6af6b-349">Lukker programmet.</span><span class="sxs-lookup"><span data-stu-id="6af6b-349">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="6af6b-350">upload</span><span class="sxs-lookup"><span data-stu-id="6af6b-350">upload</span></span>
<span data-ttu-id="6af6b-351">Uploader alle de filer, der hører til den angivne testpakke eller de angivne testcases.</span><span class="sxs-lookup"><span data-stu-id="6af6b-351">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="6af6b-352">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="6af6b-352">Required parameters</span></span>
<span data-ttu-id="6af6b-353">**``suite_name``** Alle de filer, der hører til den angivne testpakke, bliver uploadet.</span><span class="sxs-lookup"><span data-stu-id="6af6b-353">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="6af6b-354">**``testcase_id``** Alle de filer, der hører til den eller de angivne testcases, bliver uploadet.</span><span class="sxs-lookup"><span data-stu-id="6af6b-354">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="6af6b-355">Eksempler</span><span class="sxs-lookup"><span data-stu-id="6af6b-355">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="6af6b-356">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="6af6b-356">uploadrecording</span></span>
<span data-ttu-id="6af6b-357">Uploader kun den optagne fil, der hører til de angivne testcases.</span><span class="sxs-lookup"><span data-stu-id="6af6b-357">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="6af6b-358">Påkrævede parametre</span><span class="sxs-lookup"><span data-stu-id="6af6b-358">Required parameters</span></span>
<span data-ttu-id="6af6b-359">**``testcase_id``** Den optagne fil, der hører til de angivne testcases, bliver uploadet.</span><span class="sxs-lookup"><span data-stu-id="6af6b-359">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="6af6b-360">Eksempler</span><span class="sxs-lookup"><span data-stu-id="6af6b-360">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="6af6b-361">usage</span><span class="sxs-lookup"><span data-stu-id="6af6b-361">usage</span></span>
<span data-ttu-id="6af6b-362">Viser to måder at aktivere dette program på: en, der bruger en fil med standardindstillinger, en anden, der angiver en fil med indstillinger.</span><span class="sxs-lookup"><span data-stu-id="6af6b-362">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="6af6b-363">Windows PowerShell-eksempler</span><span class="sxs-lookup"><span data-stu-id="6af6b-363">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="6af6b-364">Køre en testsag i en løkke</span><span class="sxs-lookup"><span data-stu-id="6af6b-364">Run a test case in a loop</span></span>

<span data-ttu-id="6af6b-365">Du har et testscript, der opretter en ny kunde.</span><span class="sxs-lookup"><span data-stu-id="6af6b-365">You have a test script that creates a new customer.</span></span> <span data-ttu-id="6af6b-366">Ved hjælp af scripting kan denne testsag køres i en løkke ved at gøre følgende data tilfældige, før hver enkelt gentagelse køres:</span><span class="sxs-lookup"><span data-stu-id="6af6b-366">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="6af6b-367">Debitor-id</span><span class="sxs-lookup"><span data-stu-id="6af6b-367">Customer ID</span></span>
- <span data-ttu-id="6af6b-368">Navn på debitor</span><span class="sxs-lookup"><span data-stu-id="6af6b-368">Customer name</span></span>
- <span data-ttu-id="6af6b-369">Debitors adresse</span><span class="sxs-lookup"><span data-stu-id="6af6b-369">Customer address</span></span>

<span data-ttu-id="6af6b-370">Kunde-id'et har formatet *ATCUS\<tal\>*, hvor \<tal\> er en værdi mellem **000000001** og **999999999**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-370">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="6af6b-371">I følgende eksempel bruges en parameter, **start**, til at definere det første tal, der bruges.</span><span class="sxs-lookup"><span data-stu-id="6af6b-371">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="6af6b-372">Er bruger en anden parameter, **nr**, til at det definere det antal kunder, der skal oprettes.</span><span class="sxs-lookup"><span data-stu-id="6af6b-372">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="6af6b-373">For hver gentagelse ændres parametrene i Excel-parameterfilen ved hjælp af en UpdateCustomer-funktion.</span><span class="sxs-lookup"><span data-stu-id="6af6b-373">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="6af6b-374">Derefter kaldes RSAT-kommandolinjen i en RunTestCase-funktion.</span><span class="sxs-lookup"><span data-stu-id="6af6b-374">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="6af6b-375">Åbn Microsoft Windows PowerShell Integrated Scripting Environment (ISE) i admininistratortilstand, og indsæt følgende kode i det vindue, der hedder **Uden titel.ps1**.</span><span class="sxs-lookup"><span data-stu-id="6af6b-375">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="6af6b-376">Køre et script, der afhænger af data i Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6af6b-376">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="6af6b-377">I følgende eksempel bruges et OData-kald (Open data Protocol) til at finde ordrestatussen for en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="6af6b-377">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="6af6b-378">Hvis status ikke er **faktureret**, kan du f.eks. kalde en RSAT-testsag, der bogfører fakturaen.</span><span class="sxs-lookup"><span data-stu-id="6af6b-378">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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
