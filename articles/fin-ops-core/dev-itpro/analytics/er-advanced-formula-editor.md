---
title: Avanceret formeleditor til elektronisk rapportering
description: Denne artikel beskriver, hvordan den avancerede formeleditor kan bruges til at konfigurere udtryk i modeltilknytning til elektronisk rapportering (ER) og formatkomponenter.
author: kfend
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
ms.openlocfilehash: 269102028962cf1ebae599b9885f97871785a551
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286211"
---
# <a name="electronic-reporting-advanced-formula-editor"></a>Avanceret formeleditor til elektronisk rapportering

[!include [banner](../includes/banner.md)]

Udover den [elektroniske rapporterings](general-electronic-reporting.md) [formeleditor](general-electronic-reporting-formula-designer.md) kan du bruge den avancerede formeleditor til elektronisk rapportering til at forbedre oplevelsen i forbindelse med konfiguration af elektroniske rapporteringsudtryk (ER). Den avancerede editor er browserbaseret og er styret af [Monaco-editoren](https://microsoft.github.io/monaco-editor). De mest almindeligt anvendte avancerede funktioner i editoren er beskrevet i denne artikel:

- [Autoformatering af kode](#Autoformatting)
- [IntelliSense](#IntelliSense)
- [Fuldførelse af kode](#CodeCompletion)
- [Kodenavigation](#CodeNavigation)
- [Kodestrukturering](#CodeStructuring)
- [Søg og erstat](#FindAndReplace)
- [Indsætning af data](#DataPasting)
- [Syntaksfarvelægning](#SyntaxColorization)

## <a name=""></a><a name="ActivateAdvEditor">Aktivere den avancerede formeleditor</a>

Gennemfør følgende trin for at begynde at bruge den avancerede formeleditor i din forekomst af Microsoft Dynamics 365 Finance.

1.  Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2.  På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3.  I dialogboksen **Brugerparametre** i sektionen **Kørselssporing** skal du angive parameteren **Aktiver avanceret formeleditor** til **Ja**.

[![Dialogboksen Brugerparametre med parameteren Aktivér avanceret formeleditor fremhævet.](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)

> [!NOTE]
> Vær opmærksom på, at denne parameter er brugerspecifik og firmaspecifik.

Fra og med Microsoft Dynamics 365 Finance version 10.0.19 kan du styre, hvilken ER-formeleditor der skal tilbydes som standard. Gennemfør følgende trin for at aktivere den avancerede formeleditor for alle brugere og firmaer i den aktuelle Finance-forekomst.

1.  Åbn arbejdsområdet **Administration af funktioner**.
2.  Find og vælg funktionen **Indstil den avancerede ER-formeleditor som standard for alle brugere** på listen, og vælg derefter **Aktivér nu**.
3.  Gå til **Virksomhedsadministration** > **Elektronisk rapportering** > **Konfigurationer**.
4.  På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
5.  Find parameteren **Deaktiver avanceret formeleditor** i dialogboksen **Brugerparametre**, og kontrollér, at den er angivet til **Nej**.

[![Dialogboksen Brugerparametre med parameteren Deaktiver avanceret formeleditor fremhævet.](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)

> [!NOTE]
> Værdierne for parametrene **Aktiverer avanceret formeleditor** og **Deaktiver avanceret formeleditor** holdes adskilt for de enkelte brugere og vises i dialogboksen **Brugerparametre**, afhængigt af statussen for funktionen **Indstil den avancerede ER-formeleditor som standard for alle brugere**.

## <a name=""></a><a name="Autoformatting">Autoformatering af kode</a>

Når du skriver et komplekst udtryk, der består af flere koderækker, sker der automatisk indrykning af en ny linje baseret på indrykningen af den foregående række. Du kan markere linjer og ændre deres indrykning ved at trykke på **tabulator** eller **Skift+tabulator**.

[![Gif-billede af ER-formeleditor, der viser valg af linjer og ændring af indrykning.](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)

Automatisk formatering giver dig mulighed for at bevare hele udtrykket formateret, så yderligere vedligeholdelse bliver nemmere, og at forenkle forståelsen af den konfigurerede logik.

## <a name=""></a><a name="IntelliSense">IntelliSense</a>

Editoren indsætter ord, så du kan skrive udtryk hurtigere og undgå slåfejl. Når du begynder at indsætte ny tekst, viser editoren automatisk en liste over funktioner, der understøttes i ER-funktioner, som indeholder de tegn, du har angivet. Du kan også udløse IntelliSense på et hvilket som helst sted i et konfigureret udtryk ved at trykke på **CTRL+mellemrum**.

[![Gif-billede af ER-formeleditor, der viser udløsning af IntelliSense.](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)

## <a name=""></a><a name="CodeCompletion">Fuldførelse af kode</a>

Editoren leverer automatisk fuldførelse af kode ved at:

- Indsætte en kantet højreparentes, når du angiver en kantet venstreparentes, og holde markøren inden for de kantede parenteser.
- Indsætte det andet anførselstegn, når det første er indsat, og holde markøren inden for anførselstegnene.
- Indsætte det andet dobbelte anførselstegn, når det første er indsat, og holde markøren inden for anførselstegnene.

[![Gif-billede af ER-formeleditor, der viser, hvordan editoren automatisk færdiggør kode.](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)

Når du peger på den indsatte kantede parentes, fremhæves den anden parentes i parret automatisk, så det viser den konstruktion, som de understøtter.

## <a name=""></a><a name="CodeNavigation">Kodenavigation</a>

Du kan finde påkrævede symboler eller linjer i udtrykket ved at skrive kommandoen **Gå til** ved hjælp af kommandopaletten eller genvejsmenuen.

Hvis du f.eks. vil hoppe til linje **8**, skal du benytte følgende fremgangsmåde:

- Tryk på **Ctrl+G**, angive værdien **8** og derefter trykke på **Enter**.

  -eller-

- Tryk på **F1**, skriv **G**, vælg **Gå til linje**, skriv værdien **8**, og tryk på **Enter**.

[![Gif-billede af ER-formeleditor, der viser, hvordan du finder dele af et udtryk ved hjælp af kommandopaletten.](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)

## <a name=""></a><a name="CodeStructuring">Kodestrukturering</a>

Koden for nogle funktioner, f.eks. [IF](er-functions-logical-if.md) eller [CASE](er-functions-logical-case.md), struktureres automatisk. Du kan udvide og skjule et vilkårligt foldningsområde eller alle foldningsområder i denne kode for at reducere den redigerbare del af et udtryk for kun at fokusere på den del af koden, der kræver din opmærksomhed. Kommandoerne til at folde/folde ud kan bruges til dette.

Hvis du f.eks. vil folde alle områder, skal du benytte følgende fremgangsmåde:

- Tryk på **Ctrl+K**

  -eller-

- Tryk på **F1**, tryk på **FO**, vælg **Fold alle**, og tryk derefter på **Enter**

Hvis du vil folde alle områder ud, skal du benytte følgende fremgangsmåde:

- Tryk på **Ctrl+J**

  -eller-
  
- Tryk på **F1**, skriv **UD**, vælg **Fold alle ud**, og tryk derefter på **Enter**

[![Gif-billede af ER-formeleditor, der viser, hvordan kode foldes ud.](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)

## <a name=""></a><a name="FindAndReplace">Søg og erstat</a>

Hvis du vil søge efter forekomster af bestemt tekst, skal du markere teksten i udtrykket og gøre følgende:

- Tryk på **Ctrl+F**, og tryk derefter på **F3** for at søge efter den næste forekomst af den markerede tekst, eller tryk på **Skift+F3** for at finde den forrige forekomst.

  -eller-
  
- Tryk på **F1**, skriv **F**, og vælg derefter den påkrævede indstilling for at finde den markerede tekst.

Hvis du vil erstatte forekomster af en bestemt tekst, skal du markere teksten i udtrykket og gøre følgende:

- Tryk på **Ctrl+H**. Skriv den alternative tekst, og vælg erstatningsindstillingen for enten at erstatte den markerede tekst eller alle forekomster af denne tekst i det aktuelle udtryk.

  -eller-
  
- Tryk på **F1**, skriv **R**, og vælg derefter den påkrævede indstilling for at erstatte den markerede tekst. Skriv den alternative tekst, og vælg erstatningsindstillingen for enten at erstatte den markerede tekst eller alle forekomster af denne tekst i det aktuelle udtryk.

Hvis du vil ændre alle forekomster af en bestemt tekst, skal du markere teksten i udtrykket og gøre følgende:

- Tryk på **Ctrl+F2**, og angiv derefter den alternative tekst.

  -eller-
  
- Tryk på **F1**, skriv **C**, og vælg derefter den påkrævede indstilling for at ændre den markerede tekst. Skriv den alternative tekst.

[![Gif-billede af ER-formeleditor, der viser søg og erstat.](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)

## <a name=""></a><a name="DataPasting">Datakilder og indsætning af funktioner</a>

Du kan vælge **Tilføj datakilde**, som indsætter en datakilde, der aktuelt er valgt i **Datakilde** i det venstre panel, i udtrykket. På samme måde kan du vælge **Tilføj funktion**, som indsætter en funktion, der aktuelt er valgt i **Funktioner** i det højre panel, i udtrykket. Hvis du bruger ER-formeleditoren, vil en valgt funktion eller en valgt datakilde altid blive indsat i slutningen af det konfigurerede udtryk. Når du bruger den avancerede ER-formeleditor, kan en valgt funktion eller en valgt datakilde blive indsat i en vilkårlig del af det konfigurerede udtryk. Du skal bruge markøren til at angive, hvor du vil indsætte dataene.

[![Gif-billede af ER-formeleditor, der viser tilføjelse af en datakilde og indsættelse af en funktion.](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)

## <a name=""></a><a name="SyntaxColorization">Syntaksfarvelægning</a>

I øjeblikket bruges forskellige farver til at fremhæve følgende dele af udtryk:

- Teksten i dobbelte parenteser, der kan repræsentere et etiket-id for en tekstkonstant.

[![ER-formeleditor.](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)

## <a name="limitations"></a>Begrænsninger

Editoren understøttes i øjeblikket i følgende webbrowsere:

- Chrome
- Kant
- Firefox
- Opera
- Safari

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)
- [Monaco-editor](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
