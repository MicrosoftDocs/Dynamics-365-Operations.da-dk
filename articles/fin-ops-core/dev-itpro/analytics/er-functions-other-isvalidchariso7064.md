---
title: ER-funktionen ISVALIDCHARACTERISO7064
description: Dette emne indeholder oplysninger om, hvordan funktionen ISVALIDCHARACTERISO7064 til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 26300adce5f9a8a567510885577c6cfb9b1c859a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563360"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="69216-103">ER-funktionen ISVALIDCHARACTERISO7064</span><span class="sxs-lookup"><span data-stu-id="69216-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69216-104">Funktionen `ISVALIDCHARACTERISO7064` returnerer en *Boolesk* værdi som værende **SAND**, hvis den angivne streng repræsenterer et gyldigt internationalt bankkontonummer (IBAN).</span><span class="sxs-lookup"><span data-stu-id="69216-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="69216-105">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="69216-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="69216-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="69216-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="69216-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="69216-107">Arguments</span></span>

<span data-ttu-id="69216-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="69216-108">`text`: *String*</span></span>

<span data-ttu-id="69216-109">En tekstværdi, der repræsenterer et IBAN.</span><span class="sxs-lookup"><span data-stu-id="69216-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="69216-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="69216-110">Return values</span></span>

<span data-ttu-id="69216-111">*Streng*</span><span class="sxs-lookup"><span data-stu-id="69216-111">*String*</span></span>

<span data-ttu-id="69216-112">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="69216-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="69216-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="69216-113">Example</span></span>

<span data-ttu-id="69216-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returnerer **SANDT**.</span><span class="sxs-lookup"><span data-stu-id="69216-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="69216-115">`ISVALIDCHARACTERISO7064 ("AT61")` returnerer **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="69216-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69216-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="69216-116">Additional resources</span></span>

[<span data-ttu-id="69216-117">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="69216-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]