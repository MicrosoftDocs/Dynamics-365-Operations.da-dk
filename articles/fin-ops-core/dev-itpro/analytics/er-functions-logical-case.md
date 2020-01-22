---
title: ER-funktionen CASE
description: Dette emne indeholder oplysninger om, hvordan funktionen CASE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 38b51a4d8bf8dc997bae2ae9206d8e71ca48dec6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916056"
---
# <span data-ttu-id="2718c-103"><a name="CASE">ER-funktionen CASE</a></span><span class="sxs-lookup"><span data-stu-id="2718c-103"><a name="CASE">CASE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2718c-104">Funktionen `CASE` evaluerer værdien af det angivne udtryk i forhold til de angivne alternative indstillinger og returnerer resultatet af den første indstilling, der er lig med værdien af det angivne udtryk.</span><span class="sxs-lookup"><span data-stu-id="2718c-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="2718c-105">Ellers returneres det valgfrie standardresultat, hvis der er angivet et standardresultat som det sidste argument i den kaldte funktion, hvor der ikke er foretaget en forudgående indstilling.</span><span class="sxs-lookup"><span data-stu-id="2718c-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="2718c-106">Den returnerede værdi kan være en værdi for en hvilken som helst af de understøttede datatyper.</span><span class="sxs-lookup"><span data-stu-id="2718c-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="2718c-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="2718c-107">Syntax</span></span>

```
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="2718c-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="2718c-108">Arguments</span></span>

<span data-ttu-id="2718c-109">`expression`: *Primitiv datatype* (Boolesk, numerisk eller tekst)</span><span class="sxs-lookup"><span data-stu-id="2718c-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="2718c-110">Et gyldigt udtryk, der returnerer en værdi af den primitive datatype.</span><span class="sxs-lookup"><span data-stu-id="2718c-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="2718c-111">`option 1`: *Primitiv datatype* (Boolesk, numerisk eller tekst)</span><span class="sxs-lookup"><span data-stu-id="2718c-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="2718c-112">Et gyldigt udtryk, der returnerer en værdi af samme primitive datatype som argumentet `expression` for den kaldte funktion.</span><span class="sxs-lookup"><span data-stu-id="2718c-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="2718c-113">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="2718c-113">This argument is required.</span></span>

<span data-ttu-id="2718c-114">`result 1`: *Alle understøttede datatyper*</span><span class="sxs-lookup"><span data-stu-id="2718c-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="2718c-115">Det returnerede resultat, der svarer til den foregående indstilling.</span><span class="sxs-lookup"><span data-stu-id="2718c-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="2718c-116">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="2718c-116">This argument is required.</span></span>

<span data-ttu-id="2718c-117">`option N`: *Primitiv datatype* (Boolesk, numerisk eller tekst)</span><span class="sxs-lookup"><span data-stu-id="2718c-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="2718c-118">Et gyldigt udtryk, der returnerer en værdi af samme primitive datatype som argumentet `expression` for den kaldte funktion.</span><span class="sxs-lookup"><span data-stu-id="2718c-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="2718c-119">Dette argument er valgfrit.</span><span class="sxs-lookup"><span data-stu-id="2718c-119">This argument is optional.</span></span>

<span data-ttu-id="2718c-120">`result N`: *Alle understøttede datatyper*</span><span class="sxs-lookup"><span data-stu-id="2718c-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="2718c-121">Det returnerede resultat, der svarer til den foregående indstilling.</span><span class="sxs-lookup"><span data-stu-id="2718c-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="2718c-122">Dette argument er valgfrit.</span><span class="sxs-lookup"><span data-stu-id="2718c-122">This argument is optional.</span></span>

<span data-ttu-id="2718c-123">`default result`: *Alle understøttede datatyper*</span><span class="sxs-lookup"><span data-stu-id="2718c-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="2718c-124">Det resultat, der skal returneres, hvis der ikke er noget match.</span><span class="sxs-lookup"><span data-stu-id="2718c-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="2718c-125">Dette argument er valgfrit.</span><span class="sxs-lookup"><span data-stu-id="2718c-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="2718c-126">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="2718c-126">Return values</span></span>

<span data-ttu-id="2718c-127">*Alle understøttede datatyper*</span><span class="sxs-lookup"><span data-stu-id="2718c-127">*Any of the supported data types*</span></span>

<span data-ttu-id="2718c-128">Den resulterende værdi af en af de understøttede datatyper.</span><span class="sxs-lookup"><span data-stu-id="2718c-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2718c-129">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="2718c-129">Usage notes</span></span>

<span data-ttu-id="2718c-130">Der bliver udløst en undtagelse på kørselstidspunktet, hvis det ikke er et match, og et valgfrit standardresultat ikke er defineret.</span><span class="sxs-lookup"><span data-stu-id="2718c-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="2718c-131">Alle resultater skal angives ved hjælp af den samme datatype.</span><span class="sxs-lookup"><span data-stu-id="2718c-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="2718c-132">Der udløses en undtagelse på designtidspunktet, hvis datatyperne for de konfigurerede resultater ikke matcher.</span><span class="sxs-lookup"><span data-stu-id="2718c-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="2718c-133">Hvis den første resultatværdi og den *N*'te resultatværdi er værdier af datatypen *Container (post)* eller *Postliste*, indeholder resultatet kun de felter, der findes i begge værdier.</span><span class="sxs-lookup"><span data-stu-id="2718c-133">If the first result value and the *N*th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="2718c-134">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2718c-134">Example</span></span>

<span data-ttu-id="2718c-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returnerer strengen **"VINTER"**, hvis den aktuelle dato for programsessionen er mellem oktober og december.</span><span class="sxs-lookup"><span data-stu-id="2718c-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="2718c-136">Ellers returneres en tom streng.</span><span class="sxs-lookup"><span data-stu-id="2718c-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2718c-137">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2718c-137">Additional resources</span></span>

[<span data-ttu-id="2718c-138">Logiske funktioner</span><span class="sxs-lookup"><span data-stu-id="2718c-138">Logical functions</span></span>](er-functions-category-logical.md)
