---
title: LISTJOIN ER-funktion
description: Dette emne indeholder oplysninger om, hvordan funktionen LISTJOIN til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249029"
---
# <a name=""></a><span data-ttu-id="f3ee1-103"><a name="LISTJOIN">LISTJOIN ER-funktion</a></span><span class="sxs-lookup"><span data-stu-id="f3ee1-103"><a name="LISTJOIN">LISTJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3ee1-104">Funktionen `LISTJOIN` returnerer en *Postliste*-værdi, der repræsenterer en ny forenet liste af poster, som er oprettet på grundlag af de angivne argumenter.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3ee1-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f3ee1-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="f3ee1-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="f3ee1-106">Arguments</span></span>

<span data-ttu-id="f3ee1-107">`list 1`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="f3ee1-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="f3ee1-108">En reference til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="f3ee1-109">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-109">This argument is mandatory.</span></span>

<span data-ttu-id="f3ee1-110">`list N`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="f3ee1-110">`list N`: *Record list*</span></span>

<span data-ttu-id="f3ee1-111">En reference til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="f3ee1-112">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="f3ee1-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="f3ee1-113">Return values</span></span>

<span data-ttu-id="f3ee1-114">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="f3ee1-114">*Record list*</span></span>

<span data-ttu-id="f3ee1-115">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f3ee1-116">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="f3ee1-116">Usage notes</span></span>

<span data-ttu-id="f3ee1-117">Strukturen i den liste, der oprettes, indeholder kun de felter, som findes i strukturen for hver postliste, der er henvist til i argumenterne.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="f3ee1-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="f3ee1-118">Example</span></span>

<span data-ttu-id="f3ee1-119">Du indtaster datakilde **Post 1** af typen `Container`.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="f3ee1-120">Denne datakilde indeholder følgende indlejrede felter af typen `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="f3ee1-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="f3ee1-121">**Kode**: Dette felt indeholder et udtryk, der returnerer en værdi af typen `String`.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="f3ee1-122">**Beløb**: Dette felt indeholder et udtryk, der returnerer en værdi af typen `Real`.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="f3ee1-123">Du indtaster derefter datakilde **Post 2** af typen `Container`.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="f3ee1-124">Denne datakilde indeholder følgende indlejrede felter af typen `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="f3ee1-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="f3ee1-125">**Beløb**: Dette felt indeholder et udtryk, der returnerer en værdi af typen `Real`.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="f3ee1-126">**ErGyldig**: Dette felt indeholder et udtryk, der returnerer en værdi af typen `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

<span data-ttu-id="f3ee1-127">I dette tilfælde returnerer udtrykket `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` en ny liste, der indeholder to poster.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-127">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span> <span data-ttu-id="f3ee1-128">Strukturen i denne liste består af et enkelt felt for **Beløb** af typen `Real`, fordi dette felt er det eneste felt, der vises i alle argumenterne for den kaldte funktion.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-128">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3ee1-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f3ee1-129">Additional resources</span></span>

[<span data-ttu-id="f3ee1-130">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="f3ee1-130">List functions</span></span>](er-functions-category-list.md)
