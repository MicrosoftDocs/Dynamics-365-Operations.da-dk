---
title: ER-funktionen CN_GBT_ADDITIONALDIMENSIONID
description: Dette emne indeholder oplysninger om, hvordan funktionen CN_GBT_ADDITIONALDIMENSIONID til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: df693d745d1fe74b4500dd3fda0cc0c4be21142d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917022"
---
# <span data-ttu-id="91246-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">ER-funktionen CN_GBT_ADDITIONALDIMENSIONID</a></span><span class="sxs-lookup"><span data-stu-id="91246-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91246-104">Funktionen `CN_GBT_ADDITIONALDIMENSIONID` returnerer en *Streng*-værdi, som repræsenterer et enkelt økonomisk dimensions-ID, der er hentet fra den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="91246-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="91246-105">Den angivne streng præsenterer alle dimensioner som en kommasepareret liste over ID'er.</span><span class="sxs-lookup"><span data-stu-id="91246-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="91246-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="91246-106">Syntax</span></span>

```
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="91246-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="91246-107">Arguments</span></span>

<span data-ttu-id="91246-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="91246-108">`text`: *String*</span></span>

<span data-ttu-id="91246-109">En *Streng*-værdi der præsenterer alle dimensioner som en kommasepareret liste over ID'er.</span><span class="sxs-lookup"><span data-stu-id="91246-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="91246-110">`number`: Heltal</span><span class="sxs-lookup"><span data-stu-id="91246-110">`number`: Integer</span></span>

<span data-ttu-id="91246-111">En *Heltals*-værdi, der definerer nummerseriekoden for den ønskede dimension i den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="91246-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="91246-112">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="91246-112">Return values</span></span>

<span data-ttu-id="91246-113">*Streng*</span><span class="sxs-lookup"><span data-stu-id="91246-113">*String*</span></span>

<span data-ttu-id="91246-114">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="91246-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="91246-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="91246-115">Example</span></span>

<span data-ttu-id="91246-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returnerer **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="91246-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91246-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="91246-117">Additional resources</span></span>

[<span data-ttu-id="91246-118">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="91246-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
