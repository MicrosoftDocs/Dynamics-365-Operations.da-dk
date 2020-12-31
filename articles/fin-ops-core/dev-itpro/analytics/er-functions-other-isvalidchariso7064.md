---
title: ER-funktionen ISVALIDCHARACTERISO7064
description: Dette emne indeholder oplysninger om, hvordan funktionen ISVALIDCHARACTERISO7064 til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c3bceb15bbe1dc65abc88c1229459707a6166482
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680656"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="aff23-103">ER-funktionen ISVALIDCHARACTERISO7064</span><span class="sxs-lookup"><span data-stu-id="aff23-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aff23-104">Funktionen `ISVALIDCHARACTERISO7064` returnerer en *Boolesk* værdi som værende **SAND**, hvis den angivne streng repræsenterer et gyldigt internationalt bankkontonummer (IBAN).</span><span class="sxs-lookup"><span data-stu-id="aff23-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="aff23-105">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="aff23-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff23-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="aff23-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="aff23-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="aff23-107">Arguments</span></span>

<span data-ttu-id="aff23-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="aff23-108">`text`: *String*</span></span>

<span data-ttu-id="aff23-109">En tekstværdi, der repræsenterer et IBAN.</span><span class="sxs-lookup"><span data-stu-id="aff23-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="aff23-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="aff23-110">Return values</span></span>

<span data-ttu-id="aff23-111">*Streng*</span><span class="sxs-lookup"><span data-stu-id="aff23-111">*String*</span></span>

<span data-ttu-id="aff23-112">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="aff23-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="aff23-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="aff23-113">Example</span></span>

<span data-ttu-id="aff23-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returnerer **SANDT**.</span><span class="sxs-lookup"><span data-stu-id="aff23-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="aff23-115">`ISVALIDCHARACTERISO7064 ("AT61")` returnerer **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="aff23-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aff23-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="aff23-116">Additional resources</span></span>

[<span data-ttu-id="aff23-117">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="aff23-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
