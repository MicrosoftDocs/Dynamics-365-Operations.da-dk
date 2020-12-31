---
title: ER-funktionen LISTOFFIRSTITEM
description: Dette emne indeholder oplysninger om, hvordan funktionen LISTOFFIRSTITEM til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 8ea81bce8cd6b922f3ef1d53ec0c4b2574780377
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686482"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="c28ae-103">ER-funktionen LISTOFFIRSTITEM</span><span class="sxs-lookup"><span data-stu-id="c28ae-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c28ae-104">Funktionen `LISTOFFIRSTITEM` returnerer en ny *Postliste*-værdi, der udelukkende består af de første poster på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="c28ae-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c28ae-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="c28ae-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="c28ae-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="c28ae-106">Arguments</span></span>

<span data-ttu-id="c28ae-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="c28ae-107">`list`: *Record list*</span></span>

<span data-ttu-id="c28ae-108">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="c28ae-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="c28ae-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="c28ae-109">Return values</span></span>

<span data-ttu-id="c28ae-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="c28ae-110">*Record list*</span></span>

<span data-ttu-id="c28ae-111">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="c28ae-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="c28ae-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="c28ae-112">Example</span></span>

<span data-ttu-id="c28ae-113">Udtrykket `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returnerer tekstværdien **"A"**.</span><span class="sxs-lookup"><span data-stu-id="c28ae-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c28ae-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c28ae-114">Additional resources</span></span>

[<span data-ttu-id="c28ae-115">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="c28ae-115">List functions</span></span>](er-functions-category-list.md)
