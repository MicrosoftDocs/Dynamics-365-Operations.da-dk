---
title: ER-funktionen ISEMPTY
description: Dette emne indeholder oplysninger om, hvordan funktionen ISEMPTY til elektronisk rapportering (ER) skal anvendes.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b6fde7cbadec7aae052742ef598e1af4dbae793
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745123"
---
# <a name="isempty-er-function"></a><span data-ttu-id="d32ea-103">ER-funktionen ISEMPTY</span><span class="sxs-lookup"><span data-stu-id="d32ea-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d32ea-104">Funktionen `ISEMPTY` returnerer en *Boolesk* værdi som værende **SAND**, hvis den angivne liste ikke indeholder nogen poster.</span><span class="sxs-lookup"><span data-stu-id="d32ea-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="d32ea-105">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="d32ea-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d32ea-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="d32ea-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="d32ea-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="d32ea-107">Arguments</span></span>

<span data-ttu-id="d32ea-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="d32ea-108">`list`: *Record list*</span></span>

<span data-ttu-id="d32ea-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="d32ea-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d32ea-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="d32ea-110">Return values</span></span>

<span data-ttu-id="d32ea-111">*Boolesk*</span><span class="sxs-lookup"><span data-stu-id="d32ea-111">*Boolean*</span></span>

<span data-ttu-id="d32ea-112">Den resulterende *Booleske* værdi.</span><span class="sxs-lookup"><span data-stu-id="d32ea-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="d32ea-113">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="d32ea-113">Example 1</span></span>

<span data-ttu-id="d32ea-114">Hvis du indtaster datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("A|B|C", "|")`, returnerer udtrykket `ISEMPTY(DS)` **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="d32ea-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d32ea-115">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="d32ea-115">Example 2</span></span>

<span data-ttu-id="d32ea-116">Udtrykket `ISEMPTY (SPLIT ("",1))` returnerer **SANDT**.</span><span class="sxs-lookup"><span data-stu-id="d32ea-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d32ea-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="d32ea-117">Additional resources</span></span>

[<span data-ttu-id="d32ea-118">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="d32ea-118">List functions</span></span>](er-functions-category-list.md)
