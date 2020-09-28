---
title: ER-funktionen CONVERTCURRENCY
description: Dette emne indeholder oplysninger om, hvordan funktionen CONVERTCURRENCY til elektronisk rapportering (ER) skal anvendes.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae6e0069c6e9227d4cf1045eeebbb825a2f943c3
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744305"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="8b9c3-103">ER-funktionen CONVERTCURRENCY</span><span class="sxs-lookup"><span data-stu-id="8b9c3-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b9c3-104">Funktionen `CONVERTCURRENCY` returnerer en *Reel* værdi, som repræsenterer resultatet af konverteringen af det angivne pengebeløb fra den angivne kildevaluta til den angivne målvaluta ved hjælp af indstillingerne for det angivne firma på den angivne dato.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b9c3-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="8b9c3-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="8b9c3-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="8b9c3-106">Arguments</span></span>

<span data-ttu-id="8b9c3-107">`amount`: *Heltal* eller *Reel*</span><span class="sxs-lookup"><span data-stu-id="8b9c3-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="8b9c3-108">En numerisk værdi, der repræsenterer det pengebeløb, der skal konverteres.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="8b9c3-109">`source currency`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="8b9c3-109">`source currency`: *String*</span></span>

<span data-ttu-id="8b9c3-110">Koden for kildevalutaen</span><span class="sxs-lookup"><span data-stu-id="8b9c3-110">The code of the source currency.</span></span>

<span data-ttu-id="8b9c3-111">`target currency`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="8b9c3-111">`target currency`: *String*</span></span>

<span data-ttu-id="8b9c3-112">Koden for målvalutaen</span><span class="sxs-lookup"><span data-stu-id="8b9c3-112">The code of the target currency.</span></span>

<span data-ttu-id="8b9c3-113">`date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="8b9c3-113">`date`: *Date*</span></span>

<span data-ttu-id="8b9c3-114">En *Dato*-værdi, der repræsenterer den dato, der bruges til at bestemme valutakursen for konverteringen.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="8b9c3-115">`company`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="8b9c3-115">`company`: *String*</span></span>

<span data-ttu-id="8b9c3-116">En *Streng*-værdi, der repræsenterer koden for et firma, der leverer de indstillinger, der bruges til konverteringen.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="8b9c3-117">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="8b9c3-117">Return values</span></span>

<span data-ttu-id="8b9c3-118">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="8b9c3-118">*Real*</span></span>

<span data-ttu-id="8b9c3-119">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="8b9c3-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="8b9c3-120">Example</span></span>

<span data-ttu-id="8b9c3-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returnerer hvad der svarer til én euro i amerikanske dollar på den aktuelle sessionsdato, baseret på indstillingerne for **DEMF**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8b9c3-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8b9c3-122">Additional resources</span></span>

[<span data-ttu-id="8b9c3-123">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="8b9c3-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
