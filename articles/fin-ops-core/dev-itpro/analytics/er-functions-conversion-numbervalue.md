---
title: ER-funktionen NUMBERVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen NUMBERVALUE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: f542621c4bcc29e03d8c92b0c700e2c80c9846f6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561416"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="ee286-103">ER-funktionen NUMBERVALUE</span><span class="sxs-lookup"><span data-stu-id="ee286-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee286-104">Funktionen `NUMBERVALUE` returnerer en *Reel* værdi, der konverteres fra den angivne *Streng*-værdi.</span><span class="sxs-lookup"><span data-stu-id="ee286-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="ee286-105">Under konverteringen tages de specificerede decimal- og ciffergrupperingsseparatorer i betragtning.</span><span class="sxs-lookup"><span data-stu-id="ee286-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee286-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="ee286-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="ee286-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="ee286-107">Arguments</span></span>

<span data-ttu-id="ee286-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ee286-108">`text`: *String*</span></span>

<span data-ttu-id="ee286-109">En tekstværdi, der skal konverteres til et *Reelt* tal.</span><span class="sxs-lookup"><span data-stu-id="ee286-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="ee286-110">`decimal separator`: Streng</span><span class="sxs-lookup"><span data-stu-id="ee286-110">`decimal separator`: String</span></span>

<span data-ttu-id="ee286-111">En decimalseparator.</span><span class="sxs-lookup"><span data-stu-id="ee286-111">A decimal separator.</span></span> <span data-ttu-id="ee286-112">Det bruges til at adskille heltal og brøkdele af et decimaltal.</span><span class="sxs-lookup"><span data-stu-id="ee286-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="ee286-113">`digit grouping separator`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ee286-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="ee286-114">En ciffergrupperingsseparator.</span><span class="sxs-lookup"><span data-stu-id="ee286-114">A digit grouping separator.</span></span> <span data-ttu-id="ee286-115">Det bruges som tusindtalsseparator.</span><span class="sxs-lookup"><span data-stu-id="ee286-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="ee286-116">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="ee286-116">Return values</span></span>

<span data-ttu-id="ee286-117">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="ee286-117">*Real*</span></span>

<span data-ttu-id="ee286-118">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="ee286-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="ee286-119">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ee286-119">Example</span></span>

<span data-ttu-id="ee286-120">`NUMBERVALUE( "1 234,56", ",", " ")` returnerer **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="ee286-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ee286-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ee286-121">Additional resources</span></span>

[<span data-ttu-id="ee286-122">Typekonverteringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="ee286-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]