---
title: ER-funktionen FIRST
description: Dette emne indeholder oplysninger om, hvordan funktionen FIRST til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: d30c8481866ccf3f7080197b37586a0460a4ad2c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746573"
---
# <a name="first-er-function"></a><span data-ttu-id="9cb17-103">ER-funktionen FIRST</span><span class="sxs-lookup"><span data-stu-id="9cb17-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9cb17-104">Funktionen `FIRST` returnerer den første post på den angivne liste som en *Container (post)*-værdi, hvis denne liste ikke er tom.</span><span class="sxs-lookup"><span data-stu-id="9cb17-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="9cb17-105">Hvis listen er tom, udløser denne funktion en undtagelse.</span><span class="sxs-lookup"><span data-stu-id="9cb17-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cb17-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="9cb17-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="9cb17-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="9cb17-107">Arguments</span></span>

<span data-ttu-id="9cb17-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="9cb17-108">`list`: *Record list*</span></span>

<span data-ttu-id="9cb17-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="9cb17-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="9cb17-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="9cb17-110">Return values</span></span>

<span data-ttu-id="9cb17-111">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="9cb17-111">*Container (record)*</span></span>

<span data-ttu-id="9cb17-112">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="9cb17-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="9cb17-113">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="9cb17-113">Example 1</span></span>

<span data-ttu-id="9cb17-114">Udtrykket `FIRST(SPLIT("ABC",1)).Value` returnerer tekstværdien **"A"**.</span><span class="sxs-lookup"><span data-stu-id="9cb17-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="9cb17-115">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="9cb17-115">Example 2</span></span>

<span data-ttu-id="9cb17-116">Udtrykket `FIRST(SPLIT("",1)).Value` udløser en undtagelse under kørslen.</span><span class="sxs-lookup"><span data-stu-id="9cb17-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9cb17-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9cb17-117">Additional resources</span></span>

[<span data-ttu-id="9cb17-118">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="9cb17-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]