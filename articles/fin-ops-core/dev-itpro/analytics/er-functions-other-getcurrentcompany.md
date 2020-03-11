---
title: ER-funktionen GETCURRENTCOMPANY
description: Dette emne indeholder oplysninger om, hvordan funktionen GETCURRENTCOMPANY til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: d91caff1a1b89e060a16833e53f3647208ed3826
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041417"
---
# <span data-ttu-id="16823-103"><a name="GETCURRENTCOMPANY">ER-funktionen GETCURRENTCOMPANY</a></span><span class="sxs-lookup"><span data-stu-id="16823-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16823-104">Funktionen `GETCURRENTCOMPANY` returnerer en *Streng*-værdi, som repræsenterer koden for en juridisk enhed (firma), som en bruger i øjeblikket er logget på.</span><span class="sxs-lookup"><span data-stu-id="16823-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="16823-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="16823-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="16823-106">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="16823-106">Return values</span></span>

<span data-ttu-id="16823-107">*Streng*</span><span class="sxs-lookup"><span data-stu-id="16823-107">*String*</span></span>

<span data-ttu-id="16823-108">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="16823-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="16823-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="16823-109">Example</span></span>

<span data-ttu-id="16823-110">`GETCURRENTCOMPANY ()` returnerer **USMF** for en bruger, der er logget på firmaet **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="16823-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16823-111">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="16823-111">Additional resources</span></span>

[<span data-ttu-id="16823-112">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="16823-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
