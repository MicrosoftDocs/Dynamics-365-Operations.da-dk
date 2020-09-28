---
title: ER-funktionen STRINGJOIN
description: Dette emne indeholder oplysninger om, hvordan funktionen STRINGJOIN til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 4f5d6b9a0f43902160d1ff7fa91b86a7e2c3422d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743488"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="d6ce4-103">ER-funktionen STRINGJOIN</span><span class="sxs-lookup"><span data-stu-id="d6ce4-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6ce4-104">Funktionen `STRINGJOIN` returnerer en *Streng*-værdi, der består af sammenføjede værdier for det angivne felt fra den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="d6ce4-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="d6ce4-105">Værdierne kan være adskilt af et angivet separatortegn.</span><span class="sxs-lookup"><span data-stu-id="d6ce4-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6ce4-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="d6ce4-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="d6ce4-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="d6ce4-107">Arguments</span></span>

<span data-ttu-id="d6ce4-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="d6ce4-108">`list`: *Record list*</span></span>

<span data-ttu-id="d6ce4-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="d6ce4-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="d6ce4-110">`field`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="d6ce4-110">`field`: *Field*</span></span>

<span data-ttu-id="d6ce4-111">Den gyldige sti til et felt af datatypen *Streng* på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="d6ce4-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="d6ce4-112">`delimiter`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="d6ce4-112">`delimiter`: *String*</span></span>

<span data-ttu-id="d6ce4-113">En afgrænser, der bruges til at adskille understrenge.</span><span class="sxs-lookup"><span data-stu-id="d6ce4-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="d6ce4-114">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="d6ce4-114">Return values</span></span>

<span data-ttu-id="d6ce4-115">*Streng*</span><span class="sxs-lookup"><span data-stu-id="d6ce4-115">*String*</span></span>

<span data-ttu-id="d6ce4-116">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="d6ce4-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d6ce4-117">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d6ce4-117">Example</span></span>

<span data-ttu-id="d6ce4-118">Hvis du indtaster `SPLIT("abc" , 1)` som datakilde **DS**, returnerer udtrykket `STRINGJOIN (DS, DS.Value, "-")` **"a-b-c"**.</span><span class="sxs-lookup"><span data-stu-id="d6ce4-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d6ce4-119">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="d6ce4-119">Additional resources</span></span>

[<span data-ttu-id="d6ce4-120">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="d6ce4-120">List functions</span></span>](er-functions-category-list.md)
