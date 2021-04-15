---
title: ER-funktionen EMPTYLIST
description: Dette emne indeholder oplysninger om, hvordan funktionen EMPTYLIST til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 1e2a92d9951c3ad27503cf82f1b45026f16c3835
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746669"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="e9957-103">ER-funktionen EMPTYLIST</span><span class="sxs-lookup"><span data-stu-id="e9957-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9957-104">Funktionen `EMPTYLIST` returnerer en tom *Postliste*-værdi ved hjælp af den angivne liste som kilde til listestrukturen.</span><span class="sxs-lookup"><span data-stu-id="e9957-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9957-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="e9957-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="e9957-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="e9957-106">Arguments</span></span>

<span data-ttu-id="e9957-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="e9957-107">`list`: *Record list*</span></span>

<span data-ttu-id="e9957-108">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="e9957-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="e9957-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="e9957-109">Return values</span></span>

<span data-ttu-id="e9957-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="e9957-110">*Record list*</span></span>

<span data-ttu-id="e9957-111">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="e9957-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="e9957-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e9957-112">Example</span></span>

<span data-ttu-id="e9957-113">`EMPTYLIST (SPLIT ("abc", 1))` returnerer en ny tom liste, der har samme struktur som den liste, der er returneret af den anvendte `SPLIT`-funktion.</span><span class="sxs-lookup"><span data-stu-id="e9957-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9957-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e9957-114">Additional resources</span></span>

[<span data-ttu-id="e9957-115">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="e9957-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]