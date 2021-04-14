---
title: ER-funktionen MID
description: Dette emne indeholder oplysninger om, hvordan funktionen MID til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 9a9ff3f1055f6757d6d4073dbb816773d8bfc8ba
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746261"
---
# <a name="mid-er-function"></a><span data-ttu-id="5bb59-103">ER-funktionen MID</span><span class="sxs-lookup"><span data-stu-id="5bb59-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5bb59-104">Funktionen `MID` returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn fra den angivne streng fra begyndelsen af den angivne position.</span><span class="sxs-lookup"><span data-stu-id="5bb59-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bb59-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="5bb59-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="5bb59-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="5bb59-106">Arguments</span></span>

<span data-ttu-id="5bb59-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="5bb59-107">`text`: *String*</span></span>

<span data-ttu-id="5bb59-108">En *Streng*-værdi, som angiver den tekst, der skal returneres tegn fra.</span><span class="sxs-lookup"><span data-stu-id="5bb59-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="5bb59-109">`starting position`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="5bb59-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="5bb59-110">En *Heltals*-værdi, der angiver placeringen af det første tegn, der skal returneres fra den angivne tekst.</span><span class="sxs-lookup"><span data-stu-id="5bb59-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="5bb59-111">`number of characters`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="5bb59-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="5bb59-112">En *Heltals*-værdi, der angiver antallet af tegn, der skal returneres, som starter ved den angivne start.</span><span class="sxs-lookup"><span data-stu-id="5bb59-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="5bb59-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="5bb59-113">Return values</span></span>

<span data-ttu-id="5bb59-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="5bb59-114">*String*</span></span>

<span data-ttu-id="5bb59-115">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="5bb59-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5bb59-116">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="5bb59-116">Usage notes</span></span>

<span data-ttu-id="5bb59-117">Hvis værdien af argumentet `starting position` er mindre end 0 (nul), opgøres antallet af de returnerede tegn fra den første position i den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="5bb59-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="5bb59-118">Hvis værdien af argumentet `starting position` overskrider længden af den angivne streng, returneres en tom streng.</span><span class="sxs-lookup"><span data-stu-id="5bb59-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="5bb59-119">Eksempel</span><span class="sxs-lookup"><span data-stu-id="5bb59-119">Example</span></span>

<span data-ttu-id="5bb59-120">`MID ("Sample", 2, 3)` returnerer **"amp**.</span><span class="sxs-lookup"><span data-stu-id="5bb59-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5bb59-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5bb59-121">Additional resources</span></span>

[<span data-ttu-id="5bb59-122">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="5bb59-122">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]