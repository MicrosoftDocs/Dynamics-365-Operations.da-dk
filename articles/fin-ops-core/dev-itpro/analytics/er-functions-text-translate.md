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
ms.openlocfilehash: 07fe19c5f66c33e336f76f3a72d3bbda0c7e8d86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040911"
---
# <span data-ttu-id="ee3f8-103"><a name="TRANSLATE">ER-funktionen TRANSLATE</a></span><span class="sxs-lookup"><span data-stu-id="ee3f8-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee3f8-104">Funktionen `TRANSLATE` returnerer den angivne tekststreng som en *Streng*-værdi, efter at hele eller en del af den er blevet erstattet med en anden streng.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee3f8-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="ee3f8-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="ee3f8-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="ee3f8-106">Arguments</span></span>

<span data-ttu-id="ee3f8-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ee3f8-107">`text`: *String*</span></span>

<span data-ttu-id="ee3f8-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="ee3f8-109">`pattern`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ee3f8-109">`pattern`: *String*</span></span>

<span data-ttu-id="ee3f8-110">Den tekst, der skal erstattes.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-110">The text that must be replaced.</span></span>

<span data-ttu-id="ee3f8-111">`replacement`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ee3f8-111">`replacement`: *String*</span></span>

<span data-ttu-id="ee3f8-112">Den tekst, der skal bruges som erstatning.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="ee3f8-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="ee3f8-113">Return values</span></span>

<span data-ttu-id="ee3f8-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ee3f8-114">*String*</span></span>

<span data-ttu-id="ee3f8-115">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="ee3f8-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ee3f8-116">Example</span></span>

<span data-ttu-id="ee3f8-117">`TRANSLATE ("abcdef", "cd", "GH")` erstatter mønsteret **"cd"** med strengen **"GH"** og returnerer **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ee3f8-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ee3f8-118">Additional resources</span></span>

[<span data-ttu-id="ee3f8-119">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="ee3f8-119">Text functions</span></span>](er-functions-category-text.md)
