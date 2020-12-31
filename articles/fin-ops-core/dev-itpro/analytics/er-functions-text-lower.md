---
title: ER-funktionen LOWER
description: Dette emne indeholder oplysninger om, hvordan funktionen LOWER til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: ad971bd78fa1da17be916efcc6857aa32575f7ac
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680308"
---
# <a name="lower-er-function"></a><span data-ttu-id="d107b-103">ER-funktionen LOWER</span><span class="sxs-lookup"><span data-stu-id="d107b-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d107b-104">Funktionen `LOWER` returnerer den angivne tekststreng som en *Streng*-værdi, når den er konverteret til små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="d107b-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="d107b-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="d107b-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="d107b-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="d107b-106">Arguments</span></span>

<span data-ttu-id="d107b-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="d107b-107">`text`: *String*</span></span>

<span data-ttu-id="d107b-108">En *Streng*-værdi, der angiver teksten.</span><span class="sxs-lookup"><span data-stu-id="d107b-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="d107b-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="d107b-109">Return values</span></span>

<span data-ttu-id="d107b-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="d107b-110">*String*</span></span>

<span data-ttu-id="d107b-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="d107b-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d107b-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d107b-112">Example</span></span>

<span data-ttu-id="d107b-113">`LOWER ("Sample")` returnerer **"eksempel"**.</span><span class="sxs-lookup"><span data-stu-id="d107b-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d107b-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="d107b-114">Additional resources</span></span>

[<span data-ttu-id="d107b-115">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="d107b-115">Text functions</span></span>](er-functions-category-text.md)
