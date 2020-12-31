---
title: ER-funktionen EMPTYLIST
description: Dette emne indeholder oplysninger om, hvordan funktionen EMPTYLIST til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: ccb52d7d88f292720360ae913ead5be239165193
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687664"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="d8aa7-103">ER-funktionen EMPTYLIST</span><span class="sxs-lookup"><span data-stu-id="d8aa7-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8aa7-104">Funktionen `EMPTYLIST` returnerer en tom *Postliste*-værdi ved hjælp af den angivne liste som kilde til listestrukturen.</span><span class="sxs-lookup"><span data-stu-id="d8aa7-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8aa7-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="d8aa7-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="d8aa7-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="d8aa7-106">Arguments</span></span>

<span data-ttu-id="d8aa7-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="d8aa7-107">`list`: *Record list*</span></span>

<span data-ttu-id="d8aa7-108">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="d8aa7-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d8aa7-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="d8aa7-109">Return values</span></span>

<span data-ttu-id="d8aa7-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="d8aa7-110">*Record list*</span></span>

<span data-ttu-id="d8aa7-111">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="d8aa7-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="d8aa7-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d8aa7-112">Example</span></span>

<span data-ttu-id="d8aa7-113">`EMPTYLIST (SPLIT ("abc", 1))` returnerer en ny tom liste, der har samme struktur som den liste, der er returneret af den anvendte `SPLIT`-funktion.</span><span class="sxs-lookup"><span data-stu-id="d8aa7-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8aa7-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="d8aa7-114">Additional resources</span></span>

[<span data-ttu-id="d8aa7-115">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="d8aa7-115">List functions</span></span>](er-functions-category-list.md)
