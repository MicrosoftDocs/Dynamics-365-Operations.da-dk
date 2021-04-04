---
title: ER-funktionen FA_SUM
description: Dette emne indeholder oplysninger om, hvordan funktionen FA_SUM til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c31722537e2a6bae502800953939ca01da4527b9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567562"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="363f2-103">ER-funktionen FA_SUM</span><span class="sxs-lookup"><span data-stu-id="363f2-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="363f2-104">Funktionen `FA_SUM` returnerer en *Container (post)*-værdi, der består af data for anlægsaktivbeløbene for den angivne anlægsaktivvare, værdimodelkode, rapporteringsår og datoperioder.</span><span class="sxs-lookup"><span data-stu-id="363f2-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="363f2-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="363f2-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="363f2-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="363f2-106">Arguments</span></span>

<span data-ttu-id="363f2-107">`fixed asset code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="363f2-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="363f2-108">En *Streng*-værdi, der repræsenterer koden for en anlægsaktivvare, som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="363f2-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="363f2-109">`value model code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="363f2-109">`value model code`: *String*</span></span>

<span data-ttu-id="363f2-110">En *Streng*-værdi, der repræsenterer koden for en værdimodel, som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="363f2-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="363f2-111">`start date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="363f2-111">`start date`: *Date*</span></span>

<span data-ttu-id="363f2-112">En *Dato*-værdi, der repræsenterer startdatoen for en periode, som anlægsaktiv beløbene beregnes for.</span><span class="sxs-lookup"><span data-stu-id="363f2-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="363f2-113">`end date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="363f2-113">`end date`: *Date*</span></span>

<span data-ttu-id="363f2-114">En *Dato*-værdi, der repræsenterer slutdatoen for en periode, som anlægsaktiv beløbene beregnes for.</span><span class="sxs-lookup"><span data-stu-id="363f2-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="363f2-115">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="363f2-115">Return values</span></span>

<span data-ttu-id="363f2-116">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="363f2-116">*Container (record)*</span></span>

<span data-ttu-id="363f2-117">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="363f2-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="363f2-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="363f2-118">Example</span></span>

<span data-ttu-id="363f2-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returnerer datacontaineren for anlægsaktivet **COMP-000001**, der er forberedt for den **Aktuelle** værdimodel og for en periode fra **Dato1** til **Dato2**.</span><span class="sxs-lookup"><span data-stu-id="363f2-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="363f2-120">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="363f2-120">Additional resources</span></span>

[<span data-ttu-id="363f2-121">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="363f2-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]