---
title: ER-funktionen CN_GBT_ADDITIONALDIMENSIONID
description: Dette emne indeholder oplysninger om, hvordan funktionen CN_GBT_ADDITIONALDIMENSIONID til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: ac0b54476265171b3826e43600f99097701231e1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744385"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="bc5d4-103">ER-funktionen CN_GBT_ADDITIONALDIMENSIONID</span><span class="sxs-lookup"><span data-stu-id="bc5d4-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc5d4-104">Funktionen `CN_GBT_ADDITIONALDIMENSIONID` returnerer en *Streng*-værdi, som repræsenterer et enkelt økonomisk dimensions-ID, der er hentet fra den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="bc5d4-105">Den angivne streng præsenterer alle dimensioner som en kommasepareret liste over ID'er.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc5d4-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="bc5d4-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="bc5d4-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="bc5d4-107">Arguments</span></span>

<span data-ttu-id="bc5d4-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="bc5d4-108">`text`: *String*</span></span>

<span data-ttu-id="bc5d4-109">En *Streng*-værdi der præsenterer alle dimensioner som en kommasepareret liste over ID'er.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="bc5d4-110">`number`: Heltal</span><span class="sxs-lookup"><span data-stu-id="bc5d4-110">`number`: Integer</span></span>

<span data-ttu-id="bc5d4-111">En *Heltals*-værdi, der definerer nummerseriekoden for den ønskede dimension i den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="bc5d4-112">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="bc5d4-112">Return values</span></span>

<span data-ttu-id="bc5d4-113">*Streng*</span><span class="sxs-lookup"><span data-stu-id="bc5d4-113">*String*</span></span>

<span data-ttu-id="bc5d4-114">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="bc5d4-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="bc5d4-115">Example</span></span>

<span data-ttu-id="bc5d4-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returnerer **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc5d4-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="bc5d4-117">Additional resources</span></span>

[<span data-ttu-id="bc5d4-118">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="bc5d4-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]