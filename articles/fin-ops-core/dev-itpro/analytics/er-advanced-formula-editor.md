---
title: Avanceret formeleditor til elektronisk rapportering
description: Dette emne beskriver, hvordan den avancerede formeleditor kan bruges til at konfigurere udtryk i modeltilknytning til elektronisk rapportering (ER) og formatkomponenter.
author: NickSelin
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f7f80928e1d3f5d4892f72d4bd2fd09b70a26c1f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270701"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="edce0-103">Avanceret formeleditor til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="edce0-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="edce0-104">Udover den [elektroniske rapporterings](general-electronic-reporting.md) [formeleditor](general-electronic-reporting-formula-designer.md) kan du bruge den avancerede formeleditor til elektronisk rapportering til at forbedre oplevelsen i forbindelse med konfiguration af elektroniske rapporteringsudtryk (ER).</span><span class="sxs-lookup"><span data-stu-id="edce0-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="edce0-105">Den avancerede editor er browserbaseret og er styret af [Monaco-editoren](https://microsoft.github.io/monaco-editor).</span><span class="sxs-lookup"><span data-stu-id="edce0-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="edce0-106">De mest almindeligt anvendte avancerede funktioner i editoren er beskrevet i dette emne:</span><span class="sxs-lookup"><span data-stu-id="edce0-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="edce0-107">Autoformatering af kode</span><span class="sxs-lookup"><span data-stu-id="edce0-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="edce0-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="edce0-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="edce0-109">Fuldførelse af kode</span><span class="sxs-lookup"><span data-stu-id="edce0-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="edce0-110">Kodenavigation</span><span class="sxs-lookup"><span data-stu-id="edce0-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="edce0-111">Kodestrukturering</span><span class="sxs-lookup"><span data-stu-id="edce0-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="edce0-112">Søg og erstat</span><span class="sxs-lookup"><span data-stu-id="edce0-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="edce0-113">Indsætning af data</span><span class="sxs-lookup"><span data-stu-id="edce0-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="edce0-114">Syntaksfarvelægning</span><span class="sxs-lookup"><span data-stu-id="edce0-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="edce0-115"><a name="ActivateAdvEditor">Aktivere den avancerede formeleditor</a></span><span class="sxs-lookup"><span data-stu-id="edce0-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="edce0-116">Gennemfør følgende trin for at begynde at bruge den avancerede formeleditor i din forekomst af Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="edce0-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="edce0-117">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="edce0-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="edce0-118">På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.</span><span class="sxs-lookup"><span data-stu-id="edce0-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="edce0-119">I dialogboksen **Brugerparametre** i sektionen **Kørselssporing** skal du angive parameteren **Aktiver avanceret formeleditor** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="edce0-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="edce0-120">[![Dialogboksen Brugerparametre med parameteren Aktivér avanceret formeleditor fremhævet](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="edce0-120">[![User parameters dialog box, Enable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="edce0-121">Vær opmærksom på, at denne parameter er brugerspecifik og firmaspecifik.</span><span class="sxs-lookup"><span data-stu-id="edce0-121">Be aware that this parameter is user specific and company specific.</span></span>

<span data-ttu-id="edce0-122">Fra og med Microsoft Dynamics 365 Finance version 10.0.19 kan du styre, hvilken ER-formeleditor der skal tilbydes som standard.</span><span class="sxs-lookup"><span data-stu-id="edce0-122">Starting in Microsoft Dynamics 365 Finance version 10.0.19, you can control what ER formula editor is offered by default.</span></span> <span data-ttu-id="edce0-123">Gennemfør følgende trin for at aktivere den avancerede formeleditor for alle brugere og firmaer i den aktuelle Finance-forekomst.</span><span class="sxs-lookup"><span data-stu-id="edce0-123">Complete the following steps to enable the advanced formula editor for all users and companies of the current Finance instance.</span></span>

