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
ms.openlocfilehash: 7e3c164c6d54d8387eed5018219da5fd82c765c8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744114"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="78ae4-103">ER-funktionen GETCURRENTCOMPANY</span><span class="sxs-lookup"><span data-stu-id="78ae4-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78ae4-104">Funktionen `GETCURRENTCOMPANY` returnerer en *Streng*-værdi, som repræsenterer koden for en juridisk enhed (firma), som en bruger i øjeblikket er logget på.</span><span class="sxs-lookup"><span data-stu-id="78ae4-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="78ae4-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="78ae4-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="78ae4-106">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="78ae4-106">Return values</span></span>

<span data-ttu-id="78ae4-107">*Streng*</span><span class="sxs-lookup"><span data-stu-id="78ae4-107">*String*</span></span>

<span data-ttu-id="78ae4-108">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="78ae4-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="78ae4-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78ae4-109">Example</span></span>

<span data-ttu-id="78ae4-110">`GETCURRENTCOMPANY ()` returnerer **USMF** for en bruger, der er logget på firmaet **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="78ae4-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="78ae4-111">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="78ae4-111">Additional resources</span></span>

[<span data-ttu-id="78ae4-112">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="78ae4-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
