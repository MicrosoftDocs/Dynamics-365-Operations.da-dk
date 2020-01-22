---
title: ER-funktionen MID
description: Dette emne indeholder oplysninger om, hvordan funktionen MID til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: e178b01740954b46e2afbd2a2be6200a652a18c0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915596"
---
# <span data-ttu-id="ed61a-103"><a name="MID">ER-funktionen MID</a></span><span class="sxs-lookup"><span data-stu-id="ed61a-103"><a name="MID">MID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed61a-104">Funktionen `MID` returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn fra den angivne streng fra begyndelsen af den angivne position.</span><span class="sxs-lookup"><span data-stu-id="ed61a-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed61a-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="ed61a-105">Syntax</span></span>

```
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="ed61a-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="ed61a-106">Arguments</span></span>

<span data-ttu-id="ed61a-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ed61a-107">`text`: *String*</span></span>

<span data-ttu-id="ed61a-108">En *Streng*-værdi, som angiver den tekst, der skal returneres tegn fra.</span><span class="sxs-lookup"><span data-stu-id="ed61a-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="ed61a-109">`starting position`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="ed61a-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="ed61a-110">En *Heltals*-værdi, der angiver placeringen af det første tegn, der skal returneres fra den angivne tekst.</span><span class="sxs-lookup"><span data-stu-id="ed61a-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="ed61a-111">`number of characters`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="ed61a-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="ed61a-112">En *Heltals*-værdi, der angiver antallet af tegn, der skal returneres, som starter ved den angivne start.</span><span class="sxs-lookup"><span data-stu-id="ed61a-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="ed61a-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="ed61a-113">Return values</span></span>

<span data-ttu-id="ed61a-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ed61a-114">*String*</span></span>

<span data-ttu-id="ed61a-115">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="ed61a-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ed61a-116">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="ed61a-116">Usage notes</span></span>

<span data-ttu-id="ed61a-117">Hvis værdien af argumentet `starting position` er mindre end 0 (nul), opgøres antallet af de returnerede tegn fra den første position i den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="ed61a-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="ed61a-118">Hvis værdien af argumentet `starting position` overskrider længden af den angivne streng, returneres en tom streng.</span><span class="sxs-lookup"><span data-stu-id="ed61a-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="ed61a-119">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ed61a-119">Example</span></span>

<span data-ttu-id="ed61a-120">`MID ("Sample", 2, 3)` returnerer **"amp**.</span><span class="sxs-lookup"><span data-stu-id="ed61a-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ed61a-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ed61a-121">Additional resources</span></span>

[<span data-ttu-id="ed61a-122">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="ed61a-122">Text functions</span></span>](er-functions-category-text.md)
