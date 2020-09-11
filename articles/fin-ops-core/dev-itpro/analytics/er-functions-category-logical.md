---
title: Liste over ER-funktioner i kategorien logisk
description: Dette emne indeholder oplysninger om de logiske funktioner, der understøttes i elektronisk rapportering (ER).
author: NickSelin
manager: kfend
ms.date: 08/19/2020
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
ms.openlocfilehash: e622778c60646e5cc84cd6e23a5d4954a0fe0bb3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705089"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="aad04-103">Liste over ER-funktioner i kategorien logisk</span><span class="sxs-lookup"><span data-stu-id="aad04-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aad04-104">Logiske funktioner til elektronisk rapportering (ER) kan bruges til at arbejde med logiske værdier for at udføre mere end én sammenligning i et enkelt udtryk eller afprøve flere betingelser.</span><span class="sxs-lookup"><span data-stu-id="aad04-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="aad04-105">Dette emne indeholder en oversigt over disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="aad04-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="aad04-106">Liste med understøttede funktioner</span><span class="sxs-lookup"><span data-stu-id="aad04-106">List of supported functions</span></span>

| <span data-ttu-id="aad04-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="aad04-107">Function</span></span> | <span data-ttu-id="aad04-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="aad04-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="aad04-109">Og</span><span class="sxs-lookup"><span data-stu-id="aad04-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="aad04-110">Denne funktion returnerer en *Boolesk* værdi som værende **SAND**, hvis alle de angivne betingelser er opfyldte.</span><span class="sxs-lookup"><span data-stu-id="aad04-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="aad04-111">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="aad04-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="aad04-112">Sag</span><span class="sxs-lookup"><span data-stu-id="aad04-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="aad04-113">Denne funktion evaluerer værdien af det angivne udtryk i forhold til de angivne alternative indstillinger og returnerer resultatet af den første indstilling, der er lig med værdien af det angivne udtryk.</span><span class="sxs-lookup"><span data-stu-id="aad04-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="aad04-114">Ellers returneres et valgfrit standardresultat, hvis der er angivet et standardresultat som det sidste argument i den kaldte funktion, hvor der ikke er foretaget en forudgående indstilling.</span><span class="sxs-lookup"><span data-stu-id="aad04-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="aad04-115">Den returnerede værdi kan være en værdi for en hvilken som helst af de understøttede datatyper.</span><span class="sxs-lookup"><span data-stu-id="aad04-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="aad04-116">Hvis</span><span class="sxs-lookup"><span data-stu-id="aad04-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="aad04-117">Denne funktion returnerer den først angivne værdi, hvis den angivne betingelse er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="aad04-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="aad04-118">Ellers returneres den anden angivne værdi.</span><span class="sxs-lookup"><span data-stu-id="aad04-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="aad04-119">Den returnerede værdi kan være en værdi for en hvilken som helst af de understøttede datatyper.</span><span class="sxs-lookup"><span data-stu-id="aad04-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="aad04-120">Negeret</span><span class="sxs-lookup"><span data-stu-id="aad04-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="aad04-121">Denne funktion returnerer den omvendte logiske værdi af den angivne betingelse som en *Boolesk* værdi.</span><span class="sxs-lookup"><span data-stu-id="aad04-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="aad04-122">Eller</span><span class="sxs-lookup"><span data-stu-id="aad04-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="aad04-123">Denne funktion returnerer en *Boolesk* værdi som værende **FALSK**, hvis alle de angivne betingelser ikke er opfyldte.</span><span class="sxs-lookup"><span data-stu-id="aad04-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="aad04-124">Hvis en eller flere af de angivne betingelser er opfyldte, returnerer denne funktion en *Boolesk* værdi som værende **SAND**.</span><span class="sxs-lookup"><span data-stu-id="aad04-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="aad04-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="aad04-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="aad04-126">Denne funktion afgør, hvorvidt det angivne input svarer til en værdi for et angivet element på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="aad04-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="aad04-127">Den returnerer en *Boolesk* værdi som værende **SANDT**, hvis det angivne input svarer til resultatet af kørslen med det angivne udtryk for mindst én post på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="aad04-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="aad04-128">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="aad04-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="aad04-129">ValueInLarge</span><span class="sxs-lookup"><span data-stu-id="aad04-129">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="aad04-130">Denne funktion afgør, om det angivne input af typen *Int64* eller *Heltal* svarer til en værdi for et angivet element på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="aad04-130">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="aad04-131">Den returnerer en *Boolesk* værdi som værende **SANDT**, hvis det angivne input svarer til resultatet af kørslen med det angivne udtryk for mindst én post på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="aad04-131">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="aad04-132">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="aad04-132">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="aad04-133">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="aad04-133">Additional resources</span></span>

[<span data-ttu-id="aad04-134">Oversigt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="aad04-134">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="aad04-135">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="aad04-135">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="aad04-136">Formelsprog i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="aad04-136">Electronic reporting formula language</span></span>](er-formula-language.md)
