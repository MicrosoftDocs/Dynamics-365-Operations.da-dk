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
ms.openlocfilehash: a6134ae7eb1a8044cf906f2a8d02eb153522a6cf
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041923"
---
# <span data-ttu-id="f4ed4-103"><a name="REVERSE">ER-funktionen REVERSE</a></span><span class="sxs-lookup"><span data-stu-id="f4ed4-103"><a name="REVERSE">REVERSE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4ed4-104">Funktionen `REVERSE` returnerer den angivne liste som en *Postliste*-værdi i omvendt sorteringsrækkefølge.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ed4-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f4ed4-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="f4ed4-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="f4ed4-106">Arguments</span></span>

<span data-ttu-id="f4ed4-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="f4ed4-107">`list`: *Record list*</span></span>

<span data-ttu-id="f4ed4-108">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f4ed4-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="f4ed4-109">Return values</span></span>

<span data-ttu-id="f4ed4-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="f4ed4-110">*Record list*</span></span>

<span data-ttu-id="f4ed4-111">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="f4ed4-112">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="f4ed4-112">Example 1</span></span>

<span data-ttu-id="f4ed4-113">Hvis du indtaster datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("C|B|A", "|")`, returnerer udtrykket `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` tekstværdien **"C"**.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f4ed4-114">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="f4ed4-114">Example 2</span></span>

<span data-ttu-id="f4ed4-115">Hvis **Leverandør** er konfigureret som en datakilde til elektronisk rapportering, der henviser til tabellen VendTable, vil udtrykket `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returnere en liste over leverandører, der er sorteret efter navn i faldende rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4ed4-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f4ed4-116">Additional resources</span></span>

[<span data-ttu-id="f4ed4-117">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="f4ed4-117">List functions</span></span>](er-functions-category-list.md)
