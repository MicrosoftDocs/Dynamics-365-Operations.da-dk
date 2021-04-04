---
title: ER-funktionen CHAR
description: Dette emne indeholder oplysninger om, hvordan funktionen CHAR til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: b008cf6ddf51d816a17e0fae1fa0db464adeabde
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563192"
---
# <a name="char-er-function"></a><span data-ttu-id="35e1c-103">ER-funktionen CHAR</span><span class="sxs-lookup"><span data-stu-id="35e1c-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35e1c-104">Funktionen `CHAR` returnerer en *Streng*-værdi, som er udtryk for et enkelt tegn, der refereres til af det angivne Unicode-nummer.</span><span class="sxs-lookup"><span data-stu-id="35e1c-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e1c-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="35e1c-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="35e1c-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="35e1c-106">Arguments</span></span>

<span data-ttu-id="35e1c-107">`number`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="35e1c-107">`number`: *Integer*</span></span>

<span data-ttu-id="35e1c-108">Et tal, der svarer til et forventet enkelt tegn.</span><span class="sxs-lookup"><span data-stu-id="35e1c-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="35e1c-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="35e1c-109">Return values</span></span>

<span data-ttu-id="35e1c-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="35e1c-110">*String*</span></span>

<span data-ttu-id="35e1c-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="35e1c-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="35e1c-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="35e1c-112">Usage notes</span></span>

<span data-ttu-id="35e1c-113">Den streng, som denne funktion returnerer, afhænger af den kodning, der er valgt i det overordnede **FIL**-formatelement.</span><span class="sxs-lookup"><span data-stu-id="35e1c-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="35e1c-114">Du kan finde en liste over understøttede kodninger under [Kodningsklasse](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="35e1c-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="35e1c-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="35e1c-115">Example</span></span>

<span data-ttu-id="35e1c-116">`CHAR (255)` returnerer **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="35e1c-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35e1c-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="35e1c-117">Additional resources</span></span>

[<span data-ttu-id="35e1c-118">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="35e1c-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]