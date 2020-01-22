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
ms.openlocfilehash: 2673b0167f7602a6d6eaa79be639905028e99822
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915527"
---
# <span data-ttu-id="e254c-103"><a name="TRIM">ER-funktionen TRIM</a></span><span class="sxs-lookup"><span data-stu-id="e254c-103"><a name="TRIM">TRIM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e254c-104">Funktionen `TRIM` returnerer den angivne tekststreng som en *Streng*-værdi, når foranstillede og efterstillede mellemrum er blevet afkortet, og flere mellemrum mellem ord er blevet fjernet.</span><span class="sxs-lookup"><span data-stu-id="e254c-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e254c-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="e254c-105">Syntax</span></span>

```
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="e254c-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="e254c-106">Arguments</span></span>

<span data-ttu-id="e254c-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="e254c-107">`text`: *String*</span></span>

<span data-ttu-id="e254c-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="e254c-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="e254c-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="e254c-109">Return values</span></span>

<span data-ttu-id="e254c-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="e254c-110">*String*</span></span>

<span data-ttu-id="e254c-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="e254c-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e254c-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e254c-112">Example</span></span>

<span data-ttu-id="e254c-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returnerer **"Eksempeltekst"**.</span><span class="sxs-lookup"><span data-stu-id="e254c-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e254c-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e254c-114">Additional resources</span></span>

[<span data-ttu-id="e254c-115">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="e254c-115">Text functions</span></span>](er-functions-category-text.md)
