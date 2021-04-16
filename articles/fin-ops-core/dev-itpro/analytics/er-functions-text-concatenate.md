---
title: ER-funktionen CONCATENATE
description: Dette emne indeholder oplysninger om, hvordan funktionen CONCATENATE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
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
ms.openlocfilehash: f1a47a05127412588f4628cb425eab0379493c3c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746474"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="e1d1a-103">ER-funktionen CONCATENATE</span><span class="sxs-lookup"><span data-stu-id="e1d1a-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1d1a-104">Funktionen `CONCATENATE` returnerer alle de angivne tekststrenge som en *Streng*-værdi, når de er blevet sammenkædet i en streng.</span><span class="sxs-lookup"><span data-stu-id="e1d1a-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d1a-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="e1d1a-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="e1d1a-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="e1d1a-106">Arguments</span></span>

<span data-ttu-id="e1d1a-107">`text 1`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="e1d1a-107">`text 1`: *String*</span></span>

<span data-ttu-id="e1d1a-108">En reference til en datakilde af datatypen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="e1d1a-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="e1d1a-109">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="e1d1a-109">This argument is required.</span></span>

<span data-ttu-id="e1d1a-110">`text N`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="e1d1a-110">`text N`: *String*</span></span>

<span data-ttu-id="e1d1a-111">En reference til en datakilde af datatypen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="e1d1a-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="e1d1a-112">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="e1d1a-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="e1d1a-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="e1d1a-113">Return values</span></span>

<span data-ttu-id="e1d1a-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="e1d1a-114">*String*</span></span>

<span data-ttu-id="e1d1a-115">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="e1d1a-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e1d1a-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e1d1a-116">Example</span></span>

<span data-ttu-id="e1d1a-117">`CONCATENATE ("abc", "def")` returnerer **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="e1d1a-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e1d1a-118">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="e1d1a-118">Usage notes</span></span>

<span data-ttu-id="e1d1a-119">Udtrykket `"abc" & "def"` returnerer også **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="e1d1a-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1d1a-120">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e1d1a-120">Additional resources</span></span>

[<span data-ttu-id="e1d1a-121">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="e1d1a-121">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]