---
title: ER-funktionen FA_SUM
description: Dette emne indeholder oplysninger om, hvordan funktionen FA_SUM til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
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
ms.openlocfilehash: d6f380e384e591e7417cfa40c73f9be6575fb0f6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744289"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="82321-103">ER-funktionen FA_SUM</span><span class="sxs-lookup"><span data-stu-id="82321-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82321-104">Funktionen `FA_SUM` returnerer en *Container (post)*-værdi, der består af data for anlægsaktivbeløbene for den angivne anlægsaktivvare, værdimodelkode, rapporteringsår og datoperioder.</span><span class="sxs-lookup"><span data-stu-id="82321-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="82321-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="82321-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="82321-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="82321-106">Arguments</span></span>

<span data-ttu-id="82321-107">`fixed asset code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="82321-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="82321-108">En *Streng*-værdi, der repræsenterer koden for en anlægsaktivvare, som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="82321-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="82321-109">`value model code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="82321-109">`value model code`: *String*</span></span>

<span data-ttu-id="82321-110">En *Streng*-værdi, der repræsenterer koden for en værdimodel, som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="82321-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="82321-111">`start date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="82321-111">`start date`: *Date*</span></span>

<span data-ttu-id="82321-112">En *Dato*-værdi, der repræsenterer startdatoen for en periode, som anlægsaktiv beløbene beregnes for.</span><span class="sxs-lookup"><span data-stu-id="82321-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="82321-113">`end date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="82321-113">`end date`: *Date*</span></span>

<span data-ttu-id="82321-114">En *Dato*-værdi, der repræsenterer slutdatoen for en periode, som anlægsaktiv beløbene beregnes for.</span><span class="sxs-lookup"><span data-stu-id="82321-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="82321-115">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="82321-115">Return values</span></span>

<span data-ttu-id="82321-116">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="82321-116">*Container (record)*</span></span>

<span data-ttu-id="82321-117">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="82321-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="82321-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="82321-118">Example</span></span>

<span data-ttu-id="82321-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returnerer datacontaineren for anlægsaktivet **COMP-000001**, der er forberedt for den **Aktuelle** værdimodel og for en periode fra **Dato1** til **Dato2**.</span><span class="sxs-lookup"><span data-stu-id="82321-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="82321-120">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="82321-120">Additional resources</span></span>

[<span data-ttu-id="82321-121">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="82321-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]