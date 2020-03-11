---
title: ER-funktionen SESSIONTODAY
description: Dette emne indeholder oplysninger om, hvordan funktionen SESSIONTODAY til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 483ff46a27068bc2d70c80a848f0329861c914b3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042254"
---
# <span data-ttu-id="0f5d2-103"><a name="SESSIONTODAY">ER-funktionen SESSIONTODAY</a></span><span class="sxs-lookup"><span data-stu-id="0f5d2-103"><a name="SESSIONTODAY">SESSIONTODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f5d2-104">Funktionen `SESSIONTODAY` returnerer en værdi i form af en *Dato*, som repræsenterer datoen for den aktuelle programsession.</span><span class="sxs-lookup"><span data-stu-id="0f5d2-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f5d2-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="0f5d2-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="0f5d2-106">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="0f5d2-106">Return values</span></span>

<span data-ttu-id="0f5d2-107">*Dato*</span><span class="sxs-lookup"><span data-stu-id="0f5d2-107">*Date*</span></span>

<span data-ttu-id="0f5d2-108">Den returnerede datoværdi.</span><span class="sxs-lookup"><span data-stu-id="0f5d2-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="0f5d2-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="0f5d2-109">Example</span></span>

<span data-ttu-id="0f5d2-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returnerer datoen for den aktuelle programsession, 24. december 2015, som strengen **"24-12-2015"**, baseret på den valgte tyske kultur og det angivne format.</span><span class="sxs-lookup"><span data-stu-id="0f5d2-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f5d2-111">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="0f5d2-111">Additional resources</span></span>

[<span data-ttu-id="0f5d2-112">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="0f5d2-112">Date and time functions</span></span>](er-functions-category-datetime.md)
