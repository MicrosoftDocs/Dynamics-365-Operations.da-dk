---
title: ER-funktionen UPPER
description: Dette emne indeholder oplysninger om, hvordan funktionen UPPER til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 0e0e9837765914c657a72c5ce04c6f565fa13788
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749135"
---
# <a name="upper-er-function"></a><span data-ttu-id="3721d-103">ER-funktionen UPPER</span><span class="sxs-lookup"><span data-stu-id="3721d-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3721d-104">Funktionen `UPPER` returnerer den angivne tekststreng som en *Streng*-værdi, når den er konverteret til blokbogstaver.</span><span class="sxs-lookup"><span data-stu-id="3721d-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="3721d-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="3721d-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="3721d-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="3721d-106">Arguments</span></span>

<span data-ttu-id="3721d-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="3721d-107">`text`: *String*</span></span>

<span data-ttu-id="3721d-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="3721d-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="3721d-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="3721d-109">Return values</span></span>

<span data-ttu-id="3721d-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="3721d-110">*String*</span></span>

<span data-ttu-id="3721d-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="3721d-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="3721d-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="3721d-112">Example</span></span>

<span data-ttu-id="3721d-113">`UPPER ("Sample")` returnerer **"EKSEMPEL"**.</span><span class="sxs-lookup"><span data-stu-id="3721d-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3721d-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3721d-114">Additional resources</span></span>

[<span data-ttu-id="3721d-115">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="3721d-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]