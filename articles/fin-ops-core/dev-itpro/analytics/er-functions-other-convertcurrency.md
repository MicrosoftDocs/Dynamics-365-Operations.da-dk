---
title: ER-funktionen CONVERTCURRENCY
description: Dette emne indeholder oplysninger om, hvordan funktionen CONVERTCURRENCY til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: fb8f7f28f5a9bb27402544efcffa6393238e38d8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744361"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="26547-103">ER-funktionen CONVERTCURRENCY</span><span class="sxs-lookup"><span data-stu-id="26547-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26547-104">Funktionen `CONVERTCURRENCY` returnerer en *Reel* værdi, som repræsenterer resultatet af konverteringen af det angivne pengebeløb fra den angivne kildevaluta til den angivne målvaluta ved hjælp af indstillingerne for det angivne firma på den angivne dato.</span><span class="sxs-lookup"><span data-stu-id="26547-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="26547-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="26547-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="26547-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="26547-106">Arguments</span></span>

<span data-ttu-id="26547-107">`amount`: *Heltal* eller *Reel*</span><span class="sxs-lookup"><span data-stu-id="26547-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="26547-108">En numerisk værdi, der repræsenterer det pengebeløb, der skal konverteres.</span><span class="sxs-lookup"><span data-stu-id="26547-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="26547-109">`source currency`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="26547-109">`source currency`: *String*</span></span>

<span data-ttu-id="26547-110">Koden for kildevalutaen</span><span class="sxs-lookup"><span data-stu-id="26547-110">The code of the source currency.</span></span>

<span data-ttu-id="26547-111">`target currency`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="26547-111">`target currency`: *String*</span></span>

<span data-ttu-id="26547-112">Koden for målvalutaen</span><span class="sxs-lookup"><span data-stu-id="26547-112">The code of the target currency.</span></span>

<span data-ttu-id="26547-113">`date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="26547-113">`date`: *Date*</span></span>

<span data-ttu-id="26547-114">En *Dato*-værdi, der repræsenterer den dato, der bruges til at bestemme valutakursen for konverteringen.</span><span class="sxs-lookup"><span data-stu-id="26547-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="26547-115">`company`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="26547-115">`company`: *String*</span></span>

<span data-ttu-id="26547-116">En *Streng*-værdi, der repræsenterer koden for et firma, der leverer de indstillinger, der bruges til konverteringen.</span><span class="sxs-lookup"><span data-stu-id="26547-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="26547-117">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="26547-117">Return values</span></span>

<span data-ttu-id="26547-118">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="26547-118">*Real*</span></span>

<span data-ttu-id="26547-119">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="26547-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="26547-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="26547-120">Example</span></span>

<span data-ttu-id="26547-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returnerer hvad der svarer til én euro i amerikanske dollar på den aktuelle sessionsdato, baseret på indstillingerne for **DEMF**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="26547-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26547-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="26547-122">Additional resources</span></span>

[<span data-ttu-id="26547-123">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="26547-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]