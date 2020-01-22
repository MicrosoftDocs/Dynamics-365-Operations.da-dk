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
ms.openlocfilehash: a60bc948ff6223b6e3acccd0ba40bf64f238aac2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917390"
---
# <span data-ttu-id="ca09c-103"><a name="EMPTYLIST">ER-funktionen EMPTYLIST</a></span><span class="sxs-lookup"><span data-stu-id="ca09c-103"><a name="EMPTYLIST">EMPTYLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca09c-104">Funktionen `EMPTYLIST` returnerer en tom *Postliste*-værdi ved hjælp af den angivne liste som kilde til listestrukturen.</span><span class="sxs-lookup"><span data-stu-id="ca09c-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca09c-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="ca09c-105">Syntax</span></span>

```
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="ca09c-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="ca09c-106">Arguments</span></span>

<span data-ttu-id="ca09c-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="ca09c-107">`list`: *Record list*</span></span>

<span data-ttu-id="ca09c-108">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="ca09c-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ca09c-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="ca09c-109">Return values</span></span>

<span data-ttu-id="ca09c-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="ca09c-110">*Record list*</span></span>

<span data-ttu-id="ca09c-111">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="ca09c-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="ca09c-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ca09c-112">Example</span></span>

<span data-ttu-id="ca09c-113">`EMPTYLIST (SPLIT ("abc", 1))` returnerer en ny tom liste, der har samme struktur som den liste, der er returneret af den anvendte `SPLIT`-funktion.</span><span class="sxs-lookup"><span data-stu-id="ca09c-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ca09c-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ca09c-114">Additional resources</span></span>

[<span data-ttu-id="ca09c-115">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="ca09c-115">List functions</span></span>](er-functions-category-list.md)
