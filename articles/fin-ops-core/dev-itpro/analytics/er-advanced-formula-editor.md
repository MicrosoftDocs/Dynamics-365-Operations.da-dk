---
title: Avanceret formeleditor til elektronisk rapportering
description: Dette emne beskriver, hvordan den avancerede formeleditor kan bruges til at konfigurere udtryk i modeltilknytning til elektronisk rapportering (ER) og formatkomponenter.
author: NickSelin
manager: AnnBe
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: d183f77da1dda0c4f04e4e48ab3db0133f494a55
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015153"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="7687e-103">Avanceret formeleditor til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="7687e-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="7687e-104">Udover den [elektroniske rapporterings](general-electronic-reporting.md) [formeleditor](general-electronic-reporting-formula-designer.md) kan du bruge den avancerede formeleditor til elektronisk rapportering til at forbedre oplevelsen i forbindelse med konfiguration af elektroniske rapporteringsudtryk (ER).</span><span class="sxs-lookup"><span data-stu-id="7687e-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="7687e-105">Den avancerede editor er browserbaseret og er styret af [Monaco-editoren](https://microsoft.github.io/monaco-editor).</span><span class="sxs-lookup"><span data-stu-id="7687e-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="7687e-106">De mest almindeligt anvendte avancerede funktioner i editoren er beskrevet i dette emne:</span><span class="sxs-lookup"><span data-stu-id="7687e-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="7687e-107">Autoformatering af kode</span><span class="sxs-lookup"><span data-stu-id="7687e-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="7687e-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="7687e-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="7687e-109">Fuldførelse af kode</span><span class="sxs-lookup"><span data-stu-id="7687e-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="7687e-110">Kodenavigation</span><span class="sxs-lookup"><span data-stu-id="7687e-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="7687e-111">Kodestrukturering</span><span class="sxs-lookup"><span data-stu-id="7687e-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="7687e-112">Søg og erstat</span><span class="sxs-lookup"><span data-stu-id="7687e-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="7687e-113">Indsætning af data</span><span class="sxs-lookup"><span data-stu-id="7687e-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="7687e-114">Syntaksfarvelægning</span><span class="sxs-lookup"><span data-stu-id="7687e-114">Syntax colorization</span></span>](#SyntaxColorization)

## <span data-ttu-id="7687e-115"><a name="ActivateAdvEditor">Aktivere den avancerede formeleditor</a></span><span class="sxs-lookup"><span data-stu-id="7687e-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="7687e-116">Gennemfør følgende trin for at begynde at bruge den avancerede formeleditor i din forekomst af Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="7687e-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="7687e-117">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="7687e-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="7687e-118">På siden **Konfigurationer** i handlingsruden under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** skal du vælge **Brugerparametre**.</span><span class="sxs-lookup"><span data-stu-id="7687e-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="7687e-119">I dialogboksen **Brugerparametre** i sektionen **Kørselssporing** skal du angive parameteren **Aktiver avanceret formeleditor** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7687e-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="7687e-120">[![Siden ER-konfigurationer](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="7687e-120">[![ER configurations page](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="7687e-121">Vær opmærksom på, at denne parameter er brugerspecifik og firmaspecifik.</span><span class="sxs-lookup"><span data-stu-id="7687e-121">Be aware that this parameter is user specific and company specific.</span></span>

