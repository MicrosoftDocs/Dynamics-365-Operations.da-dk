---
title: ER-funktionen NULLCONTAINER
description: Dette emne indeholder oplysninger om, hvordan funktionen NULLCONTAINER til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: d08a4a12d2b142744d3f35c6f1088ec25158c97c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563216"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="bf425-103">ER-funktionen NULLCONTAINER</span><span class="sxs-lookup"><span data-stu-id="bf425-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf425-104">Funktionen `NULLCONTAINER` returnerer en nulværdi for *Container (post)*, som har samme struktur, som den angivne postliste eller post.</span><span class="sxs-lookup"><span data-stu-id="bf425-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf425-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="bf425-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="bf425-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="bf425-106">Arguments</span></span>

<span data-ttu-id="bf425-107">`list`: *Postliste* eller *Container (post)*</span><span class="sxs-lookup"><span data-stu-id="bf425-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="bf425-108">En datakildes gyldig sti af typen *Postliste* eller *Container (post)*.</span><span class="sxs-lookup"><span data-stu-id="bf425-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="bf425-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="bf425-109">Return values</span></span>

<span data-ttu-id="bf425-110">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="bf425-110">*Container (record)*</span></span>

<span data-ttu-id="bf425-111">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="bf425-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bf425-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="bf425-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="bf425-113">Denne funktion er forældet.</span><span class="sxs-lookup"><span data-stu-id="bf425-113">This function is obsolete.</span></span> <span data-ttu-id="bf425-114">Brug `EMPTYRECORD`-funktionen i stedet.</span><span class="sxs-lookup"><span data-stu-id="bf425-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="bf425-115">Yderligere oplysninger finder du under [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="bf425-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="bf425-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="bf425-116">Example</span></span>

<span data-ttu-id="bf425-117">`NULLCONTAINER (SPLIT ("abc", 1))` returnerer en ny tom post, der har samme struktur som den liste, der er returneret af den anvendte `SPLIT`-funktion.</span><span class="sxs-lookup"><span data-stu-id="bf425-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="bf425-118">Yderligere oplysninger finder du under [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="bf425-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bf425-119">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="bf425-119">Additional resources</span></span>

[<span data-ttu-id="bf425-120">Postfunktioner</span><span class="sxs-lookup"><span data-stu-id="bf425-120">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]