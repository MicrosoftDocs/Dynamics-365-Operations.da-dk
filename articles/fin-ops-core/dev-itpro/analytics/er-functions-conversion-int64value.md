---
title: ER-funktionen INT64VALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen INT64VALUE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 9db2e9abcac36a8331a494c886218bbfc82e93aa
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561488"
---
# <a name="int64value-er-function"></a><span data-ttu-id="3a103-103">ER-funktionen INT64VALUE</span><span class="sxs-lookup"><span data-stu-id="3a103-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a103-104">Funktionen `INT64VALUE` returnerer en *Int64*-værdi, der repræsenterer den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="3a103-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="3a103-105">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="3a103-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="3a103-106">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="3a103-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="3a103-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="3a103-107">Arguments</span></span>

<span data-ttu-id="3a103-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="3a103-108">`text`: *String*</span></span>

<span data-ttu-id="3a103-109">En tekstværdi, der skal konverteres til et *Int64*-tal.</span><span class="sxs-lookup"><span data-stu-id="3a103-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="3a103-110">`number`: *Reel* eller *Heltal*</span><span class="sxs-lookup"><span data-stu-id="3a103-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="3a103-111">En numerisk *Reel* værdi eller *Heltals*-værdi, der skal konverteres til et *Int64*-tal.</span><span class="sxs-lookup"><span data-stu-id="3a103-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="3a103-112">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="3a103-112">Return values</span></span>

<span data-ttu-id="3a103-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="3a103-113">*Int64*</span></span>

<span data-ttu-id="3a103-114">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="3a103-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3a103-115">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="3a103-115">Usage notes</span></span>

<span data-ttu-id="3a103-116">Eventuelle decimalpladser afkortes.</span><span class="sxs-lookup"><span data-stu-id="3a103-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="3a103-117">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="3a103-117">Example 1</span></span>

<span data-ttu-id="3a103-118">`INT64VALUE ("22565422744")` returnerer værdien *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="3a103-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="3a103-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="3a103-119">Example 2</span></span>

<span data-ttu-id="3a103-120">`INT64VALUE ( VALUE("22565422744.77"))` returnerer værdien *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="3a103-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a103-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3a103-121">Additional resources</span></span>

[<span data-ttu-id="3a103-122">Typekonverteringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="3a103-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]