---
title: ER-funktionen FA_BALANCE
description: Dette emne indeholder oplysninger om, hvordan funktionen FA_BALANCE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 37c440a5c626016ebdb75703a2be63c9a1a2b560
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567586"
---
# <a name="fa_balance-er-function"></a><span data-ttu-id="cae88-103">ER-funktionen FA_BALANCE</span><span class="sxs-lookup"><span data-stu-id="cae88-103">FA_BALANCE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cae88-104">Funktionen `FA_BALANCE` returnerer en *Container (post)*-værdi, der består af data for anlægsaktivsaldoen for den angivne anlægsaktivvare, værdimodelkode, rapporteringsår og rapporteringsdato.</span><span class="sxs-lookup"><span data-stu-id="cae88-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae88-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="cae88-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="cae88-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="cae88-106">Arguments</span></span>

<span data-ttu-id="cae88-107">`fixed asset code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="cae88-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="cae88-108">En *Streng*-værdi, der repræsenterer koden for en anlægsaktivvare, som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="cae88-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="cae88-109">`value model code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="cae88-109">`value model code`: *String*</span></span>

<span data-ttu-id="cae88-110">En *Streng*-værdi, der repræsenterer koden for en værdimodel, som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="cae88-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="cae88-111">`reporting year`: *Fasttekstværdi*</span><span class="sxs-lookup"><span data-stu-id="cae88-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="cae88-112">En fasttekstværdi for programfasttekstgen **AssetYear**, der definerer en periode for saldoberegningen.</span><span class="sxs-lookup"><span data-stu-id="cae88-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="cae88-113">`reporting date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="cae88-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="cae88-114">En *Dato*-værdi, der definerer en dato for saldoberegningen.</span><span class="sxs-lookup"><span data-stu-id="cae88-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="cae88-115">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="cae88-115">Return values</span></span>

<span data-ttu-id="cae88-116">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="cae88-116">*Container (record)*</span></span>

<span data-ttu-id="cae88-117">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="cae88-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="cae88-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="cae88-118">Example</span></span>

<span data-ttu-id="cae88-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returnerer den datacontainer med saldi for anlægsaktivet **COMP-000001**, som er blevet forbedredt for værdimodellen **Aktuel** for den aktuelle programsessionsdato.</span><span class="sxs-lookup"><span data-stu-id="cae88-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cae88-120">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="cae88-120">Additional resources</span></span>

[<span data-ttu-id="cae88-121">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="cae88-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]