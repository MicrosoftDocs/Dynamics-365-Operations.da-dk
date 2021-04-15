---
title: ER-funktionen REPLACE
description: Dette emne indeholder oplysninger om, hvordan funktionen REPLACE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 04/02/2020
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
ms.openlocfilehash: 21cdd8532730925b7d5c6f5b3bb565dcd365dd6d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746190"
---
# <a name="replace-er-function"></a><span data-ttu-id="17280-103">ER-funktionen REPLACE</span><span class="sxs-lookup"><span data-stu-id="17280-103">REPLACE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17280-104">Funktionen `REPLACE` returnerer den angivne tekststreng som en *Streng*-værdi, efter at hele eller en del af den er blevet erstattet med en anden streng.</span><span class="sxs-lookup"><span data-stu-id="17280-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="17280-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="17280-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="17280-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="17280-106">Arguments</span></span>

<span data-ttu-id="17280-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="17280-107">`text`: *String*</span></span>

<span data-ttu-id="17280-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="17280-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="17280-109">`pattern`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="17280-109">`pattern`: *String*</span></span>

<span data-ttu-id="17280-110">Hvis argumentet `regular expression flag` er **FALSK**, indeholder argumentet den tekst, der skal udskiftes.</span><span class="sxs-lookup"><span data-stu-id="17280-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="17280-111">Hvis argumentet `regular expression flag` er **SANDT**, indeholder dette argument et regulært udtryk, der definerer både et søgemønster og erstatningsteksten.</span><span class="sxs-lookup"><span data-stu-id="17280-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="17280-112">`replacement`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="17280-112">`replacement`: *String*</span></span>

<span data-ttu-id="17280-113">Hvis argumentet `regular expression flag` er **FALSK**, indeholder argumentet den tekst, der anvendes i stedet for.</span><span class="sxs-lookup"><span data-stu-id="17280-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="17280-114">Hvis argumentet `regular expression flag` er **SANDT**, bruges dette argument ikke.</span><span class="sxs-lookup"><span data-stu-id="17280-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="17280-115">`regular expression flag`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="17280-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="17280-116">En *Boolesk* værdi, der angiver, om et regulært udtryk bruges til at udføre erstatningen.</span><span class="sxs-lookup"><span data-stu-id="17280-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="17280-117">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="17280-117">Return values</span></span>

<span data-ttu-id="17280-118">*Streng*</span><span class="sxs-lookup"><span data-stu-id="17280-118">*String*</span></span>

<span data-ttu-id="17280-119">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="17280-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="17280-120">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="17280-120">Usage notes</span></span>

<span data-ttu-id="17280-121">Hvis argumentet `regular expression flag` er **SANDT**, returnerer denne funktion den angivne streng, når den er blevet ændret, ved at anvende det regulære udtryk, der er angivet af argumentet `pattern`.</span><span class="sxs-lookup"><span data-stu-id="17280-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="17280-122">Dette regulære udtryk bruges til at søge efter de tegn, der skal erstattes.</span><span class="sxs-lookup"><span data-stu-id="17280-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="17280-123">Hvis argumentet `regular expression flag`er **FALSE**, returnerer denne funktion den angivne streng, efter at det sæt tegn, der er defineret i argumentet `pattern`, er erstattet af tegn i argumentet `replacement`.</span><span class="sxs-lookup"><span data-stu-id="17280-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="17280-124">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="17280-124">Example 1</span></span>

<span data-ttu-id="17280-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` anvender et almindeligt udtryk, der fjerner alle ikke-numeriske symboler og returnerer **"19234564971"**.</span><span class="sxs-lookup"><span data-stu-id="17280-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="17280-126">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="17280-126">Example 2</span></span>

<span data-ttu-id="17280-127">`REPLACE ("abcdef", "cd", "GH", false)` erstatter mønsteret **"cd"** med strengen **"GH"** og returnerer **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="17280-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17280-128">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="17280-128">Additional resources</span></span>

[<span data-ttu-id="17280-129">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="17280-129">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]