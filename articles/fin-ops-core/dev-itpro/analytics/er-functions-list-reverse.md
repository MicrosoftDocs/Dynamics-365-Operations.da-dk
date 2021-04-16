---
title: ER-funktionen REVERSE
description: Dette emne indeholder oplysninger om, hvordan funktionen REVERSE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 746a736c8797c1c1c5bd71d7d803be4212984595
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755198"
---
# <a name="reverse-er-function"></a><span data-ttu-id="a3cd7-103">ER-funktionen REVERSE</span><span class="sxs-lookup"><span data-stu-id="a3cd7-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3cd7-104">Funktionen `REVERSE` returnerer den angivne liste som en *Postliste*-værdi i omvendt sorteringsrækkefølge.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3cd7-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="a3cd7-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="a3cd7-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="a3cd7-106">Arguments</span></span>

<span data-ttu-id="a3cd7-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="a3cd7-107">`list`: *Record list*</span></span>

<span data-ttu-id="a3cd7-108">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a3cd7-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="a3cd7-109">Return values</span></span>

<span data-ttu-id="a3cd7-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="a3cd7-110">*Record list*</span></span>

<span data-ttu-id="a3cd7-111">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="a3cd7-112">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="a3cd7-112">Example 1</span></span>

<span data-ttu-id="a3cd7-113">Hvis du indtaster datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("C|B|A", "|")`, returnerer udtrykket `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` tekstværdien **"C"**.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a3cd7-114">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="a3cd7-114">Example 2</span></span>

<span data-ttu-id="a3cd7-115">Hvis **Leverandør** er konfigureret som en datakilde til elektronisk rapportering, der henviser til tabellen VendTable, vil udtrykket `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returnere en liste over leverandører, der er sorteret efter navn i faldende rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a3cd7-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a3cd7-116">Additional resources</span></span>

[<span data-ttu-id="a3cd7-117">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="a3cd7-117">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]