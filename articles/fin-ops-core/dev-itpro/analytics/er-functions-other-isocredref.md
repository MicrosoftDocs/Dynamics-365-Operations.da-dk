---
title: ER-funktionen ISOCREDREF
description: Dette emne indeholder oplysninger om, hvordan funktionen ISOCREDREF til elektronisk rapportering (ER) skal anvendes.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c9a75cedcf543b318df2850df3e4a60bac2dc6b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680680"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="86ce4-103">ER-funktionen ISOCREDREF</span><span class="sxs-lookup"><span data-stu-id="86ce4-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86ce4-104">Funktionen `ISOCREDREF` returnerer en *Streng*-værdi, som repræsenterer en International Organization for Standardization (ISO)-kreditorreference, der er baseret på cifrene og bogstaverne i det angivne fakturanummer.</span><span class="sxs-lookup"><span data-stu-id="86ce4-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="86ce4-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="86ce4-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="86ce4-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="86ce4-106">Arguments</span></span>

<span data-ttu-id="86ce4-107">`invoice number digits`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="86ce4-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="86ce4-108">En tekstværdi, der repræsenterer cifrene i et fakturanummer.</span><span class="sxs-lookup"><span data-stu-id="86ce4-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="86ce4-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="86ce4-109">Return values</span></span>

<span data-ttu-id="86ce4-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="86ce4-110">*String*</span></span>

<span data-ttu-id="86ce4-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="86ce4-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="86ce4-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="86ce4-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="86ce4-113">For at eliminere symboler fra alfabeter, der ikke er ISO-kompatible, skal argumentet `invoice number digits` oversættes, før den videresendes til denne funktion.</span><span class="sxs-lookup"><span data-stu-id="86ce4-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="86ce4-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="86ce4-114">Example</span></span>

<span data-ttu-id="86ce4-115">`ISOCredRef ("VEND-200002")` returnerer **"RF23VEND-200002"**.</span><span class="sxs-lookup"><span data-stu-id="86ce4-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86ce4-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="86ce4-116">Additional resources</span></span>

[<span data-ttu-id="86ce4-117">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="86ce4-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
