---
title: ER-funktionen DATETIMEFORMAT
description: Dette emne indeholder oplysninger om, hvordan funktionen DATETIMEFORMAT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: b7516620763e87440c0fb866ce507c744223a229
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563624"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="f885e-103">ER-funktionen DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="f885e-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f885e-104">Funktionen `DATETIMEFORMAT` returnerer en *Streng*-værdi, som præsenterer en given dato-/klokkeslætsværdi som tekst i det angivne format og i en eventuelt angivet [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="f885e-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="f885e-105">Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="f885e-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="f885e-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="f885e-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="f885e-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="f885e-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="f885e-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="f885e-108">Arguments</span></span>

<span data-ttu-id="f885e-109">`datetime`: *DatoKlokkeslæt*</span><span class="sxs-lookup"><span data-stu-id="f885e-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="f885e-110">En dato-/klokkeslætsværdi, der repræsenterer den dato og det klokkeslæt, der skal formateres.</span><span class="sxs-lookup"><span data-stu-id="f885e-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="f885e-111">`format`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="f885e-111">`format`: *String*</span></span>

<span data-ttu-id="f885e-112">Outputstrengens format.</span><span class="sxs-lookup"><span data-stu-id="f885e-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="f885e-113">Der skelnes mellem store og små bogstaver i formatstrengen, når du enten bruger et standardformat eller et brugerdefineret format.</span><span class="sxs-lookup"><span data-stu-id="f885e-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="f885e-114">F.eks. returnerer [standardformatet](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" datoen ved at bruge det korte datomønster, mens standardformatet "D" returnerer datoen ved at bruge det lange datomønster.</span><span class="sxs-lookup"><span data-stu-id="f885e-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="f885e-115">Desuden returnerer det [brugerdefinerede](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M"-format måneden fra 1 til 12, mens det brugerdefinerede "m"-format returnerer minuttallet fra 0 til og med 59.</span><span class="sxs-lookup"><span data-stu-id="f885e-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="f885e-116">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="f885e-116">`culture`: *String*</span></span>

<span data-ttu-id="f885e-117">Den kultur, du vil bruge til formatering.</span><span class="sxs-lookup"><span data-stu-id="f885e-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="f885e-118">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="f885e-118">Return values</span></span>

<span data-ttu-id="f885e-119">*Streng*</span><span class="sxs-lookup"><span data-stu-id="f885e-119">*String*</span></span>

<span data-ttu-id="f885e-120">Den resulterende strengværdi.</span><span class="sxs-lookup"><span data-stu-id="f885e-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f885e-121">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="f885e-121">Usage notes</span></span>

<span data-ttu-id="f885e-122">Hvis kulturen ikke er defineret som et argument for den kaldte funktion, er værdien af `culture` defineret af den kaldende kontekst.</span><span class="sxs-lookup"><span data-stu-id="f885e-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="f885e-123">For eksempel, hvis funktionen `DATETIMEFORMAT` kaldes ved hjælp af syntaks 1 i et elektronisk rapporteringsformat (ER) for et **FIL**-element, der er konfigureret til at bruge den tyske kultur, vil konverteringen ske ved hjælp af den tyske kultur.</span><span class="sxs-lookup"><span data-stu-id="f885e-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="f885e-124">Standardværdien for `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="f885e-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="f885e-125">Når funktionen `DATETIMEFORMAT` konverterer en given dato-/klokkeslætsværdi, tages den tidszoneindstillingen for den programbruger, der kører ER-formatet, som funktionen kaldes i sammenhæng med i betragtning.</span><span class="sxs-lookup"><span data-stu-id="f885e-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="f885e-126">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="f885e-126">Example 1</span></span>

<span data-ttu-id="f885e-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returnerer den aktuelle dato-/klokkeslætsværdi på programserver, 24. december 2015, som **"24-12-2015"**, baseret på det angivne brugerdefinerede format.</span><span class="sxs-lookup"><span data-stu-id="f885e-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="f885e-128">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="f885e-128">Example 2</span></span>

<span data-ttu-id="f885e-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returnerer datoen/klokkeslættet for den aktuelle programsession, 24. december 2015, som strengen **"24.12.2015"**, baseret på den valgte tyske kultur og det angivne format.</span><span class="sxs-lookup"><span data-stu-id="f885e-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="f885e-130">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="f885e-130">Example 3</span></span>

<span data-ttu-id="f885e-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returnerer strengværdien **2019-11-12T08:00:00.0000000-08:00**, når funktionen kaldes under en proces, der blev initieret af en programbruger, der har tidszoneværdien **(GMT-08:00) Pacific Time (USA og Canada)** i afsnittet **Sprog og land/område-præferencer**.</span><span class="sxs-lookup"><span data-stu-id="f885e-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f885e-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f885e-132">Additional resources</span></span>

[<span data-ttu-id="f885e-133">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="f885e-133">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]