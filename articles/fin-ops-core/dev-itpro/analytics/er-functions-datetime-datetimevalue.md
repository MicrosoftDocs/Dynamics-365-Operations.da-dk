---
title: ER-funktionen DATETIMEVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen DATETIMEVALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 29d81599563dec2827fa8a82c86b74cb9e34eea2
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070684"
---
# <span data-ttu-id="71b1a-103"><a name="DATETIMEVALUE">ER-funktionen DATETIMEVALUE</a></span><span class="sxs-lookup"><span data-stu-id="71b1a-103"><a name="DATETIMEVALUE">DATETIMEVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71b1a-104">Funktionen `DATETIMEVALUE` returnerer en værdi i form af *DatoKlokkeslæt*, som er konverteret fra en given tekst i det angivne format og i en eventuelt angivet [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) til en dato-/klokkeslætsværdi.</span><span class="sxs-lookup"><span data-stu-id="71b1a-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="71b1a-105">Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="71b1a-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="71b1a-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="71b1a-106">Syntax 1</span></span>

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="71b1a-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="71b1a-107">Syntax 2</span></span>

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="71b1a-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="71b1a-108">Arguments</span></span>

<span data-ttu-id="71b1a-109">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="71b1a-109">`text`: *String*</span></span>

<span data-ttu-id="71b1a-110">Tekst, der repræsenterer den værdi, der skal formateres.</span><span class="sxs-lookup"><span data-stu-id="71b1a-110">Text that represents the value to format.</span></span>

<span data-ttu-id="71b1a-111">`format`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="71b1a-111">`format`: *String*</span></span>

<span data-ttu-id="71b1a-112">Den angivne tekst format.</span><span class="sxs-lookup"><span data-stu-id="71b1a-112">The format of the given text.</span></span>

<span data-ttu-id="71b1a-113">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="71b1a-113">`culture`: *String*</span></span>

<span data-ttu-id="71b1a-114">Den kultur, der bruges til formatering af den givne tekst.</span><span class="sxs-lookup"><span data-stu-id="71b1a-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="71b1a-115">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="71b1a-115">Return values</span></span>

<span data-ttu-id="71b1a-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="71b1a-116">*DateTime*</span></span>

<span data-ttu-id="71b1a-117">Den returnerede dato-/klokkeslætsværdi.</span><span class="sxs-lookup"><span data-stu-id="71b1a-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="71b1a-118">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="71b1a-118">Usage notes</span></span>

<span data-ttu-id="71b1a-119">Når kulturen ikke er defineret som et argument for den kaldte funktion, er værdien af `culture` defineret af den kaldende kontekst.</span><span class="sxs-lookup"><span data-stu-id="71b1a-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="71b1a-120">For eksempel, hvis funktionen `DATETIMEVALUE` kaldes ved hjælp af syntaks 1 i et elektronisk rapporteringsformat (ER) for et **FIL**-element, der er konfigureret til at bruge den tyske kultur, vil konverteringen ske ved hjælp af den tyske kultur.</span><span class="sxs-lookup"><span data-stu-id="71b1a-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="71b1a-121">Standardværdien for `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="71b1a-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="71b1a-122">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="71b1a-122">Example 1</span></span>

<span data-ttu-id="71b1a-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returnerer **2:55:00 den 21. december 21 2016**, baseret på det angivne brugerdefinerede format og standardprogrammets **en-us** kultur.</span><span class="sxs-lookup"><span data-stu-id="71b1a-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="71b1a-124">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="71b1a-124">Example 2</span></span>

<span data-ttu-id="71b1a-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returnerer **2:55:00 den 21. december 21 2016**, baseret på det angivne brugerdefinerede format og kultur.</span><span class="sxs-lookup"><span data-stu-id="71b1a-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="71b1a-126">Men `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` udløser en undtagelse for at informere brugeren om, at den angivne streng ikke genkendes som en gyldig dato-/klokkeslætsværdi for den angivne kultur.</span><span class="sxs-lookup"><span data-stu-id="71b1a-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71b1a-127">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="71b1a-127">Additional resources</span></span>

[<span data-ttu-id="71b1a-128">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="71b1a-128">Date and time functions</span></span>](er-functions-category-datetime.md)
