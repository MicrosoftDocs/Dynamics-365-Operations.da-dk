---
title: ER-funktionen PADLEFT
description: Dette emne indeholder oplysninger om, hvordan funktionen PADLEFT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 86957808ca30db87e6f8202c2024d9929969fc3d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562679"
---
# <a name="padleft-er-function"></a><span data-ttu-id="0400e-103">ER-funktionen PADLEFT</span><span class="sxs-lookup"><span data-stu-id="0400e-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0400e-104">Funktionen `PADLEFT` returnerer en *Streng*-værdi af den angivne længde, hvor begyndelsen af den angivne streng er udfyldt med de angivne tegn.</span><span class="sxs-lookup"><span data-stu-id="0400e-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="0400e-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="0400e-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="0400e-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="0400e-106">Arguments</span></span>

<span data-ttu-id="0400e-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="0400e-107">`text`: *String*</span></span>

<span data-ttu-id="0400e-108">En *Streng*-værdi, der repræsenterer den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="0400e-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="0400e-109">`length`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="0400e-109">`length`: *Integer*</span></span>

<span data-ttu-id="0400e-110">En *Heltals*-værdi, der repræsenterer det endelige antal tegn i den polstrede streng.</span><span class="sxs-lookup"><span data-stu-id="0400e-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="0400e-111">`padding chars`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="0400e-111">`padding chars`: *String*</span></span>

<span data-ttu-id="0400e-112">De tegn, som skal bruges til udfyldning.</span><span class="sxs-lookup"><span data-stu-id="0400e-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="0400e-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="0400e-113">Return values</span></span>

<span data-ttu-id="0400e-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="0400e-114">*String*</span></span>

<span data-ttu-id="0400e-115">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="0400e-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="0400e-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="0400e-116">Example</span></span>

<span data-ttu-id="0400e-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returnerer tekststrengen **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span><span class="sxs-lookup"><span data-stu-id="0400e-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0400e-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="0400e-118">Additional resources</span></span>

[<span data-ttu-id="0400e-119">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="0400e-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]