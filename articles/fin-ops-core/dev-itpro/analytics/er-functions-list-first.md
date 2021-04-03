---
title: ER-funktionen FIRST
description: Dette emne indeholder oplysninger om, hvordan funktionen FIRST til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: ec94a27776cf1069b50b5437f4d167019fdef120
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564729"
---
# <a name="first-er-function"></a><span data-ttu-id="14068-103">ER-funktionen FIRST</span><span class="sxs-lookup"><span data-stu-id="14068-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14068-104">Funktionen `FIRST` returnerer den første post på den angivne liste som en *Container (post)*-værdi, hvis denne liste ikke er tom.</span><span class="sxs-lookup"><span data-stu-id="14068-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="14068-105">Hvis listen er tom, udløser denne funktion en undtagelse.</span><span class="sxs-lookup"><span data-stu-id="14068-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="14068-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="14068-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="14068-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="14068-107">Arguments</span></span>

<span data-ttu-id="14068-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="14068-108">`list`: *Record list*</span></span>

<span data-ttu-id="14068-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="14068-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="14068-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="14068-110">Return values</span></span>

<span data-ttu-id="14068-111">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="14068-111">*Container (record)*</span></span>

<span data-ttu-id="14068-112">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="14068-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="14068-113">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="14068-113">Example 1</span></span>

<span data-ttu-id="14068-114">Udtrykket `FIRST(SPLIT("ABC",1)).Value` returnerer tekstværdien **"A"**.</span><span class="sxs-lookup"><span data-stu-id="14068-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="14068-115">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="14068-115">Example 2</span></span>

<span data-ttu-id="14068-116">Udtrykket `FIRST(SPLIT("",1)).Value` udløser en undtagelse under kørslen.</span><span class="sxs-lookup"><span data-stu-id="14068-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14068-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="14068-117">Additional resources</span></span>

[<span data-ttu-id="14068-118">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="14068-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]