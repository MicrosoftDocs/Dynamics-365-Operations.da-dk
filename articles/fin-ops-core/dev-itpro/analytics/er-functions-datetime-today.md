---
title: ER-funktionen TODAY
description: Dette emne indeholder oplysninger om, hvordan funktionen TODAY til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: c7e9917dcdc45a52e0ad490f5fa194d5390cc437
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917413"
---
# <span data-ttu-id="7531e-103"><a name="TODAY">ER-funktionen TODAY</a></span><span class="sxs-lookup"><span data-stu-id="7531e-103"><a name="TODAY">TODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7531e-104">Funktionen `TODAY` returnerer en værdi i form af en *Dato*, som repræsenterer datoen for den aktuelle programserver.</span><span class="sxs-lookup"><span data-stu-id="7531e-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="7531e-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="7531e-105">Syntax</span></span>

```
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="7531e-106">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="7531e-106">Return values</span></span>

<span data-ttu-id="7531e-107">*Dato*</span><span class="sxs-lookup"><span data-stu-id="7531e-107">*Date*</span></span>

<span data-ttu-id="7531e-108">Den returnerede datoværdi.</span><span class="sxs-lookup"><span data-stu-id="7531e-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="7531e-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="7531e-109">Example</span></span>

<span data-ttu-id="7531e-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returnerer den aktuelle dato-/klokkeslætsværdi på programserver, 24. december 2015, som strengen **"24-12-2015"**, baseret på det angivne brugerdefinerede format.</span><span class="sxs-lookup"><span data-stu-id="7531e-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7531e-111">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7531e-111">Additional resources</span></span>

[<span data-ttu-id="7531e-112">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="7531e-112">Date and time functions</span></span>](er-functions-category-datetime.md)
