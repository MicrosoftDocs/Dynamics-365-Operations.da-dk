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
ms.openlocfilehash: 13346c4810d6c93d4ef47ce525831332562c7f51
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743393"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="24778-103">ER-funktionen NUMBERVALUE</span><span class="sxs-lookup"><span data-stu-id="24778-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24778-104">Funktionen `NUMBERVALUE` returnerer en *Reel* værdi, der konverteres fra den angivne *Streng*-værdi.</span><span class="sxs-lookup"><span data-stu-id="24778-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="24778-105">Under konverteringen tages de specificerede decimal- og ciffergrupperingsseparatorer i betragtning.</span><span class="sxs-lookup"><span data-stu-id="24778-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="24778-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="24778-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="24778-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="24778-107">Arguments</span></span>

<span data-ttu-id="24778-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="24778-108">`text`: *String*</span></span>

<span data-ttu-id="24778-109">En tekstværdi, der skal konverteres til et *Reelt* tal.</span><span class="sxs-lookup"><span data-stu-id="24778-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="24778-110">`decimal separator`: Streng</span><span class="sxs-lookup"><span data-stu-id="24778-110">`decimal separator`: String</span></span>

<span data-ttu-id="24778-111">En decimalseparator.</span><span class="sxs-lookup"><span data-stu-id="24778-111">A decimal separator.</span></span> <span data-ttu-id="24778-112">Det bruges til at adskille heltal og brøkdele af et decimaltal.</span><span class="sxs-lookup"><span data-stu-id="24778-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="24778-113">`digit grouping separator`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="24778-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="24778-114">En ciffergrupperingsseparator.</span><span class="sxs-lookup"><span data-stu-id="24778-114">A digit grouping separator.</span></span> <span data-ttu-id="24778-115">Det bruges som tusindtalsseparator.</span><span class="sxs-lookup"><span data-stu-id="24778-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="24778-116">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="24778-116">Return values</span></span>

<span data-ttu-id="24778-117">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="24778-117">*Real*</span></span>

<span data-ttu-id="24778-118">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="24778-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="24778-119">Eksempel</span><span class="sxs-lookup"><span data-stu-id="24778-119">Example</span></span>

<span data-ttu-id="24778-120">`NUMBERVALUE( "1 234,56", ",", " ")` returnerer **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="24778-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24778-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="24778-121">Additional resources</span></span>

[<span data-ttu-id="24778-122">Typekonverteringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="24778-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
