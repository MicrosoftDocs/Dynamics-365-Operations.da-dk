---
title: ER-funktionen SESSIONTODAY
description: Dette emne indeholder oplysninger om, hvordan funktionen SESSIONTODAY til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 6d0fcbbf1a1fb0809e3f76161314f38bcd8a74aa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746765"
---
# <a name="sessiontoday-er-function"></a><span data-ttu-id="c6bb2-103">ER-funktionen SESSIONTODAY</span><span class="sxs-lookup"><span data-stu-id="c6bb2-103">SESSIONTODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6bb2-104">Funktionen `SESSIONTODAY` returnerer en værdi i form af en *Dato*, som repræsenterer datoen for den aktuelle programsession.</span><span class="sxs-lookup"><span data-stu-id="c6bb2-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6bb2-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="c6bb2-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="c6bb2-106">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="c6bb2-106">Return values</span></span>

<span data-ttu-id="c6bb2-107">*Dato*</span><span class="sxs-lookup"><span data-stu-id="c6bb2-107">*Date*</span></span>

<span data-ttu-id="c6bb2-108">Den returnerede datoværdi.</span><span class="sxs-lookup"><span data-stu-id="c6bb2-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="c6bb2-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="c6bb2-109">Example</span></span>

<span data-ttu-id="c6bb2-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returnerer datoen for den aktuelle programsession, 24. december 2015, som strengen **"24-12-2015"**, baseret på den valgte tyske kultur og det angivne format.</span><span class="sxs-lookup"><span data-stu-id="c6bb2-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6bb2-111">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c6bb2-111">Additional resources</span></span>

[<span data-ttu-id="c6bb2-112">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="c6bb2-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]