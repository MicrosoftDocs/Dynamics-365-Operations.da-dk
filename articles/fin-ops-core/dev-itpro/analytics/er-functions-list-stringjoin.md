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
ms.openlocfilehash: 99d50313f8097d43b820ffc1c36eef0097e7ec55
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917183"
---
# <span data-ttu-id="81ea2-103"><a name="STRINGJOIN">ER-funktionen STRINGJOIN</a></span><span class="sxs-lookup"><span data-stu-id="81ea2-103"><a name="STRINGJOIN">STRINGJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81ea2-104">Funktionen `STRINGJOIN` returnerer en *Streng*-værdi, der består af sammenføjede værdier for det angivne felt fra den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="81ea2-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="81ea2-105">Værdierne kan være adskilt af et angivet separatortegn.</span><span class="sxs-lookup"><span data-stu-id="81ea2-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="81ea2-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="81ea2-106">Syntax</span></span>

```
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="81ea2-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="81ea2-107">Arguments</span></span>

<span data-ttu-id="81ea2-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="81ea2-108">`list`: *Record list*</span></span>

<span data-ttu-id="81ea2-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="81ea2-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="81ea2-110">`field`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="81ea2-110">`field`: *Field*</span></span>

<span data-ttu-id="81ea2-111">Den gyldige sti til et felt af datatypen *Streng* på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="81ea2-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="81ea2-112">`delimiter`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="81ea2-112">`delimiter`: *String*</span></span>

<span data-ttu-id="81ea2-113">En afgrænser, der bruges til at adskille understrenge.</span><span class="sxs-lookup"><span data-stu-id="81ea2-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="81ea2-114">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="81ea2-114">Return values</span></span>

<span data-ttu-id="81ea2-115">*Streng*</span><span class="sxs-lookup"><span data-stu-id="81ea2-115">*String*</span></span>

<span data-ttu-id="81ea2-116">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="81ea2-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="81ea2-117">Eksempel</span><span class="sxs-lookup"><span data-stu-id="81ea2-117">Example</span></span>

<span data-ttu-id="81ea2-118">Hvis du indtaster `SPLIT("abc" , 1)` som datakilde **DS**, returnerer udtrykket `STRINGJOIN (DS, DS.Value, "-")` **"a-b-c"**.</span><span class="sxs-lookup"><span data-stu-id="81ea2-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81ea2-119">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="81ea2-119">Additional resources</span></span>

[<span data-ttu-id="81ea2-120">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="81ea2-120">List functions</span></span>](er-functions-category-list.md)
