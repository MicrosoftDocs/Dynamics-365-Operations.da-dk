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
ms.openlocfilehash: 2395a1932e543e35ced28a2a6e56ab44835de19a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041532"
---
# <span data-ttu-id="8e17f-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">ER-funktionen CN_GBT_ADDITIONALDIMENSIONID</a></span><span class="sxs-lookup"><span data-stu-id="8e17f-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e17f-104">Funktionen `CN_GBT_ADDITIONALDIMENSIONID` returnerer en *Streng*-værdi, som repræsenterer et enkelt økonomisk dimensions-ID, der er hentet fra den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="8e17f-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="8e17f-105">Den angivne streng præsenterer alle dimensioner som en kommasepareret liste over ID'er.</span><span class="sxs-lookup"><span data-stu-id="8e17f-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e17f-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="8e17f-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="8e17f-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="8e17f-107">Arguments</span></span>

<span data-ttu-id="8e17f-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="8e17f-108">`text`: *String*</span></span>

<span data-ttu-id="8e17f-109">En *Streng*-værdi der præsenterer alle dimensioner som en kommasepareret liste over ID'er.</span><span class="sxs-lookup"><span data-stu-id="8e17f-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="8e17f-110">`number`: Heltal</span><span class="sxs-lookup"><span data-stu-id="8e17f-110">`number`: Integer</span></span>

<span data-ttu-id="8e17f-111">En *Heltals*-værdi, der definerer nummerseriekoden for den ønskede dimension i den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="8e17f-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="8e17f-112">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="8e17f-112">Return values</span></span>

<span data-ttu-id="8e17f-113">*Streng*</span><span class="sxs-lookup"><span data-stu-id="8e17f-113">*String*</span></span>

<span data-ttu-id="8e17f-114">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="8e17f-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8e17f-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="8e17f-115">Example</span></span>

<span data-ttu-id="8e17f-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returnerer **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="8e17f-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e17f-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8e17f-117">Additional resources</span></span>

[<span data-ttu-id="8e17f-118">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="8e17f-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
