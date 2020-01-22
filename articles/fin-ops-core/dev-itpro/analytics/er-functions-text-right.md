---
title: ER-funktionen RIGHT
description: Dette emne indeholder oplysninger om, hvordan funktionen RIGHT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 01718f9b153c1d6c46d50a9b17e899ccfba16915
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916723"
---
# <span data-ttu-id="5b7a4-103"><a name="RIGHT">ER-funktionen RIGHT</a></span><span class="sxs-lookup"><span data-stu-id="5b7a4-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b7a4-104">Funktionen `RIGHT` returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn i slutningen af den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="5b7a4-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b7a4-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="5b7a4-105">Syntax</span></span>

```
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="5b7a4-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="5b7a4-106">Arguments</span></span>

<span data-ttu-id="5b7a4-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="5b7a4-107">`text`: *String*</span></span>

<span data-ttu-id="5b7a4-108">En *Streng*-værdi, der repræsenterer den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="5b7a4-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="5b7a4-109">`number`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="5b7a4-109">`number`: *Integer*</span></span>

<span data-ttu-id="5b7a4-110">Det antal tegn, der skal returneres fra slutningen af den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="5b7a4-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="5b7a4-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="5b7a4-111">Return values</span></span>

<span data-ttu-id="5b7a4-112">*Streng*</span><span class="sxs-lookup"><span data-stu-id="5b7a4-112">*String*</span></span>

<span data-ttu-id="5b7a4-113">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="5b7a4-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5b7a4-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="5b7a4-114">Example</span></span>

<span data-ttu-id="5b7a4-115">`RIGHT ("Sample", 3)` returnerer **"pel"**.</span><span class="sxs-lookup"><span data-stu-id="5b7a4-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b7a4-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5b7a4-116">Additional resources</span></span>

[<span data-ttu-id="5b7a4-117">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="5b7a4-117">Text functions</span></span>](er-functions-category-text.md)
