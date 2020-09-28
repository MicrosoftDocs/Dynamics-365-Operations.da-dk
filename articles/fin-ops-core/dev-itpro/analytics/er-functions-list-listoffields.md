---
title: ER-funktionen LISTOFFIELDS
description: Dette emne indeholder oplysninger om, hvordan funktionen LISTOFFIELDS til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c288050fa1f9f1be9c38696e844e782794795471
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745075"
---
# <a name="listoffields-er-function"></a><span data-ttu-id="d1fb0-103">ER-funktionen LISTOFFIELDS</span><span class="sxs-lookup"><span data-stu-id="d1fb0-103">LISTOFFIELDS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1fb0-104">Funktionen `LISTOFFIELDS` returnerer en *Postliste*-værdi, der er oprettet på baggrund af strukturen af det angivne argument i typen *Fasttekst* eller *Container (post)*.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d1fb0-105">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="d1fb0-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="d1fb0-106">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="d1fb0-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="d1fb0-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="d1fb0-107">Arguments</span></span>

<span data-ttu-id="d1fb0-108">`path`: Datakildenreference</span><span class="sxs-lookup"><span data-stu-id="d1fb0-108">`path`: Data source reference</span></span>

<span data-ttu-id="d1fb0-109">Den gyldige referencesti til en datakilde for en af følgende datatyper:</span><span class="sxs-lookup"><span data-stu-id="d1fb0-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="d1fb0-110">Modelfasttekst</span><span class="sxs-lookup"><span data-stu-id="d1fb0-110">Model enumeration</span></span>
- <span data-ttu-id="d1fb0-111">Formatfasttekst</span><span class="sxs-lookup"><span data-stu-id="d1fb0-111">Format enumeration</span></span>
- <span data-ttu-id="d1fb0-112">Programfasttekst</span><span class="sxs-lookup"><span data-stu-id="d1fb0-112">Application enumeration</span></span>
- <span data-ttu-id="d1fb0-113">Container (post)</span><span class="sxs-lookup"><span data-stu-id="d1fb0-113">Container (record)</span></span>

<span data-ttu-id="d1fb0-114">`language`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="d1fb0-114">`language`: *String*</span></span>

<span data-ttu-id="d1fb0-115">Tekst, der repræsenterer en sprogkode.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="d1fb0-116">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="d1fb0-116">Return values</span></span>

<span data-ttu-id="d1fb0-117">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="d1fb0-117">*Record list*</span></span>

<span data-ttu-id="d1fb0-118">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d1fb0-119">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="d1fb0-119">Usage notes</span></span>

