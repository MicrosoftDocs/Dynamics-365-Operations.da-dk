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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c858ad72db7afe63baca8288f312548c4fc37d5c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041394"
---
# <span data-ttu-id="913db-103"><a name="ISVALIDCHARACTERISO7064">ER-funktionen ISVALIDCHARACTERISO7064</a></span><span class="sxs-lookup"><span data-stu-id="913db-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="913db-104">Funktionen `ISVALIDCHARACTERISO7064` returnerer en *Boolesk* værdi som værende **SAND**, hvis den angivne streng repræsenterer et gyldigt internationalt bankkontonummer (IBAN).</span><span class="sxs-lookup"><span data-stu-id="913db-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="913db-105">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="913db-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="913db-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="913db-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="913db-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="913db-107">Arguments</span></span>

<span data-ttu-id="913db-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="913db-108">`text`: *String*</span></span>

<span data-ttu-id="913db-109">En tekstværdi, der repræsenterer et IBAN.</span><span class="sxs-lookup"><span data-stu-id="913db-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="913db-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="913db-110">Return values</span></span>

<span data-ttu-id="913db-111">*Streng*</span><span class="sxs-lookup"><span data-stu-id="913db-111">*String*</span></span>

<span data-ttu-id="913db-112">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="913db-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="913db-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="913db-113">Example</span></span>

<span data-ttu-id="913db-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returnerer **SANDT**.</span><span class="sxs-lookup"><span data-stu-id="913db-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="913db-115">`ISVALIDCHARACTERISO7064 ("AT61")` returnerer **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="913db-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="913db-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="913db-116">Additional resources</span></span>

[<span data-ttu-id="913db-117">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="913db-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
