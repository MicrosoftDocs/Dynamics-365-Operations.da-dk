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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4293db244d04debf3679cf2bde0b892bd74e8ead
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041118"
---
# <span data-ttu-id="b1694-103"><a name="LEFT">ER-funktionen LEFT</a></span><span class="sxs-lookup"><span data-stu-id="b1694-103"><a name="LEFT">LEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1694-104">Funktionen `LEFT` returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn i begyndelsen af den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="b1694-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1694-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="b1694-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="b1694-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="b1694-106">Arguments</span></span>

<span data-ttu-id="b1694-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="b1694-107">`text`: *String*</span></span>

<span data-ttu-id="b1694-108">En *Streng*-værdi, der repræsenterer den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="b1694-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="b1694-109">`number`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="b1694-109">`number`: *Integer*</span></span>

<span data-ttu-id="b1694-110">Det antal tegn, der skal returneres fra begyndelsen af den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="b1694-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="b1694-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="b1694-111">Return values</span></span>

<span data-ttu-id="b1694-112">*Streng*</span><span class="sxs-lookup"><span data-stu-id="b1694-112">*String*</span></span>

<span data-ttu-id="b1694-113">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="b1694-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b1694-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="b1694-114">Example</span></span>

<span data-ttu-id="b1694-115">`LEFT ("Sample", 3)` returnerer **"Eks"**.</span><span class="sxs-lookup"><span data-stu-id="b1694-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1694-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b1694-116">Additional resources</span></span>

[<span data-ttu-id="b1694-117">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="b1694-117">Text functions</span></span>](er-functions-category-text.md)
