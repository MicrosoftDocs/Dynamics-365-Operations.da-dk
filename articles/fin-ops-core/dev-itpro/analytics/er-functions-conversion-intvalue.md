---
title: ER-funktionen INTVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen INTVALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 71eedde5a22f36a8a827824087633de32c00cc7d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755366"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="b6620-103">ER-funktionen INTVALUE</span><span class="sxs-lookup"><span data-stu-id="b6620-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6620-104">Funktionen `INTVALUE` returnerer en *Int*-værdi, der repræsenterer den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="b6620-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b6620-105">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="b6620-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="b6620-106">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="b6620-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="b6620-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="b6620-107">Arguments</span></span>

<span data-ttu-id="b6620-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="b6620-108">`text`: *String*</span></span>

<span data-ttu-id="b6620-109">En tekstværdi, der skal konverteres til et *Int*-tal.</span><span class="sxs-lookup"><span data-stu-id="b6620-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="b6620-110">`number`: *Reel* eller *Heltal*</span><span class="sxs-lookup"><span data-stu-id="b6620-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="b6620-111">En numerisk *Reel* værdi eller *Heltals*-værdi, der skal konverteres til et *Int*-tal.</span><span class="sxs-lookup"><span data-stu-id="b6620-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="b6620-112">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="b6620-112">Return values</span></span>

<span data-ttu-id="b6620-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="b6620-113">*Int*</span></span>

<span data-ttu-id="b6620-114">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="b6620-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b6620-115">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="b6620-115">Usage notes</span></span>

<span data-ttu-id="b6620-116">Eventuelle decimalpladser afkortes.</span><span class="sxs-lookup"><span data-stu-id="b6620-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="b6620-117">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="b6620-117">Example 1</span></span>

<span data-ttu-id="b6620-118">`INTVALUE ("100.77")` returnerer værdien *Int* **100**.</span><span class="sxs-lookup"><span data-stu-id="b6620-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b6620-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="b6620-119">Example 2</span></span>

<span data-ttu-id="b6620-120">`INTVALUE (-100.77)` returnerer værdien *Int* **-100**.</span><span class="sxs-lookup"><span data-stu-id="b6620-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6620-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b6620-121">Additional resources</span></span>

[<span data-ttu-id="b6620-122">Typekonverteringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="b6620-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]