---
title: ER-funktionen DATEVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen DATEVALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82feb8284f4b6116a53d174dcdd9b8c09c4fa63a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563552"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="de7b9-103">ER-funktionen DATEVALUE</span><span class="sxs-lookup"><span data-stu-id="de7b9-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de7b9-104">Funktionen `DATEVALUE` returnerer en værdi i form af en *Dato*, som er konverteret fra en given tekst i det angivne format og i en eventuelt angivet [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) til en datoværdi.</span><span class="sxs-lookup"><span data-stu-id="de7b9-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="de7b9-105">Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="de7b9-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="de7b9-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="de7b9-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="de7b9-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="de7b9-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="de7b9-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="de7b9-108">Arguments</span></span>

<span data-ttu-id="de7b9-109">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="de7b9-109">`text`: *String*</span></span>

<span data-ttu-id="de7b9-110">Tekst, der repræsenterer den værdi, der skal formateres.</span><span class="sxs-lookup"><span data-stu-id="de7b9-110">Text that represents the value to format.</span></span>

<span data-ttu-id="de7b9-111">`format`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="de7b9-111">`format`: *String*</span></span>

<span data-ttu-id="de7b9-112">Den angivne tekst format.</span><span class="sxs-lookup"><span data-stu-id="de7b9-112">The format of the given text.</span></span>

<span data-ttu-id="de7b9-113">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="de7b9-113">`culture`: *String*</span></span>

<span data-ttu-id="de7b9-114">Den kultur, der bruges til formatering af den givne tekst.</span><span class="sxs-lookup"><span data-stu-id="de7b9-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="de7b9-115">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="de7b9-115">Return values</span></span>

<span data-ttu-id="de7b9-116">*Dato*</span><span class="sxs-lookup"><span data-stu-id="de7b9-116">*Date*</span></span>

<span data-ttu-id="de7b9-117">Den returnerede datoværdi.</span><span class="sxs-lookup"><span data-stu-id="de7b9-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="de7b9-118">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="de7b9-118">Usage notes</span></span>

<span data-ttu-id="de7b9-119">Når kulturen ikke er defineret som et argument for den kaldte funktion, er værdien af `culture` defineret af den kaldende kontekst.</span><span class="sxs-lookup"><span data-stu-id="de7b9-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="de7b9-120">For eksempel, hvis funktionen `DATEVALUE` kaldes ved hjælp af syntaks 1 i et elektronisk rapporteringsformat (ER) for et **FIL**-element, der er konfigureret til at bruge den tyske kultur, vil konverteringen ske ved hjælp af den tyske kultur.</span><span class="sxs-lookup"><span data-stu-id="de7b9-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="de7b9-121">Standardværdien for `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="de7b9-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="de7b9-122">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="de7b9-122">Example 1</span></span>

<span data-ttu-id="de7b9-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returnerer datoværdien **21. december 21 2016**, baseret på det angivne brugerdefinerede format og standardprogrammets **en-us** kultur.</span><span class="sxs-lookup"><span data-stu-id="de7b9-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="de7b9-124">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="de7b9-124">Example 2</span></span>

<span data-ttu-id="de7b9-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returnerer datoværdien **21. januar 2016**, baseret på det angivne brugerdefinerede format og kultur.</span><span class="sxs-lookup"><span data-stu-id="de7b9-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="de7b9-126">Men `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` udløser en undtagelse for at informere brugeren om, at den angivne streng ikke genkendes som en gyldig dato for den angivne kultur.</span><span class="sxs-lookup"><span data-stu-id="de7b9-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de7b9-127">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="de7b9-127">Additional resources</span></span>

[<span data-ttu-id="de7b9-128">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="de7b9-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]