---
title: ER-funktionen NUMBERFORMAT
description: Dette emne indeholder oplysninger om, hvordan funktionen NUMBERFORMAT til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: a05a1e1c4cdb050bff30ea4710da927a537da14c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562703"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="ec8ec-103">ER-funktionen NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="ec8ec-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec8ec-104">Funktionen `NUMBERFORMAT` returnerer en *Streng*-værdi, som præsenterer det angivne tal i det angivne format og i en eventuelt angivet [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="ec8ec-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="ec8ec-105">Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="ec8ec-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="ec8ec-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="ec8ec-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="ec8ec-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="ec8ec-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="ec8ec-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="ec8ec-108">Arguments</span></span>

<span data-ttu-id="ec8ec-109">`number`: *Heltal* eller *Reel*</span><span class="sxs-lookup"><span data-stu-id="ec8ec-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="ec8ec-110">En numerisk værdi, der angiver det tal, der skal formateres.</span><span class="sxs-lookup"><span data-stu-id="ec8ec-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="ec8ec-111">`format`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ec8ec-111">`format` : *String*</span></span>

<span data-ttu-id="ec8ec-112">En *Streng*-værdi, der repræsenterer formatet.</span><span class="sxs-lookup"><span data-stu-id="ec8ec-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="ec8ec-113">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ec8ec-113">`culture`: *String*</span></span>

<span data-ttu-id="ec8ec-114">En *Streng*-værdi, som repræsenterer den kultur, der skal bruges til formatering.</span><span class="sxs-lookup"><span data-stu-id="ec8ec-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="ec8ec-115">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="ec8ec-115">Return values</span></span>

<span data-ttu-id="ec8ec-116">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ec8ec-116">*String*</span></span>

<span data-ttu-id="ec8ec-117">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="ec8ec-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ec8ec-118">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="ec8ec-118">Usage notes</span></span>

<span data-ttu-id="ec8ec-119">Hvis kulturen ikke er defineret som et argument for den kaldte funktion, bestemmer den kontekst, som denne funktion køres i, den kultur, der bruges til at formatere tal.</span><span class="sxs-lookup"><span data-stu-id="ec8ec-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="ec8ec-120">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="ec8ec-120">Example 1</span></span>

<span data-ttu-id="ec8ec-121">For kulturen **EN-US** returnerer `NUMBERFORMAT (0.45, "p")` **"45,00 %"**, og `NUMBERFORMAT (10.45, "#")` returner **"10"**.</span><span class="sxs-lookup"><span data-stu-id="ec8ec-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ec8ec-122">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="ec8ec-122">Example 2</span></span>

<span data-ttu-id="ec8ec-123">`NUMBERFORMAT (10/3, "F2", "de")` returnerer **3.33**, mens `NUMBERFORMAT (10/3, "F2", "en-us")` returnerer **3,33**.</span><span class="sxs-lookup"><span data-stu-id="ec8ec-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec8ec-124">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ec8ec-124">Additional resources</span></span>

[<span data-ttu-id="ec8ec-125">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="ec8ec-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]