---
title: ER-funktionen TRANSLATE
description: Dette emne indeholder oplysninger om, hvordan funktionen TRANSLATE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 51b9a2e25a9f1dfc08e9e0f7fc3ad84b359a6d1b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744233"
---
# <a name="translate-er-function"></a><span data-ttu-id="13501-103">ER-funktionen TRANSLATE</span><span class="sxs-lookup"><span data-stu-id="13501-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13501-104">Funktionen `TRANSLATE` returnerer en *Streng*-værdi, der indeholder resultatet af tegnerstatningen af den angivne tekst i tegn for et andet angivet sæt tegn.</span><span class="sxs-lookup"><span data-stu-id="13501-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="13501-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="13501-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="13501-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="13501-106">Arguments</span></span>

<span data-ttu-id="13501-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="13501-107">`text`: *String*</span></span>

<span data-ttu-id="13501-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="13501-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="13501-109">`pattern`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="13501-109">`pattern`: *String*</span></span>

<span data-ttu-id="13501-110">Den tekst, der skal erstattes.</span><span class="sxs-lookup"><span data-stu-id="13501-110">The text that must be replaced.</span></span>

<span data-ttu-id="13501-111">`replacement`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="13501-111">`replacement`: *String*</span></span>

<span data-ttu-id="13501-112">Den tekst, der skal bruges som erstatning.</span><span class="sxs-lookup"><span data-stu-id="13501-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="13501-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="13501-113">Return values</span></span>

<span data-ttu-id="13501-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="13501-114">*String*</span></span>

<span data-ttu-id="13501-115">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="13501-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="13501-116">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="13501-116">Usage notes</span></span>

<span data-ttu-id="13501-117">Funktionen `TRANSLATE` erstatter ét tegn ad gangen.</span><span class="sxs-lookup"><span data-stu-id="13501-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="13501-118">Funktionen erstatter det første tegn i argumentet `text`med det første tegn i argumentet `pattern` og derefter det andet tegn og følger det samme forløb, indtil det er afsluttet.</span><span class="sxs-lookup"><span data-stu-id="13501-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="13501-119">Når et tegn fra argumenterne `text` og `pattern` matcher, erstattes det af et tegn fra argumentet `replacement`, der er placeret i samme position som tegnet fra argumentet `pattern`.</span><span class="sxs-lookup"><span data-stu-id="13501-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="13501-120">Hvis et tegn vises flere gange i argumentet `pattern`, bruges den `replacement`-argumenttilknytning, der svarer til den første forekomst af dette tegn.</span><span class="sxs-lookup"><span data-stu-id="13501-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="13501-121">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="13501-121">Example 1</span></span>

<span data-ttu-id="13501-122">`TRANSLATE ("abcdef", "cd", "GH")` erstatter tegnet **C**-tegnet i den angivne **"abcdef-**-tekst med tegnet **" G "** i `replacement`-teksten på grund af følgende:</span><span class="sxs-lookup"><span data-stu-id="13501-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="13501-123">Tegnet **"C"** vises i `pattern`-teksten i første position.</span><span class="sxs-lookup"><span data-stu-id="13501-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="13501-124">Den første position af `replacement`-teksten indeholder tegnet **"G"**.</span><span class="sxs-lookup"><span data-stu-id="13501-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="13501-125">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="13501-125">Example 2</span></span>

<span data-ttu-id="13501-126">`TRANSLATE ("abcdef", "ccd", "GH")` returnerer **"abGdef"**.</span><span class="sxs-lookup"><span data-stu-id="13501-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="13501-127">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="13501-127">Example 3</span></span>

<span data-ttu-id="13501-128">`TRANSLATE ("abccba", "abc", "123")` returnerer **"123321"**.</span><span class="sxs-lookup"><span data-stu-id="13501-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13501-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="13501-129">Additional resources</span></span>

[<span data-ttu-id="13501-130">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="13501-130">Text functions</span></span>](er-functions-category-text.md)
