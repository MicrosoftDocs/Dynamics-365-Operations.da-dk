---
title: Forbedringer i sporing af resultaterne fra genererede ER-rapporter og sammenligning af dem med basisværdier
description: Dette emne indeholder oplysninger om, hvordan funktionen for ER-grundlag er blevet forbedret Microsoft Dynamics 365 for Finance and Operations i version 10.0.3 (juni 2019).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: a260be0f8659106907b26bf69bee3b33b09d0c24
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181329"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="aa564-103">Forbedringer i sporing af resultaterne fra genererede ER-rapporter og sammenligning af dem med basisværdier</span><span class="sxs-lookup"><span data-stu-id="aa564-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="aa564-104">Dette emne beskriver det første sæt forbedringer, der er foretaget i grundlagsfunktionen i ER-strukturen (Electronic reporting).</span><span class="sxs-lookup"><span data-stu-id="aa564-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="aa564-105">Disse forbedringer er tilgængelige i Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (juni 2019) og nyere.</span><span class="sxs-lookup"><span data-stu-id="aa564-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="aa564-106">Automatiser indstillingen af regler for grundlag</span><span class="sxs-lookup"><span data-stu-id="aa564-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="aa564-107">Emnet [Spore genererede rapportresultater og sammenligne dem med basisværdier](er-trace-reports-compare-baseline.md) forklarer, hvordan du kan konfigurere ER-strukturen til at indsamle oplysninger om udførelser af ER-formater og evaluering af resultaterne af disse udførelser.</span><span class="sxs-lookup"><span data-stu-id="aa564-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="aa564-108">Eksemplet i dette emne beskriver de trin, der skal udføres.</span><span class="sxs-lookup"><span data-stu-id="aa564-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="aa564-109">Her er nogle af trinnene:</span><span class="sxs-lookup"><span data-stu-id="aa564-109">Here are some of the steps:</span></span>

- <span data-ttu-id="aa564-110">Kør et ER-format for at oprette en udgående fil, og gem filen lokalt.</span><span class="sxs-lookup"><span data-stu-id="aa564-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="aa564-111">Tilføj den lokalt gemte fil som en vedhæftet fil til det grundlag, der blev føjet til et ER-format.</span><span class="sxs-lookup"><span data-stu-id="aa564-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="aa564-112">Konfigurer grundlagsreglen for det tilføjede grundlag.</span><span class="sxs-lookup"><span data-stu-id="aa564-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="aa564-113">Denne konfiguration omfatter følgende trin:</span><span class="sxs-lookup"><span data-stu-id="aa564-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="aa564-114">Angiv et ER-formatelement, der bruges til at generere en udgående fil.</span><span class="sxs-lookup"><span data-stu-id="aa564-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="aa564-115">Vælg den vedhæftede fil, der refererer til den genererede udgående fil.</span><span class="sxs-lookup"><span data-stu-id="aa564-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="aa564-116">Disse trin skal udføres manuelt, selvom de nye ER-funktioner gør det muligt at automatisere dem.</span><span class="sxs-lookup"><span data-stu-id="aa564-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="aa564-117">Hvis du vil vide mere om denne funktion, skal du udføre følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="aa564-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="aa564-118">Eksempel: Automatiser indstillingen af regler for grundlag</span><span class="sxs-lookup"><span data-stu-id="aa564-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="aa564-119">Hvis du vil udføre trinnene i dette eksempel, skal du først fuldføre trinenne i eksemplet [Spore genererede rapportresultater og sammenligne dem med basisværdier](er-trace-reports-compare-baseline.md) til og med afsnittet "Tilføj et nyt grundlag for designet ER-format".</span><span class="sxs-lookup"><span data-stu-id="aa564-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="aa564-120">Gennemse tilføjet grundlag</span><span class="sxs-lookup"><span data-stu-id="aa564-120">Review added baseline</span></span>

