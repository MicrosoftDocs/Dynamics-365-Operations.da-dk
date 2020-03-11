---
title: ER-funktionen DATEFORMAT
description: Dette emne indeholder oplysninger om, hvordan funktionen DATEFORMAT til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 759ccd3cf16c6c109faf44cea350745e3b2bff0b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042429"
---
# <span data-ttu-id="28d6f-103"><a name="DATEFORMAT">ER-funktionen DATEFORMAT</a></span><span class="sxs-lookup"><span data-stu-id="28d6f-103"><a name="DATEFORMAT">DATEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28d6f-104">Funktionen `DATEFORMAT` returnerer en *Streng*-værdi, som præsenterer en given datoværdi som tekst i det angivne format og i en eventuelt angivet [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="28d6f-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="28d6f-105">Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="28d6f-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="28d6f-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="28d6f-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="28d6f-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="28d6f-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="28d6f-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="28d6f-108">Arguments</span></span>

<span data-ttu-id="28d6f-109">`date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="28d6f-109">`date`: *Date*</span></span>

<span data-ttu-id="28d6f-110">En datoværdi, der repræsenterer den dato, der skal formateres.</span><span class="sxs-lookup"><span data-stu-id="28d6f-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="28d6f-111">`format`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="28d6f-111">`format`: *String*</span></span>

<span data-ttu-id="28d6f-112">Outputstrengens format.</span><span class="sxs-lookup"><span data-stu-id="28d6f-112">The format of the output string.</span></span>

<span data-ttu-id="28d6f-113">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="28d6f-113">`culture`: *String*</span></span>

<span data-ttu-id="28d6f-114">Den kultur, du vil bruge til formatering.</span><span class="sxs-lookup"><span data-stu-id="28d6f-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="28d6f-115">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="28d6f-115">Return values</span></span>

<span data-ttu-id="28d6f-116">*Streng*</span><span class="sxs-lookup"><span data-stu-id="28d6f-116">*String*</span></span>

<span data-ttu-id="28d6f-117">Den resulterende strengværdi.</span><span class="sxs-lookup"><span data-stu-id="28d6f-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="28d6f-118">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="28d6f-118">Usage notes</span></span>

<span data-ttu-id="28d6f-119">Når kulturen ikke er defineret som et argument for den kaldte funktion, er værdien af `culture` defineret af den kaldende kontekst.</span><span class="sxs-lookup"><span data-stu-id="28d6f-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="28d6f-120">For eksempel, hvis funktionen `DATEFORMAT` kaldes ved hjælp af syntaks 1 i et elektronisk rapporteringsformat (ER) for et **FIL**-element, der er konfigureret til at bruge den tyske kultur, vil konverteringen ske ved hjælp af den tyske kultur.</span><span class="sxs-lookup"><span data-stu-id="28d6f-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="28d6f-121">Standardværdien for `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="28d6f-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="28d6f-122">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="28d6f-122">Example 1</span></span>

<span data-ttu-id="28d6f-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returnerer den aktuelle dato-/klokkeslætsværdi på programserver, 24. december 2015, som strengen **"24-12-2015"**, baseret på det angivne brugerdefinerede format.</span><span class="sxs-lookup"><span data-stu-id="28d6f-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="28d6f-124">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="28d6f-124">Example 2</span></span>

<span data-ttu-id="28d6f-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returnerer datoen for den aktuelle programsession, 24. december 2015, som strengen **"24-12-2015"**, baseret på den valgte tyske kultur og det angivne format.</span><span class="sxs-lookup"><span data-stu-id="28d6f-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28d6f-126">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="28d6f-126">Additional resources</span></span>

[<span data-ttu-id="28d6f-127">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="28d6f-127">Date and time functions</span></span>](er-functions-category-datetime.md)
