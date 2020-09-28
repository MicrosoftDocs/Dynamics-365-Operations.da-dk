---
title: ER-funktionen EMPTYLIST
description: Dette emne indeholder oplysninger om, hvordan funktionen EMPTYLIST til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 747b661d0dee4e9c27741e167c89f9ef7eefa470
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745315"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="24a5f-103">ER-funktionen EMPTYLIST</span><span class="sxs-lookup"><span data-stu-id="24a5f-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24a5f-104">Funktionen `EMPTYLIST` returnerer en tom *Postliste*-værdi ved hjælp af den angivne liste som kilde til listestrukturen.</span><span class="sxs-lookup"><span data-stu-id="24a5f-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a5f-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="24a5f-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="24a5f-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="24a5f-106">Arguments</span></span>

<span data-ttu-id="24a5f-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="24a5f-107">`list`: *Record list*</span></span>

<span data-ttu-id="24a5f-108">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="24a5f-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="24a5f-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="24a5f-109">Return values</span></span>

<span data-ttu-id="24a5f-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="24a5f-110">*Record list*</span></span>

<span data-ttu-id="24a5f-111">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="24a5f-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="24a5f-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="24a5f-112">Example</span></span>

<span data-ttu-id="24a5f-113">`EMPTYLIST (SPLIT ("abc", 1))` returnerer en ny tom liste, der har samme struktur som den liste, der er returneret af den anvendte `SPLIT`-funktion.</span><span class="sxs-lookup"><span data-stu-id="24a5f-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24a5f-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="24a5f-114">Additional resources</span></span>

[<span data-ttu-id="24a5f-115">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="24a5f-115">List functions</span></span>](er-functions-category-list.md)
