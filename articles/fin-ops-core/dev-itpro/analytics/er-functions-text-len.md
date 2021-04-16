---
title: ER-funktionen LEN
description: Dette emne indeholder oplysninger om, hvordan funktionen LEN til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: 394e07a7a573cc4462196b17440f8b0547d8dd48
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746309"
---
# <a name="len-er-function"></a><span data-ttu-id="c4fcb-103">ER-funktionen LEN</span><span class="sxs-lookup"><span data-stu-id="c4fcb-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4fcb-104">Funktionen `LEN` funktion returnerer en antallet af tegn i en angivet streng som en *Heltals*-værdi.</span><span class="sxs-lookup"><span data-stu-id="c4fcb-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4fcb-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="c4fcb-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="c4fcb-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="c4fcb-106">Arguments</span></span>

<span data-ttu-id="c4fcb-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="c4fcb-107">`text`: *String*</span></span>

<span data-ttu-id="c4fcb-108">En *Streng*-værdi, der angiver teksten.</span><span class="sxs-lookup"><span data-stu-id="c4fcb-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="c4fcb-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="c4fcb-109">Return values</span></span>

<span data-ttu-id="c4fcb-110">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="c4fcb-110">*Integer*</span></span>

<span data-ttu-id="c4fcb-111">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="c4fcb-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="c4fcb-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="c4fcb-112">Example</span></span>

<span data-ttu-id="c4fcb-113">`LEN ("Sample")` returnerer **6**.</span><span class="sxs-lookup"><span data-stu-id="c4fcb-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c4fcb-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c4fcb-114">Additional resources</span></span>

[<span data-ttu-id="c4fcb-115">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="c4fcb-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]