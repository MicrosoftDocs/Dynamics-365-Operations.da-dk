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
ms.openlocfilehash: e2addace5c5606ebaae56ca658700347978a805b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744713"
---
# <a name="mid-er-function"></a><span data-ttu-id="5071b-103">ER-funktionen MID</span><span class="sxs-lookup"><span data-stu-id="5071b-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5071b-104">Funktionen `MID` returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn fra den angivne streng fra begyndelsen af den angivne position.</span><span class="sxs-lookup"><span data-stu-id="5071b-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="5071b-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="5071b-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="5071b-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="5071b-106">Arguments</span></span>

<span data-ttu-id="5071b-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="5071b-107">`text`: *String*</span></span>

<span data-ttu-id="5071b-108">En *Streng*-værdi, som angiver den tekst, der skal returneres tegn fra.</span><span class="sxs-lookup"><span data-stu-id="5071b-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="5071b-109">`starting position`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="5071b-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="5071b-110">En *Heltals*-værdi, der angiver placeringen af det første tegn, der skal returneres fra den angivne tekst.</span><span class="sxs-lookup"><span data-stu-id="5071b-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="5071b-111">`number of characters`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="5071b-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="5071b-112">En *Heltals*-værdi, der angiver antallet af tegn, der skal returneres, som starter ved den angivne start.</span><span class="sxs-lookup"><span data-stu-id="5071b-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="5071b-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="5071b-113">Return values</span></span>

<span data-ttu-id="5071b-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="5071b-114">*String*</span></span>

<span data-ttu-id="5071b-115">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="5071b-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5071b-116">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="5071b-116">Usage notes</span></span>

<span data-ttu-id="5071b-117">Hvis værdien af argumentet `starting position` er mindre end 0 (nul), opgøres antallet af de returnerede tegn fra den første position i den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="5071b-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="5071b-118">Hvis værdien af argumentet `starting position` overskrider længden af den angivne streng, returneres en tom streng.</span><span class="sxs-lookup"><span data-stu-id="5071b-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="5071b-119">Eksempel</span><span class="sxs-lookup"><span data-stu-id="5071b-119">Example</span></span>

<span data-ttu-id="5071b-120">`MID ("Sample", 2, 3)` returnerer **"amp**.</span><span class="sxs-lookup"><span data-stu-id="5071b-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5071b-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5071b-121">Additional resources</span></span>

[<span data-ttu-id="5071b-122">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="5071b-122">Text functions</span></span>](er-functions-category-text.md)
