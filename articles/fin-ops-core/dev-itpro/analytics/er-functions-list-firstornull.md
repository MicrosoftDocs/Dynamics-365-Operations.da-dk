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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e360812c5b0dbfb8df4ab279bf3e0050acebbb25
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745191"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="f9a9b-103">ER-funktionen FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="f9a9b-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9a9b-104">Funktionen `FIRSTORNULL` returnerer den første post på den angivne liste som en *Container (post)*-værdi, hvis denne post ikke er tom.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="f9a9b-105">Hvis posten er tom, returnerer denne funktion en nul *Container (post)*-værdi.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9a9b-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f9a9b-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="f9a9b-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="f9a9b-107">Arguments</span></span>

<span data-ttu-id="f9a9b-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="f9a9b-108">`list`: *Record list*</span></span>

<span data-ttu-id="f9a9b-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f9a9b-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="f9a9b-110">Return values</span></span>

<span data-ttu-id="f9a9b-111">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="f9a9b-111">*Container (record)*</span></span>

<span data-ttu-id="f9a9b-112">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="f9a9b-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="f9a9b-113">Example</span></span>

<span data-ttu-id="f9a9b-114">Udtrykket `FIRSTORNULL(SPLIT("",1)).Value` returnerer en tom streng (**""**).</span><span class="sxs-lookup"><span data-stu-id="f9a9b-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9a9b-115">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f9a9b-115">Additional resources</span></span>

[<span data-ttu-id="f9a9b-116">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="f9a9b-116">List functions</span></span>](er-functions-category-list.md)
