---
title: ER-funktionen SESSIONNOW
description: Dette emne indeholder oplysninger om, hvordan funktionen SESSIONNOW til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 4dff6daa8fbd60ef1fc84d783e428d69477aac6d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916263"
---
# <span data-ttu-id="57503-103"><a name="">ER-funktionen SESSIONNOW</a></span><span class="sxs-lookup"><span data-stu-id="57503-103"><a name="">SESSIONNOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57503-104">Funktionen `SESSIONNOW` returnerer en værdi i form af *DatoKlokkeslæt*, som repræsenterer dato og klokkeslæt for den aktuelle programsession.</span><span class="sxs-lookup"><span data-stu-id="57503-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="57503-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="57503-105">Syntax</span></span>

```
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="57503-106">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="57503-106">Return values</span></span>

<span data-ttu-id="57503-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="57503-107">*DateTime*</span></span>

<span data-ttu-id="57503-108">Den returnerede dato-/klokkeslætsværdi.</span><span class="sxs-lookup"><span data-stu-id="57503-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="57503-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="57503-109">Example</span></span>

<span data-ttu-id="57503-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returnerer datoen/klokkeslættet for den aktuelle programsession, 24. december 2015, som strengen **"24.12.2015"**, baseret på den valgte tyske kultur og det angivne format.</span><span class="sxs-lookup"><span data-stu-id="57503-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57503-111">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="57503-111">Additional resources</span></span>

[<span data-ttu-id="57503-112">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="57503-112">Date and time functions</span></span>](er-functions-category-datetime.md)
