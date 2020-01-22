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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77d889f75f38b3c07855a96bf65f1456ac2f42e2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915803"
---
# <span data-ttu-id="96ee3-103"><a name="TABLENAME2ID">ER-funktionen TABLENAME2ID</a></span><span class="sxs-lookup"><span data-stu-id="96ee3-103"><a name="TABLENAME2ID">TABLENAME2ID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96ee3-104">Funktionen `TABLENAME2ID` returnerer en numerisk gengivelse af tabel-ID'et for det angivne tabelnavn som en værdi angivet som et *Heltal*.</span><span class="sxs-lookup"><span data-stu-id="96ee3-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="96ee3-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="96ee3-105">Syntax</span></span>

```
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="96ee3-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="96ee3-106">Arguments</span></span>

<span data-ttu-id="96ee3-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="96ee3-107">`text`: *String*</span></span>

<span data-ttu-id="96ee3-108">En tekstværdi, der repræsenterer et gyldigt tabelnavn.</span><span class="sxs-lookup"><span data-stu-id="96ee3-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="96ee3-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="96ee3-109">Return values</span></span>

<span data-ttu-id="96ee3-110">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="96ee3-110">*Integer*</span></span>

<span data-ttu-id="96ee3-111">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="96ee3-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="96ee3-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="96ee3-112">Usage notes</span></span>

<span data-ttu-id="96ee3-113">Udførelse af denne funktion kan have forskellige resultater i forskellige forekomster af Microsoft Dynamics 365 Finance, selvom det samme firmanavn bruges.</span><span class="sxs-lookup"><span data-stu-id="96ee3-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="96ee3-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="96ee3-114">Example</span></span>

<span data-ttu-id="96ee3-115">`TABLENAME2ID ("Intrastat")` returnerer **1510**.</span><span class="sxs-lookup"><span data-stu-id="96ee3-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96ee3-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="96ee3-116">Additional resources</span></span>

[<span data-ttu-id="96ee3-117">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="96ee3-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
