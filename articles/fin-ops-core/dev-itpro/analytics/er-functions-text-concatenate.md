---
title: ER-funktionen CONCATENATE
description: Dette emne indeholder oplysninger om, hvordan funktionen CONCATENATE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 1a21140e5636ebd96eca4be90308c915e77510e1
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743897"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="0beac-103">ER-funktionen CONCATENATE</span><span class="sxs-lookup"><span data-stu-id="0beac-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0beac-104">Funktionen `CONCATENATE` returnerer alle de angivne tekststrenge som en *Streng*-værdi, når de er blevet sammenkædet i en streng.</span><span class="sxs-lookup"><span data-stu-id="0beac-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0beac-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="0beac-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="0beac-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="0beac-106">Arguments</span></span>

<span data-ttu-id="0beac-107">`text 1`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="0beac-107">`text 1`: *String*</span></span>

<span data-ttu-id="0beac-108">En reference til en datakilde af datatypen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="0beac-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="0beac-109">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="0beac-109">This argument is required.</span></span>

<span data-ttu-id="0beac-110">`text N`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="0beac-110">`text N`: *String*</span></span>

<span data-ttu-id="0beac-111">En reference til en datakilde af datatypen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="0beac-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="0beac-112">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="0beac-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="0beac-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="0beac-113">Return values</span></span>

<span data-ttu-id="0beac-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="0beac-114">*String*</span></span>

<span data-ttu-id="0beac-115">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="0beac-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="0beac-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="0beac-116">Example</span></span>

<span data-ttu-id="0beac-117">`CONCATENATE ("abc", "def")` returnerer **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="0beac-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0beac-118">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="0beac-118">Usage notes</span></span>

<span data-ttu-id="0beac-119">Udtrykket `"abc" & "def"` returnerer også **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="0beac-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0beac-120">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="0beac-120">Additional resources</span></span>

[<span data-ttu-id="0beac-121">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="0beac-121">Text functions</span></span>](er-functions-category-text.md)
