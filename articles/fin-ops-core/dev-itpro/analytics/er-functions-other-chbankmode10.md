---
title: ER-funktionen CH_BANK_MOD_10
description: Dette emne indeholder oplysninger om, hvordan funktionen CH_BANK_MOD_10 til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: bca82cd596ba1e3ec42b3dba91ee6c4871ff8601
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686852"
---
# <a name="ch_bank_mod_10-er-function"></a><span data-ttu-id="12a41-103">ER-funktionen CH_BANK_MOD_10</span><span class="sxs-lookup"><span data-stu-id="12a41-103">CH_BANK_MOD_10 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12a41-104">Funktionen `CH_BANK_MOD_10` returnerer en *Streng*-værdi, som repræsenterer en kreditorreference som et MOD10-udtryk, der er baseret på cifrene i det angivne fakturanummer.</span><span class="sxs-lookup"><span data-stu-id="12a41-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="12a41-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="12a41-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="12a41-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="12a41-106">Arguments</span></span>

<span data-ttu-id="12a41-107">`invoice number digits`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="12a41-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="12a41-108">En tekstværdi, der repræsenterer cifrene i et fakturanummer.</span><span class="sxs-lookup"><span data-stu-id="12a41-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="12a41-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="12a41-109">Return values</span></span>

<span data-ttu-id="12a41-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="12a41-110">*String*</span></span>

<span data-ttu-id="12a41-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="12a41-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="12a41-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="12a41-112">Example</span></span>

<span data-ttu-id="12a41-113">`CH_BANK_MOD_10 ("VEND-200002")` returnerer **3**.</span><span class="sxs-lookup"><span data-stu-id="12a41-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12a41-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="12a41-114">Additional resources</span></span>

[<span data-ttu-id="12a41-115">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="12a41-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