1. <span data-ttu-id="aa564-121">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="aa564-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="aa564-122">Vælg **Grundlag**.</span><span class="sxs-lookup"><span data-stu-id="aa564-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="aa564-123">Knappen **Grundlag** i handlingsruden er kun tilgængelig, når brugerparameteren  **Kør i fejlfindingstilstand** er aktiveret for det aktuelle firma.</span><span class="sxs-lookup"><span data-stu-id="aa564-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="aa564-124">Grundlaget er blevet tilføjet for det valgte **Format til at lære ER-grundlag**, men grundlagsreglerne er endnu ikke blevet tilføjet for dette grundlag.</span><span class="sxs-lookup"><span data-stu-id="aa564-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="aa564-125">![Siden Grundlag for elektronisk rapporteringsformat](media/GER-BaselineSample-AddBaseline2.PNG "Skærmbillede af siden Grundlag for elektronisk rapporteringsformat")</span><span class="sxs-lookup"><span data-stu-id="aa564-125">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="aa564-126">Opret en ny grundlagsregel</span><span class="sxs-lookup"><span data-stu-id="aa564-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="aa564-127">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="aa564-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="aa564-128">Udvid **Model til at lære ER-grundlag** i træet.</span><span class="sxs-lookup"><span data-stu-id="aa564-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="aa564-129">Vælg **Model til at lære ER-brundlag\\Format til at lære ER-grundlag** i træet.</span><span class="sxs-lookup"><span data-stu-id="aa564-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="aa564-130">Gå til oversigtspanelet **Versioner**, og vælg **Kør**.</span><span class="sxs-lookup"><span data-stu-id="aa564-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="aa564-131">Gå til feltet **Angiv id**, og angiv **1**.</span><span class="sxs-lookup"><span data-stu-id="aa564-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="aa564-132">Angiv indstillingen **Opret grundlagsfiler** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="aa564-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="aa564-133">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa564-133">Select **OK**.</span></span>

    <span data-ttu-id="aa564-134">![Dialogboksen Parametre for elektronisk rapportering](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Skærmbillede af dialogboksen Parametre for elektronisk rapportering")</span><span class="sxs-lookup"><span data-stu-id="aa564-134">![Electronic report parameters dialog box](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Screenshot of the Electronic report parameters dialog box")</span></span>

