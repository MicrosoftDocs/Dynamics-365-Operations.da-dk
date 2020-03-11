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
ms.openlocfilehash: 7169d9d3d2cdfb9f36bb77c1688922549e79ff32
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040865"
---
# <span data-ttu-id="be7f1-103"><a name="RIGHT">ER-funktionen RIGHT</a></span><span class="sxs-lookup"><span data-stu-id="be7f1-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be7f1-104">Funktionen `RIGHT` returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn i slutningen af den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="be7f1-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="be7f1-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="be7f1-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="be7f1-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="be7f1-106">Arguments</span></span>

<span data-ttu-id="be7f1-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="be7f1-107">`text`: *String*</span></span>

<span data-ttu-id="be7f1-108">En *Streng*-værdi, der repræsenterer den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="be7f1-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="be7f1-109">`number`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="be7f1-109">`number`: *Integer*</span></span>

<span data-ttu-id="be7f1-110">Det antal tegn, der skal returneres fra slutningen af den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="be7f1-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="be7f1-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="be7f1-111">Return values</span></span>

<span data-ttu-id="be7f1-112">*Streng*</span><span class="sxs-lookup"><span data-stu-id="be7f1-112">*String*</span></span>

<span data-ttu-id="be7f1-113">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="be7f1-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="be7f1-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="be7f1-114">Example</span></span>

<span data-ttu-id="be7f1-115">`RIGHT ("Sample", 3)` returnerer **"pel"**.</span><span class="sxs-lookup"><span data-stu-id="be7f1-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be7f1-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="be7f1-116">Additional resources</span></span>

[<span data-ttu-id="be7f1-117">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="be7f1-117">Text functions</span></span>](er-functions-category-text.md)
