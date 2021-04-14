---
title: ER-funktionen NUMBERVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen NUMBERVALUE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 84d7f17f37a83547522cf09047b72100f6f5b859
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755342"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="d64b1-103">ER-funktionen NUMBERVALUE</span><span class="sxs-lookup"><span data-stu-id="d64b1-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d64b1-104">Funktionen `NUMBERVALUE` returnerer en *Reel* værdi, der konverteres fra den angivne *Streng*-værdi.</span><span class="sxs-lookup"><span data-stu-id="d64b1-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="d64b1-105">Under konverteringen tages de specificerede decimal- og ciffergrupperingsseparatorer i betragtning.</span><span class="sxs-lookup"><span data-stu-id="d64b1-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="d64b1-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="d64b1-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="d64b1-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="d64b1-107">Arguments</span></span>

<span data-ttu-id="d64b1-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="d64b1-108">`text`: *String*</span></span>

<span data-ttu-id="d64b1-109">En tekstværdi, der skal konverteres til et *Reelt* tal.</span><span class="sxs-lookup"><span data-stu-id="d64b1-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="d64b1-110">`decimal separator`: Streng</span><span class="sxs-lookup"><span data-stu-id="d64b1-110">`decimal separator`: String</span></span>

<span data-ttu-id="d64b1-111">En decimalseparator.</span><span class="sxs-lookup"><span data-stu-id="d64b1-111">A decimal separator.</span></span> <span data-ttu-id="d64b1-112">Det bruges til at adskille heltal og brøkdele af et decimaltal.</span><span class="sxs-lookup"><span data-stu-id="d64b1-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="d64b1-113">`digit grouping separator`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="d64b1-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="d64b1-114">En ciffergrupperingsseparator.</span><span class="sxs-lookup"><span data-stu-id="d64b1-114">A digit grouping separator.</span></span> <span data-ttu-id="d64b1-115">Det bruges som tusindtalsseparator.</span><span class="sxs-lookup"><span data-stu-id="d64b1-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="d64b1-116">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="d64b1-116">Return values</span></span>

<span data-ttu-id="d64b1-117">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="d64b1-117">*Real*</span></span>

<span data-ttu-id="d64b1-118">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="d64b1-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="d64b1-119">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d64b1-119">Example</span></span>

<span data-ttu-id="d64b1-120">`NUMBERVALUE( "1 234,56", ",", " ")` returnerer **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="d64b1-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d64b1-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="d64b1-121">Additional resources</span></span>

[<span data-ttu-id="d64b1-122">Typekonverteringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="d64b1-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]