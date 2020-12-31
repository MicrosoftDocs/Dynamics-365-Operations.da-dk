---
title: ER-funktionen FIRSTORNULL
description: Dette emne beskriver, hvordan funktionen FIRSTORNULL til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 11/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 3547eeea3c6fef5cca0699002cc0c35cffd940b3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688037"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="30829-103">ER-funktionen FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="30829-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30829-104">Funktionen `FIRSTORNULL` returnerer den første post på den angivne liste som en *Container (post)*-værdi, hvis denne post ikke er tom.</span><span class="sxs-lookup"><span data-stu-id="30829-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="30829-105">Hvis posten er tom, returnerer denne funktion en nul *Container (post)*-værdi.</span><span class="sxs-lookup"><span data-stu-id="30829-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="30829-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="30829-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="30829-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="30829-107">Arguments</span></span>

<span data-ttu-id="30829-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="30829-108">`list`: *Record list*</span></span>

<span data-ttu-id="30829-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="30829-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="30829-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="30829-110">Return values</span></span>

<span data-ttu-id="30829-111">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="30829-111">*Container (record)*</span></span>

<span data-ttu-id="30829-112">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="30829-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="30829-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="30829-113">Example</span></span>

<span data-ttu-id="30829-114">Udtrykket `FIRSTORNULL(SPLIT("",1)).Value` returnerer en tom streng (**""**).</span><span class="sxs-lookup"><span data-stu-id="30829-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30829-115">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="30829-115">Additional resources</span></span>

[<span data-ttu-id="30829-116">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="30829-116">List functions</span></span>](er-functions-category-list.md)
