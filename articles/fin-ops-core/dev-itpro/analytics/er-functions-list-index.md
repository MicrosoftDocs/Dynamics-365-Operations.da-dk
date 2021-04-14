---
title: ER-funktionen INDEX
description: Dette emne indeholder oplysninger om, hvordan funktionen INDEX til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 14f10359a3f20fb9d23639babce764b9ef64243d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750454"
---
# <a name="index-er-function"></a><span data-ttu-id="03fc0-103">ER-funktionen INDEX</span><span class="sxs-lookup"><span data-stu-id="03fc0-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03fc0-104">Funktionen `INDEX` returnerer en *Container (post)*-værdi, der er valgt ved hjælp af det angivne numeriske indeks på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="03fc0-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="03fc0-105">Der udløses en undtagelse, hvis indekset er uden for området for posterne på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="03fc0-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="03fc0-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="03fc0-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="03fc0-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="03fc0-107">Arguments</span></span>

<span data-ttu-id="03fc0-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="03fc0-108">`list`: *Record list*</span></span>

<span data-ttu-id="03fc0-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="03fc0-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="03fc0-110">`index`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="03fc0-110">`index`: *Integer*</span></span>

<span data-ttu-id="03fc0-111">Et numerisk indeks, der angiver placeringen af den ønskede post på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="03fc0-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="03fc0-112">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="03fc0-112">Return values</span></span>

<span data-ttu-id="03fc0-113">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="03fc0-113">*Container (record)*</span></span>

<span data-ttu-id="03fc0-114">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="03fc0-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="03fc0-115">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="03fc0-115">Example 1</span></span>

<span data-ttu-id="03fc0-116">Hvis du angiver datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("A|B|C", "|")`, returnerer udtrykket `DS.Value` tekstværdien **"B"** for den anden post på denne postliste.</span><span class="sxs-lookup"><span data-stu-id="03fc0-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="03fc0-117">Udtrykket `INDEX (SPLIT ("A|B|C", "|"), 2).Value` returnerer også tekstværdien **"B"**.</span><span class="sxs-lookup"><span data-stu-id="03fc0-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="03fc0-118">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="03fc0-118">Example 2</span></span>

<span data-ttu-id="03fc0-119">Hvis du indtaster datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("A|B|C", "|")`, udløser udtrykket `INDEX (SPLIT ("A|B|C", "|"), 4).Value` en undtagelse under kørslen.</span><span class="sxs-lookup"><span data-stu-id="03fc0-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03fc0-120">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="03fc0-120">Additional resources</span></span>

[<span data-ttu-id="03fc0-121">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="03fc0-121">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]