---
title: ER-funktionen NULLCONTAINER
description: Dette emne indeholder oplysninger om, hvordan funktionen NULLCONTAINER til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 1dde102acf18e451cb895b51b28d22102f38936c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915780"
---
# <span data-ttu-id="2349d-103"><a name="NULLCONTAINER">ER-funktionen NULLCONTAINER</a></span><span class="sxs-lookup"><span data-stu-id="2349d-103"><a name="NULLCONTAINER">NULLCONTAINER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2349d-104">Funktionen `NULLCONTAINER` returnerer en nulværdi for *Container (post)*, som har samme struktur, som den angivne postliste eller post.</span><span class="sxs-lookup"><span data-stu-id="2349d-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="2349d-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="2349d-105">Syntax</span></span>

```
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="2349d-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="2349d-106">Arguments</span></span>

<span data-ttu-id="2349d-107">`list`: *Postliste* eller *Container (post)*</span><span class="sxs-lookup"><span data-stu-id="2349d-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="2349d-108">En datakildes gyldig sti af typen *Postliste* eller *Container (post)*.</span><span class="sxs-lookup"><span data-stu-id="2349d-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="2349d-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="2349d-109">Return values</span></span>

<span data-ttu-id="2349d-110">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="2349d-110">*Container (record)*</span></span>

<span data-ttu-id="2349d-111">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="2349d-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2349d-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="2349d-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="2349d-113">Denne funktion er forældet.</span><span class="sxs-lookup"><span data-stu-id="2349d-113">This function is obsolete.</span></span> <span data-ttu-id="2349d-114">Brug `EMPTYRECORD`-funktionen i stedet.</span><span class="sxs-lookup"><span data-stu-id="2349d-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="2349d-115">Yderligere oplysninger finder du under [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="2349d-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="2349d-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2349d-116">Example</span></span>

<span data-ttu-id="2349d-117">`NULLCONTAINER (SPLIT ("abc", 1))` returnerer en ny tom post, der har samme struktur som den liste, der er returneret af den anvendte `SPLIT`-funktion.</span><span class="sxs-lookup"><span data-stu-id="2349d-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="2349d-118">Yderligere oplysninger finder du under [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="2349d-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2349d-119">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2349d-119">Additional resources</span></span>

[<span data-ttu-id="2349d-120">Postfunktioner</span><span class="sxs-lookup"><span data-stu-id="2349d-120">Record functions</span></span>](er-functions-category-record.md)
