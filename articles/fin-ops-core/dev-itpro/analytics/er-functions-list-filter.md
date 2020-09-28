---
title: ER-funktionen FILTER
description: Dette emne indeholder oplysninger om, hvordan funktionen FILTER til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: d281fe710381b0ecb075a0d9281d46bd6edf987d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745291"
---
# <a name="filter-er-function"></a><span data-ttu-id="f41ac-103">ER-funktionen FILTER</span><span class="sxs-lookup"><span data-stu-id="f41ac-103">FILTER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f41ac-104">Funktionen `FILTER` returnerer den angivne liste som en *Postliste*-værdi, når forespørgslen er blevet ændret, så den filtrerer for den angivne betingelse.</span><span class="sxs-lookup"><span data-stu-id="f41ac-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="f41ac-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f41ac-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="f41ac-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="f41ac-106">Arguments</span></span>

<span data-ttu-id="f41ac-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="f41ac-107">`list`: *Record list*</span></span>

<span data-ttu-id="f41ac-108">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="f41ac-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="f41ac-109">`condition`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="f41ac-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="f41ac-110">Et gyldigt betinget udtryk, der bruges til at filtrere poster på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="f41ac-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="f41ac-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="f41ac-111">Return values</span></span>

<span data-ttu-id="f41ac-112">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="f41ac-112">*Record list*</span></span>

<span data-ttu-id="f41ac-113">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="f41ac-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f41ac-114">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="f41ac-114">Usage notes</span></span>

<span data-ttu-id="f41ac-115">Denne funktion adskiller sig fra funktionen [WHERE](er-functions-list-where.md), fordi den angivne betingelse anvendes på enhver elektronisk rapporteringsdatakilde (ER-datakilde) af typen *Tabelposter* på databaseniveau.</span><span class="sxs-lookup"><span data-stu-id="f41ac-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="f41ac-116">Listen og betingelse kan defineres ved hjælp af tabeller og relationer.</span><span class="sxs-lookup"><span data-stu-id="f41ac-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="f41ac-117">Hvis et eller begge argumenter, der er konfigureret for denne funktion (`list` og `condition`), ikke tillader, at denne anmodning oversættes til det direkte SQL-kald, bliver der udløst en undtagelse på designtidspunktet.</span><span class="sxs-lookup"><span data-stu-id="f41ac-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="f41ac-118">Denne undtagelse informerer brugeren om, at enten `list` eller `condition` ikke kan bruges til at forespørge på databasen.</span><span class="sxs-lookup"><span data-stu-id="f41ac-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="f41ac-119">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="f41ac-119">Example 1</span></span>

<span data-ttu-id="f41ac-120">Hvis **Leverandør** er konfigureret som en ER-datakilde, der henviser til tabellen VendTable, vil udtrykket `FILTER (Vendors, Vendors.VendGroup = "40")` alene returnere en liste over de leverandører, der tilhører leverandørgruppe 40.</span><span class="sxs-lookup"><span data-stu-id="f41ac-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="f41ac-121">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="f41ac-121">Example 2</span></span>

<span data-ttu-id="f41ac-122">Hvis **Leverandør** er konfigureret som en ER-datakilde, der henviser til VendTable-tabellen, og hvis **parmVendorBankGroup** er konfigureret som en ER-datakilde, der returnerer en værdi af datatypen *Streng*, returnerer udtrykket `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` alene en liste over de leverandørkonti, der tilhører en bestemt bankgruppe.</span><span class="sxs-lookup"><span data-stu-id="f41ac-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="f41ac-123">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="f41ac-123">Example 3</span></span>

<span data-ttu-id="f41ac-124">Du indtaster datakilden **DS** af typen *Beregnet felt* og deri er indeholdt udtrykket `SPLIT ("A,B,C", ",")`.</span><span class="sxs-lookup"><span data-stu-id="f41ac-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="f41ac-125">Derefter indtaster du et andet udtryk `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="f41ac-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="f41ac-126">Når du forsøger at gemme dette udtryk i ER-formeldesigneren, bliver følgende undtagelse udløst: "Valideringsfejl: der kan ikke forespørges på listeudtrykket for funktionen FILTER."</span><span class="sxs-lookup"><span data-stu-id="f41ac-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f41ac-127">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f41ac-127">Additional resources</span></span>

[<span data-ttu-id="f41ac-128">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="f41ac-128">List functions</span></span>](er-functions-category-list.md)
