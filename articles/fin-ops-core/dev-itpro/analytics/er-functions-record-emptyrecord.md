---
title: ER-funktionen EMPTYRECORD
description: Dette emne indeholder oplysninger om, hvordan funktionen EMPTYRECORD til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 2e46fcef3d53483b782ac39a0661fc0edc8d861c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743944"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="c491f-103">ER-funktionen EMPTYRECORD</span><span class="sxs-lookup"><span data-stu-id="c491f-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c491f-104">Funktionen `EMPTYRECORD` returnerer en nulværdi for *Container (post)*, som har samme struktur, som den angivne postliste eller post.</span><span class="sxs-lookup"><span data-stu-id="c491f-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c491f-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="c491f-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="c491f-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="c491f-106">Arguments</span></span>

<span data-ttu-id="c491f-107">`list`: *Postliste* eller *Container (post)*</span><span class="sxs-lookup"><span data-stu-id="c491f-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="c491f-108">En datakildes gyldig sti af typen *Postliste* eller *Container (post)*.</span><span class="sxs-lookup"><span data-stu-id="c491f-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="c491f-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="c491f-109">Return values</span></span>

<span data-ttu-id="c491f-110">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="c491f-110">*Container (record)*</span></span>

<span data-ttu-id="c491f-111">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="c491f-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c491f-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="c491f-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="c491f-113">En null-post er en post, hvor alle felter har en tom værdi.</span><span class="sxs-lookup"><span data-stu-id="c491f-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="c491f-114">En tom værdi er **0** (nul) for tal, en tom streng for strenge, osv.</span><span class="sxs-lookup"><span data-stu-id="c491f-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="c491f-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="c491f-115">Example</span></span>

<span data-ttu-id="c491f-116">`EMPTYRECORD (SPLIT ("abc", 1))` returnerer en ny tom post, der har samme struktur som den liste, der er returneret af den anvendte `SPLIT`-funktion.</span><span class="sxs-lookup"><span data-stu-id="c491f-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="c491f-117">Yderligere oplysninger finder du under [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="c491f-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c491f-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c491f-118">Additional resources</span></span>

[<span data-ttu-id="c491f-119">Postfunktioner</span><span class="sxs-lookup"><span data-stu-id="c491f-119">Record functions</span></span>](er-functions-category-record.md)
