---
title: ER-funktionen LIST
description: Dette emne indeholder oplysninger om, hvordan funktionen LIST til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: a31288885abda69873ae23b28a36e2a54852f593
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745147"
---
# <a name="list-er-function"></a><span data-ttu-id="8caee-103">ER-funktionen LIST</span><span class="sxs-lookup"><span data-stu-id="8caee-103">LIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8caee-104">Funktionen `LIST` returnerer en ny *Postliste*-værdi, der består af en ny postliste, som er oprettet på grundlag af de angivne argumenter.</span><span class="sxs-lookup"><span data-stu-id="8caee-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="8caee-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="8caee-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="8caee-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="8caee-106">Arguments</span></span>

<span data-ttu-id="8caee-107">`record 1`: *Container (post)*</span><span class="sxs-lookup"><span data-stu-id="8caee-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="8caee-108">En reference til en datakilde af datatypen *Post*.</span><span class="sxs-lookup"><span data-stu-id="8caee-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="8caee-109">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="8caee-109">This argument is required.</span></span>

<span data-ttu-id="8caee-110">`record N`: *Container (post)*</span><span class="sxs-lookup"><span data-stu-id="8caee-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="8caee-111">En reference til en datakilde af datatypen *Post*.</span><span class="sxs-lookup"><span data-stu-id="8caee-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="8caee-112">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="8caee-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="8caee-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="8caee-113">Return values</span></span>

<span data-ttu-id="8caee-114">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="8caee-114">*Record list*</span></span>

<span data-ttu-id="8caee-115">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="8caee-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8caee-116">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="8caee-116">Usage notes</span></span>

<span data-ttu-id="8caee-117">Strukturen i den liste, der oprettes, indeholder kun de felter, der vises i strukturen for hver post, der er nævnt i argumenterne.</span><span class="sxs-lookup"><span data-stu-id="8caee-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="8caee-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="8caee-118">Example</span></span>

<span data-ttu-id="8caee-119">Du indtaster datakilde **Post 1** af typen *Container*.</span><span class="sxs-lookup"><span data-stu-id="8caee-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="8caee-120">Denne datakilde indeholder følgende indlejrede felter af typen *Beregnet felt*:</span><span class="sxs-lookup"><span data-stu-id="8caee-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="8caee-121">**Kode:** Dette felt indeholder et udtryk, der returnerer en værdi af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="8caee-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="8caee-122">**Beløb:** Dette felt indeholder et udtryk, der returnerer en værdi af typen *Reel*.</span><span class="sxs-lookup"><span data-stu-id="8caee-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="8caee-123">Du indtaster dernæst datakilde **Post 2** af typen *Container*.</span><span class="sxs-lookup"><span data-stu-id="8caee-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="8caee-124">Denne datakilde indeholder følgende indlejrede felter af typen *Beregnet felt*:</span><span class="sxs-lookup"><span data-stu-id="8caee-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="8caee-125">**Beløb:** Dette felt indeholder et udtryk, der returnerer en værdi af typen *Reel*.</span><span class="sxs-lookup"><span data-stu-id="8caee-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="8caee-126">**IsValid:** Dette felt indeholder et udtryk, der returnerer en værdi af typen *Boolesk*.</span><span class="sxs-lookup"><span data-stu-id="8caee-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="8caee-127">I dette tilfælde returnerer udtrykket `LIST('Record 1', 'Record 2')` en ny liste, der indeholder to poster.</span><span class="sxs-lookup"><span data-stu-id="8caee-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="8caee-128">Strukturen i denne liste består af et enkelt felt for **Beløb** af typen *Reel*, fordi dette felt er det eneste felt, der vises i alle argumenterne for den kaldte funktion.</span><span class="sxs-lookup"><span data-stu-id="8caee-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8caee-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8caee-129">Additional resources</span></span>

[<span data-ttu-id="8caee-130">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="8caee-130">List functions</span></span>](er-functions-category-list.md)
