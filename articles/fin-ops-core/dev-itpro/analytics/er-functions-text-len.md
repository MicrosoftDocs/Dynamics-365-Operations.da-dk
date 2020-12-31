---
title: ER-funktionen LEN
description: Dette emne indeholder oplysninger om, hvordan funktionen LEN til elektronisk rapportering (ER) skal anvendes.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d766b8effa9d6936de7a3def252536603330965
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680352"
---
# <a name="len-er-function"></a><span data-ttu-id="fbeb5-103">ER-funktionen LEN</span><span class="sxs-lookup"><span data-stu-id="fbeb5-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbeb5-104">Funktionen `LEN` funktion returnerer en antallet af tegn i en angivet streng som en *Heltals*-værdi.</span><span class="sxs-lookup"><span data-stu-id="fbeb5-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbeb5-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="fbeb5-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="fbeb5-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="fbeb5-106">Arguments</span></span>

<span data-ttu-id="fbeb5-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="fbeb5-107">`text`: *String*</span></span>

<span data-ttu-id="fbeb5-108">En *Streng*-værdi, der angiver teksten.</span><span class="sxs-lookup"><span data-stu-id="fbeb5-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="fbeb5-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="fbeb5-109">Return values</span></span>

<span data-ttu-id="fbeb5-110">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="fbeb5-110">*Integer*</span></span>

<span data-ttu-id="fbeb5-111">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="fbeb5-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="fbeb5-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fbeb5-112">Example</span></span>

<span data-ttu-id="fbeb5-113">`LEN ("Sample")` returnerer **6**.</span><span class="sxs-lookup"><span data-stu-id="fbeb5-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fbeb5-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="fbeb5-114">Additional resources</span></span>

[<span data-ttu-id="fbeb5-115">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="fbeb5-115">Text functions</span></span>](er-functions-category-text.md)