## <span data-ttu-id="7687e-122"><a name="Autoformatting">Autoformatering af kode</a></span><span class="sxs-lookup"><span data-stu-id="7687e-122"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="7687e-123">Når du skriver et komplekst udtryk, der består af flere koderækker, sker der automatisk indrykning af en ny linje baseret på indrykningen af den foregående række.</span><span class="sxs-lookup"><span data-stu-id="7687e-123">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="7687e-124">Du kan markere linjer og ændre deres indrykning ved at trykke på **tabulator** eller **Skift+tabulator**.</span><span class="sxs-lookup"><span data-stu-id="7687e-124">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="7687e-125">[![ER-formeleditor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="7687e-125">[![ER formula editor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="7687e-126">Automatisk formatering giver dig mulighed for at bevare hele udtrykket formateret, så yderligere vedligeholdelse bliver nemmere, og at forenkle forståelsen af den konfigurerede logik.</span><span class="sxs-lookup"><span data-stu-id="7687e-126">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <span data-ttu-id="7687e-127"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="7687e-127"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="7687e-128">Editoren indsætter ord, så du kan skrive udtryk hurtigere og undgå slåfejl.</span><span class="sxs-lookup"><span data-stu-id="7687e-128">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="7687e-129">Når du begynder at indsætte ny tekst, viser editoren automatisk en liste over funktioner, der understøttes i ER-funktioner, som indeholder de tegn, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="7687e-129">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="7687e-130">Du kan også udløse IntelliSense på et hvilket som helst sted i et konfigureret udtryk ved at trykke på **CTRL+mellemrum**.</span><span class="sxs-lookup"><span data-stu-id="7687e-130">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="7687e-131">[![ER-formeleditor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="7687e-131">[![ER formula editor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <span data-ttu-id="7687e-132"><a name="CodeCompletion">Fuldførelse af kode</a></span><span class="sxs-lookup"><span data-stu-id="7687e-132"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="7687e-133">Editoren leverer automatisk fuldførelse af kode ved at:</span><span class="sxs-lookup"><span data-stu-id="7687e-133">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="7687e-134">Indsætte en kantet højreparentes, når du angiver en kantet venstreparentes, og holde markøren inden for de kantede parenteser.</span><span class="sxs-lookup"><span data-stu-id="7687e-134">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="7687e-135">Indsætte det andet anførselstegn, når det første er indsat, og holde markøren inden for anførselstegnene.</span><span class="sxs-lookup"><span data-stu-id="7687e-135">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="7687e-136">Indsætte det andet dobbelte anførselstegn, når det første er indsat, og holde markøren inden for anførselstegnene.</span><span class="sxs-lookup"><span data-stu-id="7687e-136">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="7687e-137">[![ER-formeleditor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="7687e-137">[![ER formula editor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="7687e-138">Når du peger på den indsatte kantede parentes, fremhæves den anden parentes i parret automatisk, så det viser den konstruktion, som de understøtter.</span><span class="sxs-lookup"><span data-stu-id="7687e-138">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <span data-ttu-id="7687e-139"><a name="CodeNavigation">Kodenavigation</a></span><span class="sxs-lookup"><span data-stu-id="7687e-139"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="7687e-140">Du kan finde påkrævede symboler eller linjer i udtrykket ved at skrive kommandoen **Gå til** ved hjælp af kommandopaletten eller genvejsmenuen.</span><span class="sxs-lookup"><span data-stu-id="7687e-140">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="7687e-141">Hvis du f.eks. vil hoppe til linje **8**, skal du benytte følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="7687e-141">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="7687e-142">Tryk på **Ctrl+G**, angive værdien **8** og derefter trykke på **Enter**.</span><span class="sxs-lookup"><span data-stu-id="7687e-142">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="7687e-143">-eller-</span><span class="sxs-lookup"><span data-stu-id="7687e-143">-or-</span></span>

