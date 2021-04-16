---
title: ER-funktionen ISEMPTY
description: Dette emne indeholder oplysninger om, hvordan funktionen ISEMPTY til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 9c33e8b613bf5bf5bc17a42a7668d4cc4ee58e53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750430"
---
# <a name="isempty-er-function"></a><span data-ttu-id="f7c7a-103">ER-funktionen ISEMPTY</span><span class="sxs-lookup"><span data-stu-id="f7c7a-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7c7a-104">Funktionen `ISEMPTY` returnerer en *Boolesk* værdi som værende **SAND**, hvis den angivne liste ikke indeholder nogen poster.</span><span class="sxs-lookup"><span data-stu-id="f7c7a-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="f7c7a-105">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="f7c7a-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7c7a-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f7c7a-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="f7c7a-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="f7c7a-107">Arguments</span></span>

<span data-ttu-id="f7c7a-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="f7c7a-108">`list`: *Record list*</span></span>

<span data-ttu-id="f7c7a-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="f7c7a-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f7c7a-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="f7c7a-110">Return values</span></span>

<span data-ttu-id="f7c7a-111">*Boolesk*</span><span class="sxs-lookup"><span data-stu-id="f7c7a-111">*Boolean*</span></span>

<span data-ttu-id="f7c7a-112">Den resulterende *Booleske* værdi.</span><span class="sxs-lookup"><span data-stu-id="f7c7a-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="f7c7a-113">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="f7c7a-113">Example 1</span></span>

<span data-ttu-id="f7c7a-114">Hvis du indtaster datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("A|B|C", "|")`, returnerer udtrykket `ISEMPTY(DS)` **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="f7c7a-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f7c7a-115">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="f7c7a-115">Example 2</span></span>

<span data-ttu-id="f7c7a-116">Udtrykket `ISEMPTY (SPLIT ("",1))` returnerer **SANDT**.</span><span class="sxs-lookup"><span data-stu-id="f7c7a-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7c7a-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f7c7a-117">Additional resources</span></span>

[<span data-ttu-id="f7c7a-118">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="f7c7a-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]