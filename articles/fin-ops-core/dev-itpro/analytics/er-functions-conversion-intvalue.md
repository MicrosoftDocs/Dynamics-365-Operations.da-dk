---
title: ER-funktionen INTVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen INTVALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 64f43ad29d59ade1e124b6800734b003f6ca07df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561464"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="2f1f2-103">ER-funktionen INTVALUE</span><span class="sxs-lookup"><span data-stu-id="2f1f2-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f1f2-104">Funktionen `INTVALUE` returnerer en *Int*-værdi, der repræsenterer den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="2f1f2-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="2f1f2-105">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="2f1f2-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="2f1f2-106">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="2f1f2-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="2f1f2-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="2f1f2-107">Arguments</span></span>

<span data-ttu-id="2f1f2-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="2f1f2-108">`text`: *String*</span></span>

<span data-ttu-id="2f1f2-109">En tekstværdi, der skal konverteres til et *Int*-tal.</span><span class="sxs-lookup"><span data-stu-id="2f1f2-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="2f1f2-110">`number`: *Reel* eller *Heltal*</span><span class="sxs-lookup"><span data-stu-id="2f1f2-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="2f1f2-111">En numerisk *Reel* værdi eller *Heltals*-værdi, der skal konverteres til et *Int*-tal.</span><span class="sxs-lookup"><span data-stu-id="2f1f2-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="2f1f2-112">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="2f1f2-112">Return values</span></span>

<span data-ttu-id="2f1f2-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="2f1f2-113">*Int*</span></span>

<span data-ttu-id="2f1f2-114">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="2f1f2-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2f1f2-115">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="2f1f2-115">Usage notes</span></span>

<span data-ttu-id="2f1f2-116">Eventuelle decimalpladser afkortes.</span><span class="sxs-lookup"><span data-stu-id="2f1f2-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="2f1f2-117">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="2f1f2-117">Example 1</span></span>

<span data-ttu-id="2f1f2-118">`INTVALUE ("100.77")` returnerer værdien *Int* **100**.</span><span class="sxs-lookup"><span data-stu-id="2f1f2-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="2f1f2-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="2f1f2-119">Example 2</span></span>

<span data-ttu-id="2f1f2-120">`INTVALUE (-100.77)` returnerer værdien *Int* **-100**.</span><span class="sxs-lookup"><span data-stu-id="2f1f2-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f1f2-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2f1f2-121">Additional resources</span></span>

[<span data-ttu-id="2f1f2-122">Typekonverteringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="2f1f2-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]