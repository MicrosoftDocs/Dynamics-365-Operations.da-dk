---
title: ER-funktionen UPPER
description: Dette emne indeholder oplysninger om, hvordan funktionen UPPER til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 8fb89ca48c0035e672b2de6820d6ef08d36c02af
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559983"
---
# <a name="upper-er-function"></a><span data-ttu-id="cdc87-103">ER-funktionen UPPER</span><span class="sxs-lookup"><span data-stu-id="cdc87-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cdc87-104">Funktionen `UPPER` returnerer den angivne tekststreng som en *Streng*-værdi, når den er konverteret til blokbogstaver.</span><span class="sxs-lookup"><span data-stu-id="cdc87-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc87-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="cdc87-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="cdc87-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="cdc87-106">Arguments</span></span>

<span data-ttu-id="cdc87-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="cdc87-107">`text`: *String*</span></span>

<span data-ttu-id="cdc87-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="cdc87-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="cdc87-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="cdc87-109">Return values</span></span>

<span data-ttu-id="cdc87-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="cdc87-110">*String*</span></span>

<span data-ttu-id="cdc87-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="cdc87-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="cdc87-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="cdc87-112">Example</span></span>

<span data-ttu-id="cdc87-113">`UPPER ("Sample")` returnerer **"EKSEMPEL"**.</span><span class="sxs-lookup"><span data-stu-id="cdc87-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cdc87-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="cdc87-114">Additional resources</span></span>

[<span data-ttu-id="cdc87-115">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="cdc87-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]