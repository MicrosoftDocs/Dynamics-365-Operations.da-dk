---
title: ER-funktionen DATEFORMAT
description: Dette emne indeholder oplysninger om, hvordan funktionen DATEFORMAT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 1b3a0a2608328b233004034f7ab2ccfa833c17e3
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890904"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="8f05c-103">ER-funktionen DATEFORMAT</span><span class="sxs-lookup"><span data-stu-id="8f05c-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f05c-104">Funktionen `DATEFORMAT` returnerer en *Streng*-værdi, som præsenterer en given datoværdi som tekst i det angivne format og i en eventuelt angivet [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="8f05c-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="8f05c-105">Oplysninger om understøttede formater finder du under [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [brugerdefineret](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="8f05c-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="8f05c-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="8f05c-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="8f05c-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="8f05c-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="8f05c-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="8f05c-108">Arguments</span></span>

<span data-ttu-id="8f05c-109">`date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="8f05c-109">`date`: *Date*</span></span>

<span data-ttu-id="8f05c-110">En datoværdi, der repræsenterer den dato, der skal formateres.</span><span class="sxs-lookup"><span data-stu-id="8f05c-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="8f05c-111">`format`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="8f05c-111">`format`: *String*</span></span>

<span data-ttu-id="8f05c-112">Outputstrengens format.</span><span class="sxs-lookup"><span data-stu-id="8f05c-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="8f05c-113">Der skelnes mellem store og små bogstaver i formatstrengen, når du enten bruger et standardformat eller et brugerdefineret format.</span><span class="sxs-lookup"><span data-stu-id="8f05c-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="8f05c-114">F.eks. returnerer [standardformatet](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" datoen ved at bruge det korte datomønster, mens standardformatet "D" returnerer datoen ved at bruge det lange datomønster.</span><span class="sxs-lookup"><span data-stu-id="8f05c-114">For example, the [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="8f05c-115">Desuden returnerer det [brugerdefinerede](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M"-format måneden fra 1 til 12, mens det brugerdefinerede "m"-format returnerer minuttallet fra 0 til og med 59.</span><span class="sxs-lookup"><span data-stu-id="8f05c-115">Additionally, the [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="8f05c-116">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="8f05c-116">`culture`: *String*</span></span>

<span data-ttu-id="8f05c-117">Den kultur, du vil bruge til formatering.</span><span class="sxs-lookup"><span data-stu-id="8f05c-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="8f05c-118">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="8f05c-118">Return values</span></span>

<span data-ttu-id="8f05c-119">*Streng*</span><span class="sxs-lookup"><span data-stu-id="8f05c-119">*String*</span></span>

<span data-ttu-id="8f05c-120">Den resulterende strengværdi.</span><span class="sxs-lookup"><span data-stu-id="8f05c-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8f05c-121">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="8f05c-121">Usage notes</span></span>

<span data-ttu-id="8f05c-122">Hvis kulturen ikke er defineret som et argument for den kaldte funktion, er værdien af `culture` defineret af den kaldende kontekst.</span><span class="sxs-lookup"><span data-stu-id="8f05c-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="8f05c-123">For eksempel, hvis funktionen `DATEFORMAT` kaldes ved hjælp af syntaks 1 i et elektronisk rapporteringsformat (ER) for et **FIL**-element, der er konfigureret til at bruge den tyske kultur, vil konverteringen ske ved hjælp af den tyske kultur.</span><span class="sxs-lookup"><span data-stu-id="8f05c-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="8f05c-124">Standardværdien for `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="8f05c-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="8f05c-125">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="8f05c-125">Example 1</span></span>

<span data-ttu-id="8f05c-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returnerer den aktuelle dato-/klokkeslætsværdi på programserver, 24. december 2015, som strengen **"24-12-2015"**, baseret på det angivne brugerdefinerede format.</span><span class="sxs-lookup"><span data-stu-id="8f05c-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="8f05c-127">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="8f05c-127">Example 2</span></span>

<span data-ttu-id="8f05c-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returnerer datoen for den aktuelle programsession, 24. december 2015, som strengen **"24-12-2015"**, baseret på den valgte tyske kultur og det angivne format.</span><span class="sxs-lookup"><span data-stu-id="8f05c-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8f05c-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8f05c-129">Additional resources</span></span>

[<span data-ttu-id="8f05c-130">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="8f05c-130">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]