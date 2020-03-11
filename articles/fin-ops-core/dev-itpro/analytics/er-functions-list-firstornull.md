---
title: ER-funktionen FIRSTORNULL
description: Dette emne beskriver, hvordan funktionen FIRSTORNULL til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 86c8a0ae21ffeb6268efbbd198f7c709c2ad54f6
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042107"
---
# <span data-ttu-id="afb19-103"><a name="FIRSTORNULL">ER-funktionen FIRSTORNULL</a></span><span class="sxs-lookup"><span data-stu-id="afb19-103"><a name="FIRSTORNULL">FIRSTORNULL ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afb19-104">Funktionen `FIRSTORNULL` returnerer den første post på den angivne liste som en *Container (post)*-værdi, hvis denne post ikke er tom.</span><span class="sxs-lookup"><span data-stu-id="afb19-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="afb19-105">Hvis posten er tom, returnerer denne funktion en nul *Container (post)*-værdi.</span><span class="sxs-lookup"><span data-stu-id="afb19-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="afb19-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="afb19-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="afb19-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="afb19-107">Arguments</span></span>

<span data-ttu-id="afb19-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="afb19-108">`list`: *Record list*</span></span>

<span data-ttu-id="afb19-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="afb19-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="afb19-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="afb19-110">Return values</span></span>

<span data-ttu-id="afb19-111">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="afb19-111">*Container (record)*</span></span>

<span data-ttu-id="afb19-112">Den resulterende postværdi.</span><span class="sxs-lookup"><span data-stu-id="afb19-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="afb19-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="afb19-113">Example</span></span>

<span data-ttu-id="afb19-114">Udtrykket `FIRSTORNULL(SPLIT("",1)).Value` returnerer en tom streng (**""**).</span><span class="sxs-lookup"><span data-stu-id="afb19-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="afb19-115">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="afb19-115">Additional resources</span></span>

[<span data-ttu-id="afb19-116">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="afb19-116">List functions</span></span>](er-functions-category-list.md)
