---
title: ER-funktionen ISVALIDCHARACTERISO7064
description: Dette emne indeholder oplysninger om, hvordan funktionen ISVALIDCHARACTERISO7064 til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 1f102a6a3eafe3b066101370b94fa2f17ad3ad8b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748287"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="a331a-103">ER-funktionen ISVALIDCHARACTERISO7064</span><span class="sxs-lookup"><span data-stu-id="a331a-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a331a-104">Funktionen `ISVALIDCHARACTERISO7064` returnerer en *Boolesk* værdi som værende **SAND**, hvis den angivne streng repræsenterer et gyldigt internationalt bankkontonummer (IBAN).</span><span class="sxs-lookup"><span data-stu-id="a331a-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="a331a-105">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="a331a-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a331a-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="a331a-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="a331a-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="a331a-107">Arguments</span></span>

<span data-ttu-id="a331a-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="a331a-108">`text`: *String*</span></span>

<span data-ttu-id="a331a-109">En tekstværdi, der repræsenterer et IBAN.</span><span class="sxs-lookup"><span data-stu-id="a331a-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="a331a-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="a331a-110">Return values</span></span>

<span data-ttu-id="a331a-111">*Streng*</span><span class="sxs-lookup"><span data-stu-id="a331a-111">*String*</span></span>

<span data-ttu-id="a331a-112">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="a331a-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="a331a-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a331a-113">Example</span></span>

<span data-ttu-id="a331a-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returnerer **SANDT**.</span><span class="sxs-lookup"><span data-stu-id="a331a-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="a331a-115">`ISVALIDCHARACTERISO7064 ("AT61")` returnerer **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a331a-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a331a-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a331a-116">Additional resources</span></span>

[<span data-ttu-id="a331a-117">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="a331a-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]