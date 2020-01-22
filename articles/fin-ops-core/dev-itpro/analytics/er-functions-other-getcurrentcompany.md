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
ms.openlocfilehash: a0b4c93a4705cd0e382b9b6c7af1d199beeceabe
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915987"
---
# <span data-ttu-id="f6875-103"><a name="GETCURRENTCOMPANY">ER-funktionen GETCURRENTCOMPANY</a></span><span class="sxs-lookup"><span data-stu-id="f6875-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6875-104">Funktionen `GETCURRENTCOMPANY` returnerer en *Streng*-værdi, som repræsenterer koden for en juridisk enhed (firma), som en bruger i øjeblikket er logget på.</span><span class="sxs-lookup"><span data-stu-id="f6875-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6875-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f6875-105">Syntax</span></span>

```
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="f6875-106">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="f6875-106">Return values</span></span>

<span data-ttu-id="f6875-107">*Streng*</span><span class="sxs-lookup"><span data-stu-id="f6875-107">*String*</span></span>

<span data-ttu-id="f6875-108">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="f6875-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f6875-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="f6875-109">Example</span></span>

<span data-ttu-id="f6875-110">`GETCURRENTCOMPANY ()` returnerer **USMF** for en bruger, der er logget på firmaet **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="f6875-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f6875-111">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f6875-111">Additional resources</span></span>

[<span data-ttu-id="f6875-112">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="f6875-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
