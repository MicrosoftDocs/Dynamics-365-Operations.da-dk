---
title: ER-funktionen UPPER
description: Dette emne indeholder oplysninger om, hvordan funktionen UPPER til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: ed862ab823cfc3539c420d3066c9397e1e6d870e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916677"
---
# <span data-ttu-id="34f28-103"><a name="UPPER">ER-funktionen UPPER</a></span><span class="sxs-lookup"><span data-stu-id="34f28-103"><a name="UPPER">UPPER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34f28-104">Funktionen `UPPER` returnerer den angivne tekststreng som en *Streng*-værdi, når den er konverteret til blokbogstaver.</span><span class="sxs-lookup"><span data-stu-id="34f28-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="34f28-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="34f28-105">Syntax</span></span>

```
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="34f28-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="34f28-106">Arguments</span></span>

<span data-ttu-id="34f28-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="34f28-107">`text`: *String*</span></span>

<span data-ttu-id="34f28-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="34f28-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="34f28-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="34f28-109">Return values</span></span>

<span data-ttu-id="34f28-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="34f28-110">*String*</span></span>

<span data-ttu-id="34f28-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="34f28-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="34f28-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="34f28-112">Example</span></span>

<span data-ttu-id="34f28-113">`UPPER ("Sample")` returnerer **"EKSEMPEL"**.</span><span class="sxs-lookup"><span data-stu-id="34f28-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34f28-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="34f28-114">Additional resources</span></span>

[<span data-ttu-id="34f28-115">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="34f28-115">Text functions</span></span>](er-functions-category-text.md)
