---
title: ER-funktionen RIGHT
description: Dette emne indeholder oplysninger om, hvordan funktionen RIGHT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 75255eccf4da468b0946253f7570b1621f905cd7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570234"
---
# <a name="right-er-function"></a><span data-ttu-id="f1f67-103">ER-funktionen RIGHT</span><span class="sxs-lookup"><span data-stu-id="f1f67-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1f67-104">Funktionen `RIGHT` returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn i slutningen af den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="f1f67-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1f67-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f1f67-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="f1f67-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="f1f67-106">Arguments</span></span>

<span data-ttu-id="f1f67-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="f1f67-107">`text`: *String*</span></span>

<span data-ttu-id="f1f67-108">En *Streng*-værdi, der repræsenterer den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="f1f67-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="f1f67-109">`number`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="f1f67-109">`number`: *Integer*</span></span>

<span data-ttu-id="f1f67-110">Det antal tegn, der skal returneres fra slutningen af den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="f1f67-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="f1f67-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="f1f67-111">Return values</span></span>

<span data-ttu-id="f1f67-112">*Streng*</span><span class="sxs-lookup"><span data-stu-id="f1f67-112">*String*</span></span>

<span data-ttu-id="f1f67-113">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="f1f67-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f1f67-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="f1f67-114">Example</span></span>

<span data-ttu-id="f1f67-115">`RIGHT ("Sample", 3)` returnerer **"pel"**.</span><span class="sxs-lookup"><span data-stu-id="f1f67-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1f67-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f1f67-116">Additional resources</span></span>

[<span data-ttu-id="f1f67-117">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="f1f67-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]