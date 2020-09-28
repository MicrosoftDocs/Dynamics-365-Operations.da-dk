---
title: ER-funktionen VALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen VALUE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: ecbffb7e39d7f2f2bccdfe32d593512a65da163c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745507"
---
# <a name="value-er-function"></a><span data-ttu-id="78324-103">ER-funktionen VALUE</span><span class="sxs-lookup"><span data-stu-id="78324-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78324-104">Funktionen `VALUE` returnerer en *Reel* værdi, der konverteres fra den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="78324-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="78324-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="78324-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="78324-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="78324-106">Arguments</span></span>

<span data-ttu-id="78324-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="78324-107">`text`: *String*</span></span>

<span data-ttu-id="78324-108">En strengværdi, der skal konverteres til en numerisk værdi.</span><span class="sxs-lookup"><span data-stu-id="78324-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="78324-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="78324-109">Return values</span></span>

<span data-ttu-id="78324-110">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="78324-110">*Real*</span></span>

<span data-ttu-id="78324-111">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="78324-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="78324-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="78324-112">Usage notes</span></span>

<span data-ttu-id="78324-113">Komma og punktum (.) betragtes som decimalseparator og en indledende bindestreg (-) bruges som et negativt fortegn.</span><span class="sxs-lookup"><span data-stu-id="78324-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="78324-114">Der udløses en undtagelse under kørslen, hvis den angivne streng indeholder andre ikke-numeriske tegn.</span><span class="sxs-lookup"><span data-stu-id="78324-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="78324-115">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="78324-115">Example 1</span></span>

<span data-ttu-id="78324-116">`VALUE ("1 234,56")` udløser en undtagelse.</span><span class="sxs-lookup"><span data-stu-id="78324-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="78324-117">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="78324-117">Example 2</span></span>

<span data-ttu-id="78324-118">`VALUE ("1234,56")` returnerer **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="78324-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="78324-119">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="78324-119">Additional resources</span></span>

[<span data-ttu-id="78324-120">Typekonverteringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="78324-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
