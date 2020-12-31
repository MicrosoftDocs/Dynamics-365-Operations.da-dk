---
title: ER-funktionen LEFT
description: Dette emne indeholder oplysninger om, hvordan funktionen LEFT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 9e9cdff9bb5c22c74803cf17c056c0ff1af5ef43
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685877"
---
# <a name="left-er-function"></a><span data-ttu-id="268a0-103">ER-funktionen LEFT</span><span class="sxs-lookup"><span data-stu-id="268a0-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="268a0-104">Funktionen `LEFT` returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn i begyndelsen af den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="268a0-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="268a0-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="268a0-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="268a0-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="268a0-106">Arguments</span></span>

<span data-ttu-id="268a0-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="268a0-107">`text`: *String*</span></span>

<span data-ttu-id="268a0-108">En *Streng*-værdi, der repræsenterer den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="268a0-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="268a0-109">`number`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="268a0-109">`number`: *Integer*</span></span>

<span data-ttu-id="268a0-110">Det antal tegn, der skal returneres fra begyndelsen af den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="268a0-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="268a0-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="268a0-111">Return values</span></span>

<span data-ttu-id="268a0-112">*Streng*</span><span class="sxs-lookup"><span data-stu-id="268a0-112">*String*</span></span>

<span data-ttu-id="268a0-113">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="268a0-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="268a0-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="268a0-114">Example</span></span>

<span data-ttu-id="268a0-115">`LEFT ("Sample", 3)` returnerer **"Eks"**.</span><span class="sxs-lookup"><span data-stu-id="268a0-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="268a0-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="268a0-116">Additional resources</span></span>

[<span data-ttu-id="268a0-117">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="268a0-117">Text functions</span></span>](er-functions-category-text.md)
