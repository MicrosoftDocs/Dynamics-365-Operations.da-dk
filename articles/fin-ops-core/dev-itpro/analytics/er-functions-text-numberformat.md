---
title: ER-funktionen NUMBERFORMAT
description: Dette emne indeholder oplysninger om, hvordan funktionen NUMBERFORMAT til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 4a383b3f7c0ca7c4e5afc609cc8a7b1b07021b02
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890377"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="50d32-103">ER-funktionen NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="50d32-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50d32-104">Funktionen `NUMBERFORMAT` returnerer en *Streng*-værdi, som præsenterer det angivne tal i det angivne format og i en eventuelt angivet [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="50d32-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="50d32-105">Oplysninger om understøttede formater finder du under [standard](/dotnet/standard/base-types/standard-numeric-format-strings) og [brugerdefineret](/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="50d32-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-numeric-format-strings) and [custom](/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="50d32-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="50d32-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="50d32-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="50d32-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="50d32-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="50d32-108">Arguments</span></span>

<span data-ttu-id="50d32-109">`number`: *Heltal* eller *Reel*</span><span class="sxs-lookup"><span data-stu-id="50d32-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="50d32-110">En numerisk værdi, der angiver det tal, der skal formateres.</span><span class="sxs-lookup"><span data-stu-id="50d32-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="50d32-111">`format`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="50d32-111">`format` : *String*</span></span>

<span data-ttu-id="50d32-112">En *Streng*-værdi, der repræsenterer formatet.</span><span class="sxs-lookup"><span data-stu-id="50d32-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="50d32-113">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="50d32-113">`culture`: *String*</span></span>

<span data-ttu-id="50d32-114">En *Streng*-værdi, som repræsenterer den kultur, der skal bruges til formatering.</span><span class="sxs-lookup"><span data-stu-id="50d32-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="50d32-115">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="50d32-115">Return values</span></span>

<span data-ttu-id="50d32-116">*Streng*</span><span class="sxs-lookup"><span data-stu-id="50d32-116">*String*</span></span>

<span data-ttu-id="50d32-117">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="50d32-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="50d32-118">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="50d32-118">Usage notes</span></span>

<span data-ttu-id="50d32-119">Hvis kulturen ikke er defineret som et argument for den kaldte funktion, bestemmer den kontekst, som denne funktion køres i, den kultur, der bruges til at formatere tal.</span><span class="sxs-lookup"><span data-stu-id="50d32-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="50d32-120">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="50d32-120">Example 1</span></span>

<span data-ttu-id="50d32-121">For kulturen **EN-US** returnerer `NUMBERFORMAT (0.45, "p")` **"45,00 %"**, og `NUMBERFORMAT (10.45, "#")` returner **"10"**.</span><span class="sxs-lookup"><span data-stu-id="50d32-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="50d32-122">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="50d32-122">Example 2</span></span>

<span data-ttu-id="50d32-123">`NUMBERFORMAT (10/3, "F2", "de")` returnerer **3.33**, mens `NUMBERFORMAT (10/3, "F2", "en-us")` returnerer **3,33**.</span><span class="sxs-lookup"><span data-stu-id="50d32-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="50d32-124">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="50d32-124">Additional resources</span></span>

[<span data-ttu-id="50d32-125">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="50d32-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]