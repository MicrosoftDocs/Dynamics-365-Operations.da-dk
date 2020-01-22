---
title: ER-funktionen COUNT
description: Dette emne indeholder oplysninger om, hvordan funktionen COUNT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 2d29b82a8c3b108f7651e6d593cb17e7ec8ca872
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916240"
---
# <span data-ttu-id="3b9c7-103"><a name="COUNT">ER-funktionen COUNT</a></span><span class="sxs-lookup"><span data-stu-id="3b9c7-103"><a name="COUNT">COUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b9c7-104">Funktionen `COUNT` returnerer en *Heltals*-værdi, der repræsenterer antallet af poster på den angivne liste, hvis listen ikke er tom.</span><span class="sxs-lookup"><span data-stu-id="3b9c7-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="3b9c7-105">Hvis listen er tom, returnerer denne funktion **0** (nul).</span><span class="sxs-lookup"><span data-stu-id="3b9c7-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b9c7-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="3b9c7-106">Syntax</span></span>

```
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="3b9c7-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="3b9c7-107">Arguments</span></span>

<span data-ttu-id="3b9c7-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="3b9c7-108">`list`: *Record list*</span></span>

<span data-ttu-id="3b9c7-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="3b9c7-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="3b9c7-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="3b9c7-110">Return values</span></span>

<span data-ttu-id="3b9c7-111">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="3b9c7-111">*Integer*</span></span>

<span data-ttu-id="3b9c7-112">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="3b9c7-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="3b9c7-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="3b9c7-113">Example</span></span>

<span data-ttu-id="3b9c7-114">`COUNT (SPLIT("abcd" , 3))` returnerer **2**, fordi den `SPLIT`-funktion, der bruges i dette eksempel, opretter en liste, der består af to poster.</span><span class="sxs-lookup"><span data-stu-id="3b9c7-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b9c7-115">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3b9c7-115">Additional resources</span></span>

[<span data-ttu-id="3b9c7-116">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="3b9c7-116">List functions</span></span>](er-functions-category-list.md)
