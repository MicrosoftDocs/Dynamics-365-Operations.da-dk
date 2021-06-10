---
title: ER-funktionen INDEX
description: Dette emne indeholder oplysninger om, hvordan funktionen INDEX til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087745"
---
# <a name="index-er-function"></a><span data-ttu-id="33d9e-103">ER-funktionen INDEX</span><span class="sxs-lookup"><span data-stu-id="33d9e-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33d9e-104">Funktionen `INDEX` returnerer en *Container (post)*-værdi, der er valgt ved hjælp af det angivne numeriske indeks på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="33d9e-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="33d9e-105">Der udløses en undtagelse, hvis indekset er uden for området for posterne på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="33d9e-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="33d9e-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="33d9e-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="33d9e-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="33d9e-107">Arguments</span></span>

<span data-ttu-id="33d9e-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="33d9e-108">`list`: *Record list*</span></span>

<span data-ttu-id="33d9e-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="33d9e-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="33d9e-110">`index`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="33d9e-110">`index`: *Integer*</span></span>

<span data-ttu-id="33d9e-111">Et numerisk indeks, der angiver placeringen af den ønskede post på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="33d9e-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

> [!NOTE]
> <span data-ttu-id="33d9e-112">Da der bruges ettalsbaseret nummerering til denne funktion, skal du angive værdien **1** for at returnere den første post på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="33d9e-112">Because one-based numbering is used for this function, specify the value **1** to return the first record of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="33d9e-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="33d9e-113">Return values</span></span>

<span data-ttu-id="33d9e-114">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="33d9e-114">*Container (record)*</span></span>

<span data-ttu-id="33d9e-115">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="33d9e-115">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="33d9e-116">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="33d9e-116">Example 1</span></span>

<span data-ttu-id="33d9e-117">Hvis du angiver datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("A|B|C", "|")`, returnerer udtrykket `DS.Value` tekstværdien **"B"** for den anden post på denne postliste.</span><span class="sxs-lookup"><span data-stu-id="33d9e-117">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="33d9e-118">Udtrykket `INDEX (SPLIT ("A|B|C", "|"), 2).Value` returnerer også tekstværdien **"B"**.</span><span class="sxs-lookup"><span data-stu-id="33d9e-118">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="33d9e-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="33d9e-119">Example 2</span></span>

<span data-ttu-id="33d9e-120">Hvis du indtaster datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("A|B|C", "|")`, udløser udtrykket `INDEX (SPLIT ("A|B|C", "|"), 4).Value` en undtagelse under kørslen.</span><span class="sxs-lookup"><span data-stu-id="33d9e-120">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33d9e-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="33d9e-121">Additional resources</span></span>

[<span data-ttu-id="33d9e-122">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="33d9e-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
