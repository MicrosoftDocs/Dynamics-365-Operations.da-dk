---
title: ER-funktionen CONCATENATE
description: Dette emne indeholder oplysninger om, hvordan funktionen CONCATENATE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 6e4800ce44d9da07818acec55c50224a9a000fe6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569599"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="edca3-103">ER-funktionen CONCATENATE</span><span class="sxs-lookup"><span data-stu-id="edca3-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="edca3-104">Funktionen `CONCATENATE` returnerer alle de angivne tekststrenge som en *Streng*-værdi, når de er blevet sammenkædet i en streng.</span><span class="sxs-lookup"><span data-stu-id="edca3-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="edca3-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="edca3-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="edca3-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="edca3-106">Arguments</span></span>

<span data-ttu-id="edca3-107">`text 1`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="edca3-107">`text 1`: *String*</span></span>

<span data-ttu-id="edca3-108">En reference til en datakilde af datatypen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="edca3-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="edca3-109">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="edca3-109">This argument is required.</span></span>

<span data-ttu-id="edca3-110">`text N`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="edca3-110">`text N`: *String*</span></span>

<span data-ttu-id="edca3-111">En reference til en datakilde af datatypen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="edca3-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="edca3-112">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="edca3-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="edca3-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="edca3-113">Return values</span></span>

<span data-ttu-id="edca3-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="edca3-114">*String*</span></span>

<span data-ttu-id="edca3-115">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="edca3-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="edca3-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="edca3-116">Example</span></span>

<span data-ttu-id="edca3-117">`CONCATENATE ("abc", "def")` returnerer **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="edca3-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="edca3-118">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="edca3-118">Usage notes</span></span>

<span data-ttu-id="edca3-119">Udtrykket `"abc" & "def"` returnerer også **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="edca3-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="edca3-120">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="edca3-120">Additional resources</span></span>

[<span data-ttu-id="edca3-121">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="edca3-121">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]