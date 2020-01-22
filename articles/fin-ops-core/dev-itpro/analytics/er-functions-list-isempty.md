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
ms.openlocfilehash: c8450c17fe2de964016951197b0d4e231c550a99
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916125"
---
# <span data-ttu-id="f8a7c-103"><a name="ISEMPTY">ER-funktionen ISEMPTY</a></span><span class="sxs-lookup"><span data-stu-id="f8a7c-103"><a name="ISEMPTY">ISEMPTY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8a7c-104">Funktionen `ISEMPTY` returnerer en *Boolesk* værdi som værende **SAND**, hvis den angivne liste ikke indeholder nogen poster.</span><span class="sxs-lookup"><span data-stu-id="f8a7c-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="f8a7c-105">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="f8a7c-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a7c-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f8a7c-106">Syntax</span></span>

```
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="f8a7c-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="f8a7c-107">Arguments</span></span>

<span data-ttu-id="f8a7c-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="f8a7c-108">`list`: *Record list*</span></span>

<span data-ttu-id="f8a7c-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="f8a7c-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f8a7c-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="f8a7c-110">Return values</span></span>

<span data-ttu-id="f8a7c-111">*Boolesk*</span><span class="sxs-lookup"><span data-stu-id="f8a7c-111">*Boolean*</span></span>

<span data-ttu-id="f8a7c-112">Den resulterende *Booleske* værdi.</span><span class="sxs-lookup"><span data-stu-id="f8a7c-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="f8a7c-113">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="f8a7c-113">Example 1</span></span>

<span data-ttu-id="f8a7c-114">Hvis du indtaster datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("A|B|C", "|")`, returnerer udtrykket `ISEMPTY(DS)` **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="f8a7c-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f8a7c-115">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="f8a7c-115">Example 2</span></span>

<span data-ttu-id="f8a7c-116">Udtrykket `ISEMPTY (SPLIT ("",1))` returnerer **SANDT**.</span><span class="sxs-lookup"><span data-stu-id="f8a7c-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8a7c-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f8a7c-117">Additional resources</span></span>

[<span data-ttu-id="f8a7c-118">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="f8a7c-118">List functions</span></span>](er-functions-category-list.md)
