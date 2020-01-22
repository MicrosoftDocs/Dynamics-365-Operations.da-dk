---
title: ER-funktionen REPLACE
description: Dette emne indeholder oplysninger om, hvordan funktionen REPLACE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: d9c66f4c96f35e3ad5fc92e7925b5cd07c956aac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916861"
---
# <span data-ttu-id="85d87-103"><a name="REPLACE">ER-funktionen REPLACE</a></span><span class="sxs-lookup"><span data-stu-id="85d87-103"><a name="REPLACE">REPLACE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85d87-104">Funktionen `REPLACE` returnerer den angivne tekststreng som en *Streng*-værdi, efter at hele eller en del af den er blevet erstattet med en anden streng.</span><span class="sxs-lookup"><span data-stu-id="85d87-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="85d87-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="85d87-105">Syntax</span></span>

```
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="85d87-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="85d87-106">Arguments</span></span>

<span data-ttu-id="85d87-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="85d87-107">`text`: *String*</span></span>

<span data-ttu-id="85d87-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="85d87-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="85d87-109">`pattern`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="85d87-109">`pattern`: *String*</span></span>

<span data-ttu-id="85d87-110">Hvis argumentet `regular expression flag` er **FALSK**, indeholder argumentet den tekst, der skal udskiftes.</span><span class="sxs-lookup"><span data-stu-id="85d87-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="85d87-111">Hvis argumentet `regular expression flag` er **SANDT**, indeholder dette argument et regulært udtryk, der definerer både et søgemønster og erstatningsteksten.</span><span class="sxs-lookup"><span data-stu-id="85d87-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="85d87-112">`replacement`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="85d87-112">`replacement`: *String*</span></span>

<span data-ttu-id="85d87-113">Hvis argumentet `regular expression flag` er **FALSK**, indeholder argumentet den tekst, der anvendes i stedet for.</span><span class="sxs-lookup"><span data-stu-id="85d87-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="85d87-114">Hvis argumentet `regular expression flag` er **SANDT**, bruges dette argument ikke.</span><span class="sxs-lookup"><span data-stu-id="85d87-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="85d87-115">`regular expression flag`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="85d87-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="85d87-116">En *Boolesk* værdi, der angiver, om et regulært udtryk bruges til at udføre erstatningen.</span><span class="sxs-lookup"><span data-stu-id="85d87-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="85d87-117">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="85d87-117">Return values</span></span>

<span data-ttu-id="85d87-118">*Streng*</span><span class="sxs-lookup"><span data-stu-id="85d87-118">*String*</span></span>

<span data-ttu-id="85d87-119">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="85d87-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="85d87-120">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="85d87-120">Usage notes</span></span>

<span data-ttu-id="85d87-121">Hvis argumentet `regular expression flag` er **SANDT**, returnerer denne funktion den angivne streng, når den er blevet ændret, ved at anvende det regulære udtryk, der er angivet af argumentet `pattern`.</span><span class="sxs-lookup"><span data-stu-id="85d87-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="85d87-122">Dette regulære udtryk bruges til at søge efter de tegn, der skal erstattes.</span><span class="sxs-lookup"><span data-stu-id="85d87-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="85d87-123">Hvis argumentet `regular expression flag` er **FALSK**, opfører denne funktion sig som [TRANSLATE](er-functions-text-translate.md).</span><span class="sxs-lookup"><span data-stu-id="85d87-123">If the `regular expression flag` argument is **FALSE**, this function behaves like [TRANSLATE](er-functions-text-translate.md).</span></span> <span data-ttu-id="85d87-124">De tegn, der er angivet af argumentet `replacement`, anvendes til at erstatte de tegn, der findes.</span><span class="sxs-lookup"><span data-stu-id="85d87-124">The characters that are specified by the `replacement` argument are used to replace the characters that are found.</span></span> 

## <a name="example-1"></a><span data-ttu-id="85d87-125">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="85d87-125">Example 1</span></span>

<span data-ttu-id="85d87-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` anvender et almindeligt udtryk, der fjerner alle ikke-numeriske symboler og returnerer **"19234564971"**.</span><span class="sxs-lookup"><span data-stu-id="85d87-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="85d87-127">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="85d87-127">Example 2</span></span>

<span data-ttu-id="85d87-128">`REPLACE ("abcdef", "cd", "GH", false)` erstatter mønsteret **"cd"** med strengen **"GH"** og returnerer **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="85d87-128">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85d87-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="85d87-129">Additional resources</span></span>

[<span data-ttu-id="85d87-130">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="85d87-130">Text functions</span></span>](er-functions-category-text.md)
