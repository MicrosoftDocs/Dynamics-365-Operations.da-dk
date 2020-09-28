---
title: ER-funktionen TRIM
description: Dette emne indeholder oplysninger om, hvordan funktionen TRIM til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: a1f7999ccbcd167280cca1abc48377c36d2bc15f
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744209"
---
# <a name="trim-er-function"></a><span data-ttu-id="bb568-103">ER-funktionen TRIM</span><span class="sxs-lookup"><span data-stu-id="bb568-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb568-104">Funktionen `TRIM` returnerer den angivne tekststreng som en *Streng*-værdi, når foranstillede og efterstillede mellemrum er blevet afkortet, og flere mellemrum mellem ord er blevet fjernet.</span><span class="sxs-lookup"><span data-stu-id="bb568-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb568-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="bb568-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="bb568-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="bb568-106">Arguments</span></span>

<span data-ttu-id="bb568-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="bb568-107">`text`: *String*</span></span>

<span data-ttu-id="bb568-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="bb568-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="bb568-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="bb568-109">Return values</span></span>

<span data-ttu-id="bb568-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="bb568-110">*String*</span></span>

<span data-ttu-id="bb568-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="bb568-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="bb568-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="bb568-112">Example</span></span>

<span data-ttu-id="bb568-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returnerer **"Eksempeltekst"**.</span><span class="sxs-lookup"><span data-stu-id="bb568-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb568-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="bb568-114">Additional resources</span></span>

[<span data-ttu-id="bb568-115">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="bb568-115">Text functions</span></span>](er-functions-category-text.md)
