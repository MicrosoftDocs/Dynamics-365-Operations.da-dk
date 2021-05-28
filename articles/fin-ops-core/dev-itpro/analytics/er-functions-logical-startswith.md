---
title: STARTSWITH ER-funktion
description: Dette emne indeholder oplysninger om, hvordan funktionen STARTSWITH elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 50883bb604d2d1f2947545ce27fa02099e70b0e6
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048836"
---
# <a name="startswith-er-function"></a><span data-ttu-id="87bb8-103">STARTSWITH ER-funktion</span><span class="sxs-lookup"><span data-stu-id="87bb8-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87bb8-104">Funktionen `STARTSWITH` bestemmer, om det angivne input starter med den angivne tekst.</span><span class="sxs-lookup"><span data-stu-id="87bb8-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="87bb8-105">Den returnerer en *Boolesk værdi* for **TRUE**, hvis det angivne input starter med den angivne tekst.</span><span class="sxs-lookup"><span data-stu-id="87bb8-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="87bb8-106">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="87bb8-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="87bb8-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="87bb8-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="87bb8-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="87bb8-108">Arguments</span></span>

<span data-ttu-id="87bb8-109">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="87bb8-109">`input`: *String*</span></span>

<span data-ttu-id="87bb8-110">Den gyldige sti til en vare med en datakilde af *strengtypen* eller en strengkonstant, hvis værdi kan starte med det andet argument.</span><span class="sxs-lookup"><span data-stu-id="87bb8-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="87bb8-111">`start text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="87bb8-111">`start text`: *String*</span></span>

<span data-ttu-id="87bb8-112">Den gyldige sti til en vare med en datakilde af *strengtypen* eller en strengkonstant, hvis værdi kan starte med det første argument.</span><span class="sxs-lookup"><span data-stu-id="87bb8-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="87bb8-113">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="87bb8-113">Return values</span></span>

<span data-ttu-id="87bb8-114">*Boolesk*</span><span class="sxs-lookup"><span data-stu-id="87bb8-114">*Boolean*</span></span>

<span data-ttu-id="87bb8-115">Den resulterende *Booleske* værdi.</span><span class="sxs-lookup"><span data-stu-id="87bb8-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="87bb8-116">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="87bb8-116">Usage notes</span></span>

<span data-ttu-id="87bb8-117">Denne funktion kan kun bruges til at angive et betingelsesudtryk for funktionen [FILTER](er-functions-list-filter.md), når den relevante tilknytning er konfigureret i [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) til at få adgang til [Microsoft Dataverse](/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="87bb8-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="87bb8-118">Ellers sker der en undtagelse på designtid.</span><span class="sxs-lookup"><span data-stu-id="87bb8-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="87bb8-119">Den meddelelse, du modtager, anbefaler, at du bruger funktionen [WHERE](er-functions-list-where.md) i stedet for funktionen `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="87bb8-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="87bb8-120">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="87bb8-120">Example 1</span></span>

<span data-ttu-id="87bb8-121">Udtrykket returnerer `STARTSWITH ("abc", "d")` **FALSE**, mens udtrykket `STARTSWITH ("abc", "A")` returnerer **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="87bb8-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="87bb8-122">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="87bb8-122">Example 2</span></span>

<span data-ttu-id="87bb8-123">Udtrykket `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returnerer **TRUE**, hvis værdien i feltet **Adresse** i datakilden **model** starter med strengen **123 Coffee Street**.</span><span class="sxs-lookup"><span data-stu-id="87bb8-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="87bb8-124">Ellers returneres **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="87bb8-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87bb8-125">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="87bb8-125">Additional resources</span></span>

[<span data-ttu-id="87bb8-126">Logiske funktioner</span><span class="sxs-lookup"><span data-stu-id="87bb8-126">Logical functions</span></span>](er-functions-category-logical.md)
