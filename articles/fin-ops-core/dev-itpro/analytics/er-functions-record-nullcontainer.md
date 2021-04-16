---
title: ER-funktionen NULLCONTAINER
description: Dette emne indeholder oplysninger om, hvordan funktionen NULLCONTAINER til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
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
ms.openlocfilehash: af6651ef3c62bd8d1285fa8179ac923d3c333ce7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746501"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="6fc57-103">ER-funktionen NULLCONTAINER</span><span class="sxs-lookup"><span data-stu-id="6fc57-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fc57-104">Funktionen `NULLCONTAINER` returnerer en nulværdi for *Container (post)*, som har samme struktur, som den angivne postliste eller post.</span><span class="sxs-lookup"><span data-stu-id="6fc57-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fc57-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="6fc57-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="6fc57-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="6fc57-106">Arguments</span></span>

<span data-ttu-id="6fc57-107">`list`: *Postliste* eller *Container (post)*</span><span class="sxs-lookup"><span data-stu-id="6fc57-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="6fc57-108">En datakildes gyldig sti af typen *Postliste* eller *Container (post)*.</span><span class="sxs-lookup"><span data-stu-id="6fc57-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="6fc57-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="6fc57-109">Return values</span></span>

<span data-ttu-id="6fc57-110">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="6fc57-110">*Container (record)*</span></span>

<span data-ttu-id="6fc57-111">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="6fc57-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6fc57-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="6fc57-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="6fc57-113">Denne funktion er forældet.</span><span class="sxs-lookup"><span data-stu-id="6fc57-113">This function is obsolete.</span></span> <span data-ttu-id="6fc57-114">Brug `EMPTYRECORD`-funktionen i stedet.</span><span class="sxs-lookup"><span data-stu-id="6fc57-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="6fc57-115">Yderligere oplysninger finder du under [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="6fc57-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="6fc57-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="6fc57-116">Example</span></span>

<span data-ttu-id="6fc57-117">`NULLCONTAINER (SPLIT ("abc", 1))` returnerer en ny tom post, der har samme struktur som den liste, der er returneret af den anvendte `SPLIT`-funktion.</span><span class="sxs-lookup"><span data-stu-id="6fc57-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="6fc57-118">Yderligere oplysninger finder du under [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="6fc57-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6fc57-119">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6fc57-119">Additional resources</span></span>

[<span data-ttu-id="6fc57-120">Postfunktioner</span><span class="sxs-lookup"><span data-stu-id="6fc57-120">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]