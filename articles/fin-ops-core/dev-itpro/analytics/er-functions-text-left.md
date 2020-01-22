---
title: ER-funktionen LEFT
description: Dette emne indeholder oplysninger om, hvordan funktionen LEFT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 8280a05ea180d9de499d87efa53eca8ca912b0e3
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915642"
---
# <span data-ttu-id="aecec-103"><a name="LEFT">ER-funktionen LEFT</a></span><span class="sxs-lookup"><span data-stu-id="aecec-103"><a name="LEFT">LEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aecec-104">Funktionen `LEFT` returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn i begyndelsen af den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="aecec-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="aecec-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="aecec-105">Syntax</span></span>

```
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="aecec-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="aecec-106">Arguments</span></span>

<span data-ttu-id="aecec-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="aecec-107">`text`: *String*</span></span>

<span data-ttu-id="aecec-108">En *Streng*-værdi, der repræsenterer den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="aecec-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="aecec-109">`number`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="aecec-109">`number`: *Integer*</span></span>

<span data-ttu-id="aecec-110">Det antal tegn, der skal returneres fra begyndelsen af den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="aecec-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="aecec-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="aecec-111">Return values</span></span>

<span data-ttu-id="aecec-112">*Streng*</span><span class="sxs-lookup"><span data-stu-id="aecec-112">*String*</span></span>

<span data-ttu-id="aecec-113">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="aecec-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="aecec-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="aecec-114">Example</span></span>

<span data-ttu-id="aecec-115">`LEFT ("Sample", 3)` returnerer **"Eks"**.</span><span class="sxs-lookup"><span data-stu-id="aecec-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aecec-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="aecec-116">Additional resources</span></span>

[<span data-ttu-id="aecec-117">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="aecec-117">Text functions</span></span>](er-functions-category-text.md)
