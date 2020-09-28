---
title: ER-funktionen UPPER
description: Dette emne indeholder oplysninger om, hvordan funktionen UPPER til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 672abf4938df7d96c0190bfd5325689b381e2764
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744329"
---
# <a name="upper-er-function"></a><span data-ttu-id="f234a-103">ER-funktionen UPPER</span><span class="sxs-lookup"><span data-stu-id="f234a-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f234a-104">Funktionen `UPPER` returnerer den angivne tekststreng som en *Streng*-værdi, når den er konverteret til blokbogstaver.</span><span class="sxs-lookup"><span data-stu-id="f234a-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="f234a-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f234a-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="f234a-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="f234a-106">Arguments</span></span>

<span data-ttu-id="f234a-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="f234a-107">`text`: *String*</span></span>

<span data-ttu-id="f234a-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="f234a-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f234a-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="f234a-109">Return values</span></span>

<span data-ttu-id="f234a-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="f234a-110">*String*</span></span>

<span data-ttu-id="f234a-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="f234a-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f234a-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="f234a-112">Example</span></span>

<span data-ttu-id="f234a-113">`UPPER ("Sample")` returnerer **"EKSEMPEL"**.</span><span class="sxs-lookup"><span data-stu-id="f234a-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f234a-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f234a-114">Additional resources</span></span>

[<span data-ttu-id="f234a-115">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="f234a-115">Text functions</span></span>](er-functions-category-text.md)
