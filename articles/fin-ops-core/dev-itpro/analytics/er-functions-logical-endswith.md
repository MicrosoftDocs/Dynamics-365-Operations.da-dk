---
title: ENDSWITH ER-funktion
description: Dette emne indeholder oplysninger om, hvordan funktionen ENDSWITH elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 2470bd8c75cf690d701957c4c79009659d61f7a5
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557505"
---
# <a name="endswith-er-function"></a><span data-ttu-id="605b5-103">ENDSWITH ER-funktion</span><span class="sxs-lookup"><span data-stu-id="605b5-103">ENDSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="605b5-104">Funktionen `ENDSWITH` bestemmer, om det angivne input slutter med den angivne tekst.</span><span class="sxs-lookup"><span data-stu-id="605b5-104">The `ENDSWITH` function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="605b5-105">Den returnerer en *Boolesk værdi* for **TRUE**, hvis det angivne input slutter med den angivne tekst.</span><span class="sxs-lookup"><span data-stu-id="605b5-105">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="605b5-106">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="605b5-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="605b5-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="605b5-107">Syntax</span></span>

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a><span data-ttu-id="605b5-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="605b5-108">Arguments</span></span>

<span data-ttu-id="605b5-109">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="605b5-109">`input`: *String*</span></span>

<span data-ttu-id="605b5-110">Den gyldige sti til en vare med en datakilde af *strengtypen* eller en strengkonstant, hvis værdi kan slutte med det andet argument.</span><span class="sxs-lookup"><span data-stu-id="605b5-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might end with the second argument.</span></span>

<span data-ttu-id="605b5-111">`start text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="605b5-111">`start text`: *String*</span></span>

<span data-ttu-id="605b5-112">Den gyldige sti til en vare med en datakilde af *strengtypen* eller en strengkonstant, hvis værdi kan slutte med det første argument.</span><span class="sxs-lookup"><span data-stu-id="605b5-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the end of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="605b5-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="605b5-113">Return values</span></span>

<span data-ttu-id="605b5-114">*Boolesk*</span><span class="sxs-lookup"><span data-stu-id="605b5-114">*Boolean*</span></span>

<span data-ttu-id="605b5-115">Den resulterende *Booleske* værdi.</span><span class="sxs-lookup"><span data-stu-id="605b5-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="605b5-116">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="605b5-116">Usage notes</span></span>

<span data-ttu-id="605b5-117">Denne funktion kan kun bruges til at angive et betingelsesudtryk for funktionen [FILTER](er-functions-list-filter.md), når den relevante tilknytning er konfigureret i [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) til at få adgang til [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="605b5-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="605b5-118">Ellers sker der en undtagelse på designtid.</span><span class="sxs-lookup"><span data-stu-id="605b5-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="605b5-119">Den meddelelse, du modtager, anbefaler, at du bruger funktionen [WHERE](er-functions-list-where.md) i stedet for funktionen `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="605b5-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="605b5-120">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="605b5-120">Example 1</span></span>

<span data-ttu-id="605b5-121">Udtrykket returnerer `ENDSWITH ("abc", "d")` **FALSE**, mens udtrykket `ENDSWITH ("abc", "C")` returnerer **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="605b5-121">The expression `ENDSWITH ("abc", "d")` returns **FALSE**, whereas the expression `ENDSWITH ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="605b5-122">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="605b5-122">Example 2</span></span>

<span data-ttu-id="605b5-123">Udtrykket `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returnerer **TRUE**, hvis værdien i feltet **Adresse** i datakilden **model** slutter med strengen **USA**.</span><span class="sxs-lookup"><span data-stu-id="605b5-123">The expression `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returns **TRUE** if the value of the **Address** field of the **model** data source ends with the string **USA**.</span></span> <span data-ttu-id="605b5-124">Ellers returneres **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="605b5-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="605b5-125">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="605b5-125">Additional resources</span></span>

[<span data-ttu-id="605b5-126">Logiske funktioner</span><span class="sxs-lookup"><span data-stu-id="605b5-126">Logical functions</span></span>](er-functions-category-logical.md)
