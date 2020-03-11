---
title: ER-funktionen NUMBERVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen NUMBERVALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 6eeb66f4206eb39141a5b2573fcb9d15428ae52a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042642"
---
# <span data-ttu-id="aaa72-103"><a name="NUMBERVALUE">ER-funktionen NUMBERVALUE</a></span><span class="sxs-lookup"><span data-stu-id="aaa72-103"><a name="NUMBERVALUE">NUMBERVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aaa72-104">Funktionen `NUMBERVALUE` returnerer en *Reel* værdi, der konverteres fra den angivne *Streng*-værdi.</span><span class="sxs-lookup"><span data-stu-id="aaa72-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="aaa72-105">Under konverteringen tages de specificerede decimal- og ciffergrupperingsseparatorer i betragtning.</span><span class="sxs-lookup"><span data-stu-id="aaa72-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaa72-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="aaa72-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="aaa72-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="aaa72-107">Arguments</span></span>

<span data-ttu-id="aaa72-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="aaa72-108">`text`: *String*</span></span>

<span data-ttu-id="aaa72-109">En tekstværdi, der skal konverteres til et *Reelt* tal.</span><span class="sxs-lookup"><span data-stu-id="aaa72-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="aaa72-110">`decimal separator`: Streng</span><span class="sxs-lookup"><span data-stu-id="aaa72-110">`decimal separator`: String</span></span>

<span data-ttu-id="aaa72-111">En decimalseparator.</span><span class="sxs-lookup"><span data-stu-id="aaa72-111">A decimal separator.</span></span> <span data-ttu-id="aaa72-112">Det bruges til at adskille heltal og brøkdele af et decimaltal.</span><span class="sxs-lookup"><span data-stu-id="aaa72-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="aaa72-113">`digit grouping separator`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="aaa72-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="aaa72-114">En ciffergrupperingsseparator.</span><span class="sxs-lookup"><span data-stu-id="aaa72-114">A digit grouping separator.</span></span> <span data-ttu-id="aaa72-115">Det bruges som tusindtalsseparator.</span><span class="sxs-lookup"><span data-stu-id="aaa72-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="aaa72-116">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="aaa72-116">Return values</span></span>

<span data-ttu-id="aaa72-117">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="aaa72-117">*Real*</span></span>

<span data-ttu-id="aaa72-118">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="aaa72-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="aaa72-119">Eksempel</span><span class="sxs-lookup"><span data-stu-id="aaa72-119">Example</span></span>

<span data-ttu-id="aaa72-120">`NUMBERVALUE( "1 234,56", ",", " ")` returnerer **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="aaa72-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aaa72-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="aaa72-121">Additional resources</span></span>

[<span data-ttu-id="aaa72-122">Typekonverteringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="aaa72-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