1.  <span data-ttu-id="edce0-124">Åbn arbejdsområdet **Administration af funktioner**.</span><span class="sxs-lookup"><span data-stu-id="edce0-124">Open the **Feature management** workspace.</span></span>
2.  <span data-ttu-id="edce0-125">Find og vælg funktionen **Indstil den avancerede ER-formeleditor som standard for alle brugere** på listen, og vælg derefter **Aktivér nu**.</span><span class="sxs-lookup"><span data-stu-id="edce0-125">Find and select the feature **Set the ER advanced formula editor as the default one for all users** in the list, and then select **Enable now**.</span></span>
3.  <span data-ttu-id="edce0-126">Gå til **Virksomhedsadministration** > **Elektronisk rapportering** > **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="edce0-126">Go to **Organization administration** > **Electronic reporting** > **Configurations**.</span></span>
4.  <span data-ttu-id="edce0-127">På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.</span><span class="sxs-lookup"><span data-stu-id="edce0-127">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
5.  <span data-ttu-id="edce0-128">Find parameteren **Deaktiver avanceret formeleditor** i dialogboksen **Brugerparametre**, og kontrollér, at den er angivet til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="edce0-128">In the **User parameters** dialog box, find the **Disable advanced formula editor** parameter and verify that it is set to **No**.</span></span>

