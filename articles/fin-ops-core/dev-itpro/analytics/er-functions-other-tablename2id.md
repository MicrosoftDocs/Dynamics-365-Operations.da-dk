---
title: ER-funktionen TABLENAME2ID
description: Dette emne indeholder oplysninger om, hvordan funktionen TABLENAME2ID til elektronisk rapportering (ER) skal anvendes.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a68a8e1f4afa378ab446eae12bc90cdb3aba8b19
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681152"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="24227-103">ER-funktionen TABLENAME2ID</span><span class="sxs-lookup"><span data-stu-id="24227-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24227-104">Funktionen `TABLENAME2ID` returnerer en numerisk gengivelse af tabel-ID'et for det angivne tabelnavn som en værdi angivet som et *Heltal*.</span><span class="sxs-lookup"><span data-stu-id="24227-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="24227-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="24227-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="24227-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="24227-106">Arguments</span></span>

<span data-ttu-id="24227-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="24227-107">`text`: *String*</span></span>

<span data-ttu-id="24227-108">En tekstværdi, der repræsenterer et gyldigt tabelnavn.</span><span class="sxs-lookup"><span data-stu-id="24227-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="24227-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="24227-109">Return values</span></span>

<span data-ttu-id="24227-110">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="24227-110">*Integer*</span></span>

<span data-ttu-id="24227-111">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="24227-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="24227-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="24227-112">Usage notes</span></span>

<span data-ttu-id="24227-113">Udførelse af denne funktion kan have forskellige resultater i forskellige forekomster af Microsoft Dynamics 365 Finance, selvom det samme firmanavn bruges.</span><span class="sxs-lookup"><span data-stu-id="24227-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="24227-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="24227-114">Example</span></span>

<span data-ttu-id="24227-115">`TABLENAME2ID ("Intrastat")` returnerer **1510**.</span><span class="sxs-lookup"><span data-stu-id="24227-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24227-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="24227-116">Additional resources</span></span>

[<span data-ttu-id="24227-117">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="24227-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
