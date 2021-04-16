---
title: ER-funktionen TRIM
description: Dette emne indeholder oplysninger om, hvordan funktionen TRIM til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 93b08792a7aab7245d0443da05e0330bf8b2d56e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746043"
---
# <a name="trim-er-function"></a><span data-ttu-id="1e532-103">ER-funktionen TRIM</span><span class="sxs-lookup"><span data-stu-id="1e532-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e532-104">Funktionen `TRIM` returnerer den angivne tekststreng som en *Streng*-værdi, når foranstillede og efterstillede mellemrum er blevet afkortet, og flere mellemrum mellem ord er blevet fjernet.</span><span class="sxs-lookup"><span data-stu-id="1e532-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e532-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="1e532-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="1e532-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="1e532-106">Arguments</span></span>

<span data-ttu-id="1e532-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="1e532-107">`text`: *String*</span></span>

<span data-ttu-id="1e532-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="1e532-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="1e532-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="1e532-109">Return values</span></span>

<span data-ttu-id="1e532-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="1e532-110">*String*</span></span>

<span data-ttu-id="1e532-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="1e532-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="1e532-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="1e532-112">Example</span></span>

<span data-ttu-id="1e532-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returnerer **"Eksempeltekst"**.</span><span class="sxs-lookup"><span data-stu-id="1e532-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e532-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="1e532-114">Additional resources</span></span>

[<span data-ttu-id="1e532-115">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="1e532-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]