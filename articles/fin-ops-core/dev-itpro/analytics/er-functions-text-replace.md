---
title: ER-funktionen REPLACE
description: Dette emne indeholder oplysninger om, hvordan funktionen REPLACE til elektronisk rapportering (ER) skal anvendes.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c9d3b6748ecb1680586a2d47a425b5ef98551f1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682912"
---
# <a name="replace-er-function"></a><span data-ttu-id="7d133-103">ER-funktionen REPLACE</span><span class="sxs-lookup"><span data-stu-id="7d133-103">REPLACE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d133-104">Funktionen `REPLACE` returnerer den angivne tekststreng som en *Streng*-værdi, efter at hele eller en del af den er blevet erstattet med en anden streng.</span><span class="sxs-lookup"><span data-stu-id="7d133-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d133-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="7d133-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="7d133-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="7d133-106">Arguments</span></span>

<span data-ttu-id="7d133-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="7d133-107">`text`: *String*</span></span>

<span data-ttu-id="7d133-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="7d133-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="7d133-109">`pattern`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="7d133-109">`pattern`: *String*</span></span>

<span data-ttu-id="7d133-110">Hvis argumentet `regular expression flag` er **FALSK**, indeholder argumentet den tekst, der skal udskiftes.</span><span class="sxs-lookup"><span data-stu-id="7d133-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="7d133-111">Hvis argumentet `regular expression flag` er **SANDT**, indeholder dette argument et regulært udtryk, der definerer både et søgemønster og erstatningsteksten.</span><span class="sxs-lookup"><span data-stu-id="7d133-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="7d133-112">`replacement`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="7d133-112">`replacement`: *String*</span></span>

<span data-ttu-id="7d133-113">Hvis argumentet `regular expression flag` er **FALSK**, indeholder argumentet den tekst, der anvendes i stedet for.</span><span class="sxs-lookup"><span data-stu-id="7d133-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="7d133-114">Hvis argumentet `regular expression flag` er **SANDT**, bruges dette argument ikke.</span><span class="sxs-lookup"><span data-stu-id="7d133-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="7d133-115">`regular expression flag`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="7d133-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="7d133-116">En *Boolesk* værdi, der angiver, om et regulært udtryk bruges til at udføre erstatningen.</span><span class="sxs-lookup"><span data-stu-id="7d133-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="7d133-117">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="7d133-117">Return values</span></span>

<span data-ttu-id="7d133-118">*Streng*</span><span class="sxs-lookup"><span data-stu-id="7d133-118">*String*</span></span>

<span data-ttu-id="7d133-119">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="7d133-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7d133-120">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="7d133-120">Usage notes</span></span>

<span data-ttu-id="7d133-121">Hvis argumentet `regular expression flag` er **SANDT**, returnerer denne funktion den angivne streng, når den er blevet ændret, ved at anvende det regulære udtryk, der er angivet af argumentet `pattern`.</span><span class="sxs-lookup"><span data-stu-id="7d133-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="7d133-122">Dette regulære udtryk bruges til at søge efter de tegn, der skal erstattes.</span><span class="sxs-lookup"><span data-stu-id="7d133-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="7d133-123">Hvis argumentet `regular expression flag`er **FALSE**, returnerer denne funktion den angivne streng, efter at det sæt tegn, der er defineret i argumentet `pattern`, er erstattet af tegn i argumentet `replacement`.</span><span class="sxs-lookup"><span data-stu-id="7d133-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="7d133-124">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="7d133-124">Example 1</span></span>

<span data-ttu-id="7d133-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` anvender et almindeligt udtryk, der fjerner alle ikke-numeriske symboler og returnerer **"19234564971"**.</span><span class="sxs-lookup"><span data-stu-id="7d133-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="7d133-126">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="7d133-126">Example 2</span></span>

<span data-ttu-id="7d133-127">`REPLACE ("abcdef", "cd", "GH", false)` erstatter mønsteret **"cd"** med strengen **"GH"** og returnerer **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="7d133-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d133-128">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7d133-128">Additional resources</span></span>

[<span data-ttu-id="7d133-129">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="7d133-129">Text functions</span></span>](er-functions-category-text.md)
