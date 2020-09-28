---
title: ER-funktionen DATETIMEFORMAT
description: Dette emne indeholder oplysninger om, hvordan funktionen DATETIMEFORMAT til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 65b988e6c58aed35577288e01157b8c1f76e6efd
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744857"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="b6338-103">ER-funktionen DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="b6338-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6338-104">Funktionen `DATETIMEFORMAT` returnerer en *Streng*-værdi, som præsenterer en given dato-/klokkeslætsværdi som tekst i det angivne format og i en eventuelt angivet [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="b6338-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="b6338-105">Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="b6338-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b6338-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="b6338-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="b6338-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="b6338-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="b6338-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="b6338-108">Arguments</span></span>

<span data-ttu-id="b6338-109">`datetime`: *DatoKlokkeslæt*</span><span class="sxs-lookup"><span data-stu-id="b6338-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="b6338-110">En dato-/klokkeslætsværdi, der repræsenterer den dato og det klokkeslæt, der skal formateres.</span><span class="sxs-lookup"><span data-stu-id="b6338-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="b6338-111">`format`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="b6338-111">`format`: *String*</span></span>

<span data-ttu-id="b6338-112">Outputstrengens format.</span><span class="sxs-lookup"><span data-stu-id="b6338-112">The format of the output string.</span></span>

<span data-ttu-id="b6338-113">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="b6338-113">`culture`: *String*</span></span>

<span data-ttu-id="b6338-114">Den kultur, du vil bruge til formatering.</span><span class="sxs-lookup"><span data-stu-id="b6338-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="b6338-115">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="b6338-115">Return values</span></span>

<span data-ttu-id="b6338-116">*Streng*</span><span class="sxs-lookup"><span data-stu-id="b6338-116">*String*</span></span>

<span data-ttu-id="b6338-117">Den resulterende strengværdi.</span><span class="sxs-lookup"><span data-stu-id="b6338-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b6338-118">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="b6338-118">Usage notes</span></span>

<span data-ttu-id="b6338-119">Når kulturen ikke er defineret som et argument for den kaldte funktion, er værdien af `culture` defineret af den kaldende kontekst.</span><span class="sxs-lookup"><span data-stu-id="b6338-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="b6338-120">For eksempel, hvis funktionen `DATETIMEFORMAT` kaldes ved hjælp af syntaks 1 i et elektronisk rapporteringsformat (ER) for et **FIL**-element, der er konfigureret til at bruge den tyske kultur, vil konverteringen ske ved hjælp af den tyske kultur.</span><span class="sxs-lookup"><span data-stu-id="b6338-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="b6338-121">Standardværdien for `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="b6338-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="b6338-122">Når funktionen `DATETIMEFORMAT` konverterer en given dato-/klokkeslætsværdi, tages den tidszoneindstillingen for den programbruger, der kører ER-formatet, som funktionen kaldes i sammenhæng med i betragtning.</span><span class="sxs-lookup"><span data-stu-id="b6338-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="b6338-123">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="b6338-123">Example 1</span></span>

<span data-ttu-id="b6338-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returnerer den aktuelle dato-/klokkeslætsværdi på programserver, 24. december 2015, som **"24-12-2015"**, baseret på det angivne brugerdefinerede format.</span><span class="sxs-lookup"><span data-stu-id="b6338-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="b6338-125">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="b6338-125">Example 2</span></span>

<span data-ttu-id="b6338-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returnerer datoen/klokkeslættet for den aktuelle programsession, 24. december 2015, som strengen **"24.12.2015"**, baseret på den valgte tyske kultur og det angivne format.</span><span class="sxs-lookup"><span data-stu-id="b6338-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="b6338-127">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="b6338-127">Example 3</span></span>

<span data-ttu-id="b6338-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returnerer strengværdien **2019-11-12T08:00:00.0000000-08:00**, når den kaldes under en proces, der blev initieret af en programbruger, der har tidszoneværdien **(GMT-08:00) Pacific Time (USA og Canada)** i afsnittet **Sprog og lande-/områdepræferencer**.</span><span class="sxs-lookup"><span data-stu-id="b6338-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6338-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b6338-129">Additional resources</span></span>

[<span data-ttu-id="b6338-130">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="b6338-130">Date and time functions</span></span>](er-functions-category-datetime.md)
