---
title: ER-funktionen EMPTYLIST
description: Dette emne indeholder oplysninger om, hvordan funktionen EMPTYLIST til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 5fb991eb9ee08aeb418313eb782dbde7fa22b763
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042176"
---
# <span data-ttu-id="2aee7-103"><a name="EMPTYLIST">ER-funktionen EMPTYLIST</a></span><span class="sxs-lookup"><span data-stu-id="2aee7-103"><a name="EMPTYLIST">EMPTYLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2aee7-104">Funktionen `EMPTYLIST` returnerer en tom *Postliste*-værdi ved hjælp af den angivne liste som kilde til listestrukturen.</span><span class="sxs-lookup"><span data-stu-id="2aee7-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aee7-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="2aee7-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="2aee7-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="2aee7-106">Arguments</span></span>

<span data-ttu-id="2aee7-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="2aee7-107">`list`: *Record list*</span></span>

<span data-ttu-id="2aee7-108">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="2aee7-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="2aee7-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="2aee7-109">Return values</span></span>

<span data-ttu-id="2aee7-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="2aee7-110">*Record list*</span></span>

<span data-ttu-id="2aee7-111">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="2aee7-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="2aee7-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2aee7-112">Example</span></span>

<span data-ttu-id="2aee7-113">`EMPTYLIST (SPLIT ("abc", 1))` returnerer en ny tom liste, der har samme struktur som den liste, der er returneret af den anvendte `SPLIT`-funktion.</span><span class="sxs-lookup"><span data-stu-id="2aee7-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2aee7-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2aee7-114">Additional resources</span></span>

[<span data-ttu-id="2aee7-115">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="2aee7-115">List functions</span></span>](er-functions-category-list.md)
