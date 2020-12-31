---
title: ER-funktionen FA_BALANCE
description: Dette emne indeholder oplysninger om, hvordan funktionen FA_BALANCE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 5570e1295ff6da0eadd7e18143a2206032597ae5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684829"
---
# <a name="fa_balance-er-function"></a><span data-ttu-id="78107-103">ER-funktionen FA_BALANCE</span><span class="sxs-lookup"><span data-stu-id="78107-103">FA_BALANCE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78107-104">Funktionen `FA_BALANCE` returnerer en *Container (post)*-værdi, der består af data for anlægsaktivsaldoen for den angivne anlægsaktivvare, værdimodelkode, rapporteringsår og rapporteringsdato.</span><span class="sxs-lookup"><span data-stu-id="78107-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="78107-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="78107-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="78107-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="78107-106">Arguments</span></span>

<span data-ttu-id="78107-107">`fixed asset code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="78107-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="78107-108">En *Streng*-værdi, der repræsenterer koden for en anlægsaktivvare, som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="78107-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="78107-109">`value model code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="78107-109">`value model code`: *String*</span></span>

<span data-ttu-id="78107-110">En *Streng*-værdi, der repræsenterer koden for en værdimodel, som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="78107-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="78107-111">`reporting year`: *Fasttekstværdi*</span><span class="sxs-lookup"><span data-stu-id="78107-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="78107-112">En fasttekstværdi for programfasttekstgen **AssetYear**, der definerer en periode for saldoberegningen.</span><span class="sxs-lookup"><span data-stu-id="78107-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="78107-113">`reporting date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="78107-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="78107-114">En *Dato*-værdi, der definerer en dato for saldoberegningen.</span><span class="sxs-lookup"><span data-stu-id="78107-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="78107-115">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="78107-115">Return values</span></span>

<span data-ttu-id="78107-116">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="78107-116">*Container (record)*</span></span>

<span data-ttu-id="78107-117">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="78107-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="78107-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78107-118">Example</span></span>

<span data-ttu-id="78107-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returnerer den datacontainer med saldi for anlægsaktivet **COMP-000001**, som er blevet forbedredt for værdimodellen **Aktuel** for den aktuelle programsessionsdato.</span><span class="sxs-lookup"><span data-stu-id="78107-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="78107-120">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="78107-120">Additional resources</span></span>

[<span data-ttu-id="78107-121">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="78107-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
