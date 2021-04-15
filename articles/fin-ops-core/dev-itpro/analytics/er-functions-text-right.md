---
title: ER-funktionen RIGHT
description: Dette emne indeholder oplysninger om, hvordan funktionen RIGHT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
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
ms.openlocfilehash: f59b12f0b3f7b100b953b2072677c83c836746ff
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746117"
---
# <a name="right-er-function"></a><span data-ttu-id="09604-103">ER-funktionen RIGHT</span><span class="sxs-lookup"><span data-stu-id="09604-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09604-104">Funktionen `RIGHT` returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn i slutningen af den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="09604-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="09604-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="09604-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="09604-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="09604-106">Arguments</span></span>

<span data-ttu-id="09604-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="09604-107">`text`: *String*</span></span>

<span data-ttu-id="09604-108">En *Streng*-værdi, der repræsenterer den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="09604-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="09604-109">`number`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="09604-109">`number`: *Integer*</span></span>

<span data-ttu-id="09604-110">Det antal tegn, der skal returneres fra slutningen af den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="09604-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="09604-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="09604-111">Return values</span></span>

<span data-ttu-id="09604-112">*Streng*</span><span class="sxs-lookup"><span data-stu-id="09604-112">*String*</span></span>

<span data-ttu-id="09604-113">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="09604-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="09604-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="09604-114">Example</span></span>

<span data-ttu-id="09604-115">`RIGHT ("Sample", 3)` returnerer **"pel"**.</span><span class="sxs-lookup"><span data-stu-id="09604-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09604-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="09604-116">Additional resources</span></span>

[<span data-ttu-id="09604-117">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="09604-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]