---
title: ER-funktionen LEN
description: Dette emne indeholder oplysninger om, hvordan funktionen LEN til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: fce4b5311d84364310b76545a775f1cc8db2fd70
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569962"
---
# <a name="len-er-function"></a><span data-ttu-id="0cdca-103">ER-funktionen LEN</span><span class="sxs-lookup"><span data-stu-id="0cdca-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0cdca-104">Funktionen `LEN` funktion returnerer en antallet af tegn i en angivet streng som en *Heltals*-værdi.</span><span class="sxs-lookup"><span data-stu-id="0cdca-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cdca-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="0cdca-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="0cdca-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="0cdca-106">Arguments</span></span>

<span data-ttu-id="0cdca-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="0cdca-107">`text`: *String*</span></span>

<span data-ttu-id="0cdca-108">En *Streng*-værdi, der angiver teksten.</span><span class="sxs-lookup"><span data-stu-id="0cdca-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="0cdca-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="0cdca-109">Return values</span></span>

<span data-ttu-id="0cdca-110">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="0cdca-110">*Integer*</span></span>

<span data-ttu-id="0cdca-111">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="0cdca-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="0cdca-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="0cdca-112">Example</span></span>

<span data-ttu-id="0cdca-113">`LEN ("Sample")` returnerer **6**.</span><span class="sxs-lookup"><span data-stu-id="0cdca-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0cdca-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="0cdca-114">Additional resources</span></span>

[<span data-ttu-id="0cdca-115">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="0cdca-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]