---
title: ER-funktionen FA_SUM
description: Dette emne indeholder oplysninger om, hvordan funktionen FA_SUM til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 1c46f945a9caae2836886d051da820658e8be9af
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687690"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="950b6-103">ER-funktionen FA_SUM</span><span class="sxs-lookup"><span data-stu-id="950b6-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="950b6-104">Funktionen `FA_SUM` returnerer en *Container (post)*-værdi, der består af data for anlægsaktivbeløbene for den angivne anlægsaktivvare, værdimodelkode, rapporteringsår og datoperioder.</span><span class="sxs-lookup"><span data-stu-id="950b6-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="950b6-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="950b6-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="950b6-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="950b6-106">Arguments</span></span>

<span data-ttu-id="950b6-107">`fixed asset code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="950b6-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="950b6-108">En *Streng*-værdi, der repræsenterer koden for en anlægsaktivvare, som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="950b6-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="950b6-109">`value model code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="950b6-109">`value model code`: *String*</span></span>

<span data-ttu-id="950b6-110">En *Streng*-værdi, der repræsenterer koden for en værdimodel, som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="950b6-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="950b6-111">`start date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="950b6-111">`start date`: *Date*</span></span>

<span data-ttu-id="950b6-112">En *Dato*-værdi, der repræsenterer startdatoen for en periode, som anlægsaktiv beløbene beregnes for.</span><span class="sxs-lookup"><span data-stu-id="950b6-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="950b6-113">`end date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="950b6-113">`end date`: *Date*</span></span>

<span data-ttu-id="950b6-114">En *Dato*-værdi, der repræsenterer slutdatoen for en periode, som anlægsaktiv beløbene beregnes for.</span><span class="sxs-lookup"><span data-stu-id="950b6-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="950b6-115">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="950b6-115">Return values</span></span>

<span data-ttu-id="950b6-116">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="950b6-116">*Container (record)*</span></span>

<span data-ttu-id="950b6-117">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="950b6-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="950b6-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="950b6-118">Example</span></span>

<span data-ttu-id="950b6-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returnerer datacontaineren for anlægsaktivet **COMP-000001**, der er forberedt for den **Aktuelle** værdimodel og for en periode fra **Dato1** til **Dato2**.</span><span class="sxs-lookup"><span data-stu-id="950b6-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="950b6-120">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="950b6-120">Additional resources</span></span>

[<span data-ttu-id="950b6-121">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="950b6-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
