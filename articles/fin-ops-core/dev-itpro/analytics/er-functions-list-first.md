---
title: ER-funktionen FIRST
description: Dette emne indeholder oplysninger om, hvordan funktionen FIRST til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 3ed0e0aaf29e2a67a4842d71121f1adc24f524f7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745219"
---
# <a name="first-er-function"></a><span data-ttu-id="cd265-103">ER-funktionen FIRST</span><span class="sxs-lookup"><span data-stu-id="cd265-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd265-104">Funktionen `FIRST` returnerer den første post på den angivne liste som en *Container (post)*-værdi, hvis denne liste ikke er tom.</span><span class="sxs-lookup"><span data-stu-id="cd265-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="cd265-105">Hvis listen er tom, udløser denne funktion en undtagelse.</span><span class="sxs-lookup"><span data-stu-id="cd265-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd265-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="cd265-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="cd265-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="cd265-107">Arguments</span></span>

<span data-ttu-id="cd265-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="cd265-108">`list`: *Record list*</span></span>

<span data-ttu-id="cd265-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="cd265-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="cd265-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="cd265-110">Return values</span></span>

<span data-ttu-id="cd265-111">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="cd265-111">*Container (record)*</span></span>

<span data-ttu-id="cd265-112">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="cd265-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="cd265-113">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="cd265-113">Example 1</span></span>

<span data-ttu-id="cd265-114">Udtrykket `FIRST(SPLIT("ABC",1)).Value` returnerer tekstværdien **"A"**.</span><span class="sxs-lookup"><span data-stu-id="cd265-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="cd265-115">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="cd265-115">Example 2</span></span>

<span data-ttu-id="cd265-116">Udtrykket `FIRST(SPLIT("",1)).Value` udløser en undtagelse under kørslen.</span><span class="sxs-lookup"><span data-stu-id="cd265-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cd265-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="cd265-117">Additional resources</span></span>

[<span data-ttu-id="cd265-118">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="cd265-118">List functions</span></span>](er-functions-category-list.md)
