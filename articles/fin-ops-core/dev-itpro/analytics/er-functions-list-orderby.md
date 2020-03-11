---
title: ER-funktionen ORDERBY
description: Dette emne indeholder oplysninger om, hvordan funktionen ORDERBY til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 0a6b5cddc325625dc5b3d677ffcc1da1f8b829cd
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041946"
---
# <span data-ttu-id="043d4-103"><a name="ORDERBY">ER-funktionen ORDERBY</a></span><span class="sxs-lookup"><span data-stu-id="043d4-103"><a name="ORDERBY">ORDERBY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="043d4-104">Funktionen `ORDERBY` returnerer den angivne liste som en *Postliste*-værdi, efter at den er sorteret i henhold til de angivne argumenter.</span><span class="sxs-lookup"><span data-stu-id="043d4-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="043d4-105">Disse argumenter kan defineres som udtryk.</span><span class="sxs-lookup"><span data-stu-id="043d4-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="043d4-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="043d4-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="043d4-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="043d4-107">Arguments</span></span>

<span data-ttu-id="043d4-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="043d4-108">`list`: *Record list*</span></span>

<span data-ttu-id="043d4-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="043d4-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="043d4-110">`expression 1`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="043d4-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="043d4-111">Den gyldige sti til et felt i datakilden, som `list`-argumentet for den kaldte funktion refererer til.</span><span class="sxs-lookup"><span data-stu-id="043d4-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="043d4-112">Det felt, der refereres til, skal være et felt af den primitive datatype.</span><span class="sxs-lookup"><span data-stu-id="043d4-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="043d4-113">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="043d4-113">This argument is required.</span></span>

<span data-ttu-id="043d4-114">`expression N`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="043d4-114">`expression N`: *Field*</span></span>

<span data-ttu-id="043d4-115">Den gyldige sti til et felt i datakilden, som `list`-argumentet for den kaldte funktion refererer til.</span><span class="sxs-lookup"><span data-stu-id="043d4-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="043d4-116">Det felt, der refereres til, skal være et felt af den primitive datatype.</span><span class="sxs-lookup"><span data-stu-id="043d4-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="043d4-117">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="043d4-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="043d4-118">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="043d4-118">Return values</span></span>

<span data-ttu-id="043d4-119">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="043d4-119">*Record list*</span></span>

<span data-ttu-id="043d4-120">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="043d4-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="043d4-121">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="043d4-121">Example 1</span></span>

<span data-ttu-id="043d4-122">Hvis du indtaster datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("C|B|A", "|")`, returnerer udtrykket `FIRST( ORDERBY( DS, DS. Value)).Value` tekstværdien **"A"**.</span><span class="sxs-lookup"><span data-stu-id="043d4-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="043d4-123">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="043d4-123">Example 2</span></span>

<span data-ttu-id="043d4-124">Hvis **Leverandør** er konfigureret som en datakilde til elektronisk rapportering, der henviser til tabellen VendTable, vil udtrykket `ORDERBY (Vendors, Vendors.'name()')` returnere en liste over leverandører, der er sorteret efter navn i stigende rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="043d4-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="043d4-125">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="043d4-125">Additional resources</span></span>

[<span data-ttu-id="043d4-126">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="043d4-126">List functions</span></span>](er-functions-category-list.md)
