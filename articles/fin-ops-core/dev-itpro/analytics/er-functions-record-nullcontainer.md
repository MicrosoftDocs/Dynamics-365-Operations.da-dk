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
ms.openlocfilehash: dac6283ec35d3d03f586ca157048bd3ecc4bfa8a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743921"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="5794e-103">ER-funktionen NULLCONTAINER</span><span class="sxs-lookup"><span data-stu-id="5794e-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5794e-104">Funktionen `NULLCONTAINER` returnerer en nulværdi for *Container (post)*, som har samme struktur, som den angivne postliste eller post.</span><span class="sxs-lookup"><span data-stu-id="5794e-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="5794e-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="5794e-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="5794e-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="5794e-106">Arguments</span></span>

<span data-ttu-id="5794e-107">`list`: *Postliste* eller *Container (post)*</span><span class="sxs-lookup"><span data-stu-id="5794e-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="5794e-108">En datakildes gyldig sti af typen *Postliste* eller *Container (post)*.</span><span class="sxs-lookup"><span data-stu-id="5794e-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="5794e-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="5794e-109">Return values</span></span>

<span data-ttu-id="5794e-110">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="5794e-110">*Container (record)*</span></span>

<span data-ttu-id="5794e-111">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="5794e-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5794e-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="5794e-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="5794e-113">Denne funktion er forældet.</span><span class="sxs-lookup"><span data-stu-id="5794e-113">This function is obsolete.</span></span> <span data-ttu-id="5794e-114">Brug `EMPTYRECORD`-funktionen i stedet.</span><span class="sxs-lookup"><span data-stu-id="5794e-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="5794e-115">Yderligere oplysninger finder du under [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="5794e-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="5794e-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="5794e-116">Example</span></span>

<span data-ttu-id="5794e-117">`NULLCONTAINER (SPLIT ("abc", 1))` returnerer en ny tom post, der har samme struktur som den liste, der er returneret af den anvendte `SPLIT`-funktion.</span><span class="sxs-lookup"><span data-stu-id="5794e-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="5794e-118">Yderligere oplysninger finder du under [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="5794e-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5794e-119">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5794e-119">Additional resources</span></span>

[<span data-ttu-id="5794e-120">Postfunktioner</span><span class="sxs-lookup"><span data-stu-id="5794e-120">Record functions</span></span>](er-functions-category-record.md)
