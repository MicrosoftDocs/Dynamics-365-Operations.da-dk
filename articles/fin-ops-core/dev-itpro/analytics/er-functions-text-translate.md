---
title: ER-funktionen TRANSLATE
description: Dette emne indeholder oplysninger om, hvordan funktionen TRANSLATE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 11954f3e48d8dc2257b3a0bc8768df47af3c5c0c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916700"
---
# <span data-ttu-id="9f9b1-103"><a name="TRANSLATE">ER-funktionen TRANSLATE</a></span><span class="sxs-lookup"><span data-stu-id="9f9b1-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f9b1-104">Funktionen `TRANSLATE` returnerer den angivne tekststreng som en *Streng*-værdi, efter at hele eller en del af den er blevet erstattet med en anden streng.</span><span class="sxs-lookup"><span data-stu-id="9f9b1-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f9b1-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="9f9b1-105">Syntax</span></span>

```
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="9f9b1-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="9f9b1-106">Arguments</span></span>

<span data-ttu-id="9f9b1-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="9f9b1-107">`text`: *String*</span></span>

<span data-ttu-id="9f9b1-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="9f9b1-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="9f9b1-109">`pattern`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="9f9b1-109">`pattern`: *String*</span></span>

<span data-ttu-id="9f9b1-110">Den tekst, der skal erstattes.</span><span class="sxs-lookup"><span data-stu-id="9f9b1-110">The text that must be replaced.</span></span>

<span data-ttu-id="9f9b1-111">`replacement`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="9f9b1-111">`replacement`: *String*</span></span>

<span data-ttu-id="9f9b1-112">Den tekst, der skal bruges som erstatning.</span><span class="sxs-lookup"><span data-stu-id="9f9b1-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="9f9b1-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="9f9b1-113">Return values</span></span>

<span data-ttu-id="9f9b1-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="9f9b1-114">*String*</span></span>

<span data-ttu-id="9f9b1-115">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="9f9b1-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9f9b1-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="9f9b1-116">Example</span></span>

<span data-ttu-id="9f9b1-117">`TRANSLATE ("abcdef", "cd", "GH")` erstatter mønsteret **"cd"** med strengen **"GH"** og returnerer **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="9f9b1-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9f9b1-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9f9b1-118">Additional resources</span></span>

[<span data-ttu-id="9f9b1-119">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="9f9b1-119">Text functions</span></span>](er-functions-category-text.md)
