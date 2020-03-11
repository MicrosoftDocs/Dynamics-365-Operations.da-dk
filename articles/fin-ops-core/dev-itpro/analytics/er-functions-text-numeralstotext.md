---
title: ER-funktionen NUMERALSTOTEXT
description: Dette emne indeholder oplysninger om, hvordan funktionen NUMERALSTOTEXT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 31fd4076d04ce7d849555bc8301c4d23ad8e1a7e
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041003"
---
# <span data-ttu-id="c48c9-103"><a name="NUMERALSTOTEXT">ER-funktionen NUMERALSTOTEXT</a></span><span class="sxs-lookup"><span data-stu-id="c48c9-103"><a name="NUMERALSTOTEXT">NUMERALSTOTEXT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c48c9-104">Funktionen `NUMERALSTOTEXT` returnerer det angivne tal som en *Streng*-værdi, efter at det er blevet skrevet helt ud (det vil være konverteret til tekststrenge) på det angivne sprog.</span><span class="sxs-lookup"><span data-stu-id="c48c9-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="c48c9-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="c48c9-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="c48c9-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="c48c9-106">Arguments</span></span>

<span data-ttu-id="c48c9-107">`number`: *Heltal* eller *Reel*</span><span class="sxs-lookup"><span data-stu-id="c48c9-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="c48c9-108">En numerisk værdi, der angiver det tal, der skal skrives helt ud.</span><span class="sxs-lookup"><span data-stu-id="c48c9-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="c48c9-109">`language`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="c48c9-109">`language`: *String*</span></span>

<span data-ttu-id="c48c9-110">En *Streng*-værdi, der repræsenterer sprogkoden.</span><span class="sxs-lookup"><span data-stu-id="c48c9-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="c48c9-111">`currency`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="c48c9-111">`currency`: *String*</span></span>

<span data-ttu-id="c48c9-112">En *Streng*-værdi, der repræsenterer valutakoden.</span><span class="sxs-lookup"><span data-stu-id="c48c9-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="c48c9-113">`print currency name flag`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="c48c9-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="c48c9-114">En *Boolesk* værdi, der angiver, om der skal føjes et valutanavn til den tekst, der skrives helt ud.</span><span class="sxs-lookup"><span data-stu-id="c48c9-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="c48c9-115">`decimal points`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="c48c9-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="c48c9-116">En *Heltals*-værdi, der angiver det antal decimaler, som den tekst, der er skrevet helt ud, skal have.</span><span class="sxs-lookup"><span data-stu-id="c48c9-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="c48c9-117">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="c48c9-117">Return values</span></span>

<span data-ttu-id="c48c9-118">*Streng*</span><span class="sxs-lookup"><span data-stu-id="c48c9-118">*String*</span></span>

<span data-ttu-id="c48c9-119">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="c48c9-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c48c9-120">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="c48c9-120">Usage notes</span></span>

<span data-ttu-id="c48c9-121">Sprogkoden er valgfri.</span><span class="sxs-lookup"><span data-stu-id="c48c9-121">The language code is optional.</span></span> <span data-ttu-id="c48c9-122">Hvis den er defineret som en tom streng, bruges sprogkoden for kørselskonteksten.</span><span class="sxs-lookup"><span data-stu-id="c48c9-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="c48c9-123">Standardsprogkoden er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="c48c9-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="c48c9-124">Sprogkoden for den kørende kontekst er defineret i et **Mappe**- eller **Fil**-element i det elektroniske rapporteringsformat (ER), der kører.</span><span class="sxs-lookup"><span data-stu-id="c48c9-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="c48c9-125">Valutakoden er valgfri.</span><span class="sxs-lookup"><span data-stu-id="c48c9-125">The currency code is optional.</span></span> <span data-ttu-id="c48c9-126">Hvis den er defineret som en tom streng, bruges firmavalutaen for kørselskonteksten.</span><span class="sxs-lookup"><span data-stu-id="c48c9-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="c48c9-127">Argumenterne `print currency name flag` og `decimal points` analyseres kun for følgende sprogkoder: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span><span class="sxs-lookup"><span data-stu-id="c48c9-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="c48c9-128">Desuden analyseres argumentet `print currency name flag` kun for virksomheder, hvor landets eller områdets kontekst understøtter afvigelse af valutanavne.</span><span class="sxs-lookup"><span data-stu-id="c48c9-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="c48c9-129">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="c48c9-129">Example 1</span></span>

<span data-ttu-id="c48c9-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returnerer **"Ettusindtohundredeogfireogtredive samt 56"**.</span><span class="sxs-lookup"><span data-stu-id="c48c9-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c48c9-131">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="c48c9-131">Example 2</span></span>

<span data-ttu-id="c48c9-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returnerer **"Sto dwadzieścia"**.</span><span class="sxs-lookup"><span data-stu-id="c48c9-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="c48c9-133">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="c48c9-133">Example 3</span></span>

<span data-ttu-id="c48c9-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returnerer **"сто двадцать евро 21 евроцент"**.</span><span class="sxs-lookup"><span data-stu-id="c48c9-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c48c9-135">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c48c9-135">Additional resources</span></span>

[<span data-ttu-id="c48c9-136">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="c48c9-136">Text functions</span></span>](er-functions-category-text.md)