- <span data-ttu-id="7687e-144">Tryk på **F1**, skriv **G**, vælg **Gå til linje**, skriv værdien **8**, og tryk på **Enter**.</span><span class="sxs-lookup"><span data-stu-id="7687e-144">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="7687e-145">[![ER-formeleditor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="7687e-145">[![ER formula editor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <span data-ttu-id="7687e-146"><a name="CodeStructuring">Kodestrukturering</a></span><span class="sxs-lookup"><span data-stu-id="7687e-146"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="7687e-147">Koden for nogle funktioner, f.eks. [IF](er-functions-logical-if.md) eller [CASE](er-functions-logical-case.md), struktureres automatisk.</span><span class="sxs-lookup"><span data-stu-id="7687e-147">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="7687e-148">Du kan udvide og skjule et vilkårligt foldningsområde eller alle foldningsområder i denne kode for at reducere den redigerbare del af et udtryk for kun at fokusere på den del af koden, der kræver din opmærksomhed.</span><span class="sxs-lookup"><span data-stu-id="7687e-148">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="7687e-149">Kommandoerne til at folde/folde ud kan bruges til dette.</span><span class="sxs-lookup"><span data-stu-id="7687e-149">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="7687e-150">Hvis du f.eks. vil folde alle områder, skal du benytte følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="7687e-150">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="7687e-151">Tryk på **Ctrl+K**</span><span class="sxs-lookup"><span data-stu-id="7687e-151">Press **Ctrl+K**</span></span>

  <span data-ttu-id="7687e-152">-eller-</span><span class="sxs-lookup"><span data-stu-id="7687e-152">-or-</span></span>

- <span data-ttu-id="7687e-153">Tryk på **F1**, tryk på **FO**, vælg **Fold alle**, og tryk derefter på **Enter**</span><span class="sxs-lookup"><span data-stu-id="7687e-153">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="7687e-154">Hvis du vil folde alle områder ud, skal du benytte følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="7687e-154">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="7687e-155">Tryk på **Ctrl+J**</span><span class="sxs-lookup"><span data-stu-id="7687e-155">Press **Ctrl+J**</span></span>

  <span data-ttu-id="7687e-156">-eller-</span><span class="sxs-lookup"><span data-stu-id="7687e-156">-or-</span></span>
  
- <span data-ttu-id="7687e-157">Tryk på **F1**, skriv **UD**, vælg **Fold alle ud**, og tryk derefter på **Enter**</span><span class="sxs-lookup"><span data-stu-id="7687e-157">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="7687e-158">[![ER-formeleditor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="7687e-158">[![ER formula editor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <span data-ttu-id="7687e-159"><a name="FindAndReplace">Søg og erstat</a></span><span class="sxs-lookup"><span data-stu-id="7687e-159"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="7687e-160">Hvis du vil søge efter forekomster af bestemt tekst, skal du markere teksten i udtrykket og gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="7687e-160">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="7687e-161">Tryk på **Ctrl+F**, og tryk derefter på **F3** for at søge efter den næste forekomst af den markerede tekst, eller tryk på **Skift+F3** for at finde den forrige forekomst.</span><span class="sxs-lookup"><span data-stu-id="7687e-161">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="7687e-162">-eller-</span><span class="sxs-lookup"><span data-stu-id="7687e-162">-or-</span></span>
  
- <span data-ttu-id="7687e-163">Tryk på **F1**, skriv **F**, og vælg derefter den påkrævede indstilling for at finde den markerede tekst.</span><span class="sxs-lookup"><span data-stu-id="7687e-163">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="7687e-164">Hvis du vil erstatte forekomster af en bestemt tekst, skal du markere teksten i udtrykket og gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="7687e-164">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="7687e-165">Tryk på **Ctrl+H**.</span><span class="sxs-lookup"><span data-stu-id="7687e-165">Press **Ctrl+H**.</span></span> <span data-ttu-id="7687e-166">Skriv den alternative tekst, og vælg erstatningsindstillingen for enten at erstatte den markerede tekst eller alle forekomster af denne tekst i det aktuelle udtryk.</span><span class="sxs-lookup"><span data-stu-id="7687e-166">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="7687e-167">-eller-</span><span class="sxs-lookup"><span data-stu-id="7687e-167">-or-</span></span>
  
- <span data-ttu-id="7687e-168">Tryk på **F1**, skriv **R**, og vælg derefter den påkrævede indstilling for at erstatte den markerede tekst.</span><span class="sxs-lookup"><span data-stu-id="7687e-168">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="7687e-169">Skriv den alternative tekst, og vælg erstatningsindstillingen for enten at erstatte den markerede tekst eller alle forekomster af denne tekst i det aktuelle udtryk.</span><span class="sxs-lookup"><span data-stu-id="7687e-169">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="7687e-170">Hvis du vil ændre alle forekomster af en bestemt tekst, skal du markere teksten i udtrykket og gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="7687e-170">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="7687e-171">Tryk på **Ctrl+F2**, og angiv derefter den alternative tekst.</span><span class="sxs-lookup"><span data-stu-id="7687e-171">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="7687e-172">-eller-</span><span class="sxs-lookup"><span data-stu-id="7687e-172">-or-</span></span>
  
- <span data-ttu-id="7687e-173">Tryk på **F1**, skriv **C**, og vælg derefter den påkrævede indstilling for at ændre den markerede tekst.</span><span class="sxs-lookup"><span data-stu-id="7687e-173">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="7687e-174">Skriv den alternative tekst.</span><span class="sxs-lookup"><span data-stu-id="7687e-174">Enter the alternative text.</span></span>

<span data-ttu-id="7687e-175">[![ER-formeleditor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="7687e-175">[![ER formula editor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <span data-ttu-id="7687e-176"><a name="DataPasting">Datakilder og indsætning af funktioner</a></span><span class="sxs-lookup"><span data-stu-id="7687e-176"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="7687e-177">Du kan vælge **Tilføj datakilde**, som indsætter en datakilde, der aktuelt er valgt i **Datakilde** i det venstre panel, i udtrykket.</span><span class="sxs-lookup"><span data-stu-id="7687e-177">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="7687e-178">På samme måde kan du vælge **Tilføj funktion**, som indsætter en funktion, der aktuelt er valgt i **Funktioner** i det højre panel, i udtrykket.</span><span class="sxs-lookup"><span data-stu-id="7687e-178">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="7687e-179">Hvis du bruger ER-formeleditoren, vil en valgt funktion eller en valgt datakilde altid blive indsat i slutningen af det konfigurerede udtryk.</span><span class="sxs-lookup"><span data-stu-id="7687e-179">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="7687e-180">Når du bruger den avancerede ER-formeleditor, kan en valgt funktion eller en valgt datakilde blive indsat i en vilkårlig del af det konfigurerede udtryk.</span><span class="sxs-lookup"><span data-stu-id="7687e-180">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="7687e-181">Du skal bruge markøren til at angive, hvor du vil indsætte dataene.</span><span class="sxs-lookup"><span data-stu-id="7687e-181">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="7687e-182">formel[![ER-formeleditor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="7687e-182">[![ER formula editor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <span data-ttu-id="7687e-183"><a name="SyntaxColorization">Syntaksfarvelægning</a></span><span class="sxs-lookup"><span data-stu-id="7687e-183"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="7687e-184">I øjeblikket bruges forskellige farver til at fremhæve følgende dele af udtryk:</span><span class="sxs-lookup"><span data-stu-id="7687e-184">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="7687e-185">Teksten i dobbelte parenteser, der kan repræsentere et etiket-id for en tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="7687e-185">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="7687e-186">[![ER-formeleditor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="7687e-186">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7687e-187">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7687e-187">Additional resources</span></span>

- [<span data-ttu-id="7687e-188">Oversigt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="7687e-188">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="7687e-189">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="7687e-189">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="7687e-190">Monaco-editor</span><span class="sxs-lookup"><span data-stu-id="7687e-190">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)
