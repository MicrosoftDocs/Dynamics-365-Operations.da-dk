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
ms.openlocfilehash: 80f0606dc3842cdfa56d41e2815eccd7518218b8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916516"
---
# <span data-ttu-id="31447-103"><a name="NUMBERVALUE">ER-funktionen NUMBERVALUE</a></span><span class="sxs-lookup"><span data-stu-id="31447-103"><a name="NUMBERVALUE">NUMBERVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31447-104">Funktionen `NUMBERVALUE` returnerer en *Reel* værdi, der konverteres fra den angivne *Streng*-værdi.</span><span class="sxs-lookup"><span data-stu-id="31447-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="31447-105">Under konverteringen tages de specificerede decimal- og ciffergrupperingsseparatorer i betragtning.</span><span class="sxs-lookup"><span data-stu-id="31447-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="31447-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="31447-106">Syntax</span></span>

```
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="31447-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="31447-107">Arguments</span></span>

<span data-ttu-id="31447-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="31447-108">`text`: *String*</span></span>

<span data-ttu-id="31447-109">En tekstværdi, der skal konverteres til et *Reelt* tal.</span><span class="sxs-lookup"><span data-stu-id="31447-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="31447-110">`decimal separator`: Streng</span><span class="sxs-lookup"><span data-stu-id="31447-110">`decimal separator`: String</span></span>

<span data-ttu-id="31447-111">En decimalseparator.</span><span class="sxs-lookup"><span data-stu-id="31447-111">A decimal separator.</span></span> <span data-ttu-id="31447-112">Det bruges til at adskille heltal og brøkdele af et decimaltal.</span><span class="sxs-lookup"><span data-stu-id="31447-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="31447-113">`digit grouping separator`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="31447-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="31447-114">En ciffergrupperingsseparator.</span><span class="sxs-lookup"><span data-stu-id="31447-114">A digit grouping separator.</span></span> <span data-ttu-id="31447-115">Det bruges som tusindtalsseparator.</span><span class="sxs-lookup"><span data-stu-id="31447-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="31447-116">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="31447-116">Return values</span></span>

<span data-ttu-id="31447-117">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="31447-117">*Real*</span></span>

<span data-ttu-id="31447-118">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="31447-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="31447-119">Eksempel</span><span class="sxs-lookup"><span data-stu-id="31447-119">Example</span></span>

<span data-ttu-id="31447-120">`NUMBERVALUE( "1 234,56", ",", " ")` returnerer **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="31447-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31447-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="31447-121">Additional resources</span></span>

[<span data-ttu-id="31447-122">Typekonverteringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="31447-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
