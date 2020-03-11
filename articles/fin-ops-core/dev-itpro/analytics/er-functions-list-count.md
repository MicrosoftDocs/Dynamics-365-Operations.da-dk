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
ms.openlocfilehash: 72d2ea1b26c295c97575a3c7a479ee4e06762424
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042199"
---
# <span data-ttu-id="8525b-103"><a name="COUNT">ER-funktionen COUNT</a></span><span class="sxs-lookup"><span data-stu-id="8525b-103"><a name="COUNT">COUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8525b-104">Funktionen `COUNT` returnerer en *Heltals*-værdi, der repræsenterer antallet af poster på den angivne liste, hvis listen ikke er tom.</span><span class="sxs-lookup"><span data-stu-id="8525b-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="8525b-105">Hvis listen er tom, returnerer denne funktion **0** (nul).</span><span class="sxs-lookup"><span data-stu-id="8525b-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="8525b-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="8525b-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="8525b-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="8525b-107">Arguments</span></span>

<span data-ttu-id="8525b-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="8525b-108">`list`: *Record list*</span></span>

<span data-ttu-id="8525b-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="8525b-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="8525b-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="8525b-110">Return values</span></span>

<span data-ttu-id="8525b-111">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="8525b-111">*Integer*</span></span>

<span data-ttu-id="8525b-112">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="8525b-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="8525b-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="8525b-113">Example</span></span>

<span data-ttu-id="8525b-114">`COUNT (SPLIT("abcd" , 3))` returnerer **2**, fordi den `SPLIT`-funktion, der bruges i dette eksempel, opretter en liste, der består af to poster.</span><span class="sxs-lookup"><span data-stu-id="8525b-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8525b-115">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8525b-115">Additional resources</span></span>

[<span data-ttu-id="8525b-116">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="8525b-116">List functions</span></span>](er-functions-category-list.md)
