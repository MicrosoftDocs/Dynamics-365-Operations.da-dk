---
title: ER-funktionen TABLENAME2ID
description: Dette emne indeholder oplysninger om, hvordan funktionen TABLENAME2ID til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 0f94d00d9d40830d895e906ffbaa2a236f1efc43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746549"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="fc8a4-103">ER-funktionen TABLENAME2ID</span><span class="sxs-lookup"><span data-stu-id="fc8a4-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc8a4-104">Funktionen `TABLENAME2ID` returnerer en numerisk gengivelse af tabel-ID'et for det angivne tabelnavn som en værdi angivet som et *Heltal*.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc8a4-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="fc8a4-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="fc8a4-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="fc8a4-106">Arguments</span></span>

<span data-ttu-id="fc8a4-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="fc8a4-107">`text`: *String*</span></span>

<span data-ttu-id="fc8a4-108">En tekstværdi, der repræsenterer et gyldigt tabelnavn.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="fc8a4-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="fc8a4-109">Return values</span></span>

<span data-ttu-id="fc8a4-110">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="fc8a4-110">*Integer*</span></span>

<span data-ttu-id="fc8a4-111">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fc8a4-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="fc8a4-112">Usage notes</span></span>

<span data-ttu-id="fc8a4-113">Udførelse af denne funktion kan have forskellige resultater i forskellige forekomster af Microsoft Dynamics 365 Finance, selvom det samme firmanavn bruges.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="fc8a4-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fc8a4-114">Example</span></span>

<span data-ttu-id="fc8a4-115">`TABLENAME2ID ("Intrastat")` returnerer **1510**.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fc8a4-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="fc8a4-116">Additional resources</span></span>

[<span data-ttu-id="fc8a4-117">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="fc8a4-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]