<span data-ttu-id="d1fb0-120">Den liste, der oprettes, består af poster, der har følgende felter:</span><span class="sxs-lookup"><span data-stu-id="d1fb0-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="d1fb0-121">**Navn** (*Streng*-datatype)</span><span class="sxs-lookup"><span data-stu-id="d1fb0-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="d1fb0-122">**Etiket** (*Streng*-datatype)</span><span class="sxs-lookup"><span data-stu-id="d1fb0-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="d1fb0-123">**Beskrivelse** (*Streng*-datatype)</span><span class="sxs-lookup"><span data-stu-id="d1fb0-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="d1fb0-124">**IsTranslated** (*Boolesk*-datatype)</span><span class="sxs-lookup"><span data-stu-id="d1fb0-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="d1fb0-125">Hvis `path`-argumentet refererer til en datakilde for typen *Container (post)*, føjes der en ny post til den liste, der oprettes, for hvert felt i den refererede containerpost.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="d1fb0-126">For hver post, der oprettes, returnerer feltet **Navn** navnet på feltet for den containerpost, der refereres til, som den aktuelle post blev oprettet for.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="d1fb0-127">Hvis `path`-argumentet refererer til en datakilde af typen *Fasttekst*, føjes der en ny post til den liste, der oprettes, for hver fasttekstværdi i den refererede fasttekst.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="d1fb0-128">For hver post, der oprettes, returnerer feltet **Navn** værdien af den refererede fasttekst, som den aktuelle post er oprettet for; feltet **Beskrivelse** returnerer beskrivelsen af denne fasttekst, og feltet **Etiket** returnerer etiketten for den pågældende fasttekst.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="d1fb0-129">Når der på kørselstidspunktet bruges syntaks 1, skal felterne **Etiket** og **Beskrivelse** returnere værdier, der er baseret på sprogindstillingerne i det elektroniske rapporteringsformat (ER), der kører:</span><span class="sxs-lookup"><span data-stu-id="d1fb0-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="d1fb0-130">Hvis etiketterne og beskrivelserne for det ønskede sprog er tilgængelige, returnerer felterne **Etiket** og **Beskrivelse** værdier, der er baseret på det pågældende sprog, og feltet **IsTranslated** returnerer **Sandt**.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="d1fb0-131">Hvis etiketterne og beskrivelserne for det ønskede sprog ikke er tilgængelige, returnerer felterne **Etiket** og **Beskrivelse** værdier, der er baseret på standardsproget **EN-US**, og feltet **IsTranslated** returnerer **Falsk**.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="d1fb0-132">Når der på kørselstidspunktet bruges syntaks 2, skal felterne **Etiket** og **Beskrivelse** returnere værdier, der er baseret på det sprog, som der er defineret som det andet argument i den kaldte funktion:</span><span class="sxs-lookup"><span data-stu-id="d1fb0-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="d1fb0-133">Hvis etiketterne og beskrivelserne for det ønskede sprog er tilgængelige, returnerer felterne **Etiket** og **Beskrivelse** værdier, der er baseret på det pågældende sprog, og feltet **IsTranslated** returnerer **Sandt**.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="d1fb0-134">Hvis etiketterne og beskrivelserne for det ønskede sprog ikke er tilgængelige, returnerer felterne **Etiket** og **Beskrivelse** værdier, der er baseret på sproget **EN-US**, og feltet **IsTranslated** returnerer **Falsk**.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="d1fb0-135">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="d1fb0-135">Example 1</span></span>

<span data-ttu-id="d1fb0-136">I følgende illustration introduceres en fasttekst i en ER-datamodel.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="d1fb0-137">Følgende illustration viser disse detaljer:</span><span class="sxs-lookup"><span data-stu-id="d1fb0-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="d1fb0-138">Modelfastteksten indsættes i en rapport som en datakilde.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="d1fb0-139">Et ER-udtryk bruger modelfastteksten som et parameter til funktionen `LISTOFFIELDS`.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="d1fb0-140">En datakilde af typen *Postliste* indsættes i en rapport ved hjælp af det oprettede ER-udtryk.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="d1fb0-141">Følgende eksempel viser de ER-formatelementer, der er bundet til datakilden af typen *Postliste*, der blev oprettet ved hjælp af funktionen `LISTOFFIELDS`.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="d1fb0-142">I følgende illustration vises resultatet, når det designede format køres.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="d1fb0-143">Baseret på sprogindstillingerne til de overordnede formatelementer for **FILE** og **FOLDER**, udfyldes oversat tekst til etiketter og beskrivelser i outputtet til ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="d1fb0-144">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="d1fb0-144">Example 2</span></span>

<span data-ttu-id="d1fb0-145">Du bruger datakildetypen *Beregnet felt* til at konfigurere datakilderne **enumType\_de** og **enumType\_deCH** for datamodelfastteksten **enumType**:</span><span class="sxs-lookup"><span data-stu-id="d1fb0-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="d1fb0-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="d1fb0-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="d1fb0-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="d1fb0-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="d1fb0-148">I dette tilfælde skal kan du bruge følgende udtryk til at få etiketten til tællerværdien på tysk (Schweiz), hvis den pågældende oversættelse er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="d1fb0-149">Hvis oversættelsen til tysk (Schweiz) ikke er tilgængelig, er etiketten på tysk.</span><span class="sxs-lookup"><span data-stu-id="d1fb0-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="d1fb0-150">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="d1fb0-150">Additional resources</span></span>

[<span data-ttu-id="d1fb0-151">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="d1fb0-151">List functions</span></span>](er-functions-category-list.md)