<span data-ttu-id="edce0-129">[![Dialogboksen Brugerparametre med parameteren Deaktiver avanceret formeleditor fremhævet](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span><span class="sxs-lookup"><span data-stu-id="edce0-129">[![User parameters dialog box, Disable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span></span>

> [!NOTE]
> <span data-ttu-id="edce0-130">Værdierne for parametrene **Aktiverer avanceret formeleditor** og **Deaktiver avanceret formeleditor** holdes adskilt for de enkelte brugere og vises i dialogboksen **Brugerparametre**, afhængigt af statussen for funktionen **Indstil den avancerede ER-formeleditor som standard for alle brugere**.</span><span class="sxs-lookup"><span data-stu-id="edce0-130">The values of the parameters **Enable advanced formula editor** and **Disable advanced formula editor** are kept separate for each user and offered on the **User parameters** dialog box depending on the status of the **Set the ER advanced formula editor as the default one for all users** feature.</span></span>

## <a name=""></a><span data-ttu-id="edce0-131"><a name="Autoformatting">Autoformatering af kode</a></span><span class="sxs-lookup"><span data-stu-id="edce0-131"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="edce0-132">Når du skriver et komplekst udtryk, der består af flere koderækker, sker der automatisk indrykning af en ny linje baseret på indrykningen af den foregående række.</span><span class="sxs-lookup"><span data-stu-id="edce0-132">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="edce0-133">Du kan markere linjer og ændre deres indrykning ved at trykke på **tabulator** eller **Skift+tabulator**.</span><span class="sxs-lookup"><span data-stu-id="edce0-133">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="edce0-134">[![Gif-billede af ER-formeleditor, der viser valg af linjer og ændring af indrykning](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="edce0-134">[![ER formula editor gif showing selecting lines and changing the indentation](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="edce0-135">Automatisk formatering giver dig mulighed for at bevare hele udtrykket formateret, så yderligere vedligeholdelse bliver nemmere, og at forenkle forståelsen af den konfigurerede logik.</span><span class="sxs-lookup"><span data-stu-id="edce0-135">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="edce0-136"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="edce0-136"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="edce0-137">Editoren indsætter ord, så du kan skrive udtryk hurtigere og undgå slåfejl.</span><span class="sxs-lookup"><span data-stu-id="edce0-137">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="edce0-138">Når du begynder at indsætte ny tekst, viser editoren automatisk en liste over funktioner, der understøttes i ER-funktioner, som indeholder de tegn, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="edce0-138">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="edce0-139">Du kan også udløse IntelliSense på et hvilket som helst sted i et konfigureret udtryk ved at trykke på **CTRL+mellemrum**.</span><span class="sxs-lookup"><span data-stu-id="edce0-139">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="edce0-140">[![Gif-billede af ER-formeleditor, der viser udløsning af IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="edce0-140">[![ER formula editor gif showing triggering IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="edce0-141"><a name="CodeCompletion">Fuldførelse af kode</a></span><span class="sxs-lookup"><span data-stu-id="edce0-141"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="edce0-142">Editoren leverer automatisk fuldførelse af kode ved at:</span><span class="sxs-lookup"><span data-stu-id="edce0-142">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="edce0-143">Indsætte en kantet højreparentes, når du angiver en kantet venstreparentes, og holde markøren inden for de kantede parenteser.</span><span class="sxs-lookup"><span data-stu-id="edce0-143">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="edce0-144">Indsætte det andet anførselstegn, når det første er indsat, og holde markøren inden for anførselstegnene.</span><span class="sxs-lookup"><span data-stu-id="edce0-144">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="edce0-145">Indsætte det andet dobbelte anførselstegn, når det første er indsat, og holde markøren inden for anførselstegnene.</span><span class="sxs-lookup"><span data-stu-id="edce0-145">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="edce0-146">[![Gif-billede af ER-formeleditor, der viser, hvordan editoren automatisk færdiggør kode](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="edce0-146">[![ER formula editor gif showing the editor automatically providing code completion](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="edce0-147">Når du peger på den indsatte kantede parentes, fremhæves den anden parentes i parret automatisk, så det viser den konstruktion, som de understøtter.</span><span class="sxs-lookup"><span data-stu-id="edce0-147">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="edce0-148"><a name="CodeNavigation">Kodenavigation</a></span><span class="sxs-lookup"><span data-stu-id="edce0-148"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="edce0-149">Du kan finde påkrævede symboler eller linjer i udtrykket ved at skrive kommandoen **Gå til** ved hjælp af kommandopaletten eller genvejsmenuen.</span><span class="sxs-lookup"><span data-stu-id="edce0-149">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="edce0-150">Hvis du f.eks. vil hoppe til linje **8**, skal du benytte følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="edce0-150">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="edce0-151">Tryk på **Ctrl+G**, angive værdien **8** og derefter trykke på **Enter**.</span><span class="sxs-lookup"><span data-stu-id="edce0-151">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="edce0-152">-eller-</span><span class="sxs-lookup"><span data-stu-id="edce0-152">-or-</span></span>

- <span data-ttu-id="edce0-153">Tryk på **F1**, skriv **G**, vælg **Gå til linje**, skriv værdien **8**, og tryk på **Enter**.</span><span class="sxs-lookup"><span data-stu-id="edce0-153">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="edce0-154">[![Gif-billede af ER-formeleditor, der viser, hvordan du finder dele af et udtryk ved hjælp af kommandopaletten](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="edce0-154">[![ER formula editor gif showing how to locate parts of an expression using the command palette](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="edce0-155"><a name="CodeStructuring">Kodestrukturering</a></span><span class="sxs-lookup"><span data-stu-id="edce0-155"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="edce0-156">Koden for nogle funktioner, f.eks. [IF](er-functions-logical-if.md) eller [CASE](er-functions-logical-case.md), struktureres automatisk.</span><span class="sxs-lookup"><span data-stu-id="edce0-156">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="edce0-157">Du kan udvide og skjule et vilkårligt foldningsområde eller alle foldningsområder i denne kode for at reducere den redigerbare del af et udtryk for kun at fokusere på den del af koden, der kræver din opmærksomhed.</span><span class="sxs-lookup"><span data-stu-id="edce0-157">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="edce0-158">Kommandoerne til at folde/folde ud kan bruges til dette.</span><span class="sxs-lookup"><span data-stu-id="edce0-158">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="edce0-159">Hvis du f.eks. vil folde alle områder, skal du benytte følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="edce0-159">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="edce0-160">Tryk på **Ctrl+K**</span><span class="sxs-lookup"><span data-stu-id="edce0-160">Press **Ctrl+K**</span></span>

  <span data-ttu-id="edce0-161">-eller-</span><span class="sxs-lookup"><span data-stu-id="edce0-161">-or-</span></span>

- <span data-ttu-id="edce0-162">Tryk på **F1**, tryk på **FO**, vælg **Fold alle**, og tryk derefter på **Enter**</span><span class="sxs-lookup"><span data-stu-id="edce0-162">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="edce0-163">Hvis du vil folde alle områder ud, skal du benytte følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="edce0-163">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="edce0-164">Tryk på **Ctrl+J**</span><span class="sxs-lookup"><span data-stu-id="edce0-164">Press **Ctrl+J**</span></span>

  <span data-ttu-id="edce0-165">-eller-</span><span class="sxs-lookup"><span data-stu-id="edce0-165">-or-</span></span>
  
- <span data-ttu-id="edce0-166">Tryk på **F1**, skriv **UD**, vælg **Fold alle ud**, og tryk derefter på **Enter**</span><span class="sxs-lookup"><span data-stu-id="edce0-166">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="edce0-167">[![Gif-billede af ER-formeleditor, der viser, hvordan kode foldes ud](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="edce0-167">[![ER formula editor gif showing code being unfolded](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="edce0-168"><a name="FindAndReplace">Søg og erstat</a></span><span class="sxs-lookup"><span data-stu-id="edce0-168"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="edce0-169">Hvis du vil søge efter forekomster af bestemt tekst, skal du markere teksten i udtrykket og gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="edce0-169">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="edce0-170">Tryk på **Ctrl+F**, og tryk derefter på **F3** for at søge efter den næste forekomst af den markerede tekst, eller tryk på **Skift+F3** for at finde den forrige forekomst.</span><span class="sxs-lookup"><span data-stu-id="edce0-170">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="edce0-171">-eller-</span><span class="sxs-lookup"><span data-stu-id="edce0-171">-or-</span></span>
  
- <span data-ttu-id="edce0-172">Tryk på **F1**, skriv **F**, og vælg derefter den påkrævede indstilling for at finde den markerede tekst.</span><span class="sxs-lookup"><span data-stu-id="edce0-172">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="edce0-173">Hvis du vil erstatte forekomster af en bestemt tekst, skal du markere teksten i udtrykket og gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="edce0-173">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="edce0-174">Tryk på **Ctrl+H**.</span><span class="sxs-lookup"><span data-stu-id="edce0-174">Press **Ctrl+H**.</span></span> <span data-ttu-id="edce0-175">Skriv den alternative tekst, og vælg erstatningsindstillingen for enten at erstatte den markerede tekst eller alle forekomster af denne tekst i det aktuelle udtryk.</span><span class="sxs-lookup"><span data-stu-id="edce0-175">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="edce0-176">-eller-</span><span class="sxs-lookup"><span data-stu-id="edce0-176">-or-</span></span>
  
- <span data-ttu-id="edce0-177">Tryk på **F1**, skriv **R**, og vælg derefter den påkrævede indstilling for at erstatte den markerede tekst.</span><span class="sxs-lookup"><span data-stu-id="edce0-177">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="edce0-178">Skriv den alternative tekst, og vælg erstatningsindstillingen for enten at erstatte den markerede tekst eller alle forekomster af denne tekst i det aktuelle udtryk.</span><span class="sxs-lookup"><span data-stu-id="edce0-178">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="edce0-179">Hvis du vil ændre alle forekomster af en bestemt tekst, skal du markere teksten i udtrykket og gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="edce0-179">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="edce0-180">Tryk på **Ctrl+F2**, og angiv derefter den alternative tekst.</span><span class="sxs-lookup"><span data-stu-id="edce0-180">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="edce0-181">-eller-</span><span class="sxs-lookup"><span data-stu-id="edce0-181">-or-</span></span>
  
- <span data-ttu-id="edce0-182">Tryk på **F1**, skriv **C**, og vælg derefter den påkrævede indstilling for at ændre den markerede tekst.</span><span class="sxs-lookup"><span data-stu-id="edce0-182">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="edce0-183">Skriv den alternative tekst.</span><span class="sxs-lookup"><span data-stu-id="edce0-183">Enter the alternative text.</span></span>

<span data-ttu-id="edce0-184">[![Gif-billede af ER-formeleditor, der viser søg og erstat](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="edce0-184">[![ER formula editor gif showing find and replace](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="edce0-185"><a name="DataPasting">Datakilder og indsætning af funktioner</a></span><span class="sxs-lookup"><span data-stu-id="edce0-185"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="edce0-186">Du kan vælge **Tilføj datakilde**, som indsætter en datakilde, der aktuelt er valgt i **Datakilde** i det venstre panel, i udtrykket.</span><span class="sxs-lookup"><span data-stu-id="edce0-186">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="edce0-187">På samme måde kan du vælge **Tilføj funktion**, som indsætter en funktion, der aktuelt er valgt i **Funktioner** i det højre panel, i udtrykket.</span><span class="sxs-lookup"><span data-stu-id="edce0-187">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="edce0-188">Hvis du bruger ER-formeleditoren, vil en valgt funktion eller en valgt datakilde altid blive indsat i slutningen af det konfigurerede udtryk.</span><span class="sxs-lookup"><span data-stu-id="edce0-188">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="edce0-189">Når du bruger den avancerede ER-formeleditor, kan en valgt funktion eller en valgt datakilde blive indsat i en vilkårlig del af det konfigurerede udtryk.</span><span class="sxs-lookup"><span data-stu-id="edce0-189">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="edce0-190">Du skal bruge markøren til at angive, hvor du vil indsætte dataene.</span><span class="sxs-lookup"><span data-stu-id="edce0-190">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="edce0-191">[![Gif-billede af ER-formeleditor, der viser tilføjelse af en datakilde og indsættelse af en funktion](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="edce0-191">[![ER formula editor gif showing adding a data source and pasting a function](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="edce0-192"><a name="SyntaxColorization">Syntaksfarvelægning</a></span><span class="sxs-lookup"><span data-stu-id="edce0-192"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="edce0-193">I øjeblikket bruges forskellige farver til at fremhæve følgende dele af udtryk:</span><span class="sxs-lookup"><span data-stu-id="edce0-193">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="edce0-194">Teksten i dobbelte parenteser, der kan repræsentere et etiket-id for en tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="edce0-194">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="edce0-195">[![ER-formeleditor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="edce0-195">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="edce0-196">Begrænsninger</span><span class="sxs-lookup"><span data-stu-id="edce0-196">Limitations</span></span>

<span data-ttu-id="edce0-197">Editoren understøttes i øjeblikket i følgende webbrowsere:</span><span class="sxs-lookup"><span data-stu-id="edce0-197">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="edce0-198">Chrome</span><span class="sxs-lookup"><span data-stu-id="edce0-198">Chrome</span></span>
- <span data-ttu-id="edce0-199">Kant</span><span class="sxs-lookup"><span data-stu-id="edce0-199">Edge</span></span>
- <span data-ttu-id="edce0-200">Firefox</span><span class="sxs-lookup"><span data-stu-id="edce0-200">Firefox</span></span>
- <span data-ttu-id="edce0-201">Opera</span><span class="sxs-lookup"><span data-stu-id="edce0-201">Opera</span></span>
- <span data-ttu-id="edce0-202">Safari</span><span class="sxs-lookup"><span data-stu-id="edce0-202">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="edce0-203">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="edce0-203">Additional resources</span></span>

- [<span data-ttu-id="edce0-204">Oversigt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="edce0-204">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="edce0-205">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="edce0-205">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="edce0-206">Monaco-editor</span><span class="sxs-lookup"><span data-stu-id="edce0-206">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
