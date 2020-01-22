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
ms.openlocfilehash: 1cf23f11fa92adfb7a050efd9c68e80e1bee621f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916884"
---
# <span data-ttu-id="2dd26-103"><a name="EMPTYRECORD">ER-funktionen EMPTYRECORD</a></span><span class="sxs-lookup"><span data-stu-id="2dd26-103"><a name="EMPTYRECORD">EMPTYRECORD ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2dd26-104">Funktionen `EMPTYRECORD` returnerer en nulværdi for *Container (post)*, som har samme struktur, som den angivne postliste eller post.</span><span class="sxs-lookup"><span data-stu-id="2dd26-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd26-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="2dd26-105">Syntax</span></span>

```
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="2dd26-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="2dd26-106">Arguments</span></span>

<span data-ttu-id="2dd26-107">`list`: *Postliste* eller *Container (post)*</span><span class="sxs-lookup"><span data-stu-id="2dd26-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="2dd26-108">En datakildes gyldig sti af typen *Postliste* eller *Container (post)*.</span><span class="sxs-lookup"><span data-stu-id="2dd26-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="2dd26-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="2dd26-109">Return values</span></span>

<span data-ttu-id="2dd26-110">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="2dd26-110">*Container (record)*</span></span>

<span data-ttu-id="2dd26-111">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="2dd26-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2dd26-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="2dd26-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="2dd26-113">En null-post er en post, hvor alle felter har en tom værdi.</span><span class="sxs-lookup"><span data-stu-id="2dd26-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="2dd26-114">En tom værdi er **0** (nul) for tal, en tom streng for strenge, osv.</span><span class="sxs-lookup"><span data-stu-id="2dd26-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="2dd26-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2dd26-115">Example</span></span>

<span data-ttu-id="2dd26-116">`EMPTYRECORD (SPLIT ("abc", 1))` returnerer en ny tom post, der har samme struktur som den liste, der er returneret af den anvendte `SPLIT`-funktion.</span><span class="sxs-lookup"><span data-stu-id="2dd26-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="2dd26-117">Yderligere oplysninger finder du under [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="2dd26-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2dd26-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2dd26-118">Additional resources</span></span>

[<span data-ttu-id="2dd26-119">Postfunktioner</span><span class="sxs-lookup"><span data-stu-id="2dd26-119">Record functions</span></span>](er-functions-category-record.md)
