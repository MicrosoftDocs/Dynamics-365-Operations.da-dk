---
title: ER-funktionen GETCURRENTCOMPANY
description: Dette emne indeholder oplysninger om, hvordan funktionen GETCURRENTCOMPANY til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: fcb5ef2f218a85bab25f830db583343504c46e98
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567538"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="9bd32-103">ER-funktionen GETCURRENTCOMPANY</span><span class="sxs-lookup"><span data-stu-id="9bd32-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bd32-104">Funktionen `GETCURRENTCOMPANY` returnerer en *Streng*-værdi, som repræsenterer koden for en juridisk enhed (firma), som en bruger i øjeblikket er logget på.</span><span class="sxs-lookup"><span data-stu-id="9bd32-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bd32-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="9bd32-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="9bd32-106">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="9bd32-106">Return values</span></span>

<span data-ttu-id="9bd32-107">*Streng*</span><span class="sxs-lookup"><span data-stu-id="9bd32-107">*String*</span></span>

<span data-ttu-id="9bd32-108">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="9bd32-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9bd32-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="9bd32-109">Example</span></span>

<span data-ttu-id="9bd32-110">`GETCURRENTCOMPANY ()` returnerer **USMF** for en bruger, der er logget på firmaet **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="9bd32-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9bd32-111">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9bd32-111">Additional resources</span></span>

[<span data-ttu-id="9bd32-112">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="9bd32-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]