8. <span data-ttu-id="aa564-135">Vælg **Grundlag**.</span><span class="sxs-lookup"><span data-stu-id="aa564-135">Select **Baselines**.</span></span>

    <span data-ttu-id="aa564-136">![Siden Grundlag for elektronisk rapporteringsformat](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Skærmbillede af siden Grundlag for elektronisk rapporteringsformat")</span><span class="sxs-lookup"><span data-stu-id="aa564-136">![Electronic reporting format baselines page](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="aa564-137">Den genererede udgående fil er automatisk blevet knyttet til grundlaget i det udførte ER-format.</span><span class="sxs-lookup"><span data-stu-id="aa564-137">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="aa564-138">Grundlagsreglen er automatisk blevet føjet til dette grundlag og indeholder også referencen til den vedhæftede fil.</span><span class="sxs-lookup"><span data-stu-id="aa564-138">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="aa564-139">Angiv **Grundlag1** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="aa564-139">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="aa564-140">Gå til feltet **Filnavnsmaske**, og angiv **.xml**.</span><span class="sxs-lookup"><span data-stu-id="aa564-140">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="aa564-141">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="aa564-141">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="aa564-142">Køre formatet</span><span class="sxs-lookup"><span data-stu-id="aa564-142">Run the format</span></span>

<span data-ttu-id="aa564-143">Du er nu klar til at fuldføre de resterende trin i emnet [Spore genererede rapportresultater og sammenligne dem med basisværdier](er-trace-reports-compare-baseline.md) med start fra afsnittet "Kør det designede ER-format, og gennemse logfilen for at analysere resultaterne".</span><span class="sxs-lookup"><span data-stu-id="aa564-143">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="aa564-144">Når du sletter den automatisk tilføjede grundlagsregel på oversigtspanelet **Grundlag**, slettes den refererede vedhæftede fil ikke automatisk.</span><span class="sxs-lookup"><span data-stu-id="aa564-144">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="aa564-145">Konfigurer grundlinjen, så den hele tiden ignorerer ændringer i dele af ER-outputtet</span><span class="sxs-lookup"><span data-stu-id="aa564-145">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="aa564-146">Når et ER-format er designet til at indeholde oplysninger, der ændres, når formatet køres, skal formatet være obligatorisk, før du kan bruge funktionen til grundlag til at sammenligne de genererede resultater med basisværdier.</span><span class="sxs-lookup"><span data-stu-id="aa564-146">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="aa564-147">Oplysningerne kan f. eks. være behandlingsdatoen og -tidspunktet eller det entydige id for et genereret dokument i forskellige formater (globally unique identifier \[GUID\] osv).</span><span class="sxs-lookup"><span data-stu-id="aa564-147">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="aa564-148">De nye ER-funktioner giver dig mulighed for at konfigurere grundlagsreglen, så den ignorerer de elementer i et ER-format, der kan ændres, når formatet køres, med det formål at sammenligne basisværdier med resultaterne af formatets udførelse.</span><span class="sxs-lookup"><span data-stu-id="aa564-148">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="aa564-149">Hvis du vil vide mere om denne funktion, skal du udføre følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="aa564-149">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="aa564-150">Eksempel: Konfigurer grundlaget, så det hele tiden ignorerer ændringer i dele af ER-outputtet</span><span class="sxs-lookup"><span data-stu-id="aa564-150">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="aa564-151">Hvis du vil udføre trinnene i dette eksempel, skal du først fuldføre trinnene i eksemplet [Spore genererede rapportresultater og sammenligne dem med basisværdier](er-trace-reports-compare-baseline.md).</span><span class="sxs-lookup"><span data-stu-id="aa564-151">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="aa564-152">Rediger et konfigureret ER-format</span><span class="sxs-lookup"><span data-stu-id="aa564-152">Modify a configured ER format</span></span>

1. <span data-ttu-id="aa564-153">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="aa564-153">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="aa564-154">Udvid **Model til at lære ER-grundlag** i træet.</span><span class="sxs-lookup"><span data-stu-id="aa564-154">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="aa564-155">Vælg **Model til at lære ER-brundlag\\Format til at lære ER-grundlag** i træet.</span><span class="sxs-lookup"><span data-stu-id="aa564-155">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="aa564-156">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="aa564-156">Select **Designer**.</span></span>
5. <span data-ttu-id="aa564-157">Vælg **Output\\Dokument** i træet.</span><span class="sxs-lookup"><span data-stu-id="aa564-157">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="aa564-158">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="aa564-158">Select **Add**.</span></span>
7. <span data-ttu-id="aa564-159">Vælg **XML\\Attribut** i træet i rulledialogboksen.</span><span class="sxs-lookup"><span data-stu-id="aa564-159">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="aa564-160">Angiv **ProcessingDateTime** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="aa564-160">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="aa564-161">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa564-161">Select **OK**.</span></span>
10. <span data-ttu-id="aa564-162">Gå til fanen **Tilknytning**, og vælg **Output\\Dokument\\ProcessingDateTime** i træet.</span><span class="sxs-lookup"><span data-stu-id="aa564-162">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="aa564-163">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="aa564-163">Select **Edit formula**.</span></span>
12. <span data-ttu-id="aa564-164">Gå til feltet **Formel**, og angiv følgende udtryk: **DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="aa564-164">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="aa564-165">Vælg **Gem**, og vælg derefter **Test**.</span><span class="sxs-lookup"><span data-stu-id="aa564-165">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="aa564-166">Vælg **Test** igen for at teste det konfigurerede udtryk igen.</span><span class="sxs-lookup"><span data-stu-id="aa564-166">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="aa564-167">![Siden Formeldesigner](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Skærmbillede af siden Formeldesigner")</span><span class="sxs-lookup"><span data-stu-id="aa564-167">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="aa564-168">Under **Testresultat** kan du se, at det konfigurerede udtryk returnerer en anden værdi for dato/klokkeslæt, hver gang det kaldes.</span><span class="sxs-lookup"><span data-stu-id="aa564-168">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="aa564-169">Luk siden **Formeldesigner**, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="aa564-169">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="aa564-170">![Siden Formatdesigner](media/GER-BaselineSample-FormatMappingDesign2.PNG "Skærmbillede af siden Formatdesigner")</span><span class="sxs-lookup"><span data-stu-id="aa564-170">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="aa564-171">Luk siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="aa564-171">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="aa564-172">Fjerne en eksisterende grundlagsregel</span><span class="sxs-lookup"><span data-stu-id="aa564-172">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="aa564-173">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="aa564-173">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="aa564-174">Vælg **Grundlag**.</span><span class="sxs-lookup"><span data-stu-id="aa564-174">Select **Baselines**.</span></span>
3. <span data-ttu-id="aa564-175">På listen over grundlag skal du vælge det grundlag, der er konfigureret til formatet **Format til at lære ER-grundlag**.</span><span class="sxs-lookup"><span data-stu-id="aa564-175">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="aa564-176">I oversigtspanelet **Grundlag** skal du vælge **Slet** for at fjerne den grundlagsregel, du konfigurerede tidligere.</span><span class="sxs-lookup"><span data-stu-id="aa564-176">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="aa564-177">![Siden Grundlag for elektronisk rapporteringsformat](media/GER-BaselineSample-AddBaseline3.PNG "Skærmbillede af siden Grundlag for elektronisk rapporteringsformat")</span><span class="sxs-lookup"><span data-stu-id="aa564-177">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="aa564-178">Definer erstatninger for bindinger, der er designet ER-format</span><span class="sxs-lookup"><span data-stu-id="aa564-178">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="aa564-179">Gå til siden **Konfigurationer**, og vælg **Vælg komponenter** i oversigtspanelet **Erstatninger**.</span><span class="sxs-lookup"><span data-stu-id="aa564-179">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="aa564-180">I træet til formatkomponenter skal du udvide **Output**, udvide **Output\\Dokument** og derefter markere afkrydsningsfeltet for **Output\\Dokument\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="aa564-180">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>

    <span data-ttu-id="aa564-181">![Dialogboksen Vælg komponenter](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Skærmbillede af dialogboksen Vælg Komponenter")</span><span class="sxs-lookup"><span data-stu-id="aa564-181">![Select Components dialog box](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Screenshot of the Select Components dialog box")</span></span>

3. <span data-ttu-id="aa564-182">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa564-182">Select **OK**.</span></span>

<span data-ttu-id="aa564-183">![Siden Grundlag for elektronisk rapporteringsformat](media/GER-BaselineSample-AddBaseline4.PNG "Skærmbillede af siden Grundlag for elektronisk rapporteringsformat")</span><span class="sxs-lookup"><span data-stu-id="aa564-183">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="aa564-184">Den valgte ER-formatkomponent er føjet til listen over komponenter i oversigtspanelet **Erstatninger**.</span><span class="sxs-lookup"><span data-stu-id="aa564-184">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="aa564-185">Når basis-ER-formatet køres i fejlfindingstilstand, vil formatets binding for hver komponent blive erstattet af den binding, der vises i kolonnen **Binding**.</span><span class="sxs-lookup"><span data-stu-id="aa564-185">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="aa564-186">Hvis du vil ændre standardbindingen for en komponent, der vises i oversigtspanelet **Erstatninger**, skal du vælge **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="aa564-186">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="aa564-187">Opret en ny grundlagsregel</span><span class="sxs-lookup"><span data-stu-id="aa564-187">Make a new baseline rule</span></span>

<span data-ttu-id="aa564-188">Følg trinnene i afsnittet "Eksempel: Automatiser indstillingen af regler for grundlag" tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="aa564-188">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="aa564-189">En besked advarer dig om, at den udgående fil er blevet oprettet ved hjælp af grundlagsindstillinger, og at der er foretaget en tvungen erstatning af formatbindingerne.</span><span class="sxs-lookup"><span data-stu-id="aa564-189">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="aa564-190">![Besked på siden Konfigurationer](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Skærmbillede af besked på siden Konfigurationer")</span><span class="sxs-lookup"><span data-stu-id="aa564-190">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="aa564-191">Undertryk advarsler om erstatning af formatbindinger</span><span class="sxs-lookup"><span data-stu-id="aa564-191">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="aa564-192">Hvis du angiver specifikke ER-parametre, kan du undertrykke beskeder, der advarer om erstatning af formatbindinger.</span><span class="sxs-lookup"><span data-stu-id="aa564-192">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="aa564-193">Denne undertrykkelse kan være nyttig, når formatbindinger erstattes i en automatisk tilstand ved hjælp af Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="aa564-193">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="aa564-194">I dette tilfælde kan advarslen betragtes som en fejl i den test, der kører.</span><span class="sxs-lookup"><span data-stu-id="aa564-194">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="aa564-195">Gå til siden **Konfigurationer**, gå til handlingsruden, og vælg **Brugerparametre** på fanen **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="aa564-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="aa564-196">Angiv indstillingen **Undertryk grundlagsadvarsler** til **Ja**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa564-196">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

<span data-ttu-id="aa564-197">![Dialogboksen Brugerparametre](media/GER-BaselineSample-ERUserParameters1.png "Skærmbillede af dialogboksen Brugerparametre")</span><span class="sxs-lookup"><span data-stu-id="aa564-197">![User parameters dialog box](media/GER-BaselineSample-ERUserParameters1.png "Screenshot of the User parameters dialog box")</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="aa564-198">Gennemse den genererede grundlagsfil.</span><span class="sxs-lookup"><span data-stu-id="aa564-198">Review the generated baseline file</span></span>

1. <span data-ttu-id="aa564-199">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="aa564-199">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="aa564-200">Vælg **Grundlag**.</span><span class="sxs-lookup"><span data-stu-id="aa564-200">Select **Baselines**.</span></span>
3. <span data-ttu-id="aa564-201">Vælg **Vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="aa564-201">Select **Attachments**.</span></span>

    <span data-ttu-id="aa564-202">![Siden Vedhæftede filer](media/GER-BaselineSample-AttachedBaselineFile.PNG "Skærmbillede af siden Vedhæftede filer")</span><span class="sxs-lookup"><span data-stu-id="aa564-202">![Attachments page](media/GER-BaselineSample-AttachedBaselineFile.PNG "Screenshot of the Attachments page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="aa564-203">Den genererede fil indeholder behandlingsdato- og klokkeslættetsteksten (**"#"**) fra den binding, der blev konfigureret i den tilføjede grundlagsregel, ikke fra formatets binding.</span><span class="sxs-lookup"><span data-stu-id="aa564-203">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>

4. <span data-ttu-id="aa564-204">Luk siden **Vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="aa564-204">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="aa564-205">Kør det designede ER-format, og gennemse logfilen for at analysere resultaterne</span><span class="sxs-lookup"><span data-stu-id="aa564-205">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="aa564-206">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="aa564-206">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="aa564-207">Udvid **Model til at lære ER-grundlag** i træet.</span><span class="sxs-lookup"><span data-stu-id="aa564-207">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="aa564-208">Vælg **Model til at lære ER-brundlag\\Format til at lære ER-grundlag** i træet.</span><span class="sxs-lookup"><span data-stu-id="aa564-208">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="aa564-209">Gå til oversigtspanelet **Versioner**, og vælg **Kør**.</span><span class="sxs-lookup"><span data-stu-id="aa564-209">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="aa564-210">Gå til feltet **Angiv id**, og skriv **1**.</span><span class="sxs-lookup"><span data-stu-id="aa564-210">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="aa564-211">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa564-211">Select **OK**.</span></span>
7. <span data-ttu-id="aa564-212">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Fejlfindingslogs for konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="aa564-212">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="aa564-213">Udførelseslogfilen indeholder oplysninger om resultaterne af sammenligningen af den genererede fil med det konfigurerede grundlag.</span><span class="sxs-lookup"><span data-stu-id="aa564-213">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="aa564-214">Logfilen angiver, at den genererede fil og grundlaet er ens, selvom det udførte format indeholder bindingen til at angive en konstant ændring af dato- og klokkeslætsværdien i den udgående fil.</span><span class="sxs-lookup"><span data-stu-id="aa564-214">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="aa564-215">Selvom den udgående fil er genereret ved hjælp af de grundlagsindstillinger, der gennemtvinger erstatningen af formatets bindinger, modtager du ingen advarsler om erstatningen.</span><span class="sxs-lookup"><span data-stu-id="aa564-215">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="aa564-216">Udskift indstillinger for grundlag mellem miljøer</span><span class="sxs-lookup"><span data-stu-id="aa564-216">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="aa564-217">Eksport indstillinger for grundlag</span><span class="sxs-lookup"><span data-stu-id="aa564-217">Export baseline settings</span></span>

<span data-ttu-id="aa564-218">Med de nye ER-funktioner kan du eksportere indstillinger for grundlag for det valgte ER-format fra det aktuelle miljø og gemme dem som XML-filer.</span><span class="sxs-lookup"><span data-stu-id="aa564-218">The new ER capabilities let you export baseline settings for the selected ER format from the current environment and store them as XML files.</span></span> 

<span data-ttu-id="aa564-219">Hvis du vil eksportere indstillinger for grundlag, skal du på siden **Grundlag for elektronisk rapporteringsformat** vælge **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="aa564-219">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="aa564-220">Importer oprindelige indstillinger</span><span class="sxs-lookup"><span data-stu-id="aa564-220">Import baseline settings</span></span>

<span data-ttu-id="aa564-221">Eksporterede indstillinger for grundlag kan importeres til et andet miljø.</span><span class="sxs-lookup"><span data-stu-id="aa564-221">Exported baseline settings can be imported into a different environment.</span></span> <span data-ttu-id="aa564-222">Miljøet skal først importeres som et ER-format.</span><span class="sxs-lookup"><span data-stu-id="aa564-222">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="aa564-223">Du kan derefter importere grundlagsindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="aa564-223">You can then import the baseline settings.</span></span>

<span data-ttu-id="aa564-224">Hvis du vil importere grundlagsindstillinger fra en XML-fil, der er gemt lokalt, skal du på siden **Grundlag for elektronisk rapporteringsformat** vælge **Importer** og derefter **Gennemse** for at vælge XML-filen.</span><span class="sxs-lookup"><span data-stu-id="aa564-224">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="aa564-225">![Dialogboksen Import indstillinger for grundlag](media/GER-BaselineSample-ImportBaseline1.PNG "Skærmbillede af dialogboksen Import indstillinger for grundlag")</span><span class="sxs-lookup"><span data-stu-id="aa564-225">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="aa564-226">Hvis du vil importere grundlagsindstillinger fra en XML-fil, der er gemt på Microsoft SharePoint Server, baseret på de aktuelle indstillinger for dokumentstyring og den valgte dokumenttype, skal du vælge **Importer fra kilde** på siden **Grundlag for elektronisk rapporteringsformat**.</span><span class="sxs-lookup"><span data-stu-id="aa564-226">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="aa564-227">Vælg derefter dokumenttypen, og XML-filen.</span><span class="sxs-lookup"><span data-stu-id="aa564-227">Then select the document type and the XML file.</span></span> <span data-ttu-id="aa564-228">Den krævede dokumenttype for at få adgang til SharePoint-mappen skal være konfigureret i forvejen.</span><span class="sxs-lookup"><span data-stu-id="aa564-228">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="aa564-229">![Dialogboksen Importer fra kilde](media/GER-BaselineSample-ImportBaseline2.PNG "Skærmbillede af dialogboksen Importer fra kilde")</span><span class="sxs-lookup"><span data-stu-id="aa564-229">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="aa564-230">Du kan bruge Arbejdsrutineoptager til at registrere de trin, der skal bruges til at vælge den ønskede dokument type og filnavnet i dialogboksen **Importer fra kilde**.</span><span class="sxs-lookup"><span data-stu-id="aa564-230">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="aa564-231">På denne måde kan du beholde de nødvendige indstillinger for grundlag på SharePoint Server og derefter importere dem automatisk ved at afspille en opgaveregistrering, når du kører automatiske test ved hjælp af Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="aa564-231">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa564-232">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="aa564-232">Additional resources</span></span>

- [<span data-ttu-id="aa564-233">Spore genererede rapportresultater og sammenligne dem med basisværdier</span><span class="sxs-lookup"><span data-stu-id="aa564-233">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="aa564-234">Arbejdsrutineoptager</span><span class="sxs-lookup"><span data-stu-id="aa564-234">Task recorder</span></span>](../user-interface/task-recorder.md)
