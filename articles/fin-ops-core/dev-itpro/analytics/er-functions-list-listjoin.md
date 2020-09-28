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
ms.openlocfilehash: 035bf720a892e987ff9fc073ab8ed6f6cc6ea18e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745099"
---
# <a name="listjoin-er-function"></a><span data-ttu-id="4d796-103">LISTJOIN ER-funktion</span><span class="sxs-lookup"><span data-stu-id="4d796-103">LISTJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d796-104">Funktionen `LISTJOIN` returnerer en *Postliste*-værdi, der repræsenterer en ny forenet liste af poster, som er oprettet på grundlag af de angivne argumenter.</span><span class="sxs-lookup"><span data-stu-id="4d796-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d796-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="4d796-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="4d796-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="4d796-106">Arguments</span></span>

<span data-ttu-id="4d796-107">`list 1`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="4d796-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="4d796-108">En reference til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="4d796-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="4d796-109">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="4d796-109">This argument is mandatory.</span></span>

<span data-ttu-id="4d796-110">`list N`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="4d796-110">`list N`: *Record list*</span></span>

<span data-ttu-id="4d796-111">En reference til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="4d796-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="4d796-112">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="4d796-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="4d796-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="4d796-113">Return values</span></span>

<span data-ttu-id="4d796-114">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="4d796-114">*Record list*</span></span>

<span data-ttu-id="4d796-115">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="4d796-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4d796-116">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="4d796-116">Usage notes</span></span>

<span data-ttu-id="4d796-117">Strukturen i den liste, der oprettes, indeholder kun de felter, som findes i strukturen for hver postliste, der er henvist til i argumenterne.</span><span class="sxs-lookup"><span data-stu-id="4d796-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="4d796-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4d796-118">Example</span></span>

<span data-ttu-id="4d796-119">Du indtaster datakilde **Post 1** af typen `Container`.</span><span class="sxs-lookup"><span data-stu-id="4d796-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="4d796-120">Denne datakilde indeholder følgende indlejrede felter af typen `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="4d796-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="4d796-121">**Kode**: Dette felt indeholder et udtryk, der returnerer en værdi af typen `String`.</span><span class="sxs-lookup"><span data-stu-id="4d796-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="4d796-122">**Beløb**: Dette felt indeholder et udtryk, der returnerer en værdi af typen `Real`.</span><span class="sxs-lookup"><span data-stu-id="4d796-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="4d796-123">Du indtaster derefter datakilde **Post 2** af typen `Container`.</span><span class="sxs-lookup"><span data-stu-id="4d796-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="4d796-124">Denne datakilde indeholder følgende indlejrede felter af typen `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="4d796-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="4d796-125">**Beløb**: Dette felt indeholder et udtryk, der returnerer en værdi af typen `Real`.</span><span class="sxs-lookup"><span data-stu-id="4d796-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="4d796-126">**ErGyldig**: Dette felt indeholder et udtryk, der returnerer en værdi af typen `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="4d796-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![Side for ER-modeltilknytningsdesigner](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="4d796-128">I dette tilfælde returnerer udtrykket `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` en ny liste, der indeholder to poster.</span><span class="sxs-lookup"><span data-stu-id="4d796-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![Designerside med to poster til ER-modeltilknytning](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="4d796-130">Strukturen i denne liste består af et enkelt felt for **Beløb** af typen `Real`, fordi dette felt er det eneste felt, der vises i alle argumenterne for den kaldte funktion.</span><span class="sxs-lookup"><span data-stu-id="4d796-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![Designerside med beløbsfelt til ER-modeltilknytning](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="4d796-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="4d796-132">Additional resources</span></span>

[<span data-ttu-id="4d796-133">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="4d796-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="4d796-134">Fejlfinde datakilder for et udført ER-format for at analysere dataflow og -transformering</span><span class="sxs-lookup"><span data-stu-id="4d796-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)
