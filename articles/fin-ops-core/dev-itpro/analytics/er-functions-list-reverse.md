---
title: ER-funktionen REVERSE
description: Dette emne indeholder oplysninger om, hvordan funktionen REVERSE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: ab953136b7500665bdb13e6ff585e3b76896c9ee
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744979"
---
# <a name="reverse-er-function"></a><span data-ttu-id="10277-103">ER-funktionen REVERSE</span><span class="sxs-lookup"><span data-stu-id="10277-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10277-104">Funktionen `REVERSE` returnerer den angivne liste som en *Postliste*-værdi i omvendt sorteringsrækkefølge.</span><span class="sxs-lookup"><span data-stu-id="10277-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="10277-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="10277-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="10277-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="10277-106">Arguments</span></span>

<span data-ttu-id="10277-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="10277-107">`list`: *Record list*</span></span>

<span data-ttu-id="10277-108">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="10277-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="10277-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="10277-109">Return values</span></span>

<span data-ttu-id="10277-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="10277-110">*Record list*</span></span>

<span data-ttu-id="10277-111">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="10277-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="10277-112">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="10277-112">Example 1</span></span>

<span data-ttu-id="10277-113">Hvis du indtaster datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("C|B|A", "|")`, returnerer udtrykket `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` tekstværdien **"C"**.</span><span class="sxs-lookup"><span data-stu-id="10277-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="10277-114">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="10277-114">Example 2</span></span>

<span data-ttu-id="10277-115">Hvis **Leverandør** er konfigureret som en datakilde til elektronisk rapportering, der henviser til tabellen VendTable, vil udtrykket `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returnere en liste over leverandører, der er sorteret efter navn i faldende rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="10277-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10277-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="10277-116">Additional resources</span></span>

[<span data-ttu-id="10277-117">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="10277-117">List functions</span></span>](er-functions-category-list.md)
