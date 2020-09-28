---
title: ER-funktionen LISTOFFIRSTITEM
description: Dette emne indeholder oplysninger om, hvordan funktionen LISTOFFIRSTITEM til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 069ec0c6d5578ca6ab68814adf325bd79e73b9e8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745051"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="59c99-103">ER-funktionen LISTOFFIRSTITEM</span><span class="sxs-lookup"><span data-stu-id="59c99-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59c99-104">Funktionen `LISTOFFIRSTITEM` returnerer en ny *Postliste*-værdi, der udelukkende består af de første poster på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="59c99-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="59c99-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="59c99-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="59c99-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="59c99-106">Arguments</span></span>

<span data-ttu-id="59c99-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="59c99-107">`list`: *Record list*</span></span>

<span data-ttu-id="59c99-108">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="59c99-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="59c99-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="59c99-109">Return values</span></span>

<span data-ttu-id="59c99-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="59c99-110">*Record list*</span></span>

<span data-ttu-id="59c99-111">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="59c99-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="59c99-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="59c99-112">Example</span></span>

<span data-ttu-id="59c99-113">Udtrykket `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returnerer tekstværdien **"A"**.</span><span class="sxs-lookup"><span data-stu-id="59c99-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59c99-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="59c99-114">Additional resources</span></span>

[<span data-ttu-id="59c99-115">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="59c99-115">List functions</span></span>](er-functions-category-list.md)
