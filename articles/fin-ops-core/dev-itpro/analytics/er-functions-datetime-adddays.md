---
title: ER-funktionen ADDDAYS
description: Dette emne indeholder oplysninger om, hvordan funktionen ADDDAYS til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 998cf2c0dac67040814d4a32e433b465ec51f88c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743369"
---
# <a name="adddays-er-function"></a><span data-ttu-id="733af-103">ER-funktionen ADDDAYS</span><span class="sxs-lookup"><span data-stu-id="733af-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="733af-104">Funktionen `ADDDAYS` beregner en værdi med *DatoKlokkeslæt*, der er det angivne antal dage før eller efter en angivet startdato.</span><span class="sxs-lookup"><span data-stu-id="733af-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="733af-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="733af-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="733af-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="733af-106">Arguments</span></span>

<span data-ttu-id="733af-107">`datetime`: *DatoKlokkeslæt*</span><span class="sxs-lookup"><span data-stu-id="733af-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="733af-108">En dato-/klokkeslætsværdi, der repræsenterer startdatoen.</span><span class="sxs-lookup"><span data-stu-id="733af-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="733af-109">`days`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="733af-109">`days`: *Integer*</span></span>

<span data-ttu-id="733af-110">Antallet af dage inden eller efter `datetime`.</span><span class="sxs-lookup"><span data-stu-id="733af-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="733af-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="733af-111">Return values</span></span>

<span data-ttu-id="733af-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="733af-112">*DateTime*</span></span>

<span data-ttu-id="733af-113">Den returnerede dato-/klokkeslætsværdi.</span><span class="sxs-lookup"><span data-stu-id="733af-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="733af-114">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="733af-114">Usage notes</span></span>

<span data-ttu-id="733af-115">En positiv værdi for `days` leverer en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="733af-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="733af-116">En negativ værdi giver en tidligere dato.</span><span class="sxs-lookup"><span data-stu-id="733af-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="733af-117">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="733af-117">Example 1</span></span>

<span data-ttu-id="733af-118">`ADDDAYS (NOW(), 7)` returnerer datoen og klokkeslættet syv dage ud i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="733af-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="733af-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="733af-119">Example 2</span></span>

<span data-ttu-id="733af-120">`ADDDAYS (NOW(), -3)` returnerer datoen og klokkeslættet tre dage før.</span><span class="sxs-lookup"><span data-stu-id="733af-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="733af-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="733af-121">Additional resources</span></span>

[<span data-ttu-id="733af-122">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="733af-122">Date and time functions</span></span>](er-functions-category-datetime.md)
