---
title: ER-funktionen CHAR
description: Dette emne indeholder oplysninger om, hvordan funktionen CHAR til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: d42afcf97690351763138fd9e16265aa104a6bc4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915734"
---
# <span data-ttu-id="8c8e0-103"><a name="CHAR">ER-funktionen CHAR</a></span><span class="sxs-lookup"><span data-stu-id="8c8e0-103"><a name="CHAR">CHAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c8e0-104">Funktionen `CHAR` returnerer en *Streng*-værdi, som er udtryk for et enkelt tegn, der refereres til af det angivne Unicode-nummer.</span><span class="sxs-lookup"><span data-stu-id="8c8e0-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c8e0-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="8c8e0-105">Syntax</span></span>

```
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="8c8e0-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="8c8e0-106">Arguments</span></span>

<span data-ttu-id="8c8e0-107">`number`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="8c8e0-107">`number`: *Integer*</span></span>

<span data-ttu-id="8c8e0-108">Et tal, der svarer til et forventet enkelt tegn.</span><span class="sxs-lookup"><span data-stu-id="8c8e0-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="8c8e0-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="8c8e0-109">Return values</span></span>

<span data-ttu-id="8c8e0-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="8c8e0-110">*String*</span></span>

<span data-ttu-id="8c8e0-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="8c8e0-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8c8e0-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="8c8e0-112">Usage notes</span></span>

<span data-ttu-id="8c8e0-113">Den streng, som denne funktion returnerer, afhænger af den kodning, der er valgt i det overordnede **FIL**-formatelement.</span><span class="sxs-lookup"><span data-stu-id="8c8e0-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="8c8e0-114">Du kan finde en liste over understøttede kodninger under [Kodningsklasse](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="8c8e0-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="8c8e0-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="8c8e0-115">Example</span></span>

<span data-ttu-id="8c8e0-116">`CHAR (255)` returnerer **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="8c8e0-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8c8e0-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8c8e0-117">Additional resources</span></span>

[<span data-ttu-id="8c8e0-118">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="8c8e0-118">Text functions</span></span>](er-functions-category-text.md)
