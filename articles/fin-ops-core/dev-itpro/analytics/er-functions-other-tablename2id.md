---
title: ER-funktionen TABLENAME2ID
description: Dette emne indeholder oplysninger om, hvordan funktionen TABLENAME2ID til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 49370af4ebb7552dd3aff4512890fd93fa67c72d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563264"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="81bdd-103">ER-funktionen TABLENAME2ID</span><span class="sxs-lookup"><span data-stu-id="81bdd-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81bdd-104">Funktionen `TABLENAME2ID` returnerer en numerisk gengivelse af tabel-ID'et for det angivne tabelnavn som en værdi angivet som et *Heltal*.</span><span class="sxs-lookup"><span data-stu-id="81bdd-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="81bdd-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="81bdd-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="81bdd-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="81bdd-106">Arguments</span></span>

<span data-ttu-id="81bdd-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="81bdd-107">`text`: *String*</span></span>

<span data-ttu-id="81bdd-108">En tekstværdi, der repræsenterer et gyldigt tabelnavn.</span><span class="sxs-lookup"><span data-stu-id="81bdd-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="81bdd-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="81bdd-109">Return values</span></span>

<span data-ttu-id="81bdd-110">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="81bdd-110">*Integer*</span></span>

<span data-ttu-id="81bdd-111">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="81bdd-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="81bdd-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="81bdd-112">Usage notes</span></span>

<span data-ttu-id="81bdd-113">Udførelse af denne funktion kan have forskellige resultater i forskellige forekomster af Microsoft Dynamics 365 Finance, selvom det samme firmanavn bruges.</span><span class="sxs-lookup"><span data-stu-id="81bdd-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="81bdd-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="81bdd-114">Example</span></span>

<span data-ttu-id="81bdd-115">`TABLENAME2ID ("Intrastat")` returnerer **1510**.</span><span class="sxs-lookup"><span data-stu-id="81bdd-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81bdd-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="81bdd-116">Additional resources</span></span>

[<span data-ttu-id="81bdd-117">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="81bdd-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]