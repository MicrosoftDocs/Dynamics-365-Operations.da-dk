---
title: ER-funktionen TRIM
description: Dette emne indeholder oplysninger om, hvordan funktionen TRIM til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: b671ef72a3558c17fb16db939770394b225656da
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560030"
---
# <a name="trim-er-function"></a><span data-ttu-id="65d19-103">ER-funktionen TRIM</span><span class="sxs-lookup"><span data-stu-id="65d19-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65d19-104">Funktionen `TRIM` returnerer den angivne tekststreng som en *Streng*-værdi, når foranstillede og efterstillede mellemrum er blevet afkortet, og flere mellemrum mellem ord er blevet fjernet.</span><span class="sxs-lookup"><span data-stu-id="65d19-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d19-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="65d19-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="65d19-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="65d19-106">Arguments</span></span>

<span data-ttu-id="65d19-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="65d19-107">`text`: *String*</span></span>

<span data-ttu-id="65d19-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="65d19-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="65d19-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="65d19-109">Return values</span></span>

<span data-ttu-id="65d19-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="65d19-110">*String*</span></span>

<span data-ttu-id="65d19-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="65d19-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="65d19-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="65d19-112">Example</span></span>

<span data-ttu-id="65d19-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returnerer **"Eksempeltekst"**.</span><span class="sxs-lookup"><span data-stu-id="65d19-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65d19-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="65d19-114">Additional resources</span></span>

[<span data-ttu-id="65d19-115">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="65d19-